# std::filesystem::filesystem_error::what

From cppreference.com
< cpp‎ | filesystem‎ | filesystem error
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

filesystem_error

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| filesystem_error::filesystem_error | | | | |
| filesystem_error::operator= | | | | |
| filesystem_error::path1filesystem_error::path2 | | | | |
| ****filesystem_error::what**** | | | | |
| Inherited from std::system_error | | | | |
| system_error::code | | | | |

|  |  |  |
| --- | --- | --- |
| const char\* what() const noexcept override; |  | (since C++17) |
|  |  |  |

Returns an explanatory byte string. This explanatory string contains the explanatory string passed at the time of construction. Implementations are encouraged to include the pathnames of path1() and path2() in native format and the std::system_error::what() string inside the returned string as well.

### Parameters

(none)

### Return value

A C-stye explanatory byte string that contains the explanatory string passed at the time of construction.

### Example

Run this code

```
#include <cstdio>
#include <filesystem>
#include <iostream>
#include <string_view>
namespace fs = std::filesystem;
 
void explain(std::string_view note, fs::filesystem_error const& ex)
{
    std::cout << note << " exception:\n"
              << "what(): " << ex.what() << '\n'
              << "path1(): " << ex.path1() << ", path2(): "
              << ex.path2() << "\n\n";
}
 
int main()
{
    try
    {
        std::filesystem::rename("/dev", "/null");
    }
    catch(fs::filesystem_error const& ex)
    {
        explain("fs::rename()", ex);
    }
 
    for (auto const path : {"/bool", "/bin/cat", "/bin/mouse"})
        try
        {
            std::filesystem::create_directory(path);
        }
        catch(fs::filesystem_error const& ex)
        {
            explain("fs::create_directory()", ex);
        }
}

```

Possible output:

```
fs::rename() exception:
what(): filesystem error: cannot rename: Permission denied [/dev] [/null]
path1(): "/dev", path2(): "/null"
 
fs::create_directory() exception:
what(): filesystem error: cannot create directory: Permission denied [/bool]
path1(): "/bool", path2(): ""
 
fs::create_directory() exception:
what(): filesystem error: cannot create directory: File exists [/bin/cat]
path1(): "/bin/cat", path2(): ""
 
fs::create_directory() exception:
what(): filesystem error: cannot create directory: Read-only file system [/bin/mouse]
path1(): "/bin/mouse", path2(): ""

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/filesystem_error/what&oldid=136573>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 December 2021, at 14:46.