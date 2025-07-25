# asctime, asctime_s

From cppreference.com
< c‎ | chrono
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

 Date and time utilities

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Time manipulation | | | | |
| difftime | | | | |
| time | | | | |
| clock | | | | |
| timespec_get(C11) | | | | |
| timespec_getres(C23) | | | | |
| Format conversions | | | | |
| ****asctimeasctime_s****(deprecated in C23)(C11) | | | | |
| ctimectime_s(deprecated in C23)(C11) | | | | |
| strftime | | | | |
| wcsftime(C95) | | | | |
| gmtimegmtime_rgmtime_s(C23)(C11) | | | | |
| localtimelocaltime_rlocaltime_s(C23)(C11) | | | | |
| mktime | | | | |
| Constants | | | | |
| CLOCKS_PER_SEC | | | | |
| Types | | | | |
| tm | | | | |
| time_t | | | | |
| clock_t | | | | |
| timespec(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<time.h>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| char\*                asctime( const struct tm\* time_ptr ); |  | (until C23) |
| [[deprecated]] char\* asctime( const struct tm\* time_ptr ); |  | (since C23) |
|  |  |  |
| --- | --- | --- |
| errno_t asctime_s( char\* buf, rsize_t bufsz, const struct tm\* time_ptr ); | (2) | (since C11) |
|  |  |  |

1) Converts given calendar time tm to a textual representation of the following fixed 25-character form: Www Mmm dd hh:mm:ss yyyy\n

- `Www` - three-letter English abbreviated day of the week from time_ptr->tm_wday, one of `Mon`, `Tue`, `Wed`, `Thu`, `Fri`, `Sat`, `Sun`.
- `Mmm` - three-letter English abbreviated month name from time_ptr->tm_mon, one of `Jan`, `Feb`, `Mar`, `Apr`, `May`, `Jun`, `Jul`, `Aug`, `Sep`, `Oct`, `Nov`, `Dec`.
- `dd` - 2-digit day of the month from timeptr->tm_mday as if printed by sprintf using %2d.
- `hh` - 2-digit hour from timeptr->tm_hour as if printed by sprintf using %.2d.
- `mm` - 2-digit minute from timeptr->tm_min as if printed by sprintf using %.2d.
- `ss` - 2-digit second from timeptr->tm_sec as if printed by sprintf using %.2d.
- `yyyy` - 4-digit year from timeptr->tm_year + 1900 as if printed by sprintf using %4d.
 The behavior is undefined if any member of \*time_ptr is outside its normal range. The behavior is undefined if the calendar year indicated by time_ptr->tm_year has more than 4 digits or is less than the year 1000. The function does not support localization, and the newline character cannot be removed. The function modifies static storage and is not thread-safe.

|  |  |
| --- | --- |
| This function is deprecated and should not be used in new code. | (since C23) |

2) Same as (1), except that the message is written into user-provided storage buf, which is guaranteed to be null-terminated, and the following errors are detected at runtime and call the currently installed constraint handler function:

:   - buf or time_ptr is a null pointer
    - bufsz is less than 26 or greater than RSIZE_MAX
    - not all members of \*time_ptr are within their normal ranges
    - the year indicated by time_ptr->tm_year is less than 0 or greater than 9999.
:   As with all bounds-checked functions, `asctime_s` is only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including <time.h>.

### Parameters

|  |  |  |
| --- | --- | --- |
| time_ptr | - | pointer to a tm object specifying the time to print |
| buf | - | pointer to a user-supplied buffer at least 26 bytes in length |
| bufsz | - | size of the user-supplied buffer |

### Return value

1) pointer to a static null-terminated character string holding the textual representation of date and time as described above. The string may be shared between `asctime` and ctime, and may be overwritten on each invocation of any of those functions.2) zero on success, non-zero on failure, in which case buf[0] is set to zero (unless buf is a null pointer or bufsz is zero or greater than RSIZE_MAX).

### Notes

`asctime` returns a pointer to static data and is not thread-safe. POSIX marks this function obsolete and recommends strftime instead. The C standard also recommends strftime instead of `asctime` and `asctime_s` because `strftime` is more flexible and locale-sensitive.

POSIX limits undefined behaviors only to when the output string would be longer than 25 characters, when timeptr->tm_wday or timeptr->tm_mon are not within the expected ranges, or when timeptr->tm_year exceeds INT_MAX - 1990.

Some implementations handle timeptr->tm_mday == 0 as meaning the last day of the preceding month.

### Example

Run this code

```
#define __STDC_WANT_LIB_EXT1__ 1
#include <stdio.h>
#include <time.h>
 
int main(void)
{
    struct tm tm = *localtime(&(time_t){time(NULL)});
    printf("%s", asctime(&tm)); // note implicit trailing '\n'
 
#ifdef __STDC_LIB_EXT1__
    char str[26];
    asctime_s(str, sizeof str, &tm);
    printf("%s", str);
#endif
}

```

Possible output:

```
Tue May 26 21:51:50 2015
Tue May 26 21:51:50 2015

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.27.2.1 The asctime function (p: 287)

:   - K.3.8.2.1 The asctime_s function (p: 453-454)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.27.2.1 The asctime function (p: 392-393)

:   - K.3.8.2.1 The asctime_s function (p: 624-625)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.23.3.1 The asctime function (p: 341-342)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.12.3.1 The asctime function

### See also

|  |  |
| --- | --- |
| ctimectime_s(deprecated in C23)(C11) | converts a time_t object to a textual representation   (function) |
| strftime | converts a tm object to custom textual representation   (function) |
| C++ documentation for asctime | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/chrono/asctime&oldid=172468>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 June 2024, at 16:57.