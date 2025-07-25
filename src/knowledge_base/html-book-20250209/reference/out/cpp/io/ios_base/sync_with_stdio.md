# std::ios_base::sync_with_stdio

From cppreference.com
< cpp‎ | io‎ | ios base
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

std::ios_base

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ios_base::ios_base | | | | |
| ios_base::~ios_base | | | | |
| ios_base::operator= | | | | |
| Formatting | | | | |
| ios_base::flags | | | | |
| ios_base::setf | | | | |
| ios_base::unsetf | | | | |
| ios_base::precision | | | | |
| ios_base::width | | | | |
| Locales | | | | |
| ios_base::imbue | | | | |
| ios_base::getloc | | | | |
| Internal extensible array | | | | |
| ios_base::xalloc | | | | |
| ios_base::iword | | | | |
| ios_base::pword | | | | |
| Miscellaneous | | | | |
| ios_base::register_callback | | | | |
| ****ios_base::sync_with_stdio**** | | | | |
| Member classes | | | | |
| ios_base::failure | | | | |
| ios_base::Init | | | | |
| Member types | | | | |
| ios_base::openmode | | | | |
| ios_base::fmtflags | | | | |
| ios_base::iostate | | | | |
| ios_base::seekdir | | | | |
| ios_base::event | | | | |
| ios_base::event_callback | | | | |

|  |  |  |
| --- | --- | --- |
| static bool sync_with_stdio( bool sync = true ); |  |  |
|  |  |  |

Sets whether the standard C++ streams are synchronized to the standard C streams after each input/output operation.

The standard C++ streams are the following: std::cin, std::cout, std::cerr, std::clog, std::wcin, std::wcout, std::wcerr and std::wclog.

The standard C streams are the following: stdin, stdout and stderr.

For a standard stream str, synchronized with the C stream f, the following pairs of functions have identical effect:

1) std::fputc(f, c) and str.rdbuf()->sputc(c).2) std::fgetc(f) and str.rdbuf()->sbumpc().3) std::ungetc(c, f) and str.rdbuf()->sputbackc(c).

In practice, this means that the synchronized C++ streams are unbuffered, and each I/O operation on a C++ stream is immediately applied to the corresponding C stream's buffer. This makes it possible to freely mix C++ and C I/O.

In addition, synchronized C++ streams are guaranteed to be thread-safe (individual characters output from multiple threads may interleave, but no data races occur).

If the synchronization is turned off, the C++ standard streams are allowed to buffer their I/O independently, which may be considerably faster in some cases.

By default, all eight standard C++ streams are synchronized with their respective C streams.

If this function is called after I/O has occurred on the standard stream, the behavior is implementation-defined: implementations range from no effect to destroying the read buffer.

### Parameters

|  |  |  |
| --- | --- | --- |
| sync | - | the new synchronization setting |

### Return value

Synchronization state before the call to the function.

### Example

Run this code

```
#include <cstdio>
#include <iostream>
 
int main()
{
    std::ios::sync_with_stdio(false);
    std::cout << "a\n";
    std::printf("b\n");
    std::cout << "c\n";
}

```

Possible output:

```
b
a
c

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 49 | C++98 | it was unspecified (1) which state is actually returned and (2) what does 'synchronized' between standard C and C++ streams mean | both specified |

### See also

|  |  |
| --- | --- |
| coutwcout | writes to the standard C output stream stdout (global object) |
| cerrwcerr | writes to the standard C error stream stderr, unbuffered (global object) |
| clogwclog | writes to the standard C error stream stderr (global object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/ios_base/sync_with_stdio&oldid=159121>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 September 2023, at 11:32.