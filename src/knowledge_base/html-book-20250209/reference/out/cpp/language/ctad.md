# Class template argument deduction (CTAD) (since C++17)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Overview | | | | | | Declaration syntax | | | | | | **decl-specifier-seq** | | | | | | Declarator | | | | | | Conflicting declarations | | | | | | Specifiers | | | | | | typedef | | | | | | inline | | | | | | virtual function specifier | | | | | | explicit function specifier | | | | | | friend | | | | | | constexpr(C++11) | | | | | | consteval(C++20) | | | | | | constinit(C++20) | | | | | | Storage class specifiers | | | | | | Translation-unit-local (C++20) | | | | | | class/struct | | | | | | union | | | | | | enum | | | | | | decltype(C++11) | | | | | | auto(C++11) | | | | | | alignas(C++11) | | | | | | constvolatile | | | | | | Pack indexing specifier (C++26) | | | | | | Elaborated type specifier | | | | | | Attributes (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Declarators | | | | | | Reference | | | | | | Pointer | | | | | | Array | | | | | | Block declarations | | | | | | Simple-declaration | | | | | | →Structured binding declaration (C++17) | | | | | | Alias declaration (C++11) | | | | | | Namespace alias definition | | | | | | using declaration | | | | | | `using` directive | | | | | | static_assert declaration (C++11) | | | | | | asm declaration | | | | | | Opaque enum declaration (C++11) | | | | | | Other declarations | | | | | | Namespace definition | | | | | | Function declaration | | | | | | Class template declaration | | | | | | Function template declaration | | | | | | Explicit template instantiation (C++11) | | | | | | Explicit template specialization | | | | | | Linkage specification | | | | | | Attribute declaration (C++11) | | | | | | Empty declaration | | | | | |  | | | | | |

 Expressions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | Constant expressions | | | | | | Primary expressions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lambda expressions (C++11) | | | | | | Requires expressions (C++20) | | | | | | Pack indexing expression (C++26) | | | | | | Potentially-evaluated expressions | | | | | |
| Literals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Integer literals | | | | | | Floating-point literals | | | | | | Boolean literals | | | | | | Character literals | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Escape sequences | | | | | | String literals | | | | | | Null pointer literal (C++11) | | | | | | User-defined literal (C++11) | | | | | |
| Operators | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

 Templates

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Parameters and arguments | | | | |
| Class templates | | | | |
| Function templates | | | | |
| Class member templates | | | | |
| Variable templates (C++14) | | | | |
| Template argument deduction | | | | |
| ****Class template argument deduction**** (C++17) | | | | |
| Explicit (full) specialization | | | | |
| Partial specialization | | | | |
| Dependent names | | | | |
| Packs (C++11) | | | | |
| `sizeof...` (C++11) | | | | |
| Fold expressions (C++17) | | | | |
| Pack indexing (C++26) | | | | |
| SFINAE | | | | |
| Constraints and concepts (C++20) | | | | |
| Requires expression (C++20) | | | | |

In order to instantiate a class template, every template argument must be known, but not every template argument has to be specified. In the following contexts the compiler will deduce the template arguments from the type of the initializer:

- any declaration that specifies initialization of a variable and variable template, whose declared type is the class template (possibly cv-qualified):

```
std::pair p(2, 4.5);     // deduces to std::pair<int, double> p(2, 4.5);
std::tuple t(4, 3, 2.5); // same as auto t = std::make_tuple(4, 3, 2.5);
std::less l;             // same as std::less<void> l;

```

- new-expressions:

```
template<class T>
struct A
{
    A(T, T);
};
 
auto y = new A{1, 2}; // allocated type is A<int>

```

- function-style cast expressions:

```
auto lck = std::lock_guard(mtx);     // deduces to std::lock_guard<std::mutex>
std::copy_n(vi1, 3,
    std::back_insert_iterator(vi2)); // deduces to std::back_insert_iterator<T>,
                                     // where T is the type of the container vi2
std::for_each(vi.begin(), vi.end(),
    Foo(& {...}));          // deduces to Foo<T>,
                                     // where T is the unique lambda type

```

|  |  |
| --- | --- |
| - the type of a non-type template parameter:  ```text template<class T> struct X {     constexpr X(T) {} };   template<X x> struct Y {};   Y<0> y; // OK, Y<X<int>(0)> ``` | (since C++20) |

### Deduction for class templates

