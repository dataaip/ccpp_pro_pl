# std::basic_ifstream<CharT,Traits>::is_open

From cppreference.com
< cpp‎ | io‎ | basic ifstream
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

std::basic_ifstream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| basic_ifstream::basic_ifstream | | | | |
| basic_ifstream::operator=(C++11) | | | | |
| basic_ifstream::swap(C++11) | | | | |
| basic_ifstream::rdbuf | | | | |
| basic_ifstream::native_handle(C++26) | | | | |
| File operations | | | | |
| ****basic_ifstream::is_open**** | | | | |
| basic_ifstream::open | | | | |
| basic_ifstream::close | | | | |
| Non-member functions | | | | |
| swap(std::basic_ifstream)(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| bool is_open() const; |  |  |
|  |  |  |

Checks if the file stream has an associated file.

Effectively calls rdbuf()->is_open().

### Parameters

(none)

### Return value

true if the file stream has an associated file, false otherwise.

### Example

Run this code

```
#include <fstream>
#include <iostream>
#include <string>
 
// this file is called main.cpp
 
bool file_exists(const std::string& str)
{
    std::ifstream fs(str);
    return fs.is_open();
}
 
int main()
{
    std::boolalpha(std::cout);
    std::cout << file_exists("main.cpp")  << '\n'
              << file_exists("strange_file") << '\n';
}

```

Possible output:

```
true
false

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 365 | C++98 | `is_open` was not declared with const qualifier | declared with const qualifier |

### See also

|  |  |
| --- | --- |
| open | opens a file and associates it with the stream   (public member function) |
| close | closes the associated file   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_ifstream/is_open&oldid=50839>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 31 May 2013, at 19:41.