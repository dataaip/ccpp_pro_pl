# std::remainder, std::remainderf, std::remainderl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | abs(int)labsllabsimaxabs(C++11) | | | | | | abs(float)fabs | | | | | | divldivlldivimaxdiv(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmod | | | | | | ****remainder****(C++11) | | | | | | remquo(C++11) | | | | | | fma(C++11) | | | | | | fmax(C++11) | | | | | | fmin(C++11) | | | | | | fdim(C++11) | | | | | | nannanfnanl(C++11)(C++11)(C++11) | | | | | |
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
| float       remainder ( float x, float y );  double      remainder ( double x, double y ); long double remainder ( long double x, long double y ); |  | (until C++23) |
| constexpr /\*floating-point-type\*/              remainder ( /\*floating-point-type\*/ x, /\*floating-point-type\*/ y ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       remainderf( float x, float y ); | (2) | (since C++11)  (constexpr since C++23) |
| long double remainderl( long double x, long double y ); | (3) | (since C++11)  (constexpr since C++23) |
| SIMD overload (since C++26) |  |  |
| Defined in header `<simd>` |  |  |
| template< class V0, class V1 >  constexpr /\*math-common-simd-t\*/<V0, V1>             remainder ( const V0& v_x, const V1& v_y ); | (S) | (since C++26) |
| Additional overloads (since C++11) |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Integer >  double      remainder ( Integer x, Integer y ); | (A) | (constexpr since C++23) |
|  |  |  |

1-3) Computes the IEEE remainder of the floating point division operation x / y. The library provides overloads of `std::remainder` for all cv-unqualified floating-point types as the type of the parameters.(since C++23)

|  |  |
| --- | --- |
| S) The SIMD overload performs an element-wise `std::remainder` on v_xand v_y. (See **math-common-simd-t** for its definition.) | (since C++26) |

|  |  |
| --- | --- |
| A) Additional overloads are provided for all integer types, which are treated as double. | (since C++11) |

The IEEE floating-point remainder of the division operation x / y calculated by this function is exactly the value x - quo \* y, where the value quo is the integral value nearest the exact value x / y. When |quo - x / y| = ½, the value quo is chosen to be even.

In contrast to std::fmod, the returned value is not guaranteed to have the same sign as x.

If the returned value is zero, it will have the same sign as x.

### Parameters

|  |  |  |
| --- | --- | --- |
| x, y | - | floating-point or integer values |

### Return value

If successful, returns the IEEE floating-point remainder of the division x / y as defined above.

If a domain error occurs, an implementation-defined value is returned (NaN where supported).

If a range error occurs due to underflow, the correct result is returned.

If y is zero, but the domain error does not occur, zero is returned.

### Error handling

Errors are reported as specified in math_errhandling.

Domain error may occur if y is zero.

If the implementation supports IEEE floating-point arithmetic (IEC 60559),

- The current rounding mode has no effect.
- FE_INEXACT is never raised, the result is always exact.
- If x is ±∞ and y is not NaN, NaN is returned and FE_INVALID is raised.
- If y is ±0 and x is not NaN, NaN is returned and FE_INVALID is raised.
- If either argument is NaN, NaN is returned.

### Notes

POSIX requires that a domain error occurs if x is infinite or y is zero.

std::fmod, but not `std::remainder` is useful for doing silent wrapping of floating-point types to unsigned integer types: (0.0 <= (y = std::fmod(std::rint(x), 65536.0)) ? y : 65536.0 + y) is in the range `[`-0.0`,`65535.0`]`, which corresponds to unsigned short, but std::remainder(std::rint(x), 65536.0) is in the range `[`-32767.0`,`+32768.0`]`, which is outside of the range of signed short.

The additional overloads are not required to be provided exactly as (A). They only need to be sufficient to ensure that for their first argument num1 and second argument num2:

|  |  |
| --- | --- |
| - If num1 or num2 has type long double, then std::remainder(num1, num2) has the same effect as std::remainder(static_cast<long double>(num1),                static_cast<long double>(num2)). - Otherwise, if num1 and/or num2 has type double or an integer type, then std::remainder(num1, num2) has the same effect as std::remainder(static_cast<double>(num1),                static_cast<double>(num2)). - Otherwise, if num1 or num2 has type float, then std::remainder(num1, num2) has the same effect as std::remainder(static_cast<float>(num1),                static_cast<float>(num2)). | (until C++23) |
| If num1 and num2 have arithmetic types, then std::remainder(num1, num2) has the same effect as std::remainder(static_cast</\*common-floating-point-type\*/>(num1),                static_cast</\*common-floating-point-type\*/>(num2)), where /\*common-floating-point-type\*/ is the floating-point type with the greatest floating-point conversion rank and greatest floating-point conversion subrank between the types of num1 and num2, arguments of integer type are considered to have the same floating-point conversion rank as double.  If no such floating-point type with the greatest rank and subrank exists, then overload resolution does not result in a usable candidate from the overloads provided. | (since C++23) |

### Example

Run this code

```
#include <cfenv>
#include <cmath>
#include <iostream>
// #pragma STDC FENV_ACCESS ON
 
int main()
{
    std::cout << "remainder(+5.1, +3.0) = " << std::remainder(5.1, 3) << '\n'
              << "remainder(-5.1, +3.0) = " << std::remainder(-5.1, 3) << '\n'
              << "remainder(+5.1, -3.0) = " << std::remainder(5.1, -3) << '\n'
              << "remainder(-5.1, -3.0) = " << std::remainder(-5.1, -3) << '\n';
 
    // special values
    std::cout << "remainder(-0.0, 1.0) = " << std::remainder(-0.0, 1) << '\n'
              << "remainder(5.1, Inf) = " << std::remainder(5.1, INFINITY) << '\n';
 
    // error handling
    std::feclearexcept(FE_ALL_EXCEPT);
    std::cout << "remainder(+5.1, 0) = " << std::remainder(5.1, 0) << '\n';
    if (fetestexcept(FE_INVALID))
        std::cout << "    FE_INVALID raised\n";
}

```

Possible output:

```
remainder(+5.1, +3.0) = -0.9
remainder(-5.1, +3.0) = 0.9
remainder(+5.1, -3.0) = -0.9
remainder(-5.1, -3.0) = 0.9
remainder(-0.0, 1.0) = -0
remainder(5.1, Inf) = 5.1
remainder(+5.1, 0) = -nan
    FE_INVALID raised

```

### See also

|  |  |
| --- | --- |
| div(int)ldivlldiv(C++11) | computes quotient and remainder of integer division   (function) |
| fmodfmodffmodl(C++11)(C++11) | remainder of the floating point division operation   (function) |
| remquoremquofremquol(C++11)(C++11)(C++11) | signed remainder as well as the three last bits of the division operation   (function) |
| C documentation for remainder | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/math/remainder&oldid=160730>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 October 2023, at 09:12.