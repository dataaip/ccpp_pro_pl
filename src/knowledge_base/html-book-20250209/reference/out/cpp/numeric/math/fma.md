# std::fma, std::fmaf, std::fmal

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | abs(int)labsllabsimaxabs(C++11) | | | | | | abs(float)fabs | | | | | | divldivlldivimaxdiv(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmod | | | | | | remainder(C++11) | | | | | | remquo(C++11) | | | | | | ****fma****(C++11) | | | | | | fmax(C++11) | | | | | | fmin(C++11) | | | | | | fdim(C++11) | | | | | | nannanfnanl(C++11)(C++11)(C++11) | | | | | |
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
| float       fma ( float x, float y, float z );  double      fma ( double x, double y, double z ); long double fma ( long double x, long double y, long double z ); |  | (since C++11)  (until C++23) |
| constexpr /\* floating-point-type \*/              fma ( /\* floating-point-type \*/ x,                    /\* floating-point-type \*/ y, /\* floating-point-type \*/ z ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       fmaf( float x, float y, float z ); | (2) | (since C++11)  (constexpr since C++23) |
| long double fmal( long double x, long double y, long double z ); | (3) | (since C++11)  (constexpr since C++23) |
| #define FP_FAST_FMA  /\* implementation-defined \*/ | (4) | (since C++11) |
| #define FP_FAST_FMAF /\* implementation-defined \*/ | (5) | (since C++11) |
| #define FP_FAST_FMAL /\* implementation-defined \*/ | (6) | (since C++11) |
| Additional overloads |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Arithmetic1, class Arithmetic2, class Arithmetic3 >  /\* common-floating-point-type \*/     fma( Arithmetic1 x, Arithmetic2 y, Arithmetic3 z ); | (A) | (since C++11)  (constexpr since C++23) |
|  |  |  |

1-3) Computes x \* y + z as if to infinite precision and rounded only once to fit the result type. The library provides overloads of `std::fma` for all cv-unqualified floating-point types as the type of the parameters x, y and z.(since C++23)4-6) If the macro constants FP_FAST_FMA, FP_FAST_FMAF, or FP_FAST_FMAL are defined, the function `std::fma` evaluates faster (in addition to being more precise) than the expression x \* y + z for double, float, and long double arguments, respectively. If defined, these macros evaluate to integer 1.A) Additional overloads are provided for all other combinations of arithmetic types.

### Parameters

|  |  |  |
| --- | --- | --- |
| x, y, z | - | floating-point or integer values |

### Return value

If successful, returns the value of x \* y + z as if calculated to infinite precision and rounded once to fit the result type (or, alternatively, calculated as a single ternary floating-point operation).

If a range error due to overflow occurs, ±HUGE_VAL, `±HUGE_VALF`, or `±HUGE_VALL` is returned.

If a range error due to underflow occurs, the correct value (after rounding) is returned.

### Error handling

Errors are reported as specified in math_errhandling.

If the implementation supports IEEE floating-point arithmetic (IEC 60559),

- If x is zero and y is infinite or if x is infinite and y is zero, and
  - if z is not a NaN, then NaN is returned and FE_INVALID is raised,
  - if z is a NaN, then NaN is returned and FE_INVALID may be raised.
- If x \* y is an exact infinity and z is an infinity with the opposite sign, NaN is returned and FE_INVALID is raised.
- If x or y are NaN, NaN is returned.
- If z is NaN, and x \* y is not 0 \* Inf or Inf \* 0, then NaN is returned (without FE_INVALID).

### Notes

This operation is commonly implemented in hardware as fused multiply-add CPU instruction. If supported by hardware, the appropriate FP_FAST_FMA? macros are expected to be defined, but many implementations make use of the CPU instruction even when the macros are not defined.

POSIX (`fma`, `fmaf`, `fmal`) additionally specifies that the situations specified to return FE_INVALID are domain errors.

Due to its infinite intermediate precision, `std::fma` is a common building block of other correctly-rounded mathematical operations, such as std::sqrt or even the division (where not provided by the CPU, e.g. Itanium).

As with all floating-point expressions, the expression x \* y + z may be compiled as a fused multiply-add unless the #pragma STDC FP_CONTRACT is off.

