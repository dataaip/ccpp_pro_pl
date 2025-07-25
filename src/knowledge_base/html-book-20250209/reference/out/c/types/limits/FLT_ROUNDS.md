# FLT_ROUNDS

From cppreference.com
< c‎ | types‎ | limits
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

 Type support

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| size_t | | | | |
| ptrdiff_t | | | | |
| nullptr_t(C23) | | | | |
| NULL | | | | |
| max_align_t(C11) | | | | |
| offsetof | | | | |
| Numeric limits | | | | |
| Fixed width integer types (C99) | | | | |

 Numeric limits

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****FLT_ROUNDS**** | | | | |
| FLT_EVAL_METHOD(C99) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<float.h>` |  |  |
| #define FLT_ROUNDS /\* implementation defined \*/ |  |  |
|  |  |  |

Returns the current rounding direction of floating-point arithmetic operations.

|  |  |
| --- | --- |
| Value | Explanation |
| `-1` | the default rounding direction is not known |
| `0` | toward zero; same meaning as FE_TOWARDZERO |
| `1` | to nearest; same meaning as FE_TONEAREST |
| `2` | towards positive infinity; same meaning as FE_UPWARD |
| `3` | towards negative infinity; same meaning as FE_DOWNWARD |
| other values | implementation-defined behavior |

### Notes

The rounding mode can be changed with fesetround and ****FLT_ROUNDS**** reflects that change.

### See also

|  |  |
| --- | --- |
| fegetroundfesetround(C99)(C99) | gets or sets rounding direction   (function) |
| FE_DOWNWARDFE_TONEARESTFE_TOWARDZEROFE_UPWARD(C99) | floating-point rounding direction   (macro constant) |
| C++ documentation for FLT_ROUNDS | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/types/limits/FLT_ROUNDS&oldid=108863>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 February 2019, at 00:44.