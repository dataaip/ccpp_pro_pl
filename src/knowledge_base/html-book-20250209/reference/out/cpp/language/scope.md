# Scope

From cppreference.com
< cpp‎ | language
C++

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Freestanding and hosted | | | | |
| Language | | | | |
| Standard library | | | | |
| Standard library headers | | | | |
| Named requirements | | | | |
| Feature test macros (C++20) | | | | |
| Language support library | | | | |
| Concepts library (C++20) | | | | |
| Diagnostics library | | | | |
| Memory management library | | | | |
| Metaprogramming library (C++11) | | | | |
| General utilities library | | | | |
| Containers library | | | | |
| Iterators library | | | | |
| Ranges library (C++20) | | | | |
| Algorithms library | | | | |
| Strings library | | | | |
| Text processing library | | | | |
| Numerics library | | | | |
| Date and time library | | | | |
| Input/output library | | | | |
| Filesystem library (C++17) | | | | |
| Concurrency support library (C++11) | | | | |
| Execution support library (C++26) | | | | |
| Technical specifications | | | | |
| Symbols index | | | | |
| External libraries | | | | |

C++ language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General topics | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Preprocessor | | | | | | Comments | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Keywords | | | | | | Escape sequences | | | | | |
| Flow control | | | | |
| Conditional execution statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | switch | | | | | |
| Iteration statements (loops) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | for | | | | | | range-`for` (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | while | | | | | | `do-while` | | | | | |
| Jump statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | continue - break | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | goto - return | | | | | |
| Functions | | | | |
| Function declaration | | | | |
| Lambda function expression | | | | |
| `inline` specifier | | | | |
| Dynamic exception specifications (until C++17\*) | | | | |
| `noexcept` specifier (C++11) | | | | |
| Exceptions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `throw`-expression | | | | | | `try` block | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | `catch` handler | | | | | |
| Namespaces | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace declaration | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace aliases | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Fundamental types | | | | | | Enumeration types | | | | | | Function types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class/struct types | | | | | | Union types | | | | | |  | | | | | |
| Specifiers | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const`/`volatile` | | | | | | decltype (C++11) | | | | | | auto (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | constexpr (C++11) | | | | | | consteval (C++20) | | | | | | constinit (C++20) | | | | | |
| Storage duration specifiers | | | | |
| Initialization | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default-initialization | | | | | | Value-initialization | | | | | | Zero-initialization | | | | | | Copy-initialization | | | | | | Direct-initialization | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Aggregate initialization | | | | | | List-initialization (C++11) | | | | | | Constant initialization | | | | | | Reference initialization | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Expressions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Operators | | | | | | Operator precedence | | | | | |
| Alternative representations | | | | |
| Literals | | | | |
| Boolean - Integer - Floating-point | | | | |
| Character - String - nullptr (C++11) | | | | |
| User-defined (C++11) | | | | |
| Utilities | | | | |
| Attributes (C++11) | | | | |
| Types | | | | |
| `typedef` declaration | | | | |
| Type alias declaration (C++11) | | | | |
| Casts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | static_cast | | | | | | const_cast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Explicit conversions | | | | | | dynamic_cast | | | | | | reinterpret_cast | | | | | |
| Memory allocation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `new` expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `delete` expression | | | | | |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class declaration | | | | | | Constructors | | | | | | `this` pointer | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Access specifiers | | | | | | `friend` specifier | | | | | |  | | | | | |
| Class-specific function properties | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Virtual function | | | | | | `override` specifier (C++11) | | | | | | `final` specifier (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | explicit (C++11) | | | | | | static | | | | | |  | | | | | |
| Special member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default constructor | | | | | | Copy constructor | | | | | | Move constructor (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Copy assignment | | | | | | Move assignment (C++11) | | | | | | Destructor | | | | | |
| Templates | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

 Basic Concepts

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Comments | | | | |
| ASCII | | | | |
| Punctuation | | | | |
| Names and identifiers | | | | |
| Types | | | | |
| Fundamental types | | | | |
| Objects | | | | |
| ****Scope**** | | | | |
| Object lifetime | | | | |
| Storage duration and linkage | | | | |
| Definitions and ODR | | | | |
| Name lookup | | | | |
| Qualified name lookup | | | | |
| Unqualified name lookup | | | | |
| The as-if rule | | | | |
| Undefined behavior | | | | |
| Memory model | | | | |
| Multi-threaded executions and data races (C++11) | | | | |
| Character sets and encodings | | | | |
| Phases of translation | | | | |
| The `main` function | | | | |
| Modules (C++20) | | | | |

Each declaration that appears in a C++ program is only visible in some possibly discontiguous **scopes**.

Within a scope, unqualified name lookup can be used to associate a name with its declaration.

### General

Each program has a **global scope**, which **contains** the entire program.

Every other scope `S` is introduced by

- a declaration,
- a parameter in parameter list,
- a statement, or
- a handler.

`S` always appear in another scope, which thereby **contains** `S`.

An **enclosing scope** at a program point is any scope that contains it; the smallest such scope is said to be the **immediate scope** at that point.

A scope **intervenes** between a program point `P` and a scope `S` (that does not contain `P`) if it is or contains `S` but does not contain `P`.

The **parent scope** of any scope `S` that is not a template parameter scope is the smallest scope that contains `S` and is not a template parameter scope.

Unless otherwise specified:

- A declaration **inhabits** the immediate scope at its locus.
- A declaration’s **target scope** is the scope it inhabits.
- Any names (re)introduced by a declaration are **bound** to it in its target scope.

An entity **belongs** to a scope `S` if `S` is the target scope of a declaration of the entity.

```
//                global  scope  scope
//                scope     S      T
int x;         //   ─┐                 // program point X
               //    │
{              //    │     ─┐
    {          //    │      │     ─┐
        int y; //    │      │      │   // program point Y
    }          //    │      │     ─┘
}              //   ─┘     ─┘

```

In the program above:

- The global scope, scope `S` and scope `T` contains program point `Y`.

:   - In other words, these three scopes are all enclosing scopes at program point `Y`.

- The global scope contains scopes `S` and `T`, and scope `S` contains scope `T`.

:   - Therefore, scope `T` is the smallest scope among all three, which means:

    :   - Scope `T` is the immediate scope at program point `Y`.
        - The declaration of the variable y inhabits scope `T` at its locus.
        - Scope `T` is the target scope of the declaration of y.
        - The variable y belongs to scope `T`.

    - Scope `S` is the parent scope of scope `T`, and the global scope is the parent scope of scope `S`.

- Scope `S` intervenes between program point `X` and scope `T`.

### Block scope

Each

- selection statement (if, switch),
- iteration statement (for, range-for(since C++11), while, do-while),
- handler, or
- compound statement that is not the compound-statement of a handler

introduces a **block scope** that includes the statement or handler.

A variable that belongs to a block scope is a **block variable**.

```
int i = 42;
int a[10];
 
for (int i = 0; i < 10; i++) // inner “i” inhabits the block scope
    a[i] = i;                // introduced by the for-statement
 
int j = i; // j = 42

```

Block-scope extern declarations target a larger enclosing scope, but bind a name in their immediate scope.

If a declaration that is not a name-independent declaration and(since C++26) that binds a name in the block scope `S` of

- the compound-statement of a function body or function try block,

|  |  |
| --- | --- |
| - the compund statement `{` body `}` of a lambda expression, | (since C++11) |

- a substatement of a selection or iteration statement that is not itself a selection or iteration statement, or
- a handler of a function try block

potentially conflicts with a declaration whose target scope is the parent scope of `S`, the program is ill-formed.

```
if (int x = f())  // declares “x”
{ // the if-block is a substatement of the if-statement
    int x;        // error: redeclaration of “x”
}
else
{ // the else-block is also a substatement of the if-statement
    int x;        // error: redeclaration of “x”
}
 
void g(int i)
{
    extern int i; // error: redeclaration of “i”
}

```

### Function parameter scope

Each parameter declaration `P` introduces a **function parameter scope** that includes `P`.

- If the declared parameter is of the parameter list of a function declaration:

:   - If the function declaration is a function definition, the scope introduced is extended to the end of the function definition.
    - Otherwise (the function declaration is a function prototype), the scope introduced is extended to the end of the function declarator.
    - In both cases, the scope does not include the locus of the function declaration.

|  |  |
| --- | --- |
| - If the declared parameter is of the parameter list of a lambda expression, the scope introduced is extended to the end of `{` body `}`. | (since C++11) |
| - If the declared parameter is of the parameter list of a deduction guide, the scope introduced is extended to the end of that deduction guide. | (since C++17) |
| - If the declared parameter is of the parameter list of a requires expression, the scope introduced is extended to the end of `{` requirement-seq `}`. | (since C++20) |

```
int f(int n) // the declaration of the parameter “n”
{            // introduces a function parameter scope
    /* ... */
}            // the function parameter scope ends here

```

|  |  |
| --- | --- |
| Lambda scope Each lambda expression introduces a **lambda scope** that starts immediately after `[`captures ﻿`]` and extends to the end of `{` body `}`.  The captures with initializers of a lambda expression E inhabit the lambda scope introduced by E.   ```text auto lambda = [x = 1, y]() // this lambda expression introduces a lambda scope, {                          // it is the target scope of capture “x”     /* ... */ };                         // the lambda scope ends before the semicolon ``` | (since C++14) |

### Namespace scope

Every namespace definition for a namespace `N` introduces a **namespace scope** `S` that includes the declarations for every namespace definition for `N`.

For each non-friend redeclaration or specialization whose target scope is `S` or is contained by `S`, the following portions are also included in scope `S`:

- For a class (template) redeclaration or class template specialization, the portion after its class-head-name.
- For a enumeration redeclaration, the portion after its enum-head-name.
- For any other redeclaration or specialization, the portion after the unqualified-id or qualified-id of the declarator.

The global scope is the namespace scope of the global namespace.

```
namespace V   // the namespace definition of “V”
{             // introduces a namespace scope “S”
    // the first part of scope “S” begins here
    void f();
    // the first part of scope “S” ends here
}
 
void V::f()   // the portion after “f” is also a part of scope “S”
{
    void h(); // declares V::h
}             // the second part of scope “S” ends here

```

### Class scope

Each declaration of a class or class template `C` introduces a **class scope** `S` that includes the member-specification of the class definition of `C`.

For each non-friend redeclaration or specialization whose target scope is `S` or is contained by `S`, the following portions are also included in scope `S`:

- For a class (template) redeclaration or class template specialization, the portion after its class-head-name.
- For a enumeration redeclaration, the portion after its enum-head-name.
- For any other redeclaration or specialization, the portion after the unqualified-id or qualified-id of the declarator.

```
class C       // the class definition of “C”
{             // introduces a class scope “S”
    // the first part of scope “S” begins here
    void f();
    // the first part of scope “S” ends here
}
 
void C::f()   // the portion after “f” is also a part of scope “S”
{
    /* ... */
}             // the second part of scope “S” ends here

```

### Enumeration scope

Each declaration of an enumeration `E` introduces an **enumeration scope** that includes the enumerator-list of the non-opaque(since C++11) enumeration declaration of `E` (if present).

```
enum class E // the enumeration declaration of “E”
{            // introduces an enumeration scope “S”
    // scope “S” begins here
    e1, e2, e3
    // scope “S” ends here
}

```

### Template parameter scope

Each template template parameter introduces a **template parameter scope** that includes the entire template parameter list and the require clauses(since C++20) of that template template parameter.

Each template declaration `D` introduces a **template parameter scope** `S` that extends from the beginning of the template parameter list of `D` to the end of `D`. Any declaration outside the template parameter list that would inhabit `S` instead inhabits the same scope as `D`.

```
// the class template declaration of “X”
// introduces a template parameter scope “S1”
template
<
    // scope “S1” begins here
    template // the template template parameter “T”
             // introduces another template parameter scope “S2”
    <
        typename T1
        typename T2
    > requires std::convertible_from<T1, T2> // scope “S2” ends here
    class T,
    typename U
>
class X; // scope “S1” ends before the semicolon

```

### Point of declaration

In general, a name is visible after the **locus** of its first declaration, which is located as follows.

The locus of a name declared in a simple declaration is immediately after that name's declarator and before its initializer, if any.

```
int x = 32; // outer x is in scope
 
{
    int x = x; // inner x is in scope before the initializer (= x)
               // this does not initialize inner x with the value of outer x (32),
               // this initializes inner x with its own (indeterminate) value
}
 
std::function<int(int)> f = &{ return n > 1 ? n * f(n - 1) : n; };
// the name of the function f is in scope in the lambda and can
// be correctly captured by reference, giving a recursive function

```

```
const int x = 2; // outer x is in scope
 
{
    int x[x] = {}; // inner x is in scope before the initializer (= {}),
                   // but after the declarator (x[x])
                   // in the declarator, outer x is still in scope
                   // this declares an array of 2 int
}

```

The locus of a class or class template declaration is immediately after the identifier that names the class (or the template-id that names the template specialization) in its class-head. The class or class template name is already in scope in the list of base classes.

```
struct S: std::enable_shared_from_this<S> {}; // S is in scope at the colon

```

The locus of enum specifier or opaque enum declaration(since C++11) is immediately after the identifier that names the enumeration.

```
enum E : int // E is in scope at the colon
{
    A = sizeof(E)
};

```

The locus of a type alias or alias template declaration is immediately after the type-id to which the alias refers.

```
using T = int; // outer T is in scope at the semicolon
 
{
    using T = T*; // inner T is in scope at the semicolon,
                  // outer T is still in scope before the semicolon
                  // same as T = int*
}

```

The locus for a declarator in a using declaration that does not name a constructor is immediately after the declarator.

```
template<int N>
class Base
{
protected:
    static const int next = N + 1;
    static const int value = N;
};
 
struct Derived: Base<0>, Base<1>, Base<2>
{
    using Base<0>::next,     // next is in scope at the comma
          Base<next>::value; // Derived::value is 1
};

```

The locus of an enumerator is immediately after its definition (not before the initializer as it is for variables).

```
const int x = 12;
 
{
    enum
    {
        x = x + 1, // enumerator x is in scope at the comma,
                   // outer x is in scope before the comma,
                   // enumerator x is initialized to 13
        y = x + 1  // y is initialized to 14
    };
}

```

The locus for an injected-class-name is immediately following the opening brace of its class (or class template) definition.

```
template<typename T>
struct Array
//  : std::enable_shared_from_this<Array> // error: the injected class name is not in scope
    : std::enable_shared_from_this< Array<T> > // OK: the template-name Array is in scope
{ // the injected class name Array is now in scope as if a public member name
    Array* p; // pointer to Array<T>
};

```

|  |  |
| --- | --- |
| The locus of the implicit declaration for a function-local predefined variable __func__ is immediately before the function body of a function definition. | (since C++11) |

|  |  |
| --- | --- |
| The locus of a structured binding declaration is immediately after the identifier-list, but structured binding initializers are prohibited from referring to any of the names being declared. | (since C++17) |

|  |  |
| --- | --- |
| The locus of the variable or the structured bindings(since C++17) declared in the range-declaration of a range-for loop is immediately after the range-expression.   ```text std::vector<int> x;   for (auto x : x) // vector x is in scope before the closing parenthesis,                  // auto x is in scope at the closing parenthesis {     // the auto x is in scope } ``` | (since C++11) |

The locus of a template parameter is immediately after its complete template parameter (including the optional default argument).

```
typedef unsigned char T;
 
template<
    class T = T, // template parameter T is in scope at the comma,
                 // typedef name of unsigned char is in scope before the comma
    T // template parameter T is in scope
    N = 0
>
struct A
{
};

```

|  |  |
| --- | --- |
| The locus of a concept definition is immediately after the concept name, but concept definitions are prohibited from referring to the concept name being declared. | (since C++20) |

The locus of a named namespace definition is immediately after the namespace name.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: remainder of [basic.scope.pdecl] |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 2793 | C++98 | an extern declaration in a block scope could conflict with another declaration in the parent scope | prohibited |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 6.4 Scope [basic.scope]

- C++20 standard (ISO/IEC 14882:2020):

:   - 6.4 Scope [basic.scope]

- C++17 standard (ISO/IEC 14882:2017):

:   - 6.3 Scope [basic.scope]

- C++14 standard (ISO/IEC 14882:2014):

:   - 3.3 Scope [basic.scope]

- C++11 standard (ISO/IEC 14882:2011):

:   - 3.3 Scope [basic.scope]

- C++98 standard (ISO/IEC 14882:1998):

:   - 3.3 Declarative regions and scopes [basic.scope]

### See also

|  |  |
| --- | --- |
| C documentation for Scope | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/scope&oldid=173849>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 July 2024, at 21:40.