# Function template

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | ****Function template**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

Declarations

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Overview | | | | | | Declaration syntax | | | | | | **decl-specifier-seq** | | | | | | Declarator | | | | | | Conflicting declarations | | | | | | Specifiers | | | | | | typedef | | | | | | inline | | | | | | virtual function specifier | | | | | | explicit function specifier | | | | | | friend | | | | | | constexpr(C++11) | | | | | | consteval(C++20) | | | | | | constinit(C++20) | | | | | | Storage class specifiers | | | | | | Translation-unit-local (C++20) | | | | | | class/struct | | | | | | union | | | | | | enum | | | | | | decltype(C++11) | | | | | | auto(C++11) | | | | | | alignas(C++11) | | | | | | constvolatile | | | | | | Pack indexing specifier (C++26) | | | | | | Elaborated type specifier | | | | | | Attributes (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Declarators | | | | | | Reference | | | | | | Pointer | | | | | | Array | | | | | | Block declarations | | | | | | Simple-declaration | | | | | | →Structured binding declaration (C++17) | | | | | | Alias declaration (C++11) | | | | | | Namespace alias definition | | | | | | using declaration | | | | | | `using` directive | | | | | | static_assert declaration (C++11) | | | | | | asm declaration | | | | | | Opaque enum declaration (C++11) | | | | | | Other declarations | | | | | | Namespace definition | | | | | | Function declaration | | | | | | Class template declaration | | | | | | ****Function template declaration**** | | | | | | Explicit template instantiation (C++11) | | | | | | Explicit template specialization | | | | | | Linkage specification | | | | | | Attribute declaration (C++11) | | | | | | Empty declaration | | | | | |  | | | | | |

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
| ****Function templates**** | | | | |
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

A function template defines a family of functions.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `template` `<` parameter-list `>` function-declaration | (1) |  |
|  | | | | | | | | | |
| `template` `<` parameter-list `>` `requires` constraint function-declaration | (2) | (since C++20) |
|  | | | | | | | | | |
| function-declaration-with-placeholders | (3) | (since C++20) |
|  | | | | | | | | | |
| `export` `template` `<` parameter-list `>` function-declaration | (4) | (removed in C++11) |
|  | | | | | | | | | |

### Explanation

|  |  |  |
| --- | --- | --- |
| parameter-list | - | a non-empty comma-separated list of the template parameters, each of which is either non-type parameter, a type parameter, a template parameter, or a parameter pack of any of those(since C++11). As with any template, parameters may be constrained(since C++20) |
| function-declaration | - | a function declaration. The function name declared becomes a template name. |
| constraint | - | a constraint expression which restricts the template parameters accepted by this function template |
| function-declaration- with-placeholders | - | a function declaration where the type of at least one parameter uses the placeholder auto or Concept auto: the template parameter list will have one invented parameter for each placeholder (see Abbreviated function templates below) |

|  |  |
| --- | --- |
| `export` was an optional modifier which declared the template as **exported** (when used with a class template, it declared all of its members exported as well). Files that instantiated exported templates did not need to include their definitions: the declaration was sufficient. Implementations of `export` were rare and disagreed with each other on details. | (until C++11) |

|  |  |
| --- | --- |
| Abbreviated function template When placeholder types (either auto or Concept auto) appear in the parameter list of a function declaration or of a function template declaration, the declaration declares a function template, and one invented template parameter for each placeholder is appended to the template parameter list:   ```text void f1(auto); // same as template<class T> void f1(T) void f2(C1 auto); // same as template<C1 T> void f2(T), if C1 is a concept void f3(C2 auto...); // same as template<C2... Ts> void f3(Ts...), if C2 is a concept void f4(const C3 auto*, C4 auto&); // same as template<C3 T, C4 U> void f4(const T*, U&);   template<class T, C U> void g(T x, U y, C auto z); // same as template<class T, C U, C W> void g(T x, U y, W z); ```   Abbreviated function templates can be specialized like all function templates.   ```text template<> void f4<int>(const int*, const double&); // specialization of f4<int, const double> ``` | (since C++20) |

### Function template signature

Every function template has a signature.

The signature of a template-head is the template parameter list, excluding template parameter names and default arguments, and requires-clause (if any)(since C++20).

The signature of a function template contains the name, parameter-type-list, return type, trailing requires-clause (if any)(since C++20), and signature of the template-head. Except for the following cases, its signature also contains the enclosing namespace.

If the function template is a class member, its signature contains the class of which the function is a member instead of the enclosing namespace. Its signature also contains the trailing requires-clause (if any)(since C++20), ref-qualifier (if any), and(since C++11) **cv**-qualifiers (if any).

|  |  |
| --- | --- |
| If the function template is a friend with constraint involving enclosing template parameters, its signature contains the enclosing class instead of the enclosing namespace. | (since C++20) |

### Function template instantiation

A function template by itself is not a type, or a function. No code is generated from a source file that contains only template definitions. In order for any code to appear, a template must be instantiated: the template arguments must be determined so that the compiler can generate an actual function (or class, from a class template).

#### Explicit instantiation

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `template` return-type name `<` argument-list `>` `(` parameter-list `)` `;` | (1) |  |
|  | | | | | | | | | |
| `template` return-type name `(` parameter-list `)` `;` | (2) |  |
|  | | | | | | | | | |
| `extern` `template` return-type name `<` argument-list `>` `(` parameter-list `)` `;` | (3) | (since C++11) |
|  | | | | | | | | | |
| `extern` `template` return-type name `(` parameter-list `)` `;` | (4) | (since C++11) |
|  | | | | | | | | | |

1) Explicit instantiation definition (without template argument deduction if every non-default template parameter is explicitly specified)2) Explicit instantiation definition with template argument deduction for all parameters3) Explicit instantiation declaration (without template argument deduction if every non-default template parameter is explicitly specified)4) Explicit instantiation declaration with template argument deduction for all parameters

