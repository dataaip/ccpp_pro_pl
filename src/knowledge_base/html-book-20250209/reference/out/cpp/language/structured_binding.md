# Structured binding declaration (since C++17)

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

Declarations

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Overview | | | | | | Declaration syntax | | | | | | **decl-specifier-seq** | | | | | | Declarator | | | | | | Conflicting declarations | | | | | | Specifiers | | | | | | typedef | | | | | | inline | | | | | | virtual function specifier | | | | | | explicit function specifier | | | | | | friend | | | | | | constexpr(C++11) | | | | | | consteval(C++20) | | | | | | constinit(C++20) | | | | | | Storage class specifiers | | | | | | Translation-unit-local (C++20) | | | | | | class/struct | | | | | | union | | | | | | enum | | | | | | decltype(C++11) | | | | | | auto(C++11) | | | | | | alignas(C++11) | | | | | | constvolatile | | | | | | Pack indexing specifier (C++26) | | | | | | Elaborated type specifier | | | | | | Attributes (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Declarators | | | | | | Reference | | | | | | Pointer | | | | | | Array | | | | | | Block declarations | | | | | | Simple-declaration | | | | | | →****Structured binding declaration**** (C++17) | | | | | | Alias declaration (C++11) | | | | | | Namespace alias definition | | | | | | using declaration | | | | | | `using` directive | | | | | | static_assert declaration (C++11) | | | | | | asm declaration | | | | | | Opaque enum declaration (C++11) | | | | | | Other declarations | | | | | | Namespace definition | | | | | | Function declaration | | | | | | Class template declaration | | | | | | Function template declaration | | | | | | Explicit template instantiation (C++11) | | | | | | Explicit template specialization | | | | | | Linkage specification | | | | | | Attribute declaration (C++11) | | | | | | Empty declaration | | | | | |  | | | | | |

Binds the specified names to subobjects or elements of the initializer.

Like a reference, a structured binding is an alias to an existing object. Unlike a reference, a structured binding does not have to be of a reference type.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr ﻿(optional) decl-specifier-seq ref-qualifier ﻿(optional) `[` sb-identifier-list `]` initializer ﻿`;` |  |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| attr | - | sequence of any number of attributes |
| decl-specifier-seq | - | sequence of the following specifiers (following the rules of simple declaration):  |  |  | | --- | --- | | - `constexpr` - `constinit` | (since C++26) |  - static - thread_local - const - volatile (deprecated in C++20) - `auto` |
| ref-qualifier | - | either `&` or `&&` |
| sb-identifier-list | - | list of comma-separated identifiers introduced by this declaration, each identifier may be followed by an attribute specifier sequence(since C++26) |
| initializer | - | an initializer (see below) |

initializer may be one of the following:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `=` expression | (1) |  |
|  | | | | | | | | | |
| `{` expression } | (2) |  |
|  | | | | | | | | | |
| `(` expression `)` | (3) |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| expression | - | any expression (except unparenthesized comma expressions) |

A structured binding declaration introduces all identifiers in the sb-identifier-list as names in the surrounding scope and binds them to subobjects or elements of the object denoted by expression. The bindings so introduced are called **structured bindings**.

|  |  |
| --- | --- |
| One of the identifiers in the sb-identifier-list can be preceded by an ellipsis. Such an identifier introduces a **structured binding pack**.  The identifier must declare a templated entity. | (since C++26) |

A structured binding is an identifier in the sb-identifier-list ﻿ that is not preceded by an ellipsis, or an element of a structured binding pack introduced in the same identifier list(since C++26).

### Binding process

A structured binding declaration first introduces a uniquely-named variable (here denoted by e) to hold the value of the initializer, as follows:

- If expression has array type **cv1** `A` and no ref-qualifier is present, define e as attr ﻿(optional) specifiers `A e;`, where specifiers is a sequence of the specifiers in decl-specifier-seq excluding auto.

:   Then each element of e is initialized from the corresponding element of expression as specified by the form of initializer ﻿:

    - For initializer syntax (1), the elements are copy-initialized.
    - For initializer syntaxes (2,3), the elements are direct-initialized.