#### Implicitly-generated deduction guides

When, in a function-style cast or in a variable's declaration, the type specifier consists solely
of the name of a primary class template `C` (i.e., there is no accompanying template argument list), candidates for deduction are formed as follows:

- If `C` is defined, for each constructor (or constructor template) `Ci` declared in the named primary template, a fictional function template `Fi`, is constructed, such that all following conditions are satisfied:

:   - The template parameters of `Fi` are the template parameters of `C` followed (if `Ci` is a constructor template) by the template parameters of `Ci` (default template arguments are included too).

|  |  |
| --- | --- |
| - The associated constraints of `Fi` are the conjunction of the associated constraints of `C` and the associated constraints of `Ci`. | (since C++20) |

:   - The parameter list of `Fi` is the parameter list of `Ci`.
    - The return type of `Fi` is `C` followed by the template parameters of the class template enclosed in `<>`.

- If `C` is not defined or does not declare any constructors, an additional fictional function template is added, derived as above from a hypothetical constructor `C()`.

- In any case, an additional fictional function template derived as above from a hypothetical constructor `C(C)` is added, called the copy deduction candidate.

- For each user-defined deduction guide `Gi`, a fictional function or function template `Fi`, is constructed, such that all following conditions are satisfied:

:   - The parameter list of `Fi` is the parameter list of `Gi`.
    - The return type of `Fi` is the simple template identifier of `Gi`.
    - If `Gi` has template parameters (syntax (2)), `Fi` is a function template, and its template parameter list is the template parameter list of `Gi`. Otherwise, `Fi` is a function.

|  |  |
| --- | --- |
| - In addition, if   - `C` is defined and satisfies the requirements of an aggregate type with the assumption that any dependent base class has no virtual functions or virtual base classes, - there are no user-defined deduction guides for `C`, and - the variable is initialized from a non-empty list of initializers arg1, arg2, ..., argn (which may use designated initializer),  an aggregate deduction candidate may be added. The parameter list of the aggregate deduction candidate is produced from the aggregate element types, as follows:  - Let `ei` be the (possibly recursive) aggregate element that would be initialized from `argi`, where   - brace elision is not considered for any aggregate element that has   - a dependent non-array type, - an array type with a value-dependent bound, or - an array type with a dependent array element type and `argi` is a string literal   - if `C` (or its element that is itself an aggregate) has a base that is a pack expansion:   - if the pack expansion is a trailing aggregate element, it is considered to match all remaining elements of the initializer list; - otherwise, the pack is considered to be empty.   - If there is no such `ei`, the aggregate deduction candidate is not added. - Otherwise, determine the parameter list `T1, T2, ..., Tn` of the aggregate deduction candidate as follows:   - If `ei` is an array and `argi` is a braced-init-list ﻿, `Ti` is an rvalue reference to the declared type of `ei`. - If `ei` is an array and `argi` is a string literal, `Ti` is an lvalue reference to the const-qualified declared type of `ei`. - Otherwise, `Ti` is the declared type of `ei`. - If a pack was skipped because it is a non-trailing aggregate element, an additional parameter pack of the form `Pj ...` is inserted in its original aggregate element position. (This will generally cause deduction to fail.) - If a pack is a trailing aggregate element, the trailing sequence of parameters corresponding to it is replaced by a single parameter of the form `Tn ...`.  The aggregate deduction candidate is a fictional function template derived as above from a hypothetical constructor `C(T1, T2, ..., Tn)`.  During template argument deduction for the aggregate deduction candidate, the number of elements in a trailing parameter pack is only deduced from the number of remaining function arguments if it is not otherwise deduced.   ```text template<class T> struct A {     T t;       struct     {         long a, b;     } u; };   A a{1, 2, 3}; // aggregate deduction candidate: //   template<class T> //   A<T> F(T, long, long);   template<class... Args> struct B : std::tuple<Args...>, Args... {};   B b{std::tuple<std::any, std::string>{}, std::any{}}; // aggregate deduction candidate: //   template<class... Args> //   B<Args...> F(std::tuple<Args...>, Args...);   // type of b is deduced as B<std::any, std::string> ``` | (since C++20) |

Template argument deduction and overload resolution is then performed for initialization of a fictional object of hypothetical class type, whose constructor signatures match the guides (except for return type) for the purpose of forming an overload set, and the initializer is provided by the context in which class template argument deduction was performed, except that the first phase of list-initialization (considering initializer-list constructors) is omitted if the initializer list consists of a single expression of type (possibly cv-qualified) `U`, where `U` is a specialization of `C` or a class derived from a specialization of `C`.

