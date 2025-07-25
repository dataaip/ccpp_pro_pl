# std::chrono::parse

From cppreference.com
< cpp‎ | chrono
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
| ****parse****(C++20) | | | | |
| C-style date and time | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| template< class CharT, class Parsable >  /\* unspecified \*/ parse( const CharT\* fmt, Parsable& tp ); | (1) | (since C++20) |
| template< class CharT, class Traits, class Alloc, class Parsable >  /\* unspecified \*/ parse( const std::basic_string<CharT, Traits, Alloc>& fmt,                          Parsable& tp ); | (2) | (since C++20) |
| template< class CharT, class Traits, class Alloc, class Parsable >  /\* unspecified \*/ parse( const CharT\* fmt, Parsable& tp, std::basic_string<CharT, Traits, Alloc>& abbrev ); | (3) | (since C++20) |
| template< class CharT, class Traits, class Alloc, class Parsable >  /\* unspecified \*/ parse( const std::basic_string<CharT, Traits, Alloc>& fmt,                           Parsable& tp, std::basic_string<CharT, Traits, Alloc>& abbrev ); | (4) | (since C++20) |
| template< class CharT, class Parsable >  /\* unspecified \*/ parse( const CharT\* fmt, Parsable& tp, std::chrono::minutes& offset ); | (5) | (since C++20) |
| template< class CharT, class Traits, class Alloc, class Parsable >  /\* unspecified \*/ parse( const std::basic_string<CharT, Traits, Alloc>& fmt,                          Parsable& tp, std::chrono::minutes& offset ); | (6) | (since C++20) |
| template< class CharT, class Traits, class Alloc, class Parsable >  /\* unspecified \*/ parse( const CharT\* fmt, Parsable& tp,                           std::basic_string<CharT, Traits, Alloc>& abbrev, std::chrono::minutes& offset ); | (7) | (since C++20) |
| template< class CharT, class Traits, class Alloc, class Parsable >  /\* unspecified \*/ parse( const std::basic_string<CharT, Traits, Alloc>& fmt,                           Parsable& tp,                           std::basic_string<CharT, Traits, Alloc>& abbrev, std::chrono::minutes& offset ); | (8) | (since C++20) |
|  |  |  |

Returns an object `manip` of unspecified type such that, given a std::basic_istream<CharT, Traits> object `is`, the expression is >> manip calls `from_stream` (unqualified, to enable argument-dependent lookup) as follows:

1) from_stream(is, fmt, tp)2) from_stream(is, fmt.c_str(), tp)3) from_stream(is, fmt, tp, std::addressof(abbrev))4) from_stream(is, fmt.c_str(), tp, std::addressof(abbrev))5) from_stream(is, fmt, tp,  
            static_cast<std::basic_string<CharT, Traits, Alloc>\*>(nullptr), &offset)6) from_stream(is, fmt.c_str(), tp,  
            static_cast<std::basic_string<CharT, Traits, Alloc>\*>(nullptr), &offset)7) from_stream(is, fmt, tp, std::addressof(abbrev), &offset)8) from_stream(is, fmt.c_str(), tp, std::addressof(abbrev), &offset).

The expression is >> manip is an lvalue of type std::basic_istream<CharT, Traits> with the value `is`.

These overloads participate in overload resolution only if the corresponding `from_stream` expression is well-formed.

Implementations are recommended to make it difficult to use potentially dangling references to the format string, e.g., by making return types non-movable and preventing operator>> from accepting lvalues of return types.

### Parameters

|  |  |  |
| --- | --- | --- |
| fmt | - | a format string (see below) |
| tp | - | object to hold the parse result |
| abbrev | - | string to hold the time zone abbreviation or name corresponding to the `%Z` specifier |
| offset | - | duration to represent the offset from UTC corresponding to the `%z` specifier |

### Format string

The format string consists of zero or more conversion specifiers and ordinary characters. Each ordinary character, excluding whitespace characters and the terminating null character, matches one identical character from the input stream, or causes the function to fail if the next character on the stream does not compare equal.

Each whitespace character matches zero or more whitespace characters in the input stream.

Each unmodified conversion specifier begins with a `%` character followed by a character that determines the behavior of the specifier. Some conversion specifiers have a modified form in which an `E` or `O` modifier character is inserted after the `%` character. Some conversion specifiers have a modified form in which a width parameter given as a positive decimal integer (shown as **`N`** below) is inserted after the `%` character. Each conversion specifier causes the matched characters to be interpreted as parts of date and time types according to the table below.

