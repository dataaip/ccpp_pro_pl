# std::numeric_limits<T>::is_modulo

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
| ****numeric_limits::is_modulo**** | | | | |
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
| static const bool is_modulo; |  | (until C++11) |
| static constexpr bool is_modulo; |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

The value of std::numeric_limits<T>::is_modulo is true for all arithmetic types `T` that handle overflows with modulo arithmetic, that is, if the result of addition, subtraction, multiplication, or division of this type would fall outside the range ``[min()`,`max()`]`, the value returned by such operation differs from the expected value by a multiple of max() - min() + 1.

`is_modulo` is false for signed integer types, unless the implementation defines signed integer overflow to wrap.

### Standard specializations

|  |  |
| --- | --- |
| `T` | value of std::numeric_limits<T>::is_modulo |
| /\* non-specialized \*/ | false |
| bool | false |
| char | implementation-defined |
| signed char | implementation-defined |
| unsigned char | true |
| wchar_t | implementation-defined |
| char8_t (since C++20) | true |
| char16_t (since C++11) | true |
| char32_t (since C++11) | true |
| short | implementation-defined |
| unsigned short | true |
| int | implementation-defined |
| unsigned int | true |
| long | implementation-defined |
| unsigned long | true |
| long long (C++11) | implementation-defined |
| unsigned long long (C++11) | true |
| float | false |
| double | false |
| long double | false |

### Notes

The standard said "On most machines, this is true for signed integers." before the resolution of LWG issue 2422. See GCC PR 22200 for a related discussion.

### Example

Demonstrates the behavior of modulo types:

Run this code

```
#include <iostream>
#include <type_traits>
#include <limits>
 
template<class T>
typename std::enable_if<std::numeric_limits<T>::is_modulo>::type
    check_overflow()
{
    std::cout << "max value is " << std::numeric_limits<T>::max() << '\n'
              << "min value is " << std::numeric_limits<T>::min() << '\n'
              << "max value + 1 is " << std::numeric_limits<T>::max()+1 << '\n';
}
 
int main()
{
    check_overflow<int>();
    std::cout << '\n';
    check_overflow<unsigned long>();
//  check_overflow<float>(); // compile-time error, not a modulo type
}

```

Possible output:

```
max value is 2147483647
min value is -2147483648
max value + 1 is -2147483648
 
max value is 18446744073709551615
min value is 0
max value + 1 is 0

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 612 | C++98 | the definition of "handle overflows with modulo arithmetic" was poor[[1]](is_modulo.html#cite_note-1) | provided a better definition |
| LWG 2422 | C++98 | `is_modulo` was required to be true for signed integer types on most machines | required to be false for signed integer types unless signed integer overflow is defined to wrap |

1. ↑ The definition is "adding two positive numbers can have a result that wraps around to a third number that is less". It has the following problems:
   - It does not define the wrapped value.
   - It does not state whether result is repeatable.
   - It does not require that doing addition, subtraction and other operations on all values have defined behavior.

### See also

|  |  |
| --- | --- |
| is_integer[static] | identifies integer types   (public static member constant) |
| is_iec559[static] | identifies the IEC 559/IEEE 754 floating-point types   (public static member constant) |
| is_exact[static] | identifies exact types   (public static member constant) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/types/numeric_limits/is_modulo&oldid=148715>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 March 2023, at 01:49.