# Standard library header <filesystem> (C++17)

From cppreference.com
< cpp‎ | header
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

Standard library headers

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | ****<filesystem>**** (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the filesystem support library.

|  |  |
| --- | --- |
| Includes | |
| <compare>(C++20) | Three-way comparison operator support |
| Classes | |
| Defined in namespace `std::filesystem` | |
| path(C++17) | represents a path   (class) |
| filesystem_error(C++17) | an exception thrown on file system errors   (class) |
| directory_entry(C++17) | a directory entry   (class) |
| directory_iterator(C++17) | an iterator to the contents of the directory   (class) |
| recursive_directory_iterator(C++17) | an iterator to the contents of a directory and its subdirectories   (class) |
| file_status(C++17) | represents file type and permissions   (class) |
| space_info(C++17) | information about free and available space on the filesystem   (class) |
| file_type(C++17) | the type of a file   (enum) |
| perms(C++17) | identifies file system permissions   (enum) |
| perm_options(C++17) | specifies semantics of permissions operations   (enum) |
| copy_options(C++17) | specifies semantics of copy operations   (enum) |
| directory_options(C++17) | options for iterating directory contents   (enum) |
| file_time_type(C++17) | represents file time values   (typedef) |
| Defined in namespace `std` | |
| std::hash<std::filesystem::path>(C++17) | hash support for std::filesystem::path   (class template specialization) |
| Forward declarations | |
| Defined in header `<functional>` | |
| Defined in namespace `std` | |
| hash(C++11) | hash function object   (class template) |
| Functions | |
| Defined in namespace `std::filesystem` | |
| u8path(C++17)(deprecated in C++20) | creates a `path` from a UTF-8 encoded source   (function) |
| absolute(C++17) | composes an absolute path   (function) |
| canonicalweakly_canonical(C++17) | composes a canonical path   (function) |
| relativeproximate(C++17) | composes a relative path   (function) |
| copy(C++17) | copies files or directories   (function) |
| copy_file(C++17) | copies file contents   (function) |
| copy_symlink(C++17) | copies a symbolic link   (function) |
| create_directorycreate_directories(C++17)(C++17) | creates new directory   (function) |
| create_hard_link(C++17) | creates a hard link   (function) |
| create_symlinkcreate_directory_symlink(C++17)(C++17) | creates a symbolic link   (function) |
| current_path(C++17) | returns or sets the current working directory   (function) |
| exists(C++17) | checks whether path refers to existing file system object   (function) |
| equivalent(C++17) | checks whether two paths refer to the same file system object   (function) |
| file_size(C++17) | returns the size of a file   (function) |
| hard_link_count(C++17) | returns the number of hard links referring to the specific file   (function) |
| last_write_time(C++17) | gets or sets the time of the last data modification   (function) |
| permissions(C++17) | modifies file access permissions   (function) |
| read_symlink(C++17) | obtains the target of a symbolic link   (function) |
| removeremove_all(C++17)(C++17) | removes a file or empty directory removes a file or directory and all its contents, recursively   (function) |
| rename(C++17) | moves or renames a file or directory   (function) |
| resize_file(C++17) | changes the size of a regular file by truncation or zero-fill   (function) |
| space(C++17) | determines available free space on the file system   (function) |
| statussymlink_status(C++17)(C++17) | determines file attributes determines file attributes, checking the symlink target   (function) |
| temp_directory_path(C++17) | returns a directory suitable for temporary files   (function) |
| File types | |
| is_block_file(C++17) | checks whether the given path refers to block device   (function) |
| is_character_file(C++17) | checks whether the given path refers to a character device   (function) |
| is_directory(C++17) | checks whether the given path refers to a directory   (function) |
| is_empty(C++17) | checks whether the given path refers to an empty file or directory   (function) |
| is_fifo(C++17) | checks whether the given path refers to a named pipe   (function) |
| is_other(C++17) | checks whether the argument refers to an **other** file   (function) |
| is_regular_file(C++17) | checks whether the argument refers to a regular file   (function) |
| is_socket(C++17) | checks whether the argument refers to a named IPC socket   (function) |
| is_symlink(C++17) | checks whether the argument refers to a symbolic link   (function) |
| status_known(C++17) | checks whether file status is known   (function) |

### Synopsis

```
#include <compare>
 
namespace std::filesystem {
  // paths
  class path;
 
  // path non-member functions
  void swap(path& lhs, path& rhs) noexcept;
  size_t hash_value(const path& p) noexcept;
 
  // filesystem errors
  class filesystem_error;
 
  // directory entries
  class directory_entry;
 
  // directory iterators
  class directory_iterator;
 
  // range access for directory iterators
  directory_iterator begin(directory_iterator iter) noexcept;
  directory_iterator end(directory_iterator) noexcept;
 
  // recursive directory iterators
  class recursive_directory_iterator;
 
  // range access for recursive directory iterators
  recursive_directory_iterator begin(recursive_directory_iterator iter) noexcept;
  recursive_directory_iterator end(recursive_directory_iterator) noexcept;
 
  // file status
  class file_status;
 
  struct space_info {
    uintmax_t capacity;
    uintmax_t free;
    uintmax_t available;
 
    friend bool operator==(const space_info&, const space_info&) = default;
  };
 
  // enumerations
  enum class file_type;
  enum class perms;
  enum class perm_options;
  enum class copy_options;
  enum class directory_options;
 
  using file_time_type = chrono::time_point<chrono::file_clock>;
 
  // filesystem operations
  path absolute(const path& p);
  path absolute(const path& p, error_code& ec);
 
  path canonical(const path& p);
  path canonical(const path& p, error_code& ec);
 
  void copy(const path& from, const path& to);
  void copy(const path& from, const path& to, error_code& ec);
  void copy(const path& from, const path& to, copy_options options);
  void copy(const path& from, const path& to, copy_options options,
            error_code& ec);
 
  bool copy_file(const path& from, const path& to);
  bool copy_file(const path& from, const path& to, error_code& ec);
  bool copy_file(const path& from, const path& to, copy_options option);
  bool copy_file(const path& from, const path& to, copy_options option,
                 error_code& ec);
 
  void copy_symlink(const path& existing_symlink, const path& new_symlink);
  void copy_symlink(const path& existing_symlink, const path& new_symlink,
                    error_code& ec) noexcept;
 
  bool create_directories(const path& p);
  bool create_directories(const path& p, error_code& ec);
 
  bool create_directory(const path& p);
  bool create_directory(const path& p, error_code& ec) noexcept;
 
  bool create_directory(const path& p, const path& attributes);
  bool create_directory(const path& p, const path& attributes,
                        error_code& ec) noexcept;
 
  void create_directory_symlink(const path& to, const path& new_symlink);
  void create_directory_symlink(const path& to, const path& new_symlink,
                                error_code& ec) noexcept;
 
  void create_hard_link(const path& to, const path& new_hard_link);
  void create_hard_link(const path& to, const path& new_hard_link,
                        error_code& ec) noexcept;
 
  void create_symlink(const path& to, const path& new_symlink);
  void create_symlink(const path& to, const path& new_symlink,
                      error_code& ec) noexcept;
 
  path current_path();
  path current_path(error_code& ec);
  void current_path(const path& p);
  void current_path(const path& p, error_code& ec) noexcept;
 
  bool equivalent(const path& p1, const path& p2);
  bool equivalent(const path& p1, const path& p2, error_code& ec) noexcept;
 
  bool exists(file_status s) noexcept;
  bool exists(const path& p);
  bool exists(const path& p, error_code& ec) noexcept;
 
  uintmax_t file_size(const path& p);
  uintmax_t file_size(const path& p, error_code& ec) noexcept;
 
  uintmax_t hard_link_count(const path& p);
  uintmax_t hard_link_count(const path& p, error_code& ec) noexcept;
 
  bool is_block_file(file_status s) noexcept;
  bool is_block_file(const path& p);
  bool is_block_file(const path& p, error_code& ec) noexcept;
 
  bool is_character_file(file_status s) noexcept;
  bool is_character_file(const path& p);
  bool is_character_file(const path& p, error_code& ec) noexcept;
 
  bool is_directory(file_status s) noexcept;
  bool is_directory(const path& p);
  bool is_directory(const path& p, error_code& ec) noexcept;
 
  bool is_empty(const path& p);
  bool is_empty(const path& p, error_code& ec);
 
  bool is_fifo(file_status s) noexcept;
  bool is_fifo(const path& p);
  bool is_fifo(const path& p, error_code& ec) noexcept;
 
  bool is_other(file_status s) noexcept;
  bool is_other(const path& p);
  bool is_other(const path& p, error_code& ec) noexcept;
 
  bool is_regular_file(file_status s) noexcept;
  bool is_regular_file(const path& p);
  bool is_regular_file(const path& p, error_code& ec) noexcept;
 
  bool is_socket(file_status s) noexcept;
  bool is_socket(const path& p);
  bool is_socket(const path& p, error_code& ec) noexcept;
 
  bool is_symlink(file_status s) noexcept;
  bool is_symlink(const path& p);
  bool is_symlink(const path& p, error_code& ec) noexcept;
 
  file_time_type last_write_time(const path& p);
  file_time_type last_write_time(const path& p, error_code& ec) noexcept;
  void last_write_time(const path& p, file_time_type new_time);
  void last_write_time(const path& p, file_time_type new_time,
                       error_code& ec) noexcept;
 
  void permissions(const path& p, perms prms, perm_options opts=perm_options::replace);
  void permissions(const path& p, perms prms, error_code& ec) noexcept;
  void permissions(const path& p, perms prms, perm_options opts, error_code& ec);
 
  path proximate(const path& p, error_code& ec);
  path proximate(const path& p, const path& base = current_path());
  path proximate(const path& p, const path& base, error_code& ec);
 
  path read_symlink(const path& p);
  path read_symlink(const path& p, error_code& ec);
 
  path relative(const path& p, error_code& ec);
  path relative(const path& p, const path& base = current_path());
  path relative(const path& p, const path& base, error_code& ec);
 
  bool remove(const path& p);
  bool remove(const path& p, error_code& ec) noexcept;
 
  uintmax_t remove_all(const path& p);
  uintmax_t remove_all(const path& p, error_code& ec);
 
  void rename(const path& from, const path& to);
  void rename(const path& from, const path& to, error_code& ec) noexcept;
 
  void resize_file(const path& p, uintmax_t size);
  void resize_file(const path& p, uintmax_t size, error_code& ec) noexcept;
 
  space_info space(const path& p);
  space_info space(const path& p, error_code& ec) noexcept;
 
  file_status status(const path& p);
  file_status status(const path& p, error_code& ec) noexcept;
 
  bool status_known(file_status s) noexcept;
 
  file_status symlink_status(const path& p);
  file_status symlink_status(const path& p, error_code& ec) noexcept;
 
  path temp_directory_path();
  path temp_directory_path(error_code& ec);
 
  path weakly_canonical(const path& p);
  path weakly_canonical(const path& p, error_code& ec);
}
 
// hash support
namespace std {
  template<class T> struct hash;
  template<> struct hash<filesystem::path>;
}
 
namespace std::ranges {
  template<>
  inline constexpr bool enable_borrowed_range<filesystem::directory_iterator> = true;
  template<>
  inline constexpr bool
    enable_borrowed_range<filesystem::recursive_directory_iterator> = true;
 
  template<>
  inline constexpr bool enable_view<filesystem::directory_iterator> = true;
  template<>
  inline constexpr bool enable_view<filesystem::recursive_directory_iterator> = true;
}

```

#### Class std::filesystem::path

```
namespace std::filesystem {
  class path {
  public:
    using value_type  = /* see description */;
    using string_type = basic_string<value_type>;
    static constexpr value_type preferred_separator = /* see description */;
 
    // enumeration format
    enum format;
 
    // constructors and destructor
    path() noexcept;
    path(const path& p);
    path(path&& p) noexcept;
    path(string_type&& source, format fmt = auto_format);
    template<class Source>
      path(const Source& source, format fmt = auto_format);
    template<class InputIt>
      path(InputIt first, InputIt last, format fmt = auto_format);
    template<class Source>
      path(const Source& source, const locale& loc, format fmt = auto_format);
    template<class InputIt>
      path(InputIt first, InputIt last, const locale& loc, format fmt = auto_format);
    ~path();
 
    // assignments
    path& operator=(const path& p);
    path& operator=(path&& p) noexcept;
    path& operator=(string_type&& source);
    path& assign(string_type&& source);
    template<class Source>
      path& operator=(const Source& source);
    template<class Source>
      path& assign(const Source& source);
    template<class InputIt>
      path& assign(InputIt first, InputIt last);
 
    // appends
    path& operator/=(const path& p);
    template<class Source>
      path& operator/=(const Source& source);
    template<class Source>
      path& append(const Source& source);
    template<class InputIt>
      path& append(InputIt first, InputIt last);
 
    // concatenation
    path& operator+=(const path& x);
    path& operator+=(const string_type& x);
    path& operator+=(basic_string_view<value_type> x);
    path& operator+=(const value_type* x);
    path& operator+=(value_type x);
    template<class Source>
      path& operator+=(const Source& x);
    template<class ECharT>
      path& operator+=(ECharT x);
    template<class Source>
      path& concat(const Source& x);
    template<class InputIt>
      path& concat(InputIt first, InputIt last);
 
    // modifiers
    void  clear() noexcept;
    path& make_preferred();
    path& remove_filename();
    path& replace_filename(const path& replacement);
    path& replace_extension(const path& replacement = path());
    void  swap(path& rhs) noexcept;
 
    // non-member operators
    friend bool operator==(const path& lhs, const path& rhs) noexcept;
    friend strong_ordering operator<=>(const path& lhs, const path& rhs) noexcept;
 
    friend path operator/ (const path& lhs, const path& rhs);
 
    // native format observers
    const string_type& native() const noexcept;
    const value_type*  c_str() const noexcept;
    operator string_type() const;
 
    template<class ECharT, class Traits = char_traits<ECharT>,
             class Allocator = allocator<ECharT>>
      basic_string<ECharT, Traits, Allocator>
        string(const Allocator& a = Allocator()) const;
    std::string    string() const;
    std::wstring   wstring() const;
    std::u8string  u8string() const;
    std::u16string u16string() const;
    std::u32string u32string() const;
 
    // generic format observers
    template<class ECharT, class Traits = char_traits<ECharT>,
             class Allocator = allocator<ECharT>>
      basic_string<ECharT, Traits, Allocator>
        generic_string(const Allocator& a = Allocator()) const;
    std::string    generic_string() const;
    std::wstring   generic_wstring() const;
    std::u8string  generic_u8string() const;
    std::u16string generic_u16string() const;
    std::u32string generic_u32string() const;
 
    // compare
    int compare(const path& p) const noexcept;
    int compare(const string_type& s) const;
    int compare(basic_string_view<value_type> s) const;
    int compare(const value_type* s) const;
 
    // decomposition
    path root_name() const;
    path root_directory() const;
    path root_path() const;
    path relative_path() const;
    path parent_path() const;
    path filename() const;
    path stem() const;
    path extension() const;
 
    // query
    bool empty() const noexcept;
    bool has_root_name() const;
    bool has_root_directory() const;
    bool has_root_path() const;
    bool has_relative_path() const;
    bool has_parent_path() const;
    bool has_filename() const;
    bool has_stem() const;
    bool has_extension() const;
    bool is_absolute() const;
    bool is_relative() const;
 
    // generation
    path lexically_normal() const;
    path lexically_relative(const path& base) const;
    path lexically_proximate(const path& base) const;
 
    // iterators
    class iterator;
    using const_iterator = iterator;
 
    iterator begin() const;
    iterator end() const;
 
    // path inserter and extractor
    template<class CharT, class Traits>
      friend basic_ostream<CharT, Traits>&
        operator<<(basic_ostream<CharT, Traits>& os, const path& p);
    template<class CharT, class Traits>
      friend basic_istream<CharT, Traits>&
        operator>>(basic_istream<CharT, Traits>& is, path& p);
  };
}

```

#### Class std::filesystem::filesystem_error

```
namespace std::filesystem {
  class filesystem_error : public system_error {
  public:
    filesystem_error(const string& what_arg, error_code ec);
    filesystem_error(const string& what_arg,
                     const path& p1, error_code ec);
    filesystem_error(const string& what_arg,
                     const path& p1, const path& p2, error_code ec);
 
    const path& path1() const noexcept;
    const path& path2() const noexcept;
    const char* what() const noexcept override;
  };
}

```

#### Class std::filesystem::directory_entry

```
namespace std::filesystem {
  class directory_entry {
  public:
    // constructors and destructor
    directory_entry() noexcept = default;
    directory_entry(const directory_entry&) = default;
    directory_entry(directory_entry&&) noexcept = default;
    explicit directory_entry(const filesystem::path& p);
    directory_entry(const filesystem::path& p, error_code& ec);
    ~directory_entry();
 
    // assignments
    directory_entry& operator=(const directory_entry&) = default;
    directory_entry& operator=(directory_entry&&) noexcept = default;
 
    // modifiers
    void assign(const filesystem::path& p);
    void assign(const filesystem::path& p, error_code& ec);
    void replace_filename(const filesystem::path& p);
    void replace_filename(const filesystem::path& p, error_code& ec);
    void refresh();
    void refresh(error_code& ec) noexcept;
 
    // observers
    const filesystem::path& path() const noexcept;
    operator const filesystem::path&() const noexcept;
    bool exists() const;
    bool exists(error_code& ec) const noexcept;
    bool is_block_file() const;
    bool is_block_file(error_code& ec) const noexcept;
    bool is_character_file() const;
    bool is_character_file(error_code& ec) const noexcept;
    bool is_directory() const;
    bool is_directory(error_code& ec) const noexcept;
    bool is_fifo() const;
    bool is_fifo(error_code& ec) const noexcept;
    bool is_other() const;
    bool is_other(error_code& ec) const noexcept;
    bool is_regular_file() const;
    bool is_regular_file(error_code& ec) const noexcept;
    bool is_socket() const;
    bool is_socket(error_code& ec) const noexcept;
    bool is_symlink() const;
    bool is_symlink(error_code& ec) const noexcept;
    uintmax_t file_size() const;
    uintmax_t file_size(error_code& ec) const noexcept;
    uintmax_t hard_link_count() const;
    uintmax_t hard_link_count(error_code& ec) const noexcept;
    file_time_type last_write_time() const;
    file_time_type last_write_time(error_code& ec) const noexcept;
    file_status status() const;
    file_status status(error_code& ec) const noexcept;
    file_status symlink_status() const;
    file_status symlink_status(error_code& ec) const noexcept;
 
    bool operator==(const directory_entry& rhs) const noexcept;
    strong_ordering operator<=>(const directory_entry& rhs) const noexcept;
 
    // inserter
    template<class CharT, class Traits>
      friend basic_ostream<CharT, Traits>&
        operator<<(basic_ostream<CharT, Traits>& os, const directory_entry& d);
 
  private:
    filesystem::path pathobject;        // exposition only
    friend class directory_iterator;    // exposition only
  };
}

```

#### Class std::filesystem::directory_iterator

```
namespace std::filesystem {
  class directory_iterator {
  public:
    using iterator_category = input_iterator_tag;
    using value_type        = directory_entry;
    using difference_type   = ptrdiff_t;
    using pointer           = const directory_entry*;
    using reference         = const directory_entry&;
 
    // member functions
    directory_iterator() noexcept;
    explicit directory_iterator(const path& p);
    directory_iterator(const path& p, directory_options options);
    directory_iterator(const path& p, error_code& ec);
    directory_iterator(const path& p, directory_options options,
                       error_code& ec);
    directory_iterator(const directory_iterator& rhs);
    directory_iterator(directory_iterator&& rhs) noexcept;
    ~directory_iterator();
 
    directory_iterator& operator=(const directory_iterator& rhs);
    directory_iterator& operator=(directory_iterator&& rhs) noexcept;
 
    const directory_entry& operator*() const;
    const directory_entry* operator->() const;
    directory_iterator&    operator++();
    directory_iterator&    increment(error_code& ec);
 
    bool operator==(default_sentinel_t) const noexcept {
      return *this == directory_iterator();
    }
 
    // other members as required by input iterators
  };
}

```

#### Class std::filesystem::recursive_directory_iterator

```
namespace std::filesystem {
  class recursive_directory_iterator {
  public:
    using iterator_category = input_iterator_tag;
    using value_type        = directory_entry;
    using difference_type   = ptrdiff_t;
    using pointer           = const directory_entry*;
    using reference         = const directory_entry&;
 
    // constructors and destructor
    recursive_directory_iterator() noexcept;
    explicit recursive_directory_iterator(const path& p);
    recursive_directory_iterator(const path& p, directory_options options);
    recursive_directory_iterator(const path& p, directory_options options,
                                 error_code& ec);
    recursive_directory_iterator(const path& p, error_code& ec);
    recursive_directory_iterator(const recursive_directory_iterator& rhs);
    recursive_directory_iterator(recursive_directory_iterator&& rhs) noexcept;
    ~recursive_directory_iterator();
 
    // observers
    directory_options  options() const;
    int                depth() const;
    bool               recursion_pending() const;
 
    const directory_entry& operator*() const;
    const directory_entry* operator->() const;
 
    // modifiers
    recursive_directory_iterator&
      operator=(const recursive_directory_iterator& rhs);
    recursive_directory_iterator&
      operator=(recursive_directory_iterator&& rhs) noexcept;
 
    recursive_directory_iterator& operator++();
    recursive_directory_iterator& increment(error_code& ec);
 
    void pop();
    void pop(error_code& ec);
    void disable_recursion_pending();
 
    bool operator==(default_sentinel_t) const noexcept {
      return *this == recursive_directory_iterator();
    }
 
    // other members as required by input iterators
  };
}

```

#### Class std::filesystem::file_status

```
namespace std::filesystem {
  class file_status {
  public:
    // constructors and destructor
    file_status() noexcept : file_status(file_type::none) {}
    explicit file_status(file_type ft,
                         perms prms = perms::unknown) noexcept;
    file_status(const file_status&) noexcept = default;
    file_status(file_status&&) noexcept = default;
    ~file_status();
 
    // assignments
    file_status& operator=(const file_status&) noexcept = default;
    file_status& operator=(file_status&&) noexcept = default;
 
    // modifiers
    void       type(file_type ft) noexcept;
    void       permissions(perms prms) noexcept;
 
    // observers
    file_type  type() const noexcept;
    perms      permissions() const noexcept;
 
    friend bool operator==(const file_status& lhs, const file_status& rhs) noexcept
      { return lhs.type() == rhs.type() && lhs.permissions() == rhs.permissions(); }
  };
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/filesystem&oldid=163913>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 November 2023, at 06:34.