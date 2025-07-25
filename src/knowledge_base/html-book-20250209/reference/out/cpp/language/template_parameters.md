# Template parameters and template arguments

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
| ****Parameters and arguments**** | | | | |
| Class templates | | | | |
| Function templates | | | | |
| Class member templates | | | | |
| Variable templates (C++14) | | | | |
| Template argument deduction | | | | |
| Class template argument deduction (C++17) | | | | |
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

### Template parameters

Every template is parameterized by one or more template parameters, indicated in the parameter-list of the template declaration syntax:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `template` `<` parameter-list `>` declaration | (1) |  |
|  | | | | | | | | | |
| `template` `<` parameter-list `>` `requires` constraint declaration | (2) | (since C++20) |
|  | | | | | | | | | |

Each parameter in parameter-list may be:

- a non-type template parameter;
- a type template parameter;
- a template template parameter.

#### Non-type template parameter

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| type name ﻿(optional) | (1) |  |
|  | | | | | | | | | |
| type name ﻿(optional) `=` default | (2) |  |
|  | | | | | | | | | |
| type `...` name ﻿(optional) | (3) | (since C++11) |
|  | | | | | | | | | |

1) A non-type template parameter.2) A non-type template parameter with a default template argument.3) A non-type template parameter pack.

|  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| type | - | one of the following types:  - a structural type (see below)  |  |  | | --- | --- | | - a type that contains a placeholder type | (since C++17) | | - a placeholder for a deduced class type | (since C++20) | |
| name | - | the name of the non-type template parameter |
| default | - | the default template argument |

A **structural type** is one of the following types (optionally cv-qualified, the qualifiers are ignored):

- lvalue reference type (to object or to function);
- an integral type;
- a pointer type (to object or to function);
- a pointer to member type (to member object or to member function);
- an enumeration type;

|  |  |
| --- | --- |
| - std::nullptr_t; | (since C++11) |

|  |  |
| --- | --- |
| - a floating-point type; - a lambda closure type whose lambda expression has no capture; - a non-closure literal class type with the following properties:   - all base classes and non-static data members are public and non-mutable and - the types of all base classes and non-static data members are structural types or (possibly multi-dimensional) array thereof. | (since C++20) |

Array and function types may be written in a template declaration, but they are automatically replaced by pointer to object and pointer to function as appropriate.

When the name of a non-type template parameter is used in an expression within the body of the class template, it is an unmodifiable prvalue unless its type was an lvalue reference type, or unless its type is a class type(since C++20).

A template parameter of the form class Foo is not an unnamed non-type template parameter of type `Foo`, even if otherwise class Foo is an elaborated type specifier and class Foo x; declares x to be of type `Foo`.

|  |  |
| --- | --- |
| An identifier that names a non-type template parameter of class type `T` denotes a static storage duration object of type const T, called a **template parameter object**, which is template-argument-equivalent to the corresponding template argument after it has been converted to the type of the template parameter. No two template parameter objects are template-argument-equivalent.   ```text struct A {     friend bool operator==(const A&, const A&) = default; };   template<A a> void f() {     &a;                       // OK     const A& ra = a, &rb = a; // Both bound to the same template parameter object     assert(&ra == &rb);       // passes } ``` | (since C++20) |

#### Type template parameter

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| type-parameter-key name ﻿(optional) | (1) |  |
|  | | | | | | | | | |
| type-parameter-key name ﻿(optional) `=` default | (2) |  |
|  | | | | | | | | | |
| type-parameter-key `...` name ﻿(optional) | (3) | (since C++11) |
|  | | | | | | | | | |
| type-constraint name ﻿(optional) | (4) | (since C++20) |
|  | | | | | | | | | |
| type-constraint name ﻿(optional) `=` default | (5) | (since C++20) |
|  | | | | | | | | | |
| type-constraint `...` name ﻿(optional) | (6) | (since C++20) |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| type-parameter-key | - | either `typename` or `class`. There is no difference between these keywords in a type template parameter declaration |
| type-constraint | - | either the name of a concept or the name of a concept followed by a list of template arguments (in angle brackets). Either way, the concept name may be optionally qualified |
| name | - | the name of the type template parameter |
| default | - | the default template argument |

