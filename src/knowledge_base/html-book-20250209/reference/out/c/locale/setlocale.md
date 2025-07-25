# setlocale

From cppreference.com
< c‎ | locale
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

 Localization support

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****setlocale**** | | | | |
| localeconv | | | | |
| lconv | | | | |
| Locale categories | | | | |
| LC_ALLLC_COLLATELC_CTYPELC_MONETARYLC_NUMERICLC_TIME | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<locale.h>` |  |  |
| char\* setlocale( int category, const char\* locale ); |  |  |
|  |  |  |

The `setlocale` function installs the specified system locale or its portion as the new C locale. The modifications remain in effect and influences the execution of all locale-sensitive C library functions until the next call to `setlocale`. If `locale` is a null pointer, `setlocale` queries the current C locale without modifying it.

### Parameters

|  |  |  |
| --- | --- | --- |
| category | - | locale category identifier, one of the `LC_xxx` macros. May be null. |
| locale | - | system-specific locale identifier. Can be "" for the user-preferred locale or "C" for the minimal locale |

### Return value

pointer to a narrow null-terminated string identifying the C locale after applying the changes, if any, or null pointer on failure.

A copy of the returned string along with the category used in this call to `setlocale` may be used later in the program to restore the locale back to the state at the end of this call.

### Notes

During program startup, the equivalent of setlocale(LC_ALL, "C"); is executed before any user code is run.

Although the return type is char\*, modifying the pointed-to characters is undefined behavior.

Because `setlocale` modifies global state which affects execution of locale-dependent functions, it is undefined behavior to call it from one thread, while another thread is executing any of the following functions: fprintf, isprint, iswdigit, localeconv, tolower, fscanf, ispunct, iswgraph, mblen, toupper, isalnum, isspace, iswlower, mbstowcs, towlower, isalpha, isupper, iswprint, mbtowc, towupper, isblank, iswalnum, iswpunct, `setlocale`, wcscoll, iscntrl, iswalpha, iswspace, strcoll, wcstod, isdigit, iswblank, iswupper, strerror, wcstombs, isgraph, iswcntrl, iswxdigit, strtod, wcsxfrm, islower, iswctype, isxdigit.

POSIX also defines a locale named "POSIX", which is always accessible and is exactly equivalent to the default minimal "C" locale.

POSIX also specifies that the returned pointer, not just the contents of the pointed-to string, may be invalidated by subsequent calls to `setlocale`.

### Example

Run this code

```
#include <locale.h>
#include <stdio.h>
#include <time.h>
#include <wchar.h>
 
int main(void)
{
    // the C locale will be UTF-8 enabled English;
    // decimal dot will be German
    // date and time formatting will be Japanese
    setlocale(LC_ALL, "en_US.UTF-8");
    setlocale(LC_NUMERIC, "de_DE.utf8");
    setlocale(LC_TIME, "ja_JP.utf8");
 
    wchar_t str[100];
    time_t t = time(NULL);
    wcsftime(str, 100, L"%A %c", localtime(&t));
    wprintf(L"Number: %.2f\nDate: %ls\n", 3.14, str);
}

```

Possible output:

```
Number: 3,14
Date: 月曜日 2017年09月25日 13時00分15秒

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.11.1.1 The setlocale function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.11.1.1 The setlocale function (p: 163-164)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.11.1.1 The setlocale function (p: 224-225)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.11.1.1 The setlocale function (p: 205-206)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.4.1.1 The setlocale function

### See also

|  |  |
| --- | --- |
| LC_ALLLC_COLLATELC_CTYPELC_MONETARYLC_NUMERICLC_TIME | locale categories for ****setlocale****   (macro constant) |
| C++ documentation for setlocale | |

### External links

|  |  |
| --- | --- |
| 1. | List of Windows locale names. |
| 2. | List of Linux locale names. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/locale/setlocale&oldid=180065>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 February 2025, at 20:20.