# std::filesystem::directory_entry::exists

From cppreference.com
< cpp‎ | filesystem‎ | directory entry
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

std::filesystem::directory_entry

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| directory_entry::directory_entry | | | | |
| Modifiers | | | | |
| directory_entry::operator= | | | | |
| directory_entry::assign | | | | |
| directory_entry::replace_filename | | | | |
| directory_entry::refresh | | | | |
| Observers | | | | |
| directory_entry::pathdirectory_entry::operator const path& | | | | |
| ****directory_entry::exists**** | | | | |
| directory_entry::is_block_file | | | | |
| directory_entry::is_character_file | | | | |
| directory_entry::is_directory | | | | |
| directory_entry::is_fifo | | | | |
| directory_entry::is_other | | | | |
| directory_entry::is_regular_file | | | | |
| directory_entry::is_socket | | | | |
| directory_entry::is_symlink | | | | |
| directory_entry::file_size | | | | |
| directory_entry::hard_link_count | | | | |
| directory_entry::last_write_time | | | | |
| directory_entry::statusdirectory_entry::symlink_status | | | | |
| directory_entry::operator==directory_entry::operator!=directory_entry::operator<directory_entry::operator>directory_entry::operator<=directory_entry::operator>=directory_entry::operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | |
| Non-member functions | | | | |
| operator<< | | | | |

|  |  |  |
| --- | --- | --- |
| bool exists() const; | (1) | (since C++17) |
| bool exists( std::error_code& ec ) const noexcept; | (2) | (since C++17) |
|  |  |  |

Checks whether the pointed-to object exists. Effectively returns:

1) std::filesystem::exists(status()),2) std::filesystem::exists(status(ec)).

Note that `status()` follows symlinks to their targets.

### Parameters

|  |  |  |
| --- | --- | --- |
| ec | - | out-parameter for error reporting in the non-throwing overload |

### Return value

true if the referred-to filesystem object exists.

### Exceptions

Any overload not marked `noexcept` may throw std::bad_alloc if memory allocation fails.

1) Throws std::filesystem::filesystem_error on underlying OS API errors, constructed with p as the first path argument and the OS error code as the error code argument.2) Sets a std::error_code& parameter to the OS API error code if an OS API call fails, and executes ec.clear() if no errors occur.

### Example

Run this code

```
#include <filesystem>
#include <iostream>
 
int main()
{
    for (auto const str:
    {
        "/usr/bin/cat",
        "/usr/bin/mouse",
        "/usr/bin/python",
        "/usr/bin/bison",
        "/usr/bin/yacc",
        "/usr/bin/c++",
    })
    {
        std::filesystem::directory_entry entry{str};
 
        std::cout << "directory entry " << entry
                  << (entry.exists() ? " exists\n" : " does not exist\n");
    }
}

```

Possible output:

```
// Output on a POSIX system:
directory entry "/usr/bin/cat" exist
directory entry "/usr/bin/mouse" does not exist
directory entry "/usr/bin/python" exists
directory entry "/usr/bin/bison" exists
directory entry "/usr/bin/yacc" does not exist
directory entry "/usr/bin/c++" exists

```

### See also

|  |  |
| --- | --- |
| exists(C++17) | checks whether path refers to existing file system object   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/directory_entry/exists&oldid=158261>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 September 2023, at 13:29.