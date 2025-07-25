# Freestanding and hosted implementations

From cppreference.com
< cpp
C++

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| ****Freestanding and hosted**** | | | | |
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

There are two kinds of implementations defined by the C++ standard: ******hosted****** and ******freestanding****** implementations. For **hosted** implementations, the set of standard library headers required by the C++ standard is much larger than for **freestanding** ones. In a **freestanding** implementation, execution may happen without an operating system.

The kind of the implementation is implementation-defined. The macro `__STDC_HOSTED__` is predefined to `1` for hosted implementations and `0` for freestanding implementations.(since C++11)

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| Requirements on multi-threaded executions and data races  | **freestanding** | **hosted** | | --- | --- | | Under a **freestanding** implementation, it is implementation-defined whether a program can have more than one thread of execution. | Under a **hosted** implementation, a C++ program can have more than one thread running concurrently. | | (since C++11) |

### Requirements on the main function

| **freestanding** | **hosted** |
| --- | --- |
| In a **freestanding** implementation, it is implementation-defined whether a program is required to define a main function. Start-up and termination is implementation-defined; start-up contains the execution of constructors for objects of namespace scope with static storage duration; termination contains the execution of destructors for objects with static storage duration. | In a **hosted** implementation, a program must contain a global function called main. Executing a program starts a main thread of execution in which the `main` function is invoked, and in which variables of static storage duration might be initialized and destroyed. |

### Requirements on standard library headers

A **freestanding** implementation has an implementation-defined set of headers. This set includes at least the headers in the following table.

For partially freestanding headers, freestanding implementations only needs to provide part of the entities in the corresponding synopsis:

- If an entity is commented // freestanding, it is guaranteed to be provided.

|  |  |
| --- | --- |
| - If an entity (function or function template) is commented // freestanding-deleted, it is guaranteed to be either provided or deleted. | (since C++26) |

Headers required for a freestanding implementation

| Library | Component | Headers | Freestanding |
| Language support | Common definitions | <cstddef> | All |
| C standard library | <cstdlib> | Partial |
| Implementation properties | <cfloat> <climits> (since C++11) <limits> <version> (since C++20) | All |
| Integer types | <cstdint> (since C++11) | All |
| Dynamic memory management | <new> | All |
| Type identification | <typeinfo> | All |
| Source location | <source_location> (since C++20) | All |
| Exception handling | <exception> | All |
| Initializer lists | <initializer_list> (since C++11) | All |
| Comparisons | <compare> (since C++20) | All |
| Coroutines support | <coroutine> (since C++20) | All |
| Other runtime support | <cstdarg> | All |
| Debugging support | <debugging> (since C++26) | All |
| Concepts | | <concepts> (since C++20) | All |
| Diagnostics | Error numbers | <cerrno> (since C++26) | Partial |
| System error support | <system_error> (since C++26) | Partial |
| Memory management | Memory | <memory> (since C++23) | Partial |
| Metaprogramming | Type traits | <type_traits> (since C++11) | All |
| Compile-time rational arithmetic | <ratio> (since C++23) | All |
| General utilities | Utility components | <utility> (since C++23) | All |
| Tuples | <tuple> (since C++23) | All |
| Function objects | <functional> (since C++20) | Partial |
| Primitive numeric conversions | <charconv> (since C++26) | Partial |
| Bit manipulation | <bit> (since C++20) | All |
| Strings | String classes | <string> (since C++26) | Partial |
| Null-terminated sequence utilities | <cstring> (since C++26) <cwchar> (since C++26) | Partial |
| Iterators | | <iterator> (since C++23) | Partial |
| Ranges | | <ranges> (since C++23) | Partial |
| Numerics | Mathematical functions for floating-point types | <cmath> (since C++26) | Partial |
| Concurrency support | Atomics | <atomic> (since C++11) | All[[1]](freestanding.html#cite_note-1) |
| ****Deprecated**** headers | | <ciso646> (until C++20) <cstdalign> (since C++11)(until C++20)  <cstdbool> (since C++11)(until C++20) | All |

1. ↑ Support for always lock-free integral atomic types and presence of type aliases std::atomic_signed_lock_free and std::atomic_unsigned_lock_free are implementation-defined in a freestanding implementation.(since C++20)

### Notes

Some compiler vendors may not fully support freestanding implementation. For example, GCC libstdc++ has had implementation and build issues before version 13, while LLVM libcxx and MSVC STL do not support freestanding.

In C++23, many features are made freestanding with partial headers. However, it is still up for discussion in WG21 whether some headers will be made freestanding in the future standards. Regardless, containers like vector, list, deque, and map will never be freestanding due to their dependencies on exceptions and heap.

GCC 13 provides more headers, such as <optional>, <span>, <array>, and <bitset>, for freestanding, although these headers may not be portable or provide the same capabilities as a hosted implementation. It is better to avoid using them in a freestanding environment, even if the toolchain provides them.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_freestanding_feature_test_macros` | `202306L` | (C++26) | freestanding feature test macros |
| `__cpp_lib_freestanding_algorithm` | `202311L` | (C++26) | freestanding <algorithm> |
| `__cpp_lib_freestanding_array` | `202311L` | (C++26) | freestanding <array> |
| `__cpp_lib_freestanding_char_traits` | `202306L` | (C++26) | freestanding std::char_traits |
| `__cpp_lib_freestanding_charconv` | `202306L` | (C++26) | freestanding <charconv> |
| `__cpp_lib_freestanding_cstdlib` | `202306L` | (C++26) | freestanding <cstdlib> |
| `__cpp_lib_freestanding_cstring` | `202311L` | (C++26) | freestanding <cstring> |
| `__cpp_lib_freestanding_cwchar` | `202306L` | (C++26) | freestanding <cwchar> |
| `__cpp_lib_freestanding_errc` | `202306L` | (C++26) | freestanding std::errc |
| `__cpp_lib_freestanding_expected` | `202311L` | (C++26) | freestanding <expected> |
| `__cpp_lib_freestanding_functional` | `202306L` | (C++26) | freestanding <functional> |
| `__cpp_lib_freestanding_iterator` | `202306L` | (C++26) | freestanding <iterator> |
| `__cpp_lib_freestanding_mdspan` | `202311L` | (C++26) | freestanding <mdspan> |
| `__cpp_lib_freestanding_memory` | `202306L` | (C++26) | freestanding <memory> |
| `__cpp_lib_freestanding_numeric` | `202311L` | (C++26) | freestanding <numeric> |
| `__cpp_lib_freestanding_optional` | `202311L` | (C++26) | freestanding <optional> |
| `__cpp_lib_freestanding_ranges` | `202306L` | (C++26) | freestanding <ranges> |
| `__cpp_lib_freestanding_ratio` | `202306L` | (C++26) | freestanding <ratio> |
| `__cpp_lib_freestanding_string_view` | `202311L` | (C++26) | freestanding <string_view> |
| `__cpp_lib_freestanding_tuple` | `202306L` | (C++26) | freestanding <tuple> |
| `__cpp_lib_freestanding_utility` | `202306L` | (C++26) | freestanding <utility> |
| `__cpp_lib_freestanding_variant` | `202311L` | (C++26) | freestanding <variant> |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 4.1 Implementation compliance [intro.compliance] (p: 10)

:   - 6.9.2 Multi-threaded executions and data races [intro.multithread] (p: 84)

:   - 6.9.3.1 main function [basic.start.main] (p: 89)

:   - 16.4.2.5 Freestanding implementations [compliance] (p: 483)

- C++20 standard (ISO/IEC 14882:2020):

:   - 4.1 Implementation compliance [intro.compliance] (p: 7)

:   - 6.9.2 Multi-threaded executions and data races [intro.multithread] (p: 77)

:   - 6.9.3.1 main function [basic.start.main] (p: 82)

:   - 16.5.1.3 Freestanding implementations [compliance] (p: 470)

- C++17 standard (ISO/IEC 14882:2017):

:   - 4.1 Implementation compliance [intro.compliance] (p: 5)

:   - 4.7 Multi-threaded executions and data races [intro.multithread] (p: 15)

:   - 6.6.1 main function [basic.start.main] (p: 66)

:   - 20.5.1.3 Freestanding implementations [compliance] (p: 458)

- C++14 standard (ISO/IEC 14882:2014):

:   - 1.4 Implementation compliance [intro.compliance] (p: 5)

:   - 1.10 Multi-threaded executions and data races [intro.multithread] (p: 11)

:   - 3.6.1 Main function [basic.start.main] (p: 62)

:   - 17.6.1.3 Freestanding implementations [compliance] (p: 441)

- C++11 standard (ISO/IEC 14882:2011):

:   - 1.4 Implementation compliance [intro.compliance] (p: 5)

:   - 1.10 Multi-threaded executions and data races [intro.multithread] (p: 11)

:   - 3.6.1 Main function [basic.start.main] (p: 58)

:   - 17.6.1.3 Freestanding implementations [compliance] (p: 408)

- C++03 standard (ISO/IEC 14882:2003):

:   - 1.4 Implementation compliance [intro.compliance] (p: 3)

:   - 3.6.1 Main function [basic.start.main] (p: 43)

:   - 17.4.1.3 Freestanding implementations [lib.compliance] (p: 326)

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 1938 | C++98 | an implementation did not need to document whether it is hosted | made the implementation kind implementation- defined (thus requires a documentation) |
| LWG 3653 (P1642R11) | C++20 | <coroutine> is freestanding, but uses std::hash which was not | made <functional> being  partially freestanding |

### See also

|  |  |
| --- | --- |
| C documentation for Conformance | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/freestanding&oldid=167777>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 December 2023, at 23:40.