An explicit instantiation definition forces instantiation of the function or member function they refer to. It may appear in the program anywhere after the template definition, and for a given argument-list, is only allowed to appear once in the program, no diagnostic required.

|  |  |
| --- | --- |
| An explicit instantiation declaration (an extern template) prevents implicit instantiations: the code that would otherwise cause an implicit instantiation has to use the explicit instantiation definition provided somewhere else in the program. | (since C++11) |

A trailing template-argument can be left unspecified in an explicit instantiation of a function template specialization or of a member function template specialization if it can be deduced from the function parameter:

```
template<typename T>
void f(T s)
{
    std::cout << s << '\n';
}
 
template void f<double>(double); // instantiates f<double>(double)
template void f<>(char);         // instantiates f<char>(char), template argument deduced
template void f(int);            // instantiates f<int>(int), template argument deduced

```

Explicit instantiation of a function template or of a member function of a class template cannot use `inline` or `constexpr`. If the declaration of the explicit instantiation names an implicitly-declared special member function, the program is ill-formed.

Explicit instantiation of a constructor cannot use a template parameter list (syntax (1)), which is also never necessary because they can be deduced (syntax (2)).

|  |  |
| --- | --- |
| Explicit instantiation of a prospective destructor must name the selected destructor of the class. | (since C++20) |

Explicit instantiation declarations do not suppress the implicit instantiation of inline functions, auto-declarations, references, and class template specializations. (thus, when the inline function that is a subject of explicit instantiation declaration is ODR-used, it is implicitly instantiated for inlining, but its out-of-line copy is not generated in this translation unit)

Explicit instantiation definition of a function template with default arguments is not a use of the arguments, and does not attempt to initialize them:

```
char* p = 0;
 
template<class T>
T g(T x = &p) { return x; }
 
template int g<int>(int); // OK even though &p isn’t an int.

```

#### Implicit instantiation

When code refers to a function in context that requires the function definition to exist, or if the existence of the definition affects the semantics of the program(since C++11), and this particular function has not been explicitly instantiated, implicit instantiation occurs. The list of template arguments does not have to be supplied if it can be deduced from context.

Run this code

```
#include <iostream>
 
template<typename T>
void f(T s)
{
    std::cout << s << '\n';
}
 
int main()
{
    f<double>(1); // instantiates and calls f<double>(double)
    f<>('a');     // instantiates and calls f<char>(char)
    f(7);         // instantiates and calls f<int>(int)
    void (*pf)(std::string) = f; // instantiates f<string>(string)
    pf("∇");                     // calls f<string>(string)
}

```

|  |  |
| --- | --- |
| The existence of a definition of function is considered to affect the semantics of the program if the function is needed for constant evaluation by an expression, even if constant evaluation of the expression is not required or if constant expression evaluation does not use the definition.   ```text template<typename T> constexpr int f() { return T::value; }   template<bool B, typename T> void g(decltype(B ? f<T>() : 0)); template<bool B, typename T> void g(...);   template<bool B, typename T> void h(decltype(int{B ? f<T>() : 0})); template<bool B, typename T> void h(...);   void x() {     g<false, int>(0); // OK: B ? f<T>() : 0 is not potentially constant evaluated     h<false, int>(0); // error: instantiates f<int> even though B evaluates to false                       // and list-initialization of int from int cannot be narrowing } ``` | (since C++11) |

Note: omitting `<>` entirely allows overload resolution to examine both template and non-template overloads.

### Template argument deduction