1) A type template parameter without a default.

```
template<class T>
class My_vector { /* ... */ };

```

2) A type template parameter with a default.

```
template<class T = void>
struct My_op_functor { /* ... */ };

```

3) A type template parameter pack.

```
template<typename... Ts>
class My_tuple { /* ... */ };

```

4) A constrained type template parameter without a default.

```
template<My_concept T>
class My_constrained_vector { /* ... */ };

```

5) A constrained type template parameter with a default.

```
template<My_concept T = void>
class My_constrained_op_functor { /* ... */ };

```

6) A constrained type template parameter pack.

```
template<My_concept... Ts>
class My_constrained_tuple { /* ... */ };

```

The name of the parameter is optional:

```
// Declarations of the templates shown above:
template<class>
class My_vector;
template<class = void>
struct My_op_functor;
template<typename...>
class My_tuple;

```

In the body of the template declaration, the name of a type parameter is a typedef-name which aliases the type supplied when the template is instantiated.

|  |  |
| --- | --- |
| Each constrained parameter `P` whose type-constraint is Q designating the concept `C` introduces a constraint-expression `E` according to the following rules:   - if `Q` is `C` (without an argument list),   - if `P` is not a parameter pack, `E` is simply `C<P>` - otherwise, `P` is a parameter pack, `E` is a fold-expression `(C<P> && ...)`   - if `Q` is `C<A1,A2...,AN>`, then `E` is `C<P,A1,A2,...AN>` or `(C<P,A1,A2,...AN> && ...)`, respectively.  ```text template<typename T> concept C1 = true; template<typename... Ts> // variadic concept concept C2 = true; template<typename T, typename U> concept C3 = true;   template<C1 T>         struct s1; // constraint-expression is C1<T> template<C1... T>      struct s2; // constraint-expression is (C1<T> && ...) template<C2... T>      struct s3; // constraint-expression is (C2<T> && ...) template<C3<int> T>    struct s4; // constraint-expression is C3<T, int> template<C3<int>... T> struct s5; // constraint-expression is (C3<T, int> && ...) ``` | (since C++20) |

#### Template template parameter

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `template` `<` parameter-list `>` type-parameter-key name ﻿(optional) | (1) |  |
|  | | | | | | | | | |
| `template` `<` parameter-list `>` type-parameter-key name ﻿(optional) `=` default | (2) |  |
|  | | | | | | | | | |
| `template` `<` parameter-list `>` type-parameter-key `...` name ﻿(optional) | (3) | (since C++11) |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| type-parameter-key | - | `class` or `typename`(since C++17) |

1) A template template parameter with an optional name.2) A template template parameter with an optional name and a default.3) A template template parameter pack with an optional name.

In the body of the template declaration, the name of this parameter is a template-name (and needs arguments to be instantiated).

```
template<typename T>
class my_array {};
 
// two type template parameters and one template template parameter:
template<typename K, typename V, template<typename> typename C = my_array>
class Map
{
    C<K> key;
    C<V> value;
};

```

#### Name resolution for template parameters

The name of a template parameter is not allowed to be redeclared within its scope (including nested scopes). A template parameter is not allowed to have the same name as the template name.

```
template<class T, int N>
class Y
{
    int T;      // error: template parameter redeclared
    void f()
    {
        char T; // error: template parameter redeclared
    }
};
 
template<class X>
class X; // error: template parameter redeclared

```

In the definition of a member of a class template that appears outside of the class template definition, the name of a member of the class template hides the name of a template parameter of any enclosing class templates, but not a template parameter of the member if the member is a class or function template.

```
template<class T>
struct A
{
    struct B {};
    typedef void C;
    void f();
 
    template<class U>
    void g(U);
};
 
template<class B>
void A<B>::f()
{
    B b; // A's B, not the template parameter
}
 
template<class B>
template<class C>
void A<B>::g(C)
{
    B b; // A's B, not the template parameter
    C c; // the template parameter C, not A's C
}

```

