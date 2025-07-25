# cabsf, cabs, cabsl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cimag(C99) | | | | | | creal(C99) | | | | | | carg(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****cabs****(C99) | | | | | | conj(C99) | | | | | | cproj(C99) | | | | | |
| Power and exponential functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cexp(C99) | | | | | | clog(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cpow(C99) | | | | | | csqrt(C99) | | | | | |
| Trigonometric functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccos(C99) | | | | | | csin(C99) | | | | | | ctan(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacos(C99) | | | | | | casin(C99) | | | | | | catan(C99) | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccosh(C99) | | | | | | csinh(C99) | | | | | | ctanh(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacosh(C99) | | | | | | casinh(C99) | | | | | | catanh(C99) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex.h>` |  |  |
| float       cabsf( float complex z ); | (1) | (since C99) |
| double      cabs( double complex z ); | (2) | (since C99) |
| long double cabsl( long double complex z ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define fabs( z ) | (4) | (since C99) |
|  |  |  |

1-3) Computes the complex absolute value (also known as norm, modulus, or magnitude) of `z`.4) Type-generic macro: if `z` has type long double complex or long double imaginary, `cabsl` is called. If `z` has type float complex or float imaginary, `cabsf` is called. If `z` has type double complex or double imaginary, `cabs` is called. For real and integer types, the corresponding version of fabs is called.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex argument |

### Return value

If no errors occur, returns the absolute value (norm, magnitude) of `z`.

Errors and special cases are handled as if the function is implemented as hypot(creal(z), cimag(z))

### Example

Run this code

```
#include <stdio.h>
#include <complex.h>
 
int main(void)
{
    double complex z = 1.0 + 1.0*I;
    printf("%.1f%+.1fi cartesian is rho=%f theta=%f polar\n",
           creal(z), cimag(z), cabs(z), carg(z));
}

```

Output:

```
1.0+1.0i cartesian is rho=1.414214 theta=0.785398 polar

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.8.1 The cabs functions (p: 195)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - G.7 Type-generic math <tgmath.h> (p: 545)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.8.1 The cabs functions (p: 177)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - G.7 Type-generic math <tgmath.h> (p: 480)

### See also

|  |  |
| --- | --- |
| cargcargfcargl(C99)(C99)(C99) | computes the phase angle of a complex number   (function) |
| abslabsllabs(C99) | computes absolute value of an integral value (\(\small{|x|}\)|x|)   (function) |
| fabsfabsffabsl(C99)(C99) | computes absolute value of a floating-point value (\(\small{|x|}\)|x|)   (function) |
| hypothypotfhypotl(C99)(C99)(C99) | computes square root of the sum of the squares of two given numbers (\(\scriptsize{\sqrt{x^2+y^2} }\)√x2 +y2 )   (function) |
| C++ documentation for abs | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/cabs&oldid=77459>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 March 2015, at 05:45.