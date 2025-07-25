# Templates

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
| ****Templates**** | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

 ****Templates****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Parameters and arguments | | | | |
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

A template is a C++ entity that defines one of the following:

- a family of classes (class template), which may be nested classes
- a family of functions (function template), which may be member functions

|  |  |
| --- | --- |
| - an alias to a family of types (alias template) | (since C++11) |

|  |  |
| --- | --- |
| - a family of variables (variable template) | (since C++14) |

|  |  |
| --- | --- |
| - a concept (constraints and concepts) | (since C++20) |

Templates are parameterized by one or more template parameters, of three kinds: type template parameters, non-type template parameters, and template template parameters.

When template arguments are provided, or, for function  and class(since C++17) templates only, deduced, they are substituted for the template parameters to obtain a **specialization** of the template, that is, a specific type or a specific function lvalue.

Specializations may also be provided explicitly: full specializations are allowed for class, variable(since C++14) and function templates, partial specializations are only allowed for class templates and variable templates(since C++14).

When a class template specialization is referenced in context that requires a complete object type, or when a function template specialization is referenced in context that requires a function definition to exist, the template is **instantiated** (the code for it is actually compiled), unless the template was already explicitly specialized or explicitly instantiated. Instantiation of a class template does not instantiate any of its member functions unless they are also used. At link time, identical instantiations generated by different translation units are merged.

The definition of a class template must be visible at the point of implicit instantiation, which is why template libraries typically provide all template definitions in the headers (e.g. most boost libraries are header-only).

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `template <`parameter-list ﻿`>` requires-clause ﻿(optional) declaration | (1) |  |
|  | | | | | | | | | |
| `export template <`parameter-list ﻿`>` declaration | (2) | (until C++11) |
|  | | | | | | | | | |
| `template <`parameter-list ﻿`> concept` concept-name `=` constraint-expression ﻿`;` | (3) | (since C++20) |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| parameter-list | - | a non-empty comma-separated list of the template parameters, each of which is either non-type parameter, a type parameter, a template parameter, or a parameter pack of any of those(since C++11). |
| requires-clause | - | (since C++20) a requires-clause that specifies the constraints on the template arguments. |
| declaration | - | declaration of a class (including struct and union), a member class or member enumeration type, a function or member function, a static data member at namespace scope, a variable or static data member at class scope(since C++14), or an alias template(since C++11). It may also define a template specialization. |
| concept-name constraint-expression | - | see constraints and concepts |

|  |  |
| --- | --- |
| export was an optional modifier which declared the template as **exported** (when used with a class template, it declared all of its members exported as well). Files that instantiated exported templates did not need to include their definitions: the declaration was sufficient. Implementations of export were rare and disagreed with each other on details. | (until C++11) |

|  |  |
| --- | --- |
|  | This section is incomplete Reason: core syntax, template parameters, and instantiations, take content common between class_template and function_template |

### Template identifiers

A template identifier has one of the following syntaxes:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| template-name ﻿`<`template-argument-list ﻿(optional)`>` | (1) |  |
|  | | | | | | | | | |
| `operator`op ﻿`<`template-argument-list ﻿(optional)`>` | (2) |  |
|  | | | | | | | | | |
| `operator ""` identifier `<`template-argument-list ﻿(optional)`>` | (3) | (since C++11) (deprecated) |
|  | | | | | | | | | |
| `operator` user-defined-string-literal `<`template-argument-list ﻿(optional)`>` | (4) | (since C++11) |
|  | | | | | | | | | |

1) A **simple template identifier**.2) An operator function template identifier.3,4) A literal operator function template identifier.

|  |  |  |
| --- | --- | --- |
| template-name | - | an identifier that names a template |
| op | - | an overloadable operator |
| identifier | - | an identifier |
| user-defined-string-literal | - | "" followed by an identifier |

A simple template identifier that names a class template specialization names a class.

A template identifier that names an alias template specialization names a type.

A template identifier that names a function template specialization names a function.

