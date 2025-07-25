# std::time_put<CharT,OutputIt>::put, std::time_put<CharT,OutputIt>::do_put

From cppreference.com
< cpp‎ | locale‎ | time put
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

Text processing library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Localization library | | | | |
| Regular expressions library (C++11) | | | | |
| Formatting library (C++20) | | | | |
| Null-terminated sequence utilities | | | | |
| Byte strings | | | | |
| Multibyte strings | | | | |
| Wide strings | | | | |
| Primitive numeric conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | to_chars(C++17) | | | | | | to_chars_result(C++17) | | | | | | from_chars(C++17) | | | | | | from_chars_result(C++17) | | | | | | chars_format(C++17) | | | | | |
| Text encoding identifications | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | text_encoding(C++26) | | | | | |

Localization library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Locales and facets | | | | | | Locales | | | | | | has_facet | | | | | | use_facet | | | | | | locale | | | | | | Facet category base classes | | | | | | ctype_base | | | | | | codecvt_base | | | | | | messages_base | | | | | | time_base | | | | | | money_base | | | | | | ctype facets | | | | | | ctype | | | | | | ctype<char> | | | | | | ctype_byname | | | | | | codecvt | | | | | | codecvt_byname | | | | | | numeric facets | | | | | | num_get | | | | | | num_put | | | | | | numpunct | | | | | | numpunct_byname | | | | | | collate facets | | | | | | collate | | | | | | collate_byname | | | | | | time facets | | | | | | time_get | | | | | | time_put | | | | | | time_get_byname | | | | | | time_put_byname | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | monetary facets | | | | | | money_get | | | | | | money_put | | | | | | moneypunct | | | | | | moneypunct_byname | | | | | | messages facets | | | | | | messages | | | | | | messages_byname | | | | | | Character classification and conversion | | | | | | Character classification | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isspace | | | | | | iscntrl | | | | | | isupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | islower | | | | | | isalpha | | | | | | ispunct | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isdigit | | | | | | isxdigit | | | | | | isalnum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isblank(C++11) | | | | | | isprint | | | | | | isgraph | | | | | | | | Character conversions | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | toupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tolower | | | | | | | | String and stream conversions | | | | | | wstring_convert(C++11/17/26\*) | | | | | | wbuffer_convert(C++11/17/26\*) | | | | | | Unicode conversion facets | | | | | | codecvt_utf8(C++11/17/26\*) | | | | | | codecvt_utf16(C++11/17/26\*) | | | | | | codecvt_utf8_utf16(C++11/17/26\*) | | | | | | codecvt_mode(C++11/17/26\*) | | | | | | C library locales | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | LC_ALLLC_COLLATELC_CTYPELC_MONETARYLC_NUMERICLC_TIME | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setlocale | | | | | | localeconv | | | | | | lconv | | | | | |  | | | | | |  | | | | | |  | | | | | | | |

