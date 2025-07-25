# std::strxfrm

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | atof | | | | | | atoiatolatoll(C++11) | | | | | | strtolstrtoll(C++11) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strtoulstrtoull(C++11) | | | | | | strtofstrtodstrtold(C++11)(C++11) | | | | | | strtoimaxstrtouimax(C++11)(C++11) | | | | | |
| String manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcpy | | | | | | strncpy | | | | | | ****strxfrm**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcat | | | | | | strncat | | | | | |  | | | | | |
| String examination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlen | | | | | | strcmp | | | | | | strncmp | | | | | | strcoll | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | strtok | | | | | |  | | | | | |
| Character array functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpy | | | | | | memmove | | | | | |  | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strerror | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstring>` |  |  |
| std::size_t strxfrm( char\* dest, const char\* src, std::size_t count ); |  |  |
|  |  |  |

Transforms the null-terminated byte string pointed to by src into the implementation-defined form such that comparing two transformed strings with std::strcmp gives the same result as comparing the original strings with std::strcoll, in the current C locale.

The first count characters of the transformed string are written to destination, including the terminating null character, and the length of the full transformed string is returned, excluding the terminating null character.

The behavior is undefined if the dest array is not large enough. The behavior is undefined if dest and src overlap.

If count is ​0​, then dest is allowed to be a null pointer.

### Notes

The correct length of the buffer that can receive the entire transformed string is 1 + std::strxfrm(nullptr, src, 0).

This function is used when making multiple locale-dependent comparisons using the same string or set of strings, because it is more efficient to use ****std::strxfrm**** to transform all the strings just once, and subsequently compare the transformed strings with std::strcmp.

### Parameters

|  |  |  |
| --- | --- | --- |
| dest | - | pointer to the first element of the array where the transformed string will be written |
| src | - | pointer to the first character of a null-terminated byte string to transform |
| count | - | maximum number of characters to be written |

### Return value

The length of the transformed string, not including the terminating null-character.

### Example

Run this code

```
#include <cassert>
#include <cstring>
#include <iomanip>
#include <iostream>
#include <string>
 
int main()
{
    char* loc = std::setlocale(LC_COLLATE, "cs_CZ.iso88592");
    assert(loc);
 
    std::string in1 = "hrnec";
    std::string out1(1 + std::strxfrm(nullptr, in1.c_str(), 0), ' ');
    std::string in2 = "chrt";
    std::string out2(1 + std::strxfrm(nullptr, in2.c_str(), 0), ' ');
 
    std::strxfrm(&out1[0], in1.c_str(), out1.size());
    std::strxfrm(&out2[0], in2.c_str(), out2.size());
 
    std::cout << "In the Czech locale: ";
    if (out1 < out2)
        std::cout << in1 << " before " << in2 << '\n';
    else
        std::cout << in2 << " before " << in1 << '\n';
 
    std::cout << "In lexicographical comparison: ";
    if (in1 < in2)
        std::cout << in1 << " before " << in2 << '\n';
    else
        std::cout << in2 << " before " << in1 << '\n';
}

```

Possible output:

```
In the Czech locale: hrnec before chrt
In lexicographical comparison: chrt before hrnec

```

### See also

|  |  |
| --- | --- |
| wcsxfrm | transform a wide string so that `wcscmp` would produce the same result as `wcscoll`   (function) |
| do_transform[virtual] | transforms a string so that collation can be replaced by comparison   (virtual protected member function of `std::collate<CharT>`) |
| strcoll | compares two strings in accordance to the current locale   (function) |
| C documentation for strxfrm | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/byte/strxfrm&oldid=152868>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 June 2023, at 09:06.