# std::quoted

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | showpointnoshowpoint | | | | | | setprecision | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fixedscientifichexfloatdefaultfloat(C++11)(C++11) | | | | | |
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
| ****quoted****(C++14) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<iomanip>` |  |  |
| template< class CharT >  /\*unspecified\*/ quoted( const CharT\* s,                         CharT delim = CharT('"'), CharT escape = CharT('\\') ); | (1) | (since C++14) |
| template< class CharT, class Traits, class Allocator >  /\*unspecified\*/ quoted( const std::basic_string<CharT, Traits, Allocator>& s,                         CharT delim = CharT('"'), CharT escape = CharT('\\') ); | (2) | (since C++14) |
| template< class CharT, class Traits>  /\*unspecified\*/ quoted( std::basic_string_view<CharT, Traits> s,                         CharT delim = CharT('"'), CharT escape = CharT('\\') ); | (3) | (since C++17) |
| template< class CharT, class Traits, class Allocator >  /\*unspecified\*/ quoted( std::basic_string<CharT, Traits, Allocator>& s,                         CharT delim=CharT('"'), CharT escape=CharT('\\') ); | (4) | (since C++14) |
|  |  |  |

Allows insertion and extraction of quoted strings, such as the ones found in CSV or XML.

1-3) When used in an expression out << quoted(s, delim, escape), where `out` is an output stream with `char_type` equal to `CharT` and, for overloads (2,3), `traits_type` equal to `Traits`, behaves as a FormattedOutputFunction, which inserts into out a sequence of characters `seq` constructed as follows:a) First, the character delim is added to the sequence.b) Then every character from s, except if the next character to output equals delim or equals escape (as determined by the stream's traits_type::eq), then first appends an extra copy of escape.c) In the end, delim is appended to `seq` once more.

:   Then, if seq.size() < out.width(), adds out.width()-seq.size() copies of the fill character out.fill() either at the end of the sequence (if ios_base::left is set in out.flags()) or at the beginning of the sequence (in all other cases).

:   Finally, outputs each character from the resulting sequence as if by calling out.rdbuf()->sputn(seq, n), where n=std::max(out.width(), seq.size()) and out.width(0) to cancel the effects of std::setw, if any.

4) When used in an expression in >> quoted(s, delim, escape), where `in` is an input stream with `char_type` equal to `CharT` and `traits_type` equal to `Traits`, extracts characters from in, using std::basic_istream::operator>>, according to the following rules:a) If the first character extracted does not equal delim (as determined by the stream's `traits_type::eq`), then simply performs in >> s.b) Otherwise (if the first character is the delimiter):1) Turns off the skipws flag on the input stream.2) Empties the destination string by calling s.clear().3) Extracts characters from `in` and appends them to s, except that whenever an escape character is extracted, it is ignored and the next character is appended to s. Extraction stops when !in == true or when an unescaped delim character is found.4) Discards the final (unescaped) delim character.5) Restores the skipws flag on the input stream to its original value.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | the string to insert or extract |
| delim | - | the character to use as the delimiter, defaults to " |
| escape | - | the character to use as the escape character, defaults to \ |

### Return value

Returns an object of unspecified type such that the described behavior takes place.

### Exceptions

Throws std::ios_base::failure if operator>> or operator<< throws.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_quoted_string_io` | `201304L` | (C++14) | `std::quoted` |

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <sstream>
 
void default_delimiter()
{
    const std::string in = "std::quoted() quotes this string and embedded \"quotes\" too";
    std::stringstream ss;
    ss << std::quoted(in);
    std::string out;
    ss >> std::quoted(out);
 
    std::cout << "Default delimiter case:\n"
                 "read in     [" << in << "]\n"
                 "stored as   [" << ss.str() << "]\n"
                 "written out [" << out << "]\n\n";
}
 
void custom_delimiter()
{
    const char delim{'$'};
    const char escape{'%'};
 
    const std::string in = "std::quoted() quotes this string and embedded $quotes$ $too";
    std::stringstream ss;
    ss << std::quoted(in, delim, escape);
    std::string out;
    ss >> std::quoted(out, delim, escape);
 
    std::cout << "Custom delimiter case:\n"
                 "read in     [" << in << "]\n"
                 "stored as   [" << ss.str() << "]\n"
                 "written out [" << out << "]\n\n";
}
 
int main()
{
    default_delimiter();
    custom_delimiter();
}

```

Output:

```
Default delimiter case:
read in     [std::quoted() quotes this string and embedded "quotes" too]
stored as   ["std::quoted() quotes this string and embedded \"quotes\" too"]
written out [std::quoted() quotes this string and embedded "quotes" too]
 
Custom delimiter case:
read in     [std::quoted() quotes this string and embedded $quotes$ $too]
stored as   [$std::quoted() quotes this string and embedded %$quotes%$ %$too$]
written out [std::quoted() quotes this string and embedded $quotes$ $too]

```

### See also

|  |  |
| --- | --- |
| format(C++20) | stores formatted representation of the arguments in a new string   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/manip/quoted&oldid=159180>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 September 2023, at 22:46.