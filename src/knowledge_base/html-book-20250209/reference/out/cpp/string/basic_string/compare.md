# std::basic_string<CharT,Traits,Allocator>::compare

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string::basic_string | | | | | | basic_string::~basic_string | | | | | | basic_string::operator= | | | | | | basic_string::assign | | | | | | basic_string::assign_range(C++23) | | | | | | basic_string::get_allocator | | | | | | Element access | | | | | | basic_string::at | | | | | | [basic_string::operator[]](operator_at.html "cpp/string/basic string/operator at") | | | | | | basic_string::front(DR\*) | | | | | | basic_string::back(DR\*) | | | | | | basic_string::data | | | | | | basic_string::c_str | | | | | | basic_string::operator  basic_string_view(C++17) | | | | | | Iterators | | | | | | basic_string::beginbasic_string::cbegin(C++11) | | | | | | basic_string::endbasic_string::cend(C++11) | | | | | | basic_string::rbeginbasic_string::crbegin(C++11) | | | | | | basic_string::rendbasic_string::crend(C++11) | | | | | | Search | | | | | | basic_string::find | | | | | | basic_string::rfind | | | | | | basic_string::find_first_of | | | | | | basic_string::find_first_not_of | | | | | | basic_string::find_last_of | | | | | | basic_string::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | basic_string::clear | | | | | | basic_string::insert | | | | | | basic_string::insert_range(C++23) | | | | | | basic_string::erase | | | | | | basic_string::push_back | | | | | | basic_string::pop_back(DR\*) | | | | | | basic_string::append | | | | | | basic_string::append_range(C++23) | | | | | | basic_string::operator+= | | | | | | basic_string::replace | | | | | | basic_string::replace_with_range(C++23) | | | | | | basic_string::copy | | | | | | basic_string::resize | | | | | | basic_string::resize_and_overwrite(C++23) | | | | | | basic_string::swap | | | | | | Capacity | | | | | | basic_string::empty | | | | | | basic_string::sizebasic_string::length | | | | | | basic_string::max_size | | | | | | basic_string::reserve | | | | | | basic_string::capacity | | | | | | basic_string::shrink_to_fit(DR\*) | | | | | | Operations | | | | | | ****basic_string::compare**** | | | | | | basic_string::starts_with(C++20) | | | | | | basic_string::ends_with(C++20) | | | | | | basic_string::contains(C++23) | | | | | | basic_string::substr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constants | | | | | | basic_string::npos | | | | | | Non-member functions | | | | | | operator+ | | | | | | swap(std::basic_string) | | | | | | erase(std::basic_string)erase_if(std::basic_string)(C++20)(C++20) | | | | | | I/O | | | | | | operator<<operator>> | | | | | | getline | | | | | | Comparison | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | Numeric conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stoistolstoll(C++11)(C++11)(C++11) | | | | | | stoulstoull(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stofstodstold(C++11)(C++11)(C++11) | | | | | | to_string(C++11) | | | | | | to_wstring(C++11) | | | | | | | Literals | | | | | | operator""s(C++14) | | | | | | Helper classes | | | | | | hash<std::basic_string>(C++11) | | | | | | Deduction guides (C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| int compare( const basic_string& str ) const; | (1) | (noexcept since C++11)  (constexpr since C++20) |
| int compare( size_type pos1, size_type count1,               const basic_string& str ) const; | (2) | (constexpr since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| int compare( size_type pos1, size_type count1,  const basic_string& str,              size_type pos2, size_type count2 ) const; |  | (until C++14) |
| int compare( size_type pos1, size_type count1,  const basic_string& str,              size_type pos2, size_type count2 = npos ) const; |  | (since C++14)  (constexpr since C++20) |
|  |  |  |
| --- | --- | --- |
| int compare( const CharT\* s ) const; | (4) | (constexpr since C++20) |
| int compare( size_type pos1, size_type count1,               const CharT\* s ) const; | (5) | (constexpr since C++20) |
| int compare( size_type pos1, size_type count1,               const CharT\* s, size_type count2 ) const; | (6) | (constexpr since C++20) |
| template< class StringViewLike >  int compare( const StringViewLike& t ) const noexcept(/\* see below \*/); | (7) | (since C++17)  (constexpr since C++20) |
| template< class StringViewLike >  int compare( size_type pos1, size_type count1, const StringViewLike& t ) const; | (8) | (since C++17)  (constexpr since C++20) |
| template< class StringViewLike >  int compare( size_type pos1, size_type count1,               const StringViewLike& t,              size_type pos2, size_type count2 = npos) const; | (9) | (since C++17)  (constexpr since C++20) |
|  |  |  |

Compares two character sequences.

1) Compares this string to str.2) Compares a ``pos1`,`pos1 + count1`)` substring of this string to str.

- If count1 > size() - pos1, the substring is `[`pos1`,`size()`)`.
3) Compares a `[`pos1`,`pos1 + count1`)` substring of this string to a substring `[`pos2`,`pos2 + count2`)` of str.

