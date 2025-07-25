# Function declarations

From cppreference.com
< c‎ | language
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 C language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Basic concepts | | | | |
| Keywords | | | | |
| Preprocessor | | | | |
| Statements | | | | |
| Expressions | | | | |
| Initialization | | | | |
| Declarations | | | | |
| Functions | | | | |
| Miscellaneous | | | | |
| History of C | | | | |
| Technical Specifications | | | | |

 Functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****function declaration**** | | | | |
| function definition | | | | |
| variadic arguments | | | | |
| inline(C99) | | | | |
| _Noreturn(C11) | | | | |

A function declaration introduces an identifier that designates a function and, optionally, specifies the types of the function parameters (the **prototype**). Function declarations (unlike definitions) may appear at block scope as well as file scope.

### Syntax

In the declaration grammar of a function declaration, the type-specifier sequence, possibly modified by the declarator, designates the **return type** (which may be any type other than array or function type), and the declarator has one of three forms:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| noptr-declarator `(` parameter-list `)` attr-spec-seq(optional) | (1) |  |
|  | | | | | | | | | |
| noptr-declarator `(` identifier-list `)` attr-spec-seq(optional) | (2) | (until C23) |
|  | | | | | | | | | |
| noptr-declarator `(` `)` attr-spec-seq(optional) | (3) |  |
|  | | | | | | | | | |

where

|  |  |  |
| --- | --- | --- |
| noptr-declarator | - | any declarator except unparenthesized pointer declarator. The identifier that is contained in this declarator is the identifier that becomes the function designator. |
| parameter-list | - | either the single keyword void or a comma-separated list of **parameters**, which may end with an ellipsis parameter |
| identifier-list | - | comma-separated list of identifiers, only possible if this declarator is used as part of old-style function definition |
| attr-spec-seq | - | (C23)an optional list of attributes, applied to the function type |

1) New-style (C89) function declaration. This declaration both introduces the function designator itself and also serves as a function prototype for any future function call expressions, forcing conversions from argument expressions to the declared parameter types and compile-time checks for the number of arguments.

```
int max(int a, int b); // declaration
int n = max(12.01, 3.14); // OK, conversion from double to int

```

2) (until C23) Old-style (K&R) function definition. This declaration does not introduce a prototype and any future function call expressions will perform default argument promotions and will invoke undefined behavior if the number of arguments doesn't match the number of parameters.

```
int max(a, b) 
    int a, b; // definition expects ints; the second call is undefined
{
    return a > b ? a : b;
}
 
int n = max(true, (char)'a'); // calls max with two int args (after promotions)
 
int n = max(12.01f, 3.14); // calls max with two double args (after promotions)

```

3) Non-prototype function declaration. This declaration does not introduce a prototype(until C23). A new style function declaration equivalent to the parameter-list void(since C23).

### Explanation

The return type of the function, determined by the type specifier in specifiers-and-qualifiers and possibly modified by the declarator as usual in declarations, must be a non-array object type or the type void. If the function declaration is not a definition, the return type can be incomplete. The return type cannot be cvr-qualified: any qualified return type is adjusted to its unqualified version for the purpose of constructing the function type.

```
void f(char *s);                    // return type is void
int sum(int a, int b);              // return type of sum is int.
int (*foo(const void *p))[3];       // return type is pointer to array of 3 int
 
double const bar(void);             // declares function of type double(void)
double (*barp)(void) = bar;         // OK: barp is a pointer to double(void)
double const (*barpc)(void) = barp; // OK: barpc is also a pointer to double(void)

```

Function declarators can be combined with other declarators as long as they can share their type specifiers and qualifiers

```
int f(void), *fip(), (*pfi)(), *ap[3]; // declares two functions and two objects
inline int g(int), n; // Error: inline qualifier is for functions only
typedef int array_t[3];
array_t a, h(); // Error: array type cannot be a return type for a function

```

If a function declaration appears outside of any function, the identifier it introduces has file scope and external linkage, unless `static` is used or an earlier static declaration is visible. If the declaration occurs inside another function, the identifier has block scope (and also either internal or external linkage).

