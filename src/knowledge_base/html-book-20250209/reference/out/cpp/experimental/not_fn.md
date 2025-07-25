# std::experimental::not_fn

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
| ****experimental::not_fn**** | | | | |
| experimental::observer_ptr | | | | |
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

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/functional>` |  |  |
| template< class F>  /\*unspecified\*/ not_fn( F&& f ); |  | (library fundamentals TS v2) |
|  |  |  |

Creates a forwarding call wrapper that returns the complement of the callable object it holds.

### Parameters

|  |  |  |
| --- | --- | --- |
| f | - | the object from which the Callable object held by the wrapper is constructed |

### Return value

Let `FD` be std::decay_t<F> and `fd` be an lvalue of type `FD` constructed from std::forward<F>(f).

`not_fn` returns a forwarding call wrapper `fn` of unspecified type such that fn(a1, a2, ..., aN) is equivalent to !INVOKE(fd, a1, ..., aN), where `INVOKE` is the operation described in Callable.

The returned call wrapper is always MoveConstructible, and is CopyConstructible if FD is CopyConstructible.

### Remarks

If `fd` is not Callable, or std::is_constructible<FD, F>::value is not `true`, the behavior is undefined.

### Exceptions

Throws no exceptions, unless the construction of `fd` throws.

### Possible implementation

|  |
| --- |
| ```text namespace detail {     template<class F>     struct not_fn_t {         F f;         template<class... Args>         auto operator()(Args&&... args)             noexcept(noexcept(!std::invoke(f, std::forward<Args>(args)...)))             -> decltype(!std::invoke(f, std::forward<Args>(args)...)) {             return !std::invoke(f, std::forward<Args>(args)...);         }           // cv-qualified overload for QoI         template<class... Args>         auto operator()(Args&&... args) const             noexcept(noexcept(!std::invoke(f, std::forward<Args>(args)...)))             -> decltype(!std::invoke(f, std::forward<Args>(args)...)) {             return !std::invoke(f, std::forward<Args>(args)...);         }           template<class... Args>         auto operator()(Args&&... args) volatile             noexcept(noexcept(!std::invoke(f, std::forward<Args>(args)...)))             -> decltype(!std::invoke(f, std::forward<Args>(args)...)) {             return !std::invoke(f, std::forward<Args>(args)...);         }         template<class... Args>         auto operator()(Args&&... args) const volatile             noexcept(noexcept(!std::invoke(f, std::forward<Args>(args)...)))             -> decltype(!std::invoke(f, std::forward<Args>(args)...)) {             return !std::invoke(f, std::forward<Args>(args)...);         }     }; }   template<class F> detail::not_fn_t<std::decay_t<F>> not_fn(F&& f) { return { std::forward<F>(f) }; } ``` |

### Notes

`not_fn` is intended to replace the C++03-era negators std::not1 and std::not2.

### See also

|  |  |
| --- | --- |
| not_fn(C++17) | creates a function object that returns the complement of the result of the function object it holds   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/not_fn&oldid=103392>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 June 2018, at 14:39.