std::time_put

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| time_put::time_put | | | | |
| time_put::~time_put | | | | |
| ****time_put::puttime_put::do_put**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<locale>` |  |  |
| public:  iter_type put( iter_type out, std::ios_base& str,                 char_type fill, const std::tm\* t, const CharT\* fmtbeg, const CharT\* fmtend ) const; | (1) |  |
| public:  iter_type put( iter_type out, std::ios_base& str,                 char_type fill, const std::tm\* t, char format, char modifier = 0 ) const; | (2) |  |
| protected:  virtual iter_type do_put( iter_type out, std::ios_base& str,                            char_type fill, const std::tm\* t, char format, char modifier ) const; | (3) |  |
|  |  |  |

Converts the calendar date and time stored in the std::tm object pointed to by t into a character string, according to the format string `fmtbeg, fmtend)`. The format string is the same as used by [std::strftime, but each format specifier is processed by an individual call to `do_put()`, which can be customized by extending this facet.

1) Steps through the character sequence `fmtbeg, fmtend)`, examining the characters. Every character that is not a part of a format sequence is written to the output iterator out immediately. To identify format sequences, this function narrows the next character c in `[fmtbeg, fmtend)` as if by [std::ctype<char_type>(str.getloc()).narrow(c, 0) and if it equals '%', the next one or two characters are compared to the list of format sequences recognized by std::strftime plus any additional implementation-defined formats supported by this locale. For each valid format sequence, a call to do_put(out, str, fill, t, format, modifier) is made, where format is the format sequence character, and modifier is the optional format sequence modifier ('E' or 'O'). A value of '\0' is used if the modifier is absent.2) Calls the `do_put` member function of the most derived class.3) Converts the calendar date and time stored in the std::tm object pointed to by t into a character string, according to the format conversion sequence formed by concatenating '%', the value of modifier if not '\0', and the value of format. The format is interpreted the same way as the function std::strftime, except that the formats that are described as locale-dependent are defined by this locale, and additional format specifiers may be supported (the fill argument is provided for these implementation-defined format specifiers to use). The string is written to the output iterator out.

### Parameters

|  |  |  |
| --- | --- | --- |
| out | - | output iterator where the result of the conversion is written |
| str | - | a stream object that this function uses to obtain locale facets when needed, e.g. std::ctype to narrow characters |
| t | - | pointer to the std::tm object from which the date/time values are obtained |
| fmtbeg | - | pointer to the first character of a sequence of `char_type` characters specifying the conversion format |
| fmtend | - | pointer one past the last character of a sequence of `char_type` characters specifying the conversion format |
| fill | - | fill character (usually space) |
| format | - | the character that names a conversion specifier |
| modifier | - | the optional modifier that may appear between `%` and the conversion specifier |

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

Iterator pointing one past the last character that was produced.

### Notes

No error handling is provided.

The fill character is provided for those implementation-defined format specifiers and for the user-defined overrides of `do_put()` that use padding and filling logic. Such implementations typically make use of the formatting flags from str.

### Example

Run this code

```
#include <iostream>
#include <sstream>
#include <iomanip>
#include <ctime>
 
void try_time_put(const std::tm* t, const std::string& fmt)
{
    std::cout.imbue(std::locale());
    std::cout << "In the locale '" << std::cout.getloc().name() << "' : '";
 
    std::use_facet<std::time_put<char>>(std::cout.getloc()).put(
        {std::cout}, std::cout, ' ', t, &fmt[0], &fmt[0] + fmt.size());
 
    std::cout << "'\n";
}
 
int main()
{
    std::time_t t = std::time(NULL);
    std::tm tm = *std::localtime(&t);
 
    std::string fmt = "%c";
    std::cout << "Using the format string '" << fmt
              << "' to format the time: " << std::ctime(&t) << '\n';
 
    std::locale::global(std::locale("de_DE.utf8"));
    try_time_put(&tm, fmt);
 
    std::locale::global(std::locale("el_GR.utf8"));
    try_time_put(&tm, fmt);
 
    std::locale::global(std::locale("ja_JP.utf8"));
    try_time_put(&tm, fmt);
}

```

Possible output:

```
Using the format string '%c' to format the time: Mon Feb 11 22:58:50 2013
 
In the locale 'de_DE.utf8' : 'Mo 11 Feb 2013 23:02:38 EST'
In the locale 'el_GR.utf8' : 'Δευ 11 Φεβ 2013 11:02:38 μμ EST'
In the locale 'ja_JP.utf8' : '2013年02月11日 23時02分38秒'

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 164 | C++98 | the purpose of the parameter fill was not clear | made clear |

### See also

|  |  |
| --- | --- |
| put_time(C++11) | formats and outputs a date/time value according to the specified format   (function template) |
| do_get[virtual] (C++11) | extracts date/time components from input stream, according to the specified format   (virtual protected member function of `std::time_get<CharT,InputIt>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/locale/time_put/put&oldid=143571>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 September 2022, at 19:10.