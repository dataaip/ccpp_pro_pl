# Constraints and concepts (since C++20)

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
| Partial specialization | | | | |
| Dependent names | | | | |
| Packs (C++11) | | | | |
| `sizeof...` (C++11) | | | | |
| Fold expressions (C++17) | | | | |
| Pack indexing (C++26) | | | | |
| SFINAE | | | | |
| ****Constraints and concepts**** (C++20) | | | | |
| Requires expression (C++20) | | | | |

Class templates, function templates (include generic lambdas), and other templated functions (typically members of class templates) might be associated with a **constraint**, which specifies the requirements on template arguments, which can be used to select the most appropriate function overloads and template specializations.

Named sets of such requirements are called **concepts**. Each concept is a predicate, evaluated at compile time, and becomes a part of the interface of a template where it is used as a constraint:

Run this code

```
#include <cstddef>
#include <concepts>
#include <functional>
#include <string>
 
// Declaration of the concept “Hashable”, which is satisfied by any type “T”
// such that for values “a” of type “T”, the expression std::hash<T>{}(a)
// compiles and its result is convertible to std::size_t
template<typename T>
concept Hashable = requires(T a)
{
    { std::hash<T>{}(a) } -> std::convertible_to<std::size_t>;
};
 
struct meow {};
 
// Constrained C++20 function template:
template<Hashable T>
void f(T) {}
//
// Alternative ways to apply the same constraint:
// template<typename T>
//     requires Hashable<T>
// void f(T) {}
//
// template<typename T>
// void f(T) requires Hashable<T> {}
//
// void f(Hashable auto /* parameter-name */) {}
 
int main()
{
    using std::operator""s;
 
    f("abc"s);    // OK, std::string satisfies Hashable
    // f(meow{}); // Error: meow does not satisfy Hashable
}

```

Violations of constraints are detected at compile time, early in the template instantiation process, which leads to easy to follow error messages:

```
std::list<int> l = {3, -1, 10};
std::sort(l.begin(), l.end()); 
// Typical compiler diagnostic without concepts:
// invalid operands to binary expression ('std::_List_iterator<int>' and
// 'std::_List_iterator<int>')
//                           std::__lg(__last - __first) * 2);
//                                     ~~~~~~ ^ ~~~~~~~
// ... 50 lines of output ...
//
// Typical compiler diagnostic with concepts:
// error: cannot call std::sort with std::_List_iterator<int>
// note:  concept RandomAccessIterator<std::_List_iterator<int>> was not satisfied

```

The intent of concepts is to model semantic categories (Number, Range, RegularFunction) rather than syntactic restrictions (HasPlus, Array). According to ISO C++ core guideline T.20, "The ability to specify meaningful semantics is a defining characteristic of a true concept, as opposed to a syntactic constraint."

### Concepts

A concept is a named set of requirements. The definition of a concept must appear at namespace scope.

The definition of a concept has the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `template <` template-parameter-list `>` `concept` concept-name attr ﻿(optional) `=` constraint-expression`;` |  |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| attr | - | sequence of any number of attributes |

```
// concept
template<class T, class U>
concept Derived = std::is_base_of<U, T>::value;

```

Concepts cannot recursively refer to themselves and cannot be constrained:

```
template<typename T>
concept V = V<T*>; // error: recursive concept
 
template<class T>
concept C1 = true;
template<C1 T>
concept Error1 = true; // Error: C1 T attempts to constrain a concept definition
template<class T> requires C1<T>
concept Error2 = true; // Error: the requires clause attempts to constrain a concept

```

Explicit instantiations, explicit specializations, or partial specializations of concepts are not allowed (the meaning of the original definition of a constraint cannot be changed).

Concepts can be named in an id-expression. The value of the id-expression is true if the constraint expression is satisfied, and false otherwise.

Concepts can also be named in a type-constraint, as part of

- type template parameter declaration,
- placeholder type specifier,
- compound requirement.

In a type-constraint, a concept takes one less template argument than its parameter list demands, because the contextually deduced type is implicitly used as the first argument of the concept.

```
template<class T, class U>
concept Derived = std::is_base_of<U, T>::value;
 
template<Derived<Base> T>
void f(T); // T is constrained by Derived<T, Base>

```

### Constraints

A constraint is a sequence of logical operations and operands that specifies requirements on template arguments. They can appear within requires expressions or directly as bodies of concepts.

There are three(until C++26)four(since C++26) types of constraints:

1) conjunctions2) disjunctions3) atomic constraints

|  |  |
| --- | --- |
| 4) fold expanded constraints | (since C++26) |

