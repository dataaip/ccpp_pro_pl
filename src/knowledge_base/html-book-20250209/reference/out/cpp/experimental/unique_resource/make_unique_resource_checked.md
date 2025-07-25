# std::experimental::make_unique_resource_checked

From cppreference.com
< cpp‎ | experimental‎ | unique resource
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
| Filesystem library (filesystem TS) | | | | |
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

Library fundamentals v3

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::scope_exit | | | | |
| experimental::scope_fail | | | | |
| experimental::scope_success | | | | |
| experimental::unique_resource | | | | |

std::experimental::unique_resource

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| unique_resource::unique_resource | | | | |
| unique_resource::~unique_resource | | | | |
| unique_resource::operator= | | | | |
| Modifiers | | | | |
| unique_resource::release | | | | |
| unique_resource::reset | | | | |
| Observers | | | | |
| unique_resource::get | | | | |
| unique_resource::get_deleter | | | | |
| unique_resource::operator\*unique_resource::operator-> | | | | |
| Non-member functions | | | | |
| ****make_unique_resource_checked**** | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/scope>` |  |  |
| template< class R, class D, class S = std::decay_t<R> >  std::experimental::unique_resource<std::decay_t<R>, std::decay_t<D>>      make_unique_resource_checked( R&& r, const S& invalid, D&& d ) noexcept(/\*see below\*/); |  | (library fundamentals TS v3) |
|  |  |  |

Creates a `unique_resource`, initializes its stored resource handle is initialized with std::forward<R>(r) and its deleter with std::forward<D>(d). The created `unique_resource` owns the resource if and only if bool(r == invalid) is false.

The program is ill-formed if the expression r == invalid cannot be contextually converted to bool, and the behavior is undefined if the conversion results in undefined behavior or throws an exception.

### Paramaters

|  |  |  |
| --- | --- | --- |
| r | - | a resource handle |
| d | - | a deleter to use to dispose the resource |
| invalid | - | a value indicating the resource handle is invalid |

### Reture value

A `unique_resource` described above.

### Exceptions

Any exception thrown in initialization of the stored resource handle and the deleter.

noexcept specification:noexcept(  

std::is_nothrow_constructible_v<std::decay_t<R>, R> &&  
    std::is_nothrow_constructible_v<std::decay_t<D>, D>

)

### Notes

`make_unique_resource_checked` exists to avoid calling a deleter function with an invalid argument.

Resource handle r is either copied or moved into the return value, and the created `unique_resource` always holds an underlying resource handle with object type.

### Example

Run this code

```
#include <cstdio>
#include <experimental/scope>
 
int main()
{
    // avoid calling fclose when fopen fails
    auto file = std::experimental::make_unique_resource_checked(
        std::fopen("potentially_nonexistent_file.txt", "r"),
        nullptr,
        [](std::FILE *fptr) { std::fclose(fptr); }
    );
    if (file.get())
        std::puts("The file exists.");
    else
        std::puts("The file does not exist.");
}

```

Possible output:

```
The file does not exist.

```

### See also

|  |
| --- |
|  |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/unique_resource/make_unique_resource_checked&oldid=173824>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 July 2024, at 09:59.