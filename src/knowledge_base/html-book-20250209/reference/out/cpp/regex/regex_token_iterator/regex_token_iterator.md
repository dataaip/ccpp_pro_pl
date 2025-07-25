# std::regex_token_iterator<BidirIt,CharT,Traits>::regex_token_iterator

From cppreference.com
< cpp‎ | regex‎ | regex token iterator
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
| match_flag_type(C++11) | | | | |
| error_type(C++11) | | | | |
| Regex Grammar | | | | |
| Modified ECMAScript-262(C++11) | | | | |

std::regex_token_iterator

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****regex_token_iterator::regex_token_iterator**** | | | | |
| regex_token_iterator::operator= | | | | |
| Comparisons | | | | |
| regex_token_iterator::operator==regex_token_iterator::operator!=(until C++20) | | | | |
| Observers | | | | |
| regex_token_iterator::operator\*regex_token_iterator::operator-> | | | | |
| Modifiers | | | | |
| regex_token_iterator::operator++regex_token_iterator::operator++(int) | | | | |

|  |  |  |
| --- | --- | --- |
| regex_token_iterator(); | (1) | (since C++11) |
| regex_token_iterator( BidirIt a, BidirIt b,  const regex_type& re,                        int submatch = 0,                        std::regex_constants::match_flag_type m = std::regex_constants::match_default ); | (2) | (since C++11) |
| regex_token_iterator( BidirIt a, BidirIt b,  const regex_type& re,                        const std::vector<int>& submatches,                        std::regex_constants::match_flag_type m = std::regex_constants::match_default ); | (3) | (since C++11) |
| regex_token_iterator( BidirIt a, BidirIt b,  const regex_type& re,                        std::initializer_list<int> submatches,                        std::regex_constants::match_flag_type m = std::regex_constants::match_default ); | (4) | (since C++11) |
| template< std::size_t N >  regex_token_iterator( BidirIt a, BidirIt b,                        const regex_type& re,                        const int (&submatches)[N],                        std::regex_constants::match_flag_type m = std::regex_constants::match_default ); | (5) | (since C++11) |
| regex_token_iterator( const regex_token_iterator& other ); | (6) | (since C++11) |
| regex_token_iterator( BidirIt a, BidirIt b,  const regex_type&& re,                        int submatch = 0,                        std::regex_constants::match_flag_type m = std::regex_constants::match_default ) = delete; | (7) | (since C++11) |
| regex_token_iterator( BidirIt a, BidirIt b,  const regex_type&& re,                        const std::vector<int>& submatches,                        std::regex_constants::match_flag_type m = std::regex_constants::match_default ) = delete; | (8) | (since C++11) |
| regex_token_iterator( BidirIt a, BidirIt b,  const regex_type&& re,                        std::initializer_list<int> submatches,                        std::regex_constants::match_flag_type m = std::regex_constants::match_default ) = delete; | (9) | (since C++11) |
| template< std::size_t N >  regex_token_iterator( BidirIt a, BidirIt b,                        const regex_type&& re,                        const int (&submatches)[N],                        std::regex_constants::match_flag_type m = std::regex_constants::match_default ) = delete; | (10) | (since C++11) |
|  |  |  |

Constructs a new `regex_token_iterator`:

1) Default constructor. Constructs the end-of-sequence iterator.2-5) First, copies the list of the requested submatch out of the submatches or submatch argument into the member list stored in the iterator and constructs the member std::regex_iterator by passing a, b, re, and m to its four-argument constructor (that constructor performs the initial call to std::regex_search) and sets the internal counter of submatches to zero.

- If, after construction, the member `regex_iterator` is not an end-of-sequence iterator, sets the member pointer to the address of the current std::sub_match.
- Otherwise (if the member `regex_iterator` is an end-of-sequence iterator), but the value -1 is one of the values in submatches/submatch, turns \*this into a **suffix iterator** pointing at the range ``a`,`b`)` (the entire string is the non-matched suffix).
- Otherwise (if -1 is not in the list of submatches), turns \*this into the end-of-sequence iterator.

The behavior is undefined if any value in submatches is less than -1.

6) Copy constructor: performs member-wise copy (including making a copy of the member `regex_iterator` and the member pointer to current sub_match).7-10) The overloads (2-5) are prohibited from being called with a temporary regex since otherwise the returned iterator would be immediately invalidated.

### Parameters

|  |  |  |
| --- | --- | --- |
| a | - | [LegacyBidirectionalIterator to the beginning of the target character sequence |
| b | - | LegacyBidirectionalIterator to the end of the target character sequence |
| re | - | regular expression used to search the target character sequence |
| submatch | - | the index of the submatch that should be returned. "0" represents the entire match, and "-1" represents the parts that are not matched (e.g, the stuff between matches) |
| submatches | - | the sequence of submatch indices that should be iterated over within each match, may include the special value -1 for the non-matched fragments |
| m | - | flags that govern the behavior of re |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2332 | C++11 | a `regex_token_iterator` constructed from a temporary `basic_regex` became invalid immediately | such construction is disallowed via deleted overloads |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/regex_token_iterator/regex_token_iterator&oldid=160539>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 October 2023, at 10:14.