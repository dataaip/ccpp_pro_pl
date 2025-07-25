# std::setvbuf

From cppreference.com
< cpp‎ | io‎ | c
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
| C-style I/O | | | | |
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

C-style I/O

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Types and objects | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | FILE | | | | | | fpos_t | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stdinstdoutstderr | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | File access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fopen | | | | | | freopen | | | | | | fclose | | | | | | fflush | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwide | | | | | | setbuf | | | | | | ****setvbuf**** | | | | | |  | | | | | | | Direct input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fread | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwrite | | | | | | | Unformatted input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetcgetc | | | | | | fgets | | | | | | fputcputc | | | | | | fputs | | | | | | getchar | | | | | | gets(until C++14) | | | | | | putchar | | | | | | puts | | | | | | ungetc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetwcgetwc | | | | | | fgetws | | | | | | fputwcputwc | | | | | | fputws | | | | | | getwchar | | | | | | putwchar | | | | | | ungetwc | | | | | |  | | | | | |  | | | | | | | Formatted input | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scanffscanfsscanf | | | | | | vscanfvfscanfvsscanf(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wscanffwscanfswscanf | | | | | | vwscanfvfwscanfvswscanf(C++11)(C++11)(C++11) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Formatted output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | printffprintfsprintfsnprintf(C++11) | | | | | | vprintfvfprintfvsprintfvsnprintf(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wprintffwprintfswprintf | | | | | | vwprintfvfwprintfvswprintf | | | | | | | File positioning | | | | | | ftell | | | | | | fgetpos | | | | | | fseek | | | | | | fsetpos | | | | | | rewind | | | | | | Error handling | | | | | | clearerr | | | | | | feof | | | | | | ferror | | | | | | perror | | | | | | Operations on files | | | | | | remove | | | | | | rename | | | | | | tmpfile | | | | | | tmpnam | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstdio>` |  |  |
| int setvbuf( std::FILE\* stream, char\* buffer, int mode, std::size_t size ); |  |  |
|  |  |  |

Changes the buffering mode of the given file stream stream as indicated by the argument mode. In addition,

- If buffer is a null pointer, resizes the internal buffer to size.
- If buffer is not a null pointer, instructs the stream to use the user-provided buffer of size size beginning at buffer. The stream must be closed (with std::fclose) before the lifetime of the array pointed to by buffer ends. The contents of the array after a successful call to ****std::setvbuf**** are indeterminate and any attempt to use it is undefined behavior.

### Parameters

|  |  |  |
| --- | --- | --- |
| stream | - | the file stream to set the buffer to |
| buffer | - | pointer to a buffer for the stream to use or null pointer to change size and mode only |
| mode | - | buffering mode to use. It can be one of the following values:  |  |  | | --- | --- | | _IOFBF | full buffering | | _IOLBF | line buffering | | _IONBF | no buffering | |
| size | - | size of the buffer |

### Return value

​0​ on success or nonzero on failure.

### Notes

This function may only be used after stream has been associated with an open file, but before any other operation (other than a failed call to std::setbuf/`std::setvbuf`).

Not all size bytes will necessarily be used for buffering: the actual buffer size is usually rounded down to a multiple of 2, a multiple of page size, etc.

On many implementations, line buffering is only available for terminal input streams.

A common error is setting the buffer of `stdin` or `stdout` to an array whose lifetime ends before the program terminates:

```
int main()
{
    char buf[BUFSIZ];
    std::setbuf(stdin, buf);
} // lifetime of buf ends, undefined behavior

```

The default buffer size BUFSIZ is expected to be the most efficient buffer size for file I/O on the implementation, but POSIX `fstat` often provides a better estimate.

### Example

One use case for changing buffer size is when a better size is known.

Run this code

```
#include <cstdio>
#include <cstdlib>
#include <iostream>
#include <sys/stat.h>
 
int main()
{
    std::FILE* fp = std::fopen("/tmp/test.txt", "w+");
    if (!fp)
    {
        std::perror("fopen");
        return EXIT_FAILURE;
    }
 
    struct stat stats;
    if (fstat(fileno(fp), &stats) == -1) // POSIX only
    {
        std::perror("fstat");
        return EXIT_FAILURE;
    }
 
    std::cout << "BUFSIZ is " << BUFSIZ << ", but optimal block size is "
              << stats.st_blksize << '\n';
    if (std::setvbuf(fp, nullptr, _IOFBF, stats.st_blksize) != 0)
    {
        std::perror("setvbuf failed"); // POSIX version sets errno
        return EXIT_FAILURE;
    }
 
    // Read entire file: use truss/strace to observe the read(2) syscalls used
    for (int ch; (ch = std::fgetc(fp)) != EOF;)
    {}
 
    std::fclose(fp);
    return EXIT_SUCCESS;
}

```

Possible output:

```
BUFSIZ is 8192, but optimal block size is 65536

```

### See also

|  |  |
| --- | --- |
| setbuf | sets the buffer for a file stream   (function) |
| setbuf[virtual] | provides user-supplied buffer or turns this filebuf unbuffered   (virtual protected member function of `std::basic_filebuf<CharT,Traits>`) |
| C documentation for setvbuf | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/c/setvbuf&oldid=158998>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 September 2023, at 11:54.