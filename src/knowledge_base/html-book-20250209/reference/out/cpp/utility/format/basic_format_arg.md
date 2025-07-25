# std::basic_format_arg

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
| formatter<**pair-or-tuple**>(C++23) | | | | |
| formatter<**range**>(C++23) | | | | |
| range_formatter(C++23) | | | | |
| enable_nonlocking_formatter_optimization(C++23) | | | | |
| basic_format_parse_contextformat_parse_contextwformat_parse_context(C++20)(C++20)(C++20) | | | | |
| basic_format_contextformat_contextwformat_context(C++20)(C++20)(C++20) | | | | |
| range_format(C++23) | | | | |
| format_kind(C++23) | | | | |
| Formatting arguments | | | | |
| ****basic_format_arg****(C++20) | | | | |
| basic_format_arg::handle(C++20) | | | | |
| basic_format_argsformat_argswformat_args(C++20)(C++20)(C++20) | | | | |
| visit_format_arg(C++20) (deprecated in C++26) | | | | |
| make_format_argsmake_wformat_args(C++20)(C++20) | | | | |
| Format error | | | | |
| format_error(C++20) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<format>` |  |  |
| template< class Context >  class basic_format_arg; |  | (since C++20) |
|  |  |  |

Provides access to a formatting argument.

`basic_format_arg` objects are typically created by std::make_format_args and accessed through std::visit_format_arg or the `visit` member functions(since C++26).

A `basic_format_arg` object behaves as if it stores a std::variant of the following types:

- std::monostate (only if the object was default-constructed)
- bool
- Context::char_type
- int
- unsigned int
- long long int
- unsigned long long int
- float
- double
- long double
- const Context::char_type\*
- std::basic_string_view<Context::char_type>
- const void\*
- basic_format_arg::handle

### Member classes

|  |  |
| --- | --- |
| handle(C++20) | type-erased wrapper that allows formatting an object of user-defined type   (public member class) |

### Member functions

|  |  |
| --- | --- |
| (constructor)(C++20) | constructs a `std::basic_format_arg`   (public member function) |
| operator bool(C++20) | checks if the current object holds a formatting argument   (public member function) |
| visit(C++26) | visit the stored formatting argument   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| visit_format_arg(C++20) (deprecated in C++26) | argument visitation interface for user-defined formatters   (function template) |

## std::basic_format_arg::basic_format_arg

|  |  |  |
| --- | --- | --- |
| basic_format_arg() noexcept; |  | (since C++20) |
|  |  |  |

Default constructor. Constructs a `basic_format_arg` that does not hold a formatting argument. The stored object has type std::monostate.

To create a `basic_format_arg` that holds a formatting argument, std::make_format_args has to be used.

## std::basic_format_arg::operator bool

|  |  |  |
| --- | --- | --- |
| explicit operator bool() const noexcept; |  | (since C++20) |
|  |  |  |

Checks whether \*this holds a formatting argument.

Returns true if \*this holds a formatting argument (i.e. the stored object does not have type std::monostate), false otherwise.

## std::basic_format_arg::visit

|  |  |  |
| --- | --- | --- |
| template< class Visitor >  decltype(auto) visit( this basic_format_arg arg, Visitor&& vis ); | (1) | (since C++26) |
| template< class R, class Visitor >  R visit( this basic_format_arg arg, Visitor&& vis ); | (2) | (since C++26) |
|  |  |  |

Applies the visitor vis to the object contained in arg.

The `visit` functions do not modify the `basic_format_arg` object on which it is called because a copy of the object is used when calling vis.

1) Equivalent to return std::visit(std::forward<Visitor>(vis), v);, where `v` is the std::variant stored in arg.2) Equivalent to return std::visit<R>(std::forward<Visitor>(vis), v);, where `v` is the std::variant stored in arg.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_format` | `202306L` | (C++26) | Member `visit` |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| basic_format_argsformat_argswformat_args(C++20)(C++20)(C++20) | class that provides access to all formatting arguments   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/format/basic_format_arg&oldid=159698>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 September 2023, at 04:02.