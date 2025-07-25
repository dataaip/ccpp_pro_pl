# std::char_traits<char>::eq/lt, std::char_traits<wchar_t>::eq/lt, std::char_traits<char8_t>::eq/lt, std::char_traits<char16_t>::eq/lt, std::char_traits<char32_t>::eq/lt

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
| ****char_traits::eqchar_traits::lt**** | | | | |
| char_traits::move | | | | |
| char_traits::copy | | | | |
| char_traits::compare | | | | |
| char_traits::length | | | | |
| char_traits::find | | | | |
| char_traits::to_char_type | | | | |
| char_traits::to_int_type | | | | |
| char_traits::eq_int_type | | | | |
| char_traits::eof | | | | |
| char_traits::not_eof | | | | |

|  |  |  |
| --- | --- | --- |
| static bool eq( char_type a, char_type b ); | (1) | (constexpr since C++11) (noexcept since C++11) |
| static bool lt( char_type a, char_type b ); | (2) | (constexpr since C++11) (noexcept since C++11) |
|  |  |  |

Compares two characters.

1) Compares a and b for equality, behaves identically to

- static_cast<unsigned char>(a) == static_cast<unsigned char>(b), if `char_type` is char,
- a == b otherwise.
2) Compares a and b in such a way that they are totally ordered, behaves identically to

- static_cast<unsigned char>(a) < static_cast<unsigned char>(b), if `char_type` is char,
- a < b otherwise.

See CharTraits for the general requirements on character traits for `X::eq` and `X::lt`.

### Parameters

|  |  |  |
| --- | --- | --- |
| a, b | - | character values to compare |

### Return value

1) true if a and b are equal, false otherwise.2) true if a is less than b, false otherwise.

### Complexity

Constant.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 467 | C++98 | for std::char_traits<char>, the semantics of `eq()` and `lt()` are the same as the built-in == and < on char respectively[[1]](cmp.html#cite_note-1) | changed to built-in == and < on unsigned char |

1. ↑ Most implementations call std::memcmp() for efficiency, which interprets the data as arrays of unsigned char. If char is signed on such implementations, std::char_traits<char> fails to satisfy the requirements of CharTraits.
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/char_traits/cmp&oldid=171371>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 April 2024, at 15:32.