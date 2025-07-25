# std::money_put<CharT,OutputIt>::put, do_put

From cppreference.com
< cpp‎ | locale‎ | money put
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

std::money_put

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| money_put::money_put | | | | |
| money_put::~money_put | | | | |
| ****money_put::putmoney_put::do_put**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<locale>` |  |  |
| public:  iter_type put( iter_type out, bool intl, std::ios_base& f,                char_type fill, long double quant ) const; | (1) |  |
| iter_type put( iter_type out, bool intl, std::ios_base& f,                 char_type fill, const string_type& quant ) const; | (2) |  |
| protected:  virtual iter_type do_put( iter_type out, bool intl, std::ios_base& str,                           char_type fill, long double units ) const; | (3) |  |
| virtual iter_type do_put( iter_type out, bool intl, std::ios_base& str,                            char_type fill, const string_type& digits ) const; | (4) |  |
|  |  |  |

Formats monetary value and writes the result to output stream.

1,2) Public member functions, call the member function `do_put` of the most derived class.3) The numeric arguments units is converted to a wide character string as if by
ct.widen(buf1, buf1 + std::sprintf(buf1, "%.0Lf", units), buf2), where ct is the std::ctype facet imbued in str.getloc() and buf1 and buf2 are sufficiently large character buffers. The resulting character string buf2 is processed, formatted, and output to out as desribed below.4) From the string argument digits, only the optional leading minus sign (as determined by comparing to ct.widen('-'), where ct is the std::ctype facet imbued in str.getloc()) and the immediately following digit characters (as classified by ct) are taken as the character sequence to be processed, formatted, and output to out as described below.

Given the character sequence from the previous steps, if the first character equals ct.widen('-'), calls mp.neg_format() to obtain the formatting pattern, otherwise calls mp.pos_format(), where mp is the std::moneypunct<CharT, intl> facet imbued in str.getloc().

Thousands separator and decimal point characters are inserted as required by mp.grouping(), mp.frac_digits(), mp.decimal_point(), and mp.thousands_sep(), and the resulting string is placed in the output sequence where value appears in the formatting pattern.

If str.flags() & str.showbase is non-zero (the std::showbase manipulator was used), then the currency symbol or string is generated by calling mp.curr_symbol() and placed in the output sequence where symbol appears in the formatting pattern.

If mp.positive_sign() (in case positive format pattern is used) or mp.negative_sign() (in case negative format pattern is used) returns a string with more than one character, the first character returned is placed in the output sequence where sign appears in the formatting pattern, and the rest of the characters are placed after all other characters, for example, formatting pattern {sign, value, space, symbol} with units 123 and negative_sign of "-" may result in "-1.23 €", while negative_sign of "()" would generate "(1.23 €)".

If the number of characters generated for the specified format is less than the value returned by str.width(), then copies of fill are inserted to bring the total length of the output sequence to exactly str.width(), as follows:

- If str.flags() & str.adjustfield equals str.internal, the fill characters are inserted where `none` or `space` appears in the formatting pattern.
- Otherwise, if str.flags() & str.adjustfield equals str.left, the copies of fill are appended after all other characters.
- Otherwise, the fill characters are placed before all other characters.

In the end, calls str.width(0) to cancel the effects of any std::setw.

### Return value

An iterator pointing immediately after the last character produced.

### Notes

The currency units are assumed to be the smallest non-fractional units of the currency: cents in the U.S, yen in Japan.

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <locale>
 
struct my_punct : std::moneypunct_byname<char, false>
{
    my_punct(const char* name) : moneypunct_byname(name) {}
    string_type do_negative_sign() const { return "()"; }
};
 
int main()
{
    std::locale loc("ru_RU.utf8");
    std::cout.imbue(loc);
    long double units = -123.45;
    std::cout << "In Russian locale, " << units << " prints as " << std::showbase;
 
    // note, the following is equivalent to simply std::put_money(units)
    std::use_facet<std::money_put<char>>(loc).put(
        {std::cout}, false, std::cout, std::cout.fill(), units);
    std::cout << '\n';
 
    std::cout.imbue(std::locale(std::cout.getloc(), new my_punct("ru_RU.utf8")));
    std::cout << "With negative_sign set to \"()\", it prints as ";
    std::use_facet<std::money_put<char>>(loc).put(
        {std::cout}, false, std::cout, std::cout.fill(), units);
    std::cout << '\n';
}

```

Output:

```
In Russian locale, -123,45 prints as -1.23 руб
With negative_sign set to "()", it prints as (1.23 руб)

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 328 | C++98 | the format string used for std::sprintf was "%.01f" | corrected to "%.0Lf" |

### See also

|  |  |
| --- | --- |
| moneypunct | defines monetary formatting parameters used by std::money_get and std::money_put   (class template) |
| money_get | parses and constructs a monetary value from an input character sequence   (class template) |
| put_money(C++11) | formats and outputs a monetary value   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/locale/money_put/put&oldid=160149>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 October 2023, at 10:48.