In order to instantiate a function template, every template argument must be known, but not every template argument has to be specified. When possible, the compiler will deduce the missing template arguments from the function arguments. This occurs when a function call is attempted and when an address of a function template is taken.

```
template<typename To, typename From>
To convert(From f);
 
void g(double d) 
{
    int i = convert<int>(d);    // calls convert<int,double>(double)
    char c = convert<char>(d);  // calls convert<char,double>(double)
    int(*ptr)(float) = convert; // instantiates convert<int, float>(float)
}

```

This mechanism makes it possible to use template operators, since there is no syntax to specify template arguments for an operator other than by re-writing it as a function call expression.

```
#include <iostream>
 
int main() 
{
    std::cout << "Hello, world" << std::endl;
    // operator<< is looked up via ADL as std::operator<<,
    // then deduced to operator<<<char, std::char_traits<char>> both times
    // std::endl is deduced to &std::endl<char, std::char_traits<char>>
}

```

Template argument deduction takes place after the function template name lookup (which may involve argument-dependent lookup) and before overload resolution.

See template argument deduction for details.

### Explicit template arguments

Template arguments of a function template may be obtained from

- template argument deduction
- default template arguments
- specified explicitly, which can be done in the following contexts:

:   - in a function call expression
    - when an address of a function is taken
    - when a reference to function is initialized
    - when a pointer to member function is formed
    - in an explicit specialization
    - in an explicit instantiation
    - in a friend declaration

There is no way to explicitly specify template arguments to overloaded operators, conversion functions, and constructors, because they are called without the use of the function name.

The specified template arguments must match the template parameters in kind (i.e., type for type, non-type for non-type, and template for template). There cannot be more arguments than there are parameters (unless one parameter is a parameter pack, in which case there has to be an argument for each non-pack parameter)(since C++11).

The specified non-type arguments must either match the types of the corresponding non-type template parameters, or be convertible to them.

The function parameters that do not participate in template argument deduction (e.g. if the corresponding template arguments are explicitly specified) are subject to implicit conversions to the type of the corresponding function parameter (as in the usual overload resolution).

|  |  |
| --- | --- |
| A template parameter pack that is explicitly specified may be extended by template argument deduction if there are additional arguments:   ```text template<class... Types> void f(Types... values);   void g() {     f<int*, float*>(0, 0, 0); // Types = {int*, float*, int} } ``` | (since C++11) |

### Template argument substitution

When all template arguments have been specified, deduced or obtained from default template arguments, every use of a template parameter in the function parameter list is replaced with the corresponding template arguments.

Substitution failure (that is, failure to replace template parameters with the deduced or provided template arguments) of a function template removes the function template from the overload set. This allows a number of ways to manipulate overload sets using template metaprogramming: see SFINAE for details.

After substitution, all function parameters of array and function type are adjusted to pointers and all top-level cv-qualifiers are dropped from function parameters (as in a regular function declaration).

The removal of the top-level cv-qualifiers does not affect the type of the parameter as it appears within the function:

```
template<class T>
void f(T t);
 
template<class X>
void g(const X x);
 
template<class Z>
void h(Z z, Z* zp);
 
// two different functions with the same type, but 
// within the function, t has different cv qualifications
f<int>(1);       // function type is void(int), t is int
f<const int>(1); // function type is void(int), t is const int
 
// two different functions with the same type and the same x
// (pointers to these two functions are not equal,
//  and function-local statics would have different addresses)
g<int>(1);       // function type is void(int), x is const int
g<const int>(1); // function type is void(int), x is const int
 
// only top-level cv-qualifiers are dropped:
h<const int>(1, NULL); // function type is void(int, const int*) 
                       // z is const int, zp is const int*

```

### Function template overloading

Function templates and non-template functions may be overloaded.

A non-template function is always distinct from a template specialization with the same type. Specializations of different function templates are always distinct from each other even if they have the same type. Two function templates with the same return type and the same parameter list are distinct and can be distinguished by their explicit template argument list.

When an expression that uses type or non-type template parameters appears in the function parameter list or in the return type, that expression remains a part of the function template signature for the purpose of overloading:

```
template<int I, int J>
A<I+J> f(A<I>, A<J>); // overload #1
 
template<int K, int L>
A<K+L> f(A<K>, A<L>); // same as #1
 
template<int I, int J>
A<I-J> f(A<I>, A<J>); // overload #2

```

Two expressions involving template parameters are called **equivalent** if two function definitions that contain these expressions would be the same under ODR, that is, the two expressions contain the same sequence of tokens whose names are resolved to same entities via name lookup, except template parameters may be differently named. Two lambda expressions are never equivalent.(since C++20)

