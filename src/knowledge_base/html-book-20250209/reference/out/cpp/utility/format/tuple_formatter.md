# std::formatter<**pair-or-tuple**>

From cppreference.com
< cpp‎ | utility‎ | format
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

Formatting library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Standard format specification | | | | |
| Formatting functions | | | | |
| format(C++20) | | | | |
| format_to(C++20) | | | | |
| format_to_n(C++20) | | | | |
| formatted_size(C++20) | | | | |
| vformat(C++20) | | | | |
| vformat_to(C++20) | | | | |
| Format strings | | | | |
| basic_format_stringformat_stringwformat_string(C++20)(C++20)(C++20) | | | | |
| runtime_format(C++26) | | | | |
| Formatting concepts | | | | |
| formattable(C++23) | | | | |
| Formatter | | | | |
| formatter(C++20) | | | | |
| ****formatter<**pair-or-tuple**>****(C++23) | | | | |
| formatter<**range**>(C++23) | | | | |
| range_formatter(C++23) | | | | |
| enable_nonlocking_formatter_optimization(C++23) | | | | |
| basic_format_parse_contextformat_parse_contextwformat_parse_context(C++20)(C++20)(C++20) | | | | |
| basic_format_contextformat_contextwformat_context(C++20)(C++20)(C++20) | | | | |
| range_format(C++23) | | | | |
| format_kind(C++23) | | | | |
| Formatting arguments | | | | |
| basic_format_arg(C++20) | | | | |
| basic_format_arg::handle(C++20) | | | | |
| basic_format_argsformat_argswformat_args(C++20)(C++20)(C++20) | | | | |
| visit_format_arg(C++20) (deprecated in C++26) | | | | |
| make_format_argsmake_wformat_args(C++20)(C++20) | | | | |
| Format error | | | | |
| format_error(C++20) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<format>` |  |  |
| template< class CharT, std::formattable<CharT>... Ts >  struct formatter</\*pair-or-tuple\*/<Ts...>, CharT>; |  | (since C++23) |
|  |  |  |

The template specialization of std::formatter for the std::pair and std::tuple allows users to convert a pair or a tuple to its textual representation as a collection of elements using formatting functions.

The exposition-only name /\*pair-or-tuple\*/ denotes either class template std::pair or std::tuple.

This specialization meets the Formatter requirements if (std::formattable<const Ts, CharT> && ...) is true. It always meets the BasicFormatter requirements.

### Format specification

The syntax of tuple-format-spec is:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| tuple-fill-and-align ﻿(optional) width ﻿(optional) tuple-type ﻿(optional) |  |  |
|  | | | | | | | | | |

The tuple-fill-and-align is interpreted the same way as a fill-and-align except that the fill in tuple-fill-and-align is any character other than `{`, `}`, or `:`.

The width is described in standard format width specification.

The tuple-type changes the way a tuple is formatted, with certain options only valid with certain argument types.

The available tuple presentation types are:

- `m`: Indicates that both opening and closing brackets should be "" while the separator should be ": ".

:   - If `m` is chosen as the tuple-type, the program is ill-formed unless sizeof...(Ts) == 2 is true.

- `n`: Indicates that separator, opening and closing brackets should be "".

### Member objects

|  |  |
| --- | --- |
| Member name | Definition |
| `underlying_` (private) | tuple of underlying formatters of type std::tuple<std::formatter<std::remove_cvref_t<Ts>, CharT>...> (exposition-only member object\*) |
| `separator_` (private) | a string representing the separator of the tuple formatted result (defaults to ", ") (exposition-only member object\*) |
| `opening-bracket_` (private) | a string representing the opening bracket of the tuple formatted result (defaults to "(") (exposition-only member object\*) |
| `closing-bracket_` (private) | a string representing the closing bracket of the tuple formatted result (defaults to ")") (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| set_separator | sets a specified separator for the tuple formatted result   (public member function) |
| set_brackets | sets a specified opening and closing brackets for the tuple formatted result   (public member function) |
| parse | parses the format specifier as specified by tuple-format-spec   (public member function) |
| format | writes the tuple formatted output as specified by tuple-format-spec   (public member function) |

## std::formatter<**pair-or-tuple**>::set_separator

|  |  |  |
| --- | --- | --- |
| constexpr void set_separator( std::basic_string_view<CharT> sep ) noexcept; |  |  |
|  |  |  |

Assigns sep to `separator_`.

## std::formatter<**pair-or-tuple**>::set_brackets

|  |  |  |
| --- | --- | --- |
| constexpr void set_brackets( std::basic_string_view<CharT> opening,                               std::basic_string_view<CharT> closing ) noexcept; |  |  |
|  |  |  |

Assigns opening and closing to `opening-bracket_` and `closing-bracket_`, respectively.

## std::formatter<**pair-or-tuple**>::parse

|  |  |  |
| --- | --- | --- |
| template< class ParseContext >  constexpr auto parse( ParseContext& ctx ) -> ParseContext::iterator; |  |  |
|  |  |  |

Parses the format specifiers as a tuple-format-spec and stores the parsed specifiers in the current object.

If tuple-type or the `n` option is present, the values of `opening-bracket`, `closing-bracket`, and `separator` are modified as required.

For each element e in `underlying_`, calls e.parse(ctx) to parse an empty format-spec and, if e.set_debug_format() is a valid expression, calls e.set_debug_format().

Returns an iterator past the end of the tuple-format-spec.

## std::formatter<**pair-or-tuple**>::format

|  |  |  |
| --- | --- | --- |
| template< class FormatContext >  FormatContext::iterator format( /\*maybe-const-pair-or-tuple\*/<Ts...>& elems, FormatContext& ctx ) const; |  |  |
|  |  |  |

/\*maybe-const-pair-or-tuple\*/ denotes:

- const /\*pair-or-tuple\*/, if (std::formattable<const Ts, CharT> && ...) is true,
- /\*pair-or-tuple\*/ otherwise.

Writes the following into ctx.out() as specified by tuple-format-spec, in order:

- `opening-bracket_`,
- for each index I in ``​0​`,`sizeof...(Ts)`)`:

:   - if I != 0, `separator_`,
    - the result of writing std::get<I>(elems) via std::get<I>(`underlying_`), and

- `closing-bracket_`.

Returns an iterator past the end of the output range.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| [LWG 3892 | C++23 | the formatting of nested tuples was incorrect | corrected |

### See also

|  |  |
| --- | --- |
| formatter(C++20) | defines formatting rules for a given type   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/format/tuple_formatter&oldid=171289>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 April 2024, at 07:18.