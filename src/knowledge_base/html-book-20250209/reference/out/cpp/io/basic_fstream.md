# std::basic_fstream

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
| ****basic_fstream**** | | | | |
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

****std::basic_fstream****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| basic_fstream::basic_fstream | | | | |
| basic_fstream::operator=(C++11) | | | | |
| basic_fstream::swap(C++11) | | | | |
| basic_fstream::rdbuf | | | | |
| basic_fstream::native_handle(C++26) | | | | |
| File operations | | | | |
| basic_fstream::is_open | | | | |
| basic_fstream::open | | | | |
| basic_fstream::close | | | | |
| Non-member functions | | | | |
| swap(std::basic_fstream)(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<fstream>` |  |  |
| template<  class CharT,      class Traits = std::char_traits<CharT> > class basic_fstream : public std::basic_iostream<CharT, Traits> |  |  |
|  |  |  |

The class template `basic_fstream` implements high-level input/output operations on file based streams. It interfaces a file-based streambuffer (std::basic_filebuf) with the high-level interface of (std::basic_iostream).

A typical implementation of `std::basic_fstream` holds only one non-derived data member: an instance of std::basic_filebuf<CharT, Traits>.

!std-basic fstream-inheritance.svg

Inheritance diagram

Several typedefs for common character types are provided:

|  |  |
| --- | --- |
| Defined in header `<fstream>` | |
| Type | Definition |
| `std::fstream` | std::basic_fstream<char> |
| `std::wfstream` | std::basic_fstream<wchar_t> |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `char_type` | `CharT` |
| `traits_type` | `Traits`; the program is ill-formed if `Traits::char_type` is not `CharT`. |
| `int_type` | `Traits::int_type` |
| `pos_type` | `Traits::pos_type` |
| `off_type` | `Traits::off_type` |
| `native_handle_type`(C++26) | **implementation-defined** type that is TriviallyCopyable and `semiregular` |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the file stream   (public member function) |
| (destructor)[virtual] (implicitly declared) | destructs the `basic_fstream` and the associated buffer, closes the file   (virtual public member function) |
| operator=(C++11) | moves the file stream   (public member function) |
| swap(C++11) | swaps two file streams   (public member function) |
| rdbuf | returns the underlying raw file device object   (public member function) |
| native_handle(C++26) | returns the underlying implementation-defined handle   (public member function) |
| File operations | |
| is_open | checks if the stream has an associated file   (public member function) |
| open | opens a file and associates it with the stream   (public member function) |
| close | closes the associated file   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| std::swap(std::basic_fstream)(C++11) | specializes the std::swap algorithm   (function template) |

## Inherited from std::basic_istream

### Member functions

|  |  |
| --- | --- |
| Formatted input | |
| operator>> | extracts formatted data   (public member function of `std::basic_istream<CharT,Traits>`) |
| Unformatted input | |
| get | extracts characters   (public member function of `std::basic_istream<CharT,Traits>`) |
| peek | reads the next character without extracting it   (public member function of `std::basic_istream<CharT,Traits>`) |
| unget | unextracts a character   (public member function of `std::basic_istream<CharT,Traits>`) |
| putback | puts a character into input stream   (public member function of `std::basic_istream<CharT,Traits>`) |
| getline | extracts characters until the given character is found   (public member function of `std::basic_istream<CharT,Traits>`) |
| ignore | extracts and discards characters until the given character is found   (public member function of `std::basic_istream<CharT,Traits>`) |
| read | extracts blocks of characters   (public member function of `std::basic_istream<CharT,Traits>`) |
| readsome | extracts already available blocks of characters   (public member function of `std::basic_istream<CharT,Traits>`) |
| gcount | returns number of characters extracted by last unformatted input operation   (public member function of `std::basic_istream<CharT,Traits>`) |
| Positioning | |
| tellg | returns the input position indicator   (public member function of `std::basic_istream<CharT,Traits>`) |
| seekg | sets the input position indicator   (public member function of `std::basic_istream<CharT,Traits>`) |
| Miscellaneous | |
| sync | synchronizes with the underlying storage device   (public member function of `std::basic_istream<CharT,Traits>`) |

### Member classes

|  |  |
| --- | --- |
| sentry | implements basic logic for preparation of the stream for input operations   (public member class of `std::basic_istream<CharT,Traits>`) |

## Inherited from std::basic_ostream

### Member functions

|  |  |
| --- | --- |
| Formatted output | |
| operator<< | inserts formatted data   (public member function of `std::basic_ostream<CharT,Traits>`) |
| Unformatted output | |
| put | inserts a character   (public member function of `std::basic_ostream<CharT,Traits>`) |
| write | inserts blocks of characters   (public member function of `std::basic_ostream<CharT,Traits>`) |
| Positioning | |
| tellp | returns the output position indicator   (public member function of `std::basic_ostream<CharT,Traits>`) |
| seekp | sets the output position indicator   (public member function of `std::basic_ostream<CharT,Traits>`) |
| Miscellaneous | |
| flush | synchronizes with the underlying storage device   (public member function of `std::basic_ostream<CharT,Traits>`) |

### Member classes

|  |  |
| --- | --- |
| sentry | implements basic logic for preparation of the stream for output operations   (public member class of `std::basic_ostream<CharT,Traits>`) |

## Inherited from std::basic_ios

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `char_type` | `CharT` |
| `traits_type` | `Traits` |
| `int_type` | `Traits::int_type` |
| `pos_type` | `Traits::pos_type` |
| `off_type` | `Traits::off_type` |

### Member functions

|  |  |
| --- | --- |
| State functions | |
| good | checks if no error has occurred i.e. I/O operations are available   (public member function of `std::basic_ios<CharT,Traits>`) |
| eof | checks if end-of-file has been reached   (public member function of `std::basic_ios<CharT,Traits>`) |
| fail | checks if an error has occurred   (public member function of `std::basic_ios<CharT,Traits>`) |
| bad | checks if a non-recoverable error has occurred   (public member function of `std::basic_ios<CharT,Traits>`) |
| operator! | checks if an error has occurred (synonym of fail())   (public member function of `std::basic_ios<CharT,Traits>`) |
| operator bool | checks if no error has occurred (synonym of `!`fail())   (public member function of `std::basic_ios<CharT,Traits>`) |
| rdstate | returns state flags   (public member function of `std::basic_ios<CharT,Traits>`) |
| setstate | sets state flags   (public member function of `std::basic_ios<CharT,Traits>`) |
| clear | modifies state flags   (public member function of `std::basic_ios<CharT,Traits>`) |
| Formatting | |
| copyfmt | copies formatting information   (public member function of `std::basic_ios<CharT,Traits>`) |
| fill | manages the fill character   (public member function of `std::basic_ios<CharT,Traits>`) |
| Miscellaneous | |
| exceptions | manages exception mask   (public member function of `std::basic_ios<CharT,Traits>`) |
| imbue | sets the locale   (public member function of `std::basic_ios<CharT,Traits>`) |
| rdbuf | manages associated stream buffer   (public member function of `std::basic_ios<CharT,Traits>`) |
| tie | manages tied stream   (public member function of `std::basic_ios<CharT,Traits>`) |
| narrow | narrows characters   (public member function of `std::basic_ios<CharT,Traits>`) |
| widen | widens characters   (public member function of `std::basic_ios<CharT,Traits>`) |

## Inherited from std::ios_base

### Member functions

|  |  |
| --- | --- |
| Formatting | |
| flags | manages format flags   (public member function of `std::ios_base`) |
| setf | sets specific format flag   (public member function of `std::ios_base`) |
| unsetf | clears specific format flag   (public member function of `std::ios_base`) |
| precision | manages decimal precision of floating point operations   (public member function of `std::ios_base`) |
| width | manages field width   (public member function of `std::ios_base`) |
| Locales | |
| imbue | sets locale   (public member function of `std::ios_base`) |
| getloc | returns current locale   (public member function of `std::ios_base`) |
| Internal extensible array | |
| xalloc[static] | returns a program-wide unique integer that is safe to use as index to pword() and iword()   (public static member function of `std::ios_base`) |
| iword | resizes the private storage if necessary and access to the long element at the given index   (public member function of `std::ios_base`) |
| pword | resizes the private storage if necessary and access to the void\* element at the given index   (public member function of `std::ios_base`) |
| Miscellaneous | |
| register_callback | registers event callback function   (public member function of `std::ios_base`) |
| sync_with_stdio[static] | sets whether C++ and C I/O libraries are interoperable   (public static member function of `std::ios_base`) |
| Member classes | |
| failure | stream exception   (public member class of `std::ios_base`) |
| Init | initializes standard stream objects   (public member class of `std::ios_base`) |

|  |  |
| --- | --- |
| Member types and constants | |
| Type | Explanation |
| openmode | stream open mode type The following constants are also defined:   |  |  | | --- | --- | | Constant | Explanation | | app | seek to the end of stream before each write | | binary | open in binary mode | | in | open for reading | | out | open for writing | | trunc | discard the contents of the stream when opening | | ate | seek to the end of stream immediately after open | | noreplace (C++23) | open in exclusive mode |    (typedef) |
| fmtflags | formatting flags type The following constants are also defined:   |  |  | | --- | --- | | Constant | Explanation | | dec | use decimal base for integer I/O: see std::dec | | oct | use octal base for integer I/O: see std::oct | | hex | use hexadecimal base for integer I/O: see std::hex | | basefield | dec | oct | hex. Useful for masking operations | | left | left adjustment (adds fill characters to the right): see std::left | | right | right adjustment (adds fill characters to the left): see std::right | | internal | internal adjustment (adds fill characters to the internal designated point): see std::internal | | adjustfield | left | right | internal. Useful for masking operations | | scientific | generate floating point types using scientific notation, or hex notation if combined with fixed: see std::scientific | | fixed | generate floating point types using fixed notation, or hex notation if combined with scientific: see std::fixed | | floatfield | scientific | fixed. Useful for masking operations | | boolalpha | insert and extract bool type in alphanumeric format: see std::boolalpha | | showbase | generate a prefix indicating the numeric base for integer output, require the currency indicator in monetary I/O: see std::showbase | | showpoint | generate a decimal-point character unconditionally for floating-point number output: see std::showpoint | | showpos | generate a + character for non-negative numeric output: see std::showpos | | skipws | skip leading whitespace before certain input operations: see std::skipws | | unitbuf | flush the output after each output operation: see std::unitbuf | | uppercase | replace certain lowercase letters with their uppercase equivalents in certain output operations: see std::uppercase |    (typedef) |
| iostate | state of the stream type The following constants are also defined:   |  |  | | --- | --- | | Constant | Explanation | | goodbit | no error | | badbit | irrecoverable stream error | | failbit | input/output operation failed (formatting or extraction error) | | eofbit | associated input sequence has reached end-of-file |    (typedef) |
| seekdir | seeking direction type The following constants are also defined:   |  |  | | --- | --- | | Constant | Explanation | | beg | the beginning of a stream | | end | the ending of a stream | | cur | the current position of stream position indicator |    (typedef) |
| event | specifies event type   (enum) |
| event_callback | callback function type   (typedef) |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_fstream_native_handle` | `202306L` | (C++26) | native handles support |

### Example

Run this code

```
#include <fstream>
#include <iostream>
#include <string>
 
int main()
{
    std::string filename{"test.bin"};
    std::fstream s{filename, s.binary | s.trunc | s.in | s.out};
 
    if (!s.is_open())
        std::cout << "failed to open " << filename << '\n';
    else
    {
        // write
        double d{3.14};
        s.write(reinterpret_cast<char*>(&d), sizeof d); // binary output
        s << 123 << "abc";                              // text output
 
        // for fstream, this moves the file position pointer (both put and get)
        s.seekp(0);
 
        // read
        d = 2.71828;
        s.read(reinterpret_cast<char*>(&d), sizeof d); // binary input
        int n;
        std::string str;
        if (s >> n >> str)                             // text input
            std::cout << "read back from file: " << d << ' ' << n << ' ' << str << '\n';
    }
}

```

Output:

```
read back from file: 3.14 123 abc

```

### See also

|  |  |
| --- | --- |
| getline | read data from an I/O stream into a string   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_fstream&oldid=156283>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 August 2023, at 05:15.