# Partial template specialization

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
| Class template argument deduction (C++17) | | | | |
| Explicit (full) specialization | | | | |
| ****Partial specialization**** | | | | |
| Dependent names | | | | |
| Packs (C++11) | | | | |
| `sizeof...` (C++11) | | | | |
| Fold expressions (C++17) | | | | |
| Pack indexing (C++26) | | | | |
| SFINAE | | | | |
| Constraints and concepts (C++20) | | | | |
| Requires expression (C++20) | | | | |

Allows customizing class and variable(since C++14) templates for a given category of template arguments.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `template` `<` parameter-list `>` class-key class-head-name `<` argument-list `>` declaration | (1) |  |
|  | | | | | | | | | |
| `template` `<` parameter-list `>` decl-specifier-seq declarator `<` argument-list `>` initializer ﻿(optional) | (2) | (since C++14) |
|  | | | | | | | | | |

where class-head-name identifies the name of a previously declared class template and declarator identifies the name of a previously declared variable template(since C++14).

Partial specialization may be declared in any scope where its primary template may be defined (which may be different from the scope where the primary template is defined; such as with out-of-class specialization of a member template). Partial specialization has to appear after the non-specialized template declaration.

For example,

```
template<class T1, class T2, int I>
class A {};             // primary template
 
template<class T, int I>
class A<T, T*, I> {};   // #1: partial specialization where T2 is a pointer to T1
 
template<class T, class T2, int I>
class A<T*, T2, I> {};  // #2: partial specialization where T1 is a pointer
 
template<class T>
class A<int, T*, 5> {}; // #3: partial specialization where
                        //     T1 is int, I is 5, and T2 is a pointer
 
template<class X, class T, int I>
class A<X, T*, I> {};   // #4: partial specialization where T2 is a pointer

```

Examples of partial specializations in the standard library include std::unique_ptr, which has a partial specialization for array types.

### The argument list

The following restrictions apply to the argument-list of a partial template specialization:

1) The argument list cannot be identical to the non-specialized argument list (it must specialize something):

```
template<class T1, class T2, int I> class B {};        // primary template
template<class X, class Y, int N> class B<X, Y, N> {}; // error

```

|  |  |
| --- | --- |
| Moreover, the specialization has to be more specialized than the primary template   ```text template<int N, typename T1, typename... Ts> struct B; template<typename... Ts> struct B<0, Ts...> {}; // Error: not more specialized ``` | (since C++11) |

2) Default arguments cannot appear in the argument list3) If any argument is a pack expansion, it must be the last argument in the list4)Non-type argument expressions can use template parameters as long as the parameter appears at least once outside a non-deduced context (note that only clang and gcc 12 support this feature currently):

```
template<int I, int J> struct A {};
template<int I> struct A<I + 5, I * 2> {}; // error, I is not deducible
 
template<int I, int J, int K> struct B {};
template<int I> struct B<I, I * 2, 2> {};  // OK: first parameter is deducible

```

5) Non-type template argument cannot specialize a template parameter whose type depends on a parameter of the specialization:

```
template<class T, T t> struct C {}; // primary template
template<class T> struct C<T, 1>;   // error: type of the argument 1 is T,
                                    // which depends on the parameter T
 
template<int X, int (*array_ptr)[X]> class B {}; // primary template
int array[5];
template<int X> class B<X, &array> {}; // error: type of the argument &array is
                                       // int(*)[X], which depends on the parameter X

```

### Name lookup

Partial template specializations are not found by name lookup. Only if the primary template is found by name lookup, its partial specializations are considered. In particular, a using declaration that makes a primary template visible, makes partial specializations visible as well:

```
namespace N
{
    template<class T1, class T2> class Z {}; // primary template
}
using N::Z; // refers to the primary template
 
namespace N
{
    template<class T> class Z<T, T*> {};     // partial specialization
}
Z<int, int*> z; // name lookup finds N::Z (the primary template), the
                // partial specialization with T = int is then used

```

### Partial ordering

When a class or variable(since C++14) template is instantiated, and there are partial specializations available, the compiler has to decide if the primary template is going to be used or one of its partial specializations.

1) If only one specialization matches the template arguments, that specialization is used2) If more than one specialization matches, partial order rules are used to determine which specialization is more specialized. The most specialized specialization is used, if it is unique (if it is not unique, the program cannot be compiled)3) If no specializations match, the primary template is used

```
// given the template A as defined above
A<int, int, 1> a1;   // no specializations match, uses primary template
A<int, int*, 1> a2;  // uses partial specialization #1 (T = int, I = 1)
A<int, char*, 5> a3; // uses partial specialization #3, (T = char)
A<int, char*, 1> a4; // uses partial specialization #4, (X = int, T = char, I = 1)
A<int*, int*, 2> a5; // error: matches #2 (T = int, T2 = int*, I= 2)
                     //        matches #4 (X = int*, T = int, I = 2)
                     // neither one is more specialized than the other

```

