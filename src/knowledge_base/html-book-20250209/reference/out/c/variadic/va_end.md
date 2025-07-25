# va_end

From cppreference.com
< c‎ | variadic
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

 Variadic functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| va_start | | | | |
| va_arg | | | | |
| va_copy(C99) | | | | |
| ****va_end**** | | | | |
| va_list | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdarg.h>` |  |  |
| void va_end( va_list ap ); |  |  |
|  |  |  |

The `va_end` macro performs cleanup for an `ap` object initialized by a call to va_start or va_copy. `va_end` may modify `ap` so that it is no longer usable.

If there is no corresponding call to va_start or va_copy, or if `va_end` is not called before a function that calls va_start or va_copy returns, the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| ap | - | an instance of the va_list type to clean up |

### Expanded value

(none)

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.16.1.3 The va_end macro (p: 270-271)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.15.1.3 The va_end macro (p: 250-251)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.8.1.3 The va_end macro

### See also

|  |  |
| --- | --- |
| va_arg | accesses the next variadic function argument   (function macro) |
| va_copy(C99) | makes a copy of the variadic function arguments   (function macro) |
| va_list | holds the information needed by va_start, va_arg, va_end, and va_copy   (typedef) |
| va_start | enables access to variadic function arguments   (function macro) |
| C++ documentation for va_end | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/variadic/va_end&oldid=117389>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 March 2020, at 01:14.