The constraint associated with a declaration is determined by normalizing a logical AND expression whose operands are in the following order:

1. the constraint expression introduced for each constrained type template parameter or non-type template parameter declared with a constrained placeholder type, in order of appearance;
2. the constraint expression in the requires clause after the template parameter list;
3. the constraint expression introduced for each parameter with constrained placeholder type in an abbreviated function template declaration;
4. the constraint expression in the trailing requires clause.

This order determines the order in which constraints are instantiated when checking for satisfaction.

#### Redeclarations

A constrained declaration may only be redeclared using the same syntactic form. No diagnostic is required:

```
// These first two declarations of f are fine
template<Incrementable T>
void f(T) requires Decrementable<T>;
 
template<Incrementable T>
void f(T) requires Decrementable<T>; // OK, redeclaration
 
// Inclusion of this third, logically-equivalent-but-syntactically-different
// declaration of f is ill-formed, no diagnostic required
template<typename T>
    requires Incrementable<T> && Decrementable<T>
void f(T);
 
// The following two declarations have different constraints:
// the first declaration has Incrementable<T> && Decrementable<T>
// the second declaration has Decrementable<T> && Incrementable<T>
// Even though they are logically equivalent.
 
template<Incrementable T> 
void g(T) requires Decrementable<T>;
 
template<Decrementable T> 
void g(T) requires Incrementable<T>; // ill-formed, no diagnostic required

```

#### Conjunctions

The conjunction of two constraints is formed by using the `&&` operator in the constraint expression:

```
template<class T>
concept Integral = std::is_integral<T>::value;
template<class T>
concept SignedIntegral = Integral<T> && std::is_signed<T>::value;
template<class T>
concept UnsignedIntegral = Integral<T> && !SignedIntegral<T>;

```

A conjunction of two constraints is satisfied only if both constraints are satisfied. Conjunctions are evaluated left to right and short-circuited (if the left constraint is not satisfied, template argument substitution into the right constraint is not attempted: this prevents failures due to substitution outside of immediate context).

```
template<typename T>
constexpr bool get_value() { return T::value; }
 
template<typename T>
    requires (sizeof(T) > 1 && get_value<T>())
void f(T);   // #1
 
void f(int); // #2
 
void g()
{
    f('A'); // OK, calls #2. When checking the constraints of #1,
            // 'sizeof(char) > 1' is not satisfied, so get_value<T>() is not checked
}

```

#### Disjunctions

The disjunction of two constraints is formed by using the `||` operator in the constraint expression.

A disjunction of two constraints is satisfied if either constraint is satisfied. Disjunctions are evaluated left to right and short-circuited (if the left constraint is satisfied, template argument substitution into the right constraint is not attempted).

```
template<class T = void>
    requires EqualityComparable<T> || Same<T, void>
struct equal_to;

```

#### Atomic constraints

An atomic constraint consists of an expression E and a mapping from the template parameters that appear within E to template arguments involving the template parameters of the constrained entity, called its **parameter mapping**.

Atomic constraints are formed during constraint normalization. E is never a logical AND or logical OR expression (those form conjunctions and disjunctions, respectively).

Satisfaction of an atomic constraint is checked by substituting the parameter mapping and template arguments into the expression E. If the substitution results in an invalid type or expression, the constraint is not satisfied. Otherwise, E, after any lvalue-to-rvalue conversion, must be a prvalue constant expression of type bool, and the constraint is satisfied if and only if it evaluates to true.

The type of E after substitution must be exactly bool. No conversion is permitted:

```
template<typename T>
struct S
{
    constexpr operator bool() const { return true; }
};
 
template<typename T>
    requires (S<T>{})
void f(T);   // #1
 
void f(int); // #2
 
void g()
{
    f(0); // error: S<int>{} does not have type bool when checking #1,
          // even though #2 is a better match
}

```

Two atomic constraints are considered **identical** if they are formed from the same expression at the source level and their parameter mappings are equivalent.

```
template<class T>
constexpr bool is_meowable = true;
 
template<class T>
constexpr bool is_cat = true;
 
template<class T>
concept Meowable = is_meowable<T>;
 
template<class T>
concept BadMeowableCat = is_meowable<T> && is_cat<T>;
 
template<class T>
concept GoodMeowableCat = Meowable<T> && is_cat<T>;
 
template<Meowable T>
void f1(T); // #1
 
template<BadMeowableCat T>
void f1(T); // #2
 
template<Meowable T>
void f2(T); // #3
 
template<GoodMeowableCat T>
void f2(T); // #4
 
void g()
{
    f1(0); // error, ambiguous:
           // the is_meowable<T> in Meowable and BadMeowableCat forms distinct atomic
           // constraints that are not identical (and so do not subsume each other)
 
    f2(0); // OK, calls #4, more constrained than #3
           // GoodMeowableCat got its is_meowable<T> from Meowable
}

```

