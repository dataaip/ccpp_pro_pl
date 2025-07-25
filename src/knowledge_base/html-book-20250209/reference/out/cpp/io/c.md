# C-style file input/output

From cppreference.com
< cpp‎ | io
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

Input/output library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| I/O manipulators | | | | |
| Print functions (C++23) | | | | |
| ****C-style I/O**** | | | | |
| Buffers | | | | |
| basic_streambuf | | | | |
| basic_filebuf | | | | |
| basic_stringbuf | | | | |
| basic_spanbuf(C++23) | | | | |
| strstreambuf(C++98/26\*) | | | | |
| basic_syncbuf(C++20) | | | | |
| Streams | | | | |
| Abstractions | | | | |
| ios_base | | | | |
| basic_ios | | | | |
| basic_istream | | | | |
| basic_ostream | | | | |
| basic_iostream | | | | |
| File I/O | | | | |
| basic_ifstream | | | | |
| basic_ofstream | | | | |
| basic_fstream | | | | |
| String I/O | | | | |
| basic_istringstream | | | | |
| basic_ostringstream | | | | |
| basic_stringstream | | | | |
| Array I/O | | | | |
| basic_ispanstream(C++23) | | | | |
| basic_ospanstream(C++23) | | | | |
| basic_spanstream(C++23) | | | | |
| istrstream(C++98/26\*) | | | | |
| ostrstream(C++98/26\*) | | | | |
| strstream(C++98/26\*) | | | | |
| Synchronized Output | | | | |
| basic_osyncstream(C++20) | | | | |
| Types | | | | |
| streamoff | | | | |
| streamsize | | | | |
| fpos | | | | |
| Error category interface | | | | |
| iostream_category(C++11) | | | | |
| io_errc(C++11) | | | | |

