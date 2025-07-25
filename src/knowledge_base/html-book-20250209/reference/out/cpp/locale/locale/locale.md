# std::locale::locale

From cppreference.com
< cpp‎ | locale‎ | locale
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

std::locale

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| locale::id | | | | |
| locale::facet | | | | |
| Member functions | | | | |
| ****locale::locale**** | | | | |
| locale::~locale | | | | |
| locale::operator= | | | | |
| locale::combine | | | | |
| locale::name | | | | |
| locale::encoding(C++26) | | | | |
| locale::operator==locale::operator!=(until C++20) | | | | |
| locale::operator()") | | | | |
| Static member functions | | | | |
| locale::global | | | | |
| locale::classic | | | | |

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| locale() throw(); |  | (until C++11) |
| locale() noexcept; |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| locale( const locale& other ) throw(); |  | (until C++11) |
| locale( const locale& other ) noexcept; |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| explicit locale( const char\* std_name ); | (3) |  |
| explicit locale( const std::string& std_name ); | (4) | (since C++11) |
| locale( const locale& other, const char\* std_name, category cats ); | (5) |  |
| locale( const locale& other, const std::string& std_name, category cats ); | (6) | (since C++11) |
| template< class Facet >  locale( const locale& other, Facet\* f ); | (7) |  |
| locale( const locale& other, const locale& one, category cats ); | (8) |  |
|  |  |  |

Constructs a new locale object.

1) Default constructor. Constructs a copy of the global C++ locale, which is the locale most recently used as the argument to std::locale::global or a copy of std::locale::classic() if no call to std::locale::global has been made.2) Copy constructor. Constructs a copy of other.3,4) Constructs a copy of the system locale with specified std_name (such as "C", or "POSIX", or "en_US.UTF-8", or "English_US.1251"), if such locale is supported by the operating system. The locale constructed in this manner has a name.4) Equivalent to locale(std_name.c_str()).5) Constructs a copy of other except for all the facets identified by the cats argument, which are copied from the system locale identified by its std_name. The locale constructed in this manner has a name if and only if other has a name.6) Equivalent to locale(other, std_name.c_str(), cats).7) Constructs a copy of other except for the facet of type `Facet` (typically deduced from the type of the argument) which is installed from f. If f is a null pointer, the constructed locale is a full copy of other. The program is ill-formed if `Facet` is not a facet or it is a volatile-qualified facet. If f is null, the constructed locale has the same name as other. Otherwise, the constructed locale has no name.8) Constructs a copy of other except for all the facets identified by the cats argument, which are copied from one. If cats is equal to `locale::none`, the constructed locale has a name if and only if other has a name. Otherwise, the constructed locale has a name if and only if other and one both have names.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another locale to copy |
| std_name | - | name of the system locale to use |
| f | - | pointer to a facet to merge with other |
| cats | - | the facet categories used to identify the facets to merge with other |
| one | - | another locale to take facets from |

### Exceptions

3,5) std::runtime_error if the operating system has no locale named std_name or if std_name is a null pointer.4,6) std::runtime_error if the operating system has no locale named std_name.

### Notes

Overload (7) is typically called with its second argument, f, obtained directly from a new-expression: the locale is responsible for calling the matching delete from its own destructor.

### Example

Run this code

```
#include <codecvt>
#include <iostream>
#include <locale>
 
std::ostream& operator<< (std::ostream& os, const std::locale& loc)
{
    if (loc.name().length() <= 80)
        os << loc.name();
    else
        for (const auto c : loc.name())
            os << c << (c == ';' ? "\n  " : "");
 
    return os << '\n';
}
 
int main()
{
    std::locale l1;
    std::cout << "Name of a copy of the classic \"C\" locale: " << l1;
 
    std::locale l2("en_US.UTF-8");
    std::cout << "Name of unicode locale: " << l2;
 
    std::locale l3(l1, new std::codecvt_utf8<wchar_t>);
    std::cout << "Name of \"C\" locale except for codecvt: " << l3;
 
    std::locale l4(l1, l2, std::locale::ctype);
    std::cout << "Name of \"C\" locale except for ctype, which is unicode:\n  " << l4;
}

```

Possible output:

```
Name of a copy of the classic "C" locale: C
Name of unicode locale: en_US.UTF-8
Name of "C" locale except for codecvt: *
Name of "C" locale except for ctype, which is unicode:
  LC_CTYPE=en_US.UTF-8;
  LC_NUMERIC=C;
  LC_TIME=C;
  LC_COLLATE=C;
  LC_MONETARY=C;
  LC_MESSAGES=C;
  LC_PAPER=C;
  LC_NAME=C;
  LC_ADDRESS=C;
  LC_TELEPHONE=C;
  LC_MEASUREMENT=C;
  LC_IDENTIFICATION=C

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 436 | C++98 | for overload (7), it was unclear whether `Facet` can be cv-qualified | it can be const-qualified, but not volatile-qualified |
| LWG 2295 | C++98 | for overload (7), the constructed locale had no name even if f is null | it has the name of other |

### See also

|  |  |
| --- | --- |
| (destructor) | destructs the locale and the facets whose reference count becomes zero   (public member function) |

### External links

|  |  |
| --- | --- |
| 1. | List of Windows locale names. |
| 2. | List of Linux locale names. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/locale/locale/locale&oldid=178561>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 December 2024, at 13:21.