Informally "A is more specialized than B" means "A accepts a subset of the types that B accepts".

Formally, to establish more-specialized-than relationship between partial specializations, each is first converted to a fictitious function template as follows:

- the first function template has the same template parameters as the first partial specialization and has just one function parameter, whose type is a class template specialization with all the template arguments from the first partial specialization
- the second function template has the same template parameters as the second partial specialization and has just one function parameter whose type is a class template specialization with all the template arguments from the second partial specialization.

The function templates are then ranked as if for function template overloading.

```
template<int I, int J, class T> struct X {}; // primary template
template<int I, int J>          struct X<I, J, int>
{
    static const int s = 1;
}; // partial specialization #1
// fictitious function template for #1 is
// template<int I, int J> void f(X<I, J, int>); #A
 
template<int I>                 struct X<I, I, int>
{
    static const int s = 2;
}; // partial specialization #2
// fictitious function template for #2 is 
// template<int I>        void f(X<I, I, int>); #B
 
int main()
{
    X<2, 2, int> x; // both #1 and #2 match
// partial ordering for function templates:
// #A from #B: void(X<I, J, int>) from void(X<U1, U1, int>): deduction OK
// #B from #A: void(X<I, I, int>) from void(X<U1, U2, int>): deduction fails
// #B is more specialized
// #2 is the specialization that is instantiated
    std::cout << x.s << '\n'; // prints 2
}

```

### Members of partial specializations

The template parameter list and the template argument list of a member of a partial specialization must match the parameter list and the argument list of the partial specialization.

Just like with members of primary templates, they only need to be defined if used in the program.

Members of partial specializations are not related to the members of the primary template.

Explicit (full) specialization of a member of a partial specialization is declared the same way as an explicit specialization of the primary template.

```
template<class T, int I> // primary template
struct A
{
    void f(); // member declaration
};
 
template<class T, int I>
void A<T, I>::f() {}     // primary template member definition
 
// partial specialization
template<class T>
struct A<T, 2>
{
    void f();
    void g();
    void h();
};
 
// member of partial specialization
template<class T>
void A<T, 2>::g() {}
 
// explicit (full) specialization
// of a member of partial specialization
template<>
void A<char, 2>::h() {}
 
int main()
{
    A<char, 0> a0;
    A<char, 2> a2;
    a0.f(); // OK, uses primary template’s member definition
    a2.g(); // OK, uses partial specialization's member definition
    a2.h(); // OK, uses fully-specialized definition of
            // the member of a partial specialization
    a2.f(); // error: no definition of f() in the partial
            // specialization A<T,2> (the primary template is not used)
}

```

If a primary template is a member of another class template, its partial specializations are members of the enclosing class template. If the enclosing template is instantiated, the declaration of each member partial specialization is instantiated as well (the same way declarations, but not definitions, of all other members of a template are instantiated).

If the primary member template is explicitly (fully) specialized for a given (implicit) specialization of the enclosing class template, the partial specializations of the member
template are ignored for this specialization of the enclosing class template.

If a partial specialization of the member template is explicitly specialized for a given (implicit) specialization of the enclosing class template, the primary member template and its other partial specializations are still considered for this specialization
of the enclosing class template.

```
template<class T> struct A // enclosing class template
{
    template<class T2>
    struct B {};      // primary member template
    template<class T2>
    struct B<T2*> {}; // partial specialization of member template
};
 
template<>
template<class T2>
struct A<short>::B {}; // full specialization of primary member template
                       // (will ignore the partial)
 
A<char>::B<int*> abcip;  // uses partial specialization T2=int
A<short>::B<int*> absip; // uses full specialization of the primary (ignores partial)
A<char>::B<int> abci;    // uses primary

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 727 | C++98 | partial and full specializations not allowed in class scope | allowed in any scope |
| CWG 1315 | C++98 | template parameter could not be used in non-type template arguments other than id-expressions | expressions ok as long as deducible |
| CWG 1495 | C++11 | the specification was unclear when involving parameter pack | the specialization shall be more specialized |
| CWG 1711 | C++14 | missing specification of variable template partial specializations | add support for variable templates |
| CWG 1819 | C++98 | acceptable scopes for definition of partial specialization | make partial specialization can be declared in the same scope with primary templates |
| CWG 2330 | C++14 | missing references to variable templates | add support for variable templates |

### See also

- templates
- class template
- function template
- full template specialization
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/partial_specialization&oldid=170164>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 March 2024, at 19:33.