These fictional constructors are public members of the hypothetical class type. They are explicit if the guide was formed from an explicit constructor. If overload resolution fails, the program is ill-formed. Otherwise, the return type of the selected `F` template specialization becomes the deduced class template specialization.

```
template<class T>
struct UniquePtr
{
    UniquePtr(T* t);
};
 
UniquePtr dp{new auto(2.0)};
 
// One declared constructor:
// C1: UniquePtr(T*);
 
// Set of implicitly-generated deduction guides:
 
// F1: template<class T>
//     UniquePtr<T> F(T* p);
 
// F2: template<class T> 
//     UniquePtr<T> F(UniquePtr<T>); // copy deduction candidate
 
// imaginary class to initialize:
// struct X
// {
//     template<class T>
//     X(T* p);         // from F1
//     
//     template<class T>
//     X(UniquePtr<T>); // from F2
// };
 
// direct-initialization of an X object
// with "new double(2.0)" as the initializer
// selects the constructor that corresponds to the guide F1 with T = double
// For F1 with T=double, the return type is UniquePtr<double>
 
// result:
// UniquePtr<double> dp{new auto(2.0)}

```

Or, for a more complex example (note: "`S::N`" would not compile: scope resolution qualifiers are not something that can be deduced):

```
template<class T>
struct S
{
    template<class U>
    struct N
    {
        N(T);
        N(T, U);
 
        template<class V>
        N(V, U);
    };
};
 
S<int>::N x{2.0, 1};
 
// the implicitly-generated deduction guides are (note that T is already known to be int)
 
// F1: template<class U>
//     S<int>::N<U> F(int);
 
// F2: template<class U>
//     S<int>::N<U> F(int, U);
 
// F3: template<class U, class V>
//     S<int>::N<U> F(V, U);
 
// F4: template<class U>
//     S<int>::N<U> F(S<int>::N<U>); (copy deduction candidate)
 
// Overload resolution for direct-list-init with "{2.0, 1}" as the initializer
// chooses F3 with U=int and V=double.
// The return type is S<int>::N<int>
 
// result:
// S<int>::N<int> x{2.0, 1};

```

#### User-defined deduction guides

The syntax of a user-defined deduction guide is the syntax of a function (template) declaration with a trailing return type, except that it uses the name of a class template as the function name:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| explicit ﻿(optional) template-name `(` parameter-list `)` `->` simple-template-id requires-clause ﻿(optional) `;` | (1) |  |
|  | | | | | | | | | |
| `template <`template-parameter-list ﻿`>` requires-clause ﻿(optional) explicit ﻿(optional) template-name `(` parameter-list `)` `->` simple-template-id requires-clause ﻿(optional) `;` | (2) |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| template-parameter-list | - | a non-empty comma-separated list of template parameters |
| explicit | - | an `explicit` specifier |
| template-name | - | the name of the class template whose arguments are to be deduced |
| parameter-list | - | a (possibly empty) parameter list |
| simple-template-id | - | a simple template identifier |
| requires-clause | - | (since C++20) a requires clause |

|  |  |
| --- | --- |
| The parameters of user-defined deduction guides cannot have placeholder types: the abbreviated function template syntax is not allowed. | (since C++20) |

User-defined deduction guides must name a class template and must be introduced within the same semantic scope of the class template (which could be namespace or enclosing class) and, for a member class template, must have the same access, but deduction guides do not become members of that scope.

A deduction guide is not a function and does not have a body. Deduction guides are not found by name lookup and do not participate in overload resolution except for the overload resolution against other deduction guides when deducing class template arguments. Deduction guides cannot be redeclared in the same translation unit for the same class template.

```
// declaration of the template
template<class T>
struct container
{
    container(T t) {}
 
    template<class Iter>
    container(Iter beg, Iter end);
};
 
// additional deduction guide
template<class Iter>
container(Iter b, Iter e) -> container<typename std::iterator_traits<Iter>::value_type>;
 
// uses
container c(7); // OK: deduces T=int using an implicitly-generated guide
std::vector<double> v = {/* ... */};
auto d = container(v.begin(), v.end()); // OK: deduces T=double
container e{5, 6}; // Error: there is no std::iterator_traits<int>::value_type

```

