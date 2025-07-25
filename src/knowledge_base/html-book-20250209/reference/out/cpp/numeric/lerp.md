# std::lerp

From cppreference.com
< cpp‎ | numeric
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

Numerics library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Common mathematical functions | | | | |
| Mathematical special functions (C++17) | | | | |
| Mathematical constants (C++20) | | | | |
| Basic linear algebra algorithms (C++26) | | | | |
| Data-parallel types (SIMD) (C++26) | | | | |
| Floating-point environment (C++11) | | | | |
| Complex numbers | | | | |
| Numeric array (`valarray`) | | | | |
| Pseudo-random number generation | | | | |
| Bit manipulation (C++20) | | | | |
| Factor operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | gcd(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lcm(C++17) | | | | | |
| Interpolations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | midpoint(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****lerp****(C++20) | | | | | |
| Saturation arithmetic | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | add_sat(C++26) | | | | | | sub_sat(C++26) | | | | | | saturate_cast(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mul_sat(C++26) | | | | | | div_sat(C++26) | | | | | |  | | | | | |
| Generic numeric operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | ranges::iota(C++23) | | | | | | accumulate | | | | | | inner_product | | | | | | adjacent_difference | | | | | | partial_sum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cmath>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| constexpr float       lerp( float a, float b, float t ) noexcept;  constexpr double      lerp( double a, double b, double t ) noexcept;  constexpr long double lerp( long double a, long double b, long double t ) noexcept; |  | (since C++20)  (until C++23) |
| constexpr /\* floating-point-type \*/      lerp( /\* floating-point-type \*/ a,            /\* floating-point-type \*/ b, /\* floating-point-type \*/ t ) noexcept; |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| Additional overloads |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Arithmetic1, class Arithmetic2, class Arithmetic3 >  constexpr /\* common-floating-point-type \*/     lerp( Arithmetic1 a, Arithmetic2 b, Arithmetic3 t ) noexcept; | (A) | (since C++20) |
|  |  |  |

1) Computes the linear interpolation between a and b, if the parameter t is inside ``​0​`,`1`)` (the [linear extrapolation otherwise), i.e. the result of \(a+t(b−a)\)a+t(b−a) with accounting for floating-point calculation imprecision. The library provides overloads for all cv-unqualified floating-point types as the type of the parameters a, b and t.(since C++23)A) Additional overloads are provided for all other combinations of arithmetic types.

### Parameters

|  |  |  |
| --- | --- | --- |
| a, b, t | - | floating-point or integer values |

### Return value

\(a + t(b − a)\)a + t(b − a)

When std::isfinite(a) && std::isfinite(b) is true, the following properties are guaranteed:

- If t == 0, the result is equal to a.
- If t == 1, the result is equal to b.
- If t >= 0 && t <= 1, the result is finite.
- If std::isfinite(t) && a == b, the result is equal to a.
- If std::isfinite(t) || (b - a != 0 && std::isinf(t)), the result is not NaN.

Let CMP(x, y) be 1 if x > y, -1 if x < y, and ​0​ otherwise. For any t1 and t2, the product of

- CMP(std::lerp(a, b, t2), std::lerp(a, b, t1)),
- CMP(t2, t1), and
- CMP(b, a)

is non-negative. (That is, `std::lerp` is monotonic.)

### Notes

The additional overloads are not required to be provided exactly as (A). They only need to be sufficient to ensure that for their first argument num1, second argument num2 and third argument num3:

|  |  |
| --- | --- |
| - If num1, num2 or num3 has type long double, then std::lerp(num1, num2, num3) has the same effect as std::lerp(static_cast<long double>(num1),           static_cast<long double>(num2),           static_cast<long double>(num3)). - Otherwise, if num1, num2 and/or num3 has type double or an integer type, then std::lerp(num1, num2, num3) has the same effect as std::lerp(static_cast<double>(num1),           static_cast<double>(num2),           static_cast<double>(num3)). - Otherwise, if num1, num2 or num3 has type float, then std::lerp(num1, num2, num3) has the same effect as std::lerp(static_cast<float>(num1),           static_cast<float>(num2),           static_cast<float>(num3)). | (until C++23) |
| If num1, num2 and num3 have arithmetic types, then std::lerp(num1, num2, num3) has the same effect as std::lerp(static_cast</\*common-floating-point-type\*/>(num1),           static_cast</\*common-floating-point-type\*/>(num2),           static_cast</\*common-floating-point-type\*/>(num3)), where /\*common-floating-point-type\*/ is the floating-point type with the greatest floating-point conversion rank and greatest floating-point conversion subrank among the types of num1, num2 and num3, arguments of integer type are considered to have the same floating-point conversion rank as double.  If no such floating-point type with the greatest rank and subrank exists, then overload resolution does not result in a usable candidate from the overloads provided. | (since C++23) |

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_interpolate` | `201902L` | (C++20) | `std::lerp`, std::midpoint |

### Example

Run this code

```
#include <cassert>
#include <cmath>
#include <iostream>
 
float naive_lerp(float a, float b, float t)
{
    return a + t * (b - a);
}
 
int main()
{
    std::cout << std::boolalpha;
 
    const float a = 1e8f, b = 1.0f;
    const float midpoint = std::lerp(a, b, 0.5f);
 
    std::cout << "a = " << a << ", " << "b = " << b << '\n'
              << "midpoint = " << midpoint << '\n';
 
    std::cout << "std::lerp is exact: "
              << (a == std::lerp(a, b, 0.0f)) << ' '
              << (b == std::lerp(a, b, 1.0f)) << '\n';
 
    std::cout << "naive_lerp is exact: "
              << (a == naive_lerp(a, b, 0.0f)) << ' '
              << (b == naive_lerp(a, b, 1.0f)) << '\n';
 
    std::cout << "std::lerp(a, b, 1.0f) = " << std::lerp(a, b, 1.0f) << '\n'
              << "naive_lerp(a, b, 1.0f) = " << naive_lerp(a, b, 1.0f) << '\n';
 
    assert(not std::isnan(std::lerp(a, b, INFINITY))); // lerp here can be -inf
 
    std::cout << "Extrapolation demo, given std::lerp(5, 10, t):\n";
    for (auto t{-2.0}; t <= 2.0; t += 0.5)
        std::cout << std::lerp(5.0, 10.0, t) << ' ';
    std::cout << '\n';
}

```

Possible output:

```
a = 1e+08, b = 1
midpoint = 5e+07
std::lerp is exact?: true true
naive_lerp is exact?: true false
std::lerp(a, b, 1.0f) = 1
naive_lerp(a, b, 1.0f) = 0
Extrapolation demo, given std::lerp(5, 10, t):
-5 -2.5 0 2.5 5 7.5 10 12.5 15

```

### See also

|  |  |
| --- | --- |
| midpoint(C++20) | midpoint between two numbers or pointers   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/lerp&oldid=160721>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 October 2023, at 08:32.