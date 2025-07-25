# std::indirect_array<T>::operator=

From cppreference.com
< cpp‎ | numeric‎ | valarray‎ | indirect array
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::valarray | | | | | | valarray::~valarray | | | | | | valarray::operator= | | | | | | [valarray::operator[]](../operator_at.html "cpp/numeric/valarray/operator at") | | | | | | valarray::swap | | | | | | valarray::size | | | | | | valarray::resize | | | | | | valarray::sum | | | | | | valarray::min | | | | | | valarray::max | | | | | | valarray::shift | | | | | | valarray::cshift | | | | | | valarray::apply | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::operator+valarray::operator-valarray::operator~valarray::operator! | | | | | | valarray::operator+=valarray::operator-=valarray::operator\*=valarray::operator/=valarray::operator%=valarray::operator&=valarray::operator|=valarray::operator^=valarray::operator<<=valarray::operator>>= | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::valarray)(C++11) | | | | | | begin(std::valarray)(C++11) | | | | | | end(std::valarray)(C++11) | | | | | | abs | | | | | | exp | | | | | | log | | | | | | log10 | | | | | | pow | | | | | | sqrt | | | | | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator\*operator/operator%operator+operator-operator^operator&operator|operator<<operator>>operator&&operator|| | | | | | | operator==operator!=operator<operator>operator<=operator>= | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | gslice_array | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | gslice | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

std::indirect_array

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| indirect_array::indirect_array | | | | |
| indirect_array::~indirect_array | | | | |
| ****indirect_array::operator=**** | | | | |
| indirect_array::operator+=indirect_array::operator-=indirect_array::operator\*=indirect_array::operator/=indirect_array::operator%=indirect_array::operator&=indirect_array::operator|=indirect_array::operator^=indirect_array::operator<<=indirect_array::operator>>= | | | | |

|  |  |  |
| --- | --- | --- |
| void operator=( const T& value ) const; | (1) |  |
| void operator=( const std::valarray<T>& val_arr ) const; | (2) |  |
| const indirect_array& operator=( const indirect_array& other_arr ) const; | (3) |  |
|  |  |  |

Assigns values to all referred elements.

1) Assigns value to all of the elements.2) Assigns the elements of val_arr to the referred to elements of \*this.3) Assigns the selected elements from other_arr to the referred to elements of \*this.

### Parameters

|  |  |  |
| --- | --- | --- |
| value | - | a value to assign to all of the referred elements |
| val_arr | - | std::valarray to assign |
| other_arr | - | std::indirect_array to assign |

### Return value

1,2) (none)3) \*this

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <numeric>
#include <valarray>
 
void print(int n, std::valarray<int> const& v)
{
    std::cout << n << ':';
    for (int e : v)
        std::cout << std::setw(3) << e;
    std::cout << '\n';
}
 
int main()
{
    std::valarray<int> v(8);
    std::iota(std::begin(v), std::end(v), 0);
    print(1, v);
 
    std::valarray<std::size_t> idx{1, 3, 5, 7};
    const std::indirect_array<int> ia = v[idx];
    // 'ia' refers to v[1], v[3], v[5], v[7]
    ia = -1; // (1), effectively:
             // v[1] = v[3] = v[5] = v[7] = -1;
    print(2, v);
 
    ia = /*std::valarray<int>*/{-1, -2, -3, -4}; // (2),
        // effectively: v[1] = -1, v[3] = -2, v[5] = -3, v[7] = -4;
    print(3, v);
 
    std::valarray<std::size_t> idx2{0, 2, 4, 6};
    const std::indirect_array<int> ia2 = v[idx2];
    // 'ia2' refers to v[0], v[2], v[4], v[6]
    ia = ia2; // (3), effectively:
              // v[1] = v[0], v[3] = v[2], v[5] = v[4], v[7] = v[6];
    print(4, v);
}

```

Output:

```
1:  0  1  2  3  4  5  6  7
2:  0 -1  2 -1  4 -1  6 -1
3:  0 -1  2 -2  4 -3  6 -4
4:  0  0  2  2  4  4  6  6

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 123 | C++98 | overload (2) was non-const | made const |
| LWG 253 | C++98 | the copy assignment operator was private | made public |
| LWG 621 | C++98 | the copy assignment operator was non-const | made const |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray/indirect_array/operator%3D&oldid=120735>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 July 2020, at 07:15.