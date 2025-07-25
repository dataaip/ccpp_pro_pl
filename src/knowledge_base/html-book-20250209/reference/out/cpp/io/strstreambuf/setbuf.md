# std::strstreambuf::setbuf

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
| strstreambuf::~strstreambuf | | | | |
| strstreambuf::freeze | | | | |
| strstreambuf::str | | | | |
| strstreambuf::pcount | | | | |
| Protected member functions | | | | |
| strstreambuf::underflow | | | | |
| strstreambuf::pbackfail | | | | |
| strstreambuf::overflow | | | | |
| ****strstreambuf::setbuf**** | | | | |
| strstreambuf::seekoff | | | | |
| strstreambuf::seekpos | | | | |

|  |  |  |
| --- | --- | --- |
| protected:  virtual streambuf\* setbuf( char\* s, std::streamsize n ); |  | (deprecated in C++98)  (removed in C++26) |
|  |  |  |

If s is a null pointer and n is zero, this function has no effect.

Otherwise, the effect is implementation-defined: some implementations do nothing, while some implementations deallocate the dynamic member array used as the buffer and begin using the user-supplied character array of size n, whose first element is pointed to by s.

This function is protected virtual, it may only be called through `pubsetbuf()` or from member functions of a user-defined class derived from `std::strstreambuf`.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | pointer to the first byte in the user-provided buffer |
| n | - | the number of bytes in the user-provided buffer |

### Return value

this

### Example

Implementation test to check if `setbuf()` is supported on a dynamic strstream (output obtained with Sun Studio):

Run this code

```
#include <iostream>
#include <strstream>
 
int main()
{
    char a[100] = {};
    std::strstream str;
    str.rdbuf()->pubsetbuf(a, sizeof a);
    str << "Test string" << std::ends;
    std::cout << "user-provided buffer holds \"" << a << "\"\n";
}

```

Possible output:

```
user-provided buffer holds "Test string"

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 66 | C++98 | the effect of `setbuf()` was "performs an operation that is defined separately for each class derived from `strstreambuf`", but there are no classes derived from `strstreambuf` | the effect is implementation-defined |

### See also

|  |  |
| --- | --- |
| pubsetbuf | invokes setbuf()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| setbuf[virtual] | replaces the buffer with user-defined array, if permitted   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| setbuf[virtual] | attempts to replace the controlled character sequence with an array   (virtual protected member function of `std::basic_stringbuf<CharT,Traits,Allocator>`) |
| setbuf[virtual] | provides user-supplied buffer or turns this filebuf unbuffered   (virtual protected member function of `std::basic_filebuf<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/strstreambuf/setbuf&oldid=170652>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 April 2024, at 06:45.