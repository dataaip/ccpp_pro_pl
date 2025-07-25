# complex

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****complex****(C99) | | | | | | _Complex_I(C99) | | | | | | CMPLX(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | imaginary(C99) | | | | | | _Imaginary_I(C99) | | | | | | I(C99) | | | | | |
| Manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cimag(C99) | | | | | | creal(C99) | | | | | | carg(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cabs(C99) | | | | | | conj(C99) | | | | | | cproj(C99) | | | | | |
| Power and exponential functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cexp(C99) | | | | | | clog(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cpow(C99) | | | | | | csqrt(C99) | | | | | |
| Trigonometric functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccos(C99) | | | | | | csin(C99) | | | | | | ctan(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacos(C99) | | | | | | casin(C99) | | | | | | catan(C99) | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccosh(C99) | | | | | | csinh(C99) | | | | | | ctanh(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacosh(C99) | | | | | | casinh(C99) | | | | | | catanh(C99) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex.h>` |  |  |
| #define complex _Complex |  | (since C99) |
|  |  |  |

This macro expands to a type specifier used to identify complex types.

A program may undefine and perhaps then redefine the `complex` macro.

### Example

Run this code

```
#include <complex.h>
#include <math.h>
#include <stdio.h>
 
void print_complex(const char* note, complex z)
{
    printf("%s %f%+f*i\n", note, creal(z), cimag(z));
}
 
int main(void)
{
    double complex z = -1.0 + 2.0*I;
    print_complex("z  =", z);
    print_complex("z\u00B2 =", z * z);
    double complex z2 = ccos(2.0 * carg(z)) + csin(2.0 * carg(z))*I;
    print_complex("z\u00B2 =", cabs(z) * cabs(z) * z2);
}

```

Output:

```
z  = -1.000000+2.000000*i
z² = -3.000000-4.000000*i
z² = -3.000000-4.000000*i

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.3.1/4 complex (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.3.1/4 complex (p: 136)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.1/4 complex (p: 188)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.1/2 complex (p: 170)

### See also

|  |  |
| --- | --- |
| imaginary(C99) | imaginary type macro   (keyword macro) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/complex&oldid=169480>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 February 2024, at 12:40.