- If count1 > size() - pos1, the first substring is `[`pos1`,`size()`)`.
- If count2 > str.size() - pos2, the second substring is `[`pos2`,`str.size()`)`.
4) Compares this string to the null-terminated character sequence beginning at the character pointed to by s with length Traits::length(s).5) Compares a `[`pos1`,`pos1 + count1`)` substring of this string to the null-terminated character sequence beginning at the character pointed to by s with length Traits::length(s).

- If count1 > size() - pos1, the substring is `[`pos1`,`size()`)`.
6) Compares a `[`pos1`,`pos1 + count1`)` substring of this string to the characters in the range `[`s`,`s + count2`)`. The characters in `[`s`,`s + count2`)` may include null characters.

- If count1 > size() - pos1, the substring is `[`pos1`,`size()`)`.
7-9) Implicitly converts t to a string view sv as if by [std::basic_string_view<CharT, Traits> sv = t;, then7) compares this string to sv;8) compares a ``pos1`,`pos1 + count1`)` substring of this string to sv, as if by [std::basic_string_view<CharT, Traits>(\*this).substr(pos1, count1).compare(sv);9) compares a ``pos1`,`pos1 + count1`)` substring of this string to a substring `[`pos2`,`pos2 + count2`)` of sv, as if by [std::basic_string_view<CharT, Traits>(\*this)  
    .substr(pos1, count1).compare(sv.substr(pos2, count2)). These overloads participate in overload resolution only if std::is_convertible_v<const StringViewLike&,  
                      std::basic_string_view<CharT, Traits>> is true and std::is_convertible_v<const StringViewLike&, const CharT\*> is false..

A character sequence consisting of count1 characters starting at data1 is compared to a character sequence consisting of count2 characters starting at data2 as follows:

- First, calculate the number of characters to compare, as if by size_type rlen = std::min(count1, count2).
- Then compare the sequences by calling Traits::compare(data1, data2, rlen). For standard strings this function performs character-by-character lexicographical comparison. If the result is zero (the character sequences are equal so far), then their sizes are compared as follows:

| Condition | | Result | Return value |
| --- | --- | --- | --- |
| `Traits::compare(data1, data2, rlen) < 0` | | data1 is **less** than data2 | <0 |
| `Traits::compare(data1, data2, rlen) == 0` | size1 < size2 | data1 is **less** than data2 | <0 |
| size1 == size2 | data1 is **equal** to data2 | ​0​ |
| size1 > size2 | data1 is **greater** than data2 | >0 |
| `Traits::compare(data1, data2, rlen) > 0` | | data1 is **greater** than data2 | >0 |

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | other string to compare to |
| s | - | pointer to the character string to compare to |
| count1 | - | number of characters of this string to compare |
| pos1 | - | position of the first character in this string to compare |
| count2 | - | number of characters of the given string to compare |
| pos2 | - | position of the first character of the given string to compare |
| t | - | object (convertible to std::basic_string_view) to compare to |

### Return value

- Negative value if \*this appears before the character sequence specified by the arguments, in lexicographical order.
- Zero if both character sequences compare equivalent.
- Positive value if \*this appears after the character sequence specified by the arguments, in lexicographical order.

### Exceptions

The overloads taking parameters named pos1 or pos2 throws std::out_of_range if the argument is out of range.

7)noexcept specification:noexcept(std::is_nothrow_convertible_v<const T&, std::basic_string_view<CharT, Traits>>)8,9) Throws anything thrown by the conversion to std::basic_string_view.

