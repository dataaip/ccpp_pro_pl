# std::num_get<CharT,InputIt>::get, std::num_get<CharT,InputIt>::do_get

From cppreference.com
< cpp‎ | locale‎ | num get
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

std::num_get

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| num_get::num_get | | | | |
| num_get::~num_get | | | | |
| ****num_get::getnum_get::do_get**** | | | | |

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| public:  iter_type get( iter_type in, iter_type end, std::ios_base& str, std::ios_base::iostate& err, bool& v ) const; |  |  |
| iter_type get( iter_type in, iter_type end, std::ios_base& str,                  std::ios_base::iostate& err, long& v ) const; |  |  |
| iter_type get( iter_type in, iter_type end, std::ios_base& str,                  std::ios_base::iostate& err, long long& v ) const; |  | (since C++11) |
| iter_type get( iter_type in, iter_type end, std::ios_base& str,                  std::ios_base::iostate& err, unsigned short& v ) const; |  |  |
| iter_type get( iter_type in, iter_type end, std::ios_base& str,                  std::ios_base::iostate& err, unsigned int& v ) const; |  |  |
| iter_type get( iter_type in, iter_type end, std::ios_base& str,                  std::ios_base::iostate& err, unsigned long& v ) const; |  |  |
| iter_type get( iter_type in, iter_type end, std::ios_base& str,                  std::ios_base::iostate& err, unsigned long long& v ) const; |  | (since C++11) |
| iter_type get( iter_type in, iter_type end, std::ios_base& str,                  std::ios_base::iostate& err, float& v ) const; |  |  |
| iter_type get( iter_type in, iter_type end, std::ios_base& str,                  std::ios_base::iostate& err, double& v ) const; |  |  |
| iter_type get( iter_type in, iter_type end, std::ios_base& str,                  std::ios_base::iostate& err, long double& v ) const; |  |  |
| iter_type get( iter_type in, iter_type end, std::ios_base& str,                  std::ios_base::iostate& err, void\*& v ) const; |  |  |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| protected:  virtual iter_type do_get( iter_type in, iter_type end, std::ios_base& str, std::ios_base::iostate& err, bool& v ) const; |  |  |
| virtual iter_type do_get( iter_type in, iter_type end, std::ios_base& str,                             std::ios_base::iostate& err, long& v ) const; |  |  |
| virtual iter_type do_get( iter_type in, iter_type end, std::ios_base& str,                             std::ios_base::iostate& err, long long& v ) const; |  | (since C++11) |
| virtual iter_type do_get( iter_type in, iter_type end, std::ios_base& str,                             std::ios_base::iostate& err, unsigned short& v ) const; |  |  |
| virtual iter_type do_get( iter_type in, iter_type end, std::ios_base& str,                             std::ios_base::iostate& err, unsigned int& v ) const; |  |  |
| virtual iter_type do_get( iter_type in, iter_type end, std::ios_base& str,                             std::ios_base::iostate& err, unsigned long& v ) const; |  |  |
| virtual iter_type do_get( iter_type in, iter_type end, std::ios_base& str,   std::ios_base::iostate& err, unsigned long long& v ) const; |  | (since C++11) |
| virtual iter_type do_get( iter_type in, iter_type end, std::ios_base& str,                             std::ios_base::iostate& err, float& v ) const; |  |  |
| virtual iter_type do_get( iter_type in, iter_type end, std::ios_base& str,                             std::ios_base::iostate& err, double& v ) const; |  |  |
| virtual iter_type do_get( iter_type in, iter_type end, std::ios_base& str,                             std::ios_base::iostate& err, long double& v ) const; |  |  |
| virtual iter_type do_get( iter_type in, iter_type end, std::ios_base& str,                             std::ios_base::iostate& err, void\*& v ) const; |  |  |
|  |  |  |
| --- | --- | --- |
|  |  |  |

