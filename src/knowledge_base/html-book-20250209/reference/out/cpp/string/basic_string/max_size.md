# std::basic_string<CharT,Traits,Allocator>::max_size

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string::basic_string | | | | | | basic_string::~basic_string | | | | | | basic_string::operator= | | | | | | basic_string::assign | | | | | | basic_string::assign_range(C++23) | | | | | | basic_string::get_allocator | | | | | | Element access | | | | | | basic_string::at | | | | | | [basic_string::operator[]](operator_at.html "cpp/string/basic string/operator at") | | | | | | basic_string::front(DR\*) | | | | | | basic_string::back(DR\*) | | | | | | basic_string::data | | | | | | basic_string::c_str | | | | | | basic_string::operator  basic_string_view(C++17) | | | | | | Iterators | | | | | | basic_string::beginbasic_string::cbegin(C++11) | | | | | | basic_string::endbasic_string::cend(C++11) | | | | | | basic_string::rbeginbasic_string::crbegin(C++11) | | | | | | basic_string::rendbasic_string::crend(C++11) | | | | | | Search | | | | | | basic_string::find | | | | | | basic_string::rfind | | | | | | basic_string::find_first_of | | | | | | basic_string::find_first_not_of | | | | | | basic_string::find_last_of | | | | | | basic_string::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | basic_string::clear | | | | | | basic_string::insert | | | | | | basic_string::insert_range(C++23) | | | | | | basic_string::erase | | | | | | basic_string::push_back | | | | | | basic_string::pop_back(DR\*) | | | | | | basic_string::append | | | | | | basic_string::append_range(C++23) | | | | | | basic_string::operator+= | | | | | | basic_string::replace | | | | | | basic_string::replace_with_range(C++23) | | | | | | basic_string::copy | | | | | | basic_string::resize | | | | | | basic_string::resize_and_overwrite(C++23) | | | | | | basic_string::swap | | | | | | Capacity | | | | | | basic_string::empty | | | | | | basic_string::sizebasic_string::length | | | | | | ****basic_string::max_size**** | | | | | | basic_string::reserve | | | | | | basic_string::capacity | | | | | | basic_string::shrink_to_fit(DR\*) | | | | | | Operations | | | | | | basic_string::compare | | | | | | basic_string::starts_with(C++20) | | | | | | basic_string::ends_with(C++20) | | | | | | basic_string::contains(C++23) | | | | | | basic_string::substr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constants | | | | | | basic_string::npos | | | | | | Non-member functions | | | | | | operator+ | | | | | | swap(std::basic_string) | | | | | | erase(std::basic_string)erase_if(std::basic_string)(C++20)(C++20) | | | | | | I/O | | | | | | operator<<operator>> | | | | | | getline | | | | | | Comparison | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | Numeric conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stoistolstoll(C++11)(C++11)(C++11) | | | | | | stoulstoull(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stofstodstold(C++11)(C++11)(C++11) | | | | | | to_string(C++11) | | | | | | to_wstring(C++11) | | | | | | | Literals | | | | | | operator""s(C++14) | | | | | | Helper classes | | | | | | hash<std::basic_string>(C++11) | | | | | | Deduction guides (C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| size_type max_size() const; |  | (noexcept since C++11)  (constexpr since C++20) |
|  |  |  |

Returns the maximum number of elements the string is able to hold due to system or library implementation limitations, i.e. std::distance(begin(), end()) for the largest string.

### Parameters

(none)

### Return value

Maximum number of characters.

### Complexity

Constant.

### Example

Run this code

```
#include <array>
#include <climits>
#include <iomanip>
#include <iostream>
#include <locale>
#include <string>
#include <typeinfo>
 
#include <boost/core/demangle.hpp>
 
template<typename T>
void print_basic_string_max_size()
{
    std::basic_string<T> s;
    auto max_size = s.max_size();
    std::cout.imbue(std::locale("en_US.UTF-8"));
    std::cout << "basic_string<" << boost::core::demangle(typeid(T).name())
              << ">:\n\t" << max_size << " = ";
    std::cout << std::setprecision(3) << (double) max_size << " = ";
    std::cout.imbue(std::locale("C"));
    std::cout << std::hex << std::setfill('0') << "0x"
              << std::setw(sizeof(typename decltype(s)::size_type) << 1)
              << max_size << '\n' << std::dec;
};
 
int main()
{
    std::cout << "Pointer size: " << CHAR_BIT * sizeof(void*) << " bits\n"
                 "Maximum sizes:\n";
 
    print_basic_string_max_size<char>();
    print_basic_string_max_size<char16_t>();
    print_basic_string_max_size<char32_t>();
    print_basic_string_max_size<wchar_t>();
    print_basic_string_max_size<long>();
 
    using CharT = std::array<char, 01232>;
    print_basic_string_max_size<CharT>();
}

```

Possible output:

```
Pointer size: 64 bits
Maximum sizes:
basic_string<char>:
        9,223,372,036,854,775,807 = 9.22e+18 = 0x7fffffffffffffff
basic_string<char16_t>:
        4,611,686,018,427,387,903 = 4.61e+18 = 0x3fffffffffffffff
basic_string<char32_t>:
        2,305,843,009,213,693,951 = 2.31e+18 = 0x1fffffffffffffff
basic_string<wchar_t>:
        2,305,843,009,213,693,951 = 2.31e+18 = 0x1fffffffffffffff
basic_string<long>:
        1,152,921,504,606,846,975 = 1.15e+18 = 0x0fffffffffffffff
basic_string<std::array<char, 666ul>>:
        13,848,906,962,244,407 = 1.38e+16 = 0x00313381ec031337

```

### See also

|  |  |
| --- | --- |
| sizelength | returns the number of characters   (public member function) |
| sizelength | returns the number of characters   (public member function of `std::basic_string_view<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string/max_size&oldid=177138>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 October 2024, at 13:44.