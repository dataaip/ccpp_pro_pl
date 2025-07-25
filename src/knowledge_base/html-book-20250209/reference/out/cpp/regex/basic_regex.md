# std::basic_regex

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
| ****basic_regex****(C++11) | | | | |
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
| regex_traits(C++11) | | | | |
| Constants | | | | |
| syntax_option_type(C++11) | | | | |
| match_flag_type(C++11) | | | | |
| error_type(C++11) | | | | |
| Regex Grammar | | | | |
| Modified ECMAScript-262(C++11) | | | | |

****std::basic_regex****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member Functions | | | | |
| basic_regex::basic_regex | | | | |
| basic_regex::~basic_regex | | | | |
| basic_regex::operator= | | | | |
| basic_regex::assign | | | | |
| Observers | | | | |
| basic_regex::mark_count | | | | |
| basic_regex::flags | | | | |
| Locale | | | | |
| basic_regex::getloc | | | | |
| basic_regex::imbue | | | | |
| Modifiers | | | | |
| basic_regex::swap | | | | |
| Constants | | | | |
| Non-member Functions | | | | |
| swap(std::basic_regex) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<regex>` |  |  |
| template<  class CharT,      class Traits = std::regex_traits<CharT> > class basic_regex; |  | (since C++11) |
|  |  |  |

The class template `basic_regex` provides a general framework for holding regular expressions.

Several typedefs for common character types are provided:

|  |  |
| --- | --- |
| Defined in header `<regex>` | |
| Type | Definition |
| `std::regex` | std::basic_regex<char> |
| `std::wregex` | std::basic_regex<wchar_t> |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `value_type` | `CharT` |
| `traits_type` | `Traits` |
| `string_type` | `Traits::string_type` |
| `locale_type` | `Traits::locale_type` |
| `flag_type` | std::regex_constants::syntax_option_type |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the regex object   (public member function) |
| (destructor) | destructs the regex object   (public member function) |
| operator= | assigns the contents   (public member function) |
| assign | assigns the contents   (public member function) |
| Observers | |
| mark_count | returns the number of marked sub-expressions within the regular expression   (public member function) |
| flags | returns the syntax flags   (public member function) |
| Locale | |
| getloc | get locale information   (public member function) |
| imbue | set locale information   (public member function) |
| Modifiers | |
| swap | swaps the contents   (public member function) |
| Constants | |

|  |  |
| --- | --- |
| Grammar option | Effect(s) |
| `ECMAScript` | Use the Modified ECMAScript regular expression grammar. |
| `basic` | Use the basic POSIX regular expression grammar (grammar documentation). |
| `extended` | Use the extended POSIX regular expression grammar (grammar documentation). |
| `awk` | Use the regular expression grammar used by the **awk** utility in POSIX (grammar documentation). |
| `grep` | Use the regular expression grammar used by the **grep** utility in POSIX. This is effectively the same as the `basic` option with the addition of newline '\n' as an alternation separator. |
| `egrep` | Use the regular expression grammar used by the **grep** utility, with the **-E** option, in POSIX. This is effectively the same as the `extended` option with the addition of newline '\n' as an alternation separator in addition to '|'. |
| Grammar variation | Effect(s) |
| `icase` | Character matching should be performed without regard to case. |
| `nosubs` | When performing matches, all marked sub-expressions `(expr)` are treated as non-marking sub-expressions `(?:expr)`. No matches are stored in the supplied std::regex_match structure and mark_count() is zero. |
| `optimize` | Instructs the regular expression engine to make matching faster, with the potential cost of making construction slower. For example, this might mean converting a non-deterministic FSA to a deterministic FSA. |
| `collate` | Character ranges of the form **"[a-b]"** will be locale sensitive. |
| `multiline` (C++17) | Specifies that `^` shall match the beginning of a line and `$` shall match the end of a line, if the ECMAScript engine is selected. |

At most one grammar option can be chosen out of `ECMAScript`, `basic`, `extended`, `awk`, `grep`, `egrep`. If no grammar is chosen, `ECMAScript` is assumed to be selected. The other options serve as variations, such that std::regex("meow", std::regex::icase) is equivalent to std::regex("meow", std::regex::ECMAScript|std::regex::icase).

The member constants in `basic_regex` are duplicates of the `syntax_option_type` constants defined in the namespace `std::regex_constants`.

### Non-member functions

|  |  |
| --- | --- |
| std::swap(std::basic_regex)(C++11) | specializes the std::swap algorithm   (function template) |

### Deduction guides(since C++17)

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/basic_regex&oldid=160992>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 October 2023, at 13:09.