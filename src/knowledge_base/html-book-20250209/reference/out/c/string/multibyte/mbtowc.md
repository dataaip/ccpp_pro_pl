# mbtowc

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstowcsmbstowcs_s(C11) | | | | | | btowc(C95) | | | | | | mbrtowc(C95) | | | | | | mbsrtowcsmbsrtowcs_s(C95)(C11) | | | | | | mbrtoc8(C23) | | | | | | c8rtomb(C23) | | | | | | mbrtoc16(C11) | | | | | | c16rtomb(C11) | | | | | | c32rtomb(C11) | | | | | | mbrtoc32(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | ****mbtowc**** | | | | | | wctombwctomb_s(C11) | | | | | | wcstombswcstombs_s(C11) | | | | | | wctob(C95) | | | | | | wcrtombwcrtomb_s(C95)(C11) | | | | | | wcsrtombswcsrtombs_s(C95)(C11) | | | | | | mbrlen(C95) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstate_t(C95) | | | | | | char8_t(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | char16_t(C11) | | | | | | char32_t(C11) | | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_CUR_MAX | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdlib.h>` |  |  |
| int mbtowc( wchar_t\*          pwc, const char\*          s, size_t n ) |  | (until C99) |
| int mbtowc( wchar_t\* restrict pwc, const char\* restrict s, size_t n ) |  | (since C99) |
|  |  |  |

Converts a multibyte character whose first byte is pointed to by s to a wide character, written to \*pwc if pwc is not null.

If s is a null pointer, resets the global conversion state and determines whether shift sequences are used.

### Notes

Each call to `mbtowc` updates the internal global conversion state (a static object of type mbstate_t, known only to this function). If the multibyte encoding uses shift states, care must be taken to avoid backtracking or multiple scans. In any case, multiple threads should not call `mbtowc` without synchronization: mbrtowc may be used instead.

### Parameters

|  |  |  |
| --- | --- | --- |
| pwc | - | pointer to the wide character for output |
| s | - | pointer to the multibyte character |
| n | - | limit on the number of bytes in s that can be examined |

### Return value

If s is not a null pointer, returns the number of bytes that are contained in the multibyte character or -1 if the first bytes pointed to by s do not form a valid multibyte character or ​0​ if s is pointing at the null character '\0'.

If s is a null pointer, resets its internal conversion state to represent the initial shift state and returns ​0​ if the current multibyte encoding is not state-dependent (does not use shift sequences) or a non-zero value if the current multibyte encoding is state-dependent (uses shift sequences).

### Example

Run this code

```
#include <locale.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <wchar.h>
 
// print multibyte string to wide-oriented stdout
// equivalent to wprintf(L"%s\n", ptr);
void print_mb(const char* ptr)
{
    mbtowc(NULL, NULL, 0); // reset the conversion state
    const char* end = ptr + strlen(ptr);
    int ret = 0;
    for (wchar_t wc; (ret = mbtowc(&wc, ptr, end - ptr)) > 0; ptr += ret)
        wprintf(L"%lc", wc);
    wprintf(L"\n");
}
 
int main(void)
{
    setlocale(LC_ALL, "en_US.utf8");
    // UTF-8 narrow multibyte encoding
    print_mb("z\u00df\u6c34\U0001F34C"); // or "zß水🍌"
}

```

Output:

```
zß水🍌

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.24.7.2 The mbtowc function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.22.7.2 The mbtowc function (p: 260)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.22.7.2 The mbtowc function (p: 358)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.20.7.2 The mbtowc function (p: 322)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.10.7.2 The mbtowc function

### See also

|  |  |
| --- | --- |
| mbrtowc(C95) | converts the next multibyte character to wide character, given state   (function) |
| mblen | returns the number of bytes in the next multibyte character   (function) |
| C++ documentation for mbtowc | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/multibyte/mbtowc&oldid=172144>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 May 2024, at 09:42.