If all following conditions are satisfied, a template identifier is **valid** ﻿:

- There are at most as many arguments as there are parameters or a parameter is a template parameter pack(since C++11).
- There is an argument for each non-deducible non-pack(since C++11) parameter that does not have a default template argument.
- Each template argument matches the corresponding template parameter.
- Substitution of each template argument into the following template parameters (if any) succeeds.

|  |  |
| --- | --- |
| - If the template identifier is non-dependent, the associated constraints are satisfied as specified below. | (since C++20) |

An invalid simple template id is a compile-time error, unless it names a function template specialization (in which case SFINAE may apply).

```
template<class T, T::type n = 0>
class X;
 
struct S
{
    using type = int;
};
 
using T1 = X<S, int, int>; // error: too many arguments
using T2 = X<>;            // error: no default argument for first template parameter
using T3 = X<1>;           // error: value 1 does not match type-parameter
using T4 = X<int>;         // error: substitution failure for second template parameter
using T5 = X<S>;           // OK

```

|  |  |
| --- | --- |
| When the template-name of a simple template id names a constrained non-function template or a constrained template template parameter, but not a member template that is a member of an unknown specialization, and all template arguments in the simple template id are non-dependent, the associated constraints of the constrained template must be satisfied:   ```text template<typename T> concept C1 = sizeof(T) != sizeof(int);   template<C1 T> struct S1 {};   template<C1 T> using Ptr = T*;   S1<int>* p;                      // error: constraints not satisfied Ptr<int> p;                      // error: constraints not satisfied   template<typename T> struct S2 { Ptr<int> x; };       // error, no diagnostic required   template<typename T> struct S3 { Ptr<T> x; };         // OK, satisfaction is not required   S3<int> x;                       // error: constraints not satisfied   template<template<C1 T> class X> struct S4 {     X<int> x;                    // error, no diagnostic required };   template<typename T> concept C2 = sizeof(T) == 1;   template<C2 T> struct S {};   template struct S<char[2]>;      // error: constraints not satisfied template<> struct S<char[2]> {}; // error: constraints not satisfied ``` | (since C++20) |

If all following conditions are satisfied, two template identifiers are **same** ﻿:

- Their template-name ﻿s or operators refer to the same template.
- Their corresponding type template arguments are the same type.
- The template parameter values determined by their corresponding non-type template arguments are template-argument-equivalent.
- Their corresponding template template arguments refer to the same template.

Two template identifier that are the same refer to the same variable,(since C++14) class, or function.

### Templated entity

A **templated entity** (or, in some sources, "temploid") is any entity that is defined (or, for a lambda expression, created)(since C++11) within a template definition. All of the following are templated entities:

- a class/function/variable(since C++14) template

|  |  |
| --- | --- |
| - a concept | (since C++20) |

- a member of a templated entity (such as a non-template member function of a class template)
- an enumerator of an enumeration that is a templated entity
- any entity defined or created within a templated entity: a local class, a local variable, a friend function, etc

|  |  |
| --- | --- |
| - the closure type of a lambda expression that appears in the declaration of a templated entity | (since C++11) |

For example, in

```
template<typename T>
struct A
{
    void f() {}
};

```

the function `A::f` is not a function template, but is still considered to be templated.

A **templated function** is a function template or a function that is templated.

A **templated class** is a class template or a class that is templated.

|  |  |
| --- | --- |
| A **templated variable** is a variable template or a variable that is templated. | (since C++14) |

### Keywords

template,
export

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 2293 | C++98 | the rules of determining whether a template identifier is valid were not provided | provided |
| CWG 2682 | C++98 C++14 | the definitions of templated function/template class (C++98)/templated variable (C++14) were missing | added |
| P2308R1 | C++98 | two template identifiers were different if their corresponding non-type template arguments are not template-argument-equivalent | they are different if their corresponding non-type template parameter values are not template-argument-equivalent |

### See also

|  |  |
| --- | --- |
| C documentation for Generic selection | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/templates&oldid=175216>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 August 2024, at 17:13.