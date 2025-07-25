# std::codecvt

From cppreference.com
< cpp‎ | locale
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Locales and facets | | | | | | Locales | | | | | | has_facet | | | | | | use_facet | | | | | | locale | | | | | | Facet category base classes | | | | | | ctype_base | | | | | | codecvt_base | | | | | | messages_base | | | | | | time_base | | | | | | money_base | | | | | | ctype facets | | | | | | ctype | | | | | | ctype<char> | | | | | | ctype_byname | | | | | | ****codecvt**** | | | | | | codecvt_byname | | | | | | numeric facets | | | | | | num_get | | | | | | num_put | | | | | | numpunct | | | | | | numpunct_byname | | | | | | collate facets | | | | | | collate | | | | | | collate_byname | | | | | | time facets | | | | | | time_get | | | | | | time_put | | | | | | time_get_byname | | | | | | time_put_byname | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | monetary facets | | | | | | money_get | | | | | | money_put | | | | | | moneypunct | | | | | | moneypunct_byname | | | | | | messages facets | | | | | | messages | | | | | | messages_byname | | | | | | Character classification and conversion | | | | | | Character classification | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isspace | | | | | | iscntrl | | | | | | isupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | islower | | | | | | isalpha | | | | | | ispunct | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isdigit | | | | | | isxdigit | | | | | | isalnum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isblank(C++11) | | | | | | isprint | | | | | | isgraph | | | | | | | | Character conversions | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | toupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tolower | | | | | | | | String and stream conversions | | | | | | wstring_convert(C++11/17/26\*) | | | | | | wbuffer_convert(C++11/17/26\*) | | | | | | Unicode conversion facets | | | | | | codecvt_utf8(C++11/17/26\*) | | | | | | codecvt_utf16(C++11/17/26\*) | | | | | | codecvt_utf8_utf16(C++11/17/26\*) | | | | | | codecvt_mode(C++11/17/26\*) | | | | | | C library locales | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | LC_ALLLC_COLLATELC_CTYPELC_MONETARYLC_NUMERICLC_TIME | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setlocale | | | | | | localeconv | | | | | | lconv | | | | | |  | | | | | |  | | | | | |  | | | | | | | |

****std::codecvt****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| codecvt::codecvt | | | | |
| codecvt::~codecvt | | | | |
| codecvt::outcodecvt::do_out | | | | |
| codecvt::incodecvt::do_in | | | | |
| codecvt::unshiftcodecvt::do_unshift | | | | |
| codecvt::encodingcodecvt::do_encoding | | | | |
| codecvt::always_noconvcodecvt::do_always_noconv | | | | |
| codecvt::lengthcodecvt::do_length | | | | |
| codecvt::max_lengthcodecvt::do_max_length | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<locale>` |  |  |
| template<   class InternT,       class ExternT,       class StateT > class codecvt; |  |  |
|  |  |  |

Class template `std::codecvt` encapsulates conversion of character strings, including wide and multibyte, from one encoding to another. All file I/O operations performed through std::basic_fstream<CharT> use the std::codecvt<CharT, char, std::mbstate_t> facet of the locale imbued in the stream.

!std-codecvt-inheritance.svg

Inheritance diagram

### Specializations

The standard library is guaranteed to provide the following specializations (they are required to be implemented by any locale object):

|  |  |
| --- | --- |
| Defined in header `<locale>` | |
| std::codecvt<char, char, std::mbstate_t> | identity conversion |
| std::codecvt<char16_t, char, std::mbstate_t> (since C++11)(deprecated in C++20) | conversion between UTF-16 and UTF-8 |
| std::codecvt<char16_t, char8_t, std::mbstate_t> (since C++20)(deprecated) | conversion between UTF-16 and UTF-8 |
| std::codecvt<char32_t, char, std::mbstate_t> (since C++11)(deprecated in C++20) | conversion between UTF-32 and UTF-8 |
| std::codecvt<char32_t, char8_t, std::mbstate_t> (since C++20)(deprecated) | conversion between UTF-32 and UTF-8 |
| std::codecvt<wchar_t, char, std::mbstate_t> | conversion between the system's native wide and the single-byte narrow character sets |

### Nested types

|  |  |
| --- | --- |
| Type | Definition |
| `intern_type` | `InternT` |
| `extern_type` | `ExternT` |
| `state_type` | `StateT` |

### Data members

|  |  |
| --- | --- |
| Member | Description |
| std::locale::id `id` [static] | the identifier of the facet |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new `codecvt` facet   (public member function) |
| out | invokes `do_out`   (public member function) |
| in | invokes `do_in`   (public member function) |
| unshift | invokes `do_unshift`   (public member function) |
| encoding | invokes `do_encoding`   (public member function) |
| always_noconv | invokes `do_always_noconv`   (public member function) |
| length | invokes `do_length`   (public member function) |
| max_length | invokes `do_max_length`   (public member function) |

### Protected member functions

|  |  |
| --- | --- |
| (destructor) | destructs a `codecvt` facet   (protected member function) |
| do_out[virtual] | converts a string from `InternT` to `ExternT`, such as when writing to file   (virtual protected member function) |
| do_in[virtual] | converts a string from `ExternT` to `InternT`, such as when reading from file   (virtual protected member function) |
| do_unshift[virtual] | generates the termination character sequence of `ExternT` characters for incomplete conversion   (virtual protected member function) |
| do_encoding[virtual] | returns the number of `ExternT` characters necessary to produce one `InternT` character, if constant   (virtual protected member function) |
| do_always_noconv[virtual] | tests if the facet encodes an identity conversion for all valid argument values   (virtual protected member function) |
| do_length[virtual] | calculates the length of the `ExternT` string that would be consumed by conversion into given `InternT` buffer   (virtual protected member function) |
| do_max_length[virtual] | returns the maximum number of `ExternT` characters that could be converted into a single `InternT` character   (virtual protected member function) |

## Inherited from std::codecvt_base

|  |  |
| --- | --- |
| Nested type | Definition |
| enum result { ok, partial, error, noconv }; | Unscoped enumeration type |

|  |  |
| --- | --- |
| Enumeration constant | Definition |
| `ok` | conversion was completed with no error |
| `partial` | not all source characters were converted |
| `error` | encountered an invalid character |
| `noconv` | no conversion required, input and output types are the same |

### Example

The following examples reads a UTF-8 file using a locale which implements UTF-8 conversion in codecvt<wchar_t, char, std::mbstate_t> and converts a UTF-8 string to UTF-16 using one of the standard specializations of `std::codecvt`.

Run this code

```
#include <codecvt>
#include <cstdint>
#include <fstream>
#include <iomanip>
#include <iostream>
#include <locale>
#include <string>
 
