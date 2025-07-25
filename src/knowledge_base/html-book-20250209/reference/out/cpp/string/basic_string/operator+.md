# std::operator+(std::basic_string)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string::basic_string | | | | | | basic_string::~basic_string | | | | | | basic_string::operator= | | | | | | basic_string::assign | | | | | | basic_string::assign_range(C++23) | | | | | | basic_string::get_allocator | | | | | | Element access | | | | | | basic_string::at | | | | | | [basic_string::operator[]](operator_at.html "cpp/string/basic string/operator at") | | | | | | basic_string::front(DR\*) | | | | | | basic_string::back(DR\*) | | | | | | basic_string::data | | | | | | basic_string::c_str | | | | | | basic_string::operator  basic_string_view(C++17) | | | | | | Iterators | | | | | | basic_string::beginbasic_string::cbegin(C++11) | | | | | | basic_string::endbasic_string::cend(C++11) | | | | | | basic_string::rbeginbasic_string::crbegin(C++11) | | | | | | basic_string::rendbasic_string::crend(C++11) | | | | | | Search | | | | | | basic_string::find | | | | | | basic_string::rfind | | | | | | basic_string::find_first_of | | | | | | basic_string::find_first_not_of | | | | | | basic_string::find_last_of | | | | | | basic_string::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | basic_string::clear | | | | | | basic_string::insert | | | | | | basic_string::insert_range(C++23) | | | | | | basic_string::erase | | | | | | basic_string::push_back | | | | | | basic_string::pop_back(DR\*) | | | | | | basic_string::append | | | | | | basic_string::append_range(C++23) | | | | | | basic_string::operator+= | | | | | | basic_string::replace | | | | | | basic_string::replace_with_range(C++23) | | | | | | basic_string::copy | | | | | | basic_string::resize | | | | | | basic_string::resize_and_overwrite(C++23) | | | | | | basic_string::swap | | | | | | Capacity | | | | | | basic_string::empty | | | | | | basic_string::sizebasic_string::length | | | | | | basic_string::max_size | | | | | | basic_string::reserve | | | | | | basic_string::capacity | | | | | | basic_string::shrink_to_fit(DR\*) | | | | | | Operations | | | | | | basic_string::compare | | | | | | basic_string::starts_with(C++20) | | | | | | basic_string::ends_with(C++20) | | | | | | basic_string::contains(C++23) | | | | | | basic_string::substr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constants | | | | | | basic_string::npos | | | | | | Non-member functions | | | | | | ****operator+**** | | | | | | swap(std::basic_string) | | | | | | erase(std::basic_string)erase_if(std::basic_string)(C++20)(C++20) | | | | | | I/O | | | | | | operator<<operator>> | | | | | | getline | | | | | | Comparison | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | Numeric conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stoistolstoll(C++11)(C++11)(C++11) | | | | | | stoulstoull(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stofstodstold(C++11)(C++11)(C++11) | | | | | | to_string(C++11) | | | | | | to_wstring(C++11) | | | | | | | Literals | | | | | | operator""s(C++14) | | | | | | Helper classes | | | | | | hash<std::basic_string>(C++11) | | | | | | Deduction guides (C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<string>` |  |  |
| template< class CharT, class Traits, class Alloc >  std::basic_string<CharT,Traits,Alloc>      operator+( const std::basic_string<CharT,Traits,Alloc>& lhs, const std::basic_string<CharT,Traits,Alloc>& rhs ); | (1) | (constexpr since C++20) |
| template< class CharT, class Traits, class Alloc >  std::basic_string<CharT,Traits,Alloc>      operator+( const std::basic_string<CharT,Traits,Alloc>& lhs, const CharT\* rhs ); | (2) | (constexpr since C++20) |
| template< class CharT, class Traits, class Alloc >  std::basic_string<CharT,Traits,Alloc>      operator+( const std::basic_string<CharT,Traits,Alloc>& lhs,                CharT rhs ); | (3) | (constexpr since C++20) |
| template< class CharT, class Traits, class Alloc >  constexpr std::basic_string<CharT,Traits,Alloc>      operator+( const std::basic_string<CharT,Traits,Alloc>& lhs, std::type_identity_t<std::basic_string_view<CharT,Traits>> rhs ); | (4) | (since C++26) |
| template< class CharT, class Traits, class Alloc >  std::basic_string<CharT,Traits,Alloc>      operator+( const CharT\* lhs, const std::basic_string<CharT,Traits,Alloc>& rhs ); | (5) | (constexpr since C++20) |
| template< class CharT, class Traits, class Alloc >  std::basic_string<CharT,Traits,Alloc>      operator+( CharT lhs, const std::basic_string<CharT,Traits,Alloc>& rhs ); | (6) | (constexpr since C++20) |
| template< class CharT, class Traits, class Alloc >  constexpr std::basic_string<CharT,Traits,Alloc>      operator+( std::type_identity_t<std::basic_string_view<CharT,Traits>> lhs, const std::basic_string<CharT,Traits,Alloc>& rhs ); | (7) | (since C++26) |
| template< class CharT, class Traits, class Alloc >  std::basic_string<CharT,Traits,Alloc>      operator+( std::basic_string<CharT,Traits,Alloc>&& lhs, std::basic_string<CharT,Traits,Alloc>&& rhs ); | (8) | (since C++11)  (constexpr since C++20) |
| template< class CharT, class Traits, class Alloc >  std::basic_string<CharT,Traits,Alloc>      operator+( std::basic_string<CharT,Traits,Alloc>&& lhs, const std::basic_string<CharT,Traits,Alloc>& rhs ); | (9) | (since C++11)  (constexpr since C++20) |
| template< class CharT, class Traits, class Alloc >  std::basic_string<CharT,Traits,Alloc>      operator+( std::basic_string<CharT,Traits,Alloc>&& lhs, const CharT\* rhs ); | (10) | (since C++11)  (constexpr since C++20) |
| template< class CharT, class Traits, class Alloc >  std::basic_string<CharT,Traits,Alloc>      operator+( std::basic_string<CharT,Traits,Alloc>&& lhs,                CharT rhs ); | (11) | (since C++11)  (constexpr since C++20) |
| template< class CharT, class Traits, class Alloc >  constexpr std::basic_string<CharT,Traits,Alloc>      operator+( std::basic_string<CharT,Traits,Alloc>&& lhs, std::type_identity_t<std::basic_string_view<CharT,Traits>> rhs ); | (12) | (since C++26) |
| template< class CharT, class Traits, class Alloc >  std::basic_string<CharT,Traits,Alloc>      operator+( const std::basic_string<CharT,Traits,Alloc>& lhs, std::basic_string<CharT,Traits,Alloc>&& rhs ); | (13) | (since C++11)  (constexpr since C++20) |
| template< class CharT, class Traits, class Alloc >  std::basic_string<CharT,Traits,Alloc>      operator+( const CharT\* lhs, std::basic_string<CharT,Traits,Alloc>&& rhs ); | (14) | (since C++11)  (constexpr since C++20) |
| template< class CharT, class Traits, class Alloc >  std::basic_string<CharT,Traits,Alloc>      operator+( CharT lhs, std::basic_string<CharT,Traits,Alloc>&& rhs ); | (15) | (since C++11)  (constexpr since C++20) |
| template< class CharT, class Traits, class Alloc >  constexpr std::basic_string<CharT,Traits,Alloc>      operator+( std::type_identity_t<std::basic_string_view<CharT,Traits>> lhs, std::basic_string<CharT,Traits,Alloc>&& rhs ); | (16) | (since C++26) |
|  |  |  |