1) Public member function, calls the member function `do_get` of the most derived class.2) Reads characters from the input iterator in and generates the value of the type of v, taking into account I/O stream formatting flags from str.flags(), character classification rules from std::use_facet<std::ctype<CharT>>(str.getloc()), and numeric punctuation characters from std::use_facet<std::numpunct<CharT>>(str.getloc()). This function is called by all formatted input stream operators such as std::cin >> n;.

Conversion occurs in three stages:

#### Stage 1: conversion specifier selection

- I/O format flags are obtained, as if by

:   fmtflags basefield = (str.flags() & std::ios_base::basefield);
:   fmtflags boolalpha = (str.flags() & std::ios_base::boolalpha);

- If the type of v is an integer type, the first applicable choice of the following five is selected:

:   If basefield == oct, will use conversion specifier %o
:   If basefield == hex, will use conversion specifier %X
:   If basefield == 0, will use conversion specifier %i
:   If the type of v is signed, will use conversion specifier %d
:   If the type of v is unsigned, will use conversion specifier %u

- For integer types, length modifier is added to the conversion specification if necessary: h for short and unsigned short, l for long and unsigned long, ll for long long and unsigned long long(since C++11)
- If the type of v is float, will use conversion specifier %g
- If the type of v is double, will use conversion specifier %lg
- If the type of v is long double, will use conversion specifier %Lg
- If the type of v is void\*, will use conversion specifier %p
- If the type of v is bool and boolalpha == 0, proceeds as if the type of v is long, except for the value to be stored in v in stage 3.
- If the type of v is bool and boolalpha != 0, the following replaces stages 2 and 3:
  - Successive characters obtained from the input iterator in are matched against the character sequences obtained from std::use_facet<std::numpunct<CharT>>(str.getloc()).falsename() and std::use_facet<std::numpunct<CharT>>(str.getloc()).truename() only as necessary as to identify the unique match. The input iterator in is compared to end only when necessary to obtain a character.
  - If the target sequence is uniquely matched, v is set to the corresponding bool value. Otherwise false is stored in v and std::ios_base::failbit is assigned to err. If unique match could not be found before the input ended (in == end), err |= std::ios_base::eofbit is executed.

#### Stage 2: character extraction

- If in == end, stage 2 is terminated immediately, no further characters are extracted.
- The next character is extracted from in as if by char_type ct = \*in;:
  - If the character matches one of "0123456789abcdefxABCDEFX+-"(until C++11)"0123456789abcdefpxABCDEFPX+-"(since C++11), widened to the locale's char_type as if by std::use_facet<std::ctype<CharT>>(str.getloc()).widen(), it is converted to the corresponding char.
  - If the character matches the decimal point separator (std::use_facet<std::numpunct<CharT>>(str.getloc()).decimal_point())), it is replaced by '.'.
  - If the character matches the thousands separator (std::use_facet<std::numpunct<CharT>>(str.getloc()).thousands_sep()) and the thousands separation is in use (as determined by std::use_facet<std::numpunct<CharT>>(str.getloc()).grouping().length() != 0), then if the decimal point '.' has not yet been accumulated, the position of the character is remembered, but the character is otherwise ignored. If the decimal point has already been accumulated, the character is discarded and stage 2 terminates.
  - In any case, the check is made whether the char obtained from the previous steps is allowed in the input field that would be parsed by std::scanf given the conversion specifier selected in stage 1. If it is allowed, it is accumulated in a temporary buffer and stage 2 repeats. If it is not allowed, stage 2 terminates.

#### Stage 3: conversion and storage

- The sequence of chars accumulated in stage 2 is converted to a numeric value:

|  |  |
| --- | --- |
| The input is parsed according to the rules of std::scanf. | (until C++11) |
| The input is parsed as if by  - std::strtoll for signed integer v, - std::strtoull for unsigned integer v, - std::strtof for float v, - std::strtod for double v, or - std::strtold for long double v. | (since C++11) |

