# std::remquo, std::remquof, std::remquol

From cppreference.com
< cpp‎ | numeric‎ | math
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | midpoint(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lerp(C++20) | | | | | |
| Saturation arithmetic | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | add_sat(C++26) | | | | | | sub_sat(C++26) | | | | | | saturate_cast(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mul_sat(C++26) | | | | | | div_sat(C++26) | | | | | |  | | | | | |
| Generic numeric operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | ranges::iota(C++23) | | | | | | accumulate | | | | | | inner_product | | | | | | adjacent_difference | | | | | | partial_sum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |

Common mathematical functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Basic operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | abs(int)labsllabsimaxabs(C++11) | | | | | | abs(float)fabs | | | | | | divldivlldivimaxdiv(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmod | | | | | | remainder(C++11) | | | | | | ****remquo****(C++11) | | | | | | fma(C++11) | | | | | | fmax(C++11) | | | | | | fmin(C++11) | | | | | | fdim(C++11) | | | | | | nannanfnanl(C++11)(C++11)(C++11) | | | | | |
| Exponential functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | exp | | | | | | exp2(C++11) | | | | | | expm1(C++11) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log | | | | | | log10 | | | | | | log1p(C++11) | | | | | | log2(C++11) | | | | | |
| Power functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | sqrt | | | | | | cbrt(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hypot(C++11) | | | | | | pow | | | | | |
| Trigonometric and  hyperbolic functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sinh | | | | | | cosh | | | | | | tanh | | | | | | asinh(C++11) | | | | | | acosh(C++11) | | | | | | atanh(C++11) | | | | | |  | | | | | |
| Error and gamma functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erf(C++11) | | | | | | erfc(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lgamma(C++11) | | | | | | tgamma(C++11) | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Nearest integer floating point operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ceil | | | | | | floor | | | | | | roundlroundllround(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | trunc(C++11) | | | | | | nearbyint(C++11) | | | | | | rintlrintllrint(C++11)(C++11)(C++11) | | | | | |
| Floating point manipulation functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ldexp | | | | | | scalbnscalbln(C++11)(C++11) | | | | | | ilogb(C++11) | | | | | | logb(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | frexp | | | | | | modf | | | | | | nextafternexttoward(C++11)(C++11) | | | | | | copysign(C++11) | | | | | |
| Classification and comparison | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | fpclassify(C++11) | | | | | | isfinite(C++11) | | | | | | isinf(C++11) | | | | | | isnan(C++11) | | | | | | isnormal(C++11) | | | | | | signbit(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isgreater(C++11) | | | | | | isgreaterequal(C++11) | | | | | | isless(C++11) | | | | | | islessequal(C++11) | | | | | | islessgreater(C++11) | | | | | | isunordered(C++11) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | div_t | | | | | | ldiv_t | | | | | | lldiv_t(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | imaxdiv_t(C++11) | | | | | | float_t(C++11) | | | | | | double_t(C++11) | | | | | |
| Macro constants | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | HUGE_VALFHUGE_VALHUGE_VALL(C++11)(C++11) | | | | | | math_errhandlingMATH_ERRNOMATH_ERREXCEPT(C++11) | | | | | | INFINITY(C++11) | | | | | | NAN(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Classification | | | | | | FP_NORMALFP_SUBNORMALFP_ZEROFP_INFINITEFP_NAN(C++11)(C++11)(C++11)(C++11)(C++11) | | | | | |  | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cmath>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| float       remquo ( float x, float y, int\* quo );  double      remquo ( double x, double y, int\* quo ); long double remquo ( long double x, long double y, int\* quo ); |  | (since C++11)  (until C++23) |
| constexpr /\* floating-point-type \*/              remquo ( /\* floating-point-type \*/ x, /\* floating-point-type \*/ y, int\* quo ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       remquof( float x, float y, int\* quo ); | (2) | (since C++11)  (constexpr since C++23) |
| long double remquol( long double x, long double y, int\* quo ); | (3) | (since C++11)  (constexpr since C++23) |
| Additional overloads |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Arithmetic1, class Arithmetic2 >  /\* common-floating-point-type \*/     remquo( Arithmetic1 x, Arithmetic2 y, int\* quo ); | (A) | (since C++11)  (constexpr since C++23) |
|  |  |  |

1-3) Computes the floating-point remainder of the division operation x / y as the std::remainder() function does. Additionally, the sign and at least the three of the last bits of x / y will be stored in quo, sufficient to determine the octant of the result within a period. The library provides overloads of `std::remquo` for all cv-unqualified floating-point types as the type of the parameters x and y.(since C++23)A) Additional overloads are provided for all other combinations of arithmetic types.

### Parameters

|  |  |  |
| --- | --- | --- |
| x, y | - | floating-point or integer values |
| quo | - | pointer to int to store the sign and some bits of x / y |

### Return value

If successful, returns the floating-point remainder of the division x / y as defined in std::remainder, and stores, in \*quo, the sign and at least three of the least significant bits of x / y (formally, stores a value whose sign is the sign of x / y and whose magnitude is congruent modulo 2n  
 to the magnitude of the integral quotient of x / y, where n is an implementation-defined integer greater than or equal to 3).

If y is zero, the value stored in \*quo is unspecified.

If a domain error occurs, an implementation-defined value is returned (NaN where supported).

If a range error occurs due to underflow, the correct result is returned if subnormals are supported.

If y is zero, but the domain error does not occur, zero is returned.

### Error handling

Errors are reported as specified in math_errhandling.

Domain error may occur if y is zero.

If the implementation supports IEEE floating-point arithmetic (IEC 60559),

- The current rounding mode has no effect.
- FE_INEXACT is never raised.
- If x is ±∞ and y is not NaN, NaN is returned and FE_INVALID is raised.
- If y is ±0 and x is not NaN, NaN is returned and FE_INVALID is raised.
- If either x or y is NaN, NaN is returned.

### Notes

POSIX requires that a domain error occurs if x is infinite or y is zero.

This function is useful when implementing periodic functions with the period exactly representable as a floating-point value: when calculating sin(πx) for a very large x, calling std::sin directly may result in a large error, but if the function argument is first reduced with `std::remquo`, the low-order bits of the quotient may be used to determine the sign and the octant of the result within the period, while the remainder may be used to calculate the value with high precision.

On some platforms this operation is supported by hardware (and, for example, on Intel CPUs, `FPREM1` leaves exactly 3 bits of precision in the quotient when complete).

The additional overloads are not required to be provided exactly as (A). They only need to be sufficient to ensure that for their first argument num1 and second argument num2:

|  |  |
| --- | --- |
| - If num1 or num2 has type long double, then std::remquo(num1, num2, quo) has the same effect as std::remquo(static_cast<long double>(num1),             static_cast<long double>(num2), quo). - Otherwise, if num1 and/or num2 has type double or an integer type, then std::remquo(num1, num2, quo) has the same effect as std::remquo(static_cast<double>(num1),             static_cast<double>(num2), quo). - Otherwise, if num1 or num2 has type float, then std::remquo(num1, num2, quo) has the same effect as std::remquo(static_cast<float>(num1),             static_cast<float>(num2), quo). | (until C++23) |
| If num1 and num2 have arithmetic types, then std::remquo(num1, num2, quo) has the same effect as std::remquo(static_cast</\*common-floating-point-type\*/>(num1),             static_cast</\*common-floating-point-type\*/>(num2), quo), where /\*common-floating-point-type\*/ is the floating-point type with the greatest floating-point conversion rank and greatest floating-point conversion subrank between the types of num1 and num2, arguments of integer type are considered to have the same floating-point conversion rank as double.  If no such floating-point type with the greatest rank and subrank exists, then overload resolution does not result in a usable candidate from the overloads provided. | (since C++23) |

### Example

Run this code

```
#include <cfenv>
#include <cmath>
#include <iostream>
 
#ifndef __GNUC__
#pragma STDC FENV_ACCESS ON
#endif
 
const double pi = std::acos(-1); // or std::numbers::pi since C++20
 
double cos_pi_x_naive(double x)
{
    return std::cos(pi * x);
}
 
// the period is 2, values are (0;0.5) positive, (0.5;1.5) negative, (1.5,2) positive
double cos_pi_x_smart(double x)
{
    int quadrant;
    double rem = std::remquo(x, 1, &quadrant);
    quadrant = static_cast<unsigned>(quadrant) % 2; // The period is 2.
    return quadrant == 0 ?  std::cos(pi * rem)
                         : -std::cos(pi * rem);
}
 
int main()
{
    std::cout << std::showpos
              << "naive:\n"
              << "  cos(pi * 0.25) = " << cos_pi_x_naive(0.25) << '\n'
              << "  cos(pi * 1.25) = " << cos_pi_x_naive(1.25) << '\n'
              << "  cos(pi * 2.25) = " << cos_pi_x_naive(2.25) << '\n'
              << "smart:\n"
              << "  cos(pi * 0.25) = " << cos_pi_x_smart(0.25) << '\n'
              << "  cos(pi * 1.25) = " << cos_pi_x_smart(1.25) << '\n'
              << "  cos(pi * 2.25) = " << cos_pi_x_smart(2.25) << '\n'
              << "naive:\n"
              << "  cos(pi * 1000000000000.25) = "
              << cos_pi_x_naive(1000000000000.25) << '\n'
              << "  cos(pi * 1000000000001.25) = "
              << cos_pi_x_naive(1000000000001.25) << '\n'
              << "smart:\n"
              << "  cos(pi * 1000000000000.25) = "
              << cos_pi_x_smart(1000000000000.25) << '\n'
              << "  cos(pi * 1000000000001.25) = "
              << cos_pi_x_smart(1000000000001.25) << '\n';
 
    // error handling
    std::feclearexcept(FE_ALL_EXCEPT);
 
    int quo;
    std::cout << "remquo(+Inf, 1) = " << std::remquo(INFINITY, 1, &quo) << '\n';
    if (fetestexcept(FE_INVALID))
        std::cout << "  FE_INVALID raised\n";
}

```

Possible output:

```
naive:
  cos(pi * 0.25) = +0.707107
  cos(pi * 1.25) = -0.707107
  cos(pi * 2.25) = +0.707107
smart:
  cos(pi * 0.25) = +0.707107
  cos(pi * 1.25) = -0.707107
  cos(pi * 2.25) = +0.707107
naive:
  cos(pi * 1000000000000.25) = +0.707123
  cos(pi * 1000000000001.25) = -0.707117
smart:
  cos(pi * 1000000000000.25) = +0.707107
  cos(pi * 1000000000001.25) = -0.707107
remquo(+Inf, 1) = -nan
  FE_INVALID raised

```

### See also

|  |  |
| --- | --- |
| div(int)ldivlldiv(C++11) | computes quotient and remainder of integer division   (function) |
| fmodfmodffmodl(C++11)(C++11) | remainder of the floating point division operation   (function) |
| remainderremainderfremainderl(C++11)(C++11)(C++11) | signed remainder of the division operation   (function) |
| C documentation for remquo | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/math/remquo&oldid=160731>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 October 2023, at 09:15.