****C-style I/O****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Types and objects | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | FILE | | | | | | fpos_t | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stdinstdoutstderr | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | File access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fopen | | | | | | freopen | | | | | | fclose | | | | | | fflush | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwide | | | | | | setbuf | | | | | | setvbuf | | | | | |  | | | | | | | Direct input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fread | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwrite | | | | | | | Unformatted input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetcgetc | | | | | | fgets | | | | | | fputcputc | | | | | | fputs | | | | | | getchar | | | | | | gets(until C++14) | | | | | | putchar | | | | | | puts | | | | | | ungetc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetwcgetwc | | | | | | fgetws | | | | | | fputwcputwc | | | | | | fputws | | | | | | getwchar | | | | | | putwchar | | | | | | ungetwc | | | | | |  | | | | | |  | | | | | | | Formatted input | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scanffscanfsscanf | | | | | | vscanfvfscanfvsscanf(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wscanffwscanfswscanf | | | | | | vwscanfvfwscanfvswscanf(C++11)(C++11)(C++11) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Formatted output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | printffprintfsprintfsnprintf(C++11) | | | | | | vprintfvfprintfvsprintfvsnprintf(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wprintffwprintfswprintf | | | | | | vwprintfvfwprintfvswprintf | | | | | | | File positioning | | | | | | ftell | | | | | | fgetpos | | | | | | fseek | | | | | | fsetpos | | | | | | rewind | | | | | | Error handling | | | | | | clearerr | | | | | | feof | | | | | | ferror | | | | | | perror | | | | | | Operations on files | | | | | | remove | | | | | | rename | | | | | | tmpfile | | | | | | tmpnam | | | | | |

The C I/O subset of the C++ standard library implements C-style stream input/output operations. The <cstdio> header provides generic file operation support and supplies functions with narrow and multibyte character input/output capabilities, and the <cwchar> header provides functions with wide character input/output capabilities.

C streams are denoted by objects of type std::FILE that can only be accessed and manipulated through pointers of type std::FILE\*. Each C stream is associated with an external physical device (file, standard input stream, printer, serial port, etc).

### Types

|  |  |
| --- | --- |
| Defined in header `<cstdio>` | |
| FILE | object type, capable of holding all information needed to control a C I/O stream   (typedef) |
| fpos_t | complete non-array object type, capable of uniquely specifying a position in a file, including its multibyte parse state   (typedef) |

### Predefined standard streams

|  |  |
| --- | --- |
| Defined in header `<cstdio>` | |
| stdinstdoutstderr | expression of type FILE\* associated with the input stream expression of type FILE\* associated with the output stream expression of type FILE\* associated with the error output stream   (macro constant) |

### Functions

|  |  |
| --- | --- |
| Defined in header `<cstdio>` | |
| File access | |
| fopen | opens a file   (function) |
| freopen | open an existing stream with a different name   (function) |
| fclose | closes a file   (function) |
| fflush | synchronizes an output stream with the actual file   (function) |
| fwide | switches a file stream between wide character I/O and narrow character I/O   (function) |
| setbuf | sets the buffer for a file stream   (function) |
| setvbuf | sets the buffer and its size for a file stream   (function) |
| Direct input/output | |
| fread | reads from a file   (function) |
| fwrite | writes to a file   (function) |
| Unformatted input/output | |
| Byte/multibyte character | |
| fgetcgetc | gets a character from a file stream   (function) |
| fgets | gets a character string from a file stream   (function) |
| fputcputc | writes a character to a file stream   (function) |
| fputs | writes a character string to a file stream   (function) |
| getchar | reads a character from stdin   (function) |
| gets(deprecated in C++11)(removed in C++14) | reads a character string from stdin   (function) |
| putchar | writes a character to stdout   (function) |
| puts | writes a character string to stdout   (function) |
| ungetc | puts a character back into a file stream   (function) |
| Wide character | |
| fgetwcgetwc | gets a wide character from a file stream   (function) |
| fgetws | gets a wide string from a file stream   (function) |
| fputwcputwc | writes a wide character to a file stream   (function) |
| fputws | writes a wide string to a file stream   (function) |
| getwchar | reads a wide character from stdin   (function) |
| putwchar | writes a wide character to stdout   (function) |
| ungetwc | puts a wide character back into a file stream   (function) |
| Formatted input/output | |
| Byte/multibyte character | |
| scanffscanfsscanf | reads formatted input from stdin, a file stream or a buffer   (function) |
| vscanfvfscanfvsscanf(C++11)(C++11)(C++11) | reads formatted input from stdin, a file stream or a buffer using variable argument list   (function) |
| printffprintfsprintfsnprintf(C++11) | prints formatted output to stdout, a file stream or a buffer   (function) |
| vprintfvfprintfvsprintfvsnprintf(C++11) | prints formatted output to stdout, a file stream or a buffer using variable argument list   (function) |
| Wide character | |
| wscanffwscanfswscanf | reads formatted wide character input from stdin, a file stream or a buffer   (function) |
| vwscanfvfwscanfvswscanf(C++11)(C++11)(C++11) | reads formatted wide character input from stdin, a file stream or a buffer using variable argument list   (function) |
| wprintffwprintfswprintf | prints formatted wide character output to stdout, a file stream or a buffer   (function) |
| vwprintfvfwprintfvswprintf | prints formatted wide character output to stdout, a file stream or a buffer using variable argument list   (function) |
| File positioning | |
| ftell | returns the current file position indicator   (function) |
| fgetpos | gets the file position indicator   (function) |
| fseek | moves the file position indicator to a specific location in a file   (function) |
| fsetpos | moves the file position indicator to a specific location in a file   (function) |
| rewind | moves the file position indicator to the beginning in a file   (function) |
| Error handling | |
| clearerr | clears errors   (function) |
| feof | checks for the end-of-file   (function) |
| ferror | checks for a file error   (function) |
| perror | displays a character string corresponding of the current error to stderr   (function) |
| Operations on files | |
| remove | erases a file   (function) |
| rename | renames a file   (function) |
| tmpfile | creates and opens a temporary, auto-removing file   (function) |
| tmpnam | returns a unique filename   (function) |

### Macro constants

|  |  |
| --- | --- |
| Defined in header `<cstdio>` | |
| EOF | integer constant expression of type int and negative value   (macro constant) |
| FOPEN_MAX | number of files that can be open simultaneously   (macro constant) |
| FILENAME_MAX | size needed for an array of char to hold the longest supported file name   (macro constant) |
| BUFSIZ | size of the buffer used by std::setbuf   (macro constant) |
| _IOFBF_IOLBF_IONBF | argument to std::setbuf indicating fully buffered I/O argument to std::setbuf indicating line buffered I/O argument to std::setbuf indicating unbuffered I/O   (macro constant) |
| SEEK_SETSEEK_CURSEEK_END | argument to std::fseek indicating seeking from beginning of the file argument to std::fseek indicating seeking from the current file position argument to std::fseek indicating seeking from end of the file   (macro constant) |
| TMP_MAX | maximum number of unique filenames that is guaranteed to be generatable by std::tmpnam   (macro constant) |
| L_tmpnam | size needed for an array of char to hold the result of std::tmpnam   (macro constant) |

### See also

|  |  |
| --- | --- |
| C documentation for File input/output | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/c&oldid=165230>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 December 2023, at 07:51.