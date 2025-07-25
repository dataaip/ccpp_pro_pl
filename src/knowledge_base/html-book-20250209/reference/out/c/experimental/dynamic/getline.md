# getline, getwline, getdelim, getwdelim

From cppreference.com
< c‎ | experimental‎ | dynamic
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

 Technical Specifications

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Extensions for embedded processors") | | | | |
| Dynamic memory extensions | | | | |
| Floating-point extensions part 1: Binary floating-point | | | | |
| Floating-point extensions part 4: Supplementary functions | | | | |

 Dynamic memory extensions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| fmemopen") | | | | |
| open_memstreamopen_wmemstream") | | | | |
| asprintfaswprintfvasprintfvaswprintf | | | | |
| ****getlinegetwlinegetdelimgetwdelim**** | | | | |
| strdup | | | | |
| strndup | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdio.h>` |  |  |
| ssize_t getline(char \*\*lineptr, size_t \*n, FILE \*stream); | (1) | (dynamic memory TR) |
| ssize_t getwline(wchar_t \*\*lineptr, size_t \*n, FILE \*stream); | (2) | (dynamic memory TR) |
| ssize_t getdelim(char \*\* restrict lineptr, size_t \* restrict n,                   int delimiter, FILE \*stream); | (3) | (dynamic memory TR) |
| ssize_t getwdelim(wchar_t \*\* restrict lineptr, size_t \* restrict n,                   wint_t delimiter, FILE \* stream); | (4) | (dynamic memory TR) |
|  |  |  |

1) Behaves like getdelim(lineptr, n, '\n', stream)2) Behaves like getwdelim(lineptr, n, L'\n', stream)3) Reads from the stream `stream` as if by fgetc, until `delimiter` is encountered, storing the characters in the buffer of size `*n` pointed to by `*lineptr`, automatically increasing its size as if by realloc to fit the entire input, including the delimiter, and adding a null terminator. `*lineptr` may be null, in which case `*n` is ignored and `getline` allocates a new buffer as if by malloc.
The behavior is undefined if `delimiter` has a value that is outside the range of `unsigned char` or EOF.4) Same as (3), except the characters are read as if by fgetwc and that `delimiter` must be a valid `wchar_t` or WEOF.

If `*lineptr` is not null, the behavior is undefined if `*lineptr` is not a pointer that can be passed to free or if `*n` is less than the size of the allocated memory pointed to by `*lineptr`

As all functions from Dynamic Memory TR, `getline` is only guaranteed to be available if __STDC_ALLOC_LIB__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT2__ to the integer constant 1 before including `stdio.h`.

### Parameters

|  |  |  |
| --- | --- | --- |
| lineptr | - | pointer to a pointer to the initial buffer or to a null pointer |
| n | - | pointer to the size of the initial buffer |
| delimiter | - | the delimiter character |
| stream | - | valid input stream, opened by fopen |

### Return value

The number of characters stored in the buffer, including the delimiter, but excluding the null terminator.

On error, returns -1 and sets feof or ferror on `stream`.

### Notes

These functions are identical to their POSIX versions except that it is allowed, but not required to set errno on error.

### Example

Run this code

```
#ifdef __STDC_ALLOC_LIB__
#define __STDC_WANT_LIB_EXT2__ 1
#else
#define _POSIX_C_SOURCE 200809L
#endif
 
#include <stdio.h>
#include <stdlib.h>
void get_y_or_n(void)
{
    char *response = NULL;
    size_t len;
    printf("Continue? [y] n: ");
    if((getline(&response, &len, stdin) < 0) || (len && response[0] == 'n')) {
        free(response);
        exit(0);
    }
    free(response);
    return;
}
int main(void) 
{
    get_y_or_n();
}

```

Output:

```
Continue? [y] n:

```

### See also

|  |  |
| --- | --- |
| fgets | gets a character string from a file stream   (function) |
| getsgets_s(removed in C11)(C11) | reads a character string from stdin   (function) |
| fgetws(C95) | gets a wide string from a file stream   (function) |
| malloc | allocates memory   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/experimental/dynamic/getline&oldid=102274>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 May 2018, at 18:13.