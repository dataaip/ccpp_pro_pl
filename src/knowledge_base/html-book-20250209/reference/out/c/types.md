# Type support

From cppreference.com
< c
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| ****Type support**** | | | | |
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

 ****Type support****

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

See also type system overview and arithmetic types defined by the language.

### Basic types

#### Additional basic types and convenience macros

|  |  |
| --- | --- |
| Defined in header `<stddef.h>` | |
| size_t | unsigned integer type returned by the sizeof operator   (typedef) |
| ptrdiff_t | signed integer type returned when subtracting two pointers   (typedef) |
| nullptr_t(C23) | the type of the predefined null pointer constant nullptr   (typedef) |
| NULL | implementation-defined null pointer constant   (macro constant) |
| max_align_t(C11) | a type with alignment requirement as great as any other scalar type   (typedef) |
| offsetof | byte offset from the beginning of a struct type to specified member   (function macro) |
| Defined in header `<stdbool.h>` | |
| bool(C99)(removed in C23) | convenience macro, expands to _Bool   (keyword macro) |
| true(C99)(removed in C23) | expands to integer constant 1   (macro constant) |
| false(C99)(removed in C23) | expands to integer constant ​0​   (macro constant) |
| __bool_true_false_are_defined(C99)(deprecated in C23) | expands to integer constant 1   (macro constant) |
| Defined in header `<stdalign.h>` | |
| alignas(C11)(removed in C23) | convenience macro, expands to keyword _Alignas   (keyword macro) |
| alignof(C11)(removed in C23) | convenience macro, expands to keyword _Alignof   (keyword macro) |
| __alignas_is_defined(C11)(removed in C23) | expands to integer constant 1   (macro constant) |
| __alignof_is_defined(C11)(removed in C23) | expands to integer constant 1   (macro constant) |
| Defined in header `<stdnoreturn.h>` | |
| noreturn(C11)(deprecated in C23) | convenience macro, expands to _Noreturn   (keyword macro) |

#### Fixed width integer types (since C99)

#### Numeric limits

### Notes

|  |  |
| --- | --- |
| The type of true and false is int rather than _Bool.  A program may undefine and perhaps then redefine the macros bool, true and false. However, such ability is a deprecated feature. | (since C99) (until C23) |
| The type of true and false is bool. It is unspecified whether any of bool, _Bool, true, or false is implemented as a predefined macro.  If bool, true, or false (but not _Bool) is defined as a predefined macro, a program may undefine and perhaps redefine it. | (since C23) |

### Example

Run this code

```
#include <stdalign.h>
#include <stdbool.h>
#include <stdio.h>
 
int main(void)
{
    printf("%d %d %d\n", true && false, true || false, !false);
    printf("%d %d\n", true ^ true, true + true);
    printf("%zu\n", alignof(short));
}

```

Possible output:

```
0 1 1
0 2
2

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.15 Alignment <stdalign.h> (p: TBD)

:   - 7.18 Boolean type and values <stdbool.h> (p: TBD)

:   - 7.19 Common definitions <stddef.h> (p: TBD)

:   - 7.23 _Noreturn <stdnoreturn.h> (p: TBD)

:   - 7.31.9 Boolean type and values <stdbool.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.15 Alignment <stdalign.h> (p: 196)

:   - 7.18 Boolean type and values <stdbool.h> (p: 210)

:   - 7.19 Common definitions <stddef.h> (p: 211)

:   - 7.23 _Noreturn <stdnoreturn.h> (p: 263)

:   - 7.31.9 Boolean type and values <stdbool.h> (p: 332)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.15 Alignment <stdalign.h> (p: 268)

:   - 7.18 Boolean type and values <stdbool.h> (p: 287)

:   - 7.19 Common definitions <stddef.h> (p: 288)

:   - 7.23 _Noreturn <stdnoreturn.h> (p: 361)

:   - 7.31.9 Boolean type and values <stdbool.h> (p: 456)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.18 Boolean type and values <stdbool.h> (p: 253)

:   - 7.19 Common definitions <stddef.h> (p: 254)

:   - 7.26.7 Boolean type and values <stdbool.h> (p: 401)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.1.5 Common definitions <stddef.h>

### See also

|  |  |
| --- | --- |
| C++ documentation for Type support library | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/types&oldid=180056>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 February 2025, at 04:58.