A character sequence in the format string that begins with a `%` but does not match one of the conversion specifiers below is interpreted as ordinary characters.

If `from_stream` fails to parse everything specified by the format string, or if insufficient information is parsed to specify a complete result, or if parsing discloses contradictory information, is.setstate(std::ios_base::failbit) is called.

The following conversion specifiers are available:

| Conversion  specifier | Explanation |
| --- | --- |
| `%%` | Matches a literal `%` character. |
| `%n` | Matches one whitespace character. |
| `%t` | Matches zero or one whitespace character. |
| Year | | |
| `%C`   `%NC`   `%EC` | Parses the century as a decimal number. The width **N** specifies the maximum number of characters to read. The default width is 2. Leading zeroes are permitted but not required. The modified command `%EC` interprets the locale's alternative representation of the century. |
| `%y`   `%Ny`   `%Ey`   `%Oy` | Parses the last two decimal digits of the year. If the century is not otherwise specified (e.g. with %C), values in the range [69, 99] are presumed to refer to the years 1969 to 1999, and values in the range [00, 68] are presumed to refer to the years 2000 to 2068. The width **N** specifies the maximum number of characters to read. The default width is 2. Leading zeroes are permitted but not required. The modified commands `%Ey` and `%Oy` interpret the locale's alternative representation. |
| `%Y`   `%NY`   `%EY` | Parses the year as a decimal number. The width **N** specifies the maximum number of characters to read. The default width is 4. Leading zeroes are permitted but not required. The modified command `%EY` interprets the locale's alternative representation. |
| Month | | |
| `%b` `%B` `%h` | Parses the locale's full or abbreviated case-insensitive month name. |
| `%m`  `%Nm` `%Om` | Parses the month as a decimal number (January is `1`). The width **N** specifies the maximum number of characters to read. The default width is 2. Leading zeroes are permitted but not required. The modified command `%Om` interprets the locale's alternative representation. |
| Day | | |
| `%d` `%Nd` `%Od` `%e`  `%Ne` `%Oe` | Parses the day of month as a decimal number. The width **N** specifies the maximum number of characters to read. The default width is 2. Leading zeroes are permitted but not required. The modified commands `%Od` and `%Oe` interpret the locale's alternative representation. |
| Day of the week | | |
| `%a` `%A` | Parses the locale's full or abbreviated case-insensitive weekday name. |
| `%u` `%Nu` | Parses the ISO weekday as a decimal number (1-7), where Monday is `1`. The width **N** specifies the maximum number of characters to read. The default width is 1. Leading zeroes are permitted but not required. |
| `%w` `%Nw` `%Ow` | Parses the weekday as a decimal number (0-6), where Sunday is `0`. The width **N** specifies the maximum number of characters to read. The default width is 1. Leading zeroes are permitted but not required. The modified command `%Ow` interprets the locale's alternative representation. |
| ISO 8601 week-based year | | |
| In ISO 8601 weeks begin with Monday and the first week of the year must satisfy the following requirements:   - Includes January 4 - Includes first Thursday of the year | | |
| `%g` `%Ng` | Parses the last two decimal digits of the ISO 8601 week-based year. The width **N** specifies the maximum number of characters to read. The default width is 2. Leading zeroes are permitted but not required. |
| `%G` `%NG` | Parses the ISO 8601 week-based year as a decimal number. The width **N** specifies the maximum number of characters to read. The default width is 4. Leading zeroes are permitted but not required. |
| `%V` `%NV` | Parses the ISO 8601 week of the year as a decimal number. The width **N** specifies the maximum number of characters to read. The default width is 2. Leading zeroes are permitted but not required. |
| Week/day of the year | | |
| `%j` `%Nj` | Parses the day of the year as a decimal number (January 1 is `1`). The width **N** specifies the maximum number of characters to read. The default width is 3. Leading zeroes are permitted but not required. |
| `%U` `%NU` `%OU` | Parses the week number of the year as a decimal number. The first Sunday of the year is the first day of week 01. Days of the same year prior to that are in week 00. The width **N** specifies the maximum number of characters to read. The default width is 2. Leading zeroes are permitted but not required. The modified command `%OU` interprets the locale's alternative representation. |
| `%W` `%NW` `%OW` | Parses the week number of the year as a decimal number. The first Monday of the year is the first day of week 01. Days of the same year prior to that are in week 00. The width **N** specifies the maximum number of characters to read. The default width is 2. Leading zeroes are permitted but not required. The modified command `%OW` interprets the locale's alternative representation. |
| Date | | |
| `%D` | Equivalent to `"%m/%d/%y"`. |
| `%F` `%NF` | Equivalent to `"%Y-%m-%d"`. If the width is specified, it is only applied to the `%Y`. |
| `%x` `%Ex` | Parses the locale's date representation. The modified command `%Ex` interprets the locale's alternate date representation. |
| Time of day | | |
| `%H` `%NH` `%OH` | Parses the hour (24-hour clock) as a decimal number. The width **N** specifies the maximum number of characters to read. The default width is 2. Leading zeroes are permitted but not required. The modified command `%OH` interprets the locale's alternative representation. |
| `%I` `%NI` `%OI` | Parses the hour (12-hour clock) as a decimal number. The width **N** specifies the maximum number of characters to read. The default width is 2. Leading zeroes are permitted but not required. The modified command `%OI` interprets the locale's alternative representation. |
| `%M` `%NM` `%OM` | Parses the minute as a decimal number. The width **N** specifies the maximum number of characters to read. The default width is 2. Leading zeroes are permitted but not required. The modified command `%OM` interprets the locale's alternative representation. |
| `%S` `%NS` `%OS` | Parses the second as a decimal number. The width **N** specifies the maximum number of characters to read. The default width is 2. Leading zeroes are permitted but not required. The modified command `%OS` interprets the locale's alternative representation. |
| `%p` | Parses the locale's equivalent of the AM/PM designations associated with a 12-hour clock. |
| `%R` | Equivalent to `"%H:%M"`. |
| `%T` | Equivalent to `"%H:%M:%S"`. |
| `%r` | Parses the locale's 12-hour clock time. |
| `%X` `%EX` | Parses the locale's time representation. The modified command `%EX` interprets the locale's alternate time representation. |
| Miscellaneous | | |
| `%c` `%Ec` | Parses the locale's date and time representation. The modified command `%Ec` interprets the locale's alternative date and time representation. |
| `%z` `%Ez` `%Oz` | Parses the offset from UTC in the format `[+|-]hh[mm]`. For example `-0430` refers to 4 hours 30 minutes behind UTC and `04` refers to 4 hours ahead of UTC. The modified commands `%Ez` and `%Oz` parses the format `[+|-]h[h][:mm]` (i.e., requiring a `:` between the hours and minutes and making the leading zero for hour optional). |
| `%Z` | Parses the time zone abbreviation or name, taken as the longest sequence of characters that only contains the characters `A` through `Z`, `a` through `z`, `0` through `9`, `-`, `+`, `_`, and `/`. |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3554 | C++20 | overloads for plain null-terminated character type sequences were missing | added |

