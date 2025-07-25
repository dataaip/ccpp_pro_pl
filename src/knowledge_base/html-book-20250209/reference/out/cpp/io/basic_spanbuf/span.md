# std::basic_spanbuf<CharT,Traits>::span

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
| ****basic_spanbuf::span****(C++23) | | | | |
| Protected member functions | | | | |
| basic_spanbuf::setbuf(C++23) | | | | |
| basic_spanbuf::seekoff(C++23) | | | | |
| basic_spanbuf::seekpos(C++23) | | | | |
| Non-member functions | | | | |
| swap(std::basic_spanbuf)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| std::span<CharT> span() const noexcept; | (1) | (since C++23) |
| void span( std::span<CharT> s ) noexcept; | (2) | (since C++23) |
|  |  |  |

1) Gets a `span` referencing the written area if std::ios_base::out is set in the open mode, or a `span` referencing the underlying buffer otherwise.2) Makes the `basic_spanbuf` perform I/O on the buffer referenced by `s`. Sets pointers to get area, put area, or both.

| Set bits in open mode (affecting pointers to get area) | Return value after setting | | |
| --- | --- | --- | --- |
| eback() | gptr() | egptr() |
| std::ios_base::in | s.data() | s.data() | s.data() + s.size() |
|  | | | |
| Set bits in open mode (affecting pointers to put area) | Return value after setting | | |
| pbase() | pptr() | epptr() |
| std::ios_base::out && !std::ios_base::ate | s.data() | s.data() | s.data() + s.size() |
| std::ios_base::out && std::ios_base::ate | s.data() | s.data() + s.size() | s.data() + s.size() |

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | a std::span that references the user-provided buffer |

### Return value

1) std::span<CharT>(pbase(), pptr()) if std::ios_base::out is set in the open mode, or a std::span<CharT> that references the whole underlying buffer otherwise.2) (none)

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| str | replaces or obtains a copy of the associated character string   (public member function of `std::basic_stringbuf<CharT,Traits,Allocator>`) |
| view(C++20) | obtains a view over the underlying character sequence   (public member function of `std::basic_stringbuf<CharT,Traits,Allocator>`) |
| str | marks the buffer frozen and returns the beginning pointer of the input sequence   (public member function of `std::strstreambuf`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_spanbuf/span&oldid=130776>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 June 2021, at 10:29.