- Otherwise, define e as attr ﻿(optional) decl-specifier-seq ref-qualifier ﻿(optional) `e` initializer ﻿`;`.

We use `E` to denote the type of the identifier expression e (i.e., `E` is the equivalent of std::remove_reference_t<decltype((e))>).

A **structured binding size** of `E` is the number of structured bindings that need to be introduced by the structured binding declaration.

|  |  |
| --- | --- |
| The number of identifiers in sb-identifier-list must be equal to the structured binding size of `E`. | (until C++26) |
| Given the number of identifiers in sb-identifier-list as N and the structured binding size of `E` as S:   - If there is no structured binding pack, N must be equal to S. - Otherwise, the number of non-pack elements (i.e., N - 1) must be less than or equal to S, and the number of elements of the structured binding pack is S - N + 1 (which can be zero). | (since C++26) |

```
struct C { int x, y, z; };
 
template<class T>
void now_i_know_my() 
{
    auto [a, b, c] = C(); // OK: a, b, c refer to x, y, z, respectively
    auto [d, ...e] = C(); // OK: d refers to x; ...e refers to y and z
    auto [...f, g] = C(); // OK: ...f refers x and y; g refers to z
    auto [h, i, j, ...k] = C();    // OK: the pack k is empty
    auto [l, m, n, o, ...p] = C(); // error: structured binding size is too small
}

```

A structured binding declaration performs the binding in one of three possible ways, depending on `E`:

- Case 1: If `E` is an array type, then the names are bound to the array elements.
- Case 2: If `E` is a non-union class type and std::tuple_size<E> is a complete type with a member named `value` (regardless of the type or accessibility of such member), then the "tuple-like" binding protocol is used.
- Case 3: If `E` is a non-union class type but std::tuple_size<E> is not a complete type, then the names are bound to the accessible data members of `E`.

Each of the three cases is described in more detail below.

Each structured binding has a **referenced type**, defined in the description below. This type is the type returned by `decltype` when applied to an unparenthesized structured binding.

#### Case 1: binding an array

Each structured binding in the sb-identifier-list becomes the name of an lvalue that refers to the corresponding element of the array. The structured binding size of `E` is equal to the number of array elements.

The **referenced type** for each structured binding is the array element type. Note that if the array type `E` is cv-qualified, so is its element type.

```
int a[2] = {1, 2};
 
auto [x, y] = a;    // creates e[2], copies a into e,
                    // then x refers to e[0], y refers to e[1]
auto& [xr, yr] = a; // xr refers to a[0], yr refers to a[1]

```

#### Case 2: binding a type implementing the tuple operations

The expression std::tuple_size<E>::value must be a well-formed integral constant expression, and the structured binding size of `E` is equal to std::tuple_size<E>::value.

For each structured binding, a variable whose type is "reference to std::tuple_element<I, E>::type" is introduced: lvalue reference if its corresponding initializer is an lvalue, rvalue reference otherwise. The initializer for the Ith variable is

- e.get<I>(), if lookup for the identifier `get` in the scope of `E` by class member access lookup finds at least one declaration that is a function template whose first template parameter is a non-type parameter
- Otherwise, get<I>(e), where get is looked up by argument-dependent lookup only, ignoring non-ADL lookup.

In these initializer expressions, e is an lvalue if the type of the entity e is an lvalue reference (this only happens if the ref-qualifier is `&` or if it is `&&` and the initializer expression is an lvalue) and an xvalue otherwise (this effectively performs a kind of perfect forwarding), I is a std::size_t prvalue, and <I> is always interpreted as a template parameter list.

The variable has the same storage duration as e.

The structured binding then becomes the name of an lvalue that refers to the object bound to said variable.

The **referenced type** for the Ith structured binding is std::tuple_element<I, E>::type.

```
float x{};
char  y{};
int   z{};
 
std::tuple<float&, char&&, int> tpl(x, std::move(y), z);
const auto& [a, b, c] = tpl;
// using Tpl = const std::tuple<float&, char&&, int>;
// a names a structured binding that refers to x (initialized from get<0>(tpl))
// decltype(a) is std::tuple_element<0, Tpl>::type, i.e. float&
// b names a structured binding that refers to y (initialized from get<1>(tpl))
// decltype(b) is std::tuple_element<1, Tpl>::type, i.e. char&&
// c names a structured binding that refers to the third component of tpl, get<2>(tpl)
// decltype(c) is std::tuple_element<2, Tpl>::type, i.e. const int

```

