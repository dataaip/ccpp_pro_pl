# std::fegetenv, std::fesetenv

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
| fegetroundfesetround(C++11)(C++11) | | | | |
| ****fegetenvfesetenv****(C++11)(C++11) | | | | |
| feholdexcept(C++11) | | | | |
| feupdateenv(C++11) | | | | |
| Macro constants | | | | |
| FE_ALL_EXCEPTFE_DIVBYZEROFE_INEXACTFE_INVALIDFE_OVERFLOWFE_UNDERFLOW(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | | | | |
| FE_DOWNWARDFE_TONEARESTFE_TOWARDZEROFE_UPWARD(C++11)(C++11)(C++11)(C++11) | | | | |
| FE_DFL_ENV(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cfenv>` |  |  |
| int fegetenv( std::fenv_t\* envp ) | (1) | (since C++11) |
| int fesetenv( const std::fenv_t\* envp ); | (2) | (since C++11) |
|  |  |  |

Manages the status of the floating-point environment.

1) Attempts to store the status of the floating-point environment in the object pointed to by `envp`.2) Attempts to establish the floating-point environment from the object pointed to by `envp`. The value of that object must be previously obtained by a call to std::feholdexcept or `std::fegetenv` or be a floating-point macro constant. If any of the floating-point status flags are set in `envp`, they become set in the environment (and are then testable with std::fetestexcept), but the corresponding floating-point exceptions are not raised (execution continues uninterrupted)

### Parameters

|  |  |  |
| --- | --- | --- |
| envp | - | pointer to the object of type std::fenv_t which holds the status of the floating-point environment |

### Return value

​0​ on success, non-zero otherwise.

### See also

|  |  |
| --- | --- |
| feholdexcept(C++11) | saves the environment, clears all status flags and ignores all future errors   (function) |
| feupdateenv(C++11) | restores the floating-point environment and raises the previously raised exceptions   (function) |
| FE_DFL_ENV(C++11) | default floating-point environment   (macro constant) |
| C documentation for fegetenv, fesetenv | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/fenv/feenv&oldid=95624>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 September 2017, at 07:45.