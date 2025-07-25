# std::basic_ostream<CharT,Traits>::flush

From cppreference.com
< cpp‎ | io‎ | basic ostream
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

std::basic_ostream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Global objects | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | coutwcout | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cerrwcerr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clogwclog | | | | | |
| Member functions | | | | |
| basic_ostream::basic_ostream | | | | |
| basic_ostream::~basic_ostream | | | | |
| basic_ostream::operator=(C++11) | | | | |
| Formatted output | | | | |
| basic_ostream::operator<< | | | | |
| Unformatted output | | | | |
| basic_ostream::put | | | | |
| basic_ostream::write | | | | |
| Positioning | | | | |
| basic_ostream::tellp | | | | |
| basic_ostream::seekp | | | | |
| Miscellaneous | | | | |
| ****basic_ostream::flush**** | | | | |
| basic_ostream::swap(C++11) | | | | |
| Member classes | | | | |
| basic_ostream::sentry | | | | |
| Non-member functions | | | | |
| operator<<(std::basic_ostream) | | | | |
| print(std::ostream)(C++23) | | | | |
| println(std::ostream)(C++23) | | | | |
| vprint_unicode(std::ostream)(C++23) | | | | |
| vprint_nonunicode(std::ostream)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| basic_ostream& flush(); |  |  |
|  |  |  |

Writes uncommitted changes to the underlying output sequence. Behaves as an UnformattedOutputFunction.

If rdbuf() is a null pointer, the sentry object is not constructed.

Otherwise, after constructing and checking the sentry object, calls rdbuf()->pubsync(). If the call returns -1, calls setstate(badbit).

### Parameters

(none)

### Return value

\*this

### Exceptions

May throw std::ios_base::failure if (exceptions() & badbit) != 0.

### Example

Run this code

```
#include <chrono>
#include <iostream>
#include <thread>
 
using namespace std::chrono_literals;
 
void f()
{
    std::cout << "Output from thread... ";
    for (int i{1}; i != 10; ++i)
    {
        std::this_thread::sleep_for(250ms);
        std::cout << i << ' ';
 
        // output three numbers at once;
        // the effect is observable only in real-time
        if (0 == (i % 3))
            std::cout.flush();
    }
    std::cout << std::endl; // flushes as well
}
 
int main()
{
    std::thread tr{f};
    std::this_thread::sleep_for(150ms);
    std::clog << "Output from main\n";
    tr.join();
}

```

Output:

```
Output from main
Output from thread... 1 2 3 4 5 6 7 8 9

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 581 | C++98 | `flush()` did not behave as an UnformattedOutputFunction because of the resolution of LWG issue 60 | behaves as an UnformattedOutputFunction |

### See also

|  |  |
| --- | --- |
| pubsync | invokes sync()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| sync[virtual] | synchronizes the buffers with the associated character sequence   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| flush | flushes the output stream   (function template) |
| endl | outputs '\n' and flushes the output stream   (function template) |
| sync | synchronizes with the underlying storage device   (public member function of `std::basic_istream<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_ostream/flush&oldid=148695>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 February 2023, at 21:46.