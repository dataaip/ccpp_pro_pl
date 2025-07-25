# tmpfile, tmpfile_s

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | File access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fopenfopen_s(C11) | | | | | | freopenfreopen_s(C11) | | | | | | fwide(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setbuf | | | | | | setvbuf | | | | | | fclose | | | | | | fflush | | | | | |  | | | | | | | Unformatted input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetc | | | | | | fgets | | | | | | fputc | | | | | | fputs | | | | | | getchar | | | | | | getsgets_s(until C11)(C11) | | | | | | putchar | | | | | | puts | | | | | | ungetc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetwcgetwc(C95)(C95) | | | | | | fgetws(C95) | | | | | | fputwcputwc(C95)(C95) | | | | | | fputws(C95) | | | | | | getwchar(C95) | | | | | | putwchar(C95) | | | | | | ungetwc(C95) | | | | | |  | | | | | | | Formatted input | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scanffscanfsscanfscanf_sfscanf_ssscanf_s(C11)(C11)(C11) | | | | | | wscanffwscanfswscanfwscanf_sfwscanf_sswscanf_s(C95)(C95)(C95)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vscanfvfscanfvsscanfvscanf_svfscanf_svsscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | vwscanfvfwscanfvswscanfvwscanf_svfwscanf_svswscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Direct input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fread | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwrite | | | | | | | Formatted output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | printffprintfsprintfsnprintfprintf_sfprintf_ssprintf_ssnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | wprintffwprintfswprintfwprintf_sfwprintf_sswprintf_ssnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vprintfvfprintfvsprintfvsnprintfvprintf_svfprintf_svsprintf_svsnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | vwprintfvfwprintfvswprintfvwprintf_svfwprintf_svswprintf_svsnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | | File positioning | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ftell | | | | | | fgetpos | | | | | | fseek | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fsetpos | | | | | | rewind | | | | | |  | | | | | | | Error handling | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clearerr | | | | | | feof | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ferror | | | | | | perror | | | | | | | Operations on files | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove | | | | | | ****tmpfiletmpfile_s****(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rename | | | | | | tmpnamtmpnam_s(C11) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdio.h>` |  |  |
| FILE\* tmpfile( void ); | (1) |  |
| errno_t tmpfile_s( FILE\* restrict\* restrict streamptr ); | (2) | (since C11) |
|  |  |  |

1) Creates and opens a temporary file. The file is opened as binary file for update (as if by fopen with "wb+" mode). The filename of the file is guaranteed to be unique within the filesystem. At least TMP_MAX files may be opened during the lifetime of a program (this limit may be shared with tmpnam and may be further limited by FOPEN_MAX).2) Same as (1), except that at least TMP_MAX_S files may be opened (the limit may be shared with tmpnam_s), and if streamptr is a null pointer, the currently installed constraint handler function is called.

:   As with all bounds-checked functions, `tmpfile_s` is only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including <stdio.h>.

The temporary file created by this function is closed and deleted when the program exits normally. Whether it's deleted on abnormal termination is implementation-defined.

### Parameters

1) (none)2) pointer to a pointer that will be updated by this function call

### Return value

1) Pointer to the file stream associated with the file or null pointer if an error has occurred.2) Zero if the file was created and open successfully, non-zero if the file was not created or open or if streamptr was a null pointer. In addition, pointer to the associated file stream is stored in \*streamptr on success, and a null pointer value is stored in \*streamptr on error.

### Notes

On some implementations (e.g. older Linux), this function actually creates, opens, and immediately deletes the file from the file system: as long as an open file descriptor to a deleted file is held by a program, the file exists, but since it was deleted, its name does not appear in any directory, so that no other process can open it. Once the file descriptor is closed, or once the program terminates (normally or abnormally), the space occupied by the file is reclaimed by the filesystem. Newer Linux (since 3.11 or later, depending on filesystem) creates such invisible temporary files in one step, via special flag in the `open()` syscall.

On some implementations (e.g. Windows), elevated privileges are required as the function may create the temporary file in a system directory.

### Example

Run this code

```
#define _POSIX_C_SOURCE 200112L
#include <stdio.h>
#include <unistd.h>
 
int main(void)
{
    printf("TMP_MAX = %d, FOPEN_MAX = %d\n", TMP_MAX, FOPEN_MAX);
    FILE* tmpf = tmpfile();
    fputs("Hello, world", tmpf);
    rewind(tmpf);
    char buf[6];
    fgets(buf, sizeof buf, tmpf);
    printf("got back from the file: '%s'\n", buf);
 
    // Linux-specific method to display the tmpfile name
    char fname[FILENAME_MAX], link[FILENAME_MAX] = {0};
    sprintf(fname, "/proc/self/fd/%d", fileno(tmpf));
    if (readlink(fname, link, sizeof link - 1) > 0)
        printf("File name: %s\n", link);
}

```

Possible output:

```
TMP_MAX = 238328, FOPEN_MAX = 16
got back from the file: 'Hello'
File name: /tmp/tmpfjptPe5 (deleted)

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.21.4.3 The tmpfile function (p: TBD)

:   - K.3.5.1.1 The tmpfile_s function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.21.4.3 The tmpfile function (p: 222)

:   - K.3.5.1.1 The tmpfile_s function (p: 427)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.21.4.3 The tmpfile function (p: 303)

:   - K.3.5.1.1 The tmpfile_s function (p: 586-587)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.19.4.3 The tmpfile function (p: 269)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.9.4.3 The tmpfile function

### See also

|  |  |
| --- | --- |
| tmpnamtmpnam_s(C11) | returns a unique filename   (function) |
| C++ documentation for tmpfile | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/io/tmpfile&oldid=158992>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 September 2023, at 11:29.