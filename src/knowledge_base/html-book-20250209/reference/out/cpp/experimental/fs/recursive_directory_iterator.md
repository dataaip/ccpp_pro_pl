# std::experimental::filesystem::recursive_directory_iterator

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | ****filesystem::recursive_directory_iterator**** | | | | | | filesystem::file_status | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::space_info | | | | | | filesystem::file_type | | | | | | filesystem::perms | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | | filesystem::file_time_type | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute filesystem::system_complete | | | | | | filesystem::canonical | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | | filesystem::temp_directory_path | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

****recursive_directory_iterator****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| recursive_directory_iterator::recursive_directory_iterator | | | | |
| recursive_directory_iterator::operator\*recursive_directory_iterator::operator-> | | | | |
| recursive_directory_iterator::options | | | | |
| recursive_directory_iterator::depth | | | | |
| recursive_directory_iterator::recursion_pending | | | | |
| recursive_directory_iterator::operator= | | | | |
| recursive_directory_iterator::incrementrecursive_directory_iterator::operator++ | | | | |
| recursive_directory_iterator::pop | | | | |
| recursive_directory_iterator::disable_recursion_pending | | | | |
| Non-member functions | | | | |
| begin(recursive_directory_iterator)end(recursive_directory_iterator) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/filesystem>` |  |  |
| class recursive_directory_iterator; |  | (filesystem TS) |
|  |  |  |

`recursive_directory_iterator` is a LegacyInputIterator that iterates over the directory_entry elements of a directory, and, recursively, over the entries of all subdirectories. The iteration order is unspecified, except that each directory entry is visited only once.

By default, symlinks are not followed, but this can be enabled by specifying the directory option follow_directory_symlink at construction time.

The special pathnames dot and dot-dot are skipped.

If the `recursive_directory_iterator` is advanced past the last directory entry of the top-level directory, it becomes equal to the default-constructed iterator, also known as the end iterator. Two end iterators are always equal, dereferencing or incrementing the end iterator is undefined behavior.

If a file or a directory is deleted or added to the directory tree after the recursive directory iterator has been created, it is unspecified whether the change would be observed through the iterator.

If the directory structure contains cycles, the end iterator may be unreachable.

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
| (constructor) | constructs a recursive directory iterator   (public member function) |
| (destructor) | default destructor   (public member function) |
| Observers | |
| operator\*operator-> | accesses the pointed-to entry   (public member function) |
| options | returns the currently active options that affect the iteration   (public member function) |
| depth | returns the current recursion depth   (public member function) |
| recursion_pending | checks whether the recursion is disabled for the current directory   (public member function) |
| Modifiers | |
| operator= | assigns contents   (public member function) |
| incrementoperator++ | advances to the next entry   (public member function) |
| pop | moves the iterator one level up in the directory hierarchy   (public member function) |
| disable_recursion_pending | disables recursion until the next increment   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| filesystem::begin(filesystem::recursive_directory_iterator)filesystem::end(filesystem::recursive_directory_iterator) | range-based for loop support   (function) |

Additionally, `operator==` and `operator!=` are provided, either as members or as non-members, as required by LegacyInputIterator.

### Notes

A `recursive_directory_iterator` typically holds a reference-counted **pointer** (to satisfy shallow-copy semantics of LegacyInputIterator) to an implementation object, which holds:

- a container (such as std::vector) of non-recursive directory_iterators that forms the recursion stack.
- the recursion depth counter (accessible with depth()).
- the directory options used at construction (accessible with options()).
- the pending recursion flag (accessible with recursion_pending(), may be combined with the directory options to save space).

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
    std::ofstream("sandbox/file1.txt");
    fs::create_symlink("a", "sandbox/syma");
    for (const fs::directory_entry& entry : fs::recursive_directory_iterator("sandbox"))
        std::cout << entry << '\n';
    fs::remove_all("sandbox");
}

```

Possible output:

```
"sandbox/a"
"sandbox/a/b"
"sandbox/file1.txt"
"sandbox/syma"

```

### See also

|  |  |
| --- | --- |
| directory_iterator | an iterator to the contents of the directory   (class) |
| directory_entry | a directory entry   (class) |
| directory_options | options for iterating directory contents   (enum) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/fs/recursive_directory_iterator&oldid=154916>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 July 2023, at 06:04.