# std::put_time

From cppreference.com
< cpp‎ | io‎ | manip
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

Input/output library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| I/O manipulators | | | | |
| Print functions (C++23) | | | | |
| C-style I/O | | | | |
| Buffers | | | | |
| basic_streambuf | | | | |
| basic_filebuf | | | | |
| basic_stringbuf | | | | |
| basic_spanbuf(C++23) | | | | |
| strstreambuf(C++98/26\*) | | | | |
| basic_syncbuf(C++20) | | | | |
| Streams | | | | |
| Abstractions | | | | |
| ios_base | | | | |
| basic_ios | | | | |
| basic_istream | | | | |
| basic_ostream | | | | |
| basic_iostream | | | | |
| File I/O | | | | |
| basic_ifstream | | | | |
| basic_ofstream | | | | |
| basic_fstream | | | | |
| String I/O | | | | |
| basic_istringstream | | | | |
| basic_ostringstream | | | | |
| basic_stringstream | | | | |
| Array I/O | | | | |
| basic_ispanstream(C++23) | | | | |
| basic_ospanstream(C++23) | | | | |
| basic_spanstream(C++23) | | | | |
| istrstream(C++98/26\*) | | | | |
| ostrstream(C++98/26\*) | | | | |
| strstream(C++98/26\*) | | | | |
| Synchronized Output | | | | |
| basic_osyncstream(C++20) | | | | |
| Types | | | | |
| streamoff | | | | |
| streamsize | | | | |
| fpos | | | | |
| Error category interface | | | | |
| iostream_category(C++11) | | | | |
| io_errc(C++11) | | | | |