In the definition of a member of a class template that appears outside of the namespace containing the class template definition, the name of a template parameter hides the name of a member of this namespace.

```
namespace N
{
    class C {};
 
    template<class T>
    class B
    {
        void f(T);
    };
}
 
template<class C>
void N::B<C>::f(C)
{
    C b; // C is the template parameter, not N::C
}

```

In the definition of a class template or in the definition of a member of such a template that appears outside of the template definition, for each non-dependent base class, if the name of the base class or the name of a member of the base class is the same as the name of a template parameter, the base class name or member name hides the template parameter name.

```
struct A
{
    struct B {};
    int C;
    int Y;
};
 
template<class B, class C>
struct X : A
{
    B b; // A's B
    C b; // error: A's C isn't a type name
};

```

### Template arguments

In order for a template to be instantiated, every template parameter (type, non-type, or template) must be replaced by a corresponding template argument. For class templates, the arguments are either explicitly provided, deduced from the initializer, (since C++17) or defaulted. For function templates, the arguments are explicitly provided, deduced from the context, or defaulted.

If an argument can be interpreted as both a type-id and an expression, it is always interpreted as a type-id, even if the corresponding template parameter is non-type:

```
template<class T>
void f(); // #1
 
template<int I>
void f(); // #2
 
void g()
{
    f<int()>(); // "int()" is both a type and an expression,
                // calls #1 because it is interpreted as a type
}

```

#### Template non-type arguments

|  |  |
| --- | --- |
| The template argument that can be used with a non-type template parameter can be any manifestly constant-evaluated expression. | (until C++11) |
| The template argument that can be used with a non-type template parameter can be any initializer clause. If the initializer clause is an expression, it must be manifestly constant-evaluated. | (since C++11) |

Given the type of the non-type template parameter declaration as `T` and the template argument provided for the parameter as E.

|  |  |
| --- | --- |
| The invented declaration T x = E; must satisfy the semantic constraints for the definition of a constexpr variable with static storage duration. | (since C++26) |
| If `T` contains a placeholder type, or is a placeholder for a deduced class type, the type of the template parameter is the type deduced for the variable x in the invented declaration T x = E;.  If a deduced parameter type is not a structural type, the program is ill-formed.  For non-type template parameter packs whose type uses a placeholder type, the type is independently deduced for each template argument and need not match. | (since C++17) |

```
template<auto n>
struct B { /* ... */ };
 
B<5> b1;   // OK: non-type template parameter type is int
B<'a'> b2; // OK: non-type template parameter type is char
B<2.5> b3; // error (until C++20): non-type template parameter type cannot be double
 
// C++20 deduced class type placeholder, class template arguments are deduced at the
// call site
template<std::array arr>
void f();
 
f<std::array<double, 8>{}>();
 
template<auto...>
struct C {};
 
C<'C', 0, 2L, nullptr> x; // OK

```

The value of a non-type template parameter P of (possibly deduced)(since C++17) type `T` is determined from its template argument A as follows:

|  |  |
| --- | --- |
| - If A is a converted constant expression of type `T`, the value of P is A (as converted). - Otherwise, the program is ill-formed. | (until C++11) |
| - If A is an expression:   - If A is a converted constant expression of type `T`, the value of P is A (as converted). - Otherwise, the program is ill-formed.   - Otherwise (A is a braced-enclosed initializer list), a temporary variable constexpr T v = A; is introduced. The value of P is that of v.   - The lifetime of v ends immediately after initializing it. | (since C++11) (until C++20) |
| - If `T` is not a class type and A is an expression:   - If A is a converted constant expression of type `T`, the value of P is A (as converted). - Otherwise, the program is ill-formed.   - Otherwise (`T` is a class type or A is a braced-enclosed initializer list), a temporary variable constexpr T v = A; is introduced.   - If `T` is a class type, a template parameter object exists (which is also denoted by P). P is copy-initialized from an unspecified candidate initializer that is template-argument-equivalent to v.   - The lifetime of v ends immediately after initializing it and P. - If the initialization of P satisfies any of the following conditions, the program is ill-formed:   - The initialization would be ill-formed. - The full-expression of an invented declarator-initializer sequence for the initialization would not be a constant expression when interpreted as a manifestly constant-evaluated expression. - The initialization would cause P to not be template-argument-equivalent to v.   - Otherwise, the value of P is that of v. | (since C++20) |

