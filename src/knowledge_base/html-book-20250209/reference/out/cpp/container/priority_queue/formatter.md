# std::formatter<std::priority_queue>

From cppreference.com
< cpp‎ | container‎ | priority queue
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

Containers library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Sequence | | | | |
| array(C++11) | | | | |
| vector | | | | |
| vector<bool> | | | | |
| inplace_vector(C++26) | | | | |
| deque | | | | |
| forward_list(C++11) | | | | |
| list | | | | |
| Associative | | | | |
| set | | | | |
| multiset | | | | |
| map | | | | |
| multimap | | | | |
| Unordered associative | | | | |
| unordered_set(C++11) | | | | |
| unordered_multiset(C++11) | | | | |
| unordered_map(C++11) | | | | |
| unordered_multimap(C++11) | | | | |
| Adaptors | | | | |
| stack | | | | |
| queue | | | | |
| priority_queue | | | | |
| flat_set(C++23) | | | | |
| flat_multiset(C++23) | | | | |
| flat_map(C++23) | | | | |
| flat_multimap(C++23) | | | | |
| Views | | | | |
| span(C++20) | | | | |
| mdspan(C++23) | | | | |
| Tables | | | | |
| Iterator invalidation | | | | |
| Member function table | | | | |
| Non-member function table | | | | |

`std::priority_queue`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| priority_queue::priority_queue | | | | |
| priority_queue::~priority_queue | | | | |
| priority_queue::operator= | | | | |
| Element access | | | | |
| priority_queue::top | | | | |
| Capacity | | | | |
| priority_queue::empty | | | | |
| priority_queue::size | | | | |
| Modifiers | | | | |
| priority_queue::push | | | | |
| priority_queue::push_range(C++23) | | | | |
| priority_queue::emplace(C++11) | | | | |
| priority_queue::pop | | | | |
| priority_queue::swap(C++11) | | | | |
| Non-member functions | | | | |
| swap(std::priority_queue)(C++11) | | | | |
| Helper classes | | | | |
| uses_allocator<std::priority_queue>(C++11) | | | | |
| ****formatter<std::priority_queue>****(C++23) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<queue>` |  |  |
| template< class CharT, class T, std::formattable<CharT> Container, class... U >  struct formatter<std::priority_queue<T, Container, U...>, CharT>; |  | (since C++23) |
|  |  |  |

The template specialization of std::formatter for the container adaptor type std::priority_queue allows users to convert the underlying container to its textual representation as a collection of elements using formatting functions.

The specialization is enabled if std::formattable<Container, CharT> is true.

### Member types

|  |  |
| --- | --- |
| Name | Definition |
| `maybe-const-container﻿` | `fmt-maybe-const` ﻿<Container, CharT> (exposition-only member type\*) |
| `maybe-const-adaptor` | **maybe-const** ﻿< std::is_const_v<`maybe-const-container`>, std::priority_queue<T, Container, U...>> (exposition-only member type\*) |

### Data members

|  |  |
| --- | --- |
| Name | Definition |
| `underlying_` | underlying formatter of type std::formatter<ranges::ref_view<`maybe-const-container`>, CharT> (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| parse | parses the format specifier as specified by range-format-spec   (public member function) |
| format | writes the range formatted output as specified by range-format-spec   (public member function) |

## std::formatter<std::priority_queue>::parse

|  |  |  |
| --- | --- | --- |
| template< class ParseContext >  constexpr auto parse( ParseContext& ctx ) -> ParseContext::iterator; |  |  |
|  |  |  |

Equivalent to return`underlying_` ﻿.parse(ctx);.

### Return value

An iterator past the end of the range-format-spec of the underlying container.

## std::formatter<std::priority_queue>::format

|  |  |  |
| --- | --- | --- |
| template< class FormatContext >  auto format( /\*maybe-const-adaptor\*/& r, FormatContext& ctx ) const -> FormatContext::iterator; |  |  |
|  |  |  |

Equivalent to return`underlying_` ﻿.format(r.c, ctx);.

### Return value

An iterator past the end of the output range.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| formatter(C++20) | defines formatting rules for a given type   (class template) |
| range_formatter(C++23) | class template that helps implementing std::formatter specializations for range types   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/priority_queue/formatter&oldid=171223>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 April 2024, at 17:17.