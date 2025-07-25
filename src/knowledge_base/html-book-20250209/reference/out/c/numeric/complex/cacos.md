# cacosf, cacos, cacosl

From cppreference.com
< c‎ | numeric‎ | complex
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

 Complex number arithmetic

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Types and the imaginary constant | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | complex(C99) | | | | | | _Complex_I(C99) | | | | | | CMPLX(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | imaginary(C99) | | | | | | _Imaginary_I(C99) | | | | | | I(C99) | | | | | |
| Manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cimag(C99) | | | | | | creal(C99) | | | | | | carg(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cabs(C99) | | | | | | conj(C99) | | | | | | cproj(C99) | | | | | |
| Power and exponential functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cexp(C99) | | | | | | clog(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cpow(C99) | | | | | | csqrt(C99) | | | | | |
| Trigonometric functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccos(C99) | | | | | | csin(C99) | | | | | | ctan(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****cacos****(C99) | | | | | | casin(C99) | | | | | | catan(C99) | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccosh(C99) | | | | | | csinh(C99) | | | | | | ctanh(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacosh(C99) | | | | | | casinh(C99) | | | | | | catanh(C99) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex.h>` |  |  |
| float complex       cacosf( float complex z ); | (1) | (since C99) |
| double complex      cacos( double complex z ); | (2) | (since C99) |
| long double complex cacosl( long double complex z ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define acos( z ) | (4) | (since C99) |
|  |  |  |

1-3) Computes the complex arc cosine of `z` with branch cuts outside the interval [−1,+1] along the real axis.4) Type-generic macro: If `z` has type long double complex, `cacosl` is called. if `z` has type double complex, `cacos` is called, if `z` has type float complex, `cacosf` is called. If `z` is real or integer, then the macro invokes the corresponding real function (acosf, acos, acosl). If `z` is imaginary, then the macro invokes the corresponding complex number version.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex argument |

### Return value

If no errors occur, complex arc cosine of `z` is returned, in the range a strip unbounded along the imaginary axis and in the interval [0; π] along the real axis.

### Error handling and special values

Errors are reported consistent with math_errhandling.

If the implementation supports IEEE floating-point arithmetic,

- cacos(conj(z)) == conj(cacos(z))
- If `z` is `±0+0i`, the result is `π/2-0i`
- If `z` is `±0+NaNi`, the result is `π/2+NaNi`
- If `z` is `x+∞i` (for any finite x), the result is `π/2-∞i`
- If `z` is `x+NaNi` (for any nonzero finite x), the result is `NaN+NaNi` and FE_INVALID may be raised.
- If `z` is `-∞+yi` (for any positive finite y), the result is `π-∞i`
- If `z` is `+∞+yi` (for any positive finite y), the result is `+0-∞i`
- If `z` is `-∞+∞i`, the result is `3π/4-∞i`
- If `z` is `+∞+∞i`, the result is `π/4-∞i`
- If `z` is `±∞+NaNi`, the result is `NaN±∞i` (the sign of the imaginary part is unspecified)
- If `z` is `NaN+yi` (for any finite y), the result is `NaN+NaNi` and FE_INVALID may be raised
- If `z` is `NaN+∞i`, the result is `NaN-∞i`
- If `z` is `NaN+NaNi`, the result is `NaN+NaNi`

### Notes

Inverse cosine (or arc cosine) is a multivalued function and requires a branch cut on the complex plane. The branch cut is conventially placed at the line segments (-∞,-1) and (1,∞) of the real axis.

The mathematical definition of the principal value of arc cosine is acos z = 

|  |
| --- |
| 1 |
| 2 |

π + **i**ln(**i**z + √1-z2  
)

For any z, acos(z) = π - acos(-z)

### Example

Run this code

```
#include <stdio.h>
#include <math.h>
#include <complex.h>
 
int main(void)
{
    double complex z = cacos(-2);
    printf("cacos(-2+0i) = %f%+fi\n", creal(z), cimag(z));
 
    double complex z2 = cacos(conj(-2)); // or CMPLX(-2, -0.0)
    printf("cacos(-2-0i) (the other side of the cut) = %f%+fi\n", creal(z2), cimag(z2));
 
    // for any z, acos(z) = pi - acos(-z)
    double pi = acos(-1);
    double complex z3 = ccos(pi-z2);
    printf("ccos(pi - cacos(-2-0i) = %f%+fi\n", creal(z3), cimag(z3));
}

```

Output:

```
cacos(-2+0i) = 3.141593-1.316958i
cacos(-2-0i) (the other side of the cut) = 3.141593+1.316958i
ccos(pi - cacos(-2-0i) = 2.000000+0.000000i

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.5.1 The cacos functions (p: 190)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - G.6.1.1 The cacos functions (p: 539)

:   - G.7 Type-generic math <tgmath.h> (p: 545)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.5.1 The cacos functions (p: 172)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - G.6.1.1 The cacos functions (p: 474)

:   - G.7 Type-generic math <tgmath.h> (p: 480)

### See also

|  |  |
| --- | --- |
| casincasinfcasinl(C99)(C99)(C99) | computes the complex arc sine   (function) |
| catancatanfcatanl(C99)(C99)(C99) | computes the complex arc tangent   (function) |
| ccosccosfccosl(C99)(C99)(C99) | computes the complex cosine   (function) |
| acosacosfacosl(C99)(C99) | computes arc cosine (\({\small\arccos{x} }\)arccos(x))   (function) |
| C++ documentation for acos | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/cacos&oldid=136775>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 December 2021, at 06:39.