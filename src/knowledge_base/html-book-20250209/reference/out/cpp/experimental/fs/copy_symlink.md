# std::experimental::filesystem::copy_symlink

From cppreference.com
< cpp‎ | experimental‎ | fs
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute filesystem::system_complete | | | | | | filesystem::canonical | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | ****filesystem::copy_symlink**** | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | | filesystem::temp_directory_path | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/filesystem>` |  |  |
| void copy_symlink( const path& from, const path& to ); | (1) | (filesystem TS) |
| void copy_symlink( const path& from, const path& to,                     error_code& ec ); | (2) | (filesystem TS) |
|  |  |  |

Copies a symlink to another location.

1) Effectively calls f(read_symlink(from), to) where `f` is create_symlink() or create_directory_symlink depending on whether from resolves to a file or directory.2) Effectively calls f(read_symlink(from, ec), to, ec) where `f` is create_symlink() or create_directory_symlink depending on whether from resolves to a file or directory.

### Parameters

|  |  |  |
| --- | --- | --- |
| from | - | path to a symbolic link to copy |
| to | - | destination path of the new symlink |
| ec | - | out-parameter for error reporting in the non-throwing overload |

### Return value

(none)

### Exceptions

The overload that does not take an error_code& parameter throws filesystem_error on underlying OS API errors, constructed with from as the first argument, to as the second argument, and the OS error code as the error code argument. std::bad_alloc may be thrown if memory allocation fails. The overload taking an error_code& parameter sets it to the OS API error code if an OS API call fails, and executes ec.clear() if no errors occur. This overload hasnoexcept specification:noexcept

### See also

|  |  |
| --- | --- |
| copy | copies files or directories   (function) |
| copy_file | copies file contents   (function) |
| create_symlinkcreate_directory_symlink | creates a symbolic link   (function) |
| read_symlink | obtains the target of a symbolic link   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/fs/copy_symlink&oldid=154825>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 July 2023, at 00:03.