# std::basic_string<CharT,Traits,Allocator>::find

From cppreference.com
< cpp‎ | string‎ | basic string
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

std::basic_string

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string::basic_string | | | | | | basic_string::~basic_string | | | | | | basic_string::operator= | | | | | | basic_string::assign | | | | | | basic_string::assign_range(C++23) | | | | | | basic_string::get_allocator | | | | | | Element access | | | | | | basic_string::at | | | | | | [basic_string::operator[]](operator_at.html "cpp/string/basic string/operator at") | | | | | | basic_string::front(DR\*) | | | | | | basic_string::back(DR\*) | | | | | | basic_string::data | | | | | | basic_string::c_str | | | | | | basic_string::operator  basic_string_view(C++17) | | | | | | Iterators | | | | | | basic_string::beginbasic_string::cbegin(C++11) | | | | | | basic_string::endbasic_string::cend(C++11) | | | | | | basic_string::rbeginbasic_string::crbegin(C++11) | | | | | | basic_string::rendbasic_string::crend(C++11) | | | | | | Search | | | | | | ****basic_string::find**** | | | | | | basic_string::rfind | | | | | | basic_string::find_first_of | | | | | | basic_string::find_first_not_of | | | | | | basic_string::find_last_of | | | | | | basic_string::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | basic_string::clear | | | | | | basic_string::insert | | | | | | basic_string::insert_range(C++23) | | | | | | basic_string::erase | | | | | | basic_string::push_back | | | | | | basic_string::pop_back(DR\*) | | | | | | basic_string::append | | | | | | basic_string::append_range(C++23) | | | | | | basic_string::operator+= | | | | | | basic_string::replace | | | | | | basic_string::replace_with_range(C++23) | | | | | | basic_string::copy | | | | | | basic_string::resize | | | | | | basic_string::resize_and_overwrite(C++23) | | | | | | basic_string::swap | | | | | | Capacity | | | | | | basic_string::empty | | | | | | basic_string::sizebasic_string::length | | | | | | basic_string::max_size | | | | | | basic_string::reserve | | | | | | basic_string::capacity | | | | | | basic_string::shrink_to_fit(DR\*) | | | | | | Operations | | | | | | basic_string::compare | | | | | | basic_string::starts_with(C++20) | | | | | | basic_string::ends_with(C++20) | | | | | | basic_string::contains(C++23) | | | | | | basic_string::substr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constants | | | | | | basic_string::npos | | | | | | Non-member functions | | | | | | operator+ | | | | | | swap(std::basic_string) | | | | | | erase(std::basic_string)erase_if(std::basic_string)(C++20)(C++20) | | | | | | I/O | | | | | | operator<<operator>> | | | | | | getline | | | | | | Comparison | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | Numeric conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stoistolstoll(C++11)(C++11)(C++11) | | | | | | stoulstoull(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stofstodstold(C++11)(C++11)(C++11) | | | | | | to_string(C++11) | | | | | | to_wstring(C++11) | | | | | | | Literals | | | | | | operator""s(C++14) | | | | | | Helper classes | | | | | | hash<std::basic_string>(C++11) | | | | | | Deduction guides (C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| size_type find( const basic_string& str, size_type pos = 0 ) const; | (1) | (noexcept since C++11)  (constexpr since C++20) |
| size_type find( const CharT\* s, size_type pos, size_type count ) const; | (2) | (constexpr since C++20) |
| size_type find( const CharT\* s, size_type pos = 0 ) const; | (3) | (constexpr since C++20) |
| size_type find( CharT ch, size_type pos = 0 ) const; | (4) | (noexcept since C++11)  (constexpr since C++20) |
| template< class StringViewLike >  size_type find( const StringViewLike& t,                 size_type pos = 0 ) const noexcept(/\* see below \*/); | (5) | (since C++17)  (constexpr since C++20) |
|  |  |  |

Finds the first substring equal to the given character sequence. Search begins at pos, i.e. the found substring must not begin in a position preceding pos.

1) Finds the first substring equal to str.2) Finds the first substring equal to the range ``s`,`s + count`)`. This range may contain null characters. If `[`s`,`s + count`)` is not a [valid range, the behavior is undefined.3) Finds the first substring equal to the character string pointed to by s. The length of the string is determined by the first null character using Traits::length(s). If ``s`,`s + Traits::length(s)`)` is not a [valid range, the behavior is undefined.4) Finds the first character ch (treated as a single-character substring by the formal rules below).5) Implicitly converts t to a string view sv as if by std::basic_string_view<CharT, Traits> sv = t;, then finds the first substring equal to sv. This overload participates in overload resolution only if std::is_convertible_v<const StringViewLike&,  
                      std::basic_string_view<CharT, Traits>> is true and std::is_convertible_v<const StringViewLike&, const CharT\*> is false.

Formally, a substring str is said to be **found** at position xpos if all of the following are true:

- xpos >= pos
- xpos + str.size() <= size()
- for all positions n in str, Traits::eq(at(xpos + n), str.at(n)).

In particular, this implies that

- a substring can be found only if pos <= size() - str.size()
- an empty substring is found at pos if and only if pos <= size()
- for a non-empty substring, if pos >= size(), the function always returns npos.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | string to search for |
| pos | - | position at which to start the search |
| count | - | length of substring to search for |
| s | - | pointer to a character string to search for |
| ch | - | character to search for |
| t | - | object (convertible to std::basic_string_view) to search for |

### Return value

Position of the first character of the found substring or npos if no such substring is found.

### Exceptions

1,4) Throws nothing.5)noexcept specification:noexcept(std::is_nothrow_convertible_v<const T&, std::basic_string_view<CharT, Traits>>)

If an exception is thrown for any reason, this function has no effect (strong exception safety guarantee).

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <string>
 
void print(int id, std::string::size_type n, std::string const& s)
{
    std::cout << id << ") ";
    if (std::string::npos == n)
        std::cout << "not found! n == npos\n";
    else
        std::cout << "found @ n = " << n << ", substr(" << n << ") = "
                  << std::quoted(s.substr(n)) << '\n';
}
 
int main()
{
    std::string::size_type n;
    std::string const s = "This is a string"; /*
                             ^  ^  ^
                             1  2  3          */
 
    // search from beginning of string
    n = s.find("is");
    print(1, n, s);
 
    // search from position 5
    n = s.find("is", 5);
    print(2, n, s);
 
    // find a single character
    n = s.find('a');
    print(3, n, s);
 
    // find a single character
    n = s.find('q');
    print(4, n, s);
}

```

Output:

```
1) found @ n = 2, substr(2) = "is is a string"
2) found @ n = 5, substr(5) = "is a string"
3) found @ n = 8, substr(8) = "a string"
4) not found! n == npos

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 847 | C++98 | there was no exception safety guarantee | added strong exception safety guarantee |
| LWG 2064 | C++11 | overloads (3,4) were noexcept | removed |
| LWG 2946 | C++17 | overload (5) caused ambiguity in some cases | avoided by making it a template |
| P1148R0 | C++11 C++17 | noexcept for overloads (4,5) were accidently dropped by LWG2064/LWG2946 | restored |

### See also

|  |  |
| --- | --- |
| strstr | finds the first occurrence of a substring of characters   (function) |
| wcsstr | finds the first occurrence of a wide string within another wide string   (function) |
| strchr | finds the first occurrence of a character   (function) |
| wcschr | finds the first occurrence of a wide character in a wide string   (function) |
| rfind | find the last occurrence of a substring   (public member function) |
| find_first_of | find first occurrence of characters   (public member function) |
| find_first_not_of | find first absence of characters   (public member function) |
| find_last_of | find last occurrence of characters   (public member function) |
| find_last_not_of | find last absence of characters   (public member function) |
| find | find characters in the view   (public member function of `std::basic_string_view<CharT,Traits>`) |
| search | searches for the first occurrence of a range of elements   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string/find&oldid=172135>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 May 2024, at 14:53.