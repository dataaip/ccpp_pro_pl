# ccosf, ccos, ccosl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****ccos****(C99) | | | | | | csin(C99) | | | | | | ctan(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacos(C99) | | | | | | casin(C99) | | | | | | catan(C99) | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccosh(C99) | | | | | | csinh(C99) | | | | | | ctanh(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacosh(C99) | | | | | | casinh(C99) | | | | | | catanh(C99) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex.h>` |  |  |
| float complex       ccosf( float complex z ); | (1) | (since C99) |
| double complex      ccos( double complex z ); | (2) | (since C99) |
| long double complex ccosl( long double complex z ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define cos( z ) | (4) | (since C99) |
|  |  |  |

1-3) Computes the complex cosine of `z`.4) Type-generic macro: If `z` has type long double complex, `ccosl` is called. if `z` has type double complex, `ccos` is called, if `z` has type float complex, `ccosf` is called. If `z` is real or integer, then the macro invokes the corresponding real function (cosf, cos, cosl). If `z` is imaginary, then the macro invokes the corresponding real version of the function cosh, implementing the formula cos(iy) = cosh(y), and the return type is real.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex argument |

### Return value

If no errors occur, the complex cosine of `z` is returned.

Errors and special cases are handled as if the operation is implemented by ccosh(I\*z).

### Notes

The cosine is an entire function on the complex plane, and has no branch cuts.

Mathematical definition of the cosine is cos z = 

|  |
| --- |
| eiz +e-iz |
| 2 |

### Example

Run this code

```
#include <stdio.h>
#include <math.h>
#include <complex.h>
 
int main(void)
{
    double complex z = ccos(1);  // behaves like real cosine along the real line
    printf("cos(1+0i) = %f%+fi ( cos(1)=%f)\n", creal(z), cimag(z), cos(1));
 
    double complex z2 = ccos(I); // behaves like real cosh along the imaginary line
    printf("cos(0+1i) = %f%+fi (cosh(1)=%f)\n", creal(z2), cimag(z2), cosh(1));
}

```

Output:

```
cos(1+0i) = 0.540302-0.000000i ( cos(1)=0.540302)
cos(0+1i) = 1.543081-0.000000i (cosh(1)=1.543081)

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.5.4 The ccos functions (p: 191)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - G.7 Type-generic math <tgmath.h> (p: 545)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.5.4 The ccos functions (p: 173)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - G.7 Type-generic math <tgmath.h> (p: 480)

### See also

|  |  |
| --- | --- |
| csincsinfcsinl(C99)(C99)(C99) | computes the complex sine   (function) |
| ctanctanfctanl(C99)(C99)(C99) | computes the complex tangent   (function) |
| cacoscacosfcacosl(C99)(C99)(C99) | computes the complex arc cosine   (function) |
| coscosfcosl(C99)(C99) | computes cosine (\({\small\cos{x} }\)cos(x))   (function) |
| C++ documentation for cos | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/ccos&oldid=77483>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 March 2015, at 06:35.