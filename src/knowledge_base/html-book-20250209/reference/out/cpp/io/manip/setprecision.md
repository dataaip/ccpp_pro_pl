# std::setprecision

From cppreference.com
< cpp‎ | io‎ | manip
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

Input/output manipulators

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Floating-point formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | showpointnoshowpoint | | | | | | ****setprecision**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fixedscientifichexfloatdefaultfloat(C++11)(C++11) | | | | | |
| Integer formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setbase | | | | | | showbasenoshowbase | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | dechexoct | | | | | |
| Boolean formatting | | | | |
| boolalphanoboolalpha | | | | |
| Field width and fill control | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setfill | | | | | | setw | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | internalleftright | | | | | |
| Other formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | showposnoshowpos | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uppercasenouppercase | | | | | |
| Whitespace processing | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ws | | | | | | ends | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | skipwsnoskipws | | | | | |
| Output flushing | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | flush | | | | | | endl | | | | | | flush_emit(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | unitbufnounitbuf | | | | | | emit_on_flushnoemit_on_flush(C++20)(C++20) | | | | | |
| Status flags manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | resetiosflags | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setiosflags | | | | | |
| Time and money I/O | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | get_money(C++11) | | | | | | get_time(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | put_money(C++11) | | | | | | put_time(C++11) | | | | | |
| Quoted manipulator | | | | |
| quoted(C++14) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<iomanip>` |  |  |
| /\*unspecified\*/ setprecision( int n ); |  |  |
|  |  |  |

When used in an expression out << setprecision(n) or in >> setprecision(n), sets the `precision` parameter of the stream out or in to exactly n.

### Parameters

|  |  |  |
| --- | --- | --- |
| n | - | new value for precision |

### Return value

An object of unspecified type such that

- if out is an object of type std::basic_ostream<CharT, Traits>, the expression out << setprecision(n)
  - has type std::basic_ostream<CharT, Traits>&
  - has value out
  - behaves as if it called f(out, n)
- if in is an object of type std::basic_istream<CharT, Traits>, the expression in >> setprecision(n)
  - has type std::basic_istream<CharT, Traits>&
  - has value in
  - behaves as if it called f(in, n)

where the function f is defined as:

```
void f(std::ios_base& str, int n)
{
    // set precision
    str.precision(n);
}

```

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <limits>
#include <numbers>
 
int main()
{
    constexpr long double pi{std::numbers::pi_v<long double>};
 
    const auto default_precision{std::cout.precision()};
    constexpr auto max_precision{std::numeric_limits<long double>::digits10 + 1}; 
 
    std::cout << "default precision: " << default_precision << '\n'
              << "maximum precision: " << max_precision << "\n\n"
                 "precision: pi:\n";
 
    for (int p{0}; p <= max_precision; ++p)
        std::cout << std::setw(2) << p << "  " << std::setprecision(p) << pi << '\n';
 
    std::cout << std::setprecision(default_precision); // restore defaults
}

```

Output:

```
default precision: 6
maximum precision: 19
 
precision: pi:
 0  3
 1  3
 2  3.1
 3  3.14
 4  3.142
 5  3.1416
 6  3.14159
 7  3.141593
 8  3.1415927
 9  3.14159265
10  3.141592654
11  3.1415926536
12  3.14159265359
13  3.14159265359
14  3.1415926535898
15  3.14159265358979
16  3.141592653589793
17  3.1415926535897932
18  3.14159265358979324
19  3.141592653589793239

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 183 | C++98 | `setprecision` could only be used with streams of type std::ostream or std::istream | usable with any character stream |

### See also

|  |  |
| --- | --- |
| fixedscientifichexfloatdefaultfloat(C++11)(C++11) | changes formatting used for floating-point I/O   (function) |
| precision | manages decimal precision of floating point operations   (public member function of `std::ios_base`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/manip/setprecision&oldid=159185>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 September 2023, at 23:06.