# std::numeric_limits<T>::min

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
| ****numeric_limits::min**** | | | | |
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
|  |  |  |
| --- | --- | --- |
| static T min() throw(); |  | (until C++11) |
| static constexpr T min() noexcept; |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Returns the minimum finite value representable by the numeric type `T`.

For floating-point types with denormalization, `min()` returns the minimum positive normalized value. **Note that this behavior may be unexpected**, especially when compared to the behavior of `min()` for integral types. To find the value that has no values less than it, use `lowest()`.(since C++11)

`min()` is only meaningful for bounded types and for unbounded unsigned types.

### Return value

|  |  |
| --- | --- |
| `T` | std::numeric_limits<T>::min() |
| /\* non-specialized \*/ | T() |
| bool | false |
| char | CHAR_MIN |
| signed char | SCHAR_MIN |
| unsigned char | ​0​ |
| wchar_t | WCHAR_MIN |
| char8_t (since C++20) | ​0​ |
| char16_t (since C++11) | ​0​ |
| char32_t (since C++11) | ​0​ |
| short | SHRT_MIN |
| unsigned short | ​0​ |
| int | INT_MIN |
| unsigned int | ​0​ |
| long | LONG_MIN |
| unsigned long | ​0​ |
| long long (since C++11) | LLONG_MIN |
| unsigned long long (since C++11) | ​0​ |
| float | FLT_MIN |
| double | DBL_MIN |
| long double | LDBL_MIN |

### Example

Demonstrates the use with typedef types, and the difference in the sign of the result between integer and floating-point types:

Run this code

```
#include <cstddef>
#include <iomanip>
#include <iostream>
#include <limits>
 
// we want to print char types as an integer without leading Fs
auto p(auto x) { return x; }
auto p(char x) { return x & static_cast<unsigned char>(-1); }
 
template <typename T>
void print_one(std::string_view type_name)
{
    constexpr T min = std::numeric_limits<T>::min();
 
    std::cout 
        << std::dec << std::defaultfloat << std::setw(14) << type_name
        << " (" << std::setw(2) << sizeof(T) << " bytes): " << +min;
 
    if constexpr (min != 0)
        std::cout << " or " << std::showbase << std::hex << std::hexfloat << p(min);
 
    std::cout << '\n';
}
 
#define SHOW(T) print_one<T>(#T)
 
int main()
{
    SHOW(bool);
    SHOW(char);
    SHOW(unsigned char);
    SHOW(short);
    SHOW(unsigned short);
    SHOW(signed);
    SHOW(unsigned);
    SHOW(std::ptrdiff_t);
    SHOW(std::size_t);
    SHOW(float);
    SHOW(double);
    SHOW(long double);
}

```

Possible output:

```

          bool ( 1 bytes): 0
          char ( 1 bytes): -128 or 0x80
 unsigned char ( 1 bytes): 0
         short ( 2 bytes): -32768 or 0x8000
unsigned short ( 2 bytes): 0
        signed ( 4 bytes): -2147483648 or 0x80000000
      unsigned ( 4 bytes): 0
std::ptrdiff_t ( 8 bytes): -9223372036854775808 or 0x8000000000000000
   std::size_t ( 8 bytes): 0
         float ( 4 bytes): 1.17549e-38 or 0x1p-126
        double ( 8 bytes): 2.22507e-308 or 0x1p-1022
   long double (16 bytes): 3.3621e-4932 or 0x8p-16385

```

### See also

|  |  |
| --- | --- |
| lowest[static] (C++11) | returns the lowest finite value of the given type, i.e. the most negative value for signed types, ​0​ for unsigned types   (public static member function) |
| denorm_min[static] | returns the smallest positive subnormal value of the given floating-point type   (public static member function) |
| max[static] | returns the largest finite value of the given type   (public static member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/types/numeric_limits/min&oldid=178130>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 December 2024, at 18:39.