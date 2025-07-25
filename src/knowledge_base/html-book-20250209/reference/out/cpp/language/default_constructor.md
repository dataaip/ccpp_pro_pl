# Default constructors

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****Default constructor**** | | | | | | Copy constructor | | | | | | Move constructor (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Copy assignment | | | | | | Move assignment (C++11) | | | | | | Destructor | | | | | |
| Templates | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

 Classes

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| Overview | | | | |
| `class`/`struct` types | | | | |
| `union` types | | | | |
| Injected-class-name | | | | |
| Members | | | | |
| Data members | | | | |
| Static members | | | | |
| The `this` pointer | | | | |
| Nested classes | | | | |
| Member templates | | | | |
| Bit-fields | | | | |
| `using`-declarations | | | | |
| Member functions | | | | |
| Member access specifiers | | | | |
| Constructors and member initializer lists | | | | |
| Default member initializer (C++11) | | | | |
| `friend` specifier | | | | |
| `explicit` specifier | | | | |
| Converting constructor | | | | |
| Special member functions | | | | |
| ****Default constructor**** | | | | |
| Copy constructor | | | | |
| Move constructor (C++11) | | | | |
| Copy assignment operator | | | | |
| Move assignment operator (C++11) | | | | |
| Destructor | | | | |
| Inheritance | | | | |
| Base and derived classes | | | | |
| Empty base optimization (EBO) | | | | |
| Virtual member functions | | | | |
| Pure virtual functions and abstract classes | | | | |
| `override` specifier (C++11) | | | | |
| `final` specifier (C++11) | | | | |

A default constructor is a constructor which can be called with no arguments.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| class-name ﻿`(`parameter-list ﻿(optional)`);` | (1) |  |
|  | | | | | | | | | |
| class-name ﻿`(`parameter-list ﻿(optional)`)` function-body | (2) |  |
|  | | | | | | | | | |
| class-name ﻿`() = default;` | (3) | (since C++11) |
|  | | | | | | | | | |
| class-name ﻿`(`parameter-list ﻿(optional)`) = delete;` | (4) | (since C++11) |
|  | | | | | | | | | |
| class-name ﻿`::`class-name ﻿`(`parameter-list ﻿(optional)`)` function-body | (5) |  |
|  | | | | | | | | | |
| class-name ﻿`::`class-name ﻿`() = default;` | (6) | (since C++11) |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| class-name | - | the class whose default constructor is being declared |
| parameter-list | - | a parameter list where all parameters (except parameter packs)(since C++11) have default arguments |
| function-body | - | the function body of the default constructor |

### Explanation

1) Declaration of a default constructor inside of class definition.2-4) Definition of a default constructor inside of class definition.3) The default constructor is explicitly-defaulted.4) The default constructor is deleted.5,6) Definition of a default constructor outside of class definition (the class must contain a declaration (1)).6) The default constructor is explicitly-defaulted.

Default constructors are called during default initializations and value initializations.

### Implicitly-declared default constructor

If there is no user-declared constructor or constructor template for a class type, the compiler will implicitly declare a default constructor as an inline public member of its class.

The implicitly-declared (or defaulted on its first declaration) default constructor has an exception specification as described in dynamic exception specification(until C++17) noexcept specification(since C++17).

### Implicitly-defined default constructor

If the constructor is implicitly-declared(until C++11)the implicitly-declared or explicitly-defaulted default constructor is not defined as deleted(since C++11), it is defined (that is, a function body is generated and compiled) by the compiler if odr-used or needed for constant evaluation(since C++11), and it has the same effect as a user-defined constructor with empty body and empty initializer list. That is, it calls the default constructors of the bases and of the non-static members of this class. Class types with an empty user-provided constructor may get treated differently than those with an implicitly-defined default constructor during value initialization.

|  |  |
| --- | --- |
| If this satisfies the requirements of a constexpr constructor(until C++23)constexpr function(since C++23), the generated constructor is constexpr.  If some user-defined constructors are present, the user may still force the automatic generation of a default constructor by the compiler that would be implicitly-declared otherwise with the keyword default. | (since C++11) |

### Deleted default constructor

The implicitly-declared or explicitly-defaulted(since C++11) default constructor for class `T` is undefined(until C++11)defined as deleted(since C++11) if any of the following conditions is satisfied:

