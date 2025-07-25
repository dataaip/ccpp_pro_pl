# std::ldexp, std::ldexpf, std::ldexpl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | abs(int)labsllabsimaxabs(C++11) | | | | | | abs(float)fabs | | | | | | divldivlldivimaxdiv(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmod | | | | | | remainder(C++11) | | | | | | remquo(C++11) | | | | | | fma(C++11) | | | | | | fmax(C++11) | | | | | | fmin(C++11) | | | | | | fdim(C++11) | | | | | | nannanfnanl(C++11)(C++11)(C++11) | | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****ldexp**** | | | | | | scalbnscalbln(C++11)(C++11) | | | | | | ilogb(C++11) | | | | | | logb(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | frexp | | | | | | modf | | | | | | nextafternexttoward(C++11)(C++11) | | | | | | copysign(C++11) | | | | | |
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
| float       ldexp ( float num, int exp );  double      ldexp ( double num, int exp ); long double ldexp ( long double num, int exp ); |  | (until C++23) |
| constexpr /\* floating-point-type \*/              ldexp ( /\* floating-point-type \*/ num, int exp ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       ldexpf( float num, int exp ); | (2) | (since C++11)  (constexpr since C++23) |
| long double ldexpl( long double num, int exp ); | (3) | (since C++11)  (constexpr since C++23) |
| Additional overloads (since C++11) |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Integer >  double      ldexp ( Integer num, int exp ); | (A) | (since C++11)  (constexpr since C++23) |
|  |  |  |

1-3) Multiplies a floating point value num by the number 2 raised to the exp power. The library provides overloads of `std::ldexp` for all cv-unqualified floating-point types as the type of the parameter num.(since C++23)

|  |  |
| --- | --- |
| A) Additional overloads are provided for all integer types, which are treated as double. | (since C++11) |

### Parameters

|  |  |  |
| --- | --- | --- |
| num | - | floating-point or integer value |
| exp | - | integer value |

### Return value

If no errors occur, num multiplied by 2 to the power of exp (num×2exp  
) is returned.

If a range error due to overflow occurs, ±HUGE_VAL, `±HUGE_VALF`, or `±HUGE_VALL` is returned.

If a range error due to underflow occurs, the correct result (after rounding) is returned.

### Error handling

Errors are reported as specified in math_errhandling.

If the implementation supports IEEE floating-point arithmetic (IEC 60559),

- Unless a range error occurs, FE_INEXACT is never raised (the result is exact).
- Unless a range error occurs, the current rounding mode is ignored.
- If num is ±0, it is returned, unmodified.
- If num is ±∞, it is returned, unmodified.
- If exp is 0, then num is returned, unmodified.
- If num is NaN, NaN is returned.

### Notes

On binary systems (where FLT_RADIX is 2), `std::ldexp` is equivalent to std::scalbn.

The function `std::ldexp` ("load exponent"), together with its dual, std::frexp, can be used to manipulate the representation of a floating-point number without direct bit manipulations.

On many implementations, `std::ldexp` is less efficient than multiplication or division by a power of two using arithmetic operators.

The additional overloads are not required to be provided exactly as (A). They only need to be sufficient to ensure that for their argument num of integer type, std::ldexp(num, exp) has the same effect as std::ldexp(static_cast<double>(num), exp).

For exponentiation of 2 by a floating point exponent, std::exp2 can be used.

### Example

Run this code

```
#include <cerrno>
#include <cfenv>
#include <cmath>
#include <cstring>
#include <iostream>
// #pragma STDC FENV_ACCESS ON
 
int main()
{
    std::cout
        << "ldexp(5, 3) = 5 * 8 = " << std::ldexp(5, 3) << '\n'
        << "ldexp(7, -4) = 7 / 16 = " << std::ldexp(7, -4) << '\n'
        << "ldexp(1, -1074) = " << std::ldexp(1, -1074)
        << " (minimum positive subnormal float64_t)\n"
        << "ldexp(nextafter(1,0), 1024) = "
        << std::ldexp(std::nextafter(1,0), 1024)
        << " (largest finite float64_t)\n";
 
    // special values
    std::cout << "ldexp(-0, 10) = " << std::ldexp(-0.0, 10) << '\n'
              << "ldexp(-Inf, -1) = " << std::ldexp(-INFINITY, -1) << '\n';
 
    // error handling
    std::feclearexcept(FE_ALL_EXCEPT);
    errno = 0;
    const double inf = std::ldexp(1, 1024);
    const bool is_range_error = errno == ERANGE;
 
    std::cout << "ldexp(1, 1024) = " << inf << '\n';
    if (is_range_error)
        std::cout << "    errno == ERANGE: " << std::strerror(ERANGE) << '\n';
    if (std::fetestexcept(FE_OVERFLOW))
        std::cout << "    FE_OVERFLOW raised\n";
}

```

Possible output:

```
ldexp(5, 3) = 5 * 8 = 40
ldexp(7, -4) = 7 / 16 = 0.4375
ldexp(1, -1074) = 4.94066e-324 (minimum positive subnormal float64_t)
ldexp(nextafter(1,0), 1024) = 1.79769e+308 (largest finite float64_t)
ldexp(-0, 10) = -0
ldexp(-Inf, -1) = -inf
ldexp(1, 1024) = inf
    errno == ERANGE: Numerical result out of range
    FE_OVERFLOW raised

```

### See also

|  |  |
| --- | --- |
| frexpfrexpffrexpl(C++11)(C++11) | decomposes a number into significand and base-2 exponent   (function) |
| scalbnscalbnfscalbnlscalblnscalblnfscalblnl(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | multiplies a number by FLT_RADIX raised to a power   (function) |
| exp2exp2fexp2l(C++11)(C++11)(C++11) | returns 2 raised to the given power (\({\small 2^x}\)2x)   (function) |
| C documentation for ldexp | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/math/ldexp&oldid=177736>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 November 2024, at 07:42.