Returns a string containing characters from lhs followed by the characters from rhs. Equivalent to:

1,2) std::basic_string<CharT, Traits, Allocator> r = lhs; r.append(rhs); return r;3) std::basic_string<CharT, Traits, Allocator> r = lhs; r.push_back(rhs); return r;4) std::basic_string<CharT, Traits, Allocator> r = lhs; r.append(rhs); return r;5) std::basic_string<CharT, Traits, Allocator> r = rhs; r.insert(0, lhs); return r;6) std::basic_string<CharT, Traits, Allocator> r = rhs; r.insert(r.begin(), lhs); return r;7) std::basic_string<CharT, Traits, Allocator> r = rhs; r.insert(0, lhs); return r;8) lhs.append(rhs); return std::move(lhs); except that both lhs and rhs are left in valid but unspecified states. If lhs and rhs have equal allocators, the implementation can move from either.9,10) lhs.append(rhs); return std::move(lhs);11) lhs.push_back(rhs); return std::move(lhs);12) lhs.append(rhs); return std::move(lhs);13,14) rhs.insert(0, lhs); return std::move(rhs);15) rhs.insert(rhs.begin(), lhs); return std::move(rhs);16) rhs.insert(0, lhs); return std::move(rhs);

|  |  |
| --- | --- |
| The allocator used for the result is: 1-4) std::allocator_traits<Alloc>::select_on_container_copy_construction(lhs.get_allocator())5-7) std::allocator_traits<Alloc>::select_on_container_copy_construction(rhs.get_allocator())8-12) lhs.get_allocator()13-16) rhs.get_allocator() In other words:   - If one operand is a `basic_string` rvalue, its allocator is used. - Otherwise, `select_on_container_copy_construction` is used on the allocator of the lvalue `basic_string` operand.   In each case, the left operand is preferred when both are `basic_string`s of the same value category.  For (8-16), all rvalue `basic_string` operands are left in valid but unspecified states. | (since C++11) |

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs | - | string, string view(since C++26), character, or pointer to the first character in a null-terminated array |
| rhs | - | string, string view(since C++26), character, or pointer to the first character in a null-terminated array |

