# std::basic_string_view<CharT,Traits>::contains

From cppreference.com
< cpp‎ | string‎ | basic string view
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

std::basic_string_view

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string_view::basic_string_view | | | | | | basic_string_view::operator= | | | | | | Iterators | | | | | | basic_string_view::beginbasic_string_view::cbegin | | | | | | basic_string_view::endbasic_string_view::cend | | | | | | basic_string_view::rbeginbasic_string_view::crbegin | | | | | | basic_string_view::rendbasic_string_view::crend | | | | | | Capacity | | | | | | basic_string_view::sizebasic_string_view::length | | | | | | basic_string_view::max_size | | | | | | basic_string_view::empty | | | | | | Operations | | | | | | basic_string_view::copy | | | | | | basic_string_view::substr | | | | | | basic_string_view::compare | | | | | | basic_string_view::starts_with(C++20) | | | | | | basic_string_view::ends_with(C++20) | | | | | | ****basic_string_view::contains****(C++23) | | | | | | basic_string_view::find | | | | | | basic_string_view::rfind | | | | | | basic_string_view::find_first_of | | | | | | basic_string_view::find_last_of | | | | | | basic_string_view::find_first_not_of | | | | | | basic_string_view::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | basic_string_view::at | | | | | | [basic_string_view::operator[]](operator_at.html "cpp/string/basic string view/operator at") | | | | | | basic_string_view::front | | | | | | basic_string_view::back | | | | | | basic_string_view::data | | | | | | Modifiers | | | | | | basic_string_view::remove_prefix | | | | | | basic_string_view::remove_suffix | | | | | | basic_string_view::swap | | | | | | Constants | | | | | | basic_string_view::npos | | | | | | Non-member functions | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | operator<< | | | | | | operator""sv | | | | | | Helper classes | | | | | | hash<std::string_view>hash<std::wstring_view>hash<std::u8string_view>hash<std::u16string_view>hash<std::u32string_view>(C++20) | | | | | | Deduction guides (C++20) | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr bool contains( basic_string_view sv ) const noexcept; | (1) | (since C++23) |
| constexpr bool contains( CharT c ) const noexcept; | (2) | (since C++23) |
| constexpr bool contains( const CharT\* s ) const; | (3) | (since C++23) |
|  |  |  |

Checks if the string view contains the given substring, where

1) the substring is a string view.2) the substring is a single character.3) the substring is a null-terminated character string.

All three overloads are equivalent to return find(x) != npos;, where `x` is the parameter.

### Parameters

|  |  |  |
| --- | --- | --- |
| sv | - | a string view |
| c | - | a single character |
| s | - | a null-terminated character string |

### Return value

true if the string view contains the provided substring, false otherwise.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_string_contains` | `202011L` | (C++23) | `contains` functions |

### Example

Run this code

```
#include <string_view>
using namespace std::literals;
 
static_assert
(
    // bool contains(basic_string_view x) const noexcept;
    "https://cppreference.com"sv.contains("cpp"sv) == true and
    "https://cppreference.com"sv.contains("php"sv) == false and
 
    // bool contains(CharT x) const noexcept;
    "C++23"sv.contains('+') == true and
    "C++23"sv.contains('-') == false and
 
    // bool contains(const CharT* x) const;
    std::string_view("basic_string_view").contains("string") == true and
    std::string_view("basic_string_view").contains("String") == false
);
 
int main() {}

```

### See also

|  |  |
| --- | --- |
| starts_with(C++20) | checks if the string view starts with the given prefix   (public member function) |
| ends_with(C++20) | checks if the string view ends with the given suffix   (public member function) |
| find | find characters in the view   (public member function) |
| substr | returns a substring   (public member function) |
| contains(C++23) | checks if the string contains the given substring or character   (public member function of `std::basic_string<CharT,Traits,Allocator>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string_view/contains&oldid=153327>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 June 2023, at 14:31.