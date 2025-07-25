# std::experimental::basic_string_view

From cppreference.com
< cpp‎ | experimental
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Library fundamentals

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::optional | | | | |
| experimental::any | | | | |
| ****experimental::basic_string_view**** | | | | |
| experimental::sample | | | | |
| experimental::shared_ptr | | | | |
| experimental::weak_ptr | | | | |
| experimental::apply | | | | |
| experimental::invocation_typeexperimental::raw_invocation_type | | | | |
| experimental::search | | | | |
| experimental::default_searcherexperimental::make_default_searcher | | | | |
| experimental::boyer_moore_searcherexperimental::make_boyer_moore_searcher | | | | |
| experimental::boyer_moore_horspool_searcherexperimental::make_boyer_moore_horspool_searcher | | | | |
| Type-erased and polymorphic allocators | | | | |
| Variable templates for type traits | | | | |

****std::experimental::basic_string_view****

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string_view::basic_string_view | | | | | | basic_string_view::operator= | | | | | | Iterators | | | | | | basic_string_view::beginbasic_string_view::cbegin | | | | | | basic_string_view::endbasic_string_view::cend | | | | | | basic_string_view::rbeginbasic_string_view::crbegin | | | | | | basic_string_view::rendbasic_string_view::crend | | | | | | Element access | | | | | | basic_string_view::at | | | | | | [basic_string_view::operator[]](basic_string_view/operator_at.html "cpp/experimental/basic string view/operator at") | | | | | | basic_string_view::front | | | | | | basic_string_view::back | | | | | | basic_string_view::data | | | | | | Capacity | | | | | | basic_string_view::sizebasic_string_view::length | | | | | | basic_string_view::max_size | | | | | | basic_string_view::empty | | | | | | Modifiers | | | | | | basic_string_view::remove_prefix | | | | | | basic_string_view::remove_suffix | | | | | | basic_string_view::swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Operations | | | | | | basic_string_view::to_stringbasic_string_view::operator basic_string | | | | | | basic_string_view::copy | | | | | | basic_string_view::substr | | | | | | basic_string_view::compare | | | | | | basic_string_view::find | | | | | | basic_string_view::rfind | | | | | | basic_string_view::find_first_of | | | | | | basic_string_view::find_last_of | | | | | | basic_string_view::find_first_not_of | | | | | | basic_string_view::find_last_not_of | | | | | | Constants | | | | | | basic_string_view::npos | | | | | | Non-member functions | | | | | | operator==operator!=operator<operator>operator<=operator>= | | | | | | operator<< | | | | | | Helper classes | | | | | | hash<std::string_view>hash<std::wstring_view>hash<std::u16string_view>hash<std::u32string_view> | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/string_view>` |  |  |
| template<   class CharT,       class Traits = std::char_traits<CharT> > class basic_string_view; |  | (library fundamentals TS) |
|  |  |  |

The class template `basic_string_view` describes an object that can refer to a constant contiguous sequence of char-like objects with the first element of the sequence at position zero.

A typical implementation holds only two members: a pointer to constant `CharT` and a size.

Several typedefs for common character types are provided:

|  |  |
| --- | --- |
| Defined in header `<experimental/string_view>` | |
| Type | Definition |
| ****std::experimental::string_view**** | std::experimental::basic_string_view<char> |
| ****std::experimental::wstring_view**** | std::experimental::basic_string_view<wchar_t> |
| ****std::experimental::u16string_view**** | std::experimental::basic_string_view<char16_t> |
| ****std::experimental::u32string_view**** | std::experimental::basic_string_view<char32_t> |

### Template parameters

|  |  |  |
| --- | --- | --- |
| CharT | - | character type |
| Traits | - | traits class specifying the operations on the character type |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `traits_type` | `Traits` |
| `value_type` | `CharT` |
| `pointer` | `CharT*` |
| `const_pointer` | `const CharT*` |
| `reference` | `CharT&` |
| `const_reference` | `const CharT&` |
| `const_iterator` | implementation-defined LegacyRandomAccessIterator |
| `iterator` | `const_iterator` |
| `reverse_iterator` | `const_reverse_iterator` |
| `const_reverse_iterator` | std::reverse_iterator<const_iterator> |
| `size_type` | std::size_t |
| `difference_type` | std::ptrdiff_t |

Note: `iterator` and `const_iterator` are the same type because string views are views into constant character sequences.

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `basic_string_view`   (public member function) |
| operator= | assigns a view   (public member function) |
| Iterators | |
| begincbegin | returns an iterator to the beginning   (public member function) |
| endcend | returns an iterator to the end   (public member function) |
| rbegincrbegin | returns a reverse iterator to the beginning   (public member function) |
| rendcrend | returns a reverse iterator to the end   (public member function) |
| Element access | |
| [operator[]](basic_string_view/operator_at.html "cpp/experimental/basic string view/operator at") | access specified character   (public member function) |
| at | access specified character with bounds checking   (public member function) |
| front | accesses the first character   (public member function) |
| back | accesses the last character   (public member function) |
| data | returns a pointer to the first character of a view   (public member function) |
| Capacity | |
| sizelength | returns the number of characters   (public member function) |
| max_size | returns the maximum number of characters   (public member function) |
| empty | checks whether the view is empty   (public member function) |
| Modifiers | |
| remove_prefix | shrinks the view by moving its start forward   (public member function) |
| remove_suffix | shrinks the view by moving its end backward   (public member function) |
| swap | swaps the contents   (public member function) |
| Operations | |
| to_stringoperator basic_string | creates a string from the view   (public member function) |
| copy | copies characters   (public member function) |
| substr | returns a substring   (public member function) |
| compare | compares two views   (public member function) |
| find | find characters in the view   (public member function) |
| rfind | find the last occurrence of a substring   (public member function) |
| find_first_of | find first occurrence of characters   (public member function) |
| find_last_of | find last occurrence of characters   (public member function) |
| find_first_not_of | find first absence of characters   (public member function) |
| find_last_not_of | find last absence of characters   (public member function) |
| Constants | |
| npos[static] | special value. The exact meaning depends on the context   (public static member constant) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=operator<operator>operator<=operator>= | lexicographically compares two views   (function template) |
| Input/output | |
| operator<< | performs stream output on views   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::hash<std::experimental::string_view>std::hash<std::experimental::wstring_view>std::hash<std::experimental::u16string_view>std::hash<std::experimental::u32string_view> | hash support for views   (class template specialization) |

### Feature test macros

|  |  |
| --- | --- |
| __cpp_lib_experimental_string_view | a value of at least 201411 indicates that basic_string_view template is supported   (macro constant) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/basic_string_view&oldid=163664>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 November 2023, at 06:35.