### Return value

A string containing characters from lhs followed by the characters from rhs, using the allocator determined as above(since C++11).

|  |  |
| --- | --- |
| Notes `operator+` should be used with great caution when stateful allocators are involved (such as when std::pmr::string is used)(since C++17). Prior to P1165R1, the allocator used for the result was determined by historical accident and can vary from overload to overload for no apparent reason. Moreover, for (1-5), the allocator propagation behavior varies across major standard library implementations and differs from the behavior depicted in the standard.  Because the allocator used by the result of `operator+` is sensitive to value category, `operator+` is not associative with respect to allocator propagation:   ```text using my_string = std::basic_string<char, std::char_traits<char>, my_allocator<char>>; my_string cat(); const my_string& dog();   my_string meow = /* ... */, woof = /* ... */; meow + cat() + /* ... */; // uses select_on_container_copy_construction on meow's allocator woof + dog() + /* ... */; // uses allocator of dog()'s return value instead   meow + woof + meow; // uses select_on_container_copy_construction on meow's allocator meow + (woof + meow); // uses SOCCC on woof's allocator instead ```   For a chain of `operator+` invocations, the allocator used for the ultimate result may be controlled by prepending an rvalue `basic_string` with the desired allocator:   ```text // use my_favorite_allocator for the final result my_string(my_favorite_allocator) + meow + woof + cat() + dog(); ```   For better and portable control over allocators, member functions like `append`, `insert`, and `operator+=` should be used on a result string constructed with the desired allocator. | (since C++11) |

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| The usage of std::type_identity_t as parameter in overloads (4), (7), (12), and (16) ensures that an object of type std::basic_string<CharT, Traits, Allocator> can always be concatenated to an object of a type `T` with an implicit conversion to std::basic_string_view<CharT, Traits>, and vice versa, as per overload resolution rules.   | Feature-test macro | Value | Std | Feature | | --- | --- | --- | --- | | `__cpp_lib_string_view` | `202403` | (C++26) | Concatenation of strings and string views, overloads (4), (7), (12), (16) | | (since C++26) |

### Example

Run this code

```
#include <iostream>
#include <string>
#include <string_view>
 
int main()
{
    std::string s1 = "Hello";
    std::string s2 = "world";
    const char* end = "!\n";
    std::cout << s1 + ' ' + s2 + end;
 
    std::string_view water{" Water"};
    #if __cpp_lib_string_view >= 202403
    std::cout << s1 + water + s2 << end; // overload (4), then (1)
    #else
    std::cout << s1 + std::string(water) + s2 << end; // OK, but less efficient
    #endif
}

```

Output:

```
Hello world!
Hello Waterworld!

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P1165R1 | C++11 | allocator propagation is haphazard and inconsistent | made more consistent |

### See also

|  |  |
| --- | --- |
| operator+= | appends characters to the end   (public member function) |
| append | appends characters to the end   (public member function) |
| insert | inserts characters   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string/operator%2B&oldid=171693>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 May 2024, at 16:26.