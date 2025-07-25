# std::bitset<N>::bitset

From cppreference.com
< cpp‎ | utility‎ | bitset
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

Utilities library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

std::bitset

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| bitset::reference | | | | |
| Member functions | | | | |
| ****bitset::bitset**** | | | | |
| bitset::operator==bitset::operator!=(until C++20) | | | | |
| Element access | | | | |
| [bitset::operator[]](operator_at.html "cpp/utility/bitset/operator at") | | | | |
| bitset::test | | | | |
| bitset::allbitset::anybitset::none(C++11) | | | | |
| bitset::count | | | | |
| Capacity | | | | |
| bitset::size | | | | |
| Modifiers | | | | |
| bitset::operator&=bitset::operator|=bitset::operator^=bitset::operator~ | | | | |
| bitset::operator<<=bitset::operator>>=bitset::operator<<bitset::operator>> | | | | |
| bitset::set | | | | |
| bitset::reset | | | | |
| bitset::flip | | | | |
| Conversions | | | | |
| bitset::to_string | | | | |
| bitset::to_ulong | | | | |
| bitset::to_ullong(C++11) | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator&operator|operator^ | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator<<operator>> | | | | | |  | | | | | |
| Helper classes | | | | |
| std::hash(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| bitset(); | (1) | (noexcept since C++11)  (constexpr since C++11) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| bitset( unsigned long val ); |  | (until C++11) |
| constexpr bitset( unsigned long long val ) noexcept; |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| template< class CharT, class Traits, class Alloc >  explicit bitset      ( const std::basic_string<CharT, Traits, Alloc>& str,        typename std::basic_string                     <CharT, Traits, Alloc>::size_type pos = 0,        typename std::basic_string<CharT, Traits, Alloc>::size_type            n = std::basic_string<CharT, Traits, Alloc>::npos,       CharT zero = CharT('0'), CharT one = CharT('1') ); | (3) | (constexpr since C++23) |
| template< class CharT, class Traits >  constexpr explicit bitset      ( std::basic_string_view<CharT, Traits> str,        std::size_t pos = 0, std::size_t n = std::size_t(-1),       CharT zero = CharT('0'), CharT one = CharT('1') ); | (4) | (since C++26) |
| template< class CharT >  explicit bitset( const CharT\* str, std::size_t n = std::size_t(-1),                  CharT zero = CharT('0'), CharT one = CharT('1') ); | (5) | (since C++11)  (constexpr since C++23) |
|  |  |  |

Constructs a new bitset from one of several optional data sources:

1) Default constructor. Constructs a bitset with all bits set to zero.2) Constructs a bitset from an unsigned integer val. Given the number of bits in the value representation of unsigned long(until C++11)unsigned long long(since C++11) as S:

- The first (rightmost, least significant) std::min(S, N) bit positions are initialized with the corresponding bit values of val.
- If S is less than N, the remaining bit positions are initialized to zeroes.
3) Constructs a bitset using the characters in str. An optional starting position pos and length n can be provided, as well as characters denoting alternate values for set (one) and unset (zero) bits. `Traits::eq()` is used to compare the character values. The effective length of the initializing string is std::min(n, str.size() - pos).4) Similar to (3), but uses a std::basic_string_view instead of a std::basic_string.5) Similar to (3), but uses a const CharT\* instead of a std::basic_string.

|  |  |
| --- | --- |
| Equivalent to bitset(n == std::basic_string<CharT>::npos           ? std::basic_string<CharT>(str)           : std::basic_string<CharT>(str, n), 0, n, zero, one). | (until C++26) |
| Equivalent to bitset(n == std::basic_string_view<CharT>::npos           ? std::basic_string_view<CharT>(str)           : std::basic_string_view<CharT>(str, n), 0, n, zero, one). | (since C++26) |

### Parameters

|  |  |  |
| --- | --- | --- |
| val | - | number used to initialize the bitset |
| str | - | string used to initialize the bitset |
| pos | - | a starting offset into str |
| n | - | number of characters to use from str |
| zero | - | alternate character for unset bits in str |
| one | - | alternate character for set bits in str |

### Exceptions

3,4) std::out_of_range if pos > str.size(), std::invalid_argument if any character is not one or zero.5) std::invalid_argument if any character is not one or zero.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_constexpr_bitset` | `202207L` | (C++23) | A more constexpr `std::bitset`, overloads (3,5) |
| `__cpp_lib_bitset` | `202306L` | (C++26) | Interfacing `std::bitset` with std::string_view, (4) |

### Example

Run this code

```
#include <bitset>
#include <climits>
#include <iostream>
#include <string>
 
int main()
{
    // empty constructor (1)
    std::bitset<8> b1; // [0,0,0,0,0,0,0,0]
 
    // unsigned long long constructor (2)
    std::bitset<8> b2(42);          // [0,0,1,0,1,0,1,0]
    std::bitset<70> bl(ULLONG_MAX); // [0,0,0,0,0,0,1,1,1,...,1,1,1] in C++11
    std::bitset<8> bs(0xfff0);      // [1,1,1,1,0,0,0,0]
 
    // string constructor (3)
    std::string bit_string = "110010";
    std::bitset<8> b3(bit_string);       // [0,0,1,1,0,0,1,0]
    std::bitset<8> b4(bit_string, 2);    // [0,0,0,0,0,0,1,0]
    std::bitset<8> b5(bit_string, 2, 3); // [0,0,0,0,0,0,0,1]
 
    // string constructor using custom zero/one digits (3)
    std::string alpha_bit_string = "aBaaBBaB";
    std::bitset<8> b6(alpha_bit_string, 0, alpha_bit_string.size(),
                      'a', 'B');         // [0,1,0,0,1,1,0,1]
 
    // char* constructor using custom digits (5)
    std::bitset<8> b7("XXXXYYYY", 8, 'X', 'Y'); // [0,0,0,0,1,1,1,1]
 
    std::cout <<   "b1: " << b1 << "\nb2: " << b2 << "\nbl: " << bl
              << "\nbs: " << bs << "\nb3: " << b3 << "\nb4: " << b4
              << "\nb5: " << b5 << "\nb6: " << b6 << "\nb7: " << b7 << '\n';
}

```

Possible output:

```
b1: 00000000
b2: 00101010
bl: 0000001111111111111111111111111111111111111111111111111111111111111111
bs: 11110000
b3: 00110010
b4: 00000010
b5: 00000001
b6: 01001101
b7: 00001111

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 396 | C++98 | the values of the zero and one characters for overload (3) were ​0​ and 1 (which do not correspond to '0' and '1') | added parameters to provide values for these characters |
| LWG 457 | C++98 | S was CHAR_BIT \* sizeof(unsigned long) for overload (2), but unsigned long is not guaranteed to use all its bits to represent its value | consider the number of bits of the value representation instead |
| LWG 2250 | C++98 | the behavior was undefined if pos > str.size() is true | always throws an exception in this case |

### See also

|  |  |
| --- | --- |
| set | sets bits to true or given value   (public member function) |
| reset | sets bits to false   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/bitset/bitset&oldid=178330>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 December 2024, at 06:13.