# std::experimental::ranges::SizedRange

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

Ranges library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range | | | | | | ****SizedRange**** | | | | | | View | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | BoundedRange | | | | | | InputRange | | | | | | OutputRange | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ForwardRange | | | | | | BidirectionalRange | | | | | | RandomAccessRange | | | | | |
| Range access | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | begincbegin") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | endcend") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rbegincrbegin") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rendcrend") | | | | | |
| Range primitives | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iterator_tsentinel_t | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | size") | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | datacdata") | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty") | | | | | |  | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/ranges/range>` |  |  |
| template< class T >  concept bool SizedRange =      Range<T> &&      !ranges::disable_sized_range<std::remove_cv_t<std::remove_reference_t<T>>> &&      requires(T& t) {          { ranges::size(t) }               -> ConvertibleTo<ranges::difference_type_t<ranges::iterator_t<T>>>; }; |  | (ranges TS) |
|  |  |  |

|  |  |
| --- | --- |
|  | This section is incomplete Reason: add description and extra caveats |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/range/SizedRange&oldid=155565>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 July 2023, at 23:30.