|  |  |
| --- | --- |
| Fold expanded constraints A **fold expanded constraint** is formed from a constraint `C` and a fold operator (either `&&` or `||`). A fold expanded constraint is a pack expansion.  Let N be the number of elements in the pack expansion parameters:   - If the pack expansion is invalid (such as expanding packs of different size), the fold expanded constraint is not satisfied. - If N is ​0​, the fold expanded constraint is satisfied if the fold operator is `&&`, or not satisfied if the fold operator is `||`. - For a fold expanded constraint with a positive N,for each i in `[`1`,`N`]`, each pack expansion parameter is replaced with the corresponding ith element in increasing order:   - For fold expanded constraints whose fold operator is `&&`, if the replacement of the jth element violates `C`, the fold expanded constraint is not satisfied. In this case, no substitution takes place for any i greater than j. Otherwise, the fold expanded constraint is satisfied. - For fold expanded constraints whose fold operator is `||`, if the replacement of the jth element satisfies `C`, the fold expanded constraint is satisfied. In this case, no substitution takes place for any i greater than j. Otherwise, the fold expanded constraint is not satisfied.     ```text template <class T> concept A = std::is_move_constructible_v<T>; template <class T> concept B = std::is_copy_constructible_v<T>; template <class T> concept C = A<T> && B<T>;   // in C++23, these two overloads of g() have distinct atomic constraints  // that are not identical and so do not subsume each other: calls to g() are ambiguous // in C++26, the folds are expanded and constraint on overload #2 (both move and copy // required), subsumes constraint on overload #1 (just the move is required) template <class... T> requires (A<T> && ...) void g(T...); // #1   template <class... T> requires (C<T> && ...) void g(T...); // #2 ``` | (since C++26) |

#### Constraint normalization

**Constraint normalization** is the process that transforms a constraint expression into a sequence of conjunctions and disjunctions of atomic constraints. The **normal form** of an expression is defined as follows:

- The normal form of an expression (E) is the normal form of E.
- The normal form of an expression E1 && E2 is the conjunction of the normal forms of E1 and E2.
- The normal form of an expression E1 || E2 is the disjunction of the normal forms of E1 and E2.
- The normal form of an expression C<A1, A2, ... , AN>, where `C` names a concept, is the normal form of the constraint expression of `C`, after substituting `A1`, `A2`, ... , `AN` for `C`'s respective template parameters in the parameter mappings of each atomic constraint of `C`. If any such substitution into the parameter mappings results in an invalid type or expression, the program is ill-formed, no diagnostic required.

```
template<typename T>
concept A = T::value || true;
 
template<typename U>
concept B = A<U*>; // OK: normalized to the disjunction of 
                   // - T::value (with mapping T -> U*) and
                   // - true (with an empty mapping).
                   // No invalid type in mapping even though
                   // T::value is ill-formed for all pointer types
 
template<typename V>
concept C = B<V&>; // Normalizes to the disjunction of
                   // - T::value (with mapping T-> V&*) and
                   // - true (with an empty mapping).
                   // Invalid type V&* formed in mapping => ill-formed NDR

```

|  |  |
| --- | --- |
| - The normal form of expressions (E && ...) and (... && E) is a fold expanded constraint, where `C` is the normal form of E and the fold operator is `&&`. - The normal form of expressions (E || ...) and (... || E) is a fold expanded constraint, where `C` is the normal form of E and the fold operator is `||`. - The normal forms of expressions (E1 && ... && E2) and (E1 || ... || E2) are the normal forms of   - (E1 && ...) && E2 and (E1 || ...) || E2 respectively, if E1 contains an unexpanded pack, or - E1 && (... && E2) and E1 || (... || E2) respectively otherwise. | (since C++26) |

- The normal form of any other expression E is the atomic constraint whose expression is E and whose parameter mapping is the identity mapping. This includes all fold expressions, even those folding over the `&&` or `||` operators.

User-defined overloads of `&&` or `||` have no effect on constraint normalization.

### requires clauses

The keyword requires is used to introduce a **requires clause**, which specifies constraints on template arguments or on a function declaration.

```
template<typename T>
void f(T&&) requires Eq<T>; // can appear as the last element of a function declarator
 
template<typename T> requires Addable<T> // or right after a template parameter list
T add(T a, T b) { return a + b; }

```

