# std::char_traits<char>::compare, std::char_traits<wchar_t>::compare, std::char_traits<char8_t>::compare, std::char_traits<char16_t>::compare, std::char_traits<char32_t>::compare

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
| ****char_traits::compare**** | | | | |
| char_traits::length | | | | |
| char_traits::find | | | | |
| char_traits::to_char_type | | | | |
| char_traits::to_int_type | | | | |
| char_traits::eq_int_type | | | | |
| char_traits::eof | | | | |
| char_traits::not_eof | | | | |

|  |  |  |
| --- | --- | --- |
| static int compare( const char_type\* s1, const char_type\* s2,                      std::size_t count ); |  | (constexpr since C++17) |
|  |  |  |

Compares the first count characters of the character strings s1 and s2. The comparison is done lexicographically.

If count is zero, strings are considered equal.

See CharTraits for the general requirements on character traits for `X::compare`.

### Parameters

|  |  |  |
| --- | --- | --- |
| s1, s2 | - | pointers to character strings to compare |
| count | - | the number of characters to compare from each character string |

### Return value

Negative value if s1 is **less than** s2.

​0​ if s1 is **equal to** s2.

Positive value if s1 is **greater than** s2.

### Complexity

Linear in count.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/char_traits/compare&oldid=158860>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 September 2023, at 01:20.