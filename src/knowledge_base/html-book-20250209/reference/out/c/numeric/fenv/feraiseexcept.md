# feraiseexcept

From cppreference.com
< c‎ | numeric‎ | fenv
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
| Floating-point environment (C99) | | | | |
| Pseudo-random number generation | | | | |
| Complex number arithmetic (C99) | | | | |
| Type-generic math (C99) | | | | |
| Bit manipulation (C23) | | | | |
| Checked integer arithmetic (C23) | | | | |

 Floating-point environment

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| feclearexcept(C99) | | | | |
| fetestexcept(C99) | | | | |
| ****feraiseexcept****(C99) | | | | |
| fegetexceptflagfesetexceptflag(C99)(C99) | | | | |
| fegetroundfesetround(C99)(C99) | | | | |
| fegetenvfesetenv(C99) | | | | |
| feholdexcept(C99) | | | | |
| feupdateenv(C99) | | | | |
| Macro constants | | | | |
| FE_ALL_EXCEPTFE_DIVBYZEROFE_INEXACTFE_INVALIDFE_OVERFLOWFE_UNDERFLOW(C99) | | | | |
| FE_DOWNWARDFE_TONEARESTFE_TOWARDZEROFE_UPWARD(C99) | | | | |
| FE_DFL_ENV(C99) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<fenv.h>` |  |  |
| int feraiseexcept( int excepts ); |  | (since C99) |
|  |  |  |

Attempts to raise all floating-point exceptions listed in `excepts` (a bitwise OR of the floating-point exception macros). If one of the exceptions is FE_OVERFLOW or FE_UNDERFLOW, this function may additionally raise FE_INEXACT. The order in which the exceptions are raised is unspecified, except that FE_OVERFLOW and FE_UNDERFLOW are always raised before FE_INEXACT.

### Parameters

|  |  |  |
| --- | --- | --- |
| excepts | - | bitmask listing the exception flags to raise |

### Return value

​0​ if all listed exceptions were raised, non-zero value otherwise.

### Example

Run this code

```
#include <stdio.h>
#include <fenv.h>
 
#pragma STDC FENV_ACCESS ON
 
void show_fe_exceptions(void)
{
    printf("current exceptions raised: ");
    if(fetestexcept(FE_DIVBYZERO))     printf(" FE_DIVBYZERO");
    if(fetestexcept(FE_INEXACT))       printf(" FE_INEXACT");
    if(fetestexcept(FE_INVALID))       printf(" FE_INVALID");
    if(fetestexcept(FE_OVERFLOW))      printf(" FE_OVERFLOW");
    if(fetestexcept(FE_UNDERFLOW))     printf(" FE_UNDERFLOW");
    if(fetestexcept(FE_ALL_EXCEPT)==0) printf(" none");
    feclearexcept(FE_ALL_EXCEPT);
    printf("\n");
}
 
double some_computation(void)
{
    /* Computation reaches a state that causes overflow. */
    int r = feraiseexcept(FE_OVERFLOW | FE_INEXACT);
    printf("feraiseexcept() %s\n", (r?"fails":"succeeds"));
    return 0.0;
}
 
int main(void)
{
    some_computation();
    show_fe_exceptions();
 
    return 0;
}

```

Output:

```
feraiseexcept() succeeds
current exceptions raised:  FE_INEXACT FE_OVERFLOW

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.6.2.3 The feraiseexcept function (p: 210)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.6.2.3 The feraiseexcept function (p: 191)

### See also

|  |  |
| --- | --- |
| feclearexcept(C99) | clears the specified floating-point status flags   (function) |
| fetestexcept(C99) | determines which of the specified floating-point status flags are set   (function) |
| C++ documentation for feraiseexcept | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/fenv/feraiseexcept&oldid=133795>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 September 2021, at 02:01.