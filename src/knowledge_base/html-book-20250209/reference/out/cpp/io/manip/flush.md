# std::flush

From cppreference.com
< cpp‎ | io‎ | manip
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

Input/output manipulators

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Floating-point formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | showpointnoshowpoint | | | | | | setprecision | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fixedscientifichexfloatdefaultfloat(C++11)(C++11) | | | | | |
| Integer formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setbase | | | | | | showbasenoshowbase | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | dechexoct | | | | | |
| Boolean formatting | | | | |
| boolalphanoboolalpha | | | | |
| Field width and fill control | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setfill | | | | | | setw | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | internalleftright | | | | | |
| Other formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | showposnoshowpos | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uppercasenouppercase | | | | | |
| Whitespace processing | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ws | | | | | | ends | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | skipwsnoskipws | | | | | |
| Output flushing | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****flush**** | | | | | | endl | | | | | | flush_emit(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | unitbufnounitbuf | | | | | | emit_on_flushnoemit_on_flush(C++20)(C++20) | | | | | |
| Status flags manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | resetiosflags | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setiosflags | | | | | |
| Time and money I/O | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | get_money(C++11) | | | | | | get_time(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | put_money(C++11) | | | | | | put_time(C++11) | | | | | |
| Quoted manipulator | | | | |
| quoted(C++14) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ostream>` |  |  |
| template< class CharT, class Traits >  std::basic_ostream<CharT, Traits>& flush( std::basic_ostream<CharT, Traits>& os ); |  |  |
|  |  |  |

Flushes the output sequence os as if by calling os.flush().

This is an output-only I/O manipulator, it may be called with an expression such as out << std::flush for any `out` of type std::basic_ostream.

### Notes

This manipulator may be used to produce an incomplete line of output immediately, e.g. when displaying output from a long-running process, logging activity of multiple threads or logging activity of a program that may crash unexpectedly. An explicit flush of std::cout is also necessary before a call to std::system, if the spawned process performs any screen I/O (a common example is std::system("pause") on Windows). In most other usual interactive I/O scenarios, std::endl is redundant when used with std::cout because any input from std::cin, output to std::cerr, or program termination forces a call to std::cout.flush().

When a complete line of output needs to be flushed, the std::endl manipulator may be used.

When every output operation needs to be flushed, the std::unitbuf manipulator may be used.

### Parameters

|  |  |  |
| --- | --- | --- |
| os | - | reference to output stream |

### Return value

os (reference to the stream after manipulation).

### Example

Without `std::flush`, the output would be the same, but may not appear in real time.

Run this code

```
#include <chrono>
#include <iostream>
 
template<typename Diff>
void log_progress(Diff d)
{
    std::cout << std::chrono::duration_cast<std::chrono::milliseconds>(d) << " ... "
              << std::flush;
}
 
int main()
{
    volatile int sink = 0;
 
    auto t1 = std::chrono::high_resolution_clock::now();
    for (int j = 0; j < 5; ++j)
    {
        for (int n = 0; n < 10000; ++n)
            for (int m = 0; m < 20000; ++m)
                sink += m * n; // do some work
        auto now = std::chrono::high_resolution_clock::now();
        log_progress(now - t1);
    }
    std::cout << '\n';
}

```

Possible output:

```
567ms ... 1137ms ... 1707ms ... 2269ms ... 2842ms ...

```

### See also

|  |  |
| --- | --- |
| unitbufnounitbuf | controls whether output is flushed after each operation   (function) |
| endl | outputs '\n' and flushes the output stream   (function template) |
| flush | synchronizes with the underlying storage device   (public member function of `std::basic_ostream<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/manip/flush&oldid=159202>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 September 2023, at 10:17.