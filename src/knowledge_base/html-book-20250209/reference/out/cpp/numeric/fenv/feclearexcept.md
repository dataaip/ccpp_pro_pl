# std::feclearexcept

From cppreference.com
< cpp‎ | numeric‎ | fenv
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

Floating-point environment

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| ****feclearexcept****(C++11) | | | | |
| fetestexcept(C++11) | | | | |
| feraiseexcept(C++11) | | | | |
| fegetexceptflagfesetexceptflag(C++11)(C++11) | | | | |
| fegetroundfesetround(C++11)(C++11) | | | | |
| fegetenvfesetenv(C++11)(C++11) | | | | |
| feholdexcept(C++11) | | | | |
| feupdateenv(C++11) | | | | |
| Macro constants | | | | |
| FE_ALL_EXCEPTFE_DIVBYZEROFE_INEXACTFE_INVALIDFE_OVERFLOWFE_UNDERFLOW(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | | | | |
| FE_DOWNWARDFE_TONEARESTFE_TOWARDZEROFE_UPWARD(C++11)(C++11)(C++11)(C++11) | | | | |
| FE_DFL_ENV(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cfenv>` |  |  |
| int feclearexcept( int excepts ); |  | (since C++11) |
|  |  |  |

Attempts to clear the floating-point exceptions that are listed in the bitmask argument `excepts`, which is a bitwise OR of the floating point exception macros.

### Parameters

|  |  |  |
| --- | --- | --- |
| excepts | - | bitmask listing the exception flags to clear |

### Return value

​0​ if all indicated exceptions were successfully cleared or if `excepts` is zero. Returns a non-zero value on error.

### Example

Run this code

```
#include <cfenv>
#include <cmath>
#include <iostream>
 
// #pragma STDC FENV_ACCESS ON
 
volatile double zero = 0.0; // volatile not needed where FENV_ACCESS is supported
volatile double one = 1.0;  // volatile not needed where FENV_ACCESS is supported
 
int main()
{
    std::feclearexcept(FE_ALL_EXCEPT);
    std::cout <<  "1.0/0.0 = " << 1.0 / zero << '\n';
    if (std::fetestexcept(FE_DIVBYZERO))
        std::cout << "division by zero reported\n";
    else
        std::cout << "division by zero not reported\n";
 
    std::feclearexcept(FE_ALL_EXCEPT);
    std::cout << "1.0/10 = " << one / 10 << '\n';
    if (std::fetestexcept(FE_INEXACT))
        std::cout << "inexact result reported\n";
    else
        std::cout << "inexact result not reported\n";
 
    std::feclearexcept(FE_ALL_EXCEPT);
    std::cout << "sqrt(-1) = " << std::sqrt(-1) << '\n';
    if (std::fetestexcept(FE_INVALID))
        std::cout << "invalid result reported\n";
    else
        std::cout << "invalid result not reported\n";
}

```

Possible output:

```
1.0/0.0 = inf
division by zero reported
1.0/10 = 0.1
inexact result reported
sqrt(-1) = -nan
invalid result reported

```

### See also

|  |  |
| --- | --- |
| fetestexcept(C++11) | determines which of the specified floating-point status flags are set   (function) |
| C documentation for feclearexcept | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/fenv/feclearexcept&oldid=95618>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 September 2017, at 06:50.