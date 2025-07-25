# std::experimental::weak_ptr<T>::weak_ptr

From cppreference.com
< cpp‎ | experimental‎ | weak ptr
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

Library fundamentals

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::optional | | | | |
| experimental::any | | | | |
| experimental::basic_string_view | | | | |
| experimental::sample | | | | |
| experimental::shared_ptr | | | | |
| experimental::weak_ptr | | | | |
| experimental::apply | | | | |
| experimental::invocation_typeexperimental::raw_invocation_type | | | | |
| experimental::search | | | | |
| experimental::default_searcherexperimental::make_default_searcher | | | | |
| experimental::boyer_moore_searcherexperimental::make_boyer_moore_searcher | | | | |
| experimental::boyer_moore_horspool_searcherexperimental::make_boyer_moore_horspool_searcher | | | | |
| Type-erased and polymorphic allocators | | | | |
| Variable templates for type traits | | | | |

std::experimental::weak_ptr

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****weak_ptr::weak_ptr**** | | | | |
| Members and non-members identical to those of `std::weak_ptr` | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr weak_ptr() noexcept; | (1) | (library fundamentals TS) |
| weak_ptr( const weak_ptr& r ) noexcept; | (2) | (library fundamentals TS) |
| template< class Y >   weak_ptr( const weak_ptr<Y>& r ) noexcept; | (2) | (library fundamentals TS) |
| template< class Y >   weak_ptr( const std::experimental::shared_ptr<Y>& r ) noexcept; | (2) | (library fundamentals TS) |
| weak_ptr( weak_ptr&& r ) noexcept; | (3) | (library fundamentals TS) |
| template< class Y >   weak_ptr( weak_ptr<Y>&& r ) noexcept; | (3) | (library fundamentals TS) |
|  |  |  |

Constructs a new `weak_ptr` that potentially shares an object with r.

1) Default constructor. Constructs empty `weak_ptr`.2) Constructs new `weak_ptr` which shares an object managed by r. If r manages no object, \*this manages no object too. The templated overloads don't participate in overload resolution unless either `Y*` is implicitly convertible to `T*`, or `Y` is the type "array of `N` `U`" for some type `U` and some number `N`, and `T` is the type "array of unknown bound of (possibly cv-qualified) `U`".3) Move constructors. Moves a `weak_ptr` instance from r into \*this. After this, r is empty and r.use_count() == 0. The templated overload doesn't participate in overload resolution unless either `Y*` is implicitly convertible to `T*`, or `Y` is the type "array of `N` `U`" for some type `U` and some number `N`, and `T` is the type "array of unknown bound of (possibly cv-qualified) `U`".

### Parameters

|  |  |  |
| --- | --- | --- |
| r | - | a std::experimental::shared_ptr or std::experimental::weak_ptr that will be viewed by this std::experimental::weak_ptr |

### Exceptions

noexcept specification:noexcept

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| (constructor) | creates a new `weak_ptr`   (public member function of `std::weak_ptr<T>`) |
| operator= | assigns the `weak_ptr`   (public member function of `std::weak_ptr<T>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/weak_ptr/weak_ptr&oldid=156383>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 August 2023, at 10:13.