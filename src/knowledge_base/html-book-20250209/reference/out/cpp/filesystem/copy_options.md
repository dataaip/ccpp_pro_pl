# std::filesystem::copy_options

From cppreference.com
< cpp‎ | filesystem
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | filesystem::space_info | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_type | | | | | | filesystem::file_time_type | | | | | | filesystem::perms | | | | | | filesystem::perm_options | | | | | | ****filesystem::copy_options**** | | | | | | filesystem::directory_options | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | filesystem::relativefilesystem::proximate | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<filesystem>` |  |  |
| enum class copy_options {      none = /\* unspecified \*/,      skip_existing = /\* unspecified \*/,      overwrite_existing = /\* unspecified \*/,      update_existing = /\* unspecified \*/,      recursive = /\* unspecified \*/,      copy_symlinks = /\* unspecified \*/,      skip_symlinks = /\* unspecified \*/,      directories_only = /\* unspecified \*/,      create_symlinks = /\* unspecified \*/,      create_hard_links = /\* unspecified \*/ }; |  | (since C++17) |
|  |  |  |

This type represents available options that control the behavior of the copy() and copy_file() function.

`copy_options` satisfies the requirements of BitmaskType (which means the bitwise operators operator&, operator|, operator^, operator~, operator&=, operator|=, and operator^= are defined for this type). `none` represents the empty bitmask; every other enumerator represents a distinct bitmask element.

### Member constants

At most one copy option in each of the following options groups may be present, otherwise the behavior of the copy functions is undefined.

| Member constant | Meaning |
| --- | --- |
| options controlling copy_file() when the file already exists | |
| `none` | Report an error (default behavior). |
| `skip_existing` | Keep the existing file, without reporting an error. |
| `overwrite_existing` | Replace the existing file. |
| `update_existing` | Replace the existing file only if it is older than the file being copied. |
| options controlling the effects of copy() on subdirectories | |
| `none` | Skip subdirectories (default behavior). |
| `recursive` | Recursively copy subdirectories and their content. |
| options controlling the effects of copy() on symbolic links | |
| `none` | Follow symlinks (default behavior). |
| `copy_symlinks` | Copy symlinks as symlinks, not as the files they point to. |
| `skip_symlinks` | Ignore symlinks. |
| options controlling the kind of copying copy() does | |
| `none` | Copy file content (default behavior). |
| `directories_only` | Copy the directory structure, but do not copy any non-directory files. |
| `create_symlinks` | Instead of creating copies of files, create symlinks pointing to the originals. Note: the source path must be an absolute path unless the destination path is in the current directory. |
| `create_hard_links` | Instead of creating copies of files, create hardlinks that resolve to the same files as the originals. |

### Example

Run this code

```
#include <cstdlib>
#include <filesystem>
#include <fstream>
#include <iostream>
namespace fs = std::filesystem;
 
int main()
{
    fs::create_directories("sandbox/dir/subdir");
    std::ofstream("sandbox/file1.txt").put('a');
    fs::copy("sandbox/file1.txt", "sandbox/file2.txt"); // copy file
    fs::copy("sandbox/dir", "sandbox/dir2"); // copy directory (non-recursive)
    const auto copyOptions = fs::copy_options::update_existing
                           | fs::copy_options::recursive
                           | fs::copy_options::directories_only
                           ;
    fs::copy("sandbox", "sandbox_copy", copyOptions); 
    static_cast<void>(std::system("tree"));
    fs::remove_all("sandbox");
    fs::remove_all("sandbox_copy");
}

```

Possible output:

```
.
├── sandbox
│   ├── dir
│   │   └── subdir
│   ├── dir2
│   ├── file1.txt
│   └── file2.txt
└── sandbox_copy
    ├── dir
    │   └── subdir
    └── dir2
 
8 directories, 2 files

```

### See also

|  |  |
| --- | --- |
| copy(C++17) | copies files or directories   (function) |
| copy_file(C++17) | copies file contents   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/copy_options&oldid=157912>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 September 2023, at 01:42.