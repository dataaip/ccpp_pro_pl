# std::filesystem::relative, std::filesystem::proximate

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | filesystem::space_info | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_type | | | | | | filesystem::file_time_type | | | | | | filesystem::perms | | | | | | filesystem::perm_options | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | ****filesystem::relativefilesystem::proximate**** | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<filesystem>` |  |  |
| path relative( const std::filesystem::path& p,                 std::error_code& ec ); | (1) | (since C++17) |
| path relative( const std::filesystem::path& p,                 const std::filesystem::path& base = std::filesystem::current_path() ); | (2) | (since C++17) |
| path relative( const std::filesystem::path& p,  const std::filesystem::path& base, std::error_code& ec ); | (3) | (since C++17) |
| path proximate( const std::filesystem::path& p,                  std::error_code& ec ); | (4) | (since C++17) |
| path proximate( const std::filesystem::path& p,                  const std::filesystem::path& base = std::filesystem::current_path() ); | (5) | (since C++17) |
| path proximate( const std::filesystem::path& p,  const std::filesystem::path& base, std::error_code& ec ); | (6) | (since C++17) |
|  |  |  |

1) Returns relative(p, current_path(), ec).2,3) Returns p made relative to base. Resolves symlinks and normalizes both p and base before other processing. Effectively returns std::filesystem::weakly_canonical(p).lexically_relative(std::filesystem::weakly_canonical(base)) or std::filesystem::weakly_canonical(p, ec).lexically_relative(std::filesystem::weakly_canonical(base, ec)), except the error code form returns path() at the first error occurrence, if any.4) Returns proximate(p, current_path(), ec).5,6) Effectively returns std::filesystem::weakly_canonical(p).lexically_proximate(std::filesystem::weakly_canonical(base)) or std::filesystem::weakly_canonical(p, ec).lexically_proximate(std::filesystem::weakly_canonical(base, ec)), except the error code form returns path() at the first error occurrence, if any.

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | an existing path |
| base | - | base path, against which p will be made relative/proximate |
| ec | - | error code to store error status to |

### Return value

1) p made relative against current_path().2,3) p made relative against base.4) p made proximate against current_path().5,6) p made proximate against base.

### Exceptions

Any overload not marked `noexcept` may throw std::bad_alloc if memory allocation fails.

2,5) Throws std::filesystem::filesystem_error on underlying OS API errors, constructed with p as the first path argument, base as the second path argument, and the OS error code as the error code argument.1,3,4,6) Sets a std::error_code& parameter to the OS API error code if an OS API call fails, and executes ec.clear() if no errors occur.

### Example

Run this code

```
#include <filesystem>
#include <iostream>
 
void show(std::filesystem::path x, std::filesystem::path y)
{
    std::cout << "x:\t\t " << x << "\ny:\t\t " << y << '\n'
              << "relative(x, y):  "
              << std::filesystem::relative(x, y) << '\n'
              << "proximate(x, y): "
              << std::filesystem::proximate(x, y) << "\n\n";
}
 
int main()
{
    show("/a/b/c", "/a/b");
    show("/a/c", "/a/b");
    show("c", "/a/b");
    show("/a/b", "c");
}

```

Possible output:

```
x:               "/a/b/c"
y:               "/a/b"
relative(x, y):  "c"
proximate(x, y): "c"
 
x:               "/a/c"
y:               "/a/b"
relative(x, y):  "../c"
proximate(x, y): "../c"
 
x:               "c"
y:               "/a/b"
relative(x, y):  ""
proximate(x, y): "c"
 
x:               "/a/b"
y:               "c"
relative(x, y):  ""
proximate(x, y): "/a/b"

```

### See also

|  |  |
| --- | --- |
| path(C++17) | represents a path   (class) |
| absolute(C++17) | composes an absolute path   (function) |
| canonicalweakly_canonical(C++17) | composes a canonical path   (function) |
| lexically_normallexically_relativelexically_proximate | converts path to normal form converts path to relative form converts path to proximate form   (public member function of `std::filesystem::path`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/relative&oldid=158215>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 September 2023, at 08:07.