```
template<int i>
struct C { /* ... */ };
 
C<{42}> c1; // OK
 
template<auto n>
struct B { /* ... */ };
 
struct J1
{
    J1* self = this;
};
 
B<J1{}> j1; // error: initialization of the template parameter object
            //        is not a constant expression
 
struct J2
{
    J2 *self = this;
    constexpr J2() {}
    constexpr J2(const J2&) {}
};
 
B<J2{}> j2; // error: the template parameter object is not
            //        template-argument-equivalent to introduced temporary

```

|  |  |
| --- | --- |
| The following limitations apply when instantiating templates that have non-type template parameters:   - For integral and arithmetic types, the template argument provided during instantiation must be a converted constant expression of the template parameter's type (so certain implicit conversion applies). - For pointers to objects, the template arguments have to designate the address of a complete object with static storage duration and a linkage (either internal or external), or a constant expression that evaluates to the appropriate null pointer or std::nullptr_t(since C++11) value. - For pointers to functions, the valid arguments are pointers to functions with linkage (or constant expressions that evaluate to null pointer values). - For lvalue reference parameters, the argument provided at instantiation cannot be a temporary, an unnamed lvalue, or a named lvalue with no linkage (in other words, the argument must have linkage). - For pointers to members, the argument has to be a pointer to member expressed as &Class::Member or a constant expression that evaluates to null pointer or std::nullptr_t(since C++11) value.   In particular, this implies that string literals, addresses of array elements, and addresses of non-static members cannot be used as template arguments to instantiate templates whose corresponding non-type template parameters are pointers to objects. | (until C++17) |
| Non-type template parameters of reference or pointer type and non-static data members of reference or pointer type in a non-type template parameter of class type and its subobjects(since C++20) cannot refer to/be the address of   - a temporary object (including one created during reference initialization); - a string literal; - the result of `typeid`; - the predefined variable __func__; - or a subobject (including non-static class member, base subobject, or array element) of one of the above(since C++20). | (since C++17) |

```
template<const int* pci>
struct X {};
 
int ai[10];
X<ai> xi; // OK: array to pointer conversion and cv-qualification conversion
 
struct Y {};
 
template<const Y& b>
struct Z {};
 
Y y;
Z<y> z;   // OK: no conversion
 
template<int (&pa)[5]>
struct W {};
 
int b[5];
W<b> w;   // OK: no conversion
 
void f(char);
void f(int);
 
template<void (*pf)(int)>
struct A {};
 
A<&f> a;  // OK: overload resolution selects f(int)

```

```
template<class T, const char* p>
class X {};
 
X<int, "Studebaker"> x1; // error: string literal as template-argument
 
template<int* p>
class X {};
 
int a[10];
 
struct S
{
    int m;
    static int s;
} s;
 
X<&a[2]> x3; // error (until C++20): address of array element
X<&s.m> x4;  // error (until C++20): address of non-static member
X<&s.s> x5;  // OK: address of static member
X<&S::s> x6; // OK: address of static member
 
template<const int& CRI>
struct B {};
 
B<1> b2;     // error: temporary would be required for template argument
int c = 1;
B<c> b1;     // OK

```

#### Template type arguments

A template argument for a type template parameter must be a type-id, which may name an incomplete type:

```
template<typename T>
class X {}; // class template
 
struct A;            // incomplete type
typedef struct {} B; // type alias to an unnamed type
 
int main()
{
    X<A> x1;  // OK: 'A' names a type
    X<A*> x2; // OK: 'A*' names a type
    X<B> x3;  // OK: 'B' names a type
}

```

