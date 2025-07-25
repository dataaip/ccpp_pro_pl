# std::rint, std::rintf, std::rintl, std::lrint, std::lrintf, std::lrintl, std::llrint, std::llrintf

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ceil | | | | | | floor | | | | | | roundlroundllround(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | trunc(C++11) | | | | | | nearbyint(C++11) | | | | | | ****rintlrintllrint****(C++11)(C++11)(C++11) | | | | | |
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
| Rounding to floating-point types |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| float       rint ( float num );  double      rint ( double num ); long double rint ( long double num ); |  | (since C++11)  (until C++23) |
| /\* floating-point-type \*/ rint( /\* floating-point-type \*/ num ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       rintf( float num ); | (2) | (since C++11) |
| long double rintl( long double num ); | (3) | (since C++11) |
| Rounding to long |  |  |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| long lrint ( float num );  long lrint ( double num ); long lrint ( long double num ); |  | (since C++11)  (until C++23) |
| long lrint ( /\* floating-point-type \*/ num ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| long lrintf( float num ); | (5) | (since C++11) |
| long lrintl( long double num ); | (6) | (since C++11) |
| Rounding to long long |  |  |
|  |  |  |
| --- | --- | --- |
|  | (7) |  |
| long long llrint ( float num );  long long llrint ( double num ); long long llrint ( long double num ); |  | (since C++11)  (until C++23) |
| long long llrint ( /\* floating-point-type \*/ num ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| long long llrintf( float num ); | (8) | (since C++11) |
| long long llrintl( long double num ); | (9) | (since C++11) |
| Additional overloads |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Integer >  double rint( Integer num ); | (A) | (since C++11) |
| template< class Integer >  long lrint( Integer num ); | (B) | (since C++11) |
| template< class Integer >  long long llrint( Integer num ); | (C) | (since C++11) |
|  |  |  |

1-3) Rounds the floating-point argument num to an integer value (in floating-point format), using the current rounding mode. The library provides overloads of `std::rint` for all cv-unqualified floating-point types as the type of the parameter num.(since C++23)4-9) Rounds the floating-point argument num to an integer value, using the current rounding mode. The library provides overloads of `std::lrint` and `std::llrint` for all cv-unqualified floating-point types as the type of the parameter num.(since C++23)A-C) Additional overloads are provided for all integer types, which are treated as double.

### Parameters

|  |  |  |
| --- | --- | --- |
| num | - | floating-point or integer value |

### Return value

If no errors occur, the nearest integer value to num, according to the current rounding mode, is returned.

### Error handling

Errors are reported as specified in math_errhandling.

If the result of `std::lrint` or `std::llrint` is outside the range representable by the return type, a domain error or a range error may occur.

If the implementation supports IEEE floating-point arithmetic (IEC 60559),

:   For the `std::rint` function:

- If num is ±∞, it is returned, unmodified.
- If num is ±0, it is returned, unmodified.
- If num is NaN, NaN is returned.

:   For `std::lrint` and `std::llrint` functions:

- If num is ±∞, FE_INVALID is raised and an implementation-defined value is returned.
- If the result of the rounding is outside the range of the return type, FE_INVALID is raised and an implementation-defined value is returned.
- If num is NaN, FE_INVALID is raised and an implementation-defined value is returned.

### Notes

POSIX specifies that all cases where `std::lrint` or `std::llrint` raise FE_INEXACT are domain errors.

As specified in math_errhandling, FE_INEXACT may be (but isn't required to be on non-IEEE floating-point platforms) raised by `std::rint` when rounding a non-integer finite value.

The only difference between `std::rint` and std::nearbyint is that std::nearbyint never raises FE_INEXACT.

The largest representable floating-point values are exact integers in all standard floating-point formats, so `std::rint` never overflows on its own; however the result may overflow any integer type (including std::intmax_t), when stored in an integer variable.

If the current rounding mode is:

- FE_DOWNWARD, then `std::rint` is equivalent to std::floor.
- FE_UPWARD, then `std::rint` is equivalent to std::ceil.
- FE_TOWARDZERO, then `std::rint` is equivalent to std::trunc.
- FE_TONEAREST, then `std::rint` differs from std::round in that halfway cases are rounded to even rather than away from zero.

The additional overloads are not required to be provided exactly as (A-C). They only need to be sufficient to ensure that for their argument num of integer type:

- std::rint(num) has the same effect as std::rint(static_cast<double>(num)).
- std::lrint(num) has the same effect as std::lrint(static_cast<double>(num)).
- std::llrint(num) has the same effect as std::llrint(static_cast<double>(num)).

### Example

Run this code

```
#include <cfenv>
#include <climits>
#include <cmath>
#include <iostream>
// #pragma STDC FENV_ACCESS ON
 
int main()
{
    std::fesetround(FE_TONEAREST);
    std::cout << "Rounding to nearest (halfway cases to even):\n"
              << "  rint(+2.3) = " << std::rint(2.3) << '\n'
              << "  rint(+2.5) = " << std::rint(2.5) << '\n'
              << "  rint(+3.5) = " << std::rint(3.5) << '\n'
              << "  rint(-2.3) = " << std::rint(-2.3) << '\n'
              << "  rint(-2.5) = " << std::rint(-2.5) << '\n'
              << "  rint(-3.5) = " << std::rint(-3.5) << '\n';
 
    std::fesetround(FE_DOWNWARD);
    std::cout << "Rounding down:\n"
              << "  rint(+2.3) = " << std::rint(2.3) << '\n'
              << "  rint(+2.5) = " << std::rint(2.5) << '\n'
              << "  rint(+3.5) = " << std::rint(3.5) << '\n'
              << "  rint(-2.3) = " << std::rint(-2.3) << '\n'
              << "  rint(-2.5) = " << std::rint(-2.5) << '\n'
              << "  rint(-3.5) = " << std::rint(-3.5) << '\n'
              << "Rounding down with lrint:\n"
              << "  lrint(+2.3) = " << std::lrint(2.3) << '\n'
              << "  lrint(+2.5) = " << std::lrint(2.5) << '\n'
              << "  lrint(+3.5) = " << std::lrint(3.5) << '\n'
              << "  lrint(-2.3) = " << std::lrint(-2.3) << '\n'
              << "  lrint(-2.5) = " << std::lrint(-2.5) << '\n'
              << "  lrint(-3.5) = " << std::lrint(-3.5) << '\n'
              << "Special values:\n"
              << "  lrint(-0.0) = " << std::lrint(-0.0) << '\n'
              << std::hex << std::showbase
              << "  lrint(-Inf) = " << std::lrint(-INFINITY) << '\n';
 
    // error handling
    std::feclearexcept(FE_ALL_EXCEPT);
 
    std::cout << "std::rint(0.1) = " << std::rint(.1) << '\n';
    if (std::fetestexcept(FE_INEXACT))
        std::cout << "  FE_INEXACT was raised\n";
 
    std::feclearexcept(FE_ALL_EXCEPT);
 
    std::cout << "std::lrint(LONG_MIN-2048.0) = "
              << std::lrint(LONG_MIN - 2048.0) << '\n';
    if (std::fetestexcept(FE_INVALID))
        std::cout << "  FE_INVALID was raised\n";
}

```

Possible output:

```
Rounding to nearest (halfway cases to even):
  rint(+2.3) = 2
  rint(+2.5) = 2
  rint(+3.5) = 4
  rint(-2.3) = -2
  rint(-2.5) = -2
  rint(-3.5) = -4
Rounding down:
  rint(+2.3) = 2
  rint(+2.5) = 2
  rint(+3.5) = 4
  rint(-2.3) = -2
  rint(-2.5) = -2
  rint(-3.5) = -4
Rounding down with lrint:
  lrint(+2.3) = 2
  lrint(+2.5) = 2
  lrint(+3.5) = 3
  lrint(-2.3) = -3
  lrint(-2.5) = -3
  lrint(-3.5) = -4
Special values:
  lrint(-0.0) = 0
  lrint(-Inf) = 0x8000000000000000
std::rint(0.1) = 0
std::lrint(LONG_MIN-2048.0) = 0x8000000000000000
  FE_INVALID was raised

```

### See also

|  |  |
| --- | --- |
| trunctruncftruncl(C++11)(C++11)(C++11) | nearest integer not greater in magnitude than the given value   (function) |
| nearbyintnearbyintfnearbyintl(C++11)(C++11)(C++11) | nearest integer using current rounding mode   (function) |
| fegetroundfesetround(C++11)(C++11) | gets or sets rounding direction   (function) |
| C documentation for rint | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/math/rint&oldid=160769>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 October 2023, at 21:41.