# Floating-point environment

From cppreference.com
< c‎ | numeric
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 Numerics

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Common mathematical functions | | | | |
| ****Floating-point environment**** (C99) | | | | |
| Pseudo-random number generation | | | | |
| Complex number arithmetic (C99) | | | | |
| Type-generic math (C99) | | | | |
| Bit manipulation (C23) | | | | |
| Checked integer arithmetic (C23) | | | | |

 ****Floating-point environment****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| feclearexcept(C99) | | | | |
| fetestexcept(C99) | | | | |
| feraiseexcept(C99) | | | | |
| fegetexceptflagfesetexceptflag(C99)(C99) | | | | |
| fegetroundfesetround(C99)(C99) | | | | |
| fegetenvfesetenv(C99) | | | | |
| feholdexcept(C99) | | | | |
| feupdateenv(C99) | | | | |
| Macro constants | | | | |
| FE_ALL_EXCEPTFE_DIVBYZEROFE_INEXACTFE_INVALIDFE_OVERFLOWFE_UNDERFLOW(C99) | | | | |
| FE_DOWNWARDFE_TONEARESTFE_TOWARDZEROFE_UPWARD(C99) | | | | |
| FE_DFL_ENV(C99) | | | | |

The floating-point environment is the set of floating-point status flags and control modes supported by the implementation. It is thread-local, each thread inherits the initial state of its floating-point environment from the parent thread. Floating-point operations modify the floating-point status flags to indicate abnormal results or auxiliary information. The state of floating-point control modes affects the outcomes of some floating-point operations.

The floating-point environment access and modification is only meaningful when #pragma STDC FENV_ACCESS is set to `ON`. Otherwise the implementation is free to assume that floating-point control modes are always the default ones and that floating-point status flags are never tested or modified. In practice, few current compilers, such as HP aCC, Oracle Studio, and IBM XL, support the #pragma explicitly, but most compilers allow meaningful access to the floating-point environment anyway.

### Types

|  |  |
| --- | --- |
| Defined in header `<fenv.h>` | |
| fenv_t | The type representing the entire floating-point environment |
| fexcept_t | The type representing all floating-point status flags collectively |

### Functions

|  |  |
| --- | --- |
| feclearexcept(C99) | clears the specified floating-point status flags   (function) |
| fetestexcept(C99) | determines which of the specified floating-point status flags are set   (function) |
| feraiseexcept(C99) | raises the specified floating-point exceptions   (function) |
| fegetexceptflagfesetexceptflag(C99)(C99) | copies the state of the specified floating-point status flags from or to the floating-point environment   (function) |
| fegetroundfesetround(C99)(C99) | gets or sets rounding direction   (function) |
| fegetenvfesetenv(C99) | saves or restores the current floating-point environment   (function) |
| feholdexcept(C99) | saves the environment, clears all status flags and ignores all future errors   (function) |
| feupdateenv(C99) | restores the floating-point environment and raises the previously raise exceptions   (function) |

### Macros

|  |  |
| --- | --- |
| FE_ALL_EXCEPTFE_DIVBYZEROFE_INEXACTFE_INVALIDFE_OVERFLOWFE_UNDERFLOW(C99) | floating-point exceptions   (macro constant) |
| FE_DOWNWARDFE_TONEARESTFE_TOWARDZEROFE_UPWARD(C99) | floating-point rounding direction   (macro constant) |
| FE_DFL_ENV(C99) | default floating-point environment   (macro constant) |

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.6 Floating-point environment <fenv.h> (p: TBD)

:   - 7.31.4 Floating-point environment <fenv.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.6 Floating-point environment <fenv.h> (p: 150-156)

:   - 7.31.4 Floating-point environment <fenv.h> (p: 332)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.6 Floating-point environment <fenv.h> (p: 206-215)

:   - 7.31.4 Floating-point environment <fenv.h> (p: 455)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.6 Floating-point environment <fenv.h> (p: 187-196)

### See also

|  |  |
| --- | --- |
| C++ documentation for Floating-point environment | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/fenv&oldid=180048>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 February 2025, at 03:24.