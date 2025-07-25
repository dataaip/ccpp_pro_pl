# std::experimental::observer_ptr

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

Library fundamentals v2

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::propagate_const | | | | |
| experimental::not_fn | | | | |
| ****experimental::observer_ptr**** | | | | |
| experimental::make_array | | | | |
| experimental::to_array | | | | |
| experimental::ostream_joiner | | | | |
| experimental::gcd | | | | |
| experimental::lcm | | | | |
| experimental::source_location | | | | |
| experimental::randint | | | | |
| detection idiom | | | | |
| uniform container erasure | | | | |
| logical operator type traits | | | | |

****std::experimental::observer_ptr****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| observer_ptr::observer_ptr | | | | |
| Modifiers | | | | |
| observer_ptr::release | | | | |
| observer_ptr::reset | | | | |
| observer_ptr::swap | | | | |
| Observers | | | | |
| observer_ptr::get | | | | |
| observer_ptr::operator bool | | | | |
| observer_ptr::operator\*observer_ptr::operator-> | | | | |
| Conversions | | | | |
| observer_ptr::operator element_type\* | | | | |
| Non-member functions | | | | |
| make_observer | | | | |
| operator==operator!=operator<operator>operator<=operator>operator>= | | | | |
| swap | | | | |
| std::hash | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/memory>` |  |  |
| template< class W >  class observer_ptr; |  | (library fundamentals TS v2) |
|  |  |  |

`std::experimental::observer_ptr` is a non-owning pointer, or **observer**. The observer stores a pointer to a second object, known as the **watched object**. An `observer_ptr` may also have no watched object.

An observer is not responsible in any way for the watched object; there is no inherent relationship between an observer and the object it watches.

It is intended as a near drop-in replacement for raw pointer types, with the advantage that, as a vocabulary type, it indicates its intended use without need for detailed analysis by code readers.

Specializations of `observer_ptr` satisfy the requirements of CopyConstructible and CopyAssignable.

|  |  |  |
| --- | --- | --- |
| Type requirements | | |
| -`W` shall not be a reference type, but may be an incomplete type. | | |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| element_type | `W`, the type of the object watched by this `observer_ptr` |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new `observer_ptr`   (public member function) |
| (destructor)(implicitly declared) | destructs an `observer_ptr`   (public member function) |
| operator=(implicitly declared) | implicitly declared copy and move assignment operators that assign the stored pointer   (public member function) |
| Modifiers | |
| release | returns a pointer to the watched object and stops watching the object   (public member function) |
| reset | replaces the watched object   (public member function) |
| swap | swaps the watched objects   (public member function) |
| Observers | |
| get | returns a pointer to the watched object   (public member function) |
| operator bool | checks if there is an associated watched object   (public member function) |
| operator\*operator-> | dereferences pointer to the watched object   (public member function) |
| Conversions | |
| operator element_type\* | explicit conversion function to the stored pointer   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| make_observer | creates an `observer_ptr` that watches an object   (function template) |
| operator==operator!=operator<operator<=operator>operator>= | compares to another `observer_ptr` or with nullptr   (function template) |
| std::experimental::swap(std::experimental::observer_ptr) | specializes the `swap` algorithm   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::hash<std::experimental::observer_ptr> | hash support for `observer_ptr`   (class template specialization) |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/observer_ptr&oldid=164180>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 November 2023, at 01:11.