# std::strstreambuf::~strstreambuf

From cppreference.com
< cpp‎ | io‎ | strstreambuf
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

std::strstreambuf

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| strstreambuf::strstreambuf | | | | |
| ****strstreambuf::~strstreambuf**** | | | | |
| strstreambuf::freeze | | | | |
| strstreambuf::str | | | | |
| strstreambuf::pcount | | | | |
| Protected member functions | | | | |
| strstreambuf::underflow | | | | |
| strstreambuf::pbackfail | | | | |
| strstreambuf::overflow | | | | |
| strstreambuf::setbuf | | | | |
| strstreambuf::seekoff | | | | |
| strstreambuf::seekpos | | | | |

|  |  |  |
| --- | --- | --- |
| virtual ~strstreambuf(); |  | (deprecated in C++98)  (removed in C++26) |
|  |  |  |

Destroys a `std::strstreambuf` object. if the object is managing a dynamically-allocated buffer (the buffer state is "allocated") and if the object is not frozen, then deallocates the buffer using the deallocation function provided at construction or delete[] if none was provided.

### Parameters

(none)

### Notes

This destructor is typically called by the destructor of std::strstream.

If str() was called on a dynamic `strstream` and `freeze(false)` was not called after that, this destructor leaks memory.

### Example

Run this code

```
#include <iostream>
#include <strstream>
 
void* my_alloc(size_t n)
{
    std::cout << "my_alloc(" << n << ") called\n";
    return new char[n];
}
 
void my_free(void* p)
{
    std::cout << "my_free() called\n";
    delete[] (char*)p;
}
 
int main()
{
    {
        std::strstreambuf buf(my_alloc, my_free);
        std::ostream s(&buf);
        s << 1.23 << std::ends;
        std::cout << buf.str() << '\n';
        buf.freeze(false);
    } // destructor called here, buffer deallocated
 
    {
        std::strstreambuf buf(my_alloc, my_free);
        std::ostream s(&buf);
        s << 1.23 << std::ends;
        std::cout << buf.str() << '\n';
//      buf.freeze(false);
    } // destructor called here, memory leak!
}

```

Output:

```
my_alloc(4096) called
1.23
my_free() called
my_alloc(4096) called
1.23

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/strstreambuf/%7Estrstreambuf&oldid=170645>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 April 2024, at 06:19.