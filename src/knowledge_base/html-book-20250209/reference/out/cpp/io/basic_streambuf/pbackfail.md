# std::basic_streambuf<CharT,Traits>::pbackfail

From cppreference.com
< cpp‎ | io‎ | basic streambuf
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

std::basic_streambuf

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Public member functions | | | | | | basic_streambuf::~basic_streambuf | | | | | | Locales | | | | | | basic_streambuf::pubimbue | | | | | | basic_streambuf::getloc | | | | | | Positioning | | | | | | basic_streambuf::pubsetbuf | | | | | | basic_streambuf::pubseekoff | | | | | | basic_streambuf::pubseekpos | | | | | | basic_streambuf::pubsync | | | | | | Get area | | | | | | basic_streambuf::in_avail | | | | | | basic_streambuf::snextc | | | | | | basic_streambuf::sbumpc | | | | | | basic_streambuf::sgetc | | | | | | basic_streambuf::sgetn | | | | | | Put area | | | | | | basic_streambuf::sputc | | | | | | basic_streambuf::sputn | | | | | | Putback | | | | | | basic_streambuf::sputbackc | | | | | | basic_streambuf::sungetc | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Protected member functions | | | | | | basic_streambuf::basic_streambuf | | | | | | basic_streambuf::operator=(C++11) | | | | | | basic_streambuf::swap(C++11) | | | | | | Locales | | | | | | basic_streambuf::imbue | | | | | | Positioning | | | | | | basic_streambuf::setbuf | | | | | | basic_streambuf::seekoff | | | | | | basic_streambuf::seekpos | | | | | | basic_streambuf::sync | | | | | | Get area | | | | | | basic_streambuf::showmanyc | | | | | | basic_streambuf::underflow | | | | | | basic_streambuf::uflow | | | | | | basic_streambuf::xsgetn | | | | | | basic_streambuf::ebackbasic_streambuf::gptrbasic_streambuf::egptr | | | | | | basic_streambuf::gbump | | | | | | basic_streambuf::setg | | | | | | Put area | | | | | | basic_streambuf::xsputn | | | | | | basic_streambuf::overflow | | | | | | basic_streambuf::pbasebasic_streambuf::pptrbasic_streambuf::epptr | | | | | | basic_streambuf::pbump | | | | | | basic_streambuf::setp | | | | | | Putback | | | | | | ****basic_streambuf::pbackfail**** | | | | | |

|  |  |  |
| --- | --- | --- |
| protected:  virtual int_type pbackfail( int_type c = Traits::eof() ); |  |  |
|  |  |  |

This function can only be called if any of the following condition is satisfied:

- gptr() is null,
- gptr() == eback(), or
- traits::eq(traits::to_char_type(c), gptr()[-1]) returns false.

This function is called by the public functions sungetc() and sputbackc() (which, in turn, are called by basic_istream::unget and basic_istream::putback) when either:

1) There is no putback position in the get area (`pbackfail()` is called with no arguments). In this situation, the purpose of `pbackfail()` is to back up the get area by one character, if the associated character sequence allows this (e.g. a file-backed streambuf may reload the buffer from a file, starting one character earlier).2) The caller attempts to putback a different character from the one retrieved earlier (`pbackfail()` is called with the character that needs to be put back). In this situation, the purpose of `pbackfail()` is to place the character `c` into the get area at the position just before basic_streambuf::gptr(), and, if possible, to modify the associated character sequence to reflect this change. This may involve backing up the get area as in the first variant.

The default base class version of this function does nothing and returns Traits::eof() in all situations. This function is overridden by the derived classes: basic_stringbuf::pbackfail, basic_filebuf::pbackfail, strstreambuf::pbackfail, and is expected to be overridden by user-defined and third-party library stream classes.

### Parameters

|  |  |  |
| --- | --- | --- |
| ch | - | character to put back or Traits::eof() if only back out is requested |

### Return value

Traits::eof() in case of failure, some other value to indicate success. The base class version always fails.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 32 | C++98 | the calling condition 'traits::eq(\*gptr(),traits::to_char_type(c)) returns false' did not match the description of sputbackc() | corrected to match the description |

### See also

|  |  |
| --- | --- |
| pbackfail[virtual] | backs out the input sequence to unget a character, not affecting the associated file   (virtual protected member function of `std::basic_filebuf<CharT,Traits>`) |
| pbackfail[virtual] | puts a character back into the input sequence   (virtual protected member function of `std::basic_stringbuf<CharT,Traits,Allocator>`) |
| pbackfail[virtual] | backs out the input sequence to unget a character   (virtual protected member function of `std::strstreambuf`) |
| sungetc | moves the next pointer in the input sequence back by one   (public member function) |
| sputbackc | puts one character back in the input sequence   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_streambuf/pbackfail&oldid=141889>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 August 2022, at 23:13.