# File input/output

From cppreference.com
< c
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
| ****Input/output support**** | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 ****File input/output****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Types and objects | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stdinstdoutstderr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FILE | | | | | | fpos_t | | | | | |  | | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | File access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fopenfopen_s(C11) | | | | | | freopenfreopen_s(C11) | | | | | | fwide(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setbuf | | | | | | setvbuf | | | | | | fclose | | | | | | fflush | | | | | |  | | | | | | | Unformatted input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetc | | | | | | fgets | | | | | | fputc | | | | | | fputs | | | | | | getchar | | | | | | getsgets_s(until C11)(C11) | | | | | | putchar | | | | | | puts | | | | | | ungetc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetwcgetwc(C95)(C95) | | | | | | fgetws(C95) | | | | | | fputwcputwc(C95)(C95) | | | | | | fputws(C95) | | | | | | getwchar(C95) | | | | | | putwchar(C95) | | | | | | ungetwc(C95) | | | | | |  | | | | | | | Formatted input | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scanffscanfsscanfscanf_sfscanf_ssscanf_s(C11)(C11)(C11) | | | | | | wscanffwscanfswscanfwscanf_sfwscanf_sswscanf_s(C95)(C95)(C95)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vscanfvfscanfvsscanfvscanf_svfscanf_svsscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | vwscanfvfwscanfvswscanfvwscanf_svfwscanf_svswscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Direct input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fread | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwrite | | | | | | | Formatted output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | printffprintfsprintfsnprintfprintf_sfprintf_ssprintf_ssnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | wprintffwprintfswprintfwprintf_sfwprintf_sswprintf_ssnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vprintfvfprintfvsprintfvsnprintfvprintf_svfprintf_svsprintf_svsnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | vwprintfvfwprintfvswprintfvwprintf_svfwprintf_svswprintf_svsnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | | File positioning | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ftell | | | | | | fgetpos | | | | | | fseek | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fsetpos | | | | | | rewind | | | | | |  | | | | | | | Error handling | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clearerr | | | | | | feof | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ferror | | | | | | perror | | | | | | | Operations on files | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove | | | | | | tmpfiletmpfile_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rename | | | | | | tmpnamtmpnam_s(C11) | | | | | | |

The ****<stdio.h>**** header provides generic file operation support and supplies functions with narrow character input/output capabilities.

The <wchar.h> header supplies functions with wide character input/output capabilities.

I/O streams are denoted by objects of type FILE that can only be accessed and manipulated through pointers of type FILE\*. Each stream is associated with an external physical device (file, standard input stream, printer, serial port, etc).

### Types

|  |  |
| --- | --- |
| Defined in header `<stdio.h>` | |
| FILE | object type, capable of holding all information needed to control a C I/O stream   (typedef) |
| fpos_t | non-array complete object type, capable of uniquely specifying a position and multibyte parser state in a file   (typedef) |

### Predefined standard streams

|  |  |
| --- | --- |
| Defined in header `<stdio.h>` | |
| stdinstdoutstderr | expression of type FILE\* associated with the input stream expression of type FILE\* associated with the output stream expression of type FILE\* associated with the error output stream   (macro constant) |

### Functions

|  |  |
| --- | --- |
| File access | |
| Defined in header `<stdio.h>` | |
| fopenfopen_s(C11) | opens a file   (function) |
| freopenfreopen_s(C11) | open an existing stream with a different name   (function) |
| fclose | closes a file   (function) |
| fflush | synchronizes an output stream with the actual file   (function) |
| setbuf | sets the buffer for a file stream   (function) |
| setvbuf | sets the buffer and its size for a file stream   (function) |
| Defined in header `<wchar.h>` | |
| fwide(C95) | switches a file stream between wide character I/O and narrow character I/O   (function) |
| Direct input/output | |
| Defined in header `<stdio.h>` | |
| fread | reads from a file   (function) |
| fwrite | writes to a file   (function) |
| Unformatted input/output | |
| Narrow character | |
| Defined in header `<stdio.h>` | |
| fgetcgetc | gets a character from a file stream   (function) |
| fgets | gets a character string from a file stream   (function) |
| fputcputc | writes a character to a file stream   (function) |
| fputs | writes a character string to a file stream   (function) |
| getchar | reads a character from stdin   (function) |
| getsgets_s(removed in C11)(C11) | reads a character string from stdin   (function) |
| putchar | writes a character to stdout   (function) |
| puts | writes a character string to stdout   (function) |
| ungetc | puts a character back into a file stream   (function) |
| Wide character | |
| Defined in header `<wchar.h>` | |
| fgetwcgetwc(C95) | gets a wide character from a file stream   (function) |
| fgetws(C95) | gets a wide string from a file stream   (function) |
| fputwcputwc(C95) | writes a wide character to a file stream   (function) |
| fputws(C95) | writes a wide string to a file stream   (function) |
| getwchar(C95) | reads a wide character from stdin   (function) |
| putwchar(C95) | writes a wide character to stdout   (function) |
| ungetwc(C95) | puts a wide character back into a file stream   (function) |
| Formatted input/output | |
| Narrow character | |
| Defined in header `<stdio.h>` | |
| scanffscanfsscanfscanf_sfscanf_ssscanf_s(C11)(C11)(C11) | reads formatted input from stdin, a file stream or a buffer   (function) |
| vscanfvfscanfvsscanfvscanf_svfscanf_svsscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | reads formatted input from stdin, a file stream or a buffer  using variable argument list   (function) |
| printffprintfsprintfsnprintfprintf_sfprintf_ssprintf_ssnprintf_s(C99)(C11)(C11)(C11)(C11) | prints formatted output to stdout, a file stream or a buffer   (function) |
| vprintfvfprintfvsprintfvsnprintfvprintf_svfprintf_svsprintf_svsnprintf_s(C99)(C11)(C11)(C11)(C11) | prints formatted output to stdout, a file stream or a buffer  using variable argument list   (function) |
| Wide character | |
| Defined in header `<wchar.h>` | |
| wscanffwscanfswscanfwscanf_sfwscanf_sswscanf_s(C95)(C95)(C95)(C11)(C11)(C11) | reads formatted wide character input from stdin, a file stream or a buffer   (function) |
| vwscanfvfwscanfvswscanfvwscanf_svfwscanf_svswscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | reads formatted wide character input from stdin, a file stream  or a buffer using variable argument list   (function) |
| wprintffwprintfswprintfwprintf_sfwprintf_sswprintf_ssnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | prints formatted wide character output to stdout, a file stream or a buffer   (function) |
| vwprintfvfwprintfvswprintfvwprintf_svfwprintf_svswprintf_svsnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | prints formatted wide character output to stdout, a file stream  or a buffer using variable argument list   (function) |
| File positioning | |
| Defined in header `<stdio.h>` | |
| ftell | returns the current file position indicator   (function) |
| fgetpos | gets the file position indicator   (function) |
| fseek | moves the file position indicator to a specific location in a file   (function) |
| fsetpos | moves the file position indicator to a specific location in a file   (function) |
| rewind | moves the file position indicator to the beginning in a file   (function) |
| Error handling | |
| Defined in header `<stdio.h>` | |
| clearerr | clears errors   (function) |
| feof | checks for the end-of-file   (function) |
| ferror | checks for a file error   (function) |
| perror | displays a character string corresponding of the current error to stderr   (function) |
| Operations on files | |
| Defined in header `<stdio.h>` | |
| remove | erases a file   (function) |
| rename | renames a file   (function) |
| tmpfiletmpfile_s(C11) | returns a pointer to a temporary file   (function) |
| tmpnamtmpnam_s(C11) | returns a unique filename   (function) |

### Macro constants

|  |  |
| --- | --- |
| Defined in header `<stdio.h>` | |
| EOF | integer constant expression of type int and negative value   (macro constant) |
| FOPEN_MAX | maximum number of files that can be open simultaneously   (macro constant) |
| FILENAME_MAX | size needed for an array of char to hold the longest supported file name   (macro constant) |
| BUFSIZ | size of the buffer used by setbuf   (macro constant) |
| _IOFBF_IOLBF_IONBF | argument to setvbuf indicating fully buffered I/O argument to setvbuf indicating line buffered I/O argument to setvbuf indicating unbuffered I/O   (macro constant) |
| SEEK_SETSEEK_CURSEEK_END | argument to fseek indicating seeking from beginning of the file argument to fseek indicating seeking from the current file position argument to fseek indicating seeking from end of the file   (macro constant) |
| TMP_MAXTMP_MAX_S(C11) | maximum number of unique filenames that can be generated by tmpnam maximum number of unique filenames that can be generated by tmpnam_s   (macro constant) |
| L_tmpnamL_tmpnam_s(C11) | size needed for an array of char to hold the result of tmpnam size needed for an array of char to hold the result of tmpnam_s   (macro constant) |

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.21 Input/output <stdio.h> (p: TBD)

:   - 7.29 Extended multibyte and wide character utilities <wchar.h> (p: TBD)

:   - 7.31.11 Input/output <stdio.h> (p: TBD)

:   - 7.31.16 Extended multibyte and wide character utilities <wchar.h> (p: TBD)

:   - K.3.5 Input/output <stdio.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.21 Input/output <stdio.h> (p: TBD)

:   - 7.29 Extended multibyte and wide character utilities <wchar.h> (p: TBD)

:   - 7.31.11 Input/output <stdio.h> (p: TBD)

:   - 7.31.16 Extended multibyte and wide character utilities <wchar.h> (p: TBD)

:   - K.3.5 Input/output <stdio.h> (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.21 Input/output <stdio.h> (p: 296-339)

:   - 7.29 Extended multibyte and wide character utilities <wchar.h> (p: 402-446)

:   - 7.31.11 Input/output <stdio.h> (p: 456)

:   - 7.31.16 Extended multibyte and wide character utilities <wchar.h> (p: 456)

:   - K.3.5 Input/output <stdio.h> (p: 586-603)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.19 Input/output <stdio.h> (p: 262-305)

:   - 7.24 Extended multibyte and wide character utilities <wchar.h> (p: 348-392)

:   - 7.26.9 Input/output <stdio.h> (p: 402)

:   - 7.26.12 Extended multibyte and wide character utilities <wchar.h> (p: 402)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.9 INPUT/OUTPUT <stdio.h>

:   - 4.13.6 Input/output <stdio.h>

### See also

|  |  |
| --- | --- |
| C++ documentation for C-style file input/output | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/io&oldid=180208>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 February 2025, at 16:26.