- If the conversion function fails to convert the entire field, the value ​0​ is stored in v.
- If the type of v is a signed integer type and the conversion function results in a positive or negative value too large to fit in it, the most positive or negative representable value is stored in v, respectively.
- If the type of v is an unsigned integer type and the conversion function results in a value that does not fit in it, the most positive representable value is stored in v.
- In any case, if the conversion function fails std::ios_base::failbit is assigned to err.
- Otherwise, the numeric result of the conversion is stored in v.
  - If the type of v is bool and boolalpha is not set, then if the value to be stored is ​0​, false is stored, if the value to be stored is 1, true is stored, for any other value std::ios_base::failbit is assigned to err and true is stored.
- After this, digit grouping is checked. if the position of any of the thousands separators discarded in stage 2 does not match the grouping provided by std::use_facet<std::numpunct<CharT>>(str.getloc()).grouping(), std::ios_base::failbit is assigned to err.
- If stage 2 was terminated by the test in == end, err |= std::ios_base::eofbit is executed to set the eof bit.

### Return value

in

### Notes

Before the resolutions of LWG issue 23 and LWG issue 696, v was left unchanged if an error occurs.

Before the resolution of LWG issue 221, strings representing hexadecimal integers (e.g. "0xA0") were rejected by `do_get(int)` even if they are valid input to strtol because stage 2 filters out characters 'X' and 'x'.

Before the resolution of LWG issue 1169, converting a negative number string into an unsigned integer might produce zero (since the value represented by the string is smaller than what the target type can represent).

|  |  |
| --- | --- |
| Before the resolution of LWG issue 2381, strings representing hexadecimal floating-point numbers with exponents (e.g. "0x1.23p-10") were rejected by `do_get(double)` even if they are valid input to strtod because stage 2 filters out characters 'P' and 'p'.  The strings representing infinity or not-a-number (e.g. "NaN" and "inf") are rejected by `do_get(double)` even if they are valid input to `strtod` because stage 2 filters out characters such as 'N' or 'i'. | (since C++11) |

### Example

An implementation of `operator>>` for a user-defined type.

Run this code

```
#include <iostream>
#include <iterator>
#include <locale>
 
struct base { long x; };
 
template<class CharT, class Traits>
std::basic_istream<CharT, Traits>&
    operator >>(std::basic_istream<CharT, Traits>& is, base& b)
{
    std::ios_base::iostate err = std::ios_base::goodbit;
 
    try // setting err could throw
    {
        typename std::basic_istream<CharT, Traits>::sentry s(is);
 
        if (s) // if stream is ready for input
            std::use_facet<std::num_get<CharT>>(is.getloc()).get(is, {}, is, err, b.x);
    }
    catch (std::ios_base::failure& error)
    {
        // handle the exception
    }
 
    return is;
}
 
int main()
{
    base b;
    std::cin >> b;
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 17 | C++98 | the process of parsing text boolean values was errornous | corrected |
| LWG 18 | C++98 | the overload of `get` taking bool& value was missing | added |
| LWG 23 | C++98 | overflowing input resulted in undefined behavior | overflow handled |
| LWG 154 | C++98 | the conversion specifier for double was %g (same as float) | changed to %lg |
| LWG 221 | C++98 | `do_get` did not parse 'x' and 'X' while strtol parsed them | made 'x' and 'X' parsed |
| LWG 275 | C++98 | `get` had an overload taking short& value instead of float& | corrected |
| LWG 358 | C++98 | thousand separators after the decimal point were ignored | stage 2 is terminated if encountered |
| LWG 696 | C++98 | the result was unchanged on conversion failure | set to zero |
| LWG 1169 | C++98 | overflow handling was inconsistent between floating-point types | made consistent with `strtof`/`strtod` |
| LWG 2381 | C++11 | `do_get` did not parse 'p' and 'P' while strtod parsed them | made 'p' and 'P' parsed |

### See also

|  |  |
| --- | --- |
| operator>> | extracts formatted data   (public member function of `std::basic_istream<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/locale/num_get/get&oldid=160184>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 October 2023, at 06:57.