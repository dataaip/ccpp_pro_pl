# std::basic_istream<CharT,Traits>::read

From cppreference.com
< cpp‎ | io‎ | basic istream
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

std::basic_istream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Global objects | | | | |
| cinwcin | | | | |
| Member functions | | | | |
| basic_istream::basic_istream | | | | |
| basic_istream::~basic_istream | | | | |
| basic_istream::operator=(C++11) | | | | |
| Formatted input | | | | |
| basic_istream::operator>> | | | | |
| Unformatted input | | | | |
| basic_istream::get | | | | |
| basic_istream::peek | | | | |
| basic_istream::unget | | | | |
| basic_istream::putback | | | | |
| basic_istream::getline | | | | |
| basic_istream::ignore | | | | |
| ****basic_istream::read**** | | | | |
| basic_istream::readsome | | | | |
| basic_istream::gcount | | | | |
| Positioning | | | | |
| basic_istream::tellg | | | | |
| basic_istream::seekg | | | | |
| Miscellaneous | | | | |
| basic_istream::sync | | | | |
| basic_istream::swap(C++11) | | | | |
| Member classes | | | | |
| basic_istream::sentry | | | | |
| Non-member functions | | | | |
| operator>>(std::basic_istream) | | | | |

|  |  |  |
| --- | --- | --- |
| basic_istream& read( char_type\* s, std::streamsize count ); |  |  |
|  |  |  |

Extracts characters from stream.

Behaves as UnformattedInputFunction. After constructing and checking the sentry object, extracts characters and stores them into successive locations of the character array whose first element is pointed to by s. Characters are extracted and stored until any of the following conditions occurs:

- count characters were extracted and stored.

- end of file condition occurs on the input sequence (in which case, setstate(failbit|eofbit) is called). The number of successfully extracted characters can be queried using gcount().

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | pointer to the character array to store the characters to |
| count | - | number of characters to read |

### Return value

\*this

### Exceptions

failure if an error occurred (the error state flag is not goodbit) and exceptions() is set to throw for that state.

If an internal operation throws an exception, it is caught and badbit is set. If exceptions() is set for `badbit`, the exception is rethrown.

### Notes

When using a non-converting locale (the default locale is non-converting), the overrider of this function in std::basic_ifstream may be optimized for zero-copy bulk I/O (by means of overriding std::streambuf::xsgetn).

### Example

Run this code

```
#include <cstdint>
#include <fstream>
#include <iostream>
#include <sstream>
#include <string>
 
int main()
{
    // read() is often used for binary I/O
    std::string bin = {'\x12', '\x12', '\x12', '\x12'};
    std::istringstream raw(bin);
    std::uint32_t n;
    if (raw.read(reinterpret_cast<char*>(&n), sizeof n))
        std::cout << std::hex << std::showbase << n << '\n';
 
    // prepare file for next snippet
    std::ofstream("test.txt", std::ios::binary) << "abcd1\nabcd2\nabcd3";
 
    // read entire file into string
    if (std::ifstream is{"test.txt", std::ios::binary | std::ios::ate})
    {
        auto size = is.tellg();
        std::string str(size, '\0'); // construct string to stream size
        is.seekg(0);
        if (is.read(&str[0], size))
            std::cout << str << '\n';
    }
}

```

Output:

```
0x12121212
abcd1
abcd2
abcd3

```

### See also

|  |  |
| --- | --- |
| write | inserts blocks of characters   (public member function of `std::basic_ostream<CharT,Traits>`) |
| operator>> | extracts formatted data   (public member function) |
| readsome | extracts already available blocks of characters   (public member function) |
| get | extracts characters   (public member function) |
| getline | extracts characters until the given character is found   (public member function) |
| fread | reads from a file   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_istream/read&oldid=158531>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 September 2023, at 06:29.