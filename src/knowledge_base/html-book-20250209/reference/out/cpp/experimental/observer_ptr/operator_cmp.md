# operator==,!=,<,<=,>,>=(std::experimental::observer_ptr)

From cppreference.com
< cpp‎ | experimental‎ | observer ptr
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

std::experimental::observer_ptr

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| observer_ptr::observer_ptr | | | | |
| Modifiers | | | | |
| observer_ptr::release | | | | |
| observer_ptr::reset | | | | |
| observer_ptr::swap | | | | |
| Observers | | | | |
| observer_ptr::get | | | | |
| observer_ptr::operator bool | | | | |
| observer_ptr::operator\*observer_ptr::operator-> | | | | |
| Conversions | | | | |
| observer_ptr::operator element_type\* | | | | |
| Non-member functions | | | | |
| make_observer | | | | |
| ****operator==operator!=operator<operator>operator<=operator>operator>=**** | | | | |
| swap | | | | |
| std::hash | | | | |

|  |  |  |
| --- | --- | --- |
| template< class W1, class W2 >  bool operator==( const observer_ptr<W1>& p1, const observer_ptr<W2>& p2 ); | (1) | (library fundamentals TS v2) |
| template< class W1, class W2 >  bool operator!=( const observer_ptr<W1>& p1, const observer_ptr<W2>& p2 ); | (2) | (library fundamentals TS v2) |
| template< class W >  bool operator==( const observer_ptr<W>& p, std::nullptr_t ) noexcept; | (3) | (library fundamentals TS v2) |
| template< class W >  bool operator==( std::nullptr_t, const observer_ptr<W>& p ) noexcept; | (4) | (library fundamentals TS v2) |
| template< class W >  bool operator!=( const observer_ptr<W>& p, std::nullptr_t ) noexcept; | (5) | (library fundamentals TS v2) |
| template< class W >  bool operator!=( std::nullptr_t, const observer_ptr<W>& p ) noexcept; | (6) | (library fundamentals TS v2) |
| template< class W1, class W2 >  bool operator<( const observer_ptr<W1>& p1, const observer_ptr<W2>& p2 ); | (7) | (library fundamentals TS v2) |
| template< class W1, class W2 >  bool operator>( const observer_ptr<W1>& p1, const observer_ptr<W2>& p2 ); | (8) | (library fundamentals TS v2) |
| template< class W1, class W2 >  bool operator<=( const observer_ptr<W1>& p1, const observer_ptr<W2>& p2 ); | (9) | (library fundamentals TS v2) |
| template< class W1, class W2 >  bool operator>=( const observer_ptr<W1>& p1, const observer_ptr<W2>& p2 ); | (10) | (library fundamentals TS v2) |
|  |  |  |

Compares the pointer values of two `observer_ptr`s, or an `observer_ptr` and nullptr.

1,2) Equality comparison for two `observer_ptr`s.3-6) Equality comparison for an `observer_ptr` and nullptr.7-10) Ordered comparison for two `observer_ptr`s.

### Parameters

|  |  |  |
| --- | --- | --- |
| p, p1, p2 | - | `observer_ptr`s to compare |

### Return value

1) p1.get() == p2.get()2) !(p1 == p2)3,4) !p5,6) (bool)p7) std::less<W3>()(p1.get(), p2.get()), where `W3` is the composite pointer type of `W1*` and `W2*`.8) p2 < p19) !(p2 < p1)10) !(p1 < p2)
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/observer_ptr/operator_cmp&oldid=157742>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 September 2023, at 22:44.