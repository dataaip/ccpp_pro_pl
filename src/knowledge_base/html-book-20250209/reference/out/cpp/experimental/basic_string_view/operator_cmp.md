# operator==,!=,<,<=,>,>=(std::experimental::basic_string_view)

From cppreference.com
< cpp‎ | experimental‎ | basic string view
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

std::experimental::basic_string_view

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string_view::basic_string_view | | | | | | basic_string_view::operator= | | | | | | Iterators | | | | | | basic_string_view::beginbasic_string_view::cbegin | | | | | | basic_string_view::endbasic_string_view::cend | | | | | | basic_string_view::rbeginbasic_string_view::crbegin | | | | | | basic_string_view::rendbasic_string_view::crend | | | | | | Element access | | | | | | basic_string_view::at | | | | | | [basic_string_view::operator[]](operator_at.html "cpp/experimental/basic string view/operator at") | | | | | | basic_string_view::front | | | | | | basic_string_view::back | | | | | | basic_string_view::data | | | | | | Capacity | | | | | | basic_string_view::sizebasic_string_view::length | | | | | | basic_string_view::max_size | | | | | | basic_string_view::empty | | | | | | Modifiers | | | | | | basic_string_view::remove_prefix | | | | | | basic_string_view::remove_suffix | | | | | | basic_string_view::swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Operations | | | | | | basic_string_view::to_stringbasic_string_view::operator basic_string | | | | | | basic_string_view::copy | | | | | | basic_string_view::substr | | | | | | basic_string_view::compare | | | | | | basic_string_view::find | | | | | | basic_string_view::rfind | | | | | | basic_string_view::find_first_of | | | | | | basic_string_view::find_last_of | | | | | | basic_string_view::find_first_not_of | | | | | | basic_string_view::find_last_not_of | | | | | | Constants | | | | | | basic_string_view::npos | | | | | | Non-member functions | | | | | | ****operator==operator!=operator<operator>operator<=operator>=**** | | | | | | operator<< | | | | | | Helper classes | | | | | | hash<std::string_view>hash<std::wstring_view>hash<std::u16string_view>hash<std::u32string_view> | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/string_view>` |  |  |
| Compare two `basic_string_view` objects |  |  |
| template< class CharT, class Traits >  constexpr bool operator==( basic_string_view <CharT,Traits> lhs,                            basic_string_view <CharT,Traits> rhs ) noexcept; | (1) | (library fundamentals TS) |
| template< class CharT, class Traits >  constexpr bool operator!=( basic_string_view <CharT,Traits> lhs,                            basic_string_view <CharT,Traits> rhs ) noexcept; | (2) | (library fundamentals TS) |
| template< class CharT, class Traits >  constexpr bool operator<( basic_string_view <CharT,Traits> lhs,                           basic_string_view <CharT,Traits> rhs ) noexcept; | (3) | (library fundamentals TS) |
| template< class CharT, class Traits >  constexpr bool operator<=( basic_string_view <CharT,Traits> lhs,                            basic_string_view <CharT,Traits> rhs ) noexcept; | (4) | (library fundamentals TS) |
| template< class CharT, class Traits >  constexpr bool operator>( basic_string_view <CharT,Traits> lhs,                           basic_string_view <CharT,Traits> rhs ) noexcept; | (5) | (library fundamentals TS) |
| template< class CharT, class Traits >  constexpr bool operator>=( basic_string_view <CharT,Traits> lhs,                            basic_string_view <CharT,Traits> rhs ) noexcept; | (6) | (library fundamentals TS) |
|  |  |  |

Compares two views.

All comparisons are done via the compare() member function (which itself is defined in terms of `Traits::compare()`):

- Two views are equal if both the size of lhs and rhs are equal and each character in lhs has an equivalent character in rhs at the same position.

- The ordering comparisons are done lexicographically -- the comparison is performed by a function equivalent to std::lexicographical_compare.

The implementation shall provide sufficient additional `constexpr` and `noexcept` overloads of these functions so that a `basic_string_view<CharT,Traits>` object `sv` may be compared to another object `t` with an implicit conversion to `basic_string_view<CharT,Traits>`, with semantics identical to comparing `sv` and `basic_string_view<CharT,Traits>(t)`.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | views to compare |

### Return value

true if the corresponding comparison holds, false otherwise.

### Complexity

Linear in the size of the views.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/basic_string_view/operator_cmp&oldid=156793>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 August 2023, at 23:06.