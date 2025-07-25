# std::char_traits<char>::to_char_type, std::char_traits<wchar_t>::to_char_type, std::char_traits<char8_t>::to_char_type, std::char_traits<char16_t>::to_char_type, std::char_traits<char32_t>::to_char_type

From cppreference.com
< cpp‎ | string‎ | char traits
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

Strings library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| basic_string | | | | |
| basic_string_view(C++17) | | | | |
| char_traits | | | | |

std::char_traits

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| char_traits::assign | | | | |
| char_traits::eqchar_traits::lt | | | | |
| char_traits::move | | | | |
| char_traits::copy | | | | |
| char_traits::compare | | | | |
| char_traits::length | | | | |
| char_traits::find | | | | |
| ****char_traits::to_char_type**** | | | | |
| char_traits::to_int_type | | | | |
| char_traits::eq_int_type | | | | |
| char_traits::eof | | | | |
| char_traits::not_eof | | | | |

|  |  |  |
| --- | --- | --- |
| static char_type to_char_type( int_type c ); |  | (constexpr since C++11) (noexcept since C++11) |
|  |  |  |

Converts c to `char_type`. If there is no equivalent `char_type` value (such as when c is a copy of the `eof()` value), the result is unspecified.

See CharTraits for the general requirements on character traits for `X::to_char_type`.

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | value to convert |

### Return value

A value equivalent to c.

### Complexity

Constant.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/char_traits/to_char_type&oldid=171374>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 April 2024, at 15:38.