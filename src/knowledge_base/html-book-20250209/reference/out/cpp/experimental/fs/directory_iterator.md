# std::experimental::filesystem::directory_iterator

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

Filesystem library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | ****filesystem::directory_iterator**** | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::space_info | | | | | | filesystem::file_type | | | | | | filesystem::perms | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | | filesystem::file_time_type | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute filesystem::system_complete | | | | | | filesystem::canonical | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | | filesystem::temp_directory_path | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

****directory_iterator****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| directory_iterator::directory_iterator | | | | |
| directory_iterator::operator\*directory_iterator::operator-> | | | | |
| directory_iterator::operator= | | | | |
| directory_iterator::incrementdirectory_iterator::operator++ | | | | |
| Non-member functions | | | | |
| begin(directory_iterator)end(directory_iterator) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/filesystem>` |  |  |
| class directory_iterator; |  | (filesystem TS) |
|  |  |  |

`directory_iterator` is a LegacyInputIterator that iterates over the directory_entry elements of a directory (but does not visit the subdirectories). The iteration order is unspecified, except that each directory entry is visited only once. The special pathnames dot and dot-dot are skipped.

If the `directory_iterator` is advanced past the last directory entry, it becomes equal to the default-constructed iterator, also known as the end iterator. Two end iterators are always equal, dereferencing or incrementing the end iterator is undefined behavior.

If a file or a directory is deleted or added to the directory tree after the directory iterator has been created, it is unspecified whether the change would be observed through the iterator.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `value_type` | `filesystem::directory_entry` |
| `difference_type` | `std::ptrdiff_t` |
| `pointer` | `const filesystem::directory_entry*` |
| `reference` | `const filesystem::directory_entry&` |
| `iterator_category` | `std::input_iterator_tag` |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a directory iterator   (public member function) |
| (destructor) | default destructor   (public member function) |
| operator= | assigns contents   (public member function) |
| operator\*operator-> | accesses the pointed-to entry   (public member function) |
| incrementoperator++ | advances to the next entry   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| filesystem::begin(filesystem::directory_iterator)filesystem::end(filesystem::directory_iterator) | range-based for loop support   (function) |

Additionally, operator== and operator!= are provided, either as members or as non-members, as required by LegacyInputIterator.

### Example

Run this code

```
#include <experimental/filesystem>
#include <fstream>
#include <iostream>
namespace fs = std::experimental::filesystem;
 
int main()
{
    fs::create_directories("sandbox/a/b");
    std::ofstream{"sandbox/file1.txt"};
    std::ofstream{"sandbox/file2.txt"};
    for (const fs::directory_entry& entry : fs::directory_iterator{"sandbox"})
        std::cout << entry << '\n';
    fs::remove_all("sandbox");
}

```

Possible output:

```
"sandbox/a"
"sandbox/file1.txt"
"sandbox/file2.txt"

```

### See also

|  |  |
| --- | --- |
| recursive_directory_iterator | an iterator to the contents of a directory and its subdirectories   (class) |
| directory_options | options for iterating directory contents   (enum) |
| directory_entry | a directory entry   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/fs/directory_iterator&oldid=154836>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 July 2023, at 00:48.