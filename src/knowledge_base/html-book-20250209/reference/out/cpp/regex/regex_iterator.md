# std::regex_iterator

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
| ****regex_iterator****(C++11) | | | | |
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

****std::regex_iterator****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| regex_iterator::regex_iterator | | | | |
| regex_iterator::operator= | | | | |
| Comparisons | | | | |
| regex_iterator::operator==regex_iterator::operator!=(until C++20) | | | | |
| Observers | | | | |
| regex_iterator::operator\*regex_iterator::operator-> | | | | |
| Modifiers | | | | |
| regex_iterator::operator++regex_iterator::operator++(int) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<regex>` |  |  |
| template<  class BidirIt,      class CharT = typename std::iterator_traits<BidirIt>::value_type,      class Traits = std::regex_traits<CharT> > class regex_iterator |  | (since C++11) |
|  |  |  |

`std::regex_iterator` is a read-only iterator that accesses the individual matches of a regular expression within the underlying character sequence. It meets the requirements of a LegacyForwardIterator, except that for dereferenceable values a and b with a == b, \*a and \*b will not be bound to the same object.

On construction, and on every increment, it calls std::regex_search and remembers the result (that is, saves a copy of the std::match_results<BidirIt> value). The first object may be read when the iterator is constructed or when the first dereferencing is done. Otherwise, dereferencing only returns a copy of the most recently obtained regex match.

The default-constructed `std::regex_iterator` is the end-of-sequence iterator. When a valid `std::regex_iterator` is incremented after reaching the last match (std::regex_search returns false), it becomes equal to the end-of-sequence iterator. Dereferencing or incrementing it further invokes undefined behavior.

A typical implementation of `std::regex_iterator` holds the begin and the end iterators for the underlying sequence (two instances of `BidirIt`), a pointer to the regular expression (const regex_type\*), the match flags (std::regex_constants::match_flag_type), and the current match (std::match_results<BidirIt>).

### Type requirements

|  |  |  |
| --- | --- | --- |
| -`BidirIt` must meet the requirements of LegacyBidirectionalIterator. | | |

### Specializations

Several specializations for common character sequence types are defined:

|  |  |
| --- | --- |
| Defined in header `<regex>` | |
| Type | Definition |
| `std::cregex_iterator` | std::regex_iterator<const char\*> |
| `std::wcregex_iterator` | std::regex_iterator<const wchar_t\*> |
| `std::sregex_iterator` | std::regex_iterator<std::string::const_iterator> |
| `std::wsregex_iterator` | std::regex_iterator<std::wstring::const_iterator> |

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `value_type` | std::match_results<BidirIt> |
| `difference_type` | std::ptrdiff_t |
| `pointer` | const value_type\* |
| `reference` | const value_type& |
| `iterator_category` | std::forward_iterator_tag |
| `iterator_concept` (C++20) | std::input_iterator_tag |
| `regex_type` | std::basic_regex<CharT, Traits> |

### Data members

|  |  |
| --- | --- |
| Member | Description |
| `BidiIt` `begin` (private) | the begin iterator (exposition-only member object\*) |
| `BidiIt` `end` (private) | the end iterator (exposition-only member object\*) |
| const regex_type\* `pregex` (private) | a pointer to a regular expression (exposition-only member object\*) |
| regex_constants::match_flag_type `flags` (private) | a flag (exposition-only member object\*) |
| match_results<BidiIt> `match` (private) | the current match (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new `regex_iterator`   (public member function) |
| (destructor)(implicitly declared) | destructs a `regex_iterator`, including the cached value   (public member function) |
| operator= | assigns contents   (public member function) |
| operator==operator!=(removed in C++20) | compares two `regex_iterator`s   (public member function) |
| operator\*operator-> | accesses the current match   (public member function) |
| operator++operator++(int) | advances the iterator to the next match   (public member function) |

### Notes

It is the programmer's responsibility to ensure that the std::basic_regex object passed to the iterator's constructor outlives the iterator. Because the iterator stores a pointer to the regex, incrementing the iterator after the regex was destroyed accesses a dangling pointer.

If the part of the regular expression that matched is just an assertion (`^`, `$`, `\b`, `\B`), the match stored in the iterator is a zero-length match, that is, match[0].first == match[0].second.

### Example

Run this code

```
#include <iostream>
#include <iterator>
#include <regex>
#include <string>
 
int main()
{
    const std::string s = "Quick brown fox.";
 
    std::regex words_regex("[^\\s]+");
    auto words_begin = std::sregex_iterator(s.begin(), s.end(), words_regex);
    auto words_end = std::sregex_iterator();
 
    std::cout << "Found " << std::distance(words_begin, words_end) << " words:\n";
 
    for (std::sregex_iterator i = words_begin; i != words_end; ++i)
    {
        std::smatch match = *i;
        std::string match_str = match.str();
        std::cout << match_str << '\n';
    }
}

```

Output:

```
Found 3 words:
Quick
brown
fox.

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3698 (P2770R0) | C++20 | `regex_iterator` was a `forward_iterator` while being a stashing iterator | made `input_iterator`[[1]](regex_iterator.html#cite_note-1) |

1. ↑ `iterator_category` was unchanged by the resolution, because changing it to std::input_iterator_tag might break too much existing code.

### See also

|  |  |
| --- | --- |
| match_results(C++11) | identifies one regular expression match, including all sub-expression matches   (class template) |
| regex_search(C++11) | attempts to match a regular expression to any part of a character sequence   (function template) |

|  |
| --- |
|  |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/regex_iterator&oldid=179535>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 January 2025, at 16:54.