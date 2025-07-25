# std::basic_stringbuf<CharT,Traits,Allocator>::swap

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
| ****basic_stringbuf::swap****(C++11) | | | | |
| basic_stringbuf::str | | | | |
| basic_stringbuf::get_allocator(C++20) | | | | |
| basic_stringbuf::view(C++20) | | | | |
| Protected member functions | | | | |
| basic_stringbuf::underflow | | | | |
| basic_stringbuf::pbackfail | | | | |
| basic_stringbuf::overflow | | | | |
| basic_stringbuf::setbuf | | | | |
| basic_stringbuf::seekoff | | | | |
| basic_stringbuf::seekpos | | | | |
| Non-member functions | | | | |
| swap(std::basic_stringbuf)(C++11) | | | | |
| Exposition-only member functions | | | | |
| basic_stringbuf::**init_buf_ptrs** | | | | |

|  |  |  |
| --- | --- | --- |
| void swap( basic_stringbuf& rhs ); |  | (since C++11)  (until C++20) |
| void swap( basic_stringbuf& rhs ) noexcept(/\* see below \*/); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Swaps the state and the contents of \*this and rhs.

|  |  |
| --- | --- |
| The behavior is undefined if `Allocator` does not propagate on swap and the allocators of \*this and other are unequal. | (since C++11) |

### Parameters

|  |  |  |
| --- | --- | --- |
| rhs | - | another `basic_stringbuf` |

### Return value

(none)

### Exceptions

|  |  |
| --- | --- |
| May throw implementation-defined exceptions. | (since C++11) (until C++20) |
| noexcept specification:noexcept(std::allocator_traits<Allocator>::propagate_on_container_swap::value  || std::allocator_traits<Allocator>::is_always_equal::value) | (since C++20) |

### Notes

This function is called automatically when swapping std::stringstream objects. It is rarely necessary to call it directly.

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <sstream>
#include <string>
 
int main()
{
    std::istringstream one("one");
    std::ostringstream two("two");
 
    std::cout << "Before swap: one = " << std::quoted(one.str())
              << ", two = " << std::quoted(two.str()) << ".\n";
 
    one.rdbuf()->swap(*two.rdbuf());
 
    std::cout << "After  swap: one = " << std::quoted(one.str())
              << ", two = " << std::quoted(two.str()) << ".\n";
}

```

Output:

```
Before swap: one = "one", two = "two".
After  swap: one = "two", two = "one".

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a `basic_stringbuf` object   (public member function) |
| swap(C++11) | swaps two string streams   (public member function of `std::basic_stringstream<CharT,Traits,Allocator>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_stringbuf/swap&oldid=160458>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 October 2023, at 09:42.