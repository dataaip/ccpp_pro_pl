# std::basic_stringbuf<CharT,Traits,Allocator>::seekoff

From cppreference.com
< cpp‎ | io‎ | basic stringbuf
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

std::basic_stringbuf

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| basic_stringbuf::basic_stringbuf | | | | |
| basic_stringbuf::operator=(C++11) | | | | |
| basic_stringbuf::swap(C++11) | | | | |
| basic_stringbuf::str | | | | |
| basic_stringbuf::get_allocator(C++20) | | | | |
| basic_stringbuf::view(C++20) | | | | |
| Protected member functions | | | | |
| basic_stringbuf::underflow | | | | |
| basic_stringbuf::pbackfail | | | | |
| basic_stringbuf::overflow | | | | |
| basic_stringbuf::setbuf | | | | |
| ****basic_stringbuf::seekoff**** | | | | |
| basic_stringbuf::seekpos | | | | |
| Non-member functions | | | | |
| swap(std::basic_stringbuf)(C++11) | | | | |
| Exposition-only member functions | | | | |
| basic_stringbuf::**init_buf_ptrs** | | | | |

|  |  |  |
| --- | --- | --- |
| protected:  virtual pos_type seekoff( off_type off,                            std::ios_base::seekdir dir, std::ios_base::openmode which = std::ios_base::in | std::ios_base::out ); |  |  |
|  |  |  |

Repositions std::basic_streambuf::gptr and/or std::basic_streambuf::pptr, if possible, to the position that corresponds to exactly off characters from beginning, end, or current position of the get and/or put area of the buffer.

- If which includes std::ios_base::in and this buffer is open for reading (that is, if (which & std::ios_base::in) == std::ios_base::in), then repositions the read pointer std::basic_streambuf::gptr inside the get area as described below
- If which includes std::ios_base::out and this buffer is open for writing (that is, (which & std::ios_base::out) == std::ios_base::out), then repositions the write pointer std::basic_streambuf::pptr inside the put area as described below
- If which includes both std::ios_base::in and std::ios_base::out and the buffer is open for both reading and writing (that is, (which & (std::ios_base::in | std::ios_base::out)) == (std::ios_base::in | std::ios_base::out)), and dir is either std::ios_base::beg or std::ios_base::end, then repositions both read and write pointers as described below.
- Otherwise, this function fails.

If gptr and/or pptr is repositioned, it is done as follows:

1) The new pointer offset newoff of type `off_type` is determineda) if dir == std::ios_base::beg, then newoff is zerob) if dir == std::ios_base::cur, then newoff is the current position of the pointer (gptr() - eback() or pptr() - pbase())c) if dir == std::ios_base::end, then newoff is the length of the entire initialized part of the buffer (if over-allocation is used, the high watermark pointer minus the beginning pointer)2) If the pointer to be repositioned is a null pointer and newoff would be non-zero, this function fails.3) If newoff + off < 0 (the repositioning would move the pointer to before the beginning of the buffer) or if newoff + off would point past the end of the buffer (or past the last initialized character in the buffer if over-allocation is used), the function fails.4) Otherwise, the pointer is assigned as if by gptr() = eback() + newoff + off or pptr() = pbase() + newoff + off.

### Parameters

|  |  |  |
| --- | --- | --- |
| off | - | relative position to set the next pointer(s) to |
| dir | - | defines base position to apply the relative offset to. It can be one of the following constants:  |  |  | | --- | --- | | Constant | Explanation | | beg | the beginning of a stream | | end | the ending of a stream | | cur | the current position of stream position indicator | |
| which | - | defines whether the input sequences, the output sequence, or both are affected. It can be one or a combination of the following constants:  |  |  | | --- | --- | | Constant | Explanation | | in | affect the input sequence | | out | affect the output sequence | |

### Return value

pos_type(newoff) on success, pos_type(off_type(-1)) on failure or if `pos_type` cannot represent the resulting stream position.

### Example

Run this code

```
#include <iostream>
#include <sstream>
 
int main()
{
    std::stringstream ss("123"); // in/out
    std::cout << "put pos = " << ss.tellp()
              << " get pos = " << ss.tellg() << '\n';
 
    // absolute positioning both pointers
    ss.rdbuf()->pubseekoff(1, std::ios_base::beg); // move both 1 forward
    std::cout << "put pos = " << ss.tellp()
              << " get pos = " << ss.tellg() << '\n';
 
    // try to move both pointers 1 forward from current position
    if (-1 == ss.rdbuf()->pubseekoff(1, std::ios_base::cur))
        std::cout << "moving both pointers from current position failed\n";
    std::cout << "put pos = " << ss.tellp()
              << " get pos = " << ss.tellg() << '\n';
 
    // move the write pointer 1 forward, but not the read pointer
    // can also be called as ss.seekp(1, std::ios_base::cur);
    ss.rdbuf()->pubseekoff(1, std::ios_base::cur, std::ios_base::out);
    std::cout << "put pos = " << ss.tellp()
              << " get pos = " << ss.tellg() << '\n';
 
    ss << 'a'; // write at put position
    std::cout << "Wrote 'a' at put position, the buffer is now " << ss.str() << '\n';
 
    char ch;
    ss >> ch;
    std::cout << "reading at get position gives '" << ch << "'\n";
}

```

Output:

```
put pos = 0 get pos = 0
put pos = 1 get pos = 1
moving both pointers from current position failed
put pos = 1 get pos = 1
put pos = 2 get pos = 1
Wrote 'a' at put position, the buffer is now 12a
reading at get position gives '2'

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 55 | C++98 | `seekoff` returned an undefined invalid stream position on failure | pos_type(off_type(-1)) is returned on failure |
| LWG 375 | C++98 | static constant members of std::ios_base were misspecified as members of std::basic_ios | corrected |
| LWG 432 | C++98 | `seekoff` might succeed even if newoff + off would point past the last initialized character | `seekoff` fails in this case |
| LWG 453 | C++98 | repositioning null gptr() and/or null pptr() with a new offset of zero always failed | it can succeed in this case |
| LWG 563 | C++98 | the end pointer could not be used to calculate newoff because it could not be precisely controlled by the program after resolving LWG issue 432 | use the high watermark pointer instead |

### See also

|  |  |
| --- | --- |
| pubseekoff | invokes seekoff()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| seekpos[virtual] | repositions the next pointer in the input sequence, output sequence, or both using absolute addressing   (virtual protected member function) |
| seekoff[virtual] | repositions the file position, using relative addressing   (virtual protected member function of `std::basic_filebuf<CharT,Traits>`) |
| seekoff[virtual] | repositions the next pointer in the input sequence, output sequence, or both, using relative addressing   (virtual protected member function of `std::strstreambuf`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_stringbuf/seekoff&oldid=148675>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 February 2023, at 00:45.