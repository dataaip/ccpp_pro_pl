# std::ios_base::iostate

From cppreference.com
< cpp‎ | io‎ | ios base
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

std::ios_base

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ios_base::ios_base | | | | |
| ios_base::~ios_base | | | | |
| ios_base::operator= | | | | |
| Formatting | | | | |
| ios_base::flags | | | | |
| ios_base::setf | | | | |
| ios_base::unsetf | | | | |
| ios_base::precision | | | | |
| ios_base::width | | | | |
| Locales | | | | |
| ios_base::imbue | | | | |
| ios_base::getloc | | | | |
| Internal extensible array | | | | |
| ios_base::xalloc | | | | |
| ios_base::iword | | | | |
| ios_base::pword | | | | |
| Miscellaneous | | | | |
| ios_base::register_callback | | | | |
| ios_base::sync_with_stdio | | | | |
| Member classes | | | | |
| ios_base::failure | | | | |
| ios_base::Init | | | | |
| Member types | | | | |
| ios_base::openmode | | | | |
| ios_base::fmtflags | | | | |
| ****ios_base::iostate**** | | | | |
| ios_base::seekdir | | | | |
| ios_base::event | | | | |
| ios_base::event_callback | | | | |

|  |  |  |
| --- | --- | --- |
| typedef /\*implementation defined\*/ iostate; |  |  |
| static constexpr iostate goodbit = 0; |  |  |
| static constexpr iostate badbit  = /\* implementation defined \*/  static constexpr iostate failbit = /\* implementation defined \*/ static constexpr iostate eofbit  = /\* implementation defined \*/ |  |  |
|  |  |  |

Specifies stream state flags. It is a BitmaskType, the following constants are defined:

|  |  |
| --- | --- |
| Constant | Explanation |
| ****goodbit**** | no error |
| ****badbit**** | irrecoverable stream error |
| ****failbit**** | input/output operation failed (formatting or extraction error) |
| ****eofbit**** | associated input sequence has reached end-of-file |

#### The eofbit

The eofbit is set by the following standard library functions:

- The string input function std::getline if it completes by reaching the end of the stream, as opposed to reaching the specified terminating character.
- The numeric input overloads of basic_istream::operator>> if the end of the stream was encountered while reading the next character, on Stage 2 of num_get::get processing. Depending on the parsing state, `failbit` may or may not be set at the same time: for example, int n; istringstream buf("1"); buf >> n; sets `eofbit`, but not `failbit`: the integer 1 was successfully parsed and stored in `n`. On the other hand, bool b; istringstream buf("tr"); buf >> boolalpha >> b; sets both `eofbit` and `failbit`: there was not enough characters to complete the parsing of the boolean true.
- The character extraction overloads of operator>>std::basic_istream, if the end of the stream is reached before the limit (if any) on the number of characters to be extracted.
- The std::get_time I/O manipulator and any of the std::time_get parsing functions: time_get::get, time_get::get_time, time_get::get_date, etc., if the end of the stream is reached before the last character needed to parse the expected date/time value was processed.
- The std::get_money I/O manipulator and money_get::get function, if the end of the stream is reached before the last character needed to parse the expected monetary value was processed.
- The basic_istream::sentry constructor, executed at the beginning of every formatted input function: unless the `skipws` bit is unset (e.g. by issuing std::noskipws), sentry reads and discards the leading whitespace characters. If the end of the input stream is reached during this operation, both `eofbit` and `failbit` are set, and no input takes place.
- The I/O manipulator std::ws, if it reaches the end of the stream while consuming whitespace (but, unlike the formatted input sentry, it does not set `failbit` in this case).
- The unformatted input functions basic_istream::read, basic_istream::get, basic_istream::peek, basic_istream::readsome, basic_istream::ignore, and basic_istream::getline, when reaching the end of the stream.
- The discard input function basic_istream::ignore, when reaching the end of the stream before reaching the specified delimiter character.
- The immediate input function basic_istream::readsome, if basic_streambuf::in_avail returns -1.

The following functions clear `eofbit` as a side-effect:

- basic_istream::putback
- basic_istream::unget
- basic_istream::seekg

Note that in nearly all situations, if eofbit is set, the failbit is set as well.

#### The failbit

The failbit is set by the following standard library functions:

