# round, roundf, roundl, lround, lroundf, lroundl, llround, llroundf, llroundl

From cppreference.com
< c‎ | numeric‎ | math
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 Numerics

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Common mathematical functions | | | | |
| Floating-point environment (C99) | | | | |
| Pseudo-random number generation | | | | |
| Complex number arithmetic (C99) | | | | |
| Type-generic math (C99) | | | | |
| Bit manipulation (C23) | | | | |
| Checked integer arithmetic (C23) | | | | |

 Common mathematical functions

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | Basic operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | abslabsllabsimaxabs(C99)(C99) | | | | | | fabs | | | | | | divldivlldivimaxdiv(C99)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmod | | | | | | remainder(C99) | | | | | | remquo(C99) | | | | | | fma(C99) | | | | | | fdim(C99) | | | | | | nannanfnanlnand**N**(C99)(C99)(C99)(C23) | | | | | | | Maximum/minimum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmax(C99) | | | | | | fmin(C99) | | | | | | fmaximum")(C23) | | | | | | fminimum")(C23) | | | | | | fmaximum_mag")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmaximum_num")(C23) | | | | | | fminimum_mag")(C23) | | | | | | fminimum_num")(C23) | | | | | | fmaximum_mag_num")(C23) | | | | | | fminimum_mag_num")(C23) | | | | | | | Exponential functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | exp | | | | | | exp10")(C23) | | | | | | exp2(C99) | | | | | | expm1(C99) | | | | | | exp10m1")(C23) | | | | | | exp2m1")(C23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log | | | | | | log10 | | | | | | log2(C99) | | | | | | log1plogp1(C99)(C23) | | | | | | log10p1")(C23) | | | | | | log2p1")(C23) | | | | | | | Power functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sqrt | | | | | | cbrt(C99) | | | | | | rootn")(C23) | | | | | | rsqrt")(C23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hypot(C99) | | | | | | compound")(C23) | | | | | | pow | | | | | | pown")(C23) | | | | | | powr")(C23) | | | | | | | Trigonometric and hyperbolic functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinpi(C23) | | | | | | cospi(C23) | | | | | | tanpi")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asinpi")(C23) | | | | | | acospi")(C23) | | | | | | atanpi")(C23) | | | | | | atan2pi")(C23) | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | asinh(C99) | | | | | | acosh(C99) | | | | | | atanh(C99) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Nearest integer floating-point | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ceil | | | | | | floor | | | | | | ****roundlroundllround****(C99)(C99)(C99) | | | | | | roundeven(C23) | | | | | | trunc(C99) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | nearbyint(C99) | | | | | | rintlrintllrint(C99)(C99)(C99) | | | | | | fromfpfromfpxufromfpufromfpx")(C23)(C23)(C23)(C23) | | | | | | | Floating-point manipulation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ldexp | | | | | | frexp | | | | | | scalbnscalbln(C99)(C99) | | | | | | ilogbllogb(C99)(C23) | | | | | | logb(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | modf | | | | | | nextafternexttoward(C99)(C99) | | | | | | nextupnextdown")(C23)(C23) | | | | | | copysign(C99) | | | | | | canonicalize")(C23) | | | | | | | Narrowing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fadd")(C23) | | | | | | fsub")(C23) | | | | | | fmul")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fdiv")(C23) | | | | | | ffma")(C23) | | | | | | fsqrt")(C23) | | | | | | | Quantum and quantum exponent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | quantized**N**")(C23) | | | | | | quantumd**N**")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | samequantumd**N**")(C23) | | | | | | llquantexpd**N**")(C23) | | | | | | | Decimal re-encoding functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | encodedecd**N**")(C23) | | | | | | decodedecd**N**")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | encodebind**N**")(C23) | | | | | | decodebind**N**")(C23) | | | | | | | Total order and payload functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | totalorder")(C23) | | | | | | getpayload")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setpayload")(C23) | | | | | | setpayloadsig")(C23) | | | | | | | Classification | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fpclassify(C99) | | | | | | iscanonical")(C23) | | | | | | isfinite(C99) | | | | | | isinf(C99) | | | | | | isnan(C99) | | | | | | isnormal(C99) | | | | | | signbit(C99) | | | | | | issubnormal")(C23) | | | | | | iszero")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isgreater(C99) | | | | | | isgreaterequal(C99) | | | | | | isless(C99) | | | | | | islessequal(C99) | | | | | | islessgreater(C99) | | | | | | isunordered(C99) | | | | | | issignaling")(C23) | | | | | | iseqsig")(C23) | | | | | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Error and gamma functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | erf(C99) | | | | | | erfc(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lgamma(C99) | | | | | | tgamma(C99) | | | | | | | Types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | div_tldiv_tlldiv_timaxdiv_t(C99)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | float_tdouble_t(C99)(C99) | | | | | | _Decimal32_t_Decimal64_t")(C23)(C23) | | | | | | | Macro constants | | | | | | Special floating-point values | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | HUGE_VALHUGE_VALFHUGE_VALLHUGE_VALD**N**(C99)(C99)(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | INFINITYDEC_INFINITY(C99)(C23) | | | | | | NANDEC_NAN(C99)(C23) | | | | | | | Arguments and return values | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FP_ILOGB0FP_ILOGBNAN(C99)(C99) | | | | | | FP_NORMALFP_SUBNORMALFP_ZEROFP_INFINITEFP_NAN(C99)(C99)(C99)(C99)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FP_LLOGB0FP_LLOGBNAN(C23)(C23) | | | | | | FP_INT_UPWARDFP_INT_DOWNWARDFP_INT_TOWARDZEROFP_INT_TONEARESTFROMZEROFP_INT_TONEAREST")(C23)(C23)(C23)(C23)(C23) | | | | | | | Error handling | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MATH_ERRNOMATH_ERRNOEXCEPT(C99)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | math_errhandling(C99) | | | | | |  | | | | | | | Fast operation indicators | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FP_FAST_FMAFFP_FAST_FMA(C99)(C99) | | | | | | FP_FAST_FADDFP_FAST_FADDLFP_FAST_DADDLFP_FAST_D**M**ADDD**N**")(C23)(C23)(C23)(C23) | | | | | | FP_FAST_FMULFP_FAST_FMULLFP_FAST_DMULLFP_FAST_D**M**MULD**N**")(C23)(C23)(C23)(C23) | | | | | | FP_FAST_FFMAFP_FAST_FFMALFP_FAST_DFMALFP_FAST_D**M**FMAD**N**")(C23)(C23)(C23)(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FP_FAST_FMALFP_FAST_FMAD**N**(C99)(C23) | | | | | | FP_FAST_FSUBFP_FAST_FSUBLFP_FAST_DSUBLFP_FAST_D**M**SUBD**N**")(C23)(C23)(C23)(C23) | | | | | | FP_FAST_FDIVFP_FAST_FDIVLFP_FAST_DDIVLFP_FAST_D**M**DIVD**N**")(C23)(C23)(C23)(C23) | | | | | | FP_FAST_FSQRTFP_FAST_FSQRTLFP_FAST_DSQRTLFP_FAST_D**M**SQRTD**N**")(C23)(C23)(C23)(C23) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<math.h>` |  |  |
| float       roundf( float arg ); | (1) | (since C99) |
| double      round( double arg ); | (2) | (since C99) |
| long double roundl( long double arg ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define round( arg ) | (4) | (since C99) |
| Defined in header `<math.h>` |  |  |
| long      lroundf( float arg ); | (5) | (since C99) |
| long      lround( double arg ); | (6) | (since C99) |
| long      lroundl( long double arg ); | (7) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define lround( arg ) | (8) | (since C99) |
| Defined in header `<math.h>` |  |  |
| long long llroundf( float arg ); | (9) | (since C99) |
| long long llround( double arg ); | (10) | (since C99) |
| long long llroundl( long double arg ); | (11) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define llround( arg ) | (12) | (since C99) |
|  |  |  |

1-3) Computes the nearest integer value to arg (in floating-point format), rounding halfway cases away from zero, regardless of the current rounding mode.5-7, 9-11) Computes the nearest integer value to arg (in integer format), rounding halfway cases away from zero, regardless of the current rounding mode.4,8,12) Type-generic macros: If arg has type long double, `roundl`, `lroundl`, `llroundl` is called. Otherwise, if arg has integer type or the type double, `round`, `lround`, `llround` is called. Otherwise, `roundf`, `lroundf`, `llroundf` is called, respectively.

