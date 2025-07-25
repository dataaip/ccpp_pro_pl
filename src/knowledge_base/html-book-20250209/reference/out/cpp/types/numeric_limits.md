# std::numeric_limits

From cppreference.com
< cpp‎ | types
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
| ****numeric_limits**** | | | | |
| C numeric limits interface | | | | |
| Runtime type information | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | type_info | | | | | | type_index(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bad_typeid | | | | | | bad_cast | | | | | |

****std::numeric_limits****

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
| numeric_limits::digits10 | | | | |
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
| Defined in header `<limits>` |  |  |
| template< class T > class numeric_limits; |  |  |
|  |  |  |

The `std::numeric_limits` class template provides a standardized way to query various properties of arithmetic types (e.g. the largest possible value for type int is std::numeric_limits<int>::max()).

This information is provided via specializations of the `std::numeric_limits` template. The standard library makes available specializations for all arithmetic types (only lists the specializations for cv-unqualified arithmetic types):

|  |  |  |
| --- | --- | --- |
| Defined in header `<limits>` |  |  |
| template<> class numeric_limits<bool>; |  |  |
| template<> class numeric_limits<char>; |  |  |
| template<> class numeric_limits<signed char>; |  |  |
| template<> class numeric_limits<unsigned char>; |  |  |
| template<> class numeric_limits<wchar_t>; |  |  |
| template<> class numeric_limits<char8_t>; |  | (since C++20) |
| template<> class numeric_limits<char16_t>; |  | (since C++11) |
| template<> class numeric_limits<char32_t>; |  | (since C++11) |
| template<> class numeric_limits<short>; |  |  |
| template<> class numeric_limits<unsigned short>; |  |  |
| template<> class numeric_limits<int>; |  |  |
| template<> class numeric_limits<unsigned int>; |  |  |
| template<> class numeric_limits<long>; |  |  |
| template<> class numeric_limits<unsigned long>; |  |  |
| template<> class numeric_limits<long long>; |  | (since C++11) |
| template<> class numeric_limits<unsigned long long>; |  | (since C++11) |
| template<> class numeric_limits<float>; |  |  |
| template<> class numeric_limits<double>; |  |  |
| template<> class numeric_limits<long double>; |  |  |
|  |  |  |

The value of each member of a specialization of `std::numeric_limits` on a cv-qualified type **cv** `T` is equal to the value of the corresponding member of the specialization on the unqualified type `T`. For example, std::numeric_limits<int>::digits is equal to std::numeric_limits<const int>::digits.

Aliases of arithmetic types (such as std::size_t or std::streamsize) may also be examined with the `std::numeric_limits` type traits.

Non-arithmetic standard types, such as std::complex<T> or std::nullptr_t, do not have specializations.

|  |  |
| --- | --- |
| If the implementation defines any integer-class types, specializations of `std::numeric_limits` must also be provided for them. | (since C++20) |

Implementations may provide specializations of `std::numeric_limits` for implementation-specific types: e.g. GCC provides `std::numeric_limits<__int128>`. Non-standard libraries may add specializations for library-provided types, e.g. OpenEXR provides `std::numeric_limits<half>` for a 16-bit floating-point type.

### Template parameters

|  |  |  |
| --- | --- | --- |
| T | - | a type to retrieve numeric properties for |

### Member constants

|  |  |
| --- | --- |
| is_specialized[static] | identifies types for which ****std::numeric_limits**** is specialized   (public static member constant) |
| is_signed[static] | identifies signed types   (public static member constant) |
| is_integer[static] | identifies integer types   (public static member constant) |
| is_exact[static] | identifies exact types   (public static member constant) |
| has_infinity[static] | identifies floating-point types that can represent the special value "positive infinity"   (public static member constant) |
| has_quiet_NaN[static] | identifies floating-point types that can represent the special value "quiet not-a-number" (NaN)   (public static member constant) |
| has_signaling_NaN[static] | identifies floating-point types that can represent the special value "signaling not-a-number" (NaN)   (public static member constant) |
| has_denorm[static] | identifies the denormalization style used by the floating-point type   (public static member constant) |
| has_denorm_loss[static] | identifies the floating-point types that detect loss of precision as denormalization loss rather than inexact result   (public static member constant) |
| round_style[static] | identifies the rounding style used by the type   (public static member constant) |
| is_iec559[static] | identifies the IEC 559/IEEE 754 floating-point types   (public static member constant) |
| is_bounded[static] | identifies types that represent a finite set of values   (public static member constant) |
| is_modulo[static] | identifies types that handle overflows with modulo arithmetic   (public static member constant) |
| digits[static] | number of `radix` digits that can be represented without change   (public static member constant) |
| digits10[static] | number of decimal digits that can be represented without change   (public static member constant) |
| max_digits10[static] (C++11) | number of decimal digits necessary to differentiate all values of this type   (public static member constant) |
| radix[static] | the radix or integer base used by the representation of the given type   (public static member constant) |
| min_exponent[static] | one more than the smallest negative power of the radix that is a valid normalized floating-point value   (public static member constant) |
| min_exponent10[static] | the smallest negative power of ten that is a valid normalized floating-point value   (public static member constant) |
| max_exponent[static] | one more than the largest integer power of the radix that is a valid finite floating-point value   (public static member constant) |
| max_exponent10[static] | the largest integer power of 10 that is a valid finite floating-point value   (public static member constant) |
| traps[static] | identifies types which can cause arithmetic operations to trap   (public static member constant) |
| tinyness_before[static] | identifies floating-point types that detect tinyness before rounding   (public static member constant) |

### Member functions

|  |  |
| --- | --- |
| min[static] | returns the smallest finite value of the given non-floating-point type, or the smallest positive normal value of the given floating-point type   (public static member function) |
| lowest[static] (C++11) | returns the lowest finite value of the given type, i.e. the most negative value for signed types, ​0​ for unsigned types   (public static member function) |
| max[static] | returns the largest finite value of the given type   (public static member function) |
| epsilon[static] | returns the difference between `1.0` and the next representable value of the given floating-point type   (public static member function) |
| round_error[static] | returns the maximum rounding error of the given floating-point type   (public static member function) |
| infinity[static] | returns the positive infinity value of the given floating-point type   (public static member function) |
| quiet_NaN[static] | returns a quiet NaN value of the given floating-point type   (public static member function) |
| signaling_NaN[static] | returns a signaling NaN value of the given floating-point type   (public static member function) |
| denorm_min[static] | returns the smallest positive subnormal value of the given floating-point type   (public static member function) |

### Helper classes

|  |  |
| --- | --- |
| float_round_style | indicates floating-point rounding modes   (enum) |
| float_denorm_style | indicates floating-point denormalization modes   (enum) |

### Relationship with C library macro constants

| Specialization `std::numeric_limits<T>` where `T` is | Members | | | | | | | | | | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `min()` | `lowest()` (C++11) | `max()` | `radix` |
| bool | false | false | true | 2 |
| char | CHAR_MIN | CHAR_MIN | CHAR_MAX | 2 |
| signed char | SCHAR_MIN | SCHAR_MIN | SCHAR_MAX | 2 |
| unsigned char | ​0​ | ​0​ | UCHAR_MAX | 2 |
| wchar_t | WCHAR_MIN | WCHAR_MIN | WCHAR_MAX | 2 |
| char8_t | ​0​ | ​0​ | UCHAR_MAX | 2 |
| char16_t | ​0​ | ​0​ | UINT_LEAST16_MAX | 2 |
| char32_t | ​0​ | ​0​ | UINT_LEAST32_MAX | 2 |
| short | SHRT_MIN | SHRT_MIN | SHRT_MAX | 2 |
| signed short |
| unsigned short | ​0​ | ​0​ | USHRT_MAX | 2 |
| int | INT_MIN | INT_MIN | INT_MAX | 2 |
| signed int |
| unsigned int | ​0​ | ​0​ | UINT_MAX | 2 |
| long | LONG_MIN | LONG_MIN | LONG_MAX | 2 |
| signed long |
| unsigned long | ​0​ | ​0​ | ULONG_MAX | 2 |
| long long | LLONG_MIN | LLONG_MIN | LLONG_MAX | 2 |
| signed long long |
| unsigned long long | ​0​ | ​0​ | ULLONG_MAX | 2 |

| Specialization `std::numeric_limits<T>` where `T` is | Members | | | | | | | | | | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `denorm_min()` | `min()` | `lowest()` (C++11) | `max()` | `epsilon()` | `digits` | `digits10` |
| float | FLT_TRUE_MIN | FLT_MIN | -FLT_MAX | FLT_MAX | FLT_EPSILON | FLT_MANT_DIG | FLT_DIG |
| double | DBL_TRUE_MIN | DBL_MIN | -DBL_MAX | DBL_MAX | DBL_EPSILON | DBL_MANT_DIG | DBL_DIG |
| long double | LDBL_TRUE_MIN | LDBL_MIN | -LDBL_MAX | LDBL_MAX | LDBL_EPSILON | LDBL_MANT_DIG | LDBL_DIG |

| Specialization `std::numeric_limits<T>` where `T` is | Members (continue) | | | | | | | | | | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `min_exponent` | `min_exponent10` | `max_exponent` | `max_exponent10` | `radix` |
| float | FLT_MIN_EXP | FLT_MIN_10_EXP | FLT_MAX_EXP | FLT_MAX_10_EXP | FLT_RADIX |
| double | DBL_MIN_EXP | DBL_MIN_10_EXP | DBL_MAX_EXP | DBL_MAX_10_EXP | FLT_RADIX |
| long double | LDBL_MIN_EXP | LDBL_MIN_10_EXP | LDBL_MAX_EXP | LDBL_MAX_10_EXP | FLT_RADIX |

### Example

Run this code

```
#include <iostream>
#include <limits>
 
int main() 
{
    std::cout << "type\t│ lowest()\t│ min()\t\t│ max()\n"
              << "bool\t│ "
              << std::numeric_limits<bool>::lowest() << "\t\t│ "
              << std::numeric_limits<bool>::min() << "\t\t│ "
              << std::numeric_limits<bool>::max() << '\n'
              << "uchar\t│ "
              << +std::numeric_limits<unsigned char>::lowest() << "\t\t│ "
              << +std::numeric_limits<unsigned char>::min() << "\t\t│ "
              << +std::numeric_limits<unsigned char>::max() << '\n'
              << "int\t│ "
              << std::numeric_limits<int>::lowest() << "\t│ "
              << std::numeric_limits<int>::min() << "\t│ "
              << std::numeric_limits<int>::max() << '\n'
              << "float\t│ "
              << std::numeric_limits<float>::lowest() << "\t│ "
              << std::numeric_limits<float>::min() << "\t│ "
              << std::numeric_limits<float>::max() << '\n'
              << "double\t│ "
              << std::numeric_limits<double>::lowest() << "\t│ "
              << std::numeric_limits<double>::min() << "\t│ "
              << std::numeric_limits<double>::max() << '\n';
}

```

Possible output:

```
type	│ lowest()	│ min()		│ max()
bool	│ 0		│ 0		│ 1
uchar	│ 0		│ 0		│ 255
int	│ -2147483648	│ -2147483648	│ 2147483647
float	│ -3.40282e+38	│ 1.17549e-38	│ 3.40282e+38
double	│ -1.79769e+308	│ 2.22507e-308	│ 1.79769e+308

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 201 | C++98 | specializations for all fundamental types need to be provided | excluded non-arithmetic types |
| LWG 559 | C++98 | it was unclear whether the `std::numeric_limits` specialization for a cv-qualified type behaves as the same as the corresponding specialization for the cv-unqualified type | they have the same behavior |

### See also

- Fixed width integer types
- Arithmetic types
- C++ type system overview
- Type support (basic types, RTTI, type traits)
- C numeric limits interface
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/types/numeric_limits&oldid=167908>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 31 December 2023, at 09:44.