The fictional constructors for the purpose of overload resolution (described above) are explicit if they correspond to an implicitly-generated deduction guide formed from an explicit constructor or to a user-defined deduction guide that is declared explicit. As always, such constructors are ignored in copy-initialization context:

```
template<class T>
struct A
{
    explicit A(const T&, ...) noexcept; // #1
    A(T&&, ...);                        // #2
};
 
int i;
A a1 = {i, i}; // error: cannot deduce from rvalue reference in #2,
               // and #1 is explicit, and not considered in copy-initialization.
A a2{i, i};    // OK, #1 deduces to A<int> and also initializes
A a3{0, i};    // OK, #2 deduces to A<int> and also initializes
A a4 = {0, i}; // OK, #2 deduces to A<int> and also initializes
 
template<class T>
A(const T&, const T&) -> A<T&>; // #3
 
template<class T>
explicit A(T&&, T&&)  -> A<T>;  // #4
 
A a5 = {0, 1}; // error: #3 deduces to A<int&>
               // and #1 & #2 result in same parameter constructors.
A a6{0, 1};    // OK, #4 deduces to A<int> and #2 initializes
A a7 = {0, i}; // error: #3 deduces to A<int&>
A a8{0, i};    // error: #3 deduces to A<int&>

```

Using a member typedef or alias template in a constructor or constructor template's parameter list does not, by itself, render the corresponding parameter of the implicitly generated guide a non-deduced context.

```
template<class T>
struct B
{
    template<class U>
    using TA = T;
 
    template<class U>
    B(U, TA<U>); // #1
};
 
// Implicit deduction guide generated from #1 is the equivalent of
//     template<class T, class U>
//     B(U, T) -> B<T>;
// rather than
//     template<class T, class U>
//     B(U, typename B<T>::template TA<U>) -> B<T>;
// which would not have been deducible
 
B b{(int*)0, (char*)0}; // OK, deduces B<char*>

```

|  |  |
| --- | --- |
| Deduction for alias templates When a function-style cast or declaration of a variable uses the name of an alias template `A` without an argument list as the type specifier, where `A` is defined as an alias of `B<ArgList>`, the scope of `B` is non-dependent, and `B` is either a class template or a similarly-defined alias template, deduction will proceed in the same way as for class templates, except that the guides are instead generated from the guides of `B`, as follows:   - For each guide `f` of `B`, deduce the template arguments of the return type of `f` from `B<ArgList>` using template argument deduction, except that deduction does not fail if some arguments are not deduced. If deduction fails for another reason, proceed with an empty set of deduced template arguments. - Substitute the result of above deduction into `f`, if substitution fails, no guide is produced; otherwise, let `g` denote the result of substitution, a guide `f'` is formed, such that   - The parameter types and the return type of `f'` are the same as `g` - If `f` is a template, `f'` is a function template whose template parameter list consists of all the template parameters of `A` (including their default template arguments) that appear in the above deductions or (recursively) in their default template arguments, followed by the template parameters of `f` that were not deduced (including their default template arguments); otherwise (`f` is not a template), `f'` is a function - The associated constraints of `f'` are the conjunction of the associated constraints of `g` and a constraint that is satisfied if and only if the arguments of `A` are deducible from the result type   ```text template<class T> class unique_ptr {     /* ... */ };   template<class T> class unique_ptr<T[]> {     /* ... */ };   template<class T> unique_ptr(T*) -> unique_ptr<T>;   // #1   template<class T> unique_ptr(T*) -> unique_ptr<T[]>; // #2   template<class T> concept NonArray = !std::is_array_v<T>;   template<NonArray A> using unique_ptr_nonarray = unique_ptr<A>;   template<class A> using unique_ptr_array = unique_ptr<A[]>;   // generated guide for unique_ptr_nonarray:   // from #1 (deduction of unique_ptr<T> from unique_ptr<A> yields T = A): // template<class A> //     requires(argument_of_unique_ptr_nonarray_is_deducible_from<unique_ptr<A>>) // auto F(A*) -> unique_ptr<A>;   // from #2 (deduction of unique_ptr<T[]> from unique_ptr<A> yields nothing): // template<class T> //     requires(argument_of_unique_ptr_nonarray_is_deducible_from<unique_ptr<T[]>>) // auto F(T*) -> unique_ptr<T[]>;   // where argument_of_unique_ptr_nonarray_is_deducible_from can be defined as   // template<class> // class AA;   // template<NonArray A> // class AA<unique_ptr_nonarray<A>> {};   // template<class T> // concept argument_of_unique_ptr_nonarray_is_deducible_from = //     requires { sizeof(AA<T>); };   // generated guide for unique_ptr_array:   // from #1 (deduction of unique_ptr<T> from unique_ptr<A[]> yields T = A[]): // template<class A> //     requires(argument_of_unique_ptr_array_is_deducible_from<unique_ptr<A[]>>) // auto F(A(*)[]) -> unique_ptr<A[]>;   // from #2 (deduction of unique_ptr<T[]> from unique_ptr<A[]> yields T = A): // template<class A> //     requires(argument_of_unique_ptr_array_is_deducible_from<unique_ptr<A[]>>) // auto F(A*) -> unique_ptr<A[]>;   // where argument_of_unique_ptr_array_is_deducible_from can be defined as   // template<class> // class BB;   // template<class A> // class BB<unique_ptr_array<A>> {};   // template<class T> // concept argument_of_unique_ptr_array_is_deducible_from = //     requires { sizeof(BB<T>); };   // Use: unique_ptr_nonarray p(new int); // deduced to unique_ptr<int> // deduction guide generated from #1 returns unique_ptr<int> // deduction guide generated from #2 returns unique_ptr<int[]>, which is ignored because //   argument_of_unique_ptr_nonarray_is_deducible_from<unique_ptr<int[]>> is unsatisfied   unique_ptr_array q(new int[42]); // deduced to unique_ptr<int[]> // deduction guide generated from #1 fails (cannot deduce A in A(*)[] from new int[42]) // deduction guide generated from #2 returns unique_ptr<int[]> ``` | (since C++20) |

