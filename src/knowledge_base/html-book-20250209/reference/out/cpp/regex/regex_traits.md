# std::regex_traits

From cppreference.com
< cpp‎ | regex
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

Regular expressions library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| basic_regex(C++11) | | | | |
| sub_match(C++11) | | | | |
| match_results(C++11) | | | | |
| Algorithms | | | | |
| regex_match(C++11) | | | | |
| regex_search(C++11) | | | | |
| regex_replace(C++11) | | | | |
| Iterators | | | | |
| regex_iterator(C++11) | | | | |
| regex_token_iterator(C++11) | | | | |
| Exceptions | | | | |
| regex_error(C++11) | | | | |
| Traits | | | | |
| ****regex_traits****(C++11) | | | | |
| Constants | | | | |
| syntax_option_type(C++11) | | | | |
| match_flag_type(C++11) | | | | |
| error_type(C++11) | | | | |
| Regex Grammar | | | | |
| Modified ECMAScript-262(C++11) | | | | |

****std::regex_traits****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| regex_traits::regex_traits | | | | |
| regex_traits::length | | | | |
| regex_traits::translate | | | | |
| regex_traits::translate_nocase | | | | |
| regex_traits::transform | | | | |
| regex_traits::transform_primary | | | | |
| regex_traits::lookup_collatename | | | | |
| regex_traits::lookup_classname | | | | |
| regex_traits::isctype | | | | |
| regex_traits::value | | | | |
| regex_traits::imbue | | | | |
| regex_traits::getloc | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<regex>` |  |  |
| template< class CharT >  class regex_traits; |  | (since C++11) |
|  |  |  |

The type trait template `regex_traits` supplies std::basic_regex with the set of types and functions necessary to operate on the type `CharT`.

Since many of regex operations are locale-sensitive (when std::regex_constants::collate flag is set), the regex_traits class typically holds an instance of a std::locale as a private member.

### Standard specializations

Two specializations of `std::regex_traits` are defined by the standard library:

|  |  |
| --- | --- |
| `std::regex_traits<char>` | |
| `std::regex_traits<wchar_t>` | |

These specializations make it possible to use std::basic_regex<char> (aka std::regex) and std::basic_regex<wchar_t> (aka std::wregex). To use std::basic_regex with other character types (for example, char32_t), a user-provided trait class must be used.

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `char_type` | `CharT` |
| `string_type` | std::basic_string<CharT> |
| `locale_type` | The locale used for localized behavior in the regular expression. Must be CopyConstructible |
| `char_class_type` | Represents a character classification and is capable of holding an implementation specific set returned by `lookup_classname`. Must be a BitmaskType. |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the regex_traits object   (public member function) |
| length[static] | calculates the length of a null-terminated character string   (public static member function) |
| translate | determines the equivalence key for a character   (public member function) |
| translate_nocase | determines the case-insensitive equivalence key for a character   (public member function) |
| transform | determines the sort key for the given string, used to provide collation order   (public member function) |
| transform_primary | determines the primary sort key for the character sequence, used to determine equivalence class   (public member function) |
| lookup_collatename | gets a collation element by name   (public member function) |
| lookup_classname | gets a character class by name   (public member function) |
| isctype | indicates membership in a localized character class   (public member function) |
| value | translates the character representing a numeric digit into an integral value   (public member function) |
| imbue | sets the locale   (public member function) |
| getloc | gets the locale   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/regex_traits&oldid=167158>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 December 2023, at 07:15.