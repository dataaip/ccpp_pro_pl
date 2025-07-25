# std::pow(std::complex)

From cppreference.com
< cpp‎ | numeric‎ | complex
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

std::complex

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | complex::complex | | | | | | complex::operator= | | | | | | complex::real | | | | | | complex::imag | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | complex::operator+=complex::operator-=complex::operator\*=complex::operator/= | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+operator- | | | | | | operator+operator-operator\*operator/ | | | | | | operator==operator!=(until C++20) | | | | | | operator<<operator>> | | | | | | get(std::complex)(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | real | | | | | | imag | | | | | | abs | | | | | | arg | | | | | | norm | | | | | | conj | | | | | | proj(C++11) | | | | | | polar | | | | | | operator""ioperator""ifoperator""il(C++14)(C++14)(C++14) | | | | | |
| Exponential functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log10 | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | exp | | | | | | |
| Power functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****pow**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sqrt | | | | | | |
| Trigonometric functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sin | | | | | | cos | | | | | | tan | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asin(C++11) | | | | | | acos(C++11) | | | | | | atan(C++11) | | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asinh(C++11) | | | | | | acosh(C++11) | | | | | | atanh(C++11) | | | | | | |
| Helper types | | | | |
| tuple_size<std::complex>(C++26) | | | | |
| tuple_element<std::complex>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex>` |  |  |
| template< class T >  std::complex<T> pow( const std::complex<T>& x, int y ); | (1) | (until C++11) |
| template< class T >  std::complex<T> pow( const std::complex<T>& x, const std::complex<T>& y ); | (2) |  |
| template< class T >  std::complex<T> pow( const std::complex<T>& x, const T& y ); | (3) |  |
| template< class T >  std::complex<T> pow( const T& x, const std::complex<T>& y ); | (4) |  |
| Additional overloads (since C++11) |  |  |
| Defined in header `<complex>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (A) |  |
| template< class T1, class T2 >  std::complex</\* common-type \*/>     pow( const std::complex<T1>& x, const std::complex<T2>& y ); |  | (until C++23) |
| template< class T1, class T2 >  std::complex<std::common_type_t<T1, T2>>     pow( const std::complex<T1>& x, const std::complex<T2>& y ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
|  | (B) |  |
| template< class T, class NonComplex >  std::complex</\* common-type \*/>     pow( const std::complex<T>& x, const NonComplex& y ); |  | (until C++23) |
| template< class T, class NonComplex >  std::complex<std::common_type_t<T, NonComplex>>     pow( const std::complex<T>& x, const NonComplex& y ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
|  | (C) |  |
| template< class T, class NonComplex >  std::complex</\* common-type \*/>     pow( const NonComplex& x, const std::complex<T>& y ); |  | (until C++23) |
| template< class T, class NonComplex >  std::complex<std::common_type_t<T, NonComplex>>     pow( const NonComplex& x, const std::complex<T>& y ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

1-4) Computes complex x raised to a complex power y with a branch cut along the negative real axis for the first argument. Non-complex arguments are treated as complex numbers with positive zero imaginary component.

|  |  |
| --- | --- |
| A-C) Additional overloads are provided. `NonComplex` is not a specialization of std::complex. | (since C++11) |

### Parameters

|  |  |  |
| --- | --- | --- |
| x | - | base |
| y | - | exponent |

### Return value

1-4) If no errors occur, the complex power xy  
, is returned. Errors and special cases are handled as if the operation is implemented by std::exp(y \* std::log(x)). The result of std::pow(0, 0) is implementation-defined.A-C) Same as (2-4).

### Notes

Overload (1) was provided in C++98 to match the extra overloads (2) of std::pow. Those overloads were removed by the resolution of LWG issue 550, and overload (1) was removed by the resolution of LWG issue 844.

The additional overloads are not required to be provided exactly as (A-C). They only need to be sufficient to ensure that for their first argument base and second argument exponent:

|  |  |
| --- | --- |
| If base and/or exponent has type std::complex<T>:   - If base and/or exponent has type std::complex<long double> or long double, then `std::pow(base, exponent)` has the same effect as `std::pow`(std::complex<long double>(base),          std::complex<long double>(exponent)). - Otherwise, if base and/or exponent has type std::complex<double>, double, or an integer type, then `std::pow(base, exponent)` has the same effect as `std::pow`(std::complex<double>(base),          std::complex<double>(exponent)). - Otherwise, if base and/or exponent has type std::complex<float> or float, then `std::pow(base, exponent)` has the same effect as `std::pow`(std::complex<float>(base),          std::complex<float>(exponent)). | (until C++23) |
| If one argument has type std::complex<T1> and the other argument has type `T2` or std::complex<T2>, then `std::pow(base, exponent)` has the same effect as `std::pow`(std::complex<std::common_type_t<T1, T2>>(base),           std::complex<std::common_type_t<T1, T2>>(exponent)).  If std::common_type_t<T1, T2> is not well-formed, then the program is ill-formed. | (since C++23) |

### Example

Run this code

```
#include <complex>
#include <iostream>
 
int main()
{
    std::cout << std::fixed;
 
    std::complex<double> z(1.0, 2.0);
    std::cout << "(1,2)^2 = " << std::pow(z, 2) << '\n';
 
    std::complex<double> z2(-1.0, 0.0); // square root of -1
    std::cout << "-1^0.5 = " << std::pow(z2, 0.5) << '\n';
 
    std::complex<double> z3(-1.0, -0.0); // other side of the cut
    std::cout << "(-1,-0)^0.5 = " << std::pow(z3, 0.5) << '\n';
 
    std::complex<double> i(0.0, 1.0); // i^i = exp(-pi / 2)
    std::cout << "i^i = " << std::pow(i, i) << '\n';
}

```

Output:

```
(1,2)^2 = (-3.000000,4.000000)
-1^0.5 = (0.000000,1.000000)
(-1,-0)^0.5 = (0.000000,-1.000000)
i^i = (0.207880,0.000000)

```

### See also

|  |  |
| --- | --- |
| sqrt(std::complex) | complex square root in the range of the right half-plane   (function template) |
| powpowfpowl(C++11)(C++11) | raises a number to the given power (\(\small{x^y}\)xy)   (function) |
| pow(std::valarray) | applies the function std::pow to two valarrays or a valarray and a value   (function template) |
| C documentation for cpow | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/complex/pow&oldid=152476>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 May 2023, at 00:50.