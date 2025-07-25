# Non-static data members

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

 Classes

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| Overview | | | | |
| `class`/`struct` types | | | | |
| `union` types | | | | |
| Injected-class-name | | | | |
| Members | | | | |
| ****Data members**** | | | | |
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
| Default constructor | | | | |
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

Non-static data members are declared in a member specification of a class.

```
class S
{
    int n;              // non-static data member
    int& r;             // non-static data member of reference type
    int a[2] = {1, 2};  // non-static data member with default member initializer (C++11)
    std::string s, *ps; // two non-static data members
 
    struct NestedS
    {
        std::string s;
    } d5;               // non-static data member of nested type
 
    char bit : 2;       // two-bit bitfield
};

```

Any simple declarations are allowed, except

- extern and register storage class specifiers are not allowed;

|  |  |
| --- | --- |
| - thread_local storage class specifier is not allowed (but it is allowed for static data members); | (since C++11) |

- incomplete types, abstract class types, and arrays thereof are not allowed: in particular, a class `C` cannot have a non-static data member of type `C`, although it can have a non-static data member of type `C&` (reference to C) or `C*` (pointer to `C`);
- a non-static data member cannot have the same name as the name of the class if at least one user-declared constructor is present;

|  |  |
| --- | --- |
| - a placeholder type specifier (i.e. auto, decltype(auto)(since C++14), a class template name subject to deduction(since C++17), a constrained placeholder(since C++20)) cannot be used in a non-static data member declaration (although it is allowed for static data members that are initialized in the class definition). | (since C++11) |

In addition, bit-field declarations are allowed.

### Layout

When an object of some class `C` is created, each non-static data member of non-reference type is allocated in some part of the object representation of `C`. Whether reference members occupy any storage is implementation-defined, but their storage duration is the same as that of the object in which they are members.

|  |  |
| --- | --- |
| For non-union class types, non-zero-sized(since C++20) members not separated by an access specifier(until C++11)with the same member access(since C++11) are always allocated so that the members declared later have higher addresses within a class object. Members separated by an access specifier(until C++11)with different access control(since C++11) are allocated in unspecified order (the compiler may group them together). | (until C++23) |
| For non-union class types, non-zero-sized members are always allocated so that the members declared later have higher addresses within a class object. Note that access control of member still affects the standard-layout property (see below). | (since C++23) |

Alignment requirements may necessitate padding between members, or after the last member of a class.

### Standard-layout

|  |  |
| --- | --- |
| A class is considered to be **standard-layout** and to have properties described below if and only if it is a POD class. | (until C++11) |
| A class where all non-static data members have the same access control and certain other conditions are satisfied is known as **standard-layout class** (see standard-layout class for the list of requirements). | (since C++11) |

The **common initial sequence** of two standard-layout non-union class types is the longest sequence of non-static data members and bit-fields in declaration order, starting with the first such entity in each of the classes, such that

|  |  |
| --- | --- |
| - if __has_cpp_attribute(no_unique_address) is not ​0​, neither entity is declared with `[[no_unique_address]]` attribute, | (since C++20) |

- corresponding entities have layout-compatible types,
- corresponding entities have the same alignment requirements, and
- either both entities are bit-fields with the same width or neither is a bit-field.

```
struct A { int a; char b; };
struct B { const int b1; volatile char b2; }; 
// A and B's common initial sequence is A.a, A.b and B.b1, B.b2
 
struct C { int c; unsigned : 0; char b; };
// A and C's common initial sequence is A.a and C.c
 
struct D { int d; char b : 4; };
// A and D's common initial sequence is A.a and D.d
 
struct E { unsigned int e; char b; };
// A and E's common initial sequence is empty

```

Two standard-layout non-union class types are called **layout-compatible** if they are the same type ignoring cv-qualifiers, if any, are layout-compatible enumerations (i.e. enumerations with the same underlying type), or if their **common initial sequence** consists of every non-static data member and bit-field (in the example above, `A` and `B` are layout-compatible).

Two standard-layout unions are called **layout-compatible** if they have the same number of non-static data members and corresponding non-static data members (in any order) have layout-compatible types.

Standard-layout types have the following special properties:

:   - In a standard-layout union with an active member of non-union class type `T1`, it is permitted to read a non-static data member `m` of another union member of non-union class type `T2` provided `m` is part of the common initial sequence of `T1` and `T2` (except that reading a volatile member through non-volatile glvalue is undefined).
    - A pointer to an object of standard-layout class type can be `reinterpret_cast` to pointer to its first non-static non-bitfield data member (if it has non-static data members) or otherwise any of its base class subobjects (if it has any), and vice versa. In other words, padding is not allowed before the first data member of a standard-layout type. Note that strict aliasing rules still apply to the result of such cast.
    - The macro offsetof may be used to determine the offset of any member from the beginning of a standard-layout class.

### Member initialization

Non-static data members may be initialized in one of two ways:

1) In the member initializer list of the constructor.

```
struct S
{
    int n;
    std::string s;
    S() : n(7) {} // direct-initializes n, default-initializes s
};

```

