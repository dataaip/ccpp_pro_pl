# std::strstreambuf

From cppreference.com
< cpp‎ | io
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
| ****strstreambuf****(C++98/26\*) | | | | |
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

****std::strstreambuf****

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
| strstreambuf::setbuf | | | | |
| strstreambuf::seekoff | | | | |
| strstreambuf::seekpos | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<strstream>` |  |  |
| class strstreambuf : public std::basic_streambuf<char> |  | (deprecated in C++98)  (removed in C++26) |
|  |  |  |

`std::strstreambuf` is a std::basic_streambuf whose associated character sequence is a character array, which may be constant (e.g. a string literal), modifiable but not dynamic (e.g. a stack-allocated array), or dynamic, in which case the `std::strstreambuf` may be allowed to reallocate the array as necessary to accommodate output (e.g. by calling delete[] and new[] or user-provided functions).

Typical implementation of a `std::strstreambuf` holds four private data members:

1) buffer state, a bitmask type which can represent any combination of the four values "allocated" (destructor will deallocate), "constant" (output not allowed), "dynamic" (output may reallocate), or "frozen" (deallocation and reallocation are not allowed)2) allocated buffer size (the beginning of the buffer does not need a special data member, it may be stored in the inherited pointer eback())3) pointer to user-provided allocation function4) pointer to user-provided deallocation function.

### Notes

After any call to str() on a stream with a dynamic buffer, a call to freeze(false) is required to allow the `strstreambuf` destructor to deallocate the buffer when necessary.

`strstreambuf` has been deprecated since C++98 and removed since C++26. The recommended replacement is std::spanbuf(since C++23).

### Member functions

|  |  |
| --- | --- |
| Public member functions | |
| (constructor) | constructs a `strstreambuf` object   (public member function) |
| (destructor)[virtual] | destructs a `strstreambuf` object, optionally deallocating the character array   (virtual public member function) |
| freeze | sets/clears the frozen state of the buffer   (public member function) |
| str | marks the buffer frozen and returns the beginning pointer of the input sequence   (public member function) |
| pcount | returns the next pointer minus the beginning pointer in the output sequence: the number of characters written   (public member function) |
| Protected member functions | |
| underflow[virtual] | reads a character from the input sequence without advancing the next pointer   (virtual protected member function) |
| pbackfail[virtual] | backs out the input sequence to unget a character   (virtual protected member function) |
| overflow[virtual] | appends a character to the output sequence, may reallocate or initially allocate the buffer if dynamic and not frozen   (virtual protected member function) |
| setbuf[virtual] | attempts to replace the controlled character sequence with an array   (virtual protected member function) |
| seekoff[virtual] | repositions the next pointer in the input sequence, output sequence, or both, using relative addressing   (virtual protected member function) |
| seekpos[virtual] | repositions the next pointer in the input sequence, output sequence, or both using absolute addressing   (virtual protected member function) |

## Inherited from std::basic_streambuf

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `char_type` | `CharT` |
| `traits_type` | `Traits`; the program is ill-formed if `Traits::char_type` is not `CharT`. |
| `int_type` | `Traits::int_type` |
| `pos_type` | `Traits::pos_type` |
| `off_type` | `Traits::off_type` |

### Member functions

|  |  |
| --- | --- |
| (destructor)[virtual] | destructs the `basic_streambuf` object   (virtual public member function of `std::basic_streambuf<CharT,Traits>`) |
| Locales | |
| pubimbue | changes the associated locale and invokes imbue()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| getloc | obtains a copy of the associated locale   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| Positioning | |
| pubsetbuf | invokes setbuf()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| pubseekoff | invokes seekoff()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| pubseekpos | invokes seekpos()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| pubsync | invokes sync()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| Get area | |
| in_avail | obtains the number of characters immediately available in the get area   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| snextc | advances the input sequence, then reads one character without advancing again   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| sbumpcstossc(removed in C++17) | reads one character from the input sequence and advances the sequence   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| sgetc | reads one character from the input sequence without advancing the sequence   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| sgetn | invokes xsgetn()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| Put area | |
| sputc | writes one character to the put area and advances the next pointer   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| sputn | invokes xsputn()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| Putback | |
| sputbackc | puts one character back in the input sequence   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| sungetc | moves the next pointer in the input sequence back by one   (public member function of `std::basic_streambuf<CharT,Traits>`) |

### Protected member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `basic_streambuf` object   (protected member function) |
| operator=(C++11) | replaces a `basic_streambuf` object   (protected member function) |
| swap(C++11) | swaps two `basic_streambuf` objects   (protected member function) |
| Locales | |
| imbue[virtual] | reacts to a change of the associated locale   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| Positioning | |
| setbuf[virtual] | replaces the buffer with user-defined array, if permitted   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| seekoff[virtual] | repositions the next pointer in the input sequence, output sequence, or both, using relative addressing   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| seekpos[virtual] | repositions the next pointer in the input sequence, output sequence, or both using absolute addressing   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| sync[virtual] | synchronizes the buffers with the associated character sequence   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| Get area | |
| showmanyc[virtual] | obtains the number of characters available for input in the associated input sequence, if known   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| underflow[virtual] | reads characters from the associated input sequence to the get area   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| uflow[virtual] | reads characters from the associated input sequence to the get area and advances the next pointer   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| xsgetn[virtual] | reads multiple characters from the input sequence   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| ebackgptregptr | returns a pointer to the beginning, current character and the end of the get area   (protected member function) |
| gbump | advances the next pointer in the input sequence   (protected member function) |
| setg | repositions the beginning, next, and end pointers of the input sequence   (protected member function) |
| Put area | |
| xsputn[virtual] | writes multiple characters to the output sequence   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| overflow[virtual] | writes characters to the associated output sequence from the put area   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| pbasepptrepptr | returns a pointer to the beginning, current character and the end of the put area   (protected member function) |
| pbump | advances the next pointer of the output sequence   (protected member function) |
| setp | repositions the beginning, next, and end pointers of the output sequence   (protected member function) |
| Putback | |
| pbackfail[virtual] | puts a character back into the input sequence, possibly modifying the input sequence   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/strstreambuf&oldid=170661>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 April 2024, at 07:22.