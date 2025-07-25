# std::valarray

From cppreference.com
< cpp‎ | numeric
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
| ****Numeric array (`valarray`)**** | | | | |
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

****std::valarray****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::valarray | | | | | | valarray::~valarray | | | | | | valarray::operator= | | | | | | [valarray::operator[]](valarray/operator_at.html "cpp/numeric/valarray/operator at") | | | | | | valarray::swap | | | | | | valarray::size | | | | | | valarray::resize | | | | | | valarray::sum | | | | | | valarray::min | | | | | | valarray::max | | | | | | valarray::shift | | | | | | valarray::cshift | | | | | | valarray::apply | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::operator+valarray::operator-valarray::operator~valarray::operator! | | | | | | valarray::operator+=valarray::operator-=valarray::operator\*=valarray::operator/=valarray::operator%=valarray::operator&=valarray::operator|=valarray::operator^=valarray::operator<<=valarray::operator>>= | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::valarray)(C++11) | | | | | | begin(std::valarray)(C++11) | | | | | | end(std::valarray)(C++11) | | | | | | abs | | | | | | exp | | | | | | log | | | | | | log10 | | | | | | pow | | | | | | sqrt | | | | | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator\*operator/operator%operator+operator-operator^operator&operator|operator<<operator>>operator&&operator|| | | | | | | operator==operator!=operator<operator>operator<=operator>= | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | gslice_array | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | gslice | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<valarray>` |  |  |
| template< class T >  class valarray; |  |  |
|  |  |  |

`std::valarray` is the class for representing and manipulating arrays of values. It supports element-wise mathematical operations and various forms of generalized subscript operators, slicing and indirect access.

### Notes

`std::valarray` and helper classes are defined to be free of certain forms of aliasing, thus allowing operations on these classes to be optimized similar to the effect of the keyword restrict in the C programming language. In addition, functions and operators that take `valarray` arguments are allowed to return proxy objects to make it possible for the compiler to optimize an expression such as v1 = a \* v2 + v3; as a single loop that executes v1[i] = a \* v2[i] + v3[i]; avoiding any temporaries or multiple passes. However, expression templates make the same optimization technique available for any C++ container, and the majority of numeric libraries prefer expression templates to valarrays for flexibility. Some C++ standard library implementations use expression templates to implement efficient operations on `std::valarray` (e.g. GNU libstdc++ and LLVM libc++). Only rarely are valarrays optimized any further, as in e.g. Intel Integrated Performance Primitives.

### Template parameters

|  |  |  |
| --- | --- | --- |
| T | - | the type of the elements. The type must meet the NumericType requirements |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `value_type` | `T` |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs new numeric array   (public member function) |
| (destructor) | destructs the numeric array   (public member function) |
| operator= | assigns the contents   (public member function) |
| [operator[]](valarray/operator_at.html "cpp/numeric/valarray/operator at") | get/set valarray element, slice, or mask   (public member function) |
| operator+operator-operator~operator! | applies a unary arithmetic operator to each element of the valarray   (public member function) |
| operator+=operator-=operator\*=operator/=operator%=operator&=operator|=operator^=operator<<=operator>>= | applies compound assignment operator to each element of the valarray   (public member function) |
| swap | swaps with another valarray   (public member function) |
| size | returns the size of valarray   (public member function) |
| resize | changes the size of valarray   (public member function) |
| sum | calculates the sum of all elements   (public member function) |
| min | returns the smallest element   (public member function) |
| max | returns the largest element   (public member function) |
| shift | zero-filling shift the elements of the valarray   (public member function) |
| cshift | circular shift of the elements of the valarray   (public member function) |
| apply | applies a function to every element of a valarray   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| std::swap(std::valarray)(C++11) | specializes the std::swap algorithm   (function template) |
| std::begin(std::valarray)(C++11) | overloads std::begin   (function template) |
| std::end(std::valarray)(C++11) | specializes std::end   (function template) |
| operator+operator-operator\*operator/operator%operator&operator|operator^operator<<operator>>operator&&operator|| | applies binary operators to each element of two valarrays, or a valarray and a value   (function template) |
| operator==operator!=operator<operator<=operator>operator>= | compares two valarrays or a valarray with a value   (function template) |
| abs(std::valarray) | applies the function abs to each element of valarray   (function template) |
| Exponential functions | |
| exp(std::valarray) | applies the function std::exp to each element of valarray   (function template) |
| log(std::valarray) | applies the function std::log to each element of valarray   (function template) |
| log10(std::valarray) | applies the function std::log10 to each element of valarray   (function template) |
| Power functions | |
| pow(std::valarray) | applies the function std::pow to two valarrays or a valarray and a value   (function template) |
| sqrt(std::valarray) | applies the function std::sqrt to each element of valarray   (function template) |
| Trigonometric functions | |
| sin(std::valarray) | applies the function std::sin to each element of valarray   (function template) |
| cos(std::valarray) | applies the function std::cos to each element of valarray   (function template) |
| tan(std::valarray) | applies the function std::tan to each element of valarray   (function template) |
| asin(std::valarray) | applies the function std::asin to each element of valarray   (function template) |
| acos(std::valarray) | applies the function std::acos to each element of valarray   (function template) |
| atan(std::valarray) | applies the function std::atan to each element of valarray   (function template) |
| atan2(std::valarray) | applies the function std::atan2 to a valarray and a value   (function template) |
| Hyperbolic functions | |
| sinh(std::valarray) | applies the function std::sinh to each element of valarray   (function template) |
| cosh(std::valarray) | applies the function std::cosh to each element of valarray   (function template) |
| tanh(std::valarray) | applies the function std::tanh to each element of valarray   (function template) |

### Helper classes

|  |  |
| --- | --- |
| slice | BLAS-like slice of a valarray: starting index, length, stride   (class) |
| slice_array | proxy to a subset of a valarray after applying a slice   (class template) |
| gslice | generalized slice of a valarray: starting index, set of lengths, set of strides   (class) |
| gslice_array | proxy to a subset of a valarray after applying a gslice   (class template) |
| mask_array | proxy to a subset of a valarray after applying a boolean mask `operator[]`   (class template) |
| indirect_array | proxy to a subset of a valarray after applying indirect `operator[]`   (class template) |

### Deduction guides(since C++17)

### See also

|  |  |
| --- | --- |
| simd(C++26) | convenience alias template for `basic_simd` that can specify its width (alias template) |
| simd_mask")(C++26) | convenience alias template for `basic_simd_mask` that can specify its width (alias template) |
| simd(parallelism TS v2) | data-parallel vector type   (class template) |
| simd_mask(parallelism TS v2) | data-parallel type with the element type bool   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray&oldid=178686>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 December 2024, at 14:36.