#### Template template arguments

A template argument for a template template parameter must be an id-expression which names a class template or a template alias.

When the argument is a class template, only the primary template is considered when matching the parameter. The partial specializations, if any, are only considered when a specialization based on this template template parameter happens to be instantiated.

```
template<typename T> // primary template
class A { int x; };
 
template<typename T> // partial specialization
class A<T*> { long x; };
 
// class template with a template template parameter V
template<template<typename> class V>
class C
{
    V<int> y;  // uses the primary template
    V<int*> z; // uses the partial specialization
};
 
C<A> c; // c.y.x has type int, c.z.x has type long

```

To match a template template argument `A` to a template template parameter `P`, `P` must be **at least as specialized** as `A` (see below). If `P`'s parameter list includes a parameter pack, zero or more template parameters (or parameter packs) from `A`'s template parameter list are matched by it.(since C++11)

Formally, a template template-parameter `P` is **at least as specialized** as a template template argument `A` if, given the following rewrite to two function templates, the function template corresponding to `P` is at least as specialized as the function template corresponding to `A` according to the partial ordering rules for function templates. Given an invented class template `X` with the template parameter list of `A` (including default arguments):

- Each of the two function templates has the same template parameters, respectively, as `P` or `A`.
- Each function template has a single function parameter whose type is a specialization of `X` with template arguments corresponding to the template parameters from the respective function template where, for each template parameter `PP` in the template parameter list of the function template, a corresponding template argument `AA` is formed. If `PP` declares a parameter pack, then `AA` is the pack expansion `PP...`; otherwise,(since C++11) `AA` is the id-expression `PP`.

If the rewrite produces an invalid type, then `P` is not at least as specialized as `A`.

```
template<typename T>
struct eval;                     // primary template
 
template<template<typename, typename...> class TT, typename T1, typename... Rest>
struct eval<TT<T1, Rest...>> {}; // partial specialization of eval
 
template<typename T1> struct A;
template<typename T1, typename T2> struct B;
template<int N> struct C;
template<typename T1, int N> struct D;
template<typename T1, typename T2, int N = 17> struct E;
 
eval<A<int>> eA;        // OK: matches partial specialization of eval
eval<B<int, float>> eB; // OK: matches partial specialization of eval
eval<C<17>> eC;         // error: C does not match TT in partial specialization
                        // because TT's first parameter is a
                        // type template parameter, while 17 does not name a type
eval<D<int, 17>> eD;    // error: D does not match TT in partial specialization
                        // because TT's second parameter is a
                        // type parameter pack, while 17 does not name a type
eval<E<int, float>> eE; // error: E does not match TT in partial specialization
                        // because E's third (default) parameter is a non-type

```

Before the adoption of P0522R0, each of the template parameters of `A` must match corresponding template parameters of `P` exactly. This hinders many reasonable template argument from being accepted.

