# std::literals::chrono_literals Symbol Index

From cppreference.com
< cpp‎ | symbol index
C++Symbol Index

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| std | | | | |
| std::chrono(C++11) | | | | |
| std::execution(C++17) | | | | |
| std::filesystem(C++17) | | | | |
| std::linalg(C++26) | | | | |
| std::literals(C++14) | | | | |
| std::numbers(C++20) | | | | |
| std::placeholders(C++11) | | | | |
| std::pmr(C++17) | | | | |
| std::ranges(C++20) | | | | |
| std::regex_constants(C++11) | | | | |
| std::rel_ops(deprecated in C++20) | | | | |
| std::this_thread(C++11) | | | | |
| Macros | | | | |
| Removed symbols (Zombie names) | | | | |
| Exposition-only symbols | | | | |

std::literals

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****std::literals::chrono_literals****(C++14) | | | | |
| std::literals::complex_literals(C++14) | | | | |
| std::literals::string_literals(C++14) | | | | |
| std::literals::string_view_literals(C++17) | | | | |

This page tries to list all the symbols that are available from the standard library (date and time library) in the namespace std::literals::chrono_literals. The symbols are written as follows:

- Function names with `()`.
- Templates with `<>`.

### Notes

These operators are declared in the namespace std::literals::chrono_literals, where both literals and chrono_literals are inline namespaces. Access to these operators can be gained with:

- using namespace std::literals,
- using namespace std::chrono_literals, or
- using namespace std::literals::chrono_literals.

In addition, within the namespace std::chrono, the directive using namespace literals::chrono_literals; is provided by the standard library, so that if a programmer uses using namespace std::chrono; to gain access to the classes in the chrono library, the corresponding literal operators become visible as well.

## `D H M N S U Y`

### D

d (since C++20)

### H

h (since C++14)

### M

min (since C++14)  
ms (since C++14)

### N

ns (since C++14)

### S

s (since C++14)

### U

us (since C++14)

### Y

y (since C++20)

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/symbol_index/chrono_literals&oldid=152256>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 May 2023, at 01:29.