```
template<int I, int J>
void f(A<I+J>); // template overload #1
 
template<int K, int L>
void f(A<K+L>); // equivalent to #1

```

When determining if two dependent expressions are equivalent, only the dependent names involved are considered, not the results of name lookup. If multiple declarations of the same template differ in the result of name lookup, the first such declaration is used:

```
template<class T>
decltype(g(T())) h(); // decltype(g(T())) is a dependent type
 
int g(int);
 
template<class T>
decltype(g(T())) h()
{                  // redeclaration of h() uses earlier lookup
    return g(T()); // although the lookup here does find g(int)
}
 
int i = h<int>(); // template argument substitution fails; g(int)
                  // was not in scope at the first declaration of h()

```

Two function templates are considered **equivalent** if

- they are declared in the same scope
- they have the same name
- they have **equivalent** template parameter lists, meaning the lists are of the same length, and for each corresponding parameter pair, all of the following is true:

:   - the two parameters are of the same kind (both types, both non-types, or both templates)

|  |  |
| --- | --- |
| - they are either both parameter packs or neither | (since C++11) |

:   - if non-type, their types are equivalent,
    - if template, their template parameters are equivalent,

|  |  |
| --- | --- |
| - if one is declared with concept-name, they both are, and the concept-names are equivalent. | (since C++20) |

- the expressions involving template parameters in their return types and parameter lists are **equivalent**

|  |  |
| --- | --- |
| - the expressions in their requires-clauses that follow the template parameter lists, if present, are equivalent - the expressions in their requires-clauses that follow the function declarators, if present, are equivalent | (since C++20) |

Two potentially-evaluated(since C++20) expressions involving template parameters are called **functionally equivalent** if they are not **equivalent**, but for any given set of template arguments, the evaluation of the two expressions results in the same value.

Two function templates are considered **functionally equivalent** if they are **equivalent**, except that one or more expressions that involve template parameters in their return types and parameter lists are **functionally equivalent**.

|  |  |
| --- | --- |
| In addition, two function templates are **functionally equivalent** but not **equivalent** if their constraints are specified differently, but they accept and are satisfied by the same set of template argument lists. | (since C++20) |

If a program contains declarations of function templates that are **functionally equivalent** but not **equivalent**, the program is ill-formed; no diagnostic is required.

```
// equivalent
template<int I>
void f(A<I>, A<I+10>); // overload #1
template<int I>
void f(A<I>, A<I+10>); // redeclaration of overload #1
 
// not equivalent
template<int I>
void f(A<I>, A<I+10>); // overload #1
template<int I>
void f(A<I>, A<I+11>); // overload #2
 
// functionally-equivalent but not equivalent
// This program is ill-formed, no diagnostic required
template<int I>
void f(A<I>, A<I+10>);      // overload #1
template<int I>
void f(A<I>, A<I+1+2+3+4>); // functionally equivalent

```

When the same function template specialization matches more than one overloaded function template (this often results from template argument deduction), **partial ordering of overloaded function templates** is performed to select the best match.

Specifically, partial ordering takes place in the following situations:

1) overload resolution for a call to a function template specialization:

```
template<class X>
void f(X a);
template<class X>
void f(X* a);
 
int* p;
f(p);

```

2) when the address of a function template specialization is taken:

```
template<class X>
void f(X a);
template<class X>
void f(X* a);
 
void (*p)(int*) = &f;

```

3) when a placement operator delete that is a function template specialization is selected to match a placement operator new:

|  |  |
| --- | --- |
|  | This section is incomplete Reason: mini-example |

4) when a friend function declaration, an explicit instantiation, or an explicit specialization refers to a function template specialization:

```
template<class X>
void f(X a);  // first template f
template<class X>
void f(X* a); // second template f
template<>
void f<>(int *a) {} // explicit specialization
 
// template argument deduction comes up with two candidates:
// f<int*>(int*) and f<int>(int*)
// partial ordering selects f<int>(int*) as more specialized

```

Informally "A is more specialized than B" means "A accepts fewer types than B".

Formally, to determine which of any two function templates is more specialized, the partial ordering process first transforms one of the two templates as follows:

- For each type, non-type, and template parameter, including parameter packs,(since C++11) a unique fictitious type, value, or template is generated and substituted into function type of the template
- If only one of the two function templates being compared is a member function, and that function template is a non-static member of some class `A`, a new first parameter is inserted into its parameter list. Given **cv** as the cv-qualifiers of the function template and **ref** as the ref-qualifier of the function template(since C++11), the new parameter type is **cv** `A&` unless **ref** is `&&`, or **ref** is not present and the first parameter of the other template has rvalue reference type, in this case the type is **cv** `A&&`(since C++11). This helps the ordering of operators, which are looked up both as member and as non-member functions:

