# std::experimental::ranges::swap

From cppreference.com
< cpp‎ | experimental‎ | ranges
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Ranges

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Concepts | | | | |
| General utilities | | | | |
| Iterators | | | | |
| Ranges | | | | |
| Algorithms | | | | |

General utilities library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Utility components | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****swap**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | exchange | | | | | |
| Function objects | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | invoke | | | | | | identity | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_to | | | | | | not_equal_to | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | greater | | | | | | less | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | greater_equal | | | | | | less_equal | | | | | |
| Metaprogramming and type traits | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_swappable_withis_swappable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_nothrow_swappable_withis_nothrow_swappable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_reference | | | | | | common_type | | | | | |
| Tagged pairs and tuples | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | TagSpecifier | | | | | | TaggedType | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged | | | | | | tag specifiers | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged_pair | | | | | | make_tagged_pair | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged_tuple | | | | | | make_tagged_tuple | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/ranges/utility>` |  |  |
| namespace {  constexpr /\* unspecified \*/ swap = /\* unspecified \*/; } |  | (ranges TS)  (customization point object) |
| Call signature |  |  |
| template< class T, class U >      requires /\* see below \*/ void swap( T&& t, U&& u ) noexcept(/\* see below \*/); |  |  |
|  |  |  |

Exchanges the values referenced by t and u.

A call to `ranges::swap` is equivalent to:

1) (void)swap(std::forward<T>(t), std::forward<U>(u)), if that expression is valid, where the overload resolution is performed with the following candidates:

- template<class T> void swap(T&, T&) = delete;
- template<class T, std::size_t N> void swap(T(&)[N], T(&)[N]) = delete;
- any declarations of `swap` found by argument-dependent lookup.
 If the function selected by overload resolution does not exchange the values referenced by t and u, the program is ill-formed; no diagnostic required.2) Otherwise, (void)ranges::swap_ranges(t, u), if `T` and `U` are lvalue references to array types of equal extent (but possibly different element types) and ranges::swap(\*t, \*u) is a valid expression.3) Otherwise, if `T` and `U` are both `V&` for some type `V` that meets the syntactic requirements of MoveConstructible<V> and Assignable<V&, V>, exchanges the referenced values as if by V v{std::move(t)}; t = std::move(u); u = std::move(v);. If the semantic requirements of either concept are not satisfied, the program is ill-formed; no diagnostic required.4) In all other cases, a call to `ranges::swap` is ill-formed.

ranges::swap can be used in a constant expression if every function it calls (as specified above) can be so used.

### Customization point objects

The name `ranges::swap` denotes a **customization point object**, which is a function object of a literal `Semiregular` class type (denoted, for exposition purposes, as `SwapT`). All instances of `SwapT` are equal. Thus, `ranges::swap` can be copied freely and its copies can be used interchangeably.

Given a set of types `Args...`, if std::declval<Args>()... meet the requirements for arguments to `ranges::swap` above, `SwapT` will satisfy ranges::Invocable<const SwapT, Args...>. Otherwise, no function call operator of `SwapT` participates in overload resolution.

In every translation unit in which `ranges::swap` is defined, it refers to the same instance of the customization point object. (This means that it can be used freely in things like inline functions and function templates without violating the one-definition rule.)

### Exceptions

1)noexcept specification:noexcept(noexcept((void)swap(std::forward<T>(t), std::forward<T>(u)))), where `swap` is found as described above.2)noexcept specification:noexcept(noexcept(ranges::swap(\*t, \*u)))3)noexcept specification:noexcept(std::is_nothrow_move_constructible<V>::value &&  
         std::is_nothrow_move_assignable<V>::value)

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| swap | swaps the values of two objects   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/utility/swap&oldid=155626>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 July 2023, at 22:23.