### Notes

Class template argument deduction is only performed if no template argument list is present. If a template argument list is specified, deduction does not take place.

```
std::tuple t1(1, 2, 3);                // OK: deduction
std::tuple<int, int, int> t2(1, 2, 3); // OK: all arguments are provided
 
std::tuple<> t3(1, 2, 3);    // Error: no matching constructor in tuple<>.
                             //        No deduction performed.
std::tuple<int> t4(1, 2, 3); // Error

```

|  |  |
| --- | --- |
| Class template argument deduction of aggregates typically requires user-defined deduction guides:   ```text template<class A, class B> struct Agg {     A a;     B b; }; // implicitly-generated guides are formed from default, copy, and move constructors   template<class A, class B> Agg(A a, B b) -> Agg<A, B>; // ^ This deduction guide can be implicitly generated in C++20   Agg agg{1, 2.0}; // deduced to Agg<int, double> from the user-defined guide   template<class... T> array(T&&... t) -> array<std::common_type_t<T...>, sizeof...(T)>; auto a = array{1, 2, 5u}; // deduced to array<unsigned, 3> from the user-defined guide ``` | (until C++20) |

User-defined deduction guides do not have to be templates:

```
template<class T>
struct S
{
    S(T);
};
S(char const*) -> S<std::string>;
 
S s{"hello"}; // deduced to S<std::string>

```

Within the scope of a class template, the name of the template without a parameter list is an injected class name, and can be used as a type. In that case, class argument deduction does not happen and template parameters must be supplied explicitly:

```
template<class T>
struct X
{
    X(T) {}
 
    template<class Iter>
    X(Iter b, Iter e) {}
 
    template<class Iter>
    auto foo(Iter b, Iter e)
    {
        return X(b, e); // no deduction: X is the current X<T>
    }
 
    template<class Iter>
    auto bar(Iter b, Iter e)
    {
        return X<typename Iter::value_type>(b, e); // must specify what we want
    }
 
    auto baz()
    {
        return ::X(0); // not the injected-class-name; deduced to be X<int>
    }
};

```

In overload resolution, partial ordering takes precedence over whether a function template is generated from a user-defined deduction guide: if the function template generated from the constructor is more specialized than the one generated from the user-defined deduction guide, the one generated from the constructor is chosen. Because the copy deduction candidate is typically more specialized than a wrapping constructor, this rule means that copying is generally preferred over wrapping.

```
template<class T>
struct A
{
    A(T, int*);     // #1
    A(A<T>&, int*); // #2
 
    enum { value };
};
 
template<class T, int N = T::value>
A(T&&, int*) -> A<T>; //#3
 
A a{1, 0}; // uses #1 to deduce A<int> and initializes with #1
A b{a, 0}; // uses #2 (more specialized than #3) to deduce A<int> and initializes with #2

```

