# std::experimental::shared_ptr<T>::operator\*, std::experimental::shared_ptr<T>::operator->

From cppreference.com
< cpp‎ | experimental‎ | shared ptr
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

std::experimental::shared_ptr

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| shared_ptr::shared_ptr | | | | |
| shared_ptr::get | | | | |
| ****shared_ptr::operator\*shared_ptr::operator->**** | | | | |
| [shared_ptr::operator[]](operator_at.html "cpp/experimental/shared ptr/operator at") | | | | |
| Non-member functions | | | | |
| experimental::static_pointer_castexperimental::dynamic_pointer_castexperimental::const_pointer_castexperimental::reinterpret_pointer_cast | | | | |
| std::hash | | | | |
| Members and non-members identical to those of `std::shared_ptr` | | | | |

|  |  |  |
| --- | --- | --- |
| T& operator\*() const noexcept; | (1) | (library fundamentals TS) |
| T\* operator->() const noexcept; | (2) | (library fundamentals TS) |
|  |  |  |

Dereferences the stored pointer. The behavior is undefined if the stored pointer is null.

### Parameters

(none)

### Return value

1) The result of dereferencing the stored pointer, i.e., \*get().2) The stored pointer, i.e., get().

### Remarks

When `T` is an array type or (possibly cv-qualified) void, it is unspecified whether function (1) is declared.

When `T` is an array type, it is unspecified whether function (2) is declared.

In either case, if the function is declared, it is unspecified what its return type is, except that the declaration (although not necessarily the definition) of the function is guaranteed to be legal.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| get | returns the stored pointer   (public member function) |

Retrieved from "https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/shared_ptr/operator\*&oldid=155808"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 July 2023, at 09:11.