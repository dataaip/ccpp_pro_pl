# std::atanh(std::complex)

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
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pow | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sqrt | | | | | | |
| Trigonometric functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sin | | | | | | cos | | | | | | tan | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asin(C++11) | | | | | | acos(C++11) | | | | | | atan(C++11) | | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asinh(C++11) | | | | | | acosh(C++11) | | | | | | ****atanh****(C++11) | | | | | | |
| Helper types | | | | |
| tuple_size<std::complex>(C++26) | | | | |
| tuple_element<std::complex>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex>` |  |  |
| template< class T >   complex<T> atanh( const complex<T>& z ); |  | (since C++11) |
|  |  |  |

Computes the complex arc hyperbolic tangent of z with branch cuts outside the interval [−1; +1] along the real axis.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex value |

### Return value

If no errors occur, the complex arc hyperbolic tangent of z is returned, in the range of a half-strip mathematically unbounded along the real axis and in the interval [−iπ/2; +iπ/2] along the imaginary axis.

### Error handling and special values

Errors are reported consistent with math_errhandling.

If the implementation supports IEEE floating-point arithmetic,

- std::atanh(std::conj(z)) == std::conj(std::atanh(z))
- std::atanh(-z) == -std::atanh(z)
- If z is `(+0,+0)`, the result is `(+0,+0)`
- If z is `(+0,NaN)`, the result is `(+0,NaN)`
- If z is `(+1,+0)`, the result is `(+∞,+0)` and FE_DIVBYZERO is raised
- If z is `(x,+∞)` (for any finite positive x), the result is `(+0,π/2)`
- If z is `(x,NaN)` (for any finite nonzero x), the result is `(NaN,NaN)` and FE_INVALID may be raised
- If z is `(+∞,y)` (for any finite positive y), the result is `(+0,π/2)`
- If z is `(+∞,+∞)`, the result is `(+0,π/2)`
- If z is `(+∞,NaN)`, the result is `(+0,NaN)`
- If z is `(NaN,y)` (for any finite y), the result is `(NaN,NaN)` and FE_INVALID may be raised
- If z is `(NaN,+∞)`, the result is `(±0,π/2)` (the sign of the real part is unspecified)
- If z is `(NaN,NaN)`, the result is `(NaN,NaN)`

### Notes

Although the C++ standard names this function "complex arc hyperbolic tangent", the inverse functions of the hyperbolic functions are the area functions. Their argument is the area of a hyperbolic sector, not an arc. The correct name is "complex inverse hyperbolic tangent", and, less common, "complex area hyperbolic tangent".

Inverse hyperbolic tangent is a multivalued function and requires a branch cut on the complex plane. The branch cut is conventionally placed at the line segments (-∞,-1] and +1,+∞) of the real axis.

The mathematical definition of the principal value of the inverse hyperbolic tangent is atanh z = 

|  |
| --- |
| ln(1+z) - ln(1-z) |
| 2 |

.  
For any z, atanh(z) = 

|  |
| --- |
| atan(iz) |
| i |

.

### Example

Run this code

```
#include <complex>
#include <iostream>
 
int main()
{
    std::cout << std::fixed;
    std::complex<double> z1(2.0, 0.0);
    std::cout << "atanh" << z1 << " = " << std::atanh(z1) << '\n';
 
    std::complex<double> z2(2.0, -0.0);
    std::cout << "atanh" << z2 << " (the other side of the cut) = "
              << std::atanh(z2) << '\n';
 
    // for any z, atanh(z) = atanh(iz) / i
    std::complex<double> z3(1.0, 2.0);
    std::complex<double> i(0.0, 1.0);
    std::cout << "atanh" << z3 << " = " << std::atanh(z3) << '\n'
              << "atan" << z3 * i << " / i = " << std::atan(z3 * i) / i << '\n';
}

```

Output:

```
atanh(2.000000,0.000000) = (0.549306,1.570796)
atanh(2.000000,-0.000000) (the other side of the cut) = (0.549306,-1.570796)
atanh(1.000000,2.000000) = (0.173287,1.178097)
atan(-2.000000,1.000000) / i = (0.173287,1.178097)

```

### See also

|  |  |
| --- | --- |
| [asinh(std::complex)(C++11) | computes area hyperbolic sine of a complex number (\({\small\operatorname{arsinh}{z}}\)arsinh(z))   (function template) |
| acosh(std::complex)(C++11) | computes area hyperbolic cosine of a complex number (\({\small\operatorname{arcosh}{z}}\)arcosh(z))   (function template) |
| tanh(std::complex) | computes hyperbolic tangent of a complex number (\({\small\tanh{z}}\)tanh(z))   (function template) |
| atanhatanhfatanhl(C++11)(C++11)(C++11) | computes the inverse hyperbolic tangent (\({\small\operatorname{artanh}{x}}\)artanh(x))   (function) |
| C documentation for catanh | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/complex/atanh&oldid=150833>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 April 2023, at 12:10.