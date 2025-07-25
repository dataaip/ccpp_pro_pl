# std::cyl_bessel_k, std::cyl_bessel_kf, std::cyl_bessel_kl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | assoc_laguerreassoc_laguerrefassoc_laguerrel | | | | | | assoc_legendreassoc_legendrefassoc_legendrel | | | | | | betabetafbetal | | | | | | comp_ellint_1comp_ellint_1fcomp_ellint_1l | | | | | | comp_ellint_2comp_ellint_2fcomp_ellint_2l | | | | | | comp_ellint_3comp_ellint_3fcomp_ellint_3l | | | | | | cyl_bessel_icyl_bessel_ifcyl_bessel_il | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cyl_bessel_jcyl_bessel_jfcyl_bessel_jl | | | | | | ****cyl_bessel_kcyl_bessel_kfcyl_bessel_kl**** | | | | | | cyl_neumanncyl_neumannfcyl_neumannl | | | | | | ellint_1ellint_1fellint_1l | | | | | | ellint_2ellint_2fellint_2l | | | | | | ellint_3ellint_3fellint_3l | | | | | | expintexpintfexpintl | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hermitehermitefhermitel | | | | | | laguerrelaguerreflaguerrel | | | | | | legendrelegendreflegendrel | | | | | | riemann_zetariemann_zetafriemann_zetal | | | | | | sph_besselsph_besselfsph_bessell | | | | | | sph_legendresph_legendrefsph_legendrel | | | | | | sph_neumannsph_neumannfsph_neumannl | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cmath>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| float       cyl_bessel_k ( float nu, float x );  double      cyl_bessel_k ( double nu, double x ); long double cyl_bessel_k ( long double nu, long double x ); |  | (since C++17)  (until C++23) |
| /\* floating-point-type \*/ cyl_bessel_k( /\* floating-point-type \*/ nu,                                          /\* floating-point-type \*/ x ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       cyl_bessel_kf( float nu, float x ); | (2) | (since C++17) |
| long double cyl_bessel_kl( long double nu, long double x ); | (3) | (since C++17) |
| Additional overloads |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Arithmetic1, class Arithmetic2 >  /\* common-floating-point-type \*/     cyl_bessel_k( Arithmetic1 nu, Arithmetic2 x ); | (A) | (since C++17) |
|  |  |  |

1-3) Computes the irregular modified cylindrical Bessel function (also known as modified Bessel function of the second kind) of nu and x. The library provides overloads of `std::cyl_bessel_k` for all cv-unqualified floating-point types as the type of the parameters nu and x.(since C++23)A) Additional overloads are provided for all other combinations of arithmetic types.

### Parameters

|  |  |  |
| --- | --- | --- |
| nu | - | the order of the function |
| x | - | the argument of the function |

### Return value

If no errors occur, value of the irregular modified cylindrical Bessel function (modified Bessel function of the second kind) of nu and x, is returned, that is Knu(x) = 

|  |
| --- |
| π |
| 2 |

|  |
| --- |
| I-nu(x)-Inu(x) |
| sin(nuπ) |

 (where Inu(x) is std::cyl_bessel_i(nu, x)) for x≥0 and non-integer nu; for integer nu a limit is used.

### Error handling

Errors may be reported as specified in math_errhandling:

- If the argument is NaN, NaN is returned and domain error is not reported.
- If nu≥128, the behavior is implementation-defined.

### Notes

Implementations that do not support C++17, but support ISO 29124:2010, provide this function if `__STDCPP_MATH_SPEC_FUNCS__` is defined by the implementation to a value at least 201003L and if the user defines `__STDCPP_WANT_MATH_SPEC_FUNCS__` before including any standard library headers.

Implementations that do not support ISO 29124:2010 but support TR 19768:2007 (TR1), provide this function in the header `tr1/cmath` and namespace `std::tr1`.

An implementation of this function is also available in boost.math.

The additional overloads are not required to be provided exactly as (A). They only need to be sufficient to ensure that for their first argument num1 and second argument num2:

|  |  |
| --- | --- |
| - If num1 or num2 has type long double, then std::cyl_bessel_k(num1, num2) has the same effect as std::cyl_bessel_k(static_cast<long double>(num1),                   static_cast<long double>(num2)). - Otherwise, if num1 and/or num2 has type double or an integer type, then std::cyl_bessel_k(num1, num2) has the same effect as std::cyl_bessel_k(static_cast<double>(num1),                   static_cast<double>(num2)). - Otherwise, if num1 or num2 has type float, then std::cyl_bessel_k(num1, num2) has the same effect as std::cyl_bessel_k(static_cast<float>(num1),                   static_cast<float>(num2)). | (until C++23) |
| If num1 and num2 have arithmetic types, then std::cyl_bessel_k(num1, num2) has the same effect as std::cyl_bessel_k(static_cast</\* common-floating-point-type \*/>(num1),                   static_cast</\* common-floating-point-type \*/>(num2)), where /\* common-floating-point-type \*/ is the floating-point type with the greatest floating-point conversion rank and greatest floating-point conversion subrank between the types of num1 and num2, arguments of integer type are considered to have the same floating-point conversion rank as double.  If no such floating-point type with the greatest rank and subrank exists, then overload resolution does not result in a usable candidate from the overloads provided. | (since C++23) |

### Example

Run this code

```
#include <cmath>
#include <iostream>
#include <numbers>
 
int main()
{
    double pi = std::numbers::pi;
    const double x = 1.2345;
 
    // spot check for nu == 0.5
    std::cout << "K_.5(" << x << ") = " << std::cyl_bessel_k(.5, x) << '\n'
              << "calculated via I = "
              << (pi / 2) * (std::cyl_bessel_i(-.5, x)
                 - std::cyl_bessel_i(.5, x)) / std::sin(.5 * pi) << '\n';
}

```

Output:

```
K_.5(1.2345) = 0.32823
calculated via I = 0.32823

```

### See also

|  |  |
| --- | --- |
| cyl_bessel_icyl_bessel_ifcyl_bessel_il(C++17)(C++17)(C++17) | regular modified cylindrical Bessel functions   (function) |
| cyl_bessel_jcyl_bessel_jfcyl_bessel_jl(C++17)(C++17)(C++17) | cylindrical Bessel functions (of the first kind)   (function) |

### External links

|  |
| --- |
| Weisstein, Eric W. "Modified Bessel Function of the Second Kind." From MathWorld — A Wolfram Web Resource. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/special_functions/cyl_bessel_k&oldid=149512>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 March 2023, at 22:59.