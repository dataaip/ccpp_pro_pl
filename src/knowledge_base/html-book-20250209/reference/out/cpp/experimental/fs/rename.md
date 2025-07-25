# std::experimental::filesystem::rename

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute filesystem::system_complete | | | | | | filesystem::canonical | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | ****filesystem::rename**** | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | | filesystem::temp_directory_path | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/filesystem>` |  |  |
| void rename( const path& old_p, const path& new_p );  void rename( const path& old_p, const path& new_p, std::error_code& ec ); |  | (filesystem TS) |
|  |  |  |

Moves or renames the filesystem object identified by old_p to new_p as if by the POSIX rename:

- If old_p is a non-directory file, then new_p must be one of:

:   - the same file as old_p or a hardlink to it: nothing is done in this case.
    - existing non-directory file: new_p is first deleted, then, without allowing other processes to observe new_p as deleted, the pathname new_p is linked to the file and old_p is unlinked from the file. Write permissions are required to both the directory that contains old_p and the directory that contains new_p.
    - non-existing file in an existing directory: The pathname new_p is linked to the file and old_p is unlinked from the file. Write permissions are required to both the directory that contains old_p and the directory that contains new_p.

- If old_p is a directory, then new_p must be one of:

:   - the same directory as old_p or a hardlink to it: nothing is done in this case.
    - existing directory: new_p is deleted if empty on POSIX systems, but this may be an error on other systems. If not an error, then new_p is first deleted, then, without allowing other processes to observe new_p as deleted, the pathname new_p is linked to the directory and old_p is unlinked from the directory. Write permissions are required to both the directory that contains old_p and the directory that contains new_p.
    - non-existing directory, not ending with a directory separator, and whose parent directory exists: The pathname new_p is linked to the directory and old_p is unlinked from the directory. Write permissions are required to both the directory that contains old_p and the directory that contains new_p.

- Symlinks are not followed: if old_p is a symlink, it is itself renamed, not its target. If new_p is an existing symlink, it is itself erased, not its target.

Rename fails if

- new_p ends with dot or with dot-dot.
- new_p names a non-existing directory ending with a directory separator.
- old_p is a directory which is an ancestor of new_p.

### Parameters

|  |  |  |
| --- | --- | --- |
| old_p | - | path to move or rename |
| new_p | - | target path for the move/rename operation |
| ec | - | out-parameter for error reporting in the non-throwing overload |

### Return value

(none)

### Exceptions

The overload that does not take an error_code& parameter throws filesystem_error on underlying OS API errors, constructed with old_p as the first argument, new_p as the second argument, and the OS error code as the error code argument. std::bad_alloc may be thrown if memory allocation fails. The overload taking an error_code& parameter sets it to the OS API error code if an OS API call fails, and executes ec.clear() if no errors occur. This overload hasnoexcept specification:noexcept

### Example

Run this code

```
#include <experimental/filesystem>
#include <fstream>
#include <iostream>
namespace fs = std::experimental::filesystem;
 
int main()
{
    fs::path p = fs::current_path() / "sandbox";
    fs::create_directories(p/"from");
    std::ofstream(p/"from/file1.txt").put('a');
    fs::create_directory(p/"to");
 
//  fs::rename(p/"from/file1.txt", p/"to/"); // error: to is a directory
    fs::rename(p/"from/file1.txt", p/"to/file2.txt"); // OK
//  fs::rename(p/"from", p/"to"); // error: to is not empty
    fs::rename(p/"from", p/"to/subdir"); // OK
 
    fs::remove_all(p);
}

```

### See also

|  |  |
| --- | --- |
| rename | renames a file   (function) |
| removeremove_all | removes a file or empty directory removes a file or directory and all its contents, recursively   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/fs/rename&oldid=158947>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 September 2023, at 22:14.