# std::basic_regex<CharT,Traits>::basic_regex

From cppreference.com
< cpp‎ | regex‎ | basic regex
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

std::basic_regex

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member Functions | | | | |
| ****basic_regex::basic_regex**** | | | | |
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
| basic_regex(); | (1) | (since C++11) |
| explicit basic_regex( const CharT\* s,                        flag_type f = std::regex_constants::ECMAScript ); | (2) | (since C++11) |
| basic_regex( const CharT\* s, std::size_t count,               flag_type f = std::regex_constants::ECMAScript ); | (3) | (since C++11) |
| basic_regex( const basic_regex& other ); | (4) | (since C++11) |
| basic_regex( basic_regex&& other ) noexcept; | (5) | (since C++11) |
| template< class ST, class SA >  explicit basic_regex( const std::basic_string<CharT,ST,SA>& str,                       flag_type f = std::regex_constants::ECMAScript ); | (6) | (since C++11) |
| template< class ForwardIt >  basic_regex( ForwardIt first, ForwardIt last,              flag_type f = std::regex_constants::ECMAScript ); | (7) | (since C++11) |
| basic_regex( std::initializer_list<CharT> init,               flag_type f = std::regex_constants::ECMAScript ); | (8) | (since C++11) |
|  |  |  |

Constructs a new regular expression from a sequence of characters interpreted according to the flags f.

1) Default constructor. Constructs an empty regular expression which will match nothing.2) Constructs a regex from a null-terminated string s.3) Constructs a regex from a sequence of count characters, pointed to by s.4) Copy constructor. Constructs a regex by copying other.5) Move constructor. Constructs a regex with the contents of other using move semantics.6) Constructs a regex from a string str.7) Range constructor. Constructs the string with the contents of the range ``first`,`last`)`.8) Initializer list constructor. Constructs the string with the contents of the initializer list init.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | pointer to a null-terminated string |
| count | - | length of a character sequence used to initialize the regex |
| first, last | - | range of a character sequence used to initialize the regex |
| str | - | a basic_string used as a source used to initialize the regex |
| other | - | another regex to use as source to initialize the regex |
| init | - | initializer list used to initialize the regex |
| f | - | flags used to guide the interpretation of the character sequence as a regular expression |
| Type requirements | | |
| -`ForwardIt` must meet the requirements of [LegacyForwardIterator. | | |

### Exceptions

1) May throw implementation-defined exceptions.2,3) std::regex_error if the supplied regular expression is not valid.4) May throw implementation-defined exceptions.6-8) std::regex_error if the supplied regular expression is not valid.

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <regex>
#include <string>
 
void match_and_print(const std::string& text, const std::regex& pattern)
{
    std::sregex_iterator it(text.begin(), text.end(), pattern), it_end;
    int count = 0;
    for (; it != it_end; ++it)
    {
        const std::smatch& match = *it;
        std::cout << ++count << ". " << std::quoted(match.str()) << '\n';
    }
    std::cout << (count ? "\n" : "no match found\n\n");
}
 
int main()
{
    const std::string text = "Hello, World! 12345";
 
    // Matches one or more digits
    std::string pattern_text = "\\d+";
    std::cout << "digits (" << pattern_text << "):\n";
    auto pattern = std::regex(pattern_text);
    match_and_print(text, pattern);
 
    // Matches one or more characters split by space
    pattern_text = "[^\\s]+";
    std::cout << "words (" << pattern_text << "):\n";
    pattern = std::regex(pattern_text);
    match_and_print(text, pattern);
 
    // Matches one or more characters split by space
    pattern_text = "[a-zA-Z]+";
    std::cout << "words without symbols and digits (" << pattern_text << "):\n";
    pattern = std::regex(pattern_text);
    match_and_print(text, pattern);
 
    // Matches one non digits, non alphabet
    pattern_text = "[^0-9A-Za-z]";
    std::cout << "symbol (" << pattern_text << "):\n";
    pattern = std::regex(pattern_text);
    match_and_print(text, pattern);
 
    // Matches one or more lowercase
    pattern_text = "[a-z]+";
    std::cout << "lowercase (" << pattern_text << "):\n";
    pattern = std::regex(pattern_text);
    match_and_print(text, pattern);
 
    // Matches one or more lowercase with std::regex::icase flag
    pattern_text = "[a-z]+";
    std::cout << "lowercase with ignore case flag (" << pattern_text << "):\n";
    pattern = std::regex(pattern_text, std::regex::icase);
    match_and_print(text, pattern);
 
    // Matches basic POSIX regular expression
    pattern_text = "[[:digit:]]+";
    std::cout << "basic POSIX regex (" << pattern_text << "):\n";
    pattern = std::regex(pattern_text, std::regex::basic);
    match_and_print(text, pattern);
 
    // Matches extended POSIX regular expression
    pattern_text = "[[:digit:]]+";
    std::cout << "extended POSIX regex (" << pattern_text << "):\n";
    pattern = std::regex(pattern_text, std::regex::extended);
    match_and_print(text, pattern);
}

```

Output:

```
digits (\d+):
1. "12345"
 
words ([^\s]+):
1. "Hello,"
2. "World!"
3. "12345"
 
words without symbols and digits ([a-zA-Z]+):
1. "Hello"
2. "World"
 
symbol ([^0-9A-Za-z]):
1. ","
2. " "
3. "!"
4. " "
 
lowercase ([a-z]+):
1. "ello"
2. "orld"
 
lowercase with ignore case flag ([a-z]+):
1. "Hello"
2. "World"
 
basic POSIX regex ([[:digit:]]+):
no match found
 
extended POSIX regex ([[:digit:]]+):
1. "12345"

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/basic_regex/basic_regex&oldid=160997>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 October 2023, at 22:45.