```
struct A {};
 
template<class T>
struct B
{
    template<class R>
    int operator*(R&); // #1
};
 
template<class T, class R>
int operator*(T&, R&); // #2
 
int main()
{
    A a;
    B<A> b;
    b * a; // template argument deduction for int B<A>::operator*(R&) gives R=A 
           //                             for int operator*(T&, R&), T=B<A>, R=A
 
    // For the purpose of partial ordering, the member template B<A>::operator*
    // is transformed into template<class R> int operator*(B<A>&, R&);
 
    // partial ordering between 
    //     int operator*(   T&, R&)  T=B<A>, R=A
    // and int operator*(B<A>&, R&)  R=A 
    // selects int operator*(B<A>&, A&) as more specialized
}

```

After one of the two templates was transformed as described above, template argument deduction is executed using the transformed template as the argument template and the original template type of the other template as the parameter template. The process is then repeated using the second template (after transformations) as the argument and the first template in its original form as the parameter.

The types used to determine the order depend on the context:

- in the context of a function call, the types are those function parameter types for which the function call has arguments (default function arguments, parameter packs,(since C++11) and ellipsis parameters are not considered -- see examples below)
- in the context of a call to a user-defined conversion function, the return types of the conversion function templates are used
- in other contexts, the function template type is used

Each type from the list above from the parameter template is deduced. Before deduction begins, each parameter `P` of the parameter template and the corresponding argument `A` of the argument template is adjusted as follows:

- If both `P` and `A` are reference types before, determine which is more cv-qualified (in all other cases, cv-qualifications are ignored for partial ordering purposes)
- If `P` is a reference type, it is replaced by the type referred to
- If `A` is a reference type, it is replaced by the type referred to
- If `P` is cv-qualified, `P` is replaced with cv-unqualified version of itself
- If `A` is cv-qualified, `A` is replaced with cv-unqualified version of itself

After these adjustments, deduction of `P` from `A` is done following template argument deduction from a type.

|  |  |
| --- | --- |
| If `P` is a function parameter pack, the type `A` of each remaining parameter type of the argument template is compared with the type `P` of the declarator-id of the function parameter pack. Each comparison deduces template arguments for subsequent positions in the template parameter packs expanded by the function parameter pack.  If `A` was transformed from a function parameter pack, it is compared with each remaining parameter type of the parameter template. | (since C++11) |

If the argument `A` of the transformed template-1 can be used to deduce the corresponding parameter `P` of template-2, but not vice versa, then this `A` is more specialized than `P` with regards to the type(s) that are deduced by this `P/A` pair.

If deduction succeeds in both directions, and the original `P` and `A` were reference types, then additional tests are made:

- If `A` was lvalue reference and `P` was rvalue reference, `A` is considered to be more specialized than `P`
- If `A` was more cv-qualified than `P`, `A` is considered to be more specialized than `P`

In all other cases, neither template is more specialized than the other with regards to the type(s) deduced by this `P/A` pair.

After considering every `P` and `A` in both directions, if, for each type that was considered,

- template-1 is at least as specialized as template-2 for all types
- template-1 is more specialized than template-2 for some types
- template-2 is not more specialized than template-1 for any types OR is not at least as specialized for any types

Then template-1 is more specialized than template-2. If the conditions above are true after switching template order, then template-2 is more specialized than template-1. Otherwise, neither template is more specialized than the other.

|  |  |
| --- | --- |
| In case of a tie, if one function template has a trailing parameter pack and the other does not, the one with the omitted parameter is considered to be more specialized than the one with the empty parameter pack. | (since C++11) |

If, after considering all pairs of overloaded templates, there is one that is unambiguously more specialized than all others, that template's specialization is selected, otherwise compilation fails.

In the following examples, the fictitious arguments will be called U1, U2:

```
template<class T>
void f(T);        // template #1
template<class T>
void f(T*);       // template #2
template<class T>
void f(const T*); // template #3
 
void m()
{
    const int* p;
    f(p); // overload resolution picks: #1: void f(T ) [T = const int *]
          //                            #2: void f(T*) [T = const int]
          //                            #3: void f(const T *) [T = int]
 
    // partial ordering:
 
    // #1 from transformed #2: void(T) from void(U1*): P=T A=U1*: deduction ok: T=U1*
    // #2 from transformed #1: void(T*) from void(U1): P=T* A=U1: deduction fails
    // #2 is more specialized than #1 with regards to T
 
    // #1 from transformed #3: void(T) from void(const U1*): P=T, A=const U1*: ok
    // #3 from transformed #1: void(const T*) from void(U1): P=const T*, A=U1: fails
    // #3 is more specialized than #1 with regards to T
 
    // #2 from transformed #3: void(T*) from void(const U1*): P=T* A=const U1*: ok
    // #3 from transformed #2: void(const T*) from void(U1*): P=const T* A=U1*: fails
    // #3 is more specialized than #2 with regards to T
 
    // result: #3 is selected
    // in other words, f(const T*) is more specialized than f(T) or f(T*)
}

```

