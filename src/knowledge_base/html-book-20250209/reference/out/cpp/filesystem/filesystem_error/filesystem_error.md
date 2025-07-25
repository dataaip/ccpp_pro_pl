# std::filesystem::filesystem_error::filesystem_error

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
| ****filesystem_error::filesystem_error**** | | | | |
| filesystem_error::operator= | | | | |
| filesystem_error::path1filesystem_error::path2 | | | | |
| filesystem_error::what | | | | |
| Inherited from std::system_error | | | | |
| system_error::code | | | | |

|  |  |  |
| --- | --- | --- |
| filesystem_error( const std::string& what_arg,                    std::error_code ec ); | (1) | (since C++17) |
| filesystem_error( const std::string& what_arg,  const std::filesystem::path& p1, std::error_code ec ); | (2) | (since C++17) |
| filesystem_error( const std::string& what_arg,  const std::filesystem::path& p1,                    const std::filesystem::path& p2, std::error_code ec ); | (3) | (since C++17) |
| filesystem_error( const filesystem_error& other ) noexcept; | (4) | (since C++17) |
|  |  |  |

Constructs a new `filesystem_error` object.

1-3) The error code is set to ec and optionally, the paths that were involved in the operation that resulted in the error, are set to p1 and p2. `what()` after construction returns a string that contains what_arg (assuming that it does not contain an embedded null character ). If either or both `path` arguments are not provided, a null `path` is used instead.4) Copy constructor. Initialize the contents with those of `other`. If \*this and other both have dynamic type `std::filesystem_error::filesystem_error` then std::strcmp(what(), other.what()) == 0.

### Parameters

|  |  |  |
| --- | --- | --- |
| what_arg | - | explanatory string |
| ec | - | error code for the specific operating system dependent error |
| p1, p2 | - | paths involved in the operation raising system error |
| other | - | another `filesystem_error` object to copy |

### Notes

Because copying `std::filesystem::filesystem_error` is not permitted to throw exceptions, the explanatory string is typically stored internally in a separately-allocated reference-counted storage. This is also why there is no constructor taking `std::string&&`: it would have to copy the content anyway.

Typical implementations also store `path` objects referenced by path1() and path2() in the reference-counted storage.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/filesystem_error/filesystem_error&oldid=156761>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 August 2023, at 10:19.