|  |  |  |  |
| --- | --- | --- | --- |
| 2) Through a **default member initializer**, which is a brace or equals initializer included in the member declaration and is used if the member is omitted from the member initializer list of a constructor.  ```text struct S {     int n = 7;     std::string s{'a', 'b', 'c'};     S() {} // default member initializer will copy-initialize n, list-initialize s }; ```   If a member has a default member initializer and also appears in the member initialization list in a constructor, the default member initializer is ignored for that constructor. Run this code  ```text #include <iostream>   int x = 0; struct S {     int n = ++x;     S() {}                 // uses default member initializer     S(int arg) : n(arg) {} // uses member initializer  };   int main() {     std::cout << x << '\n'; // prints 0     S s1;                   // default initializer ran     std::cout << x << '\n'; // prints 1     S s2(7);                // default initializer did not run     std::cout << x << '\n'; // prints 1 } ```  |  |  | | --- | --- | | Default member initializers are not allowed for bit-field members. | (until C++20) |   Members of array type cannot deduce their size from member initializers:   ```text struct X {     int a[] = {1, 2, 3};  // error     int b[3] = {1, 2, 3}; // OK }; ```   Default member initializers are not allowed to cause the implicit definition of a defaulted default constructor for the enclosing class or the exception specification of that constructor:   ```text struct node {     node* p = new node; // error: use of implicit or defaulted node::node()  }; ```   Reference members cannot be bound to temporaries in a default member initializer (note; same rule exists for member initializer lists):   ```text struct A {     A() = default;     // OK     A(int v) : v(v) {} // OK     const int& v = 42; // OK };   A a1;    // error: ill-formed binding of temporary to reference A a2(1); // OK (default member initializer ignored because v appears in a constructor)          // however a2.v is a dangling reference ``` | (since C++11) |

|  |  |
| --- | --- |
| If a reference member is initialized from its default member initializer(until C++20)a member has a default member initializer(since C++20) and a potentially-evaluated subexpression thereof is an aggregate initialization that would use that default member initializer, the program is ill-formed:   ```text struct A; extern A a;   struct A {     const A& a1{A{a, a}}; // OK     const A& a2{A{}};     // error };   A a{a, a};                // OK ``` | (since C++17) |

### Usage

The name of a non-static data member or a non-static member function can only appear in the following three situations:

1) As a part of class member access expression, in which the class either has this member or is derived from a class that has this member, including the implicit this-> member access expressions that appear when a non-static member name is used in any of the contexts where `this` is allowed (inside member function bodies, in member initializer lists, in the in-class default member initializers).

```
struct S
{
    int m;
    int n;
    int x = m;            // OK: implicit this-> allowed in default initializers (C++11)
 
    S(int i) : m(i), n(m) // OK: implicit this-> allowed in member initializer lists
    {
        this->f();        // explicit member access expression
        f();              // implicit this-> allowed in member function bodies
    }
 
    void f();
};

```

2) To form a pointer to non-static member.

```
struct S
{
    int m;
    void f();
};
 
int S::*p = &S::m;       // OK: use of m to make a pointer to member
void (S::*fp)() = &S::f; // OK: use of f to make a pointer to member

```

3) (for data members only, not member functions) When used in unevaluated operands.

```
struct S
{
    int m;
    static const std::size_t sz = sizeof m; // OK: m in unevaluated operand
};
 
std::size_t j = sizeof(S::m + 42); // OK: even though there is no "this" object for m

```

 Notes: such uses are allowed via the resolution of CWG issue 613 in N2253, which is treated as a change in C++11 by some compilers (e.g. clang).

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_nsdmi` | `200809L` | (C++11) | Non-static data member initializers |
| `__cpp_aggregate_nsdmi` | `201304L` | (C++14) | Aggregate classes with default member initializers |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 80 | C++98 | all data members cannot have the same name as the name of the class (breaks C compatibility) | allow non-static data members share the class name if there is no user-declared constructor |
| CWG 190 | C++98 | when determining layout compatibility, all members were considered | only consider non- static data members |
| CWG 613 | C++98 | unevaluated uses of non-static data members not allowed | such uses are allowed |
| CWG 645 | C++98 | it was unspecified whether bit-field and non-bit-field members are layout compatible | not layout compatible |
| CWG 1397 | C++11 | class was regarded as complete in the default member initializers | default member init cannot trigger definition of default constructor |
| CWG 1425 | C++98 | it was unclear whether a standard-layout object shares the same address with the first non-static data member or the first base class subobject | non-static data member if present, otherwise base class subobject if present |
| CWG 1696 | C++98 | reference members could be initialized to temporaries (whose lifetime would end at the end of constructor) | such init is ill-formed |
| CWG 1719 | C++98 | differently cv-qualified types weren't layout-compatible | cv-quals ignored, spec improved |
| CWG 2254 | C++11 | pointer to standard-layout class with no data members can be reinterpret_cast to its first base class | can be reinterpret_cast to any of its base classes |
| CWG 2583 | C++11 | common initial sequence did not consider alignment requirements | considered |
| CWG 2759 | C++20 | common initial sequence could include members declared `[[no_unique_address]]` | they are not included |

### See also

|  |  |
| --- | --- |
| classes | |
| static members | |
| non-static member functions | |
| is_standard_layout(C++11) | checks if a type is a standard-layout type   (class template) |
| offsetof | byte offset from the beginning of a standard-layout type to specified member   (function macro) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/data_members&oldid=168790>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 January 2024, at 13:29.