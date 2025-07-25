# std::scalbn, std::scalbnf, std::scalbnl, std::scalbln, std::scalblnf, std::scalblnl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ldexp | | | | | | ****scalbnscalbln****(C++11)(C++11) | | | | | | ilogb(C++11) | | | | | | logb(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | frexp | | | | | | modf | | | | | | nextafternexttoward(C++11)(C++11) | | | | | | copysign(C++11) | | | | | |
| Classification and comparison | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | fpclassify(C++11) | | | | | | isfinite(C++11) | | | | | | isinf(C++11) | | | | | | isnan(C++11) | | | | | | isnormal(C++11) | | | | | | signbit(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isgreater(C++11) | | | | | | isgreaterequal(C++11) | | | | | | isless(C++11) | | | | | | islessequal(C++11) | | | | | | islessgreater(C++11) | | | | | | isunordered(C++11) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | div_t | | | | | | ldiv_t | | | | | | lldiv_t(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | imaxdiv_t(C++11) | | | | | | float_t(C++11) | | | | | | double_t(C++11) | | | | | |
| Macro constants | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | HUGE_VALFHUGE_VALHUGE_VALL(C++11)(C++11) | | | | | | math_errhandlingMATH_ERRNOMATH_ERREXCEPT(C++11) | | | | | | INFINITY(C++11) | | | | | | NAN(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Classification | | | | | | FP_NORMALFP_SUBNORMALFP_ZEROFP_INFINITEFP_NAN(C++11)(C++11)(C++11)(C++11)(C++11) | | | | | |  | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cmath>` |  |  |
| int exponent |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| float       scalbn ( float num, int exp );  double      scalbn ( double num, int exp ); long double scalbn ( long double num, int exp ); |  | (since C++11)  (until C++23) |
| constexpr /\* floating-point-type \*/              scalbn ( /\* floating-point-type \*/ num, int exp ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       scalbnf( float num, int exp ); | (2) | (since C++11)  (constexpr since C++23) |
| long double scalbnl( long double num, int exp ); | (3) | (since C++11)  (constexpr since C++23) |
| long exponent |  |  |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| float       scalbln ( float num, long exp );  double      scalbln ( double num, long exp ); long double scalbln ( long double num, long exp ); |  | (since C++11)  (until C++23) |
| constexpr /\* floating-point-type \*/              scalbln ( /\* floating-point-type \*/ num, long exp ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       scalblnf( float num, long exp ); | (5) | (since C++11)  (constexpr since C++23) |
| long double scalblnl( long double num, long exp ); | (6) | (since C++11)  (constexpr since C++23) |
| Additional overloads |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Integer >  double scalbn( Integer num, int exp ); | (A) | (since C++11)  (constexpr since C++23) |
| template< class Integer >  double scalbln( Integer num, long exp ); | (B) | (since C++11)  (constexpr since C++23) |
|  |  |  |

1-6) Multiplies a floating point value num by FLT_RADIX raised to power exp. The library provides overloads of `std::scalbn` and `std::scalbln` for all cv-unqualified floating-point types as the type of the parameter num.(since C++23)A,B) Additional overloads are provided for all integer types, which are treated as double.

### Parameters

|  |  |  |
| --- | --- | --- |
| num | - | floating-point or integer value |
| exp | - | integer value |

### Return value

If no errors occur, num multiplied by FLT_RADIX to the power of exp (num×FLT_RADIXexp  
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

On binary systems (where FLT_RADIX is 2), `std::scalbn` is equivalent to std::ldexp.

Although `std::scalbn` and `std::scalbln` are specified to perform the operation efficiently, on many implementations they are less efficient than multiplication or division by a power of two using arithmetic operators.

The function name stands for "new scalb", where `scalb` was an older non-standard function whose second argument had floating-point type.

The `std::scalbln` function is provided because the factor required to scale from the smallest positive floating-point value to the largest finite one may be greater than 32767, the standard-guaranteed INT_MAX. In particular, for the 80-bit long double, the factor is 32828.

The GNU implementation does not set `errno` regardless of `math_errhandling`.

The additional overloads are not required to be provided exactly as (A,B). They only need to be sufficient to ensure that for their argument num of integer type:

- std::scalbn(num, exp) has the same effect as std::scalbn(static_cast<double>(num), exp).
- std::scalbln(num, exp) has the same effect as std::scalbln(static_cast<double>(num), exp).

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
    std::cout << "scalbn(7, -4) = " << std::scalbn(7, -4) << '\n'
              << "scalbn(1, -1074) = " << std::scalbn(1, -1074)
              << " (minimum positive subnormal double)\n"
              << "scalbn(nextafter(1,0), 1024) = "
              << std::scalbn(std::nextafter(1,0), 1024)
              << " (largest finite double)\n";
 
    // special values
    std::cout << "scalbn(-0, 10) = " << std::scalbn(-0.0, 10) << '\n'
              << "scalbn(-Inf, -1) = " << std::scalbn(-INFINITY, -1) << '\n';
 
    // error handling
    errno = 0;
    std::feclearexcept(FE_ALL_EXCEPT);
 
    std::cout << "scalbn(1, 1024) = " << std::scalbn(1, 1024) << '\n';
 
    if (errno == ERANGE)
        std::cout << "    errno == ERANGE: " << std::strerror(errno) << '\n';
    if (std::fetestexcept(FE_OVERFLOW))
        std::cout << "    FE_OVERFLOW raised\n";
}

```

Possible output:

```
scalbn(7, -4) = 0.4375
scalbn(1, -1074) = 4.94066e-324 (minimum positive subnormal double)
scalbn(nextafter(1,0), 1024) = 1.79769e+308 (largest finite double)
scalbn(-0, 10) = -0
scalbn(-Inf, -1) = -inf
scalbn(1, 1024) = inf
    errno == ERANGE: Numerical result out of range
    FE_OVERFLOW raised

```

### See also

|  |  |
| --- | --- |
| frexpfrexpffrexpl(C++11)(C++11) | decomposes a number into significand and base-2 exponent   (function) |
| ldexpldexpfldexpl(C++11)(C++11) | multiplies a number by 2 raised to an integral power   (function) |
| C documentation for scalbn | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/math/scalbn&oldid=177738>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 November 2024, at 07:42.