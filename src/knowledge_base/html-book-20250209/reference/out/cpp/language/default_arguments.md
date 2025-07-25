# Default arguments

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

 Functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Declarations | | | | |
| Function declaration | | | | |
| Function parameter list | | | | |
| Function definition | | | | |
| ****Default arguments**** | | | | |
| Variadic arguments | | | | |
| `inline` specifier | | | | |
| Lambda expressions (C++11) | | | | |
| Coroutines (C++20) | | | | |
| Function calls | | | | |
| Argument-Dependent Lookup (ADL) | | | | |
| Function-call operator | | | | |
| Function objects | | | | |
| Overloading | | | | |
| Overload resolution | | | | |
| Operator overloading | | | | |
| Address of an overload set | | | | |

Allows a function to be called without providing one or more trailing arguments.

Indicated by using the following syntax for a parameter in the parameter-list of a function declaration.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr ﻿(optional) decl-specifier-seq declarator `=` initializer | (1) |  |
|  | | | | | | | | | |
| attr ﻿(optional) decl-specifier-seq abstract-declarator ﻿(optional) `=` initializer | (2) |  |
|  | | | | | | | | | |

Default arguments are used in place of the missing trailing arguments in a function call:

```
void point(int x = 3, int y = 4);
 
point(1, 2); // calls point(1, 2)
point(1);    // calls point(1, 4)
point();     // calls point(3, 4)

```

In a function declaration, after a parameter with a default argument, all subsequent parameters must:

- have a default argument supplied in this or a previous declaration from the same scope:

```
int x(int = 1, int); // Error: only the trailing parameters can have default arguments
                     // (assuming there's no previous declaration of x)
 
void f(int n, int k = 1);
void f(int n = 0, int k); // OK: the default argument of `k` is provided by
                          // the previous declaration in the same scope
 
void g(int, int = 7);
 
void h()
{
    void g(int = 1, int); // Error: not the same scope
}

```

|  |  |
| --- | --- |
| - ...unless the parameter was expanded from a parameter pack:   ```text template<class... T> struct C { void f(int n = 0, T...); };   C<int> c;  // OK; instantiates declaration void C::f(int n = 0, int) ```  - or be a function parameter pack:  ```text template<class... T> void h(int i = 0, T... args); // OK ``` | (since C++11) |

The ellipsis is not a parameter, and so can follow a parameter with a default argument:

```
int g(int n = 0, ...); // OK

```

Default arguments are only allowed in the parameter lists of function declarations and lambda-expressions,(since C++11) and are not allowed in the declarations of pointers to functions, references to functions, or in typedef declarations. Template parameter lists use similar syntax for their default template arguments.

For non-template functions, default arguments can be added to a function that was already declared if the function is redeclared in the same scope. At the point of a function call, the default arguments are a union of the default arguments provided in all visible declarations for the function. A redeclaration cannot introduce a default argument for a parameter for which a default argument is already visible (even if the value is the same). A re-declaration in an inner scope does not acquire the default arguments from outer scopes.

```
void f(int, int);     // #1
void f(int, int = 7); // #2 OK: adds a default argument
 
void h()
{
    f(3); // #1 and #2 are in scope; makes a call to f(3,7)
    void f(int = 1, int); // Error: the default argument of the second
                          // parameter is not acquired from outer scopes
}
 
void m()
{ // new scope begins
    void f(int, int); // inner scope declaration; has no default argument.
    f(4); // Error: not enough arguments to call f(int, int)
    void f(int, int = 6);
    f(4); // OK: calls f(4, 6);
    void f(int, int = 6); // Error: the second parameter already has a
                          // default argument (even if the values are the same)
}
 
void f(int = 1, int); // #3 OK, adds a default argument to #2
 
void n()
{ // new scope begins
    f(); // #1, #2, and #3 are in scope: calls f(1, 7);
}

```

If an inline function is declared in different translation units, the accumulated sets of default arguments must be the same at the end of each translation unit.

|  |  |
| --- | --- |
| If a non-inline function is declared in the same namespace scope in different translation units, the corresponding default arguments must be the same if present (but some default arguments can be absent in some TU). | (since C++20) |

If a friend declaration specifies a default argument, it must be a friend function definition, and no other declarations of this function are allowed in the translation unit.

The using-declarations carries over the set of known default arguments, and if more default arguments are added later to the function's namespace, those default arguments are also visible anywhere the using-declaration is visible:

```
namespace N
{
    void f(int, int = 1);
}
 
using N::f;
 
void g()
{
    f(7); // calls f(7, 1);
    f();  // error
}
 
namespace N
{
    void f(int = 2, int);
}
 
void h()
{
    f();  // calls f(2, 1);
}

```

