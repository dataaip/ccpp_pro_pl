# std::ctype<char>

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Locales and facets | | | | | | Locales | | | | | | has_facet | | | | | | use_facet | | | | | | locale | | | | | | Facet category base classes | | | | | | ctype_base | | | | | | codecvt_base | | | | | | messages_base | | | | | | time_base | | | | | | money_base | | | | | | ctype facets | | | | | | ctype | | | | | | ****ctype<char>**** | | | | | | ctype_byname | | | | | | codecvt | | | | | | codecvt_byname | | | | | | numeric facets | | | | | | num_get | | | | | | num_put | | | | | | numpunct | | | | | | numpunct_byname | | | | | | collate facets | | | | | | collate | | | | | | collate_byname | | | | | | time facets | | | | | | time_get | | | | | | time_put | | | | | | time_get_byname | | | | | | time_put_byname | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | monetary facets | | | | | | money_get | | | | | | money_put | | | | | | moneypunct | | | | | | moneypunct_byname | | | | | | messages facets | | | | | | messages | | | | | | messages_byname | | | | | | Character classification and conversion | | | | | | Character classification | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isspace | | | | | | iscntrl | | | | | | isupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | islower | | | | | | isalpha | | | | | | ispunct | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isdigit | | | | | | isxdigit | | | | | | isalnum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isblank(C++11) | | | | | | isprint | | | | | | isgraph | | | | | | | | Character conversions | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | toupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tolower | | | | | | | | String and stream conversions | | | | | | wstring_convert(C++11/17/26\*) | | | | | | wbuffer_convert(C++11/17/26\*) | | | | | | Unicode conversion facets | | | | | | codecvt_utf8(C++11/17/26\*) | | | | | | codecvt_utf16(C++11/17/26\*) | | | | | | codecvt_utf8_utf16(C++11/17/26\*) | | | | | | codecvt_mode(C++11/17/26\*) | | | | | | C library locales | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | LC_ALLLC_COLLATELC_CTYPELC_MONETARYLC_NUMERICLC_TIME | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setlocale | | | | | | localeconv | | | | | | lconv | | | | | |  | | | | | |  | | | | | |  | | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<locale>` |  |  |
| template<>  class ctype<char>; |  |  |
|  |  |  |

This specialization of std::ctype encapsulates character classification features for type char. Unlike general-purpose std::ctype, which uses virtual functions, this specialization uses table lookup to classify characters (which is generally faster).

The base class `std::ctype`<char> implements character classification equivalent to the minimal "C" locale. The classification rules can be extended or modified if constructed with a non-default classification table argument, if constructed as std::ctype_byname<char> or as a user-defined derived facet. All std::istream formatted input functions are required to use `std::ctype`<char> for character classing during input parsing.

!std-ctype char-inheritance.svg

Inheritance diagram

### Nested types

|  |  |
| --- | --- |
| Type | Definition |
| `char_type` | char |

### Data members

|  |  |
| --- | --- |
| Member | Description |
| std::locale::id `id` [static] | the identifier of the facet |
| const std::size_t `table_size` [static] | size of the classification table, at least 256 |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new ctype<char> facet   (public member function) |
| (destructor) | destructs a ctype<char> facet   (protected member function) |
| table | obtains the character classification table   (public member function) |
| classic_table[static] | obtains the "C" locale character classification table   (public static member function) |
| is | classifies a character or a character sequence, using the classification table   (public member function) |
| scan_is | locates the first character in a sequence that conforms to given classification, using the classification table   (public member function) |
| scan_not | locates the first character in a sequence that fails given classification, using the classification table   (public member function) |
| toupper | invokes `do_toupper`   (public member function of `std::ctype<CharT>`) |
| tolower | invokes `do_tolower`   (public member function of `std::ctype<CharT>`) |
| widen | invokes `do_widen`   (public member function of `std::ctype<CharT>`) |
| narrow | invokes `do_narrow`   (public member function of `std::ctype<CharT>`) |

### Protected member functions

|  |  |
| --- | --- |
| do_toupper[virtual] | converts a character or characters to uppercase   (virtual protected member function of `std::ctype<CharT>`) |
| do_tolower[virtual] | converts a character or characters to lowercase   (virtual protected member function of `std::ctype<CharT>`) |
| do_widen[virtual] | converts a character or characters from char to `CharT`   (virtual protected member function of `std::ctype<CharT>`) |
| do_narrow[virtual] | converts a character or characters from `CharT` to char   (virtual protected member function of `std::ctype<CharT>`) |

## Inherited from std::ctype_base

### Nested types

|  |  |
| --- | --- |
| Type | Definition |
| `mask` | unspecified BitmaskType type (enumeration, integer type, or bitset) |

### Member constants

|  |  |
| --- | --- |
| space[static] | the value of `mask` identifying whitespace character classification   (public static member constant) |
| print[static] | the value of `mask` identifying printable character classification   (public static member constant) |
| cntrl[static] | the value of `mask` identifying control character classification   (public static member constant) |
| upper[static] | the value of `mask` identifying uppercase character classification   (public static member constant) |
| lower[static] | the value of `mask` identifying lowercase character classification   (public static member constant) |
| alpha[static] | the value of `mask` identifying alphabetic character classification   (public static member constant) |
| digit[static] | the value of `mask` identifying digit character classification   (public static member constant) |
| punct[static] | the value of `mask` identifying punctuation character classification   (public static member constant) |
| xdigit[static] | the value of `mask` identifying hexadecimal digit character classification   (public static member constant) |
| blank[static] (C++11) | the value of `mask` identifying blank character classification   (public static member constant) |
| alnum[static] | alpha | digit   (public static member constant) |
| graph[static] | alnum | punct   (public static member constant) |

### Example

The following example demonstrates modification of ctype<char> to tokenize comma-separated values:

Run this code

```
#include <cstddef>
#include <iostream>
#include <locale>
#include <sstream>
#include <vector>
 
// This ctype facet classifies commas and endlines as whitespace
struct csv_whitespace : std::ctype<char>
{
    static const mask* make_table()
    {
        // make a copy of the "C" locale table
        static std::vector<mask> v(classic_table(), classic_table() + table_size);
        v[','] |=  space; // comma will be classified as whitespace
        v[' '] &= ~space; // space will not be classified as whitespace
        return &v[0];
    }
 
    csv_whitespace(std::size_t refs = 0) : ctype(make_table(), false, refs) {}
};
 
int main()
{
    std::string in = "Column 1,Column 2,Column 3\n123,456,789";
    std::string token;
 
    std::cout << "Default locale:\n";
    std::istringstream s1(in);
    while (s1 >> token)
        std::cout << "  " << token << '\n';
 
    std::cout << "Locale with modified ctype:\n";
    std::istringstream s2(in);
    s2.imbue(std::locale(s2.getloc(), new csv_whitespace));
    while (s2 >> token)
        std::cout << "  " << token << '\n';
}

```

Output:

```
Default locale:
  Column
  1,Column
  2,Column
  3
  123,456,789
Locale with modified ctype:
  Column 1
  Column 2
  Column 3
  123
  456
  789

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 695 | C++98 | `table()` and `classic_table()` were protected member functions | made them public |

### See also

|  |  |
| --- | --- |
| ctype | defines character classification tables   (class template) |
| ctype_base | defines character classification categories   (class) |
| ctype_byname | represents the system-supplied std::ctype for the named locale   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/locale/ctype_char&oldid=177713>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 November 2024, at 01:02.