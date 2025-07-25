# strcmp

From cppreference.com
< c‎ | string‎ | byte
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 Strings library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Null-terminated byte strings | | | | |
| Null-terminated multibyte strings | | | | |
| Null-terminated wide strings | | | | |

 Null-terminated byte strings

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Character manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | isalnum | | | | | | isalpha | | | | | | islower | | | | | | isupper | | | | | | isdigit | | | | | | isxdigit | | | | | | isblank(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iscntrl | | | | | | isgraph | | | | | | isspace | | | | | | isprint | | | | | | ispunct | | | | | | tolower | | | | | | toupper | | | | | |
| Conversions to and from numeric formats | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | atoiatolatoll(C99) | | | | | | atof | | | | | | strtolstrtoll(C99) | | | | | | strtoulstrtoull(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strtoimaxstrtoumax(C99)(C99) | | | | | | strtofstrtodstrtold(C99)(C99) | | | | | | strfromfstrfromdstrfroml(C23)(C23)(C23) | | | | | |
| String manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcpystrcpy_s(C11) | | | | | | strncpystrncpy_s(C11) | | | | | | strcatstrcat_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strncatstrncat_s(C11) | | | | | | strxfrm | | | | | | strdup(C23) | | | | | | strndup(C23) | | | | | |  | | | | | |
| String examination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlenstrnlen_s(C11) | | | | | | ****strcmp**** | | | | | | strncmp | | | | | | strcoll | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | strtokstrtok_s(C11) | | | | | |  | | | | | |
| Memory manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memsetmemset_explicitmemset_s(C23)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpymemcpy_s(C11) | | | | | | memmovememmove_s(C11) | | | | | | memccpy(C23) | | | | | |
| Miscellaneous | | | | |
| strerrorstrerror_sstrerrorlen_s(C11)(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<string.h>` |  |  |
| int strcmp( const char\* lhs, const char\* rhs ); |  |  |
|  |  |  |

Compares two null-terminated byte strings lexicographically.

The sign of the result is the sign of the difference between the values of the first pair of characters (both interpreted as unsigned char) that differ in the strings being compared.

The behavior is undefined if lhs or rhs are not pointers to null-terminated byte strings.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | pointers to the null-terminated byte strings to compare |

### Return value

Negative value if lhs appears before rhs in lexicographical order.

Zero if lhs and rhs compare equal.

Positive value if lhs appears after rhs in lexicographical order.

### Notes

This function is not locale-sensitive, unlike strcoll and strxfrm.

### Example

Run this code

```
#include <stdio.h>
#include <string.h>
 
void demo(const char* lhs, const char* rhs)
{
    const int rc = strcmp(lhs, rhs);
    const char* rel = rc < 0 ? "precedes" : rc > 0 ? "follows" : "equals";
    printf("[%s] %s [%s]\n", lhs, rel, rhs);
}
 
int main(void)
{
    const char* string = "Hello World!";
    demo(string, "Hello!");
    demo(string, "Hello");
    demo(string, "Hello there");
    demo("Hello, everybody!" + 12, "Hello, somebody!" + 11);
}

```

Output:

```
[Hello World!] precedes [Hello!]
[Hello World!] follows [Hello]
[Hello World!] precedes [Hello there]
[body!] equals [body!]

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.24.4.2 The strcmp function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.24.4.2 The strcmp function (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.24.4.2 The strcmp function (p: 365-366)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.21.4.2 The strcmp function (p: 328-329)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.11.4.2 The strcmp function

### See also

|  |  |
| --- | --- |
| strncmp | compares a certain amount of characters of two strings   (function) |
| wcscmp(C95) | compares two wide strings   (function) |
| memcmp | compares two buffers   (function) |
| strcoll | compares two strings in accordance to the current locale   (function) |
| C++ documentation for strcmp | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/byte/strcmp&oldid=172146>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 May 2024, at 09:49.