# std::basic_syncbuf<CharT,Traits,Allocator>::basic_syncbuf

From cppreference.com
< cpp‎ | io‎ | basic syncbuf
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

std::basic_syncbuf

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| ****basic_syncbuf::basic_syncbuf****(C++20) | | | | |
| basic_syncbuf::operator=(C++20) | | | | |
| basic_syncbuf::~basic_syncbuf(C++20) | | | | |
| basic_syncbuf::swap(C++20) | | | | |
| basic_syncbuf::emit(C++20) | | | | |
| basic_syncbuf::get_wrapped(C++20) | | | | |
| basic_syncbuf::get_allocator(C++20) | | | | |
| basic_syncbuf::set_emit_on_sync(C++20) | | | | |
| Protected member functions | | | | |
| basic_syncbuf::sync(C++20) | | | | |
| Non-member functions | | | | |
| swap(std::basic_syncbuf)(C++20) | | | | |

|  |  |  |
| --- | --- | --- |
| basic_syncbuf()      : basic_syncbuf( nullptr ) | (1) |  |
| explicit basic_syncbuf( streambuf_type\* obuf )      : basic_syncbuf( obuf, Allocator() ) {} | (2) |  |
| basic_syncbuf( streambuf_type\* obuf, const Allocator& a ); | (3) |  |
| basic_syncbuf( basic_syncbuf&& rhs ); | (4) |  |
|  |  |  |

1) Default constructor: creates an instance of `std::basic_syncbuf` with emit-on-sync policy set to false, wrapped streambuffer set to nullptr, and using default-constructed `Allocator` as the allocator for temporary storage.2,3) Creates an instance of `std::basic_syncbuf` with emit-on-sync policy set to false, wrapped streambuffer set to obuf, and using a as the allocator for temporary storage.4) Move constructor: move-constructs a `std::basic_syncbuf` object by moving all contents from another `std::basic_syncbuf` object rhs, including the temporary storage, the wrapped stream pointer, policy, and all other state (such as the mutex pointer). After move, rhs is not associated with a stream, and rhs.get_wrapped() == nullptr. The put area member pointers of the base class std::basic_streambuf of rhs are guaranteed to be null. Destroying a moved-from rhs will not produce any output.

### Parameters

|  |  |  |
| --- | --- | --- |
| obuf | - | pointer to the std::basic_streambuf to wrap |
| a | - | the allocator to use for temporary storage |
| rhs | - | another `std::basic_syncbuf` to move from |

### Exceptions

2,3) May throw std::bad_alloc from the constructor of the internal temporary storage or std::system_error from the mutex construction.

### Notes

Typically called by the appropriate constructors of std::basic_osyncstream.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| sync[virtual] | synchronizes the buffers with the associated character sequence   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| emit | atomically transmits the entire internal buffer to the wrapped streambuf   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_syncbuf/basic_syncbuf&oldid=144217>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 October 2022, at 10:45.