### See also

|  |  |
| --- | --- |
| from_stream(std::chrono::sys_time)(C++20) | parses a `sys_time` from a stream according to the provided format   (function template) |
| from_stream(std::chrono::utc_time)(C++20) | parses a `utc_time` from a stream according to the provided format   (function template) |
| from_stream(std::chrono::tai_time)(C++20) | parses a `tai_time` from a stream according to the provided format   (function template) |
| from_stream(std::chrono::gps_time)(C++20) | parses a `gps_time` from a stream according to the provided format   (function template) |
| from_stream(std::chrono::file_time)(C++20) | parses a `file_time` from a stream according to the provided format   (function template) |
| from_stream(std::chrono::local_time)(C++20) | parses a `local_time` from a stream according to the provided format   (function template) |
| from_stream(C++20) | parses a `year` from a stream according to the provided format   (function template) |
| from_stream(C++20) | parses a `month` from a stream according to the provided format   (function template) |
| from_stream(C++20) | parses a `day` from a stream according to the provided format   (function template) |
| from_stream(C++20) | parses a `weekday` from a stream according to the provided format   (function template) |
| from_stream(C++20) | parses a `month_day` from a stream according to the provided format   (function template) |
| from_stream(C++20) | parses a `year_month` from a stream according to the provided format   (function template) |
| from_stream(C++20) | parses a `year_month_day` from a stream according to the provided format   (function template) |
| get_time(C++11) | parses a date/time value of specified format   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/parse&oldid=139618>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 May 2022, at 04:01.