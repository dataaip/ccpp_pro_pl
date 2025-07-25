# std::strstreambuf::seekoff

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
| strstreambuf::setbuf | | | | |
| ****strstreambuf::seekoff**** | | | | |
| strstreambuf::seekpos | | | | |

|  |  |  |
| --- | --- | --- |
| protected:  virtual pos_type seekoff( off_type off,                            ios_base::seekdir way,                           ios_base::openmode which = ios_base::in | ios_base::out ); |  | (deprecated in C++98)  (removed in C++26) |
|  |  |  |

Repositions std::basic_streambuf::gptr and/or std::basic_streambuf::pptr, if possible, to the position that corresponds to exactly off characters from beginning, end, or current position of the get and/or put area of the buffer.

- If which includes ios_base::in and this buffer is open for reading, then repositions the read pointer std::basic_streambuf::gptr inside the get area as described below.
- If which includes ios_base::out and this buffer is open for writing, then repositions the write pointer std::basic_streambuf::pptr inside the put area as described below.
- If which includes both ios_base::in and `ios_base::out` and the buffer is open for both reading and writing, and way is either ios_base::beg or ios_base::end, then repositions both read and write pointers as described below.
- Otherwise, this function fails.

If the pointer (either `gptr` or `pptr` or both) is repositioned, it is done as follows:

1) If the pointer to be repositioned is a null pointer and the new offset newoff would be non-zero, this function fails.2) The new pointer offset newoff of type `off_type` is determineda) if way == ios_base::beg, then newoff is zerob) if way == ios_base::cur, then newoff is the current position of the pointer (gptr() - eback() or pptr() - pbase())c) if way == ios_base::end, then newoff is the length of the entire initialized part of the buffer (if overallocation is used, the high watermark pointer minus the beginning pointer)3) If newoff + off is negative or out of bounds of the initialized part of the buffer, the function fails4) Otherwise, the pointer is assigned as if by gptr() = eback() + newoff + off or pptr() = pbase() + newoff + off

### Parameters

|  |  |  |
| --- | --- | --- |
| off | - | relative position to set the next pointer(s) to |
| way | - | defines base position to apply the relative offset to. It can be one of the following constants:  |  |  | | --- | --- | | Constant | Explanation | | beg | the beginning of a stream | | end | the ending of a stream | | cur | the current position of stream position indicator | |
| which | - | defines whether the input sequences, the output sequence, or both are affected. It can be one or a combination of the following constants:  |  |  | | --- | --- | | Constant | Explanation | | in | affect the input sequence | | out | affect the output sequence | |

### Return value

pos_type(newoff) on success, pos_type(off_type(-1)) on failure and if pos_type cannot represent the resulting stream position.

### Example

Run this code

```
#include <iostream>
#include <strstream>
 
int main()
{
    char a[] = "123";
    std::strstream ss(a, sizeof a); // in/out
    std::cout << "put pos = " << ss.tellp()
              << " get pos = " << ss.tellg() << '\n';
 
    // absolute positioning both pointers
    ss.rdbuf()->pubseekoff(1, std::ios_base::beg); // move both forward
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
    std::cout << "Wrote 'a' at put position, the buffer is now: '";
    std::cout.write(a, sizeof a);
    std::cout << "'\n";
 
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
Wrote 'a' at put position, the buffer is now: '12a'
reading at get position gives '2'

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 55 | C++98 | `seekoff` returned an undefined invalid stream position on failure | pos_type(off_type(-1)) is returned on failure |

### See also

|  |  |
| --- | --- |
| seekpos[virtual] | repositions the next pointer in the input sequence, output sequence, or both using absolute addressing   (virtual protected member function) |
| seekoff[virtual] | repositions the next pointer in the input sequence, output sequence, or both, using relative addressing   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| seekoff[virtual] | repositions the next pointer in the input sequence, output sequence, or both, using relative addressing   (virtual protected member function of `std::basic_stringbuf<CharT,Traits,Allocator>`) |
| seekoff[virtual] | repositions the file position, using relative addressing   (virtual protected member function of `std::basic_filebuf<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/strstreambuf/seekoff&oldid=170653>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 April 2024, at 06:46.