# std::ctype<CharT>::narrow, do_narrow

From cppreference.com
< cpp‎ | locale‎ | ctype
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

std::ctype

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ctype::ctype | | | | |
| ctype::~ctype | | | | |
| ctype::isctype::do_is | | | | |
| ctype::scan_isctype::do_scan_is | | | | |
| ctype::scan_notctype::do_scan_not | | | | |
| ctype::toupperctype::do_toupper | | | | |
| ctype::tolowerctype::do_tolower | | | | |
| ctype::widenctype::do_widen | | | | |
| ****ctype::narrowctype::do_narrow**** | | | | |
| Member functions of ctype<char> | | | | |
| ctype<char>::ctype | | | | |
| ctype<char>::~ctype | | | | |
| ctype<char>::table | | | | |
| ctype<char>::classic_table | | | | |
| ctype<char>::is | | | | |
| ctype<char>::scan_is | | | | |
| ctype<char>::scan_not | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<locale>` |  |  |
| public:  char narrow( CharT c, char dflt ) const; | (1) |  |
| public:  const CharT\* narrow( const CharT\* beg, const CharT\* end, char dflt, char\* dst ) const; | (2) |  |
| protected:  virtual char do_narrow( CharT c, char dflt ) const; | (3) |  |
| protected:  virtual const CharT\* do_narrow( const CharT\* beg, const CharT\* end, char dflt, char\* dst ) const; | (4) |  |
|  |  |  |

1,2) Public member function, calls the corresponding protected virtual member function `do_narrow` overload of the most derived class. Overload (1) calls do_narrow(c, dflt), overload (2) calls do_narrow(beg, end, dflt, dst).3) Converts the (possibly wide) character c to multibyte representation if the character can be represented with a single byte (for example, ASCII characters in UTF-8 encoding are single bytes). Returns dflt if such conversion does not exist.4) For every character in the character array ``beg`,`end`)`, writes narrowed characters (or dflt whenever narrowing fails) to the successive locations in the character array pointed to by dst.

Narrowing is always successful and is always reversible (by calling [widen()) for all characters from the basic source character set(until C++23)basic character set(since C++23).

- i.e. do_widen(do_narrow(c, 0)) == c always holds for any character c in the basic source character set(until C++23)basic character set(since C++23).

Narrowing, if successful, preserves all character classification categories known to is().

- i.e. is(m, c) || !ctc.is(m, do_narrow(c, dflt)) is always true for any named `ctype` category with a `ctype<char>` facet ctc and `ctype_base::mask` value m (unless `do_narrow` returns dflt).

Narrowing of any digit character guarantees that if the result is subtracted from the character literal '0', the difference equals the digit value of the original character.

- i.e. for any digit character c, the expression (do_narrow(c, dflt) - '0') evaluates to the digit value of the character.

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | character to convert |
| dflt | - | default value to produce if the conversion fails |
| beg | - | pointer to the first character in an array of characters to convert |
| end | - | one past the end pointer for the array of characters to convert |
| dst | - | pointer to the first element of the array of characters to fill |

### Return value

1,3) Narrowed character or dflt if narrowing fails.2,4) end

### Example

Run this code

```
#include <iostream>
#include <locale>
 
void try_narrow(const std::ctype<wchar_t>& f, wchar_t c)
{
    char n = f.narrow(c, 0);
    if (n)
        std::wcout << '\'' << c << "' narrowed to " << +(unsigned char)n << '\n';
    else
        std::wcout << '\'' << c << "' could not be narrowed\n";
}
 
int main()
{
    std::locale::global(std::locale("en_US.utf8"));
    std::wcout.imbue(std::locale());
    std::wcout << std::hex << std::showbase << "In US English UTF-8 locale:\n";
    auto& f = std::use_facet<std::ctype<wchar_t>>(std::locale());
    try_narrow(f, L'A');
    try_narrow(f, L'Ａ');
    try_narrow(f, L'ě');
 
    std::locale::global(std::locale("cs_CZ.iso88592"));
    auto& f2 = std::use_facet<std::ctype<wchar_t>>(std::locale());
    std::wcout << "In Czech ISO-8859-2 locale:\n";
    try_narrow(f2, L'A');
    try_narrow(f2, L'Ａ');
    try_narrow(f2, L'ě');
}

```

Possible output:

```
In US English UTF-8 locale:
'A' narrowed to 0x41
'Ａ' could not be narrowed
'ě' could not be narrowed
In Czech ISO-8859-2 locale:
'A' narrowed to 0x41
'Ａ' could not be narrowed
'ě' narrowed to 0xec

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 126 | C++98 | 1. the code representing reversibility was do_widen(do_narrow(c), 0) == c 2. the code representing category preservation was is(m, c) || !ctc.is(m, do_narrow(c), dflt) | corrected both |
| LWG 153 | C++98 | `narrow` always called overload (4) | calls the corresponding overload |

### See also

|  |  |
| --- | --- |
| widen | invokes `do_widen`   (public member function) |
| narrow | narrows characters   (public member function of `std::basic_ios<CharT,Traits>`) |
| wctob | narrows a wide character to a single-byte narrow character, if possible   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/locale/ctype/narrow&oldid=169296>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 January 2024, at 08:51.