When earlier tiebreakers, including partial ordering, failed to distinguish between two candidate function templates, the following rules apply:

- A function template generated from a user-defined deduction guide is preferred over one implicitly generated from a constructor or constructor template.
- The copy deduction candidate is preferred over all other function templates implicitly generated from a constructor or constructor template.
- A function template implicitly generated from a non-template constructor is preferred over a function template implicitly generated from a constructor template.

```
template<class T>
struct A
{
    using value_type = T;
 
    A(value_type); // #1
    A(const A&);   // #2
    A(T, T, int);  // #3
 
    template<class U>
    A(int, T, U);  // #4
};                 // #5, the copy deduction candidate A(A);
 
A x(1, 2, 3); // uses #3, generated from a non-template constructor
 
template<class T>
A(T) -> A<T>; // #6, less specialized than #5
 
A a(42); // uses #6 to deduce A<int> and #1 to initialize
A b = a; // uses #5 to deduce A<int> and #2 to initialize
 
template<class T>
A(A<T>) -> A<A<T>>; // #7, as specialized as #5
 
A b2 = a; // uses #7 to deduce A<A<int>> and #1 to initialize

```

An rvalue reference to a cv-unqualified template parameter is not a forwarding reference if that parameter is a class template parameter:

```
template<class T>
struct A
{
    template<class U>
    A(T&&, U&&, int*); // #1: T&& is not a forwarding reference
                       //     U&& is a forwarding reference
 
    A(T&&, int*);      // #2: T&& is not a forwarding reference
};
 
template<class T>
A(T&&, int*) -> A<T>; // #3: T&& is a forwarding reference
 
int i, *ip;
A a{i, 0, ip};  // error, cannot deduce from #1
A a0{0, 0, ip}; // uses #1 to deduce A<int> and #1 to initialize
A a2{i, ip};    // uses #3 to deduce A<int&> and #2 to initialize

```

When initializing from a single argument of a type that is a specialization of the class template at issue, copying deduction is generally preferred over wrapping by default:

```
std::tuple t1{1};  //std::tuple<int>
std::tuple t2{t1}; //std::tuple<int>, not std::tuple<std::tuple<int>>
 
std::vector v1{1, 2};   // std::vector<int>
std::vector v2{v1};     // std::vector<int>, not std::vector<std::vector<int>> (P0702R1)
std::vector v3{v1, v2}; // std::vector<std::vector<int>>

```

Outside the special case for copying vs. wrapping, the strong preference for initializer-list constructors in list-initialization remains intact.

```
std::vector v1{1, 2}; // std::vector<int>
 
std::vector v2(v1.begin(), v1.end()); // std::vector<int>
std::vector v3{v1.begin(), v1.end()}; // std::vector<std::vector<int>::iterator>

```

Before class template argument deduction was introduced, a common approach to avoiding explicitly specifying arguments is to use a function template:

```
std::tuple p1{1, 1.0};             //std::tuple<int, double>, using deduction
auto p2 = std::make_tuple(1, 1.0); //std::tuple<int, double>, pre-C++17

```

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_deduction_guides` | `201703L` | (C++17) | Template argument deduction for class templates |
| `201907L` | (C++20) | CTAD for aggregates and aliases |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 2376 | C++17 | CTAD would be performed even if the type of the variable declared is different from the class template whose arguments will be deduced | do not perform CTAD in this case |
| CWG 2628 | C++20 | implicit deduction guides did not propagate constraints | propogate constraints |
| CWG 2697 | C++20 | it was unclear whether the abbreviated function template syntax is allowed in user-defined deduction guides | prohibited |
| CWG 2707 | C++20 | deduction guides could not have a trailing requires clause | they can |
| CWG 2714 | C++17 | implicit deduction guides did not consider the default aguments of constructors | consider them |
| CWG 2913 | C++20 | the resolution of CWG issue 2707 made the deduction guide syntax inconsistent with the function declaration syntax | adjusted the syntax |
| P0702R1 | C++17 | an initializer-list constructor can pre-empt the copy deduction candidate, resulting in wrapping | initializer-list phase skipped when copying |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/class_template_argument_deduction&oldid=179829>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 January 2025, at 22:14.