Input/output manipulators

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Floating-point formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | showpointnoshowpoint | | | | | | setprecision | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fixedscientifichexfloatdefaultfloat(C++11)(C++11) | | | | | |
| Integer formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setbase | | | | | | showbasenoshowbase | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | dechexoct | | | | | |
| Boolean formatting | | | | |
| boolalphanoboolalpha | | | | |
| Field width and fill control | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setfill | | | | | | setw | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | internalleftright | | | | | |
| Other formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | showposnoshowpos | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uppercasenouppercase | | | | | |
| Whitespace processing | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ws | | | | | | ends | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | skipwsnoskipws | | | | | |
| Output flushing | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | flush | | | | | | endl | | | | | | flush_emit(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | unitbufnounitbuf | | | | | | emit_on_flushnoemit_on_flush(C++20)(C++20) | | | | | |
| Status flags manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | resetiosflags | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setiosflags | | | | | |
| Time and money I/O | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | get_money(C++11) | | | | | | get_time(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | put_money(C++11) | | | | | | ****put_time****(C++11) | | | | | |
| Quoted manipulator | | | | |
| quoted(C++14) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<iomanip>` |  |  |
| template< class CharT >  /\*unspecified\*/ put_time( const std::tm\* tmb, const CharT\* fmt ); |  | (since C++11) |
|  |  |  |

When used in an expression out << put_time(tmb, fmt), converts the date and time information from a given calendar time tmb to a character string according to format string fmt, as if by calling std::strftime, std::wcsftime, or analog (depending on `CharT`), according to the std::time_put facet of the locale currently imbued in the output stream out.

### Parameters

|  |  |  |
| --- | --- | --- |
| tmb | - | pointer to the calendar time structure as obtained from std::localtime or std::gmtime |
| fmt | - | pointer to a null-terminated `CharT` string specifying the format of conversion |

### Format string

The format string consists of zero or more conversion specifiers and ordinary characters (except `%`). All ordinary characters, including the terminating null character, are copied to the output string without modification. Each conversion specification begins with `%` character, optionally followed by `E` or `O` modifier (ignored if unsupported by the locale), followed by the character that determines the behavior of the specifier. The following format specifiers are available:

| Conversion  specifier | Explanation | Used fields |
| --- | --- | --- |
| `%` | writes literal `%`. The full conversion specification must be `%%`. |  |
| `n` (C++11) | writes newline character |  |
| `t` (C++11) | writes horizontal tab character |  |
| Year | | |
| `Y` | writes ****year**** as a decimal number, e.g. 2017 | `tm_year` |
| `EY` (C++11) | writes ****year**** in the alternative representation, e.g.平成23年 (year Heisei 23) instead of 2011年 (year 2011) in ja_JP locale | `tm_year` |
| `y` | writes last 2 digits of ****year**** as a decimal number (range `[00,99]`) | `tm_year` |
| `Oy` (C++11) | writes last 2 digits of ****year**** using the alternative numeric system, e.g. 十一 instead of 11 in ja_JP locale | `tm_year` |
| `Ey` (C++11) | writes ****year**** as offset from locale's alternative calendar period `%EC` (locale-dependent) | `tm_year` |
| `C` (C++11) | writes first 2 digits of ****year**** as a decimal number (range `[00,99]`) | `tm_year` |
| `EC` (C++11) | writes name of the ****base year (period)**** in the locale's alternative representation, e.g. 平成 (Heisei era) in ja_JP | `tm_year` |
| `G` (C++11) | writes ****ISO 8601 week-based year****, i.e. the year that contains the specified week. In ISO 8601 weeks begin with Monday and the first week of the year must satisfy the following requirements:   - Includes January 4 - Includes first Thursday of the year | `tm_year`, `tm_wday`, `tm_yday` |
| `g` (C++11) | writes last 2 digits of ****ISO 8601 week-based year****, i.e. the year that contains the specified week (range `[00,99]`). In ISO 8601 weeks begin with Monday and the first week of the year must satisfy the following requirements:   - Includes January 4 - Includes first Thursday of the year | `tm_year`, `tm_wday`, `tm_yday` |
| Month | | |
| `b` | writes ****abbreviated month**** name, e.g. `Oct` (locale dependent) | `tm_mon` |
| `h` (C++11) | synonym of `b` | `tm_mon` |
| `B` | writes ****full month**** name, e.g. `October` (locale dependent) | `tm_mon` |
| `m` | writes ****month**** as a decimal number (range `[01,12]`) | `tm_mon` |
| `Om` (C++11) | writes ****month**** using the alternative numeric system, e.g. 十二 instead of 12 in ja_JP locale | `tm_mon` |
| Week | | |
| `U` | writes ****week of the year**** as a decimal number (Sunday is the first day of the week) (range `[00,53]`) | `tm_year`, `tm_wday`, `tm_yday` |
| `OU` (C++11) | writes ****week of the year****, as by `%U`, using the alternative numeric system, e.g. 五十二 instead of 52 in ja_JP locale | `tm_year`, `tm_wday`, `tm_yday` |
| `W` | writes ****week of the year**** as a decimal number (Monday is the first day of the week) (range `[00,53]`) | `tm_year`, `tm_wday`, `tm_yday` |
| `OW` (C++11) | writes ****week of the year****, as by `%W`, using the alternative numeric system, e.g. 五十二 instead of 52 in ja_JP locale | `tm_year`, `tm_wday`, `tm_yday` |
| `V` (C++11) | writes ****ISO 8601 week of the year**** (range `[01,53]`). In ISO 8601 weeks begin with Monday and the first week of the year must satisfy the following requirements:   - Includes January 4 - Includes first Thursday of the year | `tm_year`, `tm_wday`, `tm_yday` |
| `OV` (C++11) | writes ****week of the year****, as by `%V`, using the alternative numeric system, e.g. 五十二 instead of 52 in ja_JP locale | `tm_year`, `tm_wday`, `tm_yday` |
| Day of the year/month | | |
| `j` | writes ****day of the year**** as a decimal number (range `[001,366]`) | `tm_yday` |
| `d` | writes ****day of the month**** as a decimal number (range `[01,31]`) | `tm_mday` |
| `Od` (C++11) | writes zero-based ****day of the month**** using the alternative numeric system, e.g. 二十七 instead of 27 in ja_JP locale Single character is preceded by a space. | `tm_mday` |
| `e` (C++11) | writes ****day of the month**** as a decimal number (range `[1,31]`). Single digit is preceded by a space. | `tm_mday` |
| `Oe` (C++11) | writes one-based ****day of the month**** using the alternative numeric system, e.g. 二十七 instead of 27 in ja_JP locale Single character is preceded by a space. | `tm_mday` |
| Day of the week | | |
| `a` | writes ****abbreviated weekday**** name, e.g. `Fri` (locale dependent) | `tm_wday` |
| `A` | writes ****full weekday**** name, e.g. `Friday` (locale dependent) | `tm_wday` |
| `w` | writes ****weekday**** as a decimal number, where Sunday is `0` (range `[0-6]`) | `tm_wday` |
| `Ow` (C++11) | writes ****weekday****, where Sunday is `0`, using the alternative numeric system, e.g. 二 instead of 2 in ja_JP locale | `tm_wday` |
| `u` (C++11) | writes ****weekday**** as a decimal number, where Monday is `1` (ISO 8601 format) (range `[1-7]`) | `tm_wday` |
| `Ou` (C++11) | writes ****weekday****, where Monday is `1`, using the alternative numeric system, e.g. 二 instead of 2 in ja_JP locale | `tm_wday` |
| Hour, minute, second | | |
| `H` | writes ****hour**** as a decimal number, 24 hour clock (range `[00-23]`) | `tm_hour` |
| `OH` (C++11) | writes ****hour**** from 24-hour clock using the alternative numeric system, e.g. 十八 instead of 18 in ja_JP locale | `tm_hour` |
| `I` | writes ****hour**** as a decimal number, 12 hour clock (range `[01,12]`) | `tm_hour` |
| `OI` (C++11) | writes ****hour**** from 12-hour clock using the alternative numeric system, e.g. 六 instead of 06 in ja_JP locale | `tm_hour` |
| `M` | writes ****minute**** as a decimal number (range `[00,59]`) | `tm_min` |
| `OM` (C++11) | writes ****minute**** using the alternative numeric system, e.g. 二十五 instead of 25 in ja_JP locale | `tm_min` |
| `S` | writes ****second**** as a decimal number (range `[00,60]`) | `tm_sec` |
| `OS` (C++11) | writes ****second**** using the alternative numeric system, e.g. 二十四 instead of 24 in ja_JP locale | `tm_sec` |
| Other | | |
| `c` | writes ****standard date and time string****, e.g. `Sun Oct 17 04:41:13 2010` (locale dependent) | all |
| `Ec` (C++11) | writes ****alternative date and time string****, e.g. using 平成23年 (year Heisei 23) instead of 2011年 (year 2011) in ja_JP locale | all |
| `x` | writes localized ****date representation**** (locale dependent) | all |
| `Ex` (C++11) | writes ****alternative date representation****, e.g. using 平成23年 (year Heisei 23) instead of 2011年 (year 2011) in ja_JP locale | all |
| `X` | writes localized ****time representation****, e.g. 18:40:20 or 6:40:20 PM (locale dependent) | all |
| `EX` (C++11) | writes ****alternative time representation**** (locale dependent) | all |
| `D` (C++11) | equivalent to ****"%m/%d/%y"**** | `tm_mon`, `tm_mday`, `tm_year` |
| `F` (C++11) | equivalent to ****"%Y-%m-%d"**** (the ISO 8601 date format) | `tm_mon`, `tm_mday`, `tm_year` |
| `r` (C++11) | writes localized ****12-hour clock**** time (locale dependent) | `tm_hour`, `tm_min`, `tm_sec` |
| `R` (C++11) | equivalent to ****"%H:%M"**** | `tm_hour`, `tm_min` |
| `T` (C++11) | equivalent to ****"%H:%M:%S"**** (the ISO 8601 time format) | `tm_hour`, `tm_min`, `tm_sec` |
| `p` | writes localized ****a.m. or p.m.**** (locale dependent) | `tm_hour` |
| `z` (C++11) | writes ****offset from UTC**** in the ISO 8601 format (e.g. `-0430`), or no characters if the time zone information is not available | `tm_isdst` |
| `Z` | writes locale-dependent ****time zone name or abbreviation****, or no characters if the time zone information is not available | `tm_isdst` |

### Return value

An object of unspecified type such that

- if out is an object of type std::basic_ostream<CharT, Traits>, the expression out << put_time(tmb, fmt)
  - has type std::basic_ostream<CharT, Traits>&
  - has value out
  - behaves as if it called f(out, tmb, fmt)

where the function f is defined as:

```
template<class CharT, class Traits>
void f(std::basic_ios<CharT, Traits>& str, const std::tm* tmb, const CharT* fmt)
{
    using Iter = std::ostreambuf_iterator<CharT, Traits>;
    using TimePut = std::time_put<CharT, Iter>;
 
    const TimePut& tp = std::use_facet<TimePut>(str.getloc());
    const Iter end = tp.put(Iter(str.rdbuf()), str, str.fill(), tmb,
        fmt, fmt + Traits::length(fmt));
 
    if (end.failed())
        str.setstate(std::ios_base::badbit);
}

```

### Example

Run this code

```
#include <ctime>
#include <iomanip>
#include <iostream>
 
int main()
{
    std::time_t t = std::time(nullptr);
    std::tm tm = *std::localtime(&t);
 
    std::cout.imbue(std::locale("ru_RU.utf8"));
    std::cout << "ru_RU: " << std::put_time(&tm, "%c %Z") << '\n';
 
    std::cout.imbue(std::locale("ja_JP.utf8"));
    std::cout << "ja_JP: " << std::put_time(&tm, "%c %Z") << '\n';
}

```

Possible output:

```
ru_RU: Ср. 28 дек. 2011 10:21:16 EST
ja_JP: 2011年12月28日 10時21分16秒 EST

```

### See also

|  |  |
| --- | --- |
| time_put | formats contents of std::tm for output as character sequence   (class template) |
| get_time(C++11) | parses a date/time value of specified format   (function template) |
| strftime | converts a std::tm object to custom textual representation   (function) |
| wcsftime | converts a std::tm object to custom wide string textual representation   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/manip/put_time&oldid=159179>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 September 2023, at 22:40.