#### Case 3: binding to data members

Every non-static data member of `E` must be a direct member of `E` or the same base class of `E`, and must be well-formed in the context of the structured binding when named as e.name. `E` may not have an anonymous union member. The structured binding size of `E` is equal to the number of non-static data members.

Each structured binding in sb-identifier-list becomes the name of an lvalue that refers to the next member of e in declaration order (bit-fields are supported); the type of the lvalue is that of e.mI, where `mI` refers to the Ith member.

The **referenced type** of the Ith structured binding is the type of e.mI if it is not a reference type, or the declared type of `mI` otherwise.

```
#include <iostream>
 
struct S
{
    mutable int x1 : 2;
    volatile double y1;
};
 
S f() { return S{1, 2.3}; }
 
int main()
{
    const auto [x, y] = f(); // x is an int lvalue identifying the 2-bit bit-field
                             // y is a const volatile double lvalue
    std::cout << x << ' ' << y << '\n';  // 1 2.3
    x = -2;   // OK
//  y = -2.;  // Error: y is const-qualified
    std::cout << x << ' ' << y << '\n';  // -2 2.3
}

```

#### Initialization order

Let valI be the object or reference named by the Ith structured binding in sb-identifier-list ﻿:

- The initialization of e is sequenced before the initialization of any valI.
- The initialization of each valI is sequenced before the initialization of any valJ where I is less than J.

### Notes

|  |  |
| --- | --- |
| Structured bindings cannot be constrained:   ```text template<class T> concept C = true;   C auto [x, y] = std::pair{1, 2}; // error: constrained ``` | (since C++20) |

The lookup for member `get` ignores accessibility as usual and also ignores the exact type of the non-type template parameter. A private template<char\*> void get(); member will cause the member interpretation to be used, even though it is ill-formed.

The portion of the declaration preceding `[` applies to the hidden variable e, not to the introduced structured bindings:

```
int a = 1, b = 2;
const auto& [x, y] = std::tie(a, b); // x and y are of type int&
auto [z, w] = std::tie(a, b);        // z and w are still of type int&
assert(&z == &a);                    // passes

```

The tuple-like interpretation is always used if std::tuple_size<E> is a complete type with a member named `value`, even if that would cause the program to be ill-formed:

```
struct A { int x; };
 
namespace std
{
    template<>
    struct tuple_size<::A> { void value(); };
}
 
auto [x] = A{}; // error; the "data member" interpretation is not considered.

```

The usual rules for reference-binding to temporaries (including lifetime-extension) apply if a ref-qualifier is present and the expression is a prvalue. In those cases the hidden variable e is a reference that binds to the temporary variable materialized from the prvalue expression, extending its lifetime. As usual, the binding will fail if e is a non-const lvalue reference:

```
int a = 1;
 
const auto& [x] = std::make_tuple(a); // OK, not dangling
auto&       [y] = std::make_tuple(a); // error, cannot bind auto& to rvalue std::tuple
auto&&      [z] = std::make_tuple(a); // also OK

```

decltype(x), where x denotes a structured binding, names the **referenced type** of that structured binding. In the tuple-like case, this is the type returned by std::tuple_element, which may not be a reference even though a hidden reference is always introduced in this case. This effectively emulates the behavior of binding to a struct whose non-static data members have the types returned by std::tuple_element, with the referenceness of the binding itself being a mere implementation detail.

```
std::tuple<int, int&> f();
 
auto [x, y] = f();       // decltype(x) is int
                         // decltype(y) is int&
 
const auto [z, w] = f(); // decltype(z) is const int
                         // decltype(w) is int&

```

|  |  |
| --- | --- |
| Structured bindings cannot be captured by lambda expressions:   ```text #include <cassert>   int main() {     struct S { int p{6}, q{7}; };     const auto& [b, d] = S{};     auto l = [b, d] { return b * d; }; // valid since C++20     assert(l() == 42); } ``` | (until C++20) |

