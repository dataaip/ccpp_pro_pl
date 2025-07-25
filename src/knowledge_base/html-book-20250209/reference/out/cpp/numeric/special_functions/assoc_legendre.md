# std::assoc_legendre, std::assoc_legendref, std::assoc_legendrel

From cppreference.com
< cpp‎ | numeric‎ | special functions
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

Mathematical special functions

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | assoc_laguerreassoc_laguerrefassoc_laguerrel | | | | | | ****assoc_legendreassoc_legendrefassoc_legendrel**** | | | | | | betabetafbetal | | | | | | comp_ellint_1comp_ellint_1fcomp_ellint_1l | | | | | | comp_ellint_2comp_ellint_2fcomp_ellint_2l | | | | | | comp_ellint_3comp_ellint_3fcomp_ellint_3l | | | | | | cyl_bessel_icyl_bessel_ifcyl_bessel_il | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cyl_bessel_jcyl_bessel_jfcyl_bessel_jl | | | | | | cyl_bessel_kcyl_bessel_kfcyl_bessel_kl | | | | | | cyl_neumanncyl_neumannfcyl_neumannl | | | | | | ellint_1ellint_1fellint_1l | | | | | | ellint_2ellint_2fellint_2l | | | | | | ellint_3ellint_3fellint_3l | | | | | | expintexpintfexpintl | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hermitehermitefhermitel | | | | | | laguerrelaguerreflaguerrel | | | | | | legendrelegendreflegendrel | | | | | | riemann_zetariemann_zetafriemann_zetal | | | | | | sph_besselsph_besselfsph_bessell | | | | | | sph_legendresph_legendrefsph_legendrel | | | | | | sph_neumannsph_neumannfsph_neumannl | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cmath>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| float       assoc_legendre ( unsigned int n, unsigned int m, float x );  double      assoc_legendre ( unsigned int n, unsigned int m, double x ); long double assoc_legendre ( unsigned int n, unsigned int m, long double x ); |  | (since C++17)  (until C++23) |
| /\* floating-point-type \*/ assoc_legendre( unsigned int n, unsigned int m,                                            /\* floating-point-type \*/ x ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       assoc_legendref( unsigned int n, unsigned int m, float x ); | (2) | (since C++17) |
| long double assoc_legendrel( unsigned int n, unsigned int m, long double x ); | (3) | (since C++17) |
| Additional overloads |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Integer >  double      assoc_legendre ( unsigned int n, unsigned int m, Integer x ); | (A) | (since C++17) |
|  |  |  |

1-3) Computes the Associated Legendre polynomials of the degree n, order m, and argument x. The library provides overloads of `std::assoc_legendre` for all cv-unqualified floating-point types as the type of the parameter x.(since C++23)A) Additional overloads are provided for all integer types, which are treated as double.

### Parameters

|  |  |  |
| --- | --- | --- |
| n | - | the degree of the polynomial, an unsigned integer value |
| m | - | the order of the polynomial, an unsigned integer value |
| x | - | the argument, a floating-point or integer value |

### Return value

If no errors occur, value of the associated Legendre polynomial \(\mathsf{P}_n^m\)Pm  
n of x, that is \((1 - x^2) ^ {m/2} \: \frac{ \mathsf{d} ^ m}{ \mathsf{d}x ^ m} \, \mathsf{P}_n(x)\)(1-x2  
)m/2  
 

|  |
| --- |
| dm |
| dxm |

Pn(x), is returned (where \(\mathsf{P}_n(x)\)Pn(x) is the unassociated Legendre polynomial, std::legendre(n, x)).

Note that the Condon-Shortley phase term \((-1)^m\)(-1)m  
 is omitted from this definition.

### Error handling

Errors may be reported as specified in math_errhandling

- If the argument is NaN, NaN is returned and domain error is not reported
- If |x| > 1, a domain error may occur
- If `n` is greater or equal to 128, the behavior is implementation-defined

### Notes

Implementations that do not support C++17, but support ISO 29124:2010, provide this function if `__STDCPP_MATH_SPEC_FUNCS__` is defined by the implementation to a value at least 201003L and if the user defines `__STDCPP_WANT_MATH_SPEC_FUNCS__` before including any standard library headers.

Implementations that do not support ISO 29124:2010 but support TR 19768:2007 (TR1), provide this function in the header `tr1/cmath` and namespace `std::tr1`.

An implementation of this function is also available in boost.math as `boost::math::legendre_p`, except that the boost.math definition includes the Condon-Shortley phase term.

The first few associated Legendre polynomials are:

| Function | Polynomial |
| --- | --- |
| assoc_legendre(0, 0, x) | 1 |
| assoc_legendre(1, 0, x) | x |
| assoc_legendre(1, 1, x) | (1 - x2 )1/2 |
| assoc_legendre(2, 0, x) | |  | | --- | | 1 | | 2 |  (3x2  - 1) |
| assoc_legendre(2, 1, x) | 3x(1 - x2 )1/2 |
| assoc_legendre(2, 2, x) | 3(1 - x2 ) |

The additional overloads are not required to be provided exactly as (A). They only need to be sufficient to ensure that for their argument num of integer type, std::assoc_legendre(int_num1, int_num2, num) has the same effect as std::assoc_legendre(int_num1, int_num2, static_cast<double>(num)).

### Example

Run this code

```
#include <cmath>
#include <iostream>
 
double P20(double x)
{
    return 0.5 * (3 * x * x - 1);
}
 
double P21(double x)
{
    return 3.0 * x * std::sqrt(1 - x * x);
}
 
double P22(double x)
{
    return 3 * (1 - x * x);
}
 
int main()
{
    // spot-checks
    std::cout << std::assoc_legendre(2, 0, 0.5) << '=' << P20(0.5) << '\n'
              << std::assoc_legendre(2, 1, 0.5) << '=' << P21(0.5) << '\n'
              << std::assoc_legendre(2, 2, 0.5) << '=' << P22(0.5) << '\n';
}

```

Output:

```
-0.125=-0.125
1.29904=1.29904
2.25=2.25

```

### See also

|  |  |
| --- | --- |
| legendrelegendreflegendrel(C++17)(C++17)(C++17) | Legendre polynomials   (function) |

### External links

|  |
| --- |
| Weisstein, Eric W. "Associated Legendre Polynomial." From MathWorld — A Wolfram Web Resource. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/special_functions/assoc_legendre&oldid=149536>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 March 2023, at 14:07.