```
template<class T>
void f(T, T*);   // #1
template<class T>
void f(T, int*); // #2
 
void m(int* p)
{
    f(0, p); // deduction for #1: void f(T, T*) [T = int]
             // deduction for #2: void f(T, int*) [T = int]
 
    // partial ordering:
 
    // #1 from #2: void(T,T*) from void(U1,int*): P1=T, A1=U1: T=U1
    //                                            P2=T*, A2=int*: T=int: fails
 
    // #2 from #1: void(T,int*) from void(U1,U2*): P1=T A1=U1: T=U1
    //                                             P2=int* A2=U2*: fails
 
    // neither is more specialized w.r.t T, the call is ambiguous
}

```

```
template<class T>
void g(T);  // template #1
template<class T>
void g(T&); // template #2
 
void m()
{
    float x;
    g(x); // deduction from #1: void g(T ) [T = float]
          // deduction from #2: void g(T&) [T = float]
 
    // partial ordering:
 
    // #1 from #2: void(T) from void(U1&): P=T, A=U1 (after adjustment), ok
 
    // #2 from #1: void(T&) from void(U1): P=T (after adjustment), A=U1: ok
 
    // neither is more specialized w.r.t T, the call is ambiguous
}

```

```
template<class T>
struct A { A(); };
 
template<class T>
void h(const T&); // #1
template<class T>
void h(A<T>&);    // #2
 
void m()
{
    A<int> z;
    h(z); // deduction from #1: void h(const T &) [T = A<int>]
          // deduction from #2: void h(A<T> &) [T = int]
 
    // partial ordering:
 
    // #1 from #2: void(const T&) from void(A<U1>&): P=T A=A<U1>: ok T=A<U1>
 
    // #2 from #1: void(A<T>&) from void(const U1&): P=A<T> A=const U1: fails
 
    // #2 is more specialized than #1 w.r.t T
 
    const A<int> z2;
    h(z2); // deduction from #1: void h(const T&) [T = A<int>]
           // deduction from #2: void h(A<T>&) [T = int], but substitution fails
 
    // only one overload to choose from, partial ordering not tried, #1 is called
}

```

Since a call context considers only parameters for which there are explicit call arguments, those function parameter packs,(since C++11) ellipsis parameters, and parameters with default arguments, for which there is no explicit call argument, are ignored:

```
template<class T>
void f(T);         // #1
template<class T>
void f(T*, int = 1); // #2
 
void m(int* ip)
{
    int* ip;
    f(ip); // calls #2 (T* is more specialized than T)
}

```

```
template<class T>
void g(T);       // #1
template<class T>
void g(T*, ...); // #2
 
void m(int* ip)
{
    g(ip); // calls #2 (T* is more specialized than T)
}

```

```
template<class T, class U>
struct A {};
 
template<class T, class U>
void f(U, A<U, T>* p = 0); // #1
template<class U>
void f(U, A<U, U>* p = 0); // #2
 
void h()
{
    f<int>(42, (A<int, int>*)0); // calls #2
    f<int>(42);                  // error: ambiguous
}

```

```
template<class T>
void g(T, T = T()); // #1
template<class T, class... U>
void g(T, U...);    // #2
 
void h()
{
    g(42); // error: ambiguous
}

```

```
template<class T, class... U>
void f(T, U...); // #1
template<class T>
void f(T);       // #2
 
void h(int i)
{
    f(&i); // calls #2 due to the tie-breaker between parameter pack and no parameter
           // (note: was ambiguous between DR692 and DR1395)
}

```

```
template<class T, class... U>
void g(T*, U...); // #1
template<class T>
void g(T);        // #2
 
void h(int i)
{
    g(&i); // OK: calls #1 (T* is more specialized than T)
}

```

```
template<class... T>
int f(T*...);    // #1
template<class T>
int f(const T&); // #2
 
f((int*)0); // OK: selects #2; non-variadic template is more specialized than
            // variadic template (was ambiguous before DR1395 because deduction
            // failed in both directions)

```

```
template<class... Args>
void f(Args... args);        // #1
template<class T1, class... Args>
void f(T1 a1, Args... args); // #2
template<class T1, class T2>
void f(T1 a1, T2 a2);        // #3
 
f();        // calls #1
f(1, 2, 3); // calls #2
f(1, 2);    // calls #3; non-variadic template #3 is more
            // specialized than the variadic templates #1 and #2

```