In this case, the keyword requires must be followed by some constant expression (so it's possible to write requires true), but the intent is that a named concept (as in the example above) or a conjunction/disjunction of named concepts or a requires expression is used.

The expression must have one of the following forms:

- A primary expression, e.g. Swappable<T>, std::is_integral<T>::value, (std::is_object_v<Args> && ...), or any parenthesized expression.
- A sequence of primary expressions joined with the operator `&&`.
- A sequence of aforementioned expressions joined with the operator `||`.

```
template<class T>
constexpr bool is_meowable = true;
 
template<class T>
constexpr bool is_purrable() { return true; }
 
template<class T>
void f(T) requires is_meowable<T>; // OK
 
template<class T>
void g(T) requires is_purrable<T>(); // error, is_purrable<T>() is not a primary expression
 
template<class T>
void h(T) requires (is_purrable<T>()); // OK

```

### Partial ordering of constraints

Before any further analysis, constraints are normalized by substituting the body of every named concept and every requires expression until what is left is a sequence of conjunctions and disjunctions on atomic constraints.

A constraint `P` is said to **subsume** constraint `Q` if it can be proven that `P` implies `Q` up to the identity of atomic constraints in P and Q. (Types and expressions are not analyzed for equivalence: `N > 0` does not subsume `N >= 0`).

Specifically, first `P` is converted to disjunctive normal form and `Q` is converted to conjunctive normal form. `P` subsumes `Q` if and only if:

- every disjunctive clause in the disjunctive normal form of `P` subsumes every conjunctive clause in the conjunctive normal form of `Q`, where
- a disjunctive clause subsumes a conjunctive clause if and only if there is an atomic constraint `U` in the disjunctive clause and an atomic constraint `V` in the conjunctive clause such that `U` subsumes `V`;
- an atomic constraint `A` subsumes an atomic constraint `B` if and only if they are identical using the rules described above.

|  |  |
| --- | --- |
| - A fold expanded constraint `A` subsumes another fold expanded constraint `B` if they have the same fold operator, the constraint `C` of `A` subsumes that of `B`, and both `C` contain an equivalent unexpanded pack. | (since C++26) |

Subsumption relationship defines partial order of constraints, which is used to determine:

- the best viable candidate for a non-template function in overload resolution
- the address of a non-template function in an overload set
- the best match for a template template argument
- partial ordering of class template specializations
- partial ordering of function templates

|  |  |
| --- | --- |
|  | This section is incomplete Reason: backlinks from the above to here |

If declarations `D1` and `D2` are constrained and `D1`'s associated constraints subsume `D2`'s associated constraints (or if `D2` is unconstrained), then `D1` is said to be **at least as constrained** as `D2`. If `D1` is at least as constrained as `D2`, and `D2` is not at least as constrained as `D1`, then `D1` is **more constrained** than `D2`.

If all following conditions are satisfied, a non-template function `F1` is **more partial-ordering-constrained** than a non-template function `F2`:

- They have the same parameter-type-list, omitting the types of explicit object parameters(since C++23).
- If they are member functions, both are direct members of the same class.
- If both are non-static member functions, they have the same types for their object parameters.
- `F1` is more constrained than `F2`.

```
template<typename T>
concept Decrementable = requires(T t) { --t; };
template<typename T>
concept RevIterator = Decrementable<T> && requires(T t) { *t; };
 
// RevIterator subsumes Decrementable, but not the other way around
 
template<Decrementable T>
void f(T); // #1
 
template<RevIterator T>
void f(T); // #2, more constrained than #1
 
f(0);       // int only satisfies Decrementable, selects #1
f((int*)0); // int* satisfies both constraints, selects #2 as more constrained
 
template<class T>
void g(T); // #3 (unconstrained)
 
template<Decrementable T>
void g(T); // #4
 
g(true); // bool does not satisfy Decrementable, selects #3
g(0);    // int satisfies Decrementable, selects #4 because it is more constrained
 
template<typename T>
concept RevIterator2 = requires(T t) { --t; *t; };
 
template<Decrementable T>
void h(T); // #5
 
template<RevIterator2 T>
void h(T); // #6
 
h((int*)0); // ambiguous

```

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_concepts` | `201907L` | (C++20) | Constraints |
| `202002L` | (C++20) | Conditionally trivial special member functions |

### Keywords

concept,
requires,
typename

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 2428 | C++20 | could not apply attributes to concepts | allowed |

### See also

- Concepts TS
- Named requirements

|  |  |
| --- | --- |
| Requires expression(C++20) | yields a prvalue expression of type bool that describes the constraints |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/constraints&oldid=179831>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 January 2025, at 23:56.