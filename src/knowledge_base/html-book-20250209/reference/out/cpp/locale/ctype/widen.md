# std::ctype<CharT>::widen, do_widen

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
| ****ctype::widenctype::do_widen**** | | | | |
| ctype::narrowctype::do_narrow | | | | |
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
| public:  CharT widen( char c ) const; | (1) |  |
| public:  const char\* widen( const char\* beg, const char\* end, CharT\* dst ) const; | (2) |  |
| protected:  virtual CharT do_widen( char c ) const; | (3) |  |
| protected:  virtual const char\* do_widen( const char\* beg, const char\* end, CharT\* dst ) const; | (4) |  |
|  |  |  |

1,2) Public member function, calls the corresponding protected virtual member function `do_widen` overload of the most derived class. Overload (1) calls do_widen(c), overload (2) calls do_widen(beg, end, dst).3) Converts the single-byte character c to the corresponding wide character representation using the simplest reasonable transformation. Typically, this applies only to the characters whose multibyte encoding is a single byte (e.g. U+0000-U+007F in UTF-8).4) For every character in the character array ``beg`,`end`)`, writes the corresponding widened character to the successive locations in the character array pointed to by dst.

Widening always returns a wide character, but only the characters from the [basic source character set(until C++23)basic character set(since C++23) are guaranteed to have a unique, well-defined, widening transformation, which is also guaranteed to be reversible (by narrow()). In practice, all characters whose multibyte representation is a single byte are usually widened to their wide character counterparts, and the rest of the possible single-byte values are usually mapped into the same placeholder value, typically CharT(-1).

Widening, if successful, preserves all character classification categories known to is().

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | character to convert |
| dflt | - | default value to produce if the conversion fails |
| beg | - | pointer to the first character in an array of characters to convert |
| end | - | one past the end pointer for the array of characters to convert |
| dst | - | pointer to the first element of the array of characters to fill |

### Return value

1,3) Widened character.2,4) end

### Example

Run this code

```
#include <iostream>
#include <locale>
 
void try_widen(const std::ctype<wchar_t>& f, char c)
{
    wchar_t w = f.widen(c);
    std::cout << "The single-byte character " << +(unsigned char)c
              << " widens to " << +w << '\n';
}
 
int main()
{
    std::locale::global(std::locale("cs_CZ.iso88592"));
    auto& f = std::use_facet<std::ctype<wchar_t>>(std::locale());
    std::cout << std::hex << std::showbase << "In Czech ISO-8859-2 locale:\n";
    try_widen(f, 'a');
    try_widen(f, '\xdf'); // German letter ß (U+00df) in ISO-8859-2
    try_widen(f, '\xec'); // Czech letter ě (U+011b) in ISO-8859-2
 
    std::locale::global(std::locale("cs_CZ.utf8"));
    auto& f2 = std::use_facet<std::ctype<wchar_t>>(std::locale());
    std::cout << "In Czech UTF-8 locale:\n";
    try_widen(f2, 'a');
    try_widen(f2, '\xdf'); 
    try_widen(f2, '\xec'); 
}

```

Possible output:

```
In Czech ISO-8859-2 locale:
The single-byte character 0x61 widens to 0x61
The single-byte character 0xdf widens to 0xdf
The single-byte character 0xec widens to 0x11b
In Czech UTF-8 locale:
The single-byte character 0x61 widens to 0x61
The single-byte character 0xdf widens to 0xffffffff
The single-byte character 0xec widens to 0xffffffff

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 153 | C++98 | `widen` always called overload (4) | calls the corresponding overload |

### See also

|  |  |
| --- | --- |
| narrow | invokes `do_narrow`   (public member function) |
| widen | widens characters   (public member function of `std::basic_ios<CharT,Traits>`) |
| btowc | widens a single-byte narrow character to wide character, if possible   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/locale/ctype/widen&oldid=160070>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 October 2023, at 09:53.