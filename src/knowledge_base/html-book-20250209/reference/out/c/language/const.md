# const type qualifier

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

 Declarations

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Pointer | | | | |
| Array | | | | |
| enum | | | | |
| struct | | | | |
| union | | | | |
| Bit-field | | | | |
| Atomic types (C11) | | | | |
| ****const**** | | | | |
| constexpr(C23) | | | | |
| volatile | | | | |
| restrict(C99) | | | | |
| Alignment specifiers | | | | |
| Storage duration and linkage | | | | |
| External and tentative definitions | | | | |
| typedef | | | | |
| Static assertions | | | | |
| Attributes (C23) | | | | |

Each individual type in the C type system has several **qualified** versions of that type, corresponding to one, two, or all three of the `const`, `volatile`, and, for pointers to object types, `restrict` qualifiers. This page describes the effects of the `const` qualifier.

Objects declared with const-qualified types may be placed in read-only memory by the compiler, and if the address of a const object is never taken in a program, it may not be stored at all.

Any attempt to modify an object whose type is const-qualified results in undefined behavior.

```
const int n = 1; // object of const-qualified type
int* p = (int*)&n;
*p = 2; // undefined behavior

```

`const` semantics apply to lvalue expressions only; whenever a const lvalue expression is used in context that does not require an lvalue, its `const` qualifier is lost (note that volatile qualifier, if present, isn't lost).

The lvalue expressions that designate objects of const-qualified type and the lvalue expressions that designate objects of struct or union type with at least one member of const-qualified type (including members of recursively contained aggregates or unions), are not **modifiable lvalues**. In particular, they are not assignable:

```
const int n = 1; // object of const type
n = 2; // error: the type of n is const-qualified
 
int x = 2; // object of unqualified type
const int* p = &x;
*p = 3; // error: the type of the lvalue *p is const-qualified
 
struct {int a; const int b; } s1 = {.b=1}, s2 = {.b=2};
s1 = s2; // error: the type of s1 is unqualified, but it has a const member

```

A member of a const-qualified structure or union type acquires the qualification of the type it belongs to (both when accessed using the `.` operator or the `->` operator).

```
struct s { int i; const int ci; } s;
// the type of s.i is int, the type of s.ci is const int
const struct s cs;
// the types of cs.i and cs.ci are both const int

```

|  |  |
| --- | --- |
| If an array type is declared with the const type qualifier (through the use of typedef), the array type is not const-qualified, but its element type is. | (until C23) |
| An array type and its element type are always considered to be identically const-qualified. | (since C23) |

```
typedef int A[2][3];
const A a = {{4, 5, 6}, {7, 8, 9}}; // array of array of const int
int* pi = a[0]; // Error: a[0] has type const int*
void *unqual_ptr = a; // OK until C23; error since C23
// Notes: clang applies the rule in C++/C23 even in C89-C17 modes

```

If a function type is declared with the const type qualifier (through the use of typedef), the behavior is undefined.

|  |  |
| --- | --- |
| In a function declaration, the keyword `const` may appear inside the square brackets that are used to declare an array type of a function parameter. It qualifies the pointer type to which the array type is transformed.  The following two declarations declare the same function:   ```text void f(double x[const], const double y[const]); void f(double * const x, const double * const y); ``` | (since C99) |

|  |  |
| --- | --- |
| const-qualified compound literals do not necessarily designate distinct objects; they may share storage with other compound literals and with string literals that happen to have the same or overlapping representation.   ```text const int* p1 = (const int[]){1, 2, 3}; const int* p2 = (const int[]){2, 3, 4}; // the value of p2 may equal p1+1 _Bool b = "foobar" + 3 == (const char[]){"bar"}; // the value of b may be 1 ``` | (since C99) |

A pointer to a non-const type can be implicitly converted to a pointer to const-qualified version of the same or compatible type. The reverse conversion requires a cast expression.

```
int* p = 0;
const int* cp = p; // OK: adds qualifiers (int to const int)
p = cp; // Error: discards qualifiers (const int to int)
p = (int*)cp; // OK: cast

```

Note that pointer to pointer to `T` is not convertible to pointer to pointer to `const T`; for two types to be compatible, their qualifications must be identical.

```
char *p = 0;
const char **cpp = &p; // Error: char* and const char* are not compatible types
char * const *pcp = &p; // OK, adds qualifiers (char* to char*const)

```

### Keywords

const

### Notes

C adopted the **const** qualifier from C++, but unlike in C++, expressions of const-qualified type in C are not constant expressions; they may not be used as case labels or to initialize static and thread storage duration objects, enumerators, or bit-field sizes. When they are used as array sizes, the resulting arrays are VLAs.

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.7.3 Type qualifiers (p: 87-90)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.7.3 Type qualifiers (p: 121-123)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.7.3 Type qualifiers (p: 108-110)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 6.5.3 Type qualifiers

### See also

|  |  |
| --- | --- |
| C++ documentation for cv (`const` and `volatile`) type qualifiers | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/const&oldid=154456>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 July 2023, at 23:08.