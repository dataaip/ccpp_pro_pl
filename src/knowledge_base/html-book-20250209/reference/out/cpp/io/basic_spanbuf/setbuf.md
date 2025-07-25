# std::basic_spanbuf<CharT,Traits>::setbuf

From cppreference.com
< cpp‎ | io‎ | basic spanbuf
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

std::basic_spanbuf

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| basic_spanbuf::basic_spanbuf(C++23) | | | | |
| basic_spanbuf::operator=(C++23) | | | | |
| basic_spanbuf::swap(C++23) | | | | |
| basic_spanbuf::span(C++23) | | | | |
| Protected member functions | | | | |
| ****basic_spanbuf::setbuf****(C++23) | | | | |
| basic_spanbuf::seekoff(C++23) | | | | |
| basic_spanbuf::seekpos(C++23) | | | | |
| Non-member functions | | | | |
| swap(std::basic_spanbuf)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| protected:  std::basic_streambuf<CharT, Traits>\* setbuf( CharT \*s, std::streamsize n ) override; |  | (since C++23) |
|  |  |  |

Makes the `basic_spanbuf` perform I/O on the buffer ``s`,`s + n`)`. Equivalently calls this->span([std::span<CharT>(s, n)) and then returns this.

| Set bits in open mode (affecting pointers to get area) | Return value after setting | | |
| --- | --- | --- | --- |
| eback() | gptr() | egptr() |
| std::ios_base::in | s | s | s + n |
|  | | | |
| Set bits in open mode (affecting pointers to put area) | Return value after setting | | |
| pbase() | pptr() | epptr() |
| std::ios_base::out && !std::ios_base::ate | s | s | s + n |
| std::ios_base::out && std::ios_base::ate | s | s + n | s + n |

This function is protected virtual, it may only be called through `pubsetbuf()` or from member functions of a user-defined class derived from std::basic_spanbuf.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | pointer to the first `CharT` in the user-provided buffer |
| n | - | the number of `CharT` elements in the user-provided buffer |

### Return value

this

### Notes

The deprecated stream buffer std::strstreambuf or the boost.IOStreams device `boost::basic_array` can also implement I/O buffering over a user-provided char array.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| pubsetbuf | invokes setbuf()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| setbuf[virtual] | attempts to replace the controlled character sequence with an array   (virtual protected member function of `std::basic_stringbuf<CharT,Traits,Allocator>`) |
| setbuf[virtual] | attempts to replace the controlled character sequence with an array   (virtual protected member function of `std::strstreambuf`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_spanbuf/setbuf&oldid=158805>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 September 2023, at 11:06.