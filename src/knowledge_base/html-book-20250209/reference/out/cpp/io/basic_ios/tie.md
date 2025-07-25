# std::basic_ios<CharT,Traits>::tie

From cppreference.com
< cpp‎ | io‎ | basic ios
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

std::basic_ios

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| basic_ios::basic_ios | | | | |
| basic_ios::~basic_ios | | | | |
| State functions | | | | |
| basic_ios::good | | | | |
| basic_ios::eof | | | | |
| basic_ios::fail | | | | |
| basic_ios::bad | | | | |
| basic_ios::operator! | | | | |
| basic_ios::operator bool | | | | |
| basic_ios::rdstate | | | | |
| basic_ios::setstate | | | | |
| basic_ios::clear | | | | |
| Formatting | | | | |
| basic_ios::copyfmt | | | | |
| basic_ios::fill | | | | |
| Miscellaneous | | | | |
| basic_ios::exceptions | | | | |
| basic_ios::imbue | | | | |
| basic_ios::rdbuf | | | | |
| ****basic_ios::tie**** | | | | |
| basic_ios::narrow | | | | |
| basic_ios::widen | | | | |
| Protected member functions | | | | |
| basic_ios::init | | | | |
| basic_ios::move(C++11) | | | | |
| basic_ios::swap(C++11) | | | | |
| basic_ios::set_rdbuf(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| std::basic_ostream<CharT, Traits>\* tie() const; | (1) |  |
| std::basic_ostream<CharT, Traits>\* tie( std::basic_ostream<CharT, Traits>\* str ); | (2) |  |
|  |  |  |

Manages the tied stream. A tied stream is an output stream which is synchronized with the sequence controlled by the stream buffer (rdbuf()), that is, flush() is called on the tied stream before any input/output operation on \*this.

1) Returns the current tied stream. If there is no tied stream, a null pointer is returned.2) Sets the current tied stream to str. Returns the tied stream before the operation. If there is no tied stream, a null pointer is returned. If str is not null and tie() is reachable by traversing the linked list of tied stream objects starting from str->tie(), the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | an output stream to set as the tied stream |

### Return value

The tied stream, or a null pointer if there was no tied stream.

### Exceptions

May throw implementation-defined exceptions.

### Notes

By default, the standard stream std::cout is tied to std::cin and std::cerr. Similarly, its wide counterpart std::wcout is tied to std::wcin and std::wcerr.

### Example

Run this code

```
#include <fstream>
#include <iomanip>
#include <iostream>
#include <string>
 
int main()
{
    std::ofstream os("test.txt");
    std::ifstream is("test.txt");
    std::string value("0");
 
    os << "Hello";
    is >> value;
 
    std::cout << "Result before tie(): " << std::quoted(value) << "\n";
    is.clear();
    is.tie(&os);
 
    is >> value;
 
    std::cout << "Result after tie(): " << std::quoted(value) << "\n";
}

```

Output:

```
Result before tie(): "0"
Result after tie(): "Hello"

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 835 | C++98 | two streams could be tied to each other[[1]](tie.html#cite_note-1) (either directly or through another intermediate stream object) | the behavior is undefined in this case |

1. ↑ std::basic_ostream::flush() is an UnformattedOutputFunction, so it creates a sentry object while being called. When `flush()` is called on a stream object, the constructor of the sentry object will call `flush()` on its tied stream, and that `flush()` will construct another sentry object and its constructor will call `flush()` on the tied stream of that stream and so on. Therefore, if streams a and b are (directly or indirectly) tied to each other, calling a.flush() will eventually call b.flush(), which will eventually call a.flush(), and will result in an infinite loop.
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_ios/tie&oldid=149634>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 March 2023, at 00:23.