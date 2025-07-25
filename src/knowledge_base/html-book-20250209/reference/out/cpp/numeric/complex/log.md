# std::log(std::complex)

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****log**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log10 | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | exp | | | | | | |
| Power functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pow | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sqrt | | | | | | |
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
| template< class T >  std::complex<T> log( const std::complex<T>& z ); |  |  |
|  |  |  |

Computes complex natural (base **e**) logarithm of a complex value z with a branch cut along the negative real axis.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex value |

### Return value

If no errors occur, the complex natural logarithm of z is returned, in the range of a strip in the interval [−iπ, +iπ] along the imaginary axis and mathematically unbounded along the real axis.

### Error handling and special values

Errors are reported consistent with math_errhandling.

If the implementation supports IEEE floating-point arithmetic,

- The function is continuous onto the branch cut taking into account the sign of imaginary part
- std::log(std::conj(z)) == std::conj(std::log(z))
- If z is `(-0,+0)`, the result is `(-∞,π)` and FE_DIVBYZERO is raised
- If z is `(+0,+0)`, the result is `(-∞,+0)` and FE_DIVBYZERO is raised
- If z is `(x,+∞)` (for any finite x), the result is `(+∞,π/2)`
- If z is `(x,NaN)` (for any finite x), the result is `(NaN,NaN)` and FE_INVALID may be raised
- If z is `(-∞,y)` (for any finite positive y), the result is `(+∞,π)`
- If z is `(+∞,y)` (for any finite positive y), the result is `(+∞,+0)`
- If z is `(-∞,+∞)`, the result is `(+∞,3π/4)`
- If z is `(+∞,+∞)`, the result is `(+∞,π/4)`
- If z is `(±∞,NaN)`, the result is `(+∞,NaN)`
- If z is `(NaN,y)` (for any finite y), the result is `(NaN,NaN)` and FE_INVALID may be raised
- If z is `(NaN,+∞)`, the result is `(+∞,NaN)`
- If z is `(NaN,NaN)`, the result is `(NaN,NaN)`

### Notes

The natural logarithm of a complex number z with polar coordinate components (r,θ) equals ln r + i(θ+2nπ), with the principal value ln r + iθ.

The semantics of this function are intended to be consistent with the C function clog.

### Example

Run this code

```
#include <cmath>
#include <complex>
#include <iostream>
 
int main()
{
    std::complex<double> z {0.0, 1.0}; // r = 1, θ = pi / 2
    std::cout << "2 * log" << z << " = " << 2.0 * std::log(z) << '\n';
 
    std::complex<double> z2 {sqrt(2.0) / 2, sqrt(2.0) / 2}; // r = 1, θ = pi / 4
    std::cout << "4 * log" << z2 << " = " << 4.0 * std::log(z2) << '\n';
 
    std::complex<double> z3 {-1.0, 0.0}; // r = 1, θ = pi
    std::cout << "log" << z3 << " = " << std::log(z3) << '\n';
    std::complex<double> z4 {-1.0, -0.0}; // the other side of the cut
    std::cout << "log" << z4 << " (the other side of the cut) = " << std::log(z4) << '\n';
}

```

Possible output:

```
2 * log(0,1) = (0,3.14159)
4 * log(0.707107,0.707107) = (0,3.14159)
log(-1,0) = (0,3.14159)
log(-1,-0) (the other side of the cut) = (0,-3.14159)

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2597 | C++98 | specification mishandles signed zero imaginary parts | erroneous requirement removed |

### See also

|  |  |
| --- | --- |
| log10(std::complex) | complex common logarithm with the branch cuts along the negative real axis   (function template) |
| exp(std::complex) | complex base **e** exponential   (function template) |
| loglogflogl(C++11)(C++11) | computes natural (base e) logarithm (\({\small\ln{x}}\)ln(x))   (function) |
| log(std::valarray) | applies the function std::log to each element of valarray   (function template) |
| C documentation for clog | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/complex/log&oldid=150849>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 April 2023, at 23:43.