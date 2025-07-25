# std::basic_istream<CharT,Traits>::get

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
| ****basic_istream::get**** | | | | |
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
| int_type get(); | (1) |  |
| basic_istream& get( char_type& ch ); | (2) |  |
| basic_istream& get( char_type\* s, std::streamsize count ); | (3) |  |
| basic_istream& get( char_type\* s, std::streamsize count, char_type delim ); | (4) |  |
| basic_istream& get( basic_streambuf& strbuf ); | (5) |  |
| basic_istream& get( basic_streambuf& strbuf, char_type delim ); | (6) |  |
|  |  |  |

Extracts character or characters from stream.

All versions behave as UnformattedInputFunctions. After constructing and checking the sentry object, these functions perform the following:

1) Reads one character and returns it if available. Otherwise, returns Traits::eof() and sets failbit and eofbit.2) Reads one character and stores it to ch if available. Otherwise, leaves ch unmodified and sets failbit and eofbit. Note that this function is not overloaded on the types signed char and unsigned char, unlike the formatted character input operator>>.3) Same as get(s, count, widen('\n')), that is, reads at most std::max(0, count - 1) characters and stores them into character string pointed to by s until '\n' is found.4) Reads characters and stores them into the successive locations of the character array whose first element is pointed to by s. Characters are extracted and stored until any of the following occurs:

- count is less than 1 or count - 1 characters have been stored.
- end of file condition occurs in the input sequence (setstate(eofbit) is called).
- the next available input character c equals delim, as determined by Traits::eq(c, delim). This character is not extracted (unlike `getline()`).
 In any case, if count > 0, a null character (CharT() is stored in the next successive location of the array.5) Same as get(strbuf, widen('\n')), that is, reads available characters and inserts them to the given basic_streambuf object until '\n' is found.6) Reads characters and inserts them to the output sequence controlled by the given basic_streambuf object. Characters are extracted and inserted into strbuf until any of the following occurs:

- end of file condition occurs in the input sequence.
- inserting into the output sequence fails (in which case the character that could not be inserted, is not extracted).
- the next available input character c equals delim, as determined by Traits::eq(c, delim). This character is not extracted.
- an exception occurs (in which case the exception is caught and not rethrown).

If no characters were extracted, calls setstate(failbit).

All versions set the value of gcount() to the number of characters extracted.

### Parameters

|  |  |  |
| --- | --- | --- |
| ch | - | reference to the character to write the result to |
| s | - | pointer to the character string to store the characters to |
| count | - | size of character string pointed to by s |
| delim | - | delimiting character to stop the extraction at. It is not extracted and not stored |
| strbuf | - | stream buffer to read the content to |

### Return value

1) The extracted character or Traits::eof().2-6) \*this

### Exceptions

failure if an error occurred (the error state flag is not goodbit) and exceptions() is set to throw for that state.

If an internal operation throws an exception, it is caught and badbit is set. If exceptions() is set for `badbit`, the exception is rethrown.

### Example

Run this code

```
#include <iostream>
#include <sstream>
 
int main()
{
    std::istringstream s1("Hello, world.");
    char c1 = s1.get(); // reads 'H'
    std::cout << "after reading " << c1 << ", gcount() == " <<  s1.gcount() << '\n';
 
    char c2;
    s1.get(c2);         // reads 'e'
    char str[5];
    s1.get(str, 5);     // reads "llo,"
    std::cout << "after reading " << str << ", gcount() == " <<  s1.gcount() << '\n';
 
    std::cout << c1 << c2 << str;
    s1.get(*std::cout.rdbuf()); // reads the rest, not including '\n'
    std::cout << "\nAfter the last get(), gcount() == " << s1.gcount() << '\n';
}

```

Output:

```
after reading H, gcount() == 1
after reading llo,, gcount() == 4
Hello, world.
After the last get(), gcount() == 7

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 370 | C++98 | the effect of overload (5) was get(s, count, widen('\n')), which is the effect of overload (3) | corrected to get(strbuf, widen('\n')) |
| LWG 531 | C++98 | overloads (3,4) could not handle the case where count is non-positive | no character is extracted in this case |

### See also

|  |  |
| --- | --- |
| read | extracts blocks of characters   (public member function) |
| operator>> | extracts formatted data   (public member function) |
| operator>>(std::basic_istream) | extracts characters and character arrays   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_istream/get&oldid=158516>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 September 2023, at 00:01.