The names used in the default arguments are looked up, checked for accessibility, and bound at the point of declaration, but are executed at the point of the function call:

```
int a = 1;
 
int f(int);
 
int g(int x = f(a)); // lookup for f finds ::f, lookup for a finds ::a
                     // the value of ::a, which is 1 at this point, is not used
 
void h()
{
    a = 2; // changes the value of ::a
    {
        int a = 3;
        g(); // calls f(2), then calls g() with the result
    }
}

```

For a member function of a non-templated class, the default arguments are allowed on the out-of-class definition, and are combined with the default arguments provided by the declaration inside the class body. If these out-of-class default arguments would turn a member function into a default constructor or copy/move(since C++11) constructor/assignment operator (which makes the call ambiguous), the program is ill-formed. For member functions of templated classes, all default arguments must be provided in the initial declaration of the member function.

```
class C
{
    void f(int i = 3);
    void g(int i, int j = 99);
    C(int arg); // non-default constructor
};
 
void C::f(int i = 3) {}         // error: default argument already
                                // specified in class scope
 
void C::g(int i = 88, int j) {} // OK: in this translation unit,
                                // C::g can be called with no argument
 
C::C(int arg = 1) {}            // Error: turns this into a default constructor

```

The overriders of virtual functions do not acquire the default arguments from the base class declarations, and when the virtual function call is made, the default arguments are decided based on the static type of the object (note: this can be avoided with non-virtual interface pattern).

```
struct Base
{
    virtual void f(int a = 7);
};
 
struct Derived : Base
{
    void f(int a) override;
};
 
void m()
{
    Derived d;
    Base& b = d;
    b.f(); // OK: calls Derived::f(7)
    d.f(); // Error: no default argument
}

```

Local variables are not allowed in default arguments unless they are not evaluated:

```
void f()
{
    int n = 1;
    extern void g(int x = n); // error: local variable cannot be a default argument
    extern void h(int x = sizeof n); // OK as of CWG 2082
}

```

The this pointer is not allowed in default arguments:

```
class A
{
    void f(A* p = this) {} // error: this is not allowed
};

```

Non-static class members are not allowed in default arguments (even if they are not evaluated), except when used to form a pointer-to-member or in a member access expression:

```
int b;
 
class X
{
    int a;
    int mem1(int i = a); // error: non-static member cannot be used
    int mem2(int i = b); // OK: lookup finds X::b, the static member
    int mem3(int X::* i = &X::a); // OK: non-static member can be used
    int mem4(int i = x.a); // OK: in a member access expression
 
    static X x;
    static int b;
};

```

A default argument is evaluated each time the function is called with no argument for the corresponding parameter. Function parameters are not allowed in default arguments except if they are not evaluated. Note that parameters that appear earlier in the parameter list are in scope:

```
int a;
 
int f(int a, int b = a); // Error: the parameter a used in a default argument
 
int g(int a, int b = sizeof a); // Error until resolving CWG 2082
                                // OK after resolution: use in unevaluated context is OK

```

The default arguments are not part of the function type:

```
int f(int = 0);
 
void h()
{
    int j = f(1);
    int k = f(); // calls f(0);
}
 
int (*p1)(int) = &f;
int (*p2)()    = &f; // Error: the type of f is int(int)

```

Operator functions cannot have default arguments, except for the function call operator:

```
class C
{
    int operator[](int i = 0); // ill-formed
    int operator()(int x = 0); // OK
};

```

|  |  |
| --- | --- |
| Explicit object parameters cannot have default arguments:   ```text struct S { void f(this const S& = S{}); }; // ill-formed ``` | (since C++23) |

### Note

Spaces may be necessary to avoid a compound assignment token if the parameter name is absent.

```
void f1(int*=0);         // Error, '*=' is unexpected here
void g1(const int&=0);   // Error, '&=' is unexpected here
void f2(int* = 0);       // OK
void g2(const int& = 0); // OK
void h(int&&=0);         // OK even without spaces, '&&' is a token here

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 217 | C++98 | a default argument could be added to a non- template member function of a class template | prohibited |
| CWG 1344 | C++98 | default arguments added in the out-of-class definition of a member function could change it to a special member function | prohibited |
| CWG 1716 | C++98 | default arguments were evaluated each time the function is called, even if the caller provided the arguments | evaluated only if no argument is provided for the corresponding parameter |
| CWG 2082 | C++98 | default arguments were forbidden to use local variables and preceding parameters in unevaluated context | unevaluated context use allowed |
| CWG 2233 | C++11 | parameters expanded from parameter packs could not appear after parameters with default arguments | allowed |
| CWG 2683 | C++98 | out-of-class definitions of the member functions of class templates' nested classes could have default arguments | prohibited |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/default_arguments&oldid=161841>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 31 October 2023, at 22:28.