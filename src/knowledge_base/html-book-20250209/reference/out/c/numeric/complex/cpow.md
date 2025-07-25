# cpowf, cpow, cpowl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cexp(C99) | | | | | | clog(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****cpow****(C99) | | | | | | csqrt(C99) | | | | | |
| Trigonometric functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccos(C99) | | | | | | csin(C99) | | | | | | ctan(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacos(C99) | | | | | | casin(C99) | | | | | | catan(C99) | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccosh(C99) | | | | | | csinh(C99) | | | | | | ctanh(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacosh(C99) | | | | | | casinh(C99) | | | | | | catanh(C99) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex.h>` |  |  |
| float complex       cpowf( float complex x, float complex y ); | (1) | (since C99) |
| double complex      cpow( double complex x, double complex y ); | (2) | (since C99) |
| long double complex cpowl( long double complex x, long double complex y ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define pow( x, y ) | (4) | (since C99) |
|  |  |  |

1-3) Computes the complex power function xy  
, with branch cut for the first parameter along the negative real axis.4) Type-generic macro: If any argument has type long double complex, `cpowl` is called. if any argument has type double complex, `cpow` is called, if any argument has type float complex, `cpowf` is called. If the arguments are real or integer, then the macro invokes the corresponding real function (powf, pow, powl). If any argument is imaginary, the corresponding complex number version is called.

### Parameters

|  |  |  |
| --- | --- | --- |
| x, y | - | complex argument |

### Return value

If no errors occur, the complex power xy  
, is returned.

Errors and special cases are handled as if the operation is implemented by cexp(y\*clog(x)), except that the implementation is allowed to treat special cases more carefully.

### Example

Run this code

```
#include <stdio.h>
#include <complex.h>
 
int main(void)
{    
    double complex z = cpow(1.0+2.0*I, 2);
    printf("(1+2i)^2 = %.1f%+.1fi\n", creal(z), cimag(z));
 
    double complex z2 = cpow(-1, 0.5);
    printf("(-1+0i)^0.5 = %.1f%+.1fi\n", creal(z2), cimag(z2));
 
    double complex z3 = cpow(conj(-1), 0.5); // other side of the cut
    printf("(-1-0i)^0.5 = %.1f%+.1fi\n", creal(z3), cimag(z3));
 
    double complex z4 = cpow(I, I); // i^i = exp(-pi/2)
    printf("i^i = %f%+fi\n", creal(z4), cimag(z4));
}

```

Output:

```
(1+2i)^2 = -3.0+4.0i
(-1+0i)^0.5 = 0.0+1.0i
(-1-0i)^0.5 = 0.0-1.0i
i^i = 0.207880+0.000000i

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.8.2 The cpow functions (p: 195-196)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - G.6.4.1 The cpow functions (p: 544)

:   - G.7 Type-generic math <tgmath.h> (p: 545)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.8.2 The cpow functions (p: 177)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - G.6.4.1 The cpow functions (p: 479)

:   - G.7 Type-generic math <tgmath.h> (p: 480)

### See also

|  |  |
| --- | --- |
| csqrtcsqrtfcsqrtl(C99)(C99)(C99) | computes the complex square root   (function) |
| powpowfpowl(C99)(C99) | computes a number raised to the given power (\(\small{x^y}\)xy)   (function) |
| C++ documentation for pow | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/cpow&oldid=77465>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 March 2015, at 06:01.