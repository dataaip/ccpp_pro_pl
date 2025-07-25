# std::equal_to, not_equal_to, less, greater, less_equal, greater_equal(std::experimental::propagate_const)

From cppreference.com
< cpp‎ | experimental‎ | propagate const
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

Library fundamentals v2

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::propagate_const | | | | |
| experimental::not_fn | | | | |
| experimental::observer_ptr | | | | |
| experimental::make_array | | | | |
| experimental::to_array | | | | |
| experimental::ostream_joiner | | | | |
| experimental::gcd | | | | |
| experimental::lcm | | | | |
| experimental::source_location | | | | |
| experimental::randint | | | | |
| detection idiom | | | | |
| uniform container erasure | | | | |
| logical operator type traits | | | | |

std::experimental::propagate_const

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| propagate_const::propagate_const | | | | |
| propagate_const::operator= | | | | |
| propagate_const::swap | | | | |
| Observers | | | | |
| propagate_const::get | | | | |
| propagate_const::operator bool | | | | |
| propagate_const::operator\*propagate_const::operator-> | | | | |
| propagate_const::operator element_type\*propagate_const::operator const element_type\* | | | | |
| Non-member functions | | | | |
| operator==operator!=operator<operator>operator<=operator>operator>= | | | | |
| swap | | | | |
| get_underlying | | | | |
| Helper classes | | | | |
| std::hash | | | | |
| ****std::equal_tostd::not_equal_tostd::lessstd::greaterstd::less_equalstd::greater_equal**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/propagate_const>` |  |  |
| template< class T > struct equal_to<std::experimental::propagate_const<T>>; |  | (library fundamentals TS v2) |
| template< class T > struct not_equal_to<std::experimental::propagate_const<T>>; |  | (library fundamentals TS v2) |
| template< class T > struct less<std::experimental::propagate_const<T>>; |  | (library fundamentals TS v2) |
| template< class T > struct greater<std::experimental::propagate_const<T>>; |  | (library fundamentals TS v2) |
| template< class T > struct less_equal<std::experimental::propagate_const<T>>; |  | (library fundamentals TS v2) |
| template< class T > struct greater_equal<std::experimental::propagate_const<T>>; |  | (library fundamentals TS v2) |
|  |  |  |

The standard comparison function objects are partially specialized for std::experimental::propagate_const<T>.

Let p.t_ denote the pointer-like object wrapped by a std::experimental::propagate_const<T> p, then given objects `p` and `q` of type std::experimental::propagate_const<T>, the following shall hold:

- std::equal_to<std::experimental::propagate_const<T>>()(p, q) == std::equal_to<T>()(p.t_, q.t_)
- std::not_equal_to<std::experimental::propagate_const<T>>()(p, q) == std::not_equal_to<T>()(p.t_, q.t_)
- std::less<std::experimental::propagate_const<T>>()(p, q) == std::less<T>()(p.t_, q.t_)
- std::greater<std::experimental::propagate_const<T>>()(p, q) == std::greater<T>()(p.t_, q.t_)
- std::less_equal<std::experimental::propagate_const<T>>()(p, q) == std::less_equal<T>()(p.t_, q.t_)
- std::greater_equal<std::experimental::propagate_const<T>>()(p, q) == std::greater_equal<T>()(p.t_, q.t_)

### Notes

These specializations ensure that when `T` is a pointer type, specializations of these class templates for std::experimental::propagate_const<T> yield a total order, even if the corresponding built-in operators do not.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| equal_to | function object implementing x == y   (class template) |
| not_equal_to | function object implementing x != y   (class template) |
| less | function object implementing x < y   (class template) |
| greater | function object implementing x > y   (class template) |
| less_equal | function object implementing x <= y   (class template) |
| greater_equal | function object implementing x >= y   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/propagate_const/cmp_func&oldid=155173>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 July 2023, at 02:59.