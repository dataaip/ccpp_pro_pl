# std::experimental::filesystem::path::path

From cppreference.com
< cpp‎ | experimental‎ | fs‎ | path
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Filesystem library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::space_info | | | | | | filesystem::file_type | | | | | | filesystem::perms | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | | filesystem::file_time_type | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute filesystem::system_complete | | | | | | filesystem::canonical | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | | filesystem::temp_directory_path | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

path

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****path::path**** | | | | | | path::~path | | | | | | path::operator= | | | | | | path::assign | | | | | | path::appendoperator /= | | | | | | path::concatoperator += | | | | | | path::clear | | | | | | path::make_preferred | | | | | | path::remove_filename | | | | | | path::replace_filename | | | | | | path::replace_extension | | | | | | path::swap | | | | | | path::compare | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::c_strpath::nativeoperator string_type | | | | | | path::stringpath::u8stringpath::u16stringpath::u32stringpath::wstring | | | | | | path::generic_stringpath::generic_u8stringpath::generic_u16stringpath::generic_u32stringpath::generic_wstring | | | | | | path::beginpath::end | | | | | |
| Path decomposition | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::root_name | | | | | | path::root_directory | | | | | | path::root_path | | | | | | path::relative_path | | | | | | path::parent_path | | | | | | path::filename | | | | | | path::stem | | | | | | path::extension | | | | | | path::empty | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::has_root_pathpath::has_root_namepath::has_root_directorypath::has_relative_pathpath::has_parent_pathpath::has_filenamepath::has_stempath::has_extension | | | | | | path::is_absolutepath::is_relative | | | | | |
| Non-member functions | | | | |
| swap(path) | | | | |
| operator==operator!=operator<operator<=operator>operator>= | | | | |
| operator/ | | | | |
| operator<<operator>> | | | | |
| u8path | | | | |

|  |  |  |
| --- | --- | --- |
| path(); | (1) | (filesystem TS) |
| path( const path& p ); | (2) | (filesystem TS) |
| path( path&& p ); | (3) | (filesystem TS) |
| template< class Source >  path( const Source& source ); | (4) | (filesystem TS) |
| template< class InputIt >  path( InputIt first, InputIt last ); | (5) | (filesystem TS) |
| template< class Source >  path( const Source& source, const std::locale& loc ); | (6) | (filesystem TS) |
| template< class InputIt >  path( InputIt first, InputIt last, const std::locale& loc ); | (7) | (filesystem TS) |
|  |  |  |

Constructs a new `path` object.

1) Constructs an empty path.2) Copy constructor. Constructs a copy of p.3) Move constructor. Constructs a copy of p, p is left in valid but unspecified state.4,5) Constructs the path from a character sequence provided by source (4), which is a pointer or an input iterator to a null-terminated character/wide character sequence or an std::basic_string, or represented as a pair of input iterators first, last) (5). Any of the four character types char, char16_t, char32_t, wchar_t is allowed, and the method of conversion to the native character set depends on the character type used by source.

:   - If the source character type is char, the encoding of the source is assumed to be the native narrow encoding (so no conversion takes place on POSIX systems).
    - If the source character type is char16_t, conversion from UTF-16 to native filesystem encoding is used.
    - If the source character type is char32_t, conversion from UTF-32 to native filesystem encoding is used.
    - If the source character type is wchar_t, the input is assumed to be the native wide encoding (so no conversion takes places on Windows).

6,7) Constructs the path from a character sequence provided by source (6), which is a pointer or an input iterator to a null-terminated character sequence or an [std::string, or represented as a pair of input iterators first, last) (7). The only character type allowed is char. Uses loc to perform the character encoding conversion. If `value_type` is wchar_t, converts from to wide using the [std::codecvt<wchar_t, char, std::mbstate_t> facet of loc. Otherwise, first converts to wide using the std::codecvt<wchar_t, char, std::mbstate_t> facet and then converts to filesystem native character type using std::codecvt<wchar_t, value_type> facet of loc.

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | a path to copy |
| source | - | a std::basic_string, pointer to a null-terminated character string, or an input iterator with a character value type that points to a null-terminated character sequence (the character type must be char for overload (6) |
| first, last | - | pair of LegacyInputIterators that specify a UTF-8 encoded character sequence |
| loc | - | locale that defines encoding conversion to use |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |
| -The value type of `InputIt` must be one of the four character types char, wchar_t, char16_t and char32_t to use the overload (5). | | |
| -The value type of `InputIt` must be char to use the overload (7). | | |

### Exceptions

1,2) (none)3)noexcept specification:noexcept4-7) (none)

### Notes

For portable pathname generation from Unicode strings, see u8path.

### Example

Run this code

```
#include <experimental/filesystem>
#include <iostream>
namespace fs = std::experimental::filesystem;
 
int main()
{
    fs::path p1 = "/usr/lib/sendmail.cf"; // portable format
    fs::path p2 = "C:\\users\\abcdef\\AppData\\Local\\Temp\\"; // native format
    fs::path p3 = L"D:/猫.txt"; // wide string
 
    std::cout << "p1 = " << p1 << '\n'
              << "p2 = " << p2 << '\n'
              << "p3 = " << p3 << '\n';
}

```

Output:

```
p1 = "/usr/lib/sendmail.cf"
p2 = "C:\users\abcdef\AppData\Local\Temp\"
p3 = "D:/猫.txt"

```

### See also

|  |  |
| --- | --- |
| u8path | creates a `path` from a UTF-8 encoded source   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/fs/path/path&oldid=157722>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 September 2023, at 23:47.