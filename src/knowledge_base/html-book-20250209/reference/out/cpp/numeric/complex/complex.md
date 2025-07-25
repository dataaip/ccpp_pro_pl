# std::complex<T>::complex

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****complex::complex**** | | | | | | complex::operator= | | | | | | complex::real | | | | | | complex::imag | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | complex::operator+=complex::operator-=complex::operator\*=complex::operator/= | | | | | |
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
| Primary template (std::complex<T>) |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| complex( const T& re = T(), const T& im = T() ); |  | (until C++14) |
| constexpr complex( const T& re = T(), const T& im = T() ); |  | (since C++14) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| complex( const complex& other ); |  | (until C++14) |
| constexpr complex( const complex& other ); |  | (since C++14)  (until C++23) |
| constexpr complex( const complex& other ) = default; |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| template< class X >  complex( const complex<X>& other ); |  | (until C++14) |
| template< class X >  constexpr complex( const complex<X>& other ); |  | (since C++14)  (until C++23) |
| template< class X >  constexpr explicit(/\* see below \*/) complex( const complex<X>& other ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| Standard explicit specialization std::complex<float> (until C++23) |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| complex( float re = 0.0f, float im = 0.0f ); |  | (until C++11) |
| constexpr complex( float re = 0.0f, float im = 0.0f ); |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| constexpr complex( const complex<float>& other ) = default; | (2) | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| explicit complex( const complex<double>& other );  explicit complex( const complex<long double>& other ); |  | (until C++11) |
| constexpr explicit complex( const complex<double>& other );  constexpr explicit complex( const complex<long double>& other ); |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| Standard explicit specialization std::complex<double> (until C++23) |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| complex( double re = 0.0, double im = 0.0 ); |  | (until C++11) |
| constexpr complex( double re = 0.0, double im = 0.0 ); |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| constexpr complex( const complex<double>& other ) = default; | (2) | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| complex( const complex<float>& other );  explicit complex( const complex<long double>& other ); |  | (until C++11) |
| constexpr complex( const complex<float>& other );  constexpr explicit complex( const complex<long double>& other ); |  | (since C++11) |
| Standard explicit specialization std::complex<long double> (until C++23) |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| complex( long double re = 0.0L, long double im = 0.0L ); |  | (until C++11) |
| constexpr complex( long double re = 0.0L, long double im = 0.0L ); |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| constexpr complex( const complex<long double>& other ) = default; | (2) | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| complex( const complex<float>& other );  complex( const complex<double>& other ); |  | (until C++11) |
| constexpr complex( const complex<float>& other );  constexpr complex( const complex<double>& other ); |  | (since C++11) |
|  |  |  |

Constructs the std::complex object. The standard explicit specializations (std::complex<float>, std::complex<double> and std::complex<long double>) have different constructor declarations from the main template.(until C++23)

1) Constructs the complex number from real part re and imaginary part im.2) Copy constructor. Constructs the object with the copy of the contents of other. The copy constructors are implicitly declared in the standard explicit specializations.(until C++20)3) Converting constructor. Constructs the object from a complex number of a different type.

|  |  |
| --- | --- |
| The main template provides a converting constructor template, while each standard explicit specialization provides two non-template constructors for the two other standard explicit specializations.  The non-template constructors are converting constructors (i.e. non-explicit) if and only if the conversions of the real and imaginary parts are not narrowing. | (until C++23) |
| For the main template, the expression inside explicit evaluates to false if and only if the floating-point conversion rank of `T` is greater than or equal to the floating-point conversion rank of `X`. | (since C++23) |

### Parameters

|  |  |  |
| --- | --- | --- |
| re | - | the real part |
| im | - | the imaginary part |
| other | - | another complex number to use as source |

### Notes

Since C++23, the copy constructor is required to be trivial in order to satisfy the TriviallyCopyable requirement, but implementations generally make it trivial in all modes.

### See also

|  |  |
| --- | --- |
| operator= | assigns the contents   (public member function) |
| operator""ifoperator""ioperator""il(C++14) | a std::complex literal representing purely imaginary number   (function) |
| C documentation for CMPLX | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/complex/complex&oldid=154487>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 July 2023, at 09:39.