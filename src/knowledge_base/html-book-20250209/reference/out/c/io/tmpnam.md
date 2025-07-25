# tmpnam, tmpnam_s

From cppreference.com
< c‎ | io
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

 File input/output

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Types and objects | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stdinstdoutstderr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FILE | | | | | | fpos_t | | | | | |  | | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | File access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fopenfopen_s(C11) | | | | | | freopenfreopen_s(C11) | | | | | | fwide(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setbuf | | | | | | setvbuf | | | | | | fclose | | | | | | fflush | | | | | |  | | | | | | | Unformatted input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetc | | | | | | fgets | | | | | | fputc | | | | | | fputs | | | | | | getchar | | | | | | getsgets_s(until C11)(C11) | | | | | | putchar | | | | | | puts | | | | | | ungetc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetwcgetwc(C95)(C95) | | | | | | fgetws(C95) | | | | | | fputwcputwc(C95)(C95) | | | | | | fputws(C95) | | | | | | getwchar(C95) | | | | | | putwchar(C95) | | | | | | ungetwc(C95) | | | | | |  | | | | | | | Formatted input | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scanffscanfsscanfscanf_sfscanf_ssscanf_s(C11)(C11)(C11) | | | | | | wscanffwscanfswscanfwscanf_sfwscanf_sswscanf_s(C95)(C95)(C95)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vscanfvfscanfvsscanfvscanf_svfscanf_svsscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | vwscanfvfwscanfvswscanfvwscanf_svfwscanf_svswscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Direct input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fread | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwrite | | | | | | | Formatted output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | printffprintfsprintfsnprintfprintf_sfprintf_ssprintf_ssnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | wprintffwprintfswprintfwprintf_sfwprintf_sswprintf_ssnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vprintfvfprintfvsprintfvsnprintfvprintf_svfprintf_svsprintf_svsnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | vwprintfvfwprintfvswprintfvwprintf_svfwprintf_svswprintf_svsnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | | File positioning | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ftell | | | | | | fgetpos | | | | | | fseek | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fsetpos | | | | | | rewind | | | | | |  | | | | | | | Error handling | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clearerr | | | | | | feof | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ferror | | | | | | perror | | | | | | | Operations on files | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove | | | | | | tmpfiletmpfile_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rename | | | | | | ****tmpnamtmpnam_s****(C11) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdio.h>` |  |  |
| char \*tmpnam( char \*filename ); | (1) |  |
| errno_t tmpnam_s(char \*filename_s, rsize_t maxsize); | (2) | (since C11) |
| #define TMP_MAX        /\*unspecified\*/ |  |  |
| #define TMP_MAX_S      /\*unspecified\*/ |  | (since C11) |
| #define L_tmpnam       /\*unspecified\*/ |  |  |
| #define L_tmpnam_s     /\*unspecified\*/ |  | (since C11) |
|  |  |  |

1) Creates a unique valid file name (no longer than L_tmpnam in length) and stores it in character string pointed to by filename. The function is capable of generating up to TMP_MAX of unique filenames, but some or all of them may be in use in the filesystem and thus not suitable return values.2) Same as (1), except that up to TMP_MAX_S names may be generated, no longer than L_tmpnam_s in length, and the following errors are detected at runtime and call the currently installed constraint handler function:

:   - filename_s is a null pointer
    - maxsize is greater than RSIZE_MAX
    - maxsize is less than the generated file name string
:   As with all bounds-checked functions, `tmpnam_s` is only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including <stdio.h>.

tmpnam and tmpnam_s modify static state (which may be shared between these functions) and are not required to be thread-safe.

### Parameters

|  |  |  |
| --- | --- | --- |
| filename | - | pointer to the character array capable of holding at least L_tmpnam bytes, to be used as a result buffer. If null pointer is passed, a pointer to an internal static buffer is returned. |
| filename_s | - | pointer to the character array capable of holding at least L_tmpnam_s bytes, to be used as a result buffer. |
| maxsize | - | maximum number of characters the function is allowed to write (typically the size of the `filename_s` array). |

### Return value

1) filename if filename was not a null pointer. Otherwise a pointer to an internal static buffer is returned. If no suitable filename can be generated, null pointer is returned.2) Returns zero and writes the file name to filename_s on success. On error, returns non-zero and writes the null character to filename_s[0] (only if filename_s is not null and maxsize is not zero and is not greater than RSIZE_MAX).

### Notes

Although the names generated by `tmpnam` are difficult to guess, it is possible that a file with that name is created by another process between the moment `tmpnam` returns and the moment this program attempts to use the returned name to create a file. The standard function tmpfile and the POSIX function `mkstemp` do not have this problem (creating a unique directory using only the standard C library still requires the use of `tmpnam`).

POSIX systems additionally define the similarly named function `tempnam`, which offers the choice of a directory (which defaults to the optionally defined macro `P_tmpdir`).

### Example

Run this code

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
 
int main(void)
{
    // Note, the compiler/linker may issue a security warning, e.g. GCC:
    // "warning: the use of `tmpnam' is dangerous, better use `mkstemp'"
    char* name1 = tmpnam(NULL);
    printf("temporary file name: %s\n", name1);
 
    char name2[L_tmpnam];
    if (tmpnam(name2))
        printf("temporary file name: %s\n", name2);
 
    // POSIX offers mkstemp. The following declaration might be
    // necessary as mkstemp is absent in the standard C <stdlib.h>.
    int mkstemp(char*);
 
    char name3[] = "/tmp/fileXXXXXX"; // at least six 'X' required ^_^
    int file_descriptor = mkstemp(name3);
    if (file_descriptor != -1)
        printf("temporary file name: %s\n", name3);
    else
        perror("mkstemp");
}

```

Possible output:

```
temporary file name: /tmp/file90dLlR
temporary file name: /tmp/fileY9LWAg
temporary file name: /tmp/filexgv8PF

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.21.4.4 The tmpnam function (p: TBD)

:   - K.3.5.1.2 The tmpnam_s function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.21.4.4 The tmpnam function (p: 222)

:   - K.3.5.1.2 The tmpnam_s function (p: 427-428)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.21.4.4 The tmpnam function (p: 303-304)

:   - K.3.5.1.2 The tmpnam_s function (p: 587-588)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.19.4.4 The tmpnam function (p: 269-270)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.9.4.4 The tmpnam function

### See also

|  |  |
| --- | --- |
| tmpfiletmpfile_s(C11) | returns a pointer to a temporary file   (function) |
| C++ documentation for tmpnam | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/io/tmpnam&oldid=150073>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 April 2023, at 07:47.