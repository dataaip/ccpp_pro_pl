# std::complex<T>::operator+=,-=,\*=,/=

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | complex::complex | | | | | | complex::operator= | | | | | | complex::real | | | | | | complex::imag | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****complex::operator+=complex::operator-=complex::operator\*=complex::operator/=**** | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+operator- | | | | | | operator+operator-operator\*operator/ | | | | | | operator==operator!=(until C++20) | | | | | | operator<<operator>> | | | | | | get(std::complex)(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | real | | | | | | imag | | | | | | abs | | | | | | arg | | | | | | norm | | | | | | conj | | | | | | proj(C++11) | | | | | | polar | | | | | | operator""ioperator""ifoperator""il(C++14)(C++14)(C++14) | | | | | |
| Exponential functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log10 | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | exp | | | | | | |
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
| Primary template `complex<T>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| complex& operator+=( const T& other ); |  | (until C++20) |
| constexpr complex& operator+=( const T& other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| complex& operator-=( const T& other ); |  | (until C++20) |
| constexpr complex& operator-=( const T& other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| complex& operator\*=( const T& other ); |  | (until C++20) |
| constexpr complex& operator\*=( const T& other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| complex& operator/=( const T& other ); |  | (until C++20) |
| constexpr complex& operator/=( const T& other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
| Specialization `complex<float>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| complex& operator+=( float other ); |  | (until C++20) |
| constexpr complex& operator+=( float other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| complex& operator-=( float other ); |  | (until C++20) |
| constexpr complex& operator-=( float other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| complex& operator\*=( float other ); |  | (until C++20) |
| constexpr complex& operator\*=( float other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| complex& operator/=( float other ); |  | (until C++20) |
| constexpr complex& operator/=( float other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
| Specialization `complex<double>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| complex& operator+=( double other ); |  | (until C++20) |
| constexpr complex& operator+=( double other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| complex& operator-=( double other ); |  | (until C++20) |
| constexpr complex& operator-=( double other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| complex& operator\*=( double other ); |  | (until C++20) |
| constexpr complex& operator\*=( double other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| complex& operator/=( double other ); |  | (until C++20) |
| constexpr complex& operator/=( double other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
| Specialization `complex<long double>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| complex& operator+=( long double other ); |  | (until C++20) |
| constexpr complex& operator+=( long double other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| complex& operator-=( long double other ); |  | (until C++20) |
| constexpr complex& operator-=( long double other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| complex& operator\*=( long double other ); |  | (until C++20) |
| constexpr complex& operator\*=( long double other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| complex& operator/=( long double other ); |  | (until C++20) |
| constexpr complex& operator/=( long double other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
| All specializations |  |  |
|  |  |  |
| --- | --- | --- |
|  | (5) |  |
| template<class X>  complex& operator+=( const std::complex<X>& other ); |  | (until C++20) |
| template<class X>  constexpr complex& operator+=( const std::complex<X>& other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (6) |  |
| template<class X>  complex& operator-=( const std::complex<X>& other ); |  | (until C++20) |
| template<class X>  constexpr complex& operator-=( const std::complex<X>& other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (7) |  |
| template<class X>  complex& operator\*=( const std::complex<X>& other ); |  | (until C++20) |
| template<class X>  constexpr complex& operator\*=( const std::complex<X>& other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (8) |  |
| template<class X>  complex& operator/=( const std::complex<X>& other ); |  | (until C++20) |
| template<class X>  constexpr complex& operator/=( const std::complex<X>& other ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Implements the compound assignment operators for complex arithmetic and for mixed complex/scalar arithmetic. Scalar arguments are treated as complex numbers with the real part equal to the argument and the imaginary part set to zero.

1,5) Adds `other` to \*this.2,6) Subtracts `other` from \*this.3,7) Multiplies \*this by `other`.4,8) Divides \*this by `other`.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | a complex or scalar value of matching type (float, double, long double) |

### Return value

\*this

### See also

|  |  |
| --- | --- |
| operator+operator- | applies unary operators to complex numbers   (function template) |
| operator+operator-operator\*operator/ | performs complex number arithmetic on two complex values or a complex and a scalar   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/complex/operator_arith&oldid=138939>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 March 2022, at 02:53.