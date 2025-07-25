# std::filesystem::file_size

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | filesystem::relativefilesystem::proximate | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | ****filesystem::file_size**** | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<filesystem>` |  |  |
| std::uintmax_t file_size( const std::filesystem::path& p ); | (1) | (since C++17) |
| std::uintmax_t file_size( const std::filesystem::path& p,                            std::error_code& ec ) noexcept; | (2) | (since C++17) |
|  |  |  |

If p does not exist, reports an error.

For a regular file p, returns the size determined as if by reading the `st_size` member of the structure obtained by POSIX `stat` (symlinks are followed).

The result of attempting to determine the size of a directory (as well as any other file that is not a regular file or a symlink) is implementation-defined.

The non-throwing overload returns static_cast<std::uintmax_t>(-1) on errors.

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | path to examine |
| ec | - | out-parameter for error reporting in the non-throwing overload |

### Return value

The size of the file, in bytes.

### Exceptions

Any overload not marked `noexcept` may throw std::bad_alloc if memory allocation fails.

1) Throws std::filesystem::filesystem_error on underlying OS API errors, constructed with p as the first path argument and the OS error code as the error code argument.2) Sets a std::error_code& parameter to the OS API error code if an OS API call fails, and executes ec.clear() if no errors occur.

### Example

Run this code

```
#include <cmath>
#include <filesystem>
#include <fstream>
#include <iostream>
namespace fs = std::filesystem;
 
struct HumanReadable
{
    std::uintmax_t size{};
 
private:
    friend std::ostream& operator<<(std::ostream& os, HumanReadable hr)
    {
        int o{};
        double mantissa = hr.size;
        for (; mantissa >= 1024.; mantissa /= 1024., ++o);
        os << std::ceil(mantissa * 10.) / 10. << "BKMGTPE"[o];
        return o ? os << "B (" << hr.size << ')' : os;
    }
};
 
int main(int, char const* argv[])
{
    fs::path example = "example.bin";
    fs::path p = fs::current_path() / example;
    std::ofstream(p).put('a'); // create file of size 1
    std::cout << example << " size = " << fs::file_size(p) << '\n';
    fs::remove(p);
 
    p = argv[0];
    std::cout << p << " size = " << HumanReadable{fs::file_size(p)} << '\n';
 
    try
    {
        std::cout << "Attempt to get size of a directory:\n";
        [[maybe_unused]] auto x_x = fs::file_size("/dev");
    }
    catch (fs::filesystem_error& e)
    {
        std::cout << e.what() << '\n';
    }
 
    for (std::error_code ec; fs::path bin : {"cat", "mouse"})
    {
        bin = "/bin"/bin;
        if (const std::uintmax_t size = fs::file_size(bin, ec); ec)
            std::cout << bin << " : " << ec.message() << '\n';
        else
            std::cout << bin << " size = " << HumanReadable{size} << '\n';
    }
}

```

Possible output:

```
"example.bin" size = 1
"./a.out" size = 22KB (22512)
Attempt to get size of a directory:
filesystem error: cannot get file size: Is a directory [/dev]
"/bin/cat" size = 50.9KB (52080)
"/bin/mouse" : No such file or directory

```

### See also

|  |  |
| --- | --- |
| resize_file(C++17) | changes the size of a regular file by truncation or zero-fill   (function) |
| space(C++17) | determines available free space on the file system   (function) |
| file_size | returns the size of the file to which the directory entry refers   (public member function of `std::filesystem::directory_entry`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/file_size&oldid=159791>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 September 2023, at 23:26.