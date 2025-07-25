# strcpy, strcpy_s

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****strcpystrcpy_s****(C11) | | | | | | strncpystrncpy_s(C11) | | | | | | strcatstrcat_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strncatstrncat_s(C11) | | | | | | strxfrm | | | | | | strdup(C23) | | | | | | strndup(C23) | | | | | |  | | | | | |
| String examination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlenstrnlen_s(C11) | | | | | | strcmp | | | | | | strncmp | | | | | | strcoll | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | strtokstrtok_s(C11) | | | | | |  | | | | | |
| Memory manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memsetmemset_explicitmemset_s(C23)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpymemcpy_s(C11) | | | | | | memmovememmove_s(C11) | | | | | | memccpy(C23) | | | | | |
| Miscellaneous | | | | |
| strerrorstrerror_sstrerrorlen_s(C11)(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<string.h>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| char \*strcpy( char \*dest, const char \*src ); |  | (until C99) |
| char \*strcpy( char \*restrict dest, const char \*restrict src ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
| errno_t strcpy_s( char \*restrict dest, rsize_t destsz, const char \*restrict src ); | (2) | (since C11) |
|  |  |  |

1) Copies the null-terminated byte string pointed to by `src`, including the null terminator, to the character array whose first element is pointed to by `dest`. The behavior is undefined if the `dest` array is not large enough. The behavior is undefined if the strings overlap. The behavior is undefined if either `dest` is not a pointer to a character array or `src` is not a pointer to a null-terminated byte string.2) Same as (1), except that it may clobber the rest of the destination array with unspecified values and that the following errors are detected at runtime and call the currently installed constraint handler function:

:   - `src` or `dest` is a null pointer
    - `destsz` is zero or greater than RSIZE_MAX
    - `destsz` is less or equal strnlen_s(src, destsz); in other words, truncation would occur
    - overlap would occur between the source and the destination strings

 The behavior is undefined if the size of the character array pointed to by `dest` <= strnlen_s(src, destsz) < `destsz`; in other words, an erroneous value of `destsz` does not expose the impending buffer overflow.

:   As with all bounds-checked functions, `strcpy_s` is only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including <string.h>.

### Parameters

|  |  |  |
| --- | --- | --- |
| dest | - | pointer to the character array to write to |
| src | - | pointer to the null-terminated byte string to copy from |
| destsz | - | maximum number of characters to write, typically the size of the destination buffer |

### Return value

1) returns a copy of `dest`2) returns zero on success, returns non-zero on error. Also, on error, writes zero to dest[0] (unless `dest` is a null pointer or `destsz` is zero or greater than RSIZE_MAX).

### Notes

`strcpy_s` is allowed to clobber the destination array from the last character written up to `destsz` in order to improve efficiency: it may copy in multibyte blocks and then check for null bytes.

The function `strcpy_s` is similar to the BSD function `strlcpy`, except that

- `strlcpy` truncates the source string to fit in the destination (which is a security risk)
- `strlcpy` does not perform all the runtime checks that `strcpy_s` does
- `strlcpy` does not make failures obvious by setting the destination to a null string or calling a handler if the call fails.

Although `strcpy_s` prohibits truncation due to potential security risks, it's possible to truncate a string using bounds-checked strncpy_s instead.

### Example

Run this code

```
#define __STDC_WANT_LIB_EXT1__ 1
#include <string.h>
#include <stdio.h>
#include <stdlib.h>
 
int main(void)
{
    const char *src = "Take the test.";
//  src[0] = 'M' ; // this would be undefined behavior
    char dst[strlen(src) + 1]; // +1 to accommodate for the null terminator
    strcpy(dst, src);
    dst[0] = 'M'; // OK
    printf("src = %s\ndst = %s\n", src, dst);
 
#ifdef __STDC_LIB_EXT1__
    set_constraint_handler_s(ignore_handler_s);
    int r = strcpy_s(dst, sizeof dst, src);
    printf("dst = \"%s\", r = %d\n", dst, r);
    r = strcpy_s(dst, sizeof dst, "Take even more tests.");
    printf("dst = \"%s\", r = %d\n", dst, r);
#endif
}

```

Possible output:

```
src = Take the test.
dst = Make the test.
dst = "Take the test.", r = 0
dst = "", r = 22

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.24.2.3 The strcpy function (p: 264-265)

:   - K.3.7.1.3 The strcpy_s function (p: 447)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.24.2.3 The strcpy function (p: 363)

:   - K.3.7.1.3 The strcpy_s function (p: 615-616)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.21.2.3 The strcpy function (p: 326)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.11.2.3 The strcpy function

### See also

|  |  |
| --- | --- |
| strncpystrncpy_s(C11) | copies a certain amount of characters from one string to another   (function) |
| memcpymemcpy_s(C11) | copies one buffer to another   (function) |
| wcscpywcscpy_s(C95)(C11) | copies one wide string to another   (function) |
| strdup(dynamic memory TR) | allocate a copy of a string   (function) |
| C++ documentation for strcpy | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/byte/strcpy&oldid=155879>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 July 2023, at 19:44.