# std::beta, std::betaf, std::betal

From cppreference.com
< cpp‎ | experimental‎ | special functions
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Mathematical special functions

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | assoc_laguerreassoc_laguerrefassoc_laguerrel | | | | | | assoc_legendreassoc_legendrefassoc_legendrel | | | | | | ****betabetafbetal**** | | | | | | comp_ellint_1comp_ellint_1fcomp_ellint_1l | | | | | | comp_ellint_2comp_ellint_2fcomp_ellint_2l | | | | | | comp_ellint_3comp_ellint_3fcomp_ellint_3l | | | | | | cyl_bessel_icyl_bessel_ifcyl_bessel_il") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cyl_bessel_jcyl_bessel_jfcyl_bessel_jl") | | | | | | cyl_bessel_kcyl_bessel_kfcyl_bessel_kl") | | | | | | cyl_neumanncyl_neumannfcyl_neumannl") | | | | | | ellint_1ellint_1fellint_1l") | | | | | | ellint_2ellint_2fellint_2l") | | | | | | ellint_3ellint_3fellint_3l") | | | | | | expintexpintfexpintl | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hermitehermitefhermitel | | | | | | laguerrelaguerreflaguerrel | | | | | | legendrelegendreflegendrel | | | | | | riemann_zetariemann_zetafriemann_zetal | | | | | | sph_besselsph_besselfsph_bessell") | | | | | | sph_legendresph_legendrefsph_legendrel") | | | | | | sph_neumannsph_neumannfsph_neumannl") | | | | | |

|  |  |  |
| --- | --- | --- |
| double      beta( double x, double y );  float       betaf( float x, float y ); long double betal( long double x, long double y ); | (1) |  |
| Promoted    beta( Arithmetic x, Arithmetic y ); | (2) |  |
|  |  |  |

1) Computes the beta function of x and y.2) A set of overloads or a function template for all combinations of arguments of arithmetic type not covered by (1). If any argument has integral type, it is cast to double. If any argument is long double, then the return type `Promoted` is also long double, otherwise the return type is always double.

As all special functions, `beta` is only guaranteed to be available in `<cmath>` if `__STDCPP_MATH_SPEC_FUNCS__` is defined by the implementation to a value at least 201003L and if the user defines `__STDCPP_WANT_MATH_SPEC_FUNCS__` before including any standard library headers.

### Parameters

|  |  |  |
| --- | --- | --- |
| x, y | - | values of a floating-point or integral type |

### Return value

If no errors occur, value of the beta function of x and y, that is ∫1  
0tx-1  
(1 - t)(y-1)  
d**t**, or, equivalently, 

|  |
| --- |
| Γ(x)Γ(y) |
| Γ(x + y) |

 is returned.

### Error handling

Errors may be reported as specified in math_errhandling.

- If any argument is NaN, NaN is returned and domain error is not reported.
- The function is only required to be defined where both x and y are greater than zero, and is allowed to report a domain error otherwise.

### Notes

Implementations that do not support TR 29124 but support TR 19768, provide this function in the header `tr1/cmath` and namespace `std::tr1`.

An implementation of this function is also available in boost.math.

beta(x, y) equals beta(y, x).

When x and y are positive integers, beta(x, y) equals \(\frac{(x - 1)!(y - 1)!}{(x + y - 1)!}\)

|  |
| --- |
| (x - 1)!(y - 1)! |
| (x + y - 1)! |

.
Binomial coefficients can be expressed in terms of the beta function: \(\binom{n}{k} = \frac{1}{(n + 1)B(n - k + 1, k + 1)}\)⎛  
⎜  
⎝n  
k⎞  
⎟  
⎠=

|  |
| --- |
| 1 |
| (n + 1)Β(n - k + 1, k + 1) |

.

### Example

(works as shown with gcc 6.0)

Run this code

```
#define __STDCPP_WANT_MATH_SPEC_FUNCS__ 1
#include <cmath>
#include <iomanip>
#include <iostream>
#include <string>
 
double binom(int n, int k)
{
    return 1 / ((n + 1) * std::beta(n - k + 1, k + 1));
}
 
int main()
{
    std::cout << "Pascal's triangle:\n";
    for (int n = 1; n < 10; ++n)
    {
        std::cout << std::string(20 - n * 2, ' ');
        for (int k = 1; k < n; ++k)
            std::cout << std::setw(3) << binom(n, k) << ' ';
        std::cout << '\n';
    }
}

```

Output:

```
Pascal's triangle:
 
                  2 
                3   3 
              4   6   4 
            5  10  10   5 
          6  15  20  15   6 
        7  21  35  35  21   7 
      8  28  56  70  56  28   8 
    9  36  84 126 126  84  36   9

```

### See also

|  |  |
| --- | --- |
| tgammatgammaftgammal(C++11)(C++11)(C++11) | gamma function   (function) |

### External links

Weisstein, Eric W. "Beta Function." From MathWorld--A Wolfram Web Resource.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/special_functions/beta&oldid=158794>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 September 2023, at 10:37.