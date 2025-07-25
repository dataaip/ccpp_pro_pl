# std::fegetround, std::fesetround

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
| feclearexcept(C++11) | | | | |
| fetestexcept(C++11) | | | | |
| feraiseexcept(C++11) | | | | |
| fegetexceptflagfesetexceptflag(C++11)(C++11) | | | | |
| ****fegetroundfesetround****(C++11)(C++11) | | | | |
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
| int fesetround( int round ) | (1) | (since C++11) |
| int fegetround() | (2) | (since C++11) |
|  |  |  |

Manages the floating-point rounding direction.

1) Attempts to establish the floating-point rounding direction equal to the argument `round`, which is expected to be one of the floating point rounding macros.2) Returns the value of the floating point rounding macro that corresponds to the current rounding direction.

### Parameters

|  |  |  |
| --- | --- | --- |
| round | - | rounding direction, one of floating point rounding macros |

### Return value

1) ​0​ on success, non-zero otherwise.

2) The floating point rounding macro describing the current rounding direction or a negative value if the direction cannot be determined.

### Notes

The current rounding mode, reflecting the effects of the most recent `fesetround`, can also be queried with FLT_ROUNDS.

See floating-point rounding macros for the effects of rounding.

### Example

Run this code

```
#include <cfenv>
#include <cmath>
#include <iomanip>
#include <iostream>
#include <utility>
// #pragma STDC FENV_ACCESS ON
 
int main()
{
    static constexpr std::pair<const char*, const double> samples[]
    {
        {" 12.0", 12.0},  {" 12.1", 12.1}, {"-12.1", -12.1}, {" 12.5", 12.5},
        {"-12.5", -12.5}, {" 12.9", 12.9}, {"-12.9", -12.9}, {" 13.0", 13.0}
    };
 
    std::cout <<
        "│ sample │  FE_DOWNWARD  │   FE_UPWARD   │ FE_TONEAREST  │ FE_TOWARDZERO │\n";
 
    for (const auto& [str, fp] : samples)
    {
        std::cout << "│ " << std::setw(6) << str << " │  ";
        for (const int dir : {FE_DOWNWARD, FE_UPWARD, FE_TONEAREST, FE_TOWARDZERO})
        {
            std::fesetround(dir);
            std::cout << std::setw(10) << std::fixed << std::nearbyint(fp) << "   │  ";
        }
        std::cout << '\n';
    }
}

```

Output:

```
│ sample │  FE_DOWNWARD  │   FE_UPWARD   │ FE_TONEAREST  │ FE_TOWARDZERO │
│   12.0 │   12.000000   │   12.000000   │   12.000000   │   12.000000   │
│   12.1 │   12.000000   │   13.000000   │   12.000000   │   12.000000   │
│  -12.1 │  -13.000000   │  -12.000000   │  -12.000000   │  -12.000000   │
│   12.5 │   12.000000   │   13.000000   │   12.000000   │   12.000000   │
│  -12.5 │  -13.000000   │  -12.000000   │  -12.000000   │  -12.000000   │
│   12.9 │   12.000000   │   13.000000   │   13.000000   │   12.000000   │
│  -12.9 │  -13.000000   │  -12.000000   │  -13.000000   │  -12.000000   │
│   13.0 │   13.000000   │   13.000000   │   13.000000   │   13.000000   │

```

### See also

|  |  |
| --- | --- |
| nearbyintnearbyintfnearbyintl(C++11)(C++11)(C++11) | nearest integer using current rounding mode   (function) |
| rintrintfrintllrintlrintflrintlllrintllrintfllrintl(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | nearest integer using current rounding mode with exception if the result differs   (function) |
| C documentation for fegetround, fesetround | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/fenv/feround&oldid=150982>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 April 2023, at 09:36.