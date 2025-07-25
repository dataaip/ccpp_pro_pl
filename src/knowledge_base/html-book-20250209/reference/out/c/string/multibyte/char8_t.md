# char8_t

From cppreference.com
< c‎ | string‎ | multibyte
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

 Strings library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Null-terminated byte strings | | | | |
| Null-terminated multibyte strings | | | | |
| Null-terminated wide strings | | | | |

 Null-terminated multibyte strings

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Wide/multibyte conversions | | | | |
| mbsinit(C95) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstowcsmbstowcs_s(C11) | | | | | | btowc(C95) | | | | | | mbrtowc(C95) | | | | | | mbsrtowcsmbsrtowcs_s(C95)(C11) | | | | | | mbrtoc8(C23) | | | | | | c8rtomb(C23) | | | | | | mbrtoc16(C11) | | | | | | c16rtomb(C11) | | | | | | c32rtomb(C11) | | | | | | mbrtoc32(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbtowc | | | | | | wctombwctomb_s(C11) | | | | | | wcstombswcstombs_s(C11) | | | | | | wctob(C95) | | | | | | wcrtombwcrtomb_s(C95)(C11) | | | | | | wcsrtombswcsrtombs_s(C95)(C11) | | | | | | mbrlen(C95) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstate_t(C95) | | | | | | ****char8_t****(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | char16_t(C11) | | | | | | char32_t(C11) | | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_CUR_MAX | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<uchar.h>` |  |  |
| typedef unsigned char char8_t; |  | (since C23) |
|  |  |  |

char8_t is an unsigned integer type used for UTF-8 and is the same type as unsigned char.

### Example

Run this code

```
#include <stdio.h>
#include <uchar.h>
 
int main(void)
{
    char8_t str[] = u8"zß水🍌"; // or "z\u00df\u6c34\U0001f34c"
    size_t str_sz = sizeof str; // sizeof *str == 1 by definition
    printf("%zu UTF-8 code units: [ ", str_sz);
    for (size_t n = 0; n < str_sz; ++n)
        printf("%02X ", str[n]);
    printf("]\n");
}

```

Possible output:

```
11 UTF-8 code units: [ 7A C3 9F E6 B0 B4 F0 9F 8D 8C 00 ]

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.30 Unicode utilities <uchar.h> (p: 410)

### See also

|  |  |
| --- | --- |
| C++ documentation for Fundamental types | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/multibyte/char8_t&oldid=179241>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 January 2025, at 22:32.