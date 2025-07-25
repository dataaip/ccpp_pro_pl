# operator==,!=,<,<=,>,>=,<=>(std::basic_string_view)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string_view::basic_string_view | | | | | | basic_string_view::operator= | | | | | | Iterators | | | | | | basic_string_view::beginbasic_string_view::cbegin | | | | | | basic_string_view::endbasic_string_view::cend | | | | | | basic_string_view::rbeginbasic_string_view::crbegin | | | | | | basic_string_view::rendbasic_string_view::crend | | | | | | Capacity | | | | | | basic_string_view::sizebasic_string_view::length | | | | | | basic_string_view::max_size | | | | | | basic_string_view::empty | | | | | | Operations | | | | | | basic_string_view::copy | | | | | | basic_string_view::substr | | | | | | basic_string_view::compare | | | | | | basic_string_view::starts_with(C++20) | | | | | | basic_string_view::ends_with(C++20) | | | | | | basic_string_view::contains(C++23) | | | | | | basic_string_view::find | | | | | | basic_string_view::rfind | | | | | | basic_string_view::find_first_of | | | | | | basic_string_view::find_last_of | | | | | | basic_string_view::find_first_not_of | | | | | | basic_string_view::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | basic_string_view::at | | | | | | [basic_string_view::operator[]](operator_at.html "cpp/string/basic string view/operator at") | | | | | | basic_string_view::front | | | | | | basic_string_view::back | | | | | | basic_string_view::data | | | | | | Modifiers | | | | | | basic_string_view::remove_prefix | | | | | | basic_string_view::remove_suffix | | | | | | basic_string_view::swap | | | | | | Constants | | | | | | basic_string_view::npos | | | | | | Non-member functions | | | | | | ****operator==operator!=operator<operator>operator<=operator>=operator<=>****(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | operator<< | | | | | | operator""sv | | | | | | Helper classes | | | | | | hash<std::string_view>hash<std::wstring_view>hash<std::u8string_view>hash<std::u16string_view>hash<std::u32string_view>(C++20) | | | | | | Deduction guides (C++20) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<string_view>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| template< class CharT, class Traits >  constexpr bool operator==( std::basic_string_view<CharT,Traits> lhs, std::basic_string_view<CharT,Traits> rhs ) noexcept; |  | (since C++17)  (until C++20) |
| template< class CharT, class Traits >  constexpr bool operator==(      std::basic_string_view<CharT,Traits> lhs, std::type_identity_t<std::basic_string_view<CharT,Traits>> rhs ) noexcept; |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
| template< class CharT, class Traits >  constexpr bool operator!=( std::basic_string_view<CharT,Traits> lhs, std::basic_string_view<CharT,Traits> rhs ) noexcept; | (2) | (since C++17)  (until C++20) |
| template< class CharT, class Traits >  constexpr bool operator<( std::basic_string_view<CharT,Traits> lhs, std::basic_string_view<CharT,Traits> rhs ) noexcept; | (3) | (since C++17)  (until C++20) |
| template< class CharT, class Traits >  constexpr bool operator<=( std::basic_string_view<CharT,Traits> lhs, std::basic_string_view<CharT,Traits> rhs ) noexcept; | (4) | (since C++17)  (until C++20) |
| template< class CharT, class Traits >  constexpr bool operator>( std::basic_string_view<CharT,Traits> lhs, std::basic_string_view<CharT,Traits> rhs ) noexcept; | (5) | (since C++17)  (until C++20) |
| template< class CharT, class Traits >  constexpr bool operator>=( std::basic_string_view<CharT,Traits> lhs, std::basic_string_view<CharT,Traits> rhs ) noexcept; | (6) | (since C++17)  (until C++20) |
| template< class CharT, class Traits >  constexpr /\*comp-cat\*/ operator<=>(      std::basic_string_view<CharT,Traits> lhs, std::type_identity_t<std::basic_string_view<CharT,Traits>> rhs ) noexcept; | (7) | (since C++20) |
|  |  |  |

Compares two views.

All comparisons are done via the compare() member function (which itself is defined in terms of `Traits::compare()`):

- Two views are equal if both the size of lhs and rhs are equal and each character in lhs has an equivalent character in rhs at the same position.

- The ordering comparisons are done lexicographically – the comparison is performed by a function equivalent to std::lexicographical_compare.

|  |  |
| --- | --- |
| The implementation provides sufficient additional `constexpr` and `noexcept` overloads of these functions so that a `basic_string_view<CharT,Traits>` object `sv` may be compared to another object `t` with an implicit conversion to `basic_string_view<CharT,Traits>`, with semantics identical to comparing `sv` and `basic_string_view<CharT,Traits>(t)`. | (until C++20) |
| The return type of three-way comparison operators (/\*comp-cat\*/) is Traits::comparison_category if that qualified-id denotes a type, std::weak_ordering otherwise. If /\*comp-cat\*/ is not a comparison category type, the program is ill-formed.  The `<`, `<=`, `>`, `>=`, and `!=` operators are synthesized from operator<=> and operator== respectively. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | views to compare |

### Return value

1-6) true if the corresponding comparison holds, false otherwise.7) static_cast</\*comp-cat\*/>(lhs.compare(rhs) <=> 0).

### Complexity

Linear in the size of the views.

### Notes

|  |  |
| --- | --- |
| Sufficient additional overloads can be implemented through non-deduced context in one parameter type. | (until C++20) |
| Three-way comparison result type of std::string_view, std::wstring_view, std::u8string_view, std::u16string_view and std::u32string_view is std::strong_ordering.  std::type_identity_t is used for non-deduced context, which makes arguments that implicitly convertible to the string view type comparable with the string view. | (since C++20) |

### Example

Run this code

```
#include <string_view>
 
int main()
{
    using namespace std::literals;
 
    static_assert(""sv == ""sv);
 
    static_assert(""sv == "", "Selects an additional overload until C++20.");
 
    static_assert("" == ""sv, "Selects an additional overload until C++20."
                              "Uses a rewritten candidate since C++20.");
 
    static_assert(!(""sv != ""sv), "Uses the rewritten candidate since C++20.");
 
    static_assert(!(""sv != ""), "Selects an additional overload until C++20;"
                                 "Uses a rewritten candidate since C++20.");
 
    static_assert(!("" != ""sv), "Selects an additional overload until C++20."
                                 "Uses a rewritten candidate since C++20.");
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3432 | C++20 | the return type of `operator<=>` was not required to be a comparison category type | required |
| LWG 3950 | C++20 | redundant additional overloads were still required | overload sets reduced |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string_view/operator_cmp&oldid=171346>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 April 2024, at 14:11.