// utility wrapper to adapt locale-bound facets for wstring/wbuffer convert
template<class Facet>
struct deletable_facet : Facet
{
    template<class... Args>
    deletable_facet(Args&&... args) : Facet(std::forward<Args>(args)...) {}
    ~deletable_facet() {}
};
 
int main()
{
    // UTF-8 narrow multibyte encoding
    std::string data = reinterpret_cast<const char*>(+u8"z\u00df\u6c34\U0001f34c");
                       // or reinterpret_cast<const char*>(+u8"zß水🍌")
                       // or "\x7a\xc3\x9f\xe6\xb0\xb4\xf0\x9f\x8d\x8c"
 
    std::ofstream("text.txt") << data;
 
    // using system-supplied locale's codecvt facet
    std::wifstream fin("text.txt");
    // reading from wifstream will use codecvt<wchar_t, char, std::mbstate_t>
    // this locale's codecvt converts UTF-8 to UCS4 (on systems such as Linux)
    fin.imbue(std::locale("en_US.UTF-8"));
    std::cout << "The UTF-8 file contains the following UCS4 code units:\n" << std::hex;
    for (wchar_t c; fin >> c;)
        std::cout << "U+" << std::setw(4) << std::setfill('0')
                  << static_cast<uint32_t>(c) << ' ';
 
    // using standard (locale-independent) codecvt facet
    std::wstring_convert<
        deletable_facet<std::codecvt<char16_t, char, std::mbstate_t>>, char16_t> conv16;
    std::u16string str16 = conv16.from_bytes(data);
 
    std::cout << "\n\nThe UTF-8 file contains the following UTF-16 code units:\n"
              << std::hex;
    for (char16_t c : str16)
        std::cout << "U+" << std::setw(4) << std::setfill('0')
                  << static_cast<uint16_t>(c) << ' ';
    std::cout << '\n';
}

```

Output:

```
The UTF-8 file contains the following UCS4 code units:
U+007a U+00df U+6c34 U+1f34c 
 
The UTF-8 file contains the following UTF-16 code units:
U+007a U+00df U+6c34 U+d83c U+df4c

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3767 | C++20 | std::codecvt<char16_t, char8_t, std::mbstate_t> and std::codecvt<char32_t, char8_t, std::mbstate_t> are locale-independent | deprecated them |

### See also

| Character conversions | locale-defined multibyte (UTF-8, GB18030) | UTF-8 | UTF-16 |
| --- | --- | --- | --- |
| UTF-16 | mbrtoc16 / c16rtomb (with C11's DR488) | ****codecvt****<char16_t,char,mbstate_t>  codecvt_utf8_utf16<char16_t>  codecvt_utf8_utf16<char32_t>  codecvt_utf8_utf16<wchar_t> | N/A |
| UCS-2 | c16rtomb (without C11's DR488) | codecvt_utf8<char16_t> | codecvt_utf16<char16_t> |
| UTF-32 | mbrtoc32 / c32rtomb | ****codecvt****<char32_t,char,mbstate_t>  codecvt_utf8<char32_t> | codecvt_utf16<char32_t> |
| system wchar_t: UTF-32 (non-Windows)  UCS-2 (Windows) | mbsrtowcs / wcsrtombs  use_facet<****codecvt****  <wchar_t,char,mbstate_t>>(locale) | codecvt_utf8<wchar_t> | codecvt_utf16<wchar_t> |

|  |  |
| --- | --- |
| codecvt_base | defines character conversion errors   (class) |
| codecvt_byname | represents the system-supplied ****std::codecvt**** for the named locale   (class template) |
| codecvt_utf8(C++11)(deprecated in C++17)(removed in C++26) | converts between UTF-8 and UCS-2/UCS-4   (class template) |
| codecvt_utf16(C++11)(deprecated in C++17)(removed in C++26) | converts between UTF-16 and UCS-2/UCS-4   (class template) |
| codecvt_utf8_utf16(C++11)(deprecated in C++17)(removed in C++26) | converts between UTF-8 and UTF-16   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/locale/codecvt&oldid=177703>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 November 2024, at 23:30.