- `T` is a union and all of its variant members are of const-qualified type (or possibly multi-dimensional array thereof).
- `T` is a non-union class and all members of any anonymous union member are of const-qualified type (or possibly multi-dimensional array thereof).
- `T` has a non-static data member of reference type without a default initializer(since C++11).
- `T` has a non-variant non-static non-const-default-constructible data member of const-qualified type (or possibly multi-dimensional array thereof) without a default member initializer(since C++11).
- `T` has a potentially constructed subobject of class type `M` (or possibly multi-dimensional array thereof) such that

:   - `M` has a destructor that is deleted or(since C++11) inaccessible from the default constructor, or
    - all of the following conditions are satisfied:

|  |  |
| --- | --- |
| - The subobject is not a non-static data member with a default initializer. - The subobject is not a variant member of a union where another non-static data member has a default initializer. | (since C++11) |

:   :   - The overload resolution as applied to find `M`'s default constructor

        :   - does not result in a usable candidate, or
            - in the case of the subobject being a variant member, selects a non-trivial function.

|  |  |
| --- | --- |
| If no user-defined constructors are present and the implicitly-declared default constructor is not trivial, the user may still inhibit the automatic generation of an implicitly-defined default constructor by the compiler with the keyword delete. | (since C++11) |

### Trivial default constructor

The default constructor for class `T` is trivial (i.e. performs no action) if all of the following is true:

- The constructor is not user-provided (i.e., is implicitly-defined or defaulted on its first declaration).
- `T` has no virtual member functions.
- `T` has no virtual base classes.

|  |  |
| --- | --- |
| - `T` has no non-static members with default initializers. | (since C++11) |

- Every direct base of `T` has a trivial default constructor.
- Every non-static member of class type (or array thereof) has a trivial default constructor.

A trivial default constructor is a constructor that performs no action. All data types compatible with the C language (POD types) are trivially default-constructible.

### Eligible default constructor

|  |  |
| --- | --- |
| A default constructor is eligible if it is either user-declared or both implicitly-declared and definable. | (until C++11) |
| A default constructor is eligible if it is not deleted. | (since C++11) (until C++20) |
| A default constructor is eligible if all following conditions are satisfied:   - It is not deleted. - Its associated constraints (if any) are satisfied. - No default constructor whose associated constraints are satisfied is more constrained. | (since C++20) |

Triviality of eligible default constructors determines whether the class is an implicit-lifetime type, and whether the class is a trivial type.

### Example

Run this code

```
struct A
{
    int x;
    A(int x = 1): x(x) {} // user-defined default constructor
};
 
struct B : A
{
    // B::B() is implicitly-defined, calls A::A()
};
 
struct C
{
    A a;
    // C::C() is implicitly-defined, calls A::A()
};
 
struct D : A
{
    D(int y) : A(y) {}
    // D::D() is not declared because another constructor exists
};
 
struct E : A
{
    E(int y) : A(y) {}
    E() = default; // explicitly defaulted, calls A::A()
};
 
struct F
{
    int& ref; // reference member
    const int c; // const member
    // F::F() is implicitly defined as deleted
};
 
// user declared copy constructor (either user-provided, deleted or defaulted)
// prevents the implicit generation of a default constructor
 
struct G
{
    G(const G&) {}
    // G::G() is implicitly defined as deleted
};
 
struct H
{
    H(const H&) = delete;
    // H::H() is implicitly defined as deleted
};
 
struct I
{
    I(const I&) = default;
    // I::I() is implicitly defined as deleted
};
 
int main()
{
    A a;
    B b;
    C c;
//  D d; // compile error
    E e;
//  F f; // compile error
//  G g; // compile error
//  H h; // compile error
//  I i; // compile error
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 1353 | C++98 | the conditions where implicitly-declared default constructors are undefined did not consider multi-dimensional array types | consider these types |
| CWG 2084 | C++11 | default member initializers had no effect on whether a defaulted default constructor of a union is deleted | they prevent the defaulted default constructor from being deleted |
| CWG 2595 | C++20 | a default constructor was not eligible if there is another default constructor which is more constrained but does not satisfy its associated constraints | it can be eligible in this case |
| CWG 2871 | C++98 | a default constructor would be implicitly declared even if there is a user-declared constructor template | no implicit declaration in this case |

### See also

- constructor
- initialization
  - aggregate initialization
  - constant initialization
  - copy initialization
  - default initialization
  - direct initialization
  - list initialization
  - reference initialization
  - value initialization
  - zero initialization
- `new`
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/default_constructor&oldid=174738>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 August 2024, at 19:37.