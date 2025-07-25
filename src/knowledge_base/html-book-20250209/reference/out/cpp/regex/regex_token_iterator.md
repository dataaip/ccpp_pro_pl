# std::regex_token_iterator

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
| ****regex_token_iterator****(C++11) | | | | |
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

****std::regex_token_iterator****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| regex_token_iterator::regex_token_iterator | | | | |
| regex_token_iterator::operator= | | | | |
| Comparisons | | | | |
| regex_token_iterator::operator==regex_token_iterator::operator!=(until C++20) | | | | |
| Observers | | | | |
| regex_token_iterator::operator\*regex_token_iterator::operator-> | | | | |
| Modifiers | | | | |
| regex_token_iterator::operator++regex_token_iterator::operator++(int) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<regex>` |  |  |
| template<  class BidirIt,      class CharT = typename std::iterator_traits<BidirIt>::value_type,      class Traits = std::regex_traits<CharT> > class regex_token_iterator |  | (since C++11) |
|  |  |  |

`std::regex_token_iterator` is a read-only LegacyForwardIterator that accesses the individual sub-matches of every match of a regular expression within the underlying character sequence. It can also be used to access the parts of the sequence that were not matched by the given regular expression (e.g. as a tokenizer).

On construction, it constructs an std::regex_iterator and on every increment it steps through the requested sub-matches from the current match_results, incrementing the underlying std::regex_iterator when incrementing away from the last submatch.

The default-constructed `std::regex_token_iterator` is the end-of-sequence iterator. When a valid `std::regex_token_iterator` is incremented after reaching the last submatch of the last match, it becomes equal to the end-of-sequence iterator. Dereferencing or incrementing it further invokes undefined behavior.

Just before becoming the end-of-sequence iterator, a `std::regex_token_iterator` may become a **suffix iterator**, if the index -1 (non-matched fragment) appears in the list of the requested submatch indices. Such iterator, if dereferenced, returns a match_results corresponding to the sequence of characters between the last match and the end of sequence.

A typical implementation of `std::regex_token_iterator` holds the underlying std::regex_iterator, a container (e.g. std::vector<int>) of the requested submatch indices, the internal counter equal to the index of the submatch, a pointer to std::sub_match, pointing at the current submatch of the current match, and a std::match_results object containing the last non-matched character sequence (used in tokenizer mode).

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
| `std::cregex_token_iterator` | std::regex_token_iterator<const char\*> |
| `std::wcregex_token_iterator` | std::regex_token_iterator<const wchar_t\*> |
| `std::sregex_token_iterator` | std::regex_token_iterator<std::string::const_iterator> |
| `std::wsregex_token_iterator` | std::regex_token_iterator<std::wstring::const_iterator> |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `value_type` | std::sub_match<BidirIt> |
| `difference_type` | std::ptrdiff_t |
| `pointer` | const value_type\* |
| `reference` | const value_type& |
| `iterator_category` | std::forward_iterator_tag |
| `iterator_concept` (C++20) | std::input_iterator_tag |
| `regex_type` | std::basic_regex<CharT, Traits> |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new `regex_token_iterator`   (public member function) |
| (destructor)(implicitly declared) | destructs a `regex_token_iterator`, including the cached value   (public member function) |
| operator= | assigns contents   (public member function) |
| operator==operator!=(removed in C++20) | compares two `regex_token_iterator`s   (public member function) |
| operator\*operator-> | accesses current submatch   (public member function) |
| operator++operator++(int) | advances the iterator to the next submatch   (public member function) |

### Notes

It is the programmer's responsibility to ensure that the std::basic_regex object passed to the iterator's constructor outlives the iterator. Because the iterator stores a std::regex_iterator which stores a pointer to the regex, incrementing the iterator after the regex was destroyed results in undefined behavior.

### Example

Run this code

```
#include <algorithm>
#include <fstream>
#include <iostream>
#include <iterator>
#include <regex>
 
int main()
{
    // Tokenization (non-matched fragments)
    // Note that regex is matched only two times; when the third value is obtained
    // the iterator is a suffix iterator.
    const std::string text = "Quick brown fox.";
    const std::regex ws_re("\\s+"); // whitespace
    std::copy(std::sregex_token_iterator(text.begin(), text.end(), ws_re, -1),
              std::sregex_token_iterator(),
              std::ostream_iterator<std::string>(std::cout, "\n"));
 
    std::cout << '\n';
 
    // Iterating the first submatches
    const std::string html = R"(<p><a href="http://google.com">google</a> )"
                             R"(< a HREF ="http://cppreference.com">cppreference</a>\n</p>)";
    const std::regex url_re(R"!!(<\s*A\s+[^>]*href\s*=\s*"([^"]*)")!!", std::regex::icase);
    std::copy(std::sregex_token_iterator(html.begin(), html.end(), url_re, 1),
              std::sregex_token_iterator(),
              std::ostream_iterator<std::string>(std::cout, "\n"));
}

```

Output:

```
Quick
brown
fox.
 
http://google.com
http://cppreference.com

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3698 (P2770R0) | C++20 | `regex_token_iterator` was a `forward_iterator` while being a stashing iterator | made `input_iterator`[[1]](regex_token_iterator.html#cite_note-1) |

1. ↑ `iterator_category` was unchanged by the resolution, because changing it to std::input_iterator_tag might break too much existing code.
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/regex_token_iterator&oldid=170722>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 April 2024, at 22:58.