### Parameters

|  |  |  |
| --- | --- | --- |
| arg | - | floating-point value |

### Return value

If no errors occur, the nearest integer value to arg, rounding halfway cases away from zero, is returned.

Return value!math-round away zero.svgArgument

If a domain error occurs, an implementation-defined value is returned.

### Error handling

Errors are reported as specified in `math_errhandling`.

If the result of `lround` or `llround` is outside the range representable by the return type, a domain error or a range error may occur.

If the implementation supports IEEE floating-point arithmetic (IEC 60559):

:   For the `round`, `roundf`, and `roundl` function:

    - The current rounding mode has no effect.
    - If arg is ±∞, it is returned, unmodified.
    - If arg is ±0, it is returned, unmodified.
    - If arg is NaN, NaN is returned.
:   For `lround` and `llround` families of functions:

    - FE_INEXACT is never raised.
    - The current rounding mode has no effect.
    - If arg is ±∞, FE_INVALID is raised and an implementation-defined value is returned
    - If the result of the rounding is outside the range of the return type, FE_INVALID is raised and an implementation-defined value is returned.
    - If arg is NaN, FE_INVALID is raised and an implementation-defined value is returned.

### Notes

FE_INEXACT may be (but isn't required to be) raised by `round` when rounding a non-integer finite value.

The largest representable floating-point values are exact integers in all standard floating-point formats, so `round` never overflows on its own; however the result may overflow any integer type (including intmax_t), when stored in an integer variable.

POSIX specifies that all cases where `lround` or `llround` raise FE_INVALID are domain errors.

The double version of `round` behaves as if implemented as follows:

```
#include <math.h>
#pragma STDC FENV_ACCESS ON
 
double round(double x)
{
    return signbit(x) ? ceil(x - 0.5) : floor(x + 0.5);
}

```

### Example

Run this code

```
#include <assert.h>
#include <fenv.h>
#include <float.h>
#include <limits.h>
#include <math.h>
#include <stdio.h>
// #pragma STDC FENV_ACCESS ON
 
double custom_round(double x)
{
    return signbit(x) ? ceil(x - 0.5) : floor(x + 0.5);
}
 
void test_custom_round()
{
    const double sample[] =
    {
        0.0, 2.3, 2.5 - DBL_EPSILON, 2.5, 2.5 + DBL_EPSILON, 2.7, INFINITY
    };
    for (size_t t = 0; t < sizeof sample / sizeof(double); ++t)
        assert(round(+sample[t]) == custom_round(+sample[t]) &&
               round(-sample[t]) == custom_round(-sample[t]));
}
 
int main(void)
{
    // round
    printf("round(+2.3) = %+.1f  ", round(2.3));
    printf("round(+2.5) = %+.1f  ", round(2.5));
    printf("round(+2.7) = %+.1f\n", round(2.7));
    printf("round(-2.3) = %+.1f  ", round(-2.3));
    printf("round(-2.5) = %+.1f  ", round(-2.5));
    printf("round(-2.7) = %+.1f\n", round(-2.7));
 
    printf("round(-0.0) = %+.1f\n", round(-0.0));
    printf("round(-Inf) = %+f\n",   round(-INFINITY));
 
    test_custom_round();
 
    // lround
    printf("lround(+2.3) = %+ld  ", lround(2.3));
    printf("lround(+2.5) = %+ld  ", lround(2.5));
    printf("lround(+2.7) = %+ld\n", lround(2.7));
    printf("lround(-2.3) = %+ld  ", lround(-2.3));
    printf("lround(-2.5) = %+ld  ", lround(-2.5));
    printf("lround(-2.7) = %+ld\n", lround(-2.7));
 
    printf("lround(-0.0) = %+ld\n", lround(-0.0));
    printf("lround(-Inf) = %+ld\n", lround(-INFINITY)); // FE_INVALID raised
 
    // error handling
    feclearexcept(FE_ALL_EXCEPT);
    printf("lround(LONG_MAX+1.5) = %ld\n", lround(LONG_MAX + 1.5));
    if (fetestexcept(FE_INVALID))
        puts("    FE_INVALID was raised");
}

```

Possible output:

```
round(+2.3) = +2.0  round(+2.5) = +3.0  round(+2.7) = +3.0
round(-2.3) = -2.0  round(-2.5) = -3.0  round(-2.7) = -3.0
round(-0.0) = -0.0
round(-Inf) = -inf
lround(+2.3) = +2  lround(+2.5) = +3  lround(+2.7) = +3
lround(-2.3) = -2  lround(-2.5) = -3  lround(-2.7) = -3
lround(-0.0) = +0
lround(-Inf) = -9223372036854775808
lround(LONG_MAX+1.5) = -9223372036854775808
    FE_INVALID was raised

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.12.9.6 The round functions (p: TBD)

:   - 7.12.9.7 The lround and llround functions (p: TBD)

:   - 7.25 Type-generic math <tgmath.h> (p: TBD)

:   - F.10.6.6 The round functions (p: TBD)

:   - F.10.6.7 The lround and llround functions (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.12.9.6 The round functions (p: 184)

:   - 7.12.9.7 The lround and llround functions (p: 184-185)

:   - 7.25 Type-generic math <tgmath.h> (p: 272-273)

:   - F.10.6.6 The round functions (p: 384)

:   - F.10.6.7 The lround and llround functions (p: 385)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.12.9.6 The round functions (p: 253)

:   - 7.12.9.7 The lround and llround functions (p: 253)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - F.10.6.6 The round functions (p: 527)

:   - F.10.6.7 The lround and llround functions (p: 528)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.12.9.6 The round functions (p: 233)

:   - 7.12.9.7 The lround and llround functions (p: 234)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - F.9.6.6 The round functions (p: 464)

:   - F.9.6.7 The lround and llround functions (p: 464)

### See also

|  |  |
| --- | --- |
| floorfloorffloorl(C99)(C99) | computes largest integer not greater than the given value   (function) |
| ceilceilfceill(C99)(C99) | computes smallest integer not less than the given value   (function) |
| trunctruncftruncl(C99)(C99)(C99) | rounds to nearest integer not greater in magnitude than the given value   (function) |
| C++ documentation for round | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/math/round&oldid=172059>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 May 2024, at 19:49.