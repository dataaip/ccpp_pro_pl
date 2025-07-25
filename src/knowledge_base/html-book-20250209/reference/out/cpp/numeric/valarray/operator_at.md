# std::valarray<T>::operator[]

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::valarray | | | | | | valarray::~valarray | | | | | | valarray::operator= | | | | | | ****valarray::operator[]**** | | | | | | valarray::swap | | | | | | valarray::size | | | | | | valarray::resize | | | | | | valarray::sum | | | | | | valarray::min | | | | | | valarray::max | | | | | | valarray::shift | | | | | | valarray::cshift | | | | | | valarray::apply | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::operator+valarray::operator-valarray::operator~valarray::operator! | | | | | | valarray::operator+=valarray::operator-=valarray::operator\*=valarray::operator/=valarray::operator%=valarray::operator&=valarray::operator|=valarray::operator^=valarray::operator<<=valarray::operator>>= | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::valarray)(C++11) | | | | | | begin(std::valarray)(C++11) | | | | | | end(std::valarray)(C++11) | | | | | | abs | | | | | | exp | | | | | | log | | | | | | log10 | | | | | | pow | | | | | | sqrt | | | | | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator\*operator/operator%operator+operator-operator^operator&operator|operator<<operator>>operator&&operator|| | | | | | | operator==operator!=operator<operator>operator<=operator>= | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | gslice_array | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | gslice | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| const T&               operator[]( std::size_t pos ) const; | (1) |  |
| T&                     operator[]( std::size_t pos ); | (2) |  |
| std::valarray<T>       operator[]( std::slice slicearr ) const; | (3) |  |
| std::slice_array<T>    operator[]( std::slice slicearr ); | (4) |  |
| std::valarray<T>       operator[]( const std::gslice& gslicearr ) const; | (5) |  |
| std::gslice_array<T>   operator[]( const std::gslice& gslicearr ); | (6) |  |
| std::valarray<T>       operator[]( const std::valarray<bool>& boolarr ) const; | (7) |  |
| std::mask_array<T>     operator[]( const std::valarray<bool>& boolarr ); | (8) |  |
| std::valarray<T>       operator[]( const std::valarray<std::size_t>& indarr ) const; | (9) |  |
| std::indirect_array<T> operator[]( const std::valarray<std::size_t>& indarr ); | (10) |  |
|  |  |  |

Retrieve single elements or portions of the array.

The const overloads that return element sequences create a new std::valarray object.
The non-const overloads return classes holding references to the array elements.

The selected elements(s) must exist:

- for overloads (1,2), if pos is not less than `size()`, the behavior is undefined; and
- for overloads (3-10), if the argument does not specify a valid subset of \*this, the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | position of the element to return |
| slicearr | - | slice of the elements to return |
| gslicearr | - | gslice of the elements to return |
| boolarr | - | mask of the elements to return |
| indarr | - | indices of the elements to return |

### Return value

1,2) A reference to the corresponding element.3,5,7,9) A std::valarray object containing copies of the selected items.4,6,8,10) The corresponding data structure containing references to the selected items.

### Exceptions

May throw implementation-defined exceptions.

### Notes

For proper std::valarray values a, b and proper std::size_t values i, j, all of the following expressions always evaluate to true:

1) (a[i] = q, a[i]) == q for non-const a2) &a[i + j] == &a[i] + j

- This means that std::valarray elements are adjacent in memory.
3) &a[i] != &b[j] for every objects a and b that are not aliases of one another

- This means that there are no aliases in the elements and this property can be used to perform some kinds of optimization.

References become invalid on `resize()` or when the array is destructed.

For overloads (3,5,7,9), The function can be implemented with the return type different from std::valarray. In this case, the replacement type has the following properties:

:   - All const member functions of std::valarray are provided.
    - std::valarray, std::slice_array, std::gslice_array, std::mask_array and std::indirect_array can be constructed from the replacement type.
    - For every function taking a const std::valarray<T>& except begin() and end()(since C++11), identical functions taking the replacement types shall be added;
    - For every function taking two const std::valarray<T>& arguments, identical functions taking every combination of const std::valarray<T>& and replacement types shall be added.
    - The return type does not add more than two levels of template nesting over the most deeply-nested argument type.

Slice/mask/indirect index accesses do not chain: v[v == n][std::slice(0, 5, 2)] = x; is an error because std::mask_array (the type of v[v == n]) does not have operator[].

### Example

Run this code

```
#include <cstddef>
#include <iomanip>
#include <iostream>
#include <valarray>
 
int main() 
{
    std::valarray<int> data = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9};
 
    std::cout << "Initial valarray:   ";
    for (int n : data)
        std::cout << std::setw(3) << n;
    std::cout << '\n';
 
    data[data > 5] = -1; // valarray<bool> overload of operator[]
    // the type of data > 5 is std::valarray<bool>
    // the type of data[data > 5] is std::mask_array<int>
 
    std::cout << "After v[v > 5] = -1:";
    for (std::size_t n = 0; n < data.size(); ++n) 
        std::cout << std::setw(3) << data[n]; // regular operator[]
    std::cout << '\n';
}

```

Output:

```
Initial valarray:     0  1  2  3  4  5  6  7  8  9
After v[v > 5] = -1:  0  1  2  3  4  5 -1 -1 -1 -1

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 389 | C++98 | the return type of overload (1) was `T` | corrected to const T& |
| LWG 430 | C++98 | the behavior was unclear for overloads (3-10) if an invalid subset is specified | the behavior is  undefined in this case |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray/operator_at&oldid=157957>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 September 2023, at 10:44.