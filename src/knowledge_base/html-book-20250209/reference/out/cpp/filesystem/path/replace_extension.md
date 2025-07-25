# std::filesystem::path::replace_extension

From cppreference.com
< cpp‎ | filesystem‎ | path
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

Filesystem library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | filesystem::space_info | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_type | | | | | | filesystem::file_time_type | | | | | | filesystem::perms | | | | | | filesystem::perm_options | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | filesystem::relativefilesystem::proximate | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

std::filesystem::path

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member constants | | | | |
| path::native_formatpath::generic_formatpath::auto_format | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::path | | | | | | path::~path | | | | | | path::operator= | | | | | | path::assign | | | | | | path::appendpath::operator/= | | | | | | path::concatpath::operator+= | | | | | | path::clear | | | | | | path::make_preferred | | | | | | path::remove_filename | | | | | | path::replace_filename | | | | | | ****path::replace_extension**** | | | | | | path::swap | | | | | | path::compare | | | | | | path::beginpath::end | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::c_strpath::nativepath::operator string_type | | | | | | path::stringpath::u8stringpath::u16stringpath::u32stringpath::wstring | | | | | | path::generic_stringpath::generic_u8stringpath::generic_u16stringpath::generic_u32stringpath::generic_wstring | | | | | | path::lexically_normalpath::lexically_relativepath::lexically_proximate | | | | | |  | | | | | |
| Path decomposition | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::root_name | | | | | | path::root_directory | | | | | | path::root_path | | | | | | path::relative_path | | | | | | path::parent_path | | | | | | path::filename | | | | | | path::stem | | | | | | path::extension | | | | | | path::empty | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::has_root_pathpath::has_root_namepath::has_root_directorypath::has_relative_pathpath::has_parent_pathpath::has_filenamepath::has_stempath::has_extension | | | | | | path::is_absolutepath::is_relative | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator/ | | | | | | operator<<operator>> | | | | | | swap(std::filesystem::path) | | | | | | hash_value | | | | | | u8path | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | hash<std::filesystem::path> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | formatter<std::filesystem::path>(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| path& replace_extension( const path& replacement = path() ); |  | (since C++17) |
|  |  |  |

Replaces the extension with replacement or removes it when the default value of replacement is used.

Firstly, if this path has an extension(), it is removed from the generic-format view of the pathname.

Then, a dot character is appended to the generic-format view of the pathname, if replacement is not empty and does not begin with a dot character.

Then replacement is appended as if by operator+=(replacement).

### Parameters

|  |  |  |
| --- | --- | --- |
| replacement | - | the extension to replace with |

### Return value

\*this

### Exceptions

May throw implementation-defined exceptions.

### Notes

The type of replacement is std::filesystem::path even though it is not intended to represent an object on the file system in order to correctly account for the filesystem character encoding.

### Example

Run this code

```
#include <filesystem>
#include <iomanip>
#include <iostream>
#include <utility>
 
int main()
{
    const int width1{18}, width2{11}; // columns' width
 
    std::cout << std::left << std::setw(width1) << "Path:"
              << std::setw(width2) << "Ext:" << "Result:\n";
    for (const auto& [p, e] : {
            std::make_pair("/foo/bar.jpg", ".png"),
            {"/foo/bar.jpg", "png"},
            {"/foo/bar.jpg", "."},
            {"/foo/bar.jpg", ""},
            {"/foo/bar.", "png"},
            {"/foo/bar", ".png"},
            {"/foo/bar", "png"},
            {"/foo/bar", "."},
            {"/foo/bar", ""},
            {"/foo/.", ".png"},
            {"/foo/.", "png"},
            {"/foo/.", "."},
            {"/foo/.", ""},
            {"/foo/", ".png"},
            {"/foo/", "png"}})
    {
        std::filesystem::path path{p}, ext{e};
        std::cout << std::setw(width1) << path << std::setw(width2) << ext;
        path.replace_extension(ext);
        std::cout << path << '\n';
    }
}

```

Output:

```
Path:             Ext:       Result:
"/foo/bar.jpg"    ".png"     "/foo/bar.png"
"/foo/bar.jpg"    "png"      "/foo/bar.png"
"/foo/bar.jpg"    "."        "/foo/bar."
"/foo/bar.jpg"    ""         "/foo/bar"
"/foo/bar."       "png"      "/foo/bar.png"
"/foo/bar"        ".png"     "/foo/bar.png"
"/foo/bar"        "png"      "/foo/bar.png"
"/foo/bar"        "."        "/foo/bar."
"/foo/bar"        ""         "/foo/bar"
"/foo/."          ".png"     "/foo/..png"
"/foo/."          "png"      "/foo/..png"
"/foo/."          "."        "/foo/.."
"/foo/."          ""         "/foo/."
"/foo/"           ".png"     "/foo/.png"
"/foo/"           "png"      "/foo/.png"

```

### See also

|  |  |
| --- | --- |
| extension | returns the file extension path component   (public member function) |
| filename | returns the filename path component   (public member function) |
| stem | returns the stem path component (filename without the final extension)   (public member function) |
| has_extension | checks if the corresponding path element is not empty   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/path/replace_extension&oldid=160020>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 October 2023, at 12:27.