# std::experimental::filesystem::directory_entry::status, std::experimental::filesystem::directory_entry::symlink_status

From cppreference.com
< cpp‎ | experimental‎ | fs‎ | directory entry
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::space_info | | | | | | filesystem::file_type | | | | | | filesystem::perms | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | | filesystem::file_time_type | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute filesystem::system_complete | | | | | | filesystem::canonical | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | | filesystem::temp_directory_path | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

directory_entryTemplate:cpp/experimental/fs/directory entry/navbar content")

|  |  |  |
| --- | --- | --- |
| file_status status() const;  file_status status( error_code& ec ) const; | (1) | (filesystem TS) |
| file_status symlink_status() const;  file_status symlink_status( error_code& ec ) const; | (2) | (filesystem TS) |
|  |  |  |

1) Returns the potentially cached status of the entry, as if determined by a status call (symlinks are followed to their targets).2) Returns the potentially cached status of the entry, as if determined by a symlink_status call (symlinks are not followed).

### Parameters

|  |  |  |
| --- | --- | --- |
| ec | - | out-parameter for error reporting in the non-throwing overload |

### Return value

The status of the file referred to by the entry.

### Exceptions

The overload that does not take an error_code& parameter throws filesystem_error") on underlying OS API errors, constructed with p as the first argument and the OS error code as the error code argument. std::bad_alloc may be thrown if memory allocation fails. The overload taking an error_code& parameter sets it to the OS API error code if an OS API call fails, and executes ec.clear() if no errors occur. This overload hasnoexcept specification:noexcept

### Notes

The file status information is usually provided as a byproduct of directory iteration, in which case it is cached and may be obtained by these member functions without the cost of an additional system call. During directory iteration, calling `status` is unnecessary and accessors such as `is_directory` should be called with the cached status value, not with a path.

### Example

Run this code

```
#include <cstdio>
#include <cstring>
#include <experimental/filesystem>
#include <fstream>
#include <iostream>
#include <sys/socket.h>
#include <sys/stat.h>
#include <sys/un.h>
#include <unistd.h>
 
namespace fs = std::experimental::filesystem;
 
void demo_status(const fs::path& p, fs::file_status s)
{
    std::cout << p;
    // alternative: switch(s.type()) { case fs::file_type::regular: ... }
    if (fs::is_regular_file(s))
        std::cout << " is a regular file\n";
    if (fs::is_directory(s))
        std::cout << " is a directory\n";
    if (fs::is_block_file(s))
        std::cout << " is a block device\n";
    if (fs::is_character_file(s))
        std::cout << " is a character device\n";
    if (fs::is_fifo(s))
        std::cout << " is a named IPC pipe\n";
    if (fs::is_socket(s))
        std::cout << " is a named IPC socket\n";
    if (fs::is_symlink(s))
        std::cout << " is a symlink\n";
    if (!fs::exists(s))
        std::cout << " does not exist\n";
}
 
int main()
{
    // create files of different kinds
    fs::create_directory("sandbox");
    std::ofstream("sandbox/file"); // create regular file
    fs::create_directory("sandbox/dir");
    mkfifo("sandbox/pipe", 0644);
    struct sockaddr_un addr;
    addr.sun_family = AF_UNIX;
    std::strcpy(addr.sun_path, "sandbox/sock");
    int fd = socket(PF_UNIX, SOCK_STREAM, 0);
    bind(fd, (struct sockaddr*)&addr, sizeof addr);
    fs::create_symlink("file", "sandbox/symlink");
 
    // demo different status accessors
    for (auto it = fs::directory_iterator("sandbox"); it != fs::directory_iterator(); ++it)
        demo_status(*it, it->symlink_status()); // use cached status from directory entry
    demo_status("dev/null", fs::status("/dev/null")); // direct calls to status
    demo_status("dev/sda", fs::status("/dev/sda"));
    demo_status("sandbox/no", fs::status("/sandbox/no"));
 
    // cleanup
    close(fd);
    fs::remove_all("sandbox");
}

```

Possible output:

```
"sandbox/file" is a regular file
"sandbox/dir" is a directory
"sandbox/pipe" is a named IPC pipe
"sandbox/sock" is a named IPC socket
"sandbox/symlink" is a symlink
"dev/null" is a character device
"dev/sda" is a block device
"sandbox/no" does not exist

```

### See also

|  |  |
| --- | --- |
| file_status | represents file type and permissions   (class) |
| statussymlink_status | determines file attributes determines file attributes, checking the symlink target   (function) |
| status_known | checks whether file status is known   (function) |
| is_block_file | checks whether the given path refers to block device   (function) |
| is_character_file | checks whether the given path refers to a character device   (function) |
| is_directory | checks whether the given path refers to a directory   (function) |
| is_fifo | checks whether the given path refers to a named pipe   (function) |
| is_other | checks whether the argument refers to an **other** file   (function) |
| is_regular_file | checks whether the argument refers to a regular file   (function) |
| is_socket | checks whether the argument refers to a named IPC socket   (function) |
| is_symlink | checks whether the argument refers to a symbolic link   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/fs/directory_entry/status&oldid=154834>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 July 2023, at 00:37.