# std::numeric_limits<T>::digits10

From cppreference.com
< cpp‎ | types‎ | numeric limits
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

Type support

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Basic types | | | | |
| Fixed width integer types (C++11) | | | | |
| Fixed width floating-point types (C++23) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ptrdiff_t | | | | | | size_t | | | | | | max_align_t(C++11) | | | | | | byte(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | nullptr_t(C++11) | | | | | | offsetof | | | | | | NULL | | | | | |  | | | | | |
| Numeric limits | | | | |
| numeric_limits | | | | |
| C numeric limits interface | | | | |
| Runtime type information | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | type_info | | | | | | type_index(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bad_typeid | | | | | | bad_cast | | | | | |

std::numeric_limits

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Static constants | | | | |
| numeric_limits::is_specialized | | | | |
| numeric_limits::is_signed | | | | |
| numeric_limits::is_integer | | | | |
| numeric_limits::is_exact | | | | |
| numeric_limits::has_infinity | | | | |
| numeric_limits::has_quiet_NaN | | | | |
| numeric_limits::has_signaling_NaN | | | | |
| numeric_limits::has_denorm | | | | |
| numeric_limits::has_denorm_loss | | | | |
| numeric_limits::round_style | | | | |
| numeric_limits::is_iec559 | | | | |
| numeric_limits::is_bounded | | | | |
| numeric_limits::is_modulo | | | | |
| numeric_limits::digits | | | | |
| ****numeric_limits::digits10**** | | | | |
| numeric_limits::max_digits10(C++11) | | | | |
| numeric_limits::radix | | | | |
| numeric_limits::min_exponent | | | | |
| numeric_limits::min_exponent10 | | | | |
| numeric_limits::max_exponent | | | | |
| numeric_limits::max_exponent10 | | | | |
| numeric_limits::traps | | | | |
| numeric_limits::tinyness_before | | | | |
| Static member functions | | | | |
| numeric_limits::min | | | | |
| numeric_limits::lowest(C++11) | | | | |
| numeric_limits::max | | | | |
| numeric_limits::epsilon | | | | |
| numeric_limits::round_error | | | | |
| numeric_limits::infinity | | | | |
| numeric_limits::quiet_NaN | | | | |
| numeric_limits::signaling_NaN | | | | |
| numeric_limits::denorm_min | | | | |
| Helper types | | | | |
| float_round_style | | | | |
| float_denorm_style | | | | |

|  |  |  |
| --- | --- | --- |
| static const int digits10; |  | (until C++11) |
| static constexpr int digits10; |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

The value of std::numeric_limits<T>::digits10 is the number of base-10 digits that can be represented by the type `T` without change, that is, any number with this many significant decimal digits can be converted to a value of type `T` and back to decimal form, without change due to rounding or overflow. For base-radix types, it is the value of `digits()` (digits - 1 for floating-point types) multiplied by \(\small \log_{10}{radix}\)log10(radix) and rounded down.

### Standard specializations

|  |  |
| --- | --- |
| `T` | value of std::numeric_limits<T>::digits10 |
| /\* non-specialized \*/ | ​0​ |
| bool | ​0​ |
| char | std::numeric_limits<char>::digits \* std::log10(2) |
| signed char | std::numeric_limits<signed char>::digits \* std::log10(2) |
| unsigned char | std::numeric_limits<unsigned char>::digits \* std::log10(2) |
| wchar_t | std::numeric_limits<wchar_t>::digits \* std::log10(2) |
| char8_t (since C++20) | std::numeric_limits<char8_t>::digits \* std::log10(2) |
| char16_t (since C++11) | std::numeric_limits<char16_t>::digits \* std::log10(2) |
| char32_t (since C++11) | std::numeric_limits<char32_t>::digits \* std::log10(2) |
| short | std::numeric_limits<short>::digits \* std::log10(2) |
| unsigned short | std::numeric_limits<unsigned short>::digits \* std::log10(2) |
| int | std::numeric_limits<int>::digits \* std::log10(2) |
| unsigned int | std::numeric_limits<unsigned int>::digits \* std::log10(2) |
| long | std::numeric_limits<long>::digits \* std::log10(2) |
| unsigned long | std::numeric_limits<unsigned long>::digits \* std::log10(2) |
| long long (since C++11) | std::numeric_limits<long long>::digits \* std::log10(2) |
| unsigned long long (since C++11) | std::numeric_limits<unsigned long long>::digits \* std::log10(2) |
| float | FLT_DIG (6 for IEEE float) |
| double | DBL_DIG (15 for IEEE double) |
| long double | LDBL_DIG (18 for 80-bit Intel long double; 33 for IEEE quadruple) |

### Example

An 8-bit binary type can represent any two-digit decimal number exactly, but 3-digit decimal numbers 256..999 cannot be represented. The value of `digits10` for an 8-bit type is 2 (8 \* std::log10(2) is 2.41)

The standard 32-bit IEEE 754 floating-point type has a 24 bit fractional part (23 bits written, one implied), which may suggest that it can represent 7 digit decimals (24 \* std::log10(2) is 7.22), but relative rounding errors are non-uniform and some floating-point values with 7 decimal digits do not survive conversion to 32-bit float and back: the smallest positive example is 8.589973e9, which becomes 8.589974e9 after the roundtrip. These rounding errors cannot exceed one bit in the representation, and `digits10` is calculated as (24 - 1) \* std::log10(2), which is 6.92. Rounding down results in the value 6.

Likewise, the 16-digit string 9007199254740993 does not survive text->double->text roundtrip, becoming 9007199254740992: the 64-bit IEEE 754 type double guarantees this roundtrip only for 15 decimal digits.

### See also

|  |  |
| --- | --- |
| max_digits10[static] (C++11) | number of decimal digits necessary to differentiate all values of this type   (public static member constant) |
| radix[static] | the radix or integer base used by the representation of the given type   (public static member constant) |
| digits[static] | number of `radix` digits that can be represented without change   (public static member constant) |
| min_exponent[static] | one more than the smallest negative power of the radix that is a valid normalized floating-point value   (public static member constant) |
| max_exponent[static] | one more than the largest integer power of the radix that is a valid finite floating-point value   (public static member constant) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/types/numeric_limits/digits10&oldid=148390>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 February 2023, at 01:41.