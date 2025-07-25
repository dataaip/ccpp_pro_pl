# std::filesystem::perms

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | filesystem::space_info | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_type | | | | | | filesystem::file_time_type | | | | | | ****filesystem::perms**** | | | | | | filesystem::perm_options | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | filesystem::relativefilesystem::proximate | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<filesystem>` |  |  |
| enum class perms; |  | (since C++17) |
|  |  |  |

This type represents file access permissions.

`perms` satisfies the requirements of BitmaskType (which means the bitwise operators operator&, operator|, operator^, operator~, operator&=, operator|=, and operator^= are defined for this type). `none` represents the empty bitmask; every other enumerator represents a distinct bitmask element.

Access permissions model POSIX permission bits, and any individual file permissions (as reported by filesystem::status) are a combination of some of the following bits:

### Member constants

| Member constant | Value (octal) | POSIX equivalent | Meaning |
| --- | --- | --- | --- |
| `none` | ​0​ |  | No permission bits are set |
| `owner_read` | 0400 | S_IRUSR | File owner has read permission |
| `owner_write` | 0200 | S_IWUSR | File owner has write permission |
| `owner_exec` | 0100 | S_IXUSR | File owner has execute/search permission |
| `owner_all` | 0700 | S_IRWXU | File owner has read, write, and execute/search permissions Equivalent to owner_read | owner_write | owner_exec |
| `group_read` | 040 | S_IRGRP | The file's user group has read permission |
| `group_write` | 020 | S_IWGRP | The file's user group has write permission |
| `group_exec` | 010 | S_IXGRP | The file's user group has execute/search permission |
| `group_all` | 070 | S_IRWXG | The file's user group has read, write, and execute/search permissions Equivalent to group_read | group_write | group_exec |
| `others_read` | 04 | S_IROTH | Other users have read permission |
| `others_write` | 02 | S_IWOTH | Other users have write permission |
| `others_exec` | 01 | S_IXOTH | Other users have execute/search permission |
| `others_all` | 07 | S_IRWXO | Other users have read, write, and execute/search permissions Equivalent to others_read | others_write | others_exec |
| `all` | 0777 |  | All users have read, write, and execute/search permissions Equivalent to owner_all | group_all | others_all |
| `set_uid` | 04000 | S_ISUID | Set user ID to file owner user ID on execution |
| `set_gid` | 02000 | S_ISGID | Set group ID to file's user group ID on execution |
| `sticky_bit` | 01000 | S_ISVTX | Implementation-defined meaning, but POSIX XSI specifies that when set on a directory, only file owners may delete files even if the directory is writeable to others (used with /tmp) |
| `mask` | 07777 |  | All valid permission bits. Equivalent to all | set_uid | set_gid | sticky_bit |

Additionally, the following constants of this type are defined, which do not represent permissions:

| Member constant | Value (hex) | Meaning |
| --- | --- | --- |
| `unknown` | 0xFFFF | Unknown permissions (e.g. when filesystem::file_status is created without permissions) |

### Notes

Permissions may not necessarily be implemented as bits, but they are treated that way conceptually.

Some permission bits may be ignored on some systems, and changing some bits may automatically change others (e.g. on platforms without owner/group/all distinction, setting any of the three write bits set all three).

### Example

Run this code

```
#include <filesystem>
#include <fstream>
#include <iostream>
 
void demo_perms(std::filesystem::perms p)
{
    using std::filesystem::perms;
    auto show = =
    {
        std::cout << (perms::none == (perm & p) ? '-' : op);
    };
    show('r', perms::owner_read);
    show('w', perms::owner_write);
    show('x', perms::owner_exec);
    show('r', perms::group_read);
    show('w', perms::group_write);
    show('x', perms::group_exec);
    show('r', perms::others_read);
    show('w', perms::others_write);
    show('x', perms::others_exec);
    std::cout << '\n';
}
 
int main()
{
    std::ofstream("test.txt"); // create file
 
    std::cout << "Created file with permissions: ";
    demo_perms(std::filesystem::status("test.txt").permissions());
 
    std::filesystem::permissions(
        "test.txt",
        std::filesystem::perms::owner_all | std::filesystem::perms::group_all,
        std::filesystem::perm_options::add
    );
 
    std::cout << "After adding u+rwx and g+rwx:  ";
    demo_perms(std::filesystem::status("test.txt").permissions());
 
    std::filesystem::remove("test.txt");
}

```

Possible output:

```
Created file with permissions: rw-r--r--
After adding u+rwx and g+wrx:  rwxrwxr--

```

### See also

|  |  |
| --- | --- |
| statussymlink_status(C++17)(C++17) | determines file attributes determines file attributes, checking the symlink target   (function) |
| permissions(C++17) | modifies file access permissions   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/perms&oldid=158115>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 September 2023, at 10:38.