# std::regex_constants::match_flag_type

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
| regex_traits(C++11) | | | | |
| Constants | | | | |
| syntax_option_type(C++11) | | | | |
| ****match_flag_type****(C++11) | | | | |
| error_type(C++11) | | | | |
| Regex Grammar | | | | |
| Modified ECMAScript-262(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<regex>` |  |  |
| using match_flag_type = /\* implementation-defined \*/; | (1) | (since C++11) |
| constexpr match_flag_type match_default =     {};  constexpr match_flag_type match_not_bol =     /\* unspecified \*/;  constexpr match_flag_type match_not_eol =     /\* unspecified \*/;  constexpr match_flag_type match_not_bow =     /\* unspecified \*/;  constexpr match_flag_type match_not_eow =     /\* unspecified \*/;  constexpr match_flag_type match_any =         /\* unspecified \*/;  constexpr match_flag_type match_not_null =    /\* unspecified \*/;  constexpr match_flag_type match_continuous =  /\* unspecified \*/;  constexpr match_flag_type match_prev_avail =  /\* unspecified \*/;  constexpr match_flag_type format_default =    {};  constexpr match_flag_type format_sed =        /\* unspecified \*/;  constexpr match_flag_type format_no_copy =    /\* unspecified \*/; constexpr match_flag_type format_first_only = /\* unspecified \*/; | (2) | (since C++11)  (inline since C++17) |
|  |  |  |

1) `match_flag_type` is a BitmaskType that specifies additional regular expression matching options.

### Constants

Note: ``first`,`last`)` refers to the character sequence being matched.

|  |  |
| --- | --- |
| Name | Explanation |
| `match_not_bol` | The first character in `[`first`,`last`)` will be treated as if it is ****not**** at the beginning of a line (i.e. `^` will not match `[`first`,`first`)`). |
| `match_not_eol` | The last character in `[`first`,`last`)` will be treated as if it is ****not**** at the end of a line (i.e. `$` will not match `[`last`,`last`)`). |
| `match_not_bow` | `\b` will not match `[`first`,`first`)`. |
| `match_not_eow` | `\b` will not match `[`last`,`last`)`. |
| `match_any` | If more than one match is possible, then any match is an acceptable result. |
| `match_not_null` | Do not match empty sequences. |
| `match_continuous` | Only match a sub-sequence that begins at first. |
| `match_prev_avail` | --first is a valid iterator position. When set, causes `match_not_bol` and `match_not_bow` to be ignored. |
| `format_default` | Use ECMAScript rules to construct strings in [std::regex_replace (syntax documentation). |
| `format_sed` | Use POSIX **sed** utility rules in std::regex_replace (syntax documentation). |
| `format_no_copy` | Do not copy un-matched strings to the output in std::regex_replace. |
| `format_first_only` | Only replace the first match in std::regex_replace. |

All constants, except for `match_default` and `format_default`, are bitmask elements. The `match_default` and `format_default` constants are empty bitmasks.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2053 | C++11 | 1. the constants were declared static 2. `match_default` and `format_default` were initialized from ​0​ | 1. removed the static specifier 2. initialized from {} |

### See also

|  |  |
| --- | --- |
| regex_match(C++11) | attempts to match a regular expression to an entire character sequence   (function template) |
| syntax_option_type(C++11) | general options controlling regex behavior   (typedef) |
| error_type(C++11) | describes different types of matching errors   (typedef) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/match_flag_type&oldid=173769>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 July 2024, at 03:01.