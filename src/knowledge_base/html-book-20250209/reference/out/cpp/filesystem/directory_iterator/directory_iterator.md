# std::filesystem::directory_iterator::directory_iterator

From cppreference.com
< cpp‎ | filesystem‎ | directory iterator
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

std::filesystem::directory_iterator

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****directory_iterator::directory_iterator**** | | | | |
| directory_iterator::operator\*directory_iterator::operator-> | | | | |
| directory_iterator::operator= | | | | |
| incrementoperator++ | | | | |
| Non-member functions | | | | |
| begin(std::filesystem::directory_iterator)end(std::filesystem::directory_iterator) | | | | |

|  |  |  |
| --- | --- | --- |
| directory_iterator() noexcept; | (1) | (since C++17) |
| explicit directory_iterator( const std::filesystem::path& p ); | (2) | (since C++17) |
| directory_iterator( const std::filesystem::path& p,                      std::filesystem::directory_options options ); | (3) | (since C++17) |
| directory_iterator( const std::filesystem::path& p, std::error_code& ec ); | (4) | (since C++17) |
| directory_iterator( const std::filesystem::path& p,  std::filesystem::directory_options options, std::error_code& ec ); | (5) | (since C++17) |
| directory_iterator( const directory_iterator& other ) = default; | (6) | (since C++17) |
| directory_iterator( directory_iterator&& other ) = default; | (7) | (since C++17) |
|  |  |  |

Constructs a new directory iterator.

1) Constructs the end iterator.2) Constructs a directory iterator that refers to the first directory entry of a directory identified by `p`. If `p` refers to a non-existing file or not a directory, throws std::filesystem::filesystem_error.3) Same as (2), but if std::filesystem::directory_options::skip_permission_denied is set in `options` and construction encounters a permissions denied error, constructs the end iterator and does not report an error.4) Constructs a directory iterator that refers to the first directory entry of a directory identified by `p`. If `p` refers to a non-existing file or not a directory, returns the end iterator and sets `ec`.5) Same as (4), but if std::filesystem::directory_options::skip_permission_denied is set in `options` and construction encounters a permissions denied error, constructs the end iterator and does not report an error.6) Copy constructor.7) Move constructor.

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | path to the filesystem object to which the directory iterator will refer |
| ec | - | out-parameter for error reporting in the non-throwing overloads |
| options | - | the set of BitmaskType options that control the behavior of the directory iterator |
| other | - | another directory iterator to use as source to initialize the directory iterator with |

### Exceptions

Any overload not marked `noexcept` may throw std::bad_alloc if memory allocation fails.

2,3) Throws std::filesystem::filesystem_error on underlying OS API errors, constructed with p as the first path argument and the OS error code as the error code argument.4,5) Sets a std::error_code& parameter to the OS API error code if an OS API call fails, and executes ec.clear() if no errors occur.

### Notes

To iterate over the current directory, construct the iterator as directory_iterator(".") instead of directory_iterator("").

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3013 | C++17 | `error_code` overload marked noexcept but can allocate memory | noexcept removed |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/directory_iterator/directory_iterator&oldid=158173>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 September 2023, at 15:19.