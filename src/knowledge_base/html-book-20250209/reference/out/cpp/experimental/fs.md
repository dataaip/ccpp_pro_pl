# Filesystem library

From cppreference.com
< cpp‎ | experimental
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
| ****Filesystem library**** (filesystem TS) | | | | |
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

****Filesystem library****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::space_info | | | | | | filesystem::file_type | | | | | | filesystem::perms | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | | filesystem::file_time_type | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute filesystem::system_complete | | | | | | filesystem::canonical | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | | filesystem::temp_directory_path | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

The Filesystem library, ISO/IEC TS 18822:2015, provides facilities for performing operations on file systems and their components, such as paths, regular files, and directories.

This library is an optional technical specification and may be unavailable if a hierarchical file system is not accessible to the implementation, or if it does not provide the necessary capabilities. Some features may not be available if they are not supported by the underlying file system (e.g. FAT filesystem has no hardlinks, softlinks, and other features).

The behavior is undefined if the calls to functions in this library introduce a **file system race**, that is, when multiple threads, processes, or computers interleave access and modification to the same object in a file system.

This library is directly based on boost.filesystem, which is currently available on more compilers and platforms than this experimental technical specification.

#### Library-wide definitions

- **file**: a file system object that holds data, can be written to, read from, or both. Files have names, attributes, one of which is file type:

:   - **directory**: a file that acts as a container of directory entries, which identify other files (some of which may be other, nested, directories). When discussing a particular file, the directory in which it appears as an entry is its **parent directory**. The parent directory can be represented by the relative pathname "..".
    - **hard link**: a directory entry that associates a name with an existing file. If multiple hard links are supported, the file is removed after the last hard link to it is removed.
    - **symbolic link**: a directory entry that associates a name with a path, which may or may not exist.
    - **regular file**: a file that is not one of the other file types.

- **file name**: a string of characters that names a file. Permissible characters, case sensitivity, maximum length, and the disallowed names are implementation-defined. Names . (dot) and .. (dot-dot) have special meaning at library level.
- **path**: sequence of elements that identifies a file. It begins with an optional root-name (e.g. "C:" or "//server"), followed by optional root-directory (e.g. "/" on Unix), followed by a sequence of zero or more file names (all but last of which have to be directories or links to directories). The native format (e.g. which characters are used as separators) and character encoding of the string representation of a path (the **pathname**) is implementation-defined, this library provides portable representation of paths.

:   - **absolute path**: a path that unambiguously identifies the location of a file.
    - **canonical path**: an absolute path that includes no symlinks, "." or ".." elements.
    - **relative path**: a path that identifies a file relative to some location on the file system. The special path names . (dot, "current directory") and .. (dot-dot, "parent directory") are relative paths.

### Classes

|  |  |
| --- | --- |
| path | represents a path   (class) |
| filesystem_error | an exception thrown on file system errors   (class) |
| directory_entry | a directory entry   (class) |
| directory_iterator | an iterator to the contents of the directory   (class) |
| recursive_directory_iterator | an iterator to the contents of a directory and its subdirectories   (class) |
| file_status | represents file type and permissions   (class) |
| space_info | information about free and available space on the filesystem   (class) |
| file_type | the type of a file   (enum) |
| perms | identifies file system permissions   (enum) |
| copy_options | specifies semantics of copy operations   (enum) |
| directory_options | options for iterating directory contents   (enum) |
| file_time_type | represents file time values   (typedef) |

### Non-member functions

|  |  |
| --- | --- |
| absolutesystem_complete | composes an absolute path converts a path to an absolute path replicating OS-specific behavior   (function) |
| canonical | composes a canonical path   (function) |
| copy | copies files or directories   (function) |
| copy_file | copies file contents   (function) |
| copy_symlink | copies a symbolic link   (function) |
| create_directorycreate_directories | creates new directory   (function) |
| create_hard_link | creates a hard link   (function) |
| create_symlinkcreate_directory_symlink | creates a symbolic link   (function) |
| current_path | return current working directory   (function) |
| exists | checks whether path refers to existing file system object   (function) |
| equivalent | checks whether two paths refer to the same file system object   (function) |
| file_size | returns the size of a file   (function) |
| hard_link_count | returns the number of hard links referring to the specific file   (function) |
| last_write_time | gets or sets the time of the last data modification   (function) |
| permissions | modifies file access permissions   (function) |
| read_symlink | obtains the target of a symbolic link   (function) |
| removeremove_all | removes a file or empty directory removes a file or directory and all its contents, recursively   (function) |
| rename | moves or renames a file or directory   (function) |
| resize_file | changes the size of a regular file by truncation or zero-fill   (function) |
| space | determines available free space on the file system   (function) |
| statussymlink_status | determines file attributes determines file attributes, checking the symlink target   (function) |
| temp_directory_path | returns a directory suitable for temporary files   (function) |
| File types | |
| is_block_file | checks whether the given path refers to block device   (function) |
| is_character_file | checks whether the given path refers to a character device   (function) |
| is_directory | checks whether the given path refers to a directory   (function) |
| is_empty | checks whether the given path refers to an empty file or directory   (function) |
| is_fifo | checks whether the given path refers to a named pipe   (function) |
| is_other | checks whether the argument refers to an **other** file   (function) |
| is_regular_file | checks whether the argument refers to a regular file   (function) |
| is_socket | checks whether the argument refers to a named IPC socket   (function) |
| is_symlink | checks whether the argument refers to a symbolic link   (function) |
| status_known | checks whether file status is known   (function) |

### See also

|  |  |
| --- | --- |
| C++ documentation for Filesystem library (C++17) | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/fs&oldid=163774>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 November 2023, at 00:25.