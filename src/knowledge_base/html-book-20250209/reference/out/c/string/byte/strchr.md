# strchr

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlenstrnlen_s(C11) | | | | | | strcmp | | | | | | strncmp | | | | | | strcoll | | | | | | ****strchr**** | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | strtokstrtok_s(C11) | | | | | |  | | | | | |
| Memory manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memsetmemset_explicitmemset_s(C23)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpymemcpy_s(C11) | | | | | | memmovememmove_s(C11) | | | | | | memccpy(C23) | | | | | |
| Miscellaneous | | | | |
| strerrorstrerror_sstrerrorlen_s(C11)(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<string.h>` |  |  |
| char\* strchr( const char\* str, int ch ); | (1) |  |
| /\*QChar\*/ \*strchr( /\*QChar\*/ \*str, int ch ); | (2) | (since C23) |
|  |  |  |

1) Finds the first occurrence of ch (after conversion to char as if by (char)ch) in the null-terminated byte string pointed to by str (each character interpreted as unsigned char). The terminating null character is considered to be a part of the string and can be found when searching for '\0'.2) Type-generic function equivalent to (1). Let `T` be an unqualified character object type.

:   - If `str` is of type const T\*, the return type is const char\*.
    - Otherwise, if `str` is of type T\*, the return type is char\*.
    - Otherwise, the behavior is undefined.

If a macro definition of each of these generic functions is suppressed to access an actual function (e.g. if (strchr) or a function pointer is used), the actual function declaration (1) becomes visible.

The behavior is undefined if str is not a pointer to a null-terminated byte string.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | pointer to the null-terminated byte string to be analyzed |
| ch | - | character to search for |

### Return value

Pointer to the found character in str, or null pointer if no such character is found.

### Example

Run this code

```
#include <stdio.h>
#include <string.h>
 
int main(void)
{
    const char *str = "Try not. Do, or do not. There is no try.";
    char target = 'T';
    const char* result = str;
 
    while((result = strchr(result, target)) != NULL)
    {
        printf("Found '%c' starting at '%s'\n", target, result);
        ++result; // Increment result, otherwise we'll find target at the same location
    }
}

```

Output:

```
Found 'T' starting at 'Try not. Do, or do not. There is no try.'
Found 'T' starting at 'There is no try.'

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.24.5.2 The strchr function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.24.5.2 The strchr function (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.24.5.2 The strchr function (p: 367-368)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.21.5.2 The strchr function (p: 330)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.11.5.2 The strchr function

### See also

|  |  |
| --- | --- |
| memchr | searches an array for the first occurrence of a character   (function) |
| strrchr | finds the last occurrence of a character   (function) |
| strpbrk | finds the first location of any character in one string, in another string   (function) |
| C++ documentation for strchr | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/byte/strchr&oldid=172154>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 May 2024, at 10:06.