|  |  |
| --- | --- |
| A structured binding size is allowed to be ​0​ as long as the sb-identifier-list contains exactly one identifier that can only introduce an empty structured binding pack.   ```text auto return_empty() -> std::tuple<>;   template <class> void test_empty() {     auto [] = return_empty(); // error     auto [...args] = return_empty(); // OK, args is an empty pack     auto [one, ...rest] = return_empty(); // error, structured binding size is too small } ``` | (since C++26) |

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_structured_bindings` | `201606L` | (C++17) | Structured bindings |
| `202403L` | (C++26) | Structured bindings with attributes |
| `202411L` | (C++26) | Structured bindings can introduce a pack |

### Keywords

auto

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <set>
#include <string>
 
int main()
{
    std::set<std::string> myset{"hello"};
 
    for (int i{2}; i; --i)
    {
        if (auto [iter, success] = myset.insert("Hello"); success) 
            std::cout << "Insert is successful. The value is "
                      << std::quoted(*iter) << ".\n";
        else
            std::cout << "The value " << std::quoted(*iter)
                      << " already exists in the set.\n";
    }
 
    struct BitFields
    {
        // C++20: default member initializer for bit-fields
        int b : 4 {1}, d : 4 {2}, p : 4 {3}, q : 4 {4};
    };
 
    {
        const auto [b, d, p, q] = BitFields{};
        std::cout << b << ' ' << d << ' ' << p << ' ' << q << '\n';
    }
 
    {
        const auto [b, d, p, q] = []{ return BitFields{4, 3, 2, 1}; }();
        std::cout << b << ' ' << d << ' ' << p << ' ' << q << '\n';
    }
 
    {
        BitFields s;
 
        auto& [b, d, p, q] = s;
        std::cout << b << ' ' << d << ' ' << p << ' ' << q << '\n';
 
        b = 4, d = 3, p = 2, q = 1;
        std::cout << s.b << ' ' << s.d << ' ' << s.p << ' ' << s.q << '\n';
    }
}

```

Output:

```
Insert is successful. The value is "Hello".
The value "Hello" already exists in the set.
1 2 3 4
4 3 2 1
1 2 3 4
4 3 2 1

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 2285 | C++17 | expression could refer to the names from identifier-list | the declaration is ill-formed in this case |
| CWG 2312 | C++17 | the meaning of mutable was lost in case 3 | its meaning is still kept |
| CWG 2313 | C++17 | in case 2, the structure binding variables could be redeclared | cannot be redeclared |
| CWG 2339 | C++17 | in case 2, the definition of I was missing | added the definition |
| CWG 2341 (P1091R3) | C++17 | structured bindings could not be declared with static storage duration | allowed |
| CWG 2386 | C++17 | the “tuple-like” binding protocol was used whenever std::tuple_size<E> is a complete type | used only when std::tuple_size<E> has a member `value` |
| CWG 2506 | C++17 | if expression is of a cv-qualified array type, the cv-qualification was carried over to `E` | discards that cv-qualification |
| CWG 2635 | C++20 | structured bindings could be constrained | prohibited |
| CWG 2867 | C++17 | the initialization order was unclear | made clear |
| P0961R1 | C++17 | in case 2, member `get` was used if lookup finds a `get` of any kind | only if lookup finds a function template with a non-type parameter |
| P0969R0 | C++17 | in case 3, the members were required to be public | only required to be accessible in the context of the declaration |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 9.6 Structured binding declarations [dcl.struct.bind] (p: 228-229)

- C++20 standard (ISO/IEC 14882:2020):

:   - 9.6 Structured binding declarations [dcl.struct.bind] (p: 219-220)

- C++17 standard (ISO/IEC 14882:2017):

:   - 11.5 Structured binding declarations [dcl.struct.bind] (p: 219-220)

### See also

|  |  |
| --- | --- |
| tie(C++11) | creates a tuple of lvalue references or unpacks a tuple into individual objects   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/structured_binding&oldid=179317>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 January 2025, at 01:00.