The additional overloads are not required to be provided exactly as (A). They only need to be sufficient to ensure that for their first argument num1, second argument num2 and third argument num3:

|  |  |
| --- | --- |
| - If num1, num2 or num3 has type long double, then std::fma(num1, num2, num3) has the same effect as std::fma(static_cast<long double>(num1),          static_cast<long double>(num2),          static_cast<long double>(num3)). - Otherwise, if num1, num2 and/or num3 has type double or an integer type, then std::fma(num1, num2, num3) has the same effect as std::fma(static_cast<double>(num1),          static_cast<double>(num2),          static_cast<double>(num3)). - Otherwise, if num1, num2 or num3 has type float, then std::fma(num1, num2, num3) has the same effect as std::fma(static_cast<float>(num1),          static_cast<float>(num2),          static_cast<float>(num3)). | (until C++23) |
| If num1, num2 and num3 have arithmetic types, then std::fma(num1, num2, num3) has the same effect as std::fma(static_cast</\*common-floating-point-type\*/>(num1),          static_cast</\*common-floating-point-type\*/>(num2),          static_cast</\*common-floating-point-type\*/>(num3)), where /\*common-floating-point-type\*/ is the floating-point type with the greatest floating-point conversion rank and greatest floating-point conversion subrank among the types of num1, num2 and num3, arguments of integer type are considered to have the same floating-point conversion rank as double.  If no such floating-point type with the greatest rank and subrank exists, then overload resolution does not result in a usable candidate from the overloads provided. | (since C++23) |

### Example

Run this code

```
#include <cfenv>
#include <cmath>
#include <iomanip>
#include <iostream>
 
#ifndef __GNUC__
#pragma STDC FENV_ACCESS ON
#endif
 
int main()
{
    // demo the difference between fma and built-in operators
    const double in = 0.1;
    std::cout << "0.1 double is " << std::setprecision(23) << in
              << " (" << std::hexfloat << in << std::defaultfloat << ")\n"
              << "0.1*10 is 1.0000000000000000555112 (0x8.0000000000002p-3), "
              << "or 1.0 if rounded to double\n";
 
    const double expr_result = 0.1 * 10 - 1;
    const double fma_result = std::fma(0.1, 10, -1);
    std::cout << "0.1 * 10 - 1 = " << expr_result
              << " : 1 subtracted after intermediate rounding\n"
              << "fma(0.1, 10, -1) = " << std::setprecision(6) << fma_result << " ("
              << std::hexfloat << fma_result << std::defaultfloat << ")\n\n";
 
    // fma is used in double-double arithmetic
    const double high = 0.1 * 10;
    const double low = std::fma(0.1, 10, -high);
    std::cout << "in double-double arithmetic, 0.1 * 10 is representable as "
              << high << " + " << low << "\n\n";
 
    // error handling 
    std::feclearexcept(FE_ALL_EXCEPT);
    std::cout << "fma(+Inf, 10, -Inf) = " << std::fma(INFINITY, 10, -INFINITY) << '\n';
    if (std::fetestexcept(FE_INVALID))
        std::cout << "    FE_INVALID raised\n";
}

```

Possible output:

```
0.1 double is 0.10000000000000000555112 (0x1.999999999999ap-4)
0.1*10 is 1.0000000000000000555112 (0x8.0000000000002p-3), or 1.0 if rounded to double
0.1 * 10 - 1 = 0 : 1 subtracted after intermediate rounding
fma(0.1, 10, -1) = 5.55112e-17 (0x1p-54)
 
in double-double arithmetic, 0.1 * 10 is representable as 1 + 5.55112e-17
 
fma(+Inf, 10, -Inf) = -nan
    FE_INVALID raised

```

### See also

|  |  |
| --- | --- |
| remainderremainderfremainderl(C++11)(C++11)(C++11) | signed remainder of the division operation   (function) |
| remquoremquofremquol(C++11)(C++11)(C++11) | signed remainder as well as the three last bits of the division operation   (function) |
| C documentation for fma | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/math/fma&oldid=169193>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 January 2024, at 12:25.