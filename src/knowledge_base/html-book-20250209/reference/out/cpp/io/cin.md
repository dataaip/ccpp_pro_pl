# std::cin, std::wcin

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
| ****cinwcin**** | | | | |
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
| basic_istream::read | | | | |
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
| Defined in header `<iostream>` |  |  |
| extern std::istream cin; | (1) |  |
| extern std::wistream wcin; | (2) |  |
|  |  |  |

The global objects `std::cin` and `std::wcin` control input from a stream buffer of implementation-defined type (derived from std::streambuf), associated with the standard C input stream stdin.

These objects are guaranteed to be initialized during or before the first time an object of type std::ios_base::Init is constructed and are available for use in the constructors and destructors of static objects with ordered initialization (as long as `<iostream>` is included before the object is defined).

Unless sync_with_stdio(false) has been issued, it is safe to concurrently access these objects from multiple threads for both formatted and unformatted input.

Once `std::cin` is constructed, std::cin.tie() returns &std::cout, and likewise, std::wcin.tie() returns &std::wcout. This means that any formatted input operation on `std::cin` forces a call to std::cout.flush() if any characters are pending for output.

### Notes

The 'c' in the name refers to "character" (stroustrup.com FAQ); `cin` means "character input" and `wcin` means "wide character input".

### Example

Run this code

```
#include <iostream>
 
struct Foo
{
    int n;
    Foo()
    {
        std::cout << "Enter n: "; // no flush needed
        std::cin >> n;
    }
};
 
Foo f; // static object
 
int main()
{
    std::cout << "f.n is " << f.n << '\n';
}

```

Possible output:

```
Enter n: 10
f.n is 10

```

### See also

|  |  |
| --- | --- |
| Init | initializes standard stream objects   (public member class of `std::ios_base`) |
| coutwcout | writes to the standard C output stream stdout (global object) |
| stdinstdoutstderr | expression of type FILE\* associated with the input stream expression of type FILE\* associated with the output stream expression of type FILE\* associated with the error output stream   (macro constant) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/cin&oldid=158809>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 September 2023, at 11:35.