```
int main(void)
{
    int f(int); // external linkage, block scope
    f(1); // definition needs to be available somewhere in the program
}

```

The parameters in a declaration that is not part of a function definition(until C23) do not need to be named:

```
int f(int, int); // declaration
// int f(int, int) { return 7; } // Error: parameters must be named in definitions
// This definition is allowed since C23

```

Each parameter in a parameter-list is a declaration that introduced a single variable, with the following additional properties:

- the identifier in the declarator is optional (except if this function declaration is part of a function definition)(until C23)

```
int f(int, double); // OK
int g(int a, double b); // also OK
// int f(int, double) { return 1; } // Error: definition must name parameters
// This definition is allowed since C23

```

- the only storage class specifier allowed for parameters is `register`, and it is ignored in function declarations that are not definitions

```
int f(static int x); // Error
int f(int [static 10]); // OK (array index static is not a storage class specifier)

```

- any parameter of array type is adjusted to the corresponding pointer type, which may be qualified if there are qualifiers between the square brackets of the array declarator(since C99)

```
int f(int[]); // declares int f(int*)
int g(const int[10]); // declares int g(const int*)
int h(int[const volatile]); // declares int h(int * const volatile)
int x(int[*]); // declares int x(int*)

```

- any parameter of function type is adjusted to the corresponding pointer type

```
int f(char g(double)); // declares int f(char (*g)(double))
int h(int(void)); // declares int h(int (*)(void))

```

- the parameter list may terminate with `, ...` or be `...`(since C23), see variadic functions for details.

```
int f(int, ...);

```

- parameters cannot have type void (but can have type pointer to void). The special parameter list that consists entirely of the keyword void is used to declare functions that take no parameters.

```
int f(void); // OK
int g(void x); // Error

```

- any identifier that appears in a parameter list that could be treated as a typedef name or as a parameter name is treated as a typedef name: int f(size_t, uintptr_t) is parsed as a new-style declarator for a function taking two unnamed parameters of type size_t and uintptr_t, not an old-style declarator that begins the definition of a function taking two parameters named "size_t" and "uintptr_t"
- parameters may have incomplete type and may use the VLA notation \* (except that in a function definition, the parameter types after array-to-pointer and function-to-pointer adjustment must be complete)

|  |  |
| --- | --- |
| Attribute specifier sequences can also applied to function parameters. | (since C23) |

See function call operator for other details on the mechanics of a function call and return for returning from functions.

### Notes

|  |  |
| --- | --- |
| Unlike in C++, the declarators f() and f(void) have different meaning: the declarator f(void) is a new-style (prototype) declarator that declares a function that takes no parameters. The declarator f() is a declarator that declares a function that takes **unspecified** number of parameters (unless used in a function definition)   ```text int f(void); // declaration: takes no parameters int g(); // declaration: takes unknown parameters   int main(void) {     f(1); // compile-time error     g(2); // undefined behavior }   int f(void) { return 1; } // actual definition int g(a,b,c,d) int a,b,c,d; { return 2; } // actual definition ``` | (until C23) |

Unlike in a function definition, the parameter list may be inherited from a typedef

```
typedef int p(int q, int r); // p is a function type int(int, int)
p f; // declares int f(int, int)

```

|  |  |
| --- | --- |
| In C89, specifiers-and-qualifiers was optional, and if omitted, the return type of the function defaulted to int (possibly amended by the declarator).   ```text *f() { // function returning int*    return NULL; } ``` | (until C99) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| DR 423 | C89 | the return type might be qualified | the return type is implicitly disqualified |

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.7.6.3 Function declarators (including prototypes) (p: 96-98)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.7.6.3 Function declarators (including prototypes) (p: 133-136)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.7.5.3 Function declarators (including prototypes) (p: 118-121)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.5.4.3 Function declarators (including prototypes)

### See also

|  |  |
| --- | --- |
| C++ documentation for Function declaration | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/function_declaration&oldid=162037>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 November 2023, at 10:09.