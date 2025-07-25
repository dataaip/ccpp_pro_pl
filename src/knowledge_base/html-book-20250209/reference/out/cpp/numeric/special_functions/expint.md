# std::expint, std::expintf, std::expintl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | assoc_laguerreassoc_laguerrefassoc_laguerrel | | | | | | assoc_legendreassoc_legendrefassoc_legendrel | | | | | | betabetafbetal | | | | | | comp_ellint_1comp_ellint_1fcomp_ellint_1l | | | | | | comp_ellint_2comp_ellint_2fcomp_ellint_2l | | | | | | comp_ellint_3comp_ellint_3fcomp_ellint_3l | | | | | | cyl_bessel_icyl_bessel_ifcyl_bessel_il | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cyl_bessel_jcyl_bessel_jfcyl_bessel_jl | | | | | | cyl_bessel_kcyl_bessel_kfcyl_bessel_kl | | | | | | cyl_neumanncyl_neumannfcyl_neumannl | | | | | | ellint_1ellint_1fellint_1l | | | | | | ellint_2ellint_2fellint_2l | | | | | | ellint_3ellint_3fellint_3l | | | | | | ****expintexpintfexpintl**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hermitehermitefhermitel | | | | | | laguerrelaguerreflaguerrel | | | | | | legendrelegendreflegendrel | | | | | | riemann_zetariemann_zetafriemann_zetal | | | | | | sph_besselsph_besselfsph_bessell | | | | | | sph_legendresph_legendrefsph_legendrel | | | | | | sph_neumannsph_neumannfsph_neumannl | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cmath>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| float       expint ( float num );  double      expint ( double num ); long double expint ( long double num ); |  | (since C++17)  (until C++23) |
| /\* floating-point-type \*/ expint( /\* floating-point-type \*/ num ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       expintf( float num ); | (2) | (since C++17) |
| long double expintl( long double num ); | (3) | (since C++17) |
| Additional overloads |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Integer >  double      expint ( Integer num ); | (A) | (since C++17) |
|  |  |  |

1-3) Computes the Exponential integral of num. The library provides overloads of `std::expint` for all cv-unqualified floating-point types as the type of the parameter num.(since C++23)A) Additional overloads are provided for all integer types, which are treated as double.

### Parameters

|  |  |  |
| --- | --- | --- |
| num | - | floating-point or integer value |

### Return value

If no errors occur, value of the exponential integral of num, that is -∫∞  
-num

|  |
| --- |
| **e**-t |
| t |

d**t**, is returned.

### Error handling

Errors may be reported as specified in math_errhandling.

- If the argument is NaN, NaN is returned and domain error is not reported.
- If the argument is ±0, -∞ is returned.

### Notes

Implementations that do not support C++17, but support ISO 29124:2010, provide this function if `__STDCPP_MATH_SPEC_FUNCS__` is defined by the implementation to a value at least 201003L and if the user defines `__STDCPP_WANT_MATH_SPEC_FUNCS__` before including any standard library headers.

Implementations that do not support ISO 29124:2010 but support TR 19768:2007 (TR1), provide this function in the header `tr1/cmath` and namespace `std::tr1`.

An implementation of this function is also available in boost.math.

The additional overloads are not required to be provided exactly as (A). They only need to be sufficient to ensure that for their argument num of integer type, std::expint(num) has the same effect as std::expint(static_cast<double>(num)).

### Example

Run this code

```
#include <algorithm>
#include <cmath>
#include <iostream>
#include <vector>
 
template<int Height = 5, int BarWidth = 1, int Padding = 1, int Offset = 0, class Seq>
void draw_vbars(Seq&& s, const bool DrawMinMax = true)
{
    static_assert(0 < Height and 0 < BarWidth and 0 <= Padding and 0 <= Offset);
 
    auto cout_n = [](auto&& v, int n = 1)
    {
        while (n-- > 0)
            std::cout << v;
    };
 
    const auto [min, max] = std::minmax_element(std::cbegin(s), std::cend(s));
 
    std::vector<std::div_t> qr;
    for (typedef decltype(*std::cbegin(s)) V; V e : s)
        qr.push_back(std::div(std::lerp(V(0), 8 * Height,
                                        (e - *min) / (*max - *min)), 8));
 
    for (auto h{Height}; h-- > 0; cout_n('\n'))
    {
        cout_n(' ', Offset);
 
        for (auto dv : qr)
        {
            const auto q{dv.quot}, r{dv.rem};
            unsigned char d[]{0xe2, 0x96, 0x88, 0}; // Full Block: '█'
            q < h ? d[0] = ' ', d[1] = 0 : q == h ? d[2] -= (7 - r) : 0;
            cout_n(d, BarWidth), cout_n(' ', Padding);
        }
 
        if (DrawMinMax && Height > 1)
            Height - 1 == h ? std::cout << "┬ " << *max:
                          h ? std::cout << "│ "
                            : std::cout << "┴ " << *min;
    }
}
 
int main()
{
    std::cout << "Ei(0) = " << std::expint(0) << '\n'
              << "Ei(1) = " << std::expint(1) << '\n'
              << "Gompertz constant = " << -std::exp(1) * std::expint(-1) << '\n';
 
    std::vector<float> v;
    for (float x{1.f}; x < 8.8f; x += 0.3565f)
        v.push_back(std::expint(x));
    draw_vbars<9, 1, 1>(v);
}

```

Output:

```
Ei(0) = -inf
Ei(1) = 1.89512
Gompertz constant = 0.596347
                                          █ ┬ 666.505
                                          █ │
                                        ▆ █ │
                                        █ █ │
                                      █ █ █ │
                                    ▆ █ █ █ │
                                ▁ ▆ █ █ █ █ │
                            ▂ ▅ █ █ █ █ █ █ │
▁ ▁ ▁ ▁ ▁ ▁ ▁ ▂ ▂ ▃ ▃ ▄ ▆ ▇ █ █ █ █ █ █ █ █ ┴ 1.89512

```

### External links

|  |
| --- |
| Weisstein, Eric W. "Exponential Integral." From MathWorld — A Wolfram Web Resource. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/special_functions/expint&oldid=160790>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 October 2023, at 23:38.