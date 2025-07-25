# std::asctime

From cppreference.com
< cpp‎ | chrono‎ | c
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

Date and time library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Time point | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | time_point(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clock_time_conversion(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clock_cast(C++20) | | | | | |
| Duration | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration(C++11) | | | | | |
| Clocks | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | system_clock(C++11) | | | | | | steady_clock(C++11) | | | | | | is_clock(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | utc_clock(C++20) | | | | | | tai_clock(C++20) | | | | | | high_resolution_clock(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | gps_clock(C++20) | | | | | | file_clock(C++20) | | | | | | local_t(C++20) | | | | | |
| Time of day | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_amis_pm(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | make12make24(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hh_mm_ss(C++20) | | | | | |  | | | | | |
| Calendar | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

C-style date and time utilities

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Time manipulation | | | | |
| difftime | | | | |
| time | | | | |
| clock | | | | |
| timespec_get(C++17) | | | | |
| Format conversions | | | | |
| ****asctime**** | | | | |
| ctime | | | | |
| strftime | | | | |
| wcsftime | | | | |
| gmtime | | | | |
| localtime | | | | |
| mktime | | | | |
| Constants | | | | |
| CLOCKS_PER_SEC | | | | |
| Types | | | | |
| tm | | | | |
| time_t | | | | |
| clock_t | | | | |
| timespec(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ctime>` |  |  |
| char\* asctime( const std::tm\* time_ptr ); |  |  |
|  |  |  |

Converts given calendar time std::tm to a textual representation of the following fixed 25-character form: Www Mmm dd hh:mm:ss yyyy\n.

- `Www` - three-letter English abbreviated day of the week from time_ptr->tm_wday, one of `Mon`, `Tue`, `Wed`, `Thu`, `Fri`, `Sat`, `Sun`.
- `Mmm` - three-letter English abbreviated month name from time_ptr->tm_mon, one of `Jan`, `Feb`, `Mar`, `Apr`, `May`, `Jun`, `Jul`, `Aug`, `Sep`, `Oct`, `Nov`, `Dec`.
- `dd` - 2-digit day of the month from timeptr->tm_mday as if printed by sprintf using %2d.
- `hh` - 2-digit hour from timeptr->tm_hour as if printed by sprintf using %.2d.
- `mm` - 2-digit minute from timeptr->tm_min as if printed by sprintf using %.2d.
- `ss` - 2-digit second from timeptr->tm_sec as if printed by sprintf using %.2d.
- `yyyy` - 4-digit year from timeptr->tm_year + 1900 as if printed by sprintf using %4d.

The behavior is undefined if any member of \*time_ptr is outside its normal range.

The behavior is undefined if the calendar year indicated by time_ptr->tm_year has more than 4 digits or is less than the year 1000.

The function does not support localization, and the newline character cannot be removed.

The function modifies static storage and is not thread-safe.

### Parameters

|  |  |  |
| --- | --- | --- |
| time_ptr | - | pointer to a std::tm object specifying the time to print |

### Return value

Pointer to a static null-terminated character string holding the textual representation of date and time. The string may be shared between `std::asctime` and std::ctime, and may be overwritten on each invocation of any of those functions.

### Notes

This function returns a pointer to static data and is not thread-safe. POSIX marks this function obsolete and recommends locale-dependent std::strftime instead. In std::locale`("C")` the std::strftime format string "%c\n" will be an exact match to `std::asctime` output, while in other locales the format string "%a %b %e %H:%M:%S %Y\n" will be a potentially closer but not always exact match.

POSIX limits undefined behaviors only to the cases when the output string would be longer than 25 characters, when `timeptr->tm_wday` or `timeptr->tm_mon` are not within the expected ranges, or when `timeptr->tm_year` exceeds INT_MAX-1990.

Some implementations handle timeptr->tm_mday == 0 as meaning the last day of the preceding month.

### Example

Run this code

```
#include <ctime>
#include <iomanip>
#include <iostream>
 
int main()
{
    const std::time_t now = std::time(nullptr);
 
    for (const char* localeName : {"C", "en_US.utf8", "de_DE.utf8", "ja_JP.utf8"})
    {
        std::cout << "locale " << localeName << ":\n" << std::left;
        std::locale::global(std::locale(localeName));
 
        std::cout << std::setw(40) << "    asctime" << std::asctime(std::localtime(&now));
 
        // strftime output for comparison:
        char buf[64];
        if (strftime(buf, sizeof buf, "%c\n", std::localtime(&now)))
            std::cout << std::setw(40) << "    strftime %c" << buf;
 
        if (strftime(buf, sizeof buf, "%a %b %e %H:%M:%S %Y\n", std::localtime(&now)))
            std::cout << std::setw(40) << "    strftime %a %b %e %H:%M:%S %Y" << buf;
 
        std::cout << '\n';
    }
}

```

Possible output:

```
locale C:
    asctime                             Wed Nov  4 00:45:01 2020
    strftime %c                         Wed Nov  4 00:45:01 2020
    strftime %a %b %e %H:%M:%S %Y       Wed Nov  4 00:45:01 2020
 
locale en_US.utf8:
    asctime                             Wed Nov  4 00:45:01 2020
    strftime %c                         Wed 04 Nov 2020 12:45:01 AM UTC
    strftime %a %b %e %H:%M:%S %Y       Wed Nov  4 00:45:01 2020
 
locale de_DE.utf8:
    asctime                             Wed Nov  4 00:45:01 2020
    strftime %c                         Mi 04 Nov 2020 00:45:01 UTC
    strftime %a %b %e %H:%M:%S %Y       Mi Nov  4 00:45:01 2020
 
locale ja_JP.utf8:
    asctime                             Wed Nov  4 00:45:01 2020
    strftime %c                         2020年11月04日 00時45分01秒
    strftime %a %b %e %H:%M:%S %Y       水 11月  4 00:45:01 2020

```

### See also

|  |  |
| --- | --- |
| ctime | converts a std::time_t object to a textual representation   (function) |
| strftime | converts a std::tm object to custom textual representation   (function) |
| put_time(C++11) | formats and outputs a date/time value according to the specified format   (function template) |
| C documentation for asctime | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/c/asctime&oldid=161516>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 October 2023, at 00:24.