# std::char_traits

From cppreference.com
< cpp‎ | string
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
| ****char_traits**** | | | | |

****std::char_traits****

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
| char_traits::to_char_type | | | | |
| char_traits::to_int_type | | | | |
| char_traits::eq_int_type | | | | |
| char_traits::eof | | | | |
| char_traits::not_eof | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<string>` |  |  |
| template<  class CharT > class char_traits; |  |  |
|  |  |  |

The `char_traits` class is a traits class template that abstracts basic character and string operations for a given character type. The defined operation set is such that generic algorithms almost always can be implemented in terms of it. It is thus possible to use such algorithms with almost any possible character or string type, just by supplying a customized `char_traits` class.

The `char_traits` class template serves as a basis for explicit instantiations. The user can provide a specialization for any custom character types. Several explicit specializations are provided for the standard character types (see below), other specializations are not required to satisfy the requirements of CharTraits.

### Specializations

The standard library provides the following standard specializations:

|  |  |
| --- | --- |
| Defined in header `<string>` | |
| std::char_traits<char> | the standard character traits of char |
| std::char_traits<wchar_t> | the standard character traits of wchar_t |
| std::char_traits<char8_t> (C++20) | the standard character traits of char8_t |
| std::char_traits<char16_t> (C++11) | the standard character traits of char16_t |
| std::char_traits<char32_t> (C++11) | the standard character traits of char32_t |

All these specializations satisfy the requirements of CharTraits.

#### Member types

The standard specializations define the following member types required by CharTraits:

| `CharT` | Member type | | | | |
| --- | --- | --- | --- | --- | --- |
| `char_type` | `int_type` | `off_type` | `pos_type` | `state_type` |
| char | char | int | std::streamoff | std::streampos | std::mbstate_t |
| wchar_t | wchar_t | std::wint_t | std::wstreampos |
| char8_t | char8_t | unsigned int | std::u8streampos |
| char16_t | char16_t | std::uint_least16_t | std::u16streampos |
| char32_t | char32_t | std::uint_least32_t | std::u32streampos |

|  |  |
| --- | --- |
| On top of that, the standard specializations also define the member type `comparison_category` as std::strong_ordering. | (since C++20) |

#### Member functions

The standard specializations define the following static member functions required by CharTraits:

|  |  |
| --- | --- |
| assign[static] | assigns a character   (public static member function) |
| eqlt[static] | compares two characters   (public static member function) |
| move[static] | moves one character sequence onto another   (public static member function) |
| copy[static] | copies a character sequence   (public static member function) |
| compare[static] | lexicographically compares two character sequences   (public static member function) |
| length[static] | returns the length of a character sequence   (public static member function) |
| find[static] | finds a character in a character sequence   (public static member function) |
| to_char_type[static] | converts `int_type` to equivalent `char_type`   (public static member function) |
| to_int_type[static] | converts `char_type` to equivalent `int_type`   (public static member function) |
| eq_int_type[static] | compares two `int_type` values   (public static member function) |
| eof[static] | returns an **eof** value   (public static member function) |
| not_eof[static] | checks whether a character is **eof** value   (public static member function) |

### Notes

CharTraits does not require defining the types and functions listed above as direct members, it only requires types like `X::type` and expressions like X::func(args) are valid and have the required semantics. Users-defined character traits can be derived from other character traits classes and only override some of their members, see the example below.

### Example

User-defined character traits may be used to provide case-insensitive comparison:

Run this code

```
#include <cctype>
#include <iostream>
#include <string>
#include <string_view>
 
struct ci_char_traits : public std::char_traits<char>
{
    static char to_upper(char ch)
    {
        return std::toupper((unsigned char) ch);
    }
 
    static bool eq(char c1, char c2)
    {
        return to_upper(c1) == to_upper(c2);
    }
 
    static bool lt(char c1, char c2)
    {
         return to_upper(c1) < to_upper(c2);
    }
 
    static int compare(const char* s1, const char* s2, std::size_t n)
    {
        while (n-- != 0)
        {
            if (to_upper(*s1) < to_upper(*s2))
                return -1;
            if (to_upper(*s1) > to_upper(*s2))
                return 1;
            ++s1;
            ++s2;
        }
        return 0;
    }
 
    static const char* find(const char* s, std::size_t n, char a)
    {
        const auto ua{to_upper(a)};
        while (n-- != 0) 
        {
            if (to_upper(*s) == ua)
                return s;
            s++;
        }
        return nullptr;
    }
};
 
template<class DstTraits, class CharT, class SrcTraits>
constexpr std::basic_string_view<CharT, DstTraits>
    traits_cast(const std::basic_string_view<CharT, SrcTraits> src) noexcept
{
    return {src.data(), src.size()};
}
 
int main()
{
    using namespace std::literals;
 
    constexpr auto s1 = "Hello"sv;
    constexpr auto s2 = "heLLo"sv;
 
    if (traits_cast<ci_char_traits>(s1) == traits_cast<ci_char_traits>(s2))
        std::cout << s1 << " and " << s2 << " are equal\n";
}

```

Output:

```
Hello and heLLo are equal

```

### See also

|  |  |
| --- | --- |
| basic_string | stores and manipulates sequences of characters   (class template) |
| basic_string_view(C++17) | read-only string view   (class template) |
| basic_istream | wraps a given abstract device (std::basic_streambuf) and provides high-level input interface   (class template) |
| basic_ostream | wraps a given abstract device (std::basic_streambuf) and provides high-level output interface   (class template) |
| basic_streambuf | abstracts a raw device   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/char_traits&oldid=158926>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 September 2023, at 15:24.