- The basic_istream::sentry constructor, executed at the beginning of every input function, if either `eofbit` or `badbit` is already set on the stream, or if the end of stream is encountered while consuming leading whitespace.
- The basic_ostream::sentry constructor, executed at the beginning of every output function, under implementation-defined conditions.
- operator>>(std::basic_string<>) if the function extracts no characters from the input stream.
- operator>>(std::complex<>) if the function fails to extract a valid complex number.
- The character array and single character overloads of operator>> if they fail to extract any characters.
- The streambuf overload of basic_istream::operator>> if the streambuf argument is a null pointer or if no characters were inserted into the streambuf.
- The streambuf overload of basic_ostream::operator<< if the function inserts no characters.
- operator>>(std::bitset<>) if the function extracts no characters from the input stream.
- std::getline if the function extracts no characters or if it manages to extract basic_string::max_size characters from the input stream.
- The numeric, pointer, and boolean input overloads of basic_istream::operator>> (technically, the overloads of num_get::get they call), if the input cannot be parsed as a valid value or if the value parsed does not fit in the destination type.
- The time input manipulator std::get_time (technically, time_get::get it calls), if the input cannot be unambiguously parsed as a time value according to the given format string.
- The currency input manipulator std::get_money (technically, money_get::get it calls), if the input cannot be unambiguously parsed as a monetary value according to the locale rules.
- The extraction operators of all RandomNumberEngines, if bad input is encountered.
- The extraction operators of all RandomNumberDistributions, if bad input is encountered.
- The unformatted input functions basic_istream::get if they fails to extract any characters.
- basic_istream::getline, if it extracts no characters, if it fills in the provided buffer without encountering the delimiter, or if the provided buffer size is less than 1.
- basic_istream::read, if the end-of-file condition occurs on the input stream before all requested characters could be extracted.
- basic_istream::seekg on failure
- basic_ostream::tellp on failure
- The constructors of std::basic_fstream, std::basic_ifstream, and std::basic_ofstream that takes a filename argument, if the file cannot be opened.
- basic_fstream::open, basic_ifstream::open, and basic_ofstream::open if the file cannot be opened.
- basic_fstream::close, basic_ifstream::close, and basic_ofstream::close if the file cannot be closed.

#### The badbit

The badbit is set by the following standard library functions:

- basic_ostream::put if it fails to insert a character into the output stream, for any reason.
- basic_ostream::write if it fails to insert a character into the output stream, for any reason.
- Formatted output functions operator<<, std::put_money, and std::put_time, if they encounter the end of the output stream before completing output.
- basic_ios::init when called to initialize a stream with a null pointer for `rdbuf()`.
- basic_istream::putback and basic_istream::unget when called on a stream with a null `rdbuf()`.
- basic_ostream::operator<<(basic_streambuf\*) when a null pointer is passed as the argument.
- basic_istream::putback and basic_istream::unget if rdbuf()->sputbackc() or rdbuf()->sungetc() return traits::eof().
- basic_istream::sync, basic_ostream::flush, and every output function on a `unitbuf` output stream, if rdbuf()->pubsync() returns -1.
- Every stream I/O function if an exception is thrown by any member function of the associated stream buffer (e.g. `sbumpc()`, `xsputn()`, `sgetc()`, `overflow()`, etc).
- ios_base::iword and ios_base::pword on failure (e.g. failure to allocate memory).

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

The following table shows the value of basic_ios accessors (good(), fail(), etc.) for all possible combinations of ****ios_base::iostate**** flags:

|  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ****ios_base::iostate**** flags | | | `basic_ios` accessors | | | | | |
| `eofbit` | `failbit` | `badbit` | good() | fail() | bad() | eof() | operator bool | operator! |
| false | false | false | true | false | false | false | true | false |
| false | false | true | false | true | true | false | false | true |
| false | true | false | false | true | false | false | false | true |
| false | true | true | false | true | true | false | false | true |
| true | false | false | false | false | false | true | true | false |
| true | false | true | false | true | true | true | false | true |
| true | true | false | false | true | false | true | false | true |
| true | true | true | false | true | true | true | false | true |

|  |  |
| --- | --- |
| rdstate | returns state flags   (public member function of `std::basic_ios<CharT,Traits>`) |
| setstate | sets state flags   (public member function of `std::basic_ios<CharT,Traits>`) |
| clear | modifies state flags   (public member function of `std::basic_ios<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/ios_base/iostate&oldid=148278>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 February 2023, at 10:25.