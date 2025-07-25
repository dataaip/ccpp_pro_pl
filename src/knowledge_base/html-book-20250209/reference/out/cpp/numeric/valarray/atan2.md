# std::atan2(std::valarray)

From cppreference.com
< cpp‎ | numeric‎ | valarray
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

std::valarray

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::valarray | | | | | | valarray::~valarray | | | | | | valarray::operator= | | | | | | [valarray::operator[]](operator_at.html "cpp/numeric/valarray/operator at") | | | | | | valarray::swap | | | | | | valarray::size | | | | | | valarray::resize | | | | | | valarray::sum | | | | | | valarray::min | | | | | | valarray::max | | | | | | valarray::shift | | | | | | valarray::cshift | | | | | | valarray::apply | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::operator+valarray::operator-valarray::operator~valarray::operator! | | | | | | valarray::operator+=valarray::operator-=valarray::operator\*=valarray::operator/=valarray::operator%=valarray::operator&=valarray::operator|=valarray::operator^=valarray::operator<<=valarray::operator>>= | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::valarray)(C++11) | | | | | | begin(std::valarray)(C++11) | | | | | | end(std::valarray)(C++11) | | | | | | abs | | | | | | exp | | | | | | log | | | | | | log10 | | | | | | pow | | | | | | sqrt | | | | | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | ****atan2**** | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator\*operator/operator%operator+operator-operator^operator&operator|operator<<operator>>operator&&operator|| | | | | | | operator==operator!=operator<operator>operator<=operator>= | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | gslice_array | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | gslice | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<valarray>` |  |  |
| template< class T >   std::valarray<T> atan2( const std::valarray<T>& y, const std::valarray<T>& x ); | (1) |  |
| template< class T >   std::valarray<T> atan2( const std::valarray<T>& y, const typename std::valarray<T>::value_type& vx ); | (2) |  |
| template< class T >   std::valarray<T> atan2( const typename std::valarray<T>::value_type& vy, const std::valarray<T>& x ); | (3) |  |
|  |  |  |

Computes the inverse tangent of y / x using the signs of arguments to correctly determine quadrant.

1) Computes the inverse tangent of each pair of corresponding values from y and x.

The behavior is undefined if x.size() != y.size().

2) Computes the inverse tangent of vx and each value in the numeric array y.3) Computes the inverse tangent of vy and each value in the numeric array x.

### Parameters

|  |  |  |
| --- | --- | --- |
| x, y | - | numeric arrays to compute inverse tangent of |
| vy, vx | - | values to compute inverse tangent of |

### Return value

A numeric array containing the results of computation of inverse tangent.

### Notes

Unqualified function (atan2) is used to perform the computation. If such function is not available, std::atan2 is used due to argument-dependent lookup.

The function can be implemented with the return type different from std::valarray. In this case, the replacement type has the following properties:

:   - All const member functions of std::valarray are provided.
    - std::valarray, std::slice_array, std::gslice_array, std::mask_array and std::indirect_array can be constructed from the replacement type.
    - For every function taking a const std::valarray<T>& except begin() and end()(since C++11), identical functions taking the replacement types shall be added;
    - For every function taking two const std::valarray<T>& arguments, identical functions taking every combination of const std::valarray<T>& and replacement types shall be added.
    - The return type does not add more than two levels of template nesting over the most deeply-nested argument type.

### Example

Run this code

```
#include <algorithm>
#include <cmath>
#include <iomanip>
#include <iostream>
#include <valarray>
 
void show(char const* title, const std::valarray<double>& va)
{
    std::cout << title << ' ';
    std::for_each(std::begin(va), std::end(va), [](const double x)
    { 
        std::cout << ' ' << std::right << std::setw(4) << x << "°";
    });
    std::cout << '\n';
}
 
const double pi = std::acos(-1.0); // C++20: std::numbers::pi
 
int main()
{
    auto degrees_to_radians = [](double const& x) { return (pi * x / 180); };
    auto radians_to_degrees = [](double const& x) { return (180 * x / pi); };
 
    const std::valarray<double> degrees{-90, -60, -45, -30, 0, 30, 45, 60, 90};
    const std::valarray<double> radians = degrees.apply(degrees_to_radians);
 
    const auto sin = std::sin(radians);
    const auto cos = std::cos(radians);
 
    show("(1)", std::atan2(sin, cos).apply(radians_to_degrees));
    show("(2)", std::atan2(sin/cos, 1.0).apply(radians_to_degrees));
    show("(3)", std::atan2(1.0, cos/sin).apply(radians_to_degrees));
}

```

Output:

```
(1)   -90°  -60°  -45°  -30°    0°   30°   45°   60°   90°
(2)   -90°  -60°  -45°  -30°    0°   30°   45°   60°   90°
(3)    90°  120°  135°  150°    0°   30°   45°   60°   90°

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3074 | C++98 | `T` is deduced from both the scalar and the `valarray` for (2,3), disallowing mixed-type calls | only deduce `T` from the `valarray` |

### See also

|  |  |
| --- | --- |
| asin(std::valarray) | applies the function std::asin to each element of valarray   (function template) |
| acos(std::valarray) | applies the function std::acos to each element of valarray   (function template) |
| atan(std::valarray) | applies the function std::atan to each element of valarray   (function template) |
| atan2atan2fatan2l(C++11)(C++11) | arc tangent, using signs to determine quadrants   (function) |
| arg | returns the phase angle   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray/atan2&oldid=160850>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 October 2023, at 13:44.