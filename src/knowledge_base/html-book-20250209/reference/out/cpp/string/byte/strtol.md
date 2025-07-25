# std::strtol, std::strtoll

From cppreference.com
< cpp‎ | string‎ | byte
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

Null-terminated byte strings

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Character classification | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | isalnum | | | | | | isalpha | | | | | | islower | | | | | | isupper | | | | | | isdigit | | | | | | isxdigit | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isblank(C++11) | | | | | | iscntrl | | | | | | isgraph | | | | | | isspace | | | | | | isprint | | | | | | ispunct | | | | | |
| Character manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tolower | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | toupper | | | | | |
| Conversions to numeric formats | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | atof | | | | | | atoiatolatoll(C++11) | | | | | | ****strtolstrtoll****(C++11) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strtoulstrtoull(C++11) | | | | | | strtofstrtodstrtold(C++11)(C++11) | | | | | | strtoimaxstrtouimax(C++11)(C++11) | | | | | |
| String manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcpy | | | | | | strncpy | | | | | | strxfrm | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcat | | | | | | strncat | | | | | |  | | | | | |
| String examination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlen | | | | | | strcmp | | | | | | strncmp | | | | | | strcoll | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | strtok | | | | | |  | | | | | |
| Character array functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpy | | | | | | memmove | | | | | |  | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strerror | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstdlib>` |  |  |
| long      strtol( const char\* str, char\*\* str_end, int base ); | (1) |  |
| long long strtoll( const char\* str, char\*\* str_end, int base ); | (2) | (since C++11) |
|  |  |  |

Interprets an integer value in a byte string pointed to by str.

Discards any whitespace characters (as identified by calling std::isspace) until the first non-whitespace character is found, then takes as many characters as possible to form a valid **base-n** (where n=`base`) integer number representation and converts them to an integer value. The valid integer value consists of the following parts:

- (optional) plus or minus sign
- (optional) prefix (`0`) indicating octal base (applies only when the base is 8 or ​0​)
- (optional) prefix (`0x` or `0X`) indicating hexadecimal base (applies only when the base is 16 or ​0​)
- a sequence of digits

The set of valid values for base is `{0, 2, 3, ..., 36}`. The set of valid digits for base-`2` integers is `{0, 1}`, for base-`3` integers is `{0, 1, 2}`, and so on. For bases larger than `10`, valid digits include alphabetic characters, starting from `Aa` for base-`11` integer, to `Zz` for base-`36` integer. The case of the characters is ignored.

Additional numeric formats may be accepted by the currently installed C locale.

If the value of `base` is ​0​, the numeric base is auto-detected: if the prefix is `0`, the base is octal, if the prefix is `0x` or `0X`, the base is hexadecimal, otherwise the base is decimal.

If the minus sign was part of the input sequence, the numeric value calculated from the sequence of digits is negated as if by unary minus in the result type.

The function sets the pointer pointed to by str_end to point to the character past the last character interpreted. If str_end is a null pointer, it is ignored.

If the str is empty or does not have the expected form, no conversion is performed, and (if str_end is not a null pointer) the value of str is stored in the object pointed to by str_end.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | pointer to the null-terminated byte string to be interpreted |
| str_end | - | pointer to a pointer to character |
| base | - | **base** of the interpreted integer value |

### Return value

- If successful, an integer value corresponding to the contents of str is returned.
- If the converted value falls out of range of corresponding return type, a range error occurs (setting errno to ERANGE) and LONG_MAX, LONG_MIN, LLONG_MAX or LLONG_MIN is returned.
- If no conversion can be performed, ​0​ is returned.

### Example

Run this code

```
#include <cerrno>
#include <cstdlib>
#include <iomanip>
#include <iostream>
#include <string>
 
int main()
{
    const char* p = "10 200000000000000000000000000000 30 -40";
    std::cout << "Parsing " << std::quoted(p) << ":\n";
 
    for (;;)
    {
        // errno can be set to any non-zero value by a library function call
        // regardless of whether there was an error, so it needs to be cleared
        // in order to check the error set by strtol
        errno = 0;
        char* p_end{};
        const long i = std::strtol(p, &p_end, 10);
        if (p == p_end)
            break;
 
        const bool range_error = errno == ERANGE;
        const std::string extracted(p, p_end - p);
        p = p_end;
 
        std::cout << "Extracted " << std::quoted(extracted)
                  << ", strtol returned " << i << '.';
        if (range_error)
            std::cout << "\n  Range error occurred.";
 
        std::cout << '\n';
    }
}

```

Possible output:

```
Parsing "10 200000000000000000000000000000 30 -40":
Extracted "10", strtol returned 10.
Extracted " 200000000000000000000000000000", strtol returned 9223372036854775807.
  Range error occurred.
Extracted " 30", strtol returned 30.
Extracted " -40", strtol returned -40.

```

### See also

|  |  |
| --- | --- |
| stoistolstoll(C++11)(C++11)(C++11) | converts a string to a signed integer   (function) |
| strtoulstrtoull(C++11) | converts a byte string to an unsigned integer value   (function) |
| strtoimaxstrtoumax(C++11)(C++11) | converts a byte string to std::intmax_t or std::uintmax_t   (function) |
| wcstolwcstoll | converts a wide string to an integer value   (function) |
| strtofstrtodstrtold | converts a byte string to a floating-point value   (function) |
| from_chars(C++17) | converts a character sequence to an integer or floating-point value   (function) |
| atoiatolatoll(C++11) | converts a byte string to an integer value   (function) |
| C documentation for strtol, strtoll | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/byte/strtol&oldid=152866>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 June 2023, at 08:56.