Although it was pointed out very early (CWG#150), by the time it was resolved, the changes were applied to the C++17 working paper and the resolution became a de facto C++17 feature. Many compilers disable it by default:

- GCC disables it in all language modes prior to C++17 by default, it can only be enabled by setting a compiler flag in these modes.
- Clang disables it in all language modes by default, it can only be enabled by setting a compiler flag.
- Microsoft Visual Studio treats it as a normal C++17 feature and only enables it in C++17 and later language modes (i.e. no support in C++14 language mode, which is the default mode).

```
template<class T> class A { /* ... */ };
template<class T, class U = T> class B { /* ... */ };
template<class... Types> class C { /* ... */ };
 
template<template<class> class P> class X { /* ... */ };
X<A> xa; // OK
X<B> xb; // OK after P0522R0
         // Error earlier: not an exact match
X<C> xc; // OK after P0522R0
         // Error earlier: not an exact match
 
template<template<class...> class Q> class Y { /* ... */ };
Y<A> ya; // OK
Y<B> yb; // OK
Y<C> yc; // OK
 
template<auto n> class D { /* ... */ };   // note: C++17
template<template<int> class R> class Z { /* ... */ };
Z<D> zd; // OK after P0522R0: the template parameter
         // is more specialized than the template argument
 
template<int> struct SI { /* ... */ };
template<template<auto> class> void FA(); // note: C++17
FA<SI>(); // Error

```

#### Default template arguments

Default template arguments are specified in the parameter lists after the = sign. Defaults can be specified for any kind of template parameter (type, non-type, or template), but not to parameter packs(since C++11).

If the default is specified for a template parameter of a primary class template, primary variable template,(since C++14) or alias template, each subsequent template parameter must have a default argument, except the very last one may be a template parameter pack(since C++11). In a function template, there are no restrictions on the parameters that follow a default, and a parameter pack may be followed by more type parameters only if they have defaults or can be deduced from the function arguments(since C++11).

Default parameters are not allowed

- in the out-of-class definition of a member of a class template (they have to be provided in the declaration inside the class body). Note that member templates of non-template classes can use default parameters in their out-of-class definitions (see GCC bug 53856)
- in friend class template declarations

|  |  |
| --- | --- |
| - in any function template declaration or definition | (until C++11) |

|  |  |
| --- | --- |
| On a friend function template declaration, default template arguments are allowed only if the declaration is a definition, and no other declarations of this function appear in this translation unit. | (since C++11) |

Default template arguments that appear in the declarations are merged similarly to default function arguments:

```
template<typename T1, typename T2 = int> class A;
template<typename T1 = int, typename T2> class A;
 
// the above is the same as the following:
template<typename T1 = int, typename T2 = int> class A;

```

But the same parameter cannot be given default arguments twice in the same scope:

```
template<typename T = int> class X;
template<typename T = int> class X {}; // error

```

When parsing a default template argument for a non-type template parameter, the first non-nested > is taken as the end of the template parameter list rather than a greater-than operator:

```
template<int i = 3 > 4>   // syntax error
class X { /* ... */ };
 
template<int i = (3 > 4)> // OK
class Y { /* ... */ };

```

The template parameter lists of template template parameters can have their own default arguments, which are only in effect where the template template parameter itself is in scope:

```
// class template, with a type template parameter with a default
template<typename T = float>
struct B {};
 
// template template parameter T has a parameter list, which
// consists of one type template parameter with a default
template<template<typename = float> typename T>
struct A
{
    void f();
    void g();
};
 
// out-of-body member function template definitions
 
template<template<typename TT> class T>
void A<T>::f()
{
    T<> t; // error: TT has no default in scope
}
 
template<template<typename TT = char> class T>
void A<T>::g()
{
    T<> t; // OK: t is T<char>
}

```

Member access for the names used in a default template parameter is checked at the declaration, not at the point of use:

```
class B {};
 
template<typename T>
class C
{
protected:
    typedef T TT;
};
 
template<typename U, typename V = typename U::TT>
class D: public U {};
 
D<C<B>>* d; // error: C::TT is protected

```

|  |  |
| --- | --- |
| The default template argument is implicitly instantiated when the value of that default argument is needed, except if the template is used to name a function:   ```text template<typename T, typename U = int> struct S {};   S<bool>* p; // The default argument for U is instantiated at this point             // the type of p is S<bool, int>* ``` | (since C++14) |

#### Template argument equivalence

Template argument equivalence is used to determine whether two template identifiers are same.

Two values are **template-argument-equivalent** if they are of the same type and any of the following conditions is satisfied:

- They are of integral or enumeration type and their values are the same.
- They are of pointer type and they have the same pointer value.
- They are of pointer-to-member type and they refer to the same class member or are both the null member pointer value.
- They are of lvalue reference type and they refer to the same object or function.

|  |  |
| --- | --- |
| - They are of type std::nullptr_t. | (since C++11) |

|  |  |
| --- | --- |
| - They are of floating-point type and their values are identical. - They are of array type (in which case the arrays must be member objects of some class/union) and their corresponding elements are template-argument-equivalent. - They are of union type and either they both have no active member or they have the same active member and their active members are template-argument-equivalent. - They are of a lambda closure type. - They are of non-union class type and their corresponding direct subobjects and reference members are template-argument-equivalent. | (since C++20) |

### Notes

|  |  |
| --- | --- |
| In template parameters, type constraints could be used for both type and non-type parameters, depending on whether auto is present.   ```text template<typename> concept C = true;   template<C,     // type parameter           C auto // non-type parameter         > struct S{};   S<int, 0> s; ``` | (since C++20) |

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_nontype_template_parameter_auto` | `201606L` | (C++17) | Declaring non-type template parameters with `auto` |
| `__cpp_template_template_args` | `201611L` | (c++17) (DR) | Matching of template template-arguments |
| `__cpp_nontype_template_args` | `201411L` | (C++17) | Allow constant evaluation for all non-type template arguments |
| `201911L` | (C++20) | Class types and floating-point types in non-type template parameters |

### Examples

Run this code

```
#include <array>
#include <iostream>
#include <numeric>
 
// simple non-type template parameter
template<int N>
struct S { int a[N]; };
 
template<const char*>
struct S2 {};
 
// complicated non-type example
template
<
    char c,             // integral type
    int (&ra)[5],       // lvalue reference to object (of array type)
    int (*pf)(int),     // pointer to function
    int (S<10>::*a)[10] // pointer to member object (of type int[10])
>
struct Complicated
{
    // calls the function selected at compile time
    // and stores the result in the array selected at compile time
    void foo(char base)
    {
        ra[4] = pf(c - base);
    }
};
 
//  S2<"fail"> s2;        // error: string literal cannot be used
    char okay[] = "okay"; // static object with linkage
//  S2<&okay[0]> s3;      // error: array element has no linkage
    S2<okay> s4;          // works
 
int a[5];
int f(int n) { return n; }
 
// C++20: NTTP can be a literal class type
template<std::array arr>
constexpr
auto sum() { return std::accumulate(arr.cbegin(), arr.cend(), 0); }
 
// C++20: class template arguments are deduced at the call site
static_assert(sum<std::array<double, 8>{3, 1, 4, 1, 5, 9, 2, 6}>() == 31.0);
// C++20: NTTP argument deduction and CTAD
static_assert(sum<std::array{2, 7, 1, 8, 2, 8}>() == 28);
 
int main()
{
    S<10> s; // s.a is an array of 10 int
    s.a[9] = 4;
 
    Complicated<'2', a, f, &S<10>::a> c;
    c.foo('0');
 
    std::cout << s.a[9] << a[4] << '\n';
}

```

Output:

```
42

```

|  |  |
| --- | --- |
|  | This section is incomplete Reason: more examples |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 150 (P0522R0) | C++98 | template-template arguments had to match parameter lists of template-template parameters exactly | more specialized also allowed |
| CWG 184 | C++98 | whether the template parameters of template template parameters are allowed to have default arguments is unspecified | specification added |
| CWG 354 | C++98 | null pointer values could not be non-type template arguments | allowed |
| CWG 1398 | C++11 | template non-type arguments could not have type `std::nullptr_t` | allowed |
| CWG 1570 | C++98 | template non-type arguments could designate addresses of subobjects | not allowed |
| CWG 1922 | C++98 | it was unclear whether a class template whose name is an injected-class-name can use the default arguments in prior declarations | allowed |
| CWG 2032 | C++14 | for variable templates, there was no restriction on the template parameters after a template parameter with a default argument | apply the same restriction as on class templates and alias templates |
| CWG 2542 | C++20 | it was unclear whether the closure type is structural | it is not structural |
| CWG 2845 | C++20 | the closure type was not structural | it is structural if capture-less |
| P2308R1 | C++11 C++20 | 1. list-initialization was not allowed for     non-type template arguments (C++11) 2. it was unclear how non-type template     parameters of class types are initialized (C++20) | 1. allowed 2. made clear |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/template_parameters&oldid=179336>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 January 2025, at 18:32.