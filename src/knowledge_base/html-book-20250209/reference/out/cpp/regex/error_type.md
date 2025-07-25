# std::regex_constants::error_type

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
| match_flag_type(C++11) | | | | |
| ****error_type****(C++11) | | | | |
| Regex Grammar | | | | |
| Modified ECMAScript-262(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<regex>` |  |  |
| using error_type = /\* implementation-defined \*/; | (1) | (since C++11) |
| constexpr error_type error_collate =    /\* unspecified \*/;  constexpr error_type error_ctype =      /\* unspecified \*/;  constexpr error_type error_escape =     /\* unspecified \*/;  constexpr error_type error_backref =    /\* unspecified \*/;  constexpr error_type error_brack =      /\* unspecified \*/;  constexpr error_type error_paren =      /\* unspecified \*/;  constexpr error_type error_brace =      /\* unspecified \*/;  constexpr error_type error_badbrace =   /\* unspecified \*/;  constexpr error_type error_range =      /\* unspecified \*/;  constexpr error_type error_space =      /\* unspecified \*/;  constexpr error_type error_badrepeat =  /\* unspecified \*/;  constexpr error_type error_complexity = /\* unspecified \*/; constexpr error_type error_stack =      /\* unspecified \*/; | (2) | (since C++11)  (inline since C++17) |
|  |  |  |

1) The `error_type` is a type that describes errors that may occur during regular expression parsing.

### Constants

|  |  |
| --- | --- |
| Name | Explanation |
| `error_collate` | the expression contains an invalid collating element name |
| `error_ctype` | the expression contains an invalid character class name |
| `error_escape` | the expression contains an invalid escaped character or a trailing escape |
| `error_backref` | the expression contains an invalid back reference |
| `error_brack` | the expression contains mismatched square brackets ('[' and ']') |
| `error_paren` | the expression contains mismatched parentheses ('(' and ')') |
| `error_brace` | the expression contains mismatched curly braces ('{' and '}') |
| `error_badbrace` | the expression contains an invalid range in a {} expression |
| `error_range` | the expression contains an invalid character range (e.g. [b-a]) |
| `error_space` | there was not enough memory to convert the expression into a finite state machine |
| `error_badrepeat` | '\*', '?', '+' or '{' was not preceded by a valid regular expression |
| `error_complexity` | the complexity of an attempted match exceeded a predefined level |
| `error_stack` | there was not enough memory to perform a match |

### Example

Implements regular expressions checker:

Run this code

```
#include <cstddef>
#include <iomanip>
#include <iostream>
#include <regex>
#include <sstream>
#include <string>
 
void regular_expression_checker(const std::string& text,
                                const std::string& regex,
                                const std::regex::flag_type flags)
{
    std::cout << "Text: " << std::quoted(text) << '\n'
              << "Regex: " << std::quoted(regex) << '\n';
 
    try
    {
        const std::regex re{regex, flags};
        const bool matched = std::regex_match(text, re);
 
        std::stringstream out;
        out << (matched ? "MATCH!\n" : "DOES NOT MATCH!\n");
 
        std::smatch m;
        if (std::regex_search(text, m, re); !m.empty())
        {
            out << "prefix = [" << m.prefix().str().data() << "]\n";
 
            for (std::size_t i{}; i != m.size(); ++i)
                out << "  m[" << i << "] = [" << m[i].str().data() << "]\n";
 
            out << "suffix = [" << m.suffix().str().data() << "]\n";
        }
        std::cout << out.str() << '\n';
    }
    catch (std::regex_error& e)
    {
        std::cout << "Error: " << e.what() << ".\n\n";
    }
}
 
int main()
{
    constexpr std::regex::flag_type your_flags
        = std::regex::flag_type{0}
    // Choose one of the supported grammars:
        | std::regex::ECMAScript
    //  | std::regex::basic
    //  | std::regex::extended
    //  | std::regex::awk
    //  | std::regex::grep
    //  | std::regex::egrep
    // Choose any of the next options:
    //  | std::regex::icase
    //  | std::regex::nosubs
    //  | std::regex::optimize
    //  | std::regex::collate
    //  | std::regex::multiline
        ;
 
    const std::string your_text = "Hello regular expressions.";
    const std::string your_regex = R"(([a-zA-Z]+) ([a-z]+) ([a-z]+)\.)";
    regular_expression_checker(your_text, your_regex, your_flags);
 
    regular_expression_checker("Invalid!", R"(((.)(.))", your_flags);
    regular_expression_checker("Invalid!", R"([.)", your_flags);
    regular_expression_checker("Invalid!", R"([.]{})", your_flags);
    regular_expression_checker("Invalid!", R"([1-0])", your_flags);
}

```

Possible output:

```
Text: "Hello regular expressions."
Regex: "([a-zA-Z]+) ([a-z]+) ([a-z]+)\\."
MATCH!
prefix = []
  m[0] = [Hello regular expressions.]
  m[1] = [Hello]
  m[2] = [regular]
  m[3] = [expressions]
suffix = []
 
Text: "Invalid!"
Regex: "((.)(.)"
Error: Mismatched '(' and ')' in regular expression.
 
Text: "Invalid!"
Regex: "[."
Error: Unexpected character within '[...]' in regular expression.
 
Text: "Invalid!"
Regex: "[.]{}"
Error: Invalid range in '{}' in regular expression.
 
Text: "Invalid!"
Regex: "[1-0]"
Error: Invalid range in bracket expression..

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2053 | C++11 | the constants were declared static | removed the static specifier |

### See also

|  |  |
| --- | --- |
| regex_error(C++11) | reports errors generated by the regular expressions library   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/error_type&oldid=173770>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 July 2024, at 03:02.