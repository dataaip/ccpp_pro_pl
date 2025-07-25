# std::experimental::optional<T>::swap

From cppreference.com
< cpp‎ | experimental‎ | optional
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

std::experimental::optional

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| optional::optional | | | | |
| optional::~optional | | | | |
| optional::operator= | | | | |
| Observers | | | | |
| optional::operator->optional::operator\* | | | | |
| optional::operator bool | | | | |
| optional::value | | | | |
| optional::value_or | | | | |
| Modifiers | | | | |
| optional::emplace | | | | |
| ****optional::swap**** | | | | |
| Non-member functions | | | | |
| operator==operator!=operator<operator<=operator>operator>= | | | | |
| make_optional | | | | |
| swap | | | | |
| Helper classes | | | | |
| hash | | | | |
| nullopt_t | | | | |
| in_place_t | | | | |
| bad_optional_access | | | | |
| Helper objects | | | | |
| nullopt | | | | |
| in_place | | | | |

|  |  |  |
| --- | --- | --- |
| void swap( optional& other ) noexcept(/\* see below \*/); |  | (library fundamentals TS) |
|  |  |  |

Swaps the contents with those of other.

- If neither \*this nor other contain a value, the function has no effect.

- If only one of \*this and other contains a value (let's call this object `in` and the other `un`), the contained value of `un` is direct-initialized from std::move(\*in), followed by destruction of the contained value of `in` as if by in.val->T::~T(). After this call, `in` does not contain a value `un` contains a value.

- If both \*this and other contain values, the contained values are exchanged by calling using std::swap; swap(\*\*this, \*other). `T` lvalues must satisfy Swappable.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | the `optional` object to exchange the contents with |

### Return value

(none)

### Exceptions

noexcept specification:noexcept(std::is_nothrow_move_constructible<T>::value &&   
           noexcept(swap(std::declval<T&>(), std::declval<T&>())))

In the case of thrown exception, the states of the contained values of \*this and other are determined by the exception safety guarantees of `swap` of type `T` or `T`'s move constructor, whichever is called. For both \*this and other, if the object contained a value, it is left containing a value, and the other way round.

### See also

|  |  |
| --- | --- |
| std::swap(std::experimental::optional) | specializes the std::swap algorithm   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/optional/swap&oldid=155042>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 July 2023, at 01:14.