During template argument deduction within the partial ordering process, template parameters don't require to be matched with arguments, if the argument is not used in any of the types considered for partial ordering

```
template<class T>
T f(int); // #1
template<class T, class U>
T f(U);   // #2
 
void g()
{
    f<int>(1); // specialization of #1 is explicit: T f(int) [T = int]
               // specialization of #2 is deduced:  T f(U) [T = int, U = int]
 
    // partial ordering (only considering the argument type):
 
    // #1 from #2: T(int) from U1(U2): fails
    // #2 from #1: T(U) from U1(int): ok: U=int, T unused
 
    // calls #1
}

```

|  |  |
| --- | --- |
| Partial ordering of function templates containing template parameter packs is independent of the number of deduced arguments for those template parameter packs.   ```text template<class...> struct Tuple {};   template<class... Types> void g(Tuple<Types...>);      // #1 template<class T1, class... Types> void g(Tuple<T1, Types...>);  // #2 template<class T1, class... Types> void g(Tuple<T1, Types&...>); // #3   g(Tuple<>());            // calls #1 g(Tuple<int, float>());  // calls #2 g(Tuple<int, float&>()); // calls #3 g(Tuple<int>());         // calls #3 ``` | (since C++11) |

|  |  |
| --- | --- |
|  | This section is incomplete Reason: 14.8.3[temp.over] |

To compile a call to a function template, the compiler has to decide between non-template overloads, template overloads, and the specializations of the template overloads.

```
template<class T>
void f(T);      // #1: template overload
template<class T>
void f(T*);     // #2: template overload
 
void f(double); // #3: non-template overload
template<>
void f(int);    // #4: specialization of #1
 
f('a');        // calls #1
f(new int(1)); // calls #2
f(1.0);        // calls #3
f(1);          // calls #4

```

### Function overloads vs function specializations

Note that only non-template and primary template overloads participate in overload resolution. The specializations are not overloads and are not considered. Only after the overload resolution selects the best-matching primary function template, its specializations are examined to see if one is a better match.

```
template<class T>
void f(T);    // #1: overload for all types
template<>
void f(int*); // #2: specialization of #1 for pointers to int
template<class T>
void f(T*);   // #3: overload for all pointer types
 
f(new int(1)); // calls #3, even though specialization of #1 would be a perfect match

```

It is important to remember this rule while ordering the header files of a translation unit. For more examples of the interplay between function overloads and function specializations, expand below:

| Examples |
| --- |
| Consider first some scenarios where the argument-dependent lookup is not employed. For that, we use the call (f)(t). As described in ADL, wrapping the function name in parentheses is suppressing the argument-dependent lookup.   - Multiple overloads of f() declared before the **point-of-reference** (POR) in g().  Run this code  ```text #include <iostream>   struct A {};   template<class T> void f(T)  { std::cout << "#1\n"; } // overload #1 before f() POR template<class T> void f(T*) { std::cout << "#2\n"; } // overload #2 before f() POR   template<class T> void g(T* t)  {     (f)(t); // f() POR }   int main() {     A* p = nullptr;     g(p); // POR of g() and f() }   // Both #1 and #2 are added to the candidate list; // #2 is selected because it is a better match. ```   Output:   ```text #2 ```      - A better matching template overload is declared after POR.  Run this code  ```text #include <iostream>   struct A {};   template<class T> void f(T)  { std::cout << "#1\n"; } // #1   template<class T> void g(T* t)  {     (f)(t); // f() POR }   template<class T> void f(T*) { std::cout << "#2\n"; } // #2   int main() {     A* p = nullptr;     g(p); // POR of g() and f() }   // Only #1 is added to the candidate list; #2 is defined after POR; // therefore, it is not considered for overloading even if it is a better match. ```   Output:   ```text #1 ```      - A better matching explicit template specialization is declared after POR.  Run this code  ```text #include <iostream>   struct A {};   template<class T> void f(T)    { std::cout << "#1\n"; } // #1   template<class T> void g(T* t)  {     (f)(t); // f() POR } template<> void f<>(A*) { std::cout << "#3\n"; } // #3   int main() {     A* p = nullptr;     g(p); // POR of g() and f() }   // #1 is added to the candidate list; #3 is a better match defined after POR. The // candidate list consists of #1 which is eventually selected. After that, the explicit  // specialization #3 of #1 declared after POI is selected because it is a better match.  // This behavior is governed by 14.7.3/6 [temp.expl.spec] and has nothing to do with ADL. ```   Output:   ```text #3 ```      - A better matching template overload is declared after POR. The best matching explicit template specialization is declared after the better matching overload.  Run this code  ```text #include <iostream>   struct A {};   template<class T> void f(T)    { std::cout << "#1\n"; } // #1   template<class T> void g(T* t)  {     (f)(t); // f() POR }   template<class T> void f(T*)   { std::cout << "#2\n"; } // #2 template<> void f<>(A*) { std::cout << "#3\n"; } // #3   int main() {     A* p = nullptr;     g(p); // POR of g() and f() }   // #1 is the only member of the candidate list and it is eventually selected.  // After that, the explicit specialization #3 is skipped because it actually  // specializes #2 declared after POR. ```   Output:   ```text #1 ```   Let's consider now those cases employing argument-dependent lookup (i.e., we use the more common call format f(t)).   - A better matching template overload is declared after POR.  Run this code  ```text #include <iostream>   struct A {};   template<class T> void f(T)  { std::cout << "#1\n"; } // #1   template<class T> void g(T* t)  {     f(t); // f() POR }   template<class T> void f(T*) { std::cout << "#2\n"; } // #2   int main() {     A* p = nullptr;     g(p); // POR of g() and f() }   // #1 is added to the candidate list as a result of the ordinary lookup; // #2 is defined after POR but it is added to the candidate list via ADL lookup. // #2 is selected being the better match. ```   Output:   ```text #2 ```      - A better matching template overload is declared after POR. The best matching explicit template specialization is declared before the better matching overload.  Run this code  ```text #include <iostream>   struct A {};   template<class T> void f(T)    { std::cout << "#1\n"; } // #1   template<class T> void g(T* t)  {     f(t); // f() POR }   template<> void f<>(A*) { std::cout << "#3\n"; } // #3 template<class T> void f(T*)   { std::cout << "#2\n"; } // #2   int main() {     A* p = nullptr;     g(p); // POR of g() and f() }   // #1 is added to the candidate list as a result of the ordinary lookup; // #2 is defined after POR but it is added to the candidate list via ADL lookup. // #2 is selected among the primary templates, being the better match. // Since #3 is declared before #2, it is an explicit specialization of #1. // Hence the final selection is #2. ```   Output:   ```text #2 ```      - A better matching template overload is declared after POR. The best matching explicit template specialization is declared last.  Run this code  ```text #include <iostream>   struct A {};   template<class T> void f(T)    { std::cout << "#1\n"; } // #1   template<class T> void g(T* t)  {     f(t); // f() POR }   template<class T> void f(T*)   { std::cout << "#2\n"; } // #2 template<> void f<>(A*) { std::cout << "#3\n"; } // #3   int main() {     A* p = nullptr;     g(p); // POR of g() and f() }   // #1 is added to the candidate list as a result of the ordinary lookup; // #2 is defined after POR but it is added to the candidate list via ADL lookup. // #2 is selected among the primary templates, being the better match. // Since #3 is declared after #2, it is an explicit specialization of #2; // therefore, selected as the function to call. ```   Output:   ```text #3 ```   Whenever the arguments are some C++ basic types, there are no ADL-associated namespaces. Hence, those scenarios are identical with the non-ADL examples above. |

For detailed rules on overload resolution, see overload resolution.

### Function template specialization

|  |  |
| --- | --- |
|  | This section is incomplete Reason: 14.8[temp.fct.spec] (note that 14.8.1[temp.arg.explicit] is already in full specialization article: either function specifics go here: lack of partials, interaction with function overloads, or just refer to that |

### Keywords

template,
extern
(since C++11)

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 214 | C++98 | the exact procedure of partial ordering was not specified | specification added |
| CWG 532 | C++98 | the order between a non-static member function template and a non-member function template was not specified | specification added |
| CWG 581 | C++98 | template argument list in an explicit specialization or instantiation of a constructor template was allowed | forbidden |
| CWG 1321 | C++98 | it was unclear whether same dependent names in the first declaration and a redeclaration are equivalent | they are equivalent and the meaning is same as in the first declaration |
| CWG 1395 | C++11 | deduction failed when A was from a pack, and there was no empty pack tie-breaker | deduction allowed, tie-breaker added |
| CWG 1406 | C++11 | the type of the new first parameter added for a non-static member function template was not relevant to the ref-qualifier of that template | the type is an rvalue reference type if the ref-qualifier is `&&` |
| CWG 1446 | C++11 | the type of the new first parameter added for a non-static member function template without ref-qualifier was an lvalue reference type, even if that member function template is compared with a function template whose first parameter has rvalue reference type | the type is an rvalue reference type in this case |
| CWG 2373 | C++98 | new first parameters were added to the parameter lists of static member function templates in partial ordering | not added |

### See also

- class template
- function declaration
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/function_template&oldid=178103>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 December 2024, at 04:30.