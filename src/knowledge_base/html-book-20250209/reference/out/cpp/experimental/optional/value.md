# std::experimental::optional<T>::value

From cppreference.com
< cpp‎ | experimental‎ | optional
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

Library fundamentals

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::optional | | | | |
| experimental::any | | | | |
| experimental::basic_string_view | | | | |
| experimental::sample | | | | |
| experimental::shared_ptr | | | | |
| experimental::weak_ptr | | | | |
| experimental::apply | | | | |
| experimental::invocation_typeexperimental::raw_invocation_type | | | | |
| experimental::search | | | | |
| experimental::default_searcherexperimental::make_default_searcher | | | | |
| experimental::boyer_moore_searcherexperimental::make_boyer_moore_searcher | | | | |
| experimental::boyer_moore_horspool_searcherexperimental::make_boyer_moore_horspool_searcher | | | | |
| Type-erased and polymorphic allocators | | | | |
| Variable templates for type traits | | | | |

std::experimental::optional

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| optional::optional | | | | |
| optional::~optional | | | | |
| optional::operator= | | | | |
| Observers | | | | |
| optional::operator->optional::operator\* | | | | |
| optional::operator bool | | | | |
| ****optional::value**** | | | | |
| optional::value_or | | | | |
| Modifiers | | | | |
| optional::emplace | | | | |
| optional::swap | | | | |
| Non-member functions | | | | |
| operator==operator!=operator<operator<=operator>operator>= | | | | |
| make_optional | | | | |
| swap | | | | |
| Helper classes | | | | |
| hash | | | | |
| nullopt_t | | | | |
| in_place_t | | | | |
| bad_optional_access | | | | |
| Helper objects | | | | |
| nullopt | | | | |
| in_place | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr T& value() &;  constexpr const T & value() const &; | (1) | (library fundamentals TS) |
| constexpr T&& value() &&;  constexpr const T&& value() const &&; | (2) | (library fundamentals TS) |
|  |  |  |

Returns the contained value.

1) Equivalent to return bool(\*this) ? \*val : throw bad_optional_access();.2) Equivalent to return bool(\*this) ? std::move(\*val) : throw bad_optional_access();.

### Parameters

(none)

### Return value

A reference to the contained value.

### Exceptions

std::experimental::bad_optional_access if \*this does not contain a value.

### Notes

The dereference operator operator\*() does not check if this optional contains a value, which may be more efficient than `value()`.

### Example

Run this code

```
#include <experimental/optional>
#include <iostream>
 
int main()
{
    std::experimental::optional<int> opt = {};
 
    try
    {
        int n = opt.value();
    }
    catch (const std::logic_error& e)
    {
        std::cout << e.what() << '\n';
    }
}

```

Possible output:

```
optional<T>::value: not engaged

```

### See also

|  |  |
| --- | --- |
| value_or | returns the contained value if available, another value otherwise   (public member function) |
| operator->operator\* | accesses the contained value   (public member function) |
| bad_optional_access(library fundamentals TS) | exception indicating checked access to an optional that doesn't contain a value   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/optional/value&oldid=155044>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 July 2023, at 01:19.