If an exception is thrown for any reason, this function has no effect (strong exception safety guarantee).

### Possible implementation

| overload (1) |
| --- |
| ```text template<class CharT, class Traits, class Alloc> int std::basic_string<CharT, Traits, Alloc>::compare     (const std::basic_string& s) const noexcept {     size_type lhs_sz = size();     size_type rhs_sz = s.size();     int result = traits_type::compare(data(), s.data(), std::min(lhs_sz, rhs_sz));     if (result != 0)         return result;     if (lhs_sz < rhs_sz)         return -1;     if (lhs_sz > rhs_sz)         return 1;     return 0; } ``` |

### Notes

For the situations when three-way comparison is not required, std::basic_string provides the usual relational operators (`<`, `<=`, `==`, `>`, etc).

By default (with the default std::char_traits), this function is not locale-sensitive. See std::collate::compare for locale-aware three-way string comparison.

### Example

Run this code

```
#include <cassert>
#include <iomanip>
#include <iostream>
#include <string>
#include <string_view>
 
void print_compare_result(std::string_view str1,
                          std::string_view str2,
                          int compare_result)
{
    if (compare_result < 0)
        std::cout << std::quoted(str1) << " comes before "
                  << std::quoted(str2) << ".\n";
    else if (compare_result > 0)
        std::cout << std::quoted(str2) << " comes before "
                  << std::quoted(str1) << ".\n";
    else
        std::cout << std::quoted(str1) << " and "
                  << std::quoted(str2) << " are the same.\n";
}
 
int main()
{
    std::string batman{"Batman"};
    std::string superman{"Superman"};
    int compare_result{0};
 
    // 1) Compare with other string
    compare_result = batman.compare(superman);
    std::cout << "1) ";
    print_compare_result("Batman", "Superman", compare_result);
 
    // 2) Compare substring with other string
    compare_result = batman.compare(3, 3, superman);
    std::cout << "2) ";
    print_compare_result("man", "Superman", compare_result);
 
    // 3) Compare substring with other substring
    compare_result = batman.compare(3, 3, superman, 5, 3);
    std::cout << "3) ";
    print_compare_result("man", "man", compare_result);
 
    // Compare substring with other substring
    // defaulting to end of other string
    assert(compare_result == batman.compare(3, 3, superman, 5));
 
    // 4) Compare with char pointer
    compare_result = batman.compare("Superman");
    std::cout << "4) ";
    print_compare_result("Batman", "Superman", compare_result);
 
    // 5) Compare substring with char pointer
    compare_result = batman.compare(3, 3, "Superman");
    std::cout << "5) ";
    print_compare_result("man", "Superman", compare_result);
 
    // 6) Compare substring with char pointer substring
    compare_result = batman.compare(0, 3, "Superman", 5);
    std::cout << "6) ";
    print_compare_result("Bat", "Super", compare_result);
}

```

Output:

```
1) "Batman" comes before "Superman".
2) "Superman" comes before "man".
3) "man" and "man" are the same.
4) "Batman" comes before "Superman".
5) "Superman" comes before "man".
6) "Bat" comes before "Super".

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 5 | C++98 | the parameter count2 of overload (6) had a default argument npos | default argument removed, split to overloads (5) and (6) |
| LWG 847 | C++98 | there was no exception safety guarantee | added strong exception safety guarantee |
| LWG 2946 | C++17 | overload (7) caused ambiguity in some cases | avoided by making it a template |
| P1148R0 | C++17 | noexcept for overload (7) was accidentally dropped by the resolution of LWG2946 | restored |

### See also

|  |  |
| --- | --- |
| operator==operator!=operator<operator>operator<=operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares two strings   (function template) |
| substr | returns a substring   (public member function) |
| collate | defines lexicographical comparison and hashing of strings   (class template) |
| strcoll | compares two strings in accordance to the current locale   (function) |
| lexicographical_compare | returns true if one range is lexicographically less than another   (function template) |
| compare | compares two views   (public member function of `std::basic_string_view<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string/compare&oldid=172152>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 May 2024, at 10:02.