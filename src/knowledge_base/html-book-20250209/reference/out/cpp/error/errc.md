# std::errc

From cppreference.com
< cpp‎ | error
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

Utilities library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

Diagnostics library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception handling | | | | | | exception | | | | | | uncaught_exceptionuncaught_exceptions(until C++20\*)(C++17) | | | | | | exception_ptr(C++11) | | | | | | make_exception_ptr(C++11) | | | | | | current_exception(C++11) | | | | | | rethrow_exception(C++11) | | | | | | nested_exception(C++11) | | | | | | throw_with_nested(C++11) | | | | | | rethrow_if_nested(C++11) | | | | | | Exception handling failures | | | | | | terminate | | | | | | terminate_handler | | | | | | get_terminate(C++11) | | | | | | set_terminate | | | | | | bad_exception | | | | | | unexpected(until C++17\*) | | | | | | unexpected_handler(until C++17\*) | | | | | | get_unexpected(until C++17\*) | | | | | | set_unexpected(until C++17\*) | | | | | | Error numbers | | | | | | Error codes | | | | | | errno | | | | | | Assertions | | | | | | assert | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception categories | | | | | | logic_error | | | | | | invalid_argument | | | | | | domain_error | | | | | | length_error | | | | | | out_of_range | | | | | | runtime_error | | | | | | range_error | | | | | | overflow_error | | | | | | underflow_error | | | | | | tx_exception(TM TS) | | | | | | System error | | | | | | error_category(C++11) | | | | | | generic_category(C++11) | | | | | | system_category(C++11) | | | | | | error_condition(C++11) | | | | | | ****errc****(C++11) | | | | | | error_code(C++11) | | | | | | system_error(C++11) | | | | | | Stacktrace | | | | | | stacktrace_entry(C++23) | | | | | | basic_stacktrace(C++23) | | | | | | Debugging support | | | | | | is_debugger_present(C++26) | | | | | | breakpoint_if_debugging(C++26) | | | | | | breakpoint(C++26) | | | | | |

****std::errc****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Non-member functions | | | | |
| make_error_code | | | | |
| make_error_condition | | | | |
| Helper classes | | | | |
| is_error_condition_enum | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<system_error>` |  |  |
| enum class errc; |  | (since C++11) |
|  |  |  |

The scoped enumeration `std::errc` defines the values of portable error conditions that correspond to the POSIX error codes.

### Member constants

|  |  |
| --- | --- |
| Name | Equivalent POSIX Error |
| `address_family_not_supported` | `EAFNOSUPPORT` |
| `address_in_use` | `EADDRINUSE` |
| `address_not_available` | `EADDRNOTAVAIL` |
| `already_connected` | `EISCONN` |
| `argument_list_too_long` | `E2BIG` |
| `argument_out_of_domain` | `EDOM` |
| `bad_address` | `EFAULT` |
| `bad_file_descriptor` | `EBADF` |
| `bad_message` | `EBADMSG` |
| `broken_pipe` | `EPIPE` |
| `connection_aborted` | `ECONNABORTED` |
| `connection_already_in_progress` | `EALREADY` |
| `connection_refused` | `ECONNREFUSED` |
| `connection_reset` | `ECONNRESET` |
| `cross_device_link` | `EXDEV` |
| `destination_address_required` | `EDESTADDRREQ` |
| `device_or_resource_busy` | `EBUSY` |
| `directory_not_empty` | `ENOTEMPTY` |
| `executable_format_error` | `ENOEXEC` |
| `file_exists` | `EEXIST` |
| `file_too_large` | `EFBIG` |
| `filename_too_long` | `ENAMETOOLONG` |
| `function_not_supported` | `ENOSYS` |
| `host_unreachable` | `EHOSTUNREACH` |
| `identifier_removed` | `EIDRM` |
| `illegal_byte_sequence` | `EILSEQ` |
| `inappropriate_io_control_operation` | `ENOTTY` |
| `interrupted` | `EINTR` |
| `invalid_argument` | `EINVAL` |
| `invalid_seek` | `ESPIPE` |
| `io_error` | `EIO` |
| `is_a_directory` | `EISDIR` |
| `message_size` | `EMSGSIZE` |
| `network_down` | `ENETDOWN` |
| `network_reset` | `ENETRESET` |
| `network_unreachable` | `ENETUNREACH` |
| `no_buffer_space` | `ENOBUFS` |
| `no_child_process` | `ECHILD` |
| `no_link` | `ENOLINK` |
| `no_lock_available` | `ENOLCK` |
| `no_message_available` (deprecated) | `ENODATA` |
| `no_message` | `ENOMSG` |
| `no_protocol_option` | `ENOPROTOOPT` |
| `no_space_on_device` | `ENOSPC` |
| `no_stream_resources` (deprecated) | `ENOSR` |
| `no_such_device_or_address` | `ENXIO` |
| `no_such_device` | `ENODEV` |
| `no_such_file_or_directory` | `ENOENT` |
| `no_such_process` | `ESRCH` |
| `not_a_directory` | `ENOTDIR` |
| `not_a_socket` | `ENOTSOCK` |
| `not_a_stream` (deprecated) | `ENOSTR` |
| `not_connected` | `ENOTCONN` |
| `not_enough_memory` | `ENOMEM` |
| `not_supported` | `ENOTSUP` |
| `operation_canceled` | `ECANCELED` |
| `operation_in_progress` | `EINPROGRESS` |
| `operation_not_permitted` | `EPERM` |
| `operation_not_supported` | `EOPNOTSUPP` |
| `operation_would_block` | `EWOULDBLOCK` |
| `owner_dead` | `EOWNERDEAD` |
| `permission_denied` | `EACCES` |
| `protocol_error` | `EPROTO` |
| `protocol_not_supported` | `EPROTONOSUPPORT` |
| `read_only_file_system` | `EROFS` |
| `resource_deadlock_would_occur` | `EDEADLK` |
| `resource_unavailable_try_again` | `EAGAIN` |
| `result_out_of_range` | `ERANGE` |
| `state_not_recoverable` | `ENOTRECOVERABLE` |
| `stream_timeout` (deprecated) | `ETIME` |
| `text_file_busy` | `ETXTBSY` |
| `timed_out` | `ETIMEDOUT` |
| `too_many_files_open_in_system` | `ENFILE` |
| `too_many_files_open` | `EMFILE` |
| `too_many_links` | `EMLINK` |
| `too_many_symbolic_link_levels` | `ELOOP` |
| `value_too_large` | `EOVERFLOW` |
| `wrong_protocol_type` | `EPROTOTYPE` |

### Non-member functions

|  |  |
| --- | --- |
| make_error_code(std::errc)(C++11) | creates error code value for `errc` enum e   (function) |
| make_error_condition(std::errc)(C++11) | creates an error condition for an `errc` value e   (function) |

### Helper classes

|  |  |
| --- | --- |
| is_error_condition_enum<std::errc>(C++11) | extends the type trait std::is_error_condition_enum to identify `errc` values as error conditions   (function template) |

### Example

Run this code

```
#include <filesystem>
#include <fstream>
#include <iomanip>
#include <iostream>
#include <string>
#include <system_error>
#include <thread>
 
void print_error(const std::string& details, std::error_code error_code)
{
    std::string value_name;
    if (error_code == std::errc::invalid_argument)
        value_name = "std::errc::invalid_argument";
    if (error_code == std::errc::no_such_file_or_directory)
        value_name = "std::errc::no_such_file_or_directory";
    if (error_code == std::errc::is_a_directory)
        value_name = "std::errc::is_a_directory";
    if (error_code == std::errc::permission_denied)
        value_name = "std::errc::permission_denied";
 
    std::cout << details << ":\n  "
              << std::quoted(error_code.message())
              << " (" << value_name << ")\n\n";
}
 
void print_errno(const std::string& details, int errno_value = errno)
{
    print_error(details, std::make_error_code(std::errc(errno_value)));
}
 
int main()
{
    std::cout << "Detaching a not-a-thread...\n";
    try
    {
        std::thread().detach();
    }
    catch (const std::system_error& e)
    {
        print_error("Error detaching empty thread", e.code());
    }
 
    std::cout << "Opening nonexistent file...\n";
    std::ifstream nofile{"nonexistent-file"};
    if (!nofile.is_open())
        print_errno("Error opening nonexistent file for reading");
 
    std::cout << "Reading from directory as a file...\n";
    std::filesystem::create_directory("dir");
    std::ifstream dir_stream{"dir"};
    [[maybe_unused]] char c = dir_stream.get();
    if (!dir_stream.good())
        print_errno("Error reading data from directory");
 
    std::cout << "Open read-only file for writing...\n";
    std::fstream{"readonly-file", std::ios::out};
    std::filesystem::permissions("readonly-file", std::filesystem::perms::owner_read);
    std::fstream write_readonly("readonly-file", std::ios::out);
    if (!write_readonly.is_open())
        print_errno("Error opening read-only file for writing");
}

```

Possible output:

```
Detaching a not-a-thread...
Error detaching empty thread:
  "Invalid argument" (std::errc::invalid_argument)
 
Opening nonexistent file...
Error opening nonexistent file for reading:
  "No such file or directory" (std::errc::no_such_file_or_directory)
 
Reading from directory as a file...
Error reading data from directory:
  "Is a directory" (std::errc::is_a_directory)
 
Open read-only file for writing...
Error opening read-only file for writing:
  "Permission denied" (std::errc::permission_denied)

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3869 | C++11 | the member constants `no_message_available`, `no_stream_resources`, `not_a_stream` and `stream_timeout` referred to the obsolete POSIX STREAMS API[[1]](errc.html#cite_note-1) | deprecated them |

1. ↑ Although the corresponding POSIX error numbers ENODATA, ENOSR, ENOSTR and ETIME were marked "obsolescent" in POSIX 2017, the STREAMS API was optional and not required for conformance to the previous POSIX standard (because popular unix-like systems refused to implement it).

### See also

|  |  |
| --- | --- |
| error_code(C++11) | holds a platform-dependent error code   (class) |
| error_condition(C++11) | holds a portable error code   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/error/errc&oldid=173417>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 July 2024, at 07:41.