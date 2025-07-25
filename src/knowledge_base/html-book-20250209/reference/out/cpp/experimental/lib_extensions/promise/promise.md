# std::experimental::promise<R>::promise (library fundamentals TS)

From cppreference.com
< cpp‎ | experimental‎ | lib extensions‎ | promise
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

Polymorphic allocator library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| polymorphic_allocator | | | | |
| Convenience aliases for containers using `polymorphic_allocator` | | | | |
| Memory resource classes | | | | |
| memory_resource | | | | |
| synchronized_pool_resource | | | | |
| unsynchronized_pool_resource | | | | |
| monotonic_buffer_resource | | | | |
| resource_adaptor | | | | |
| Global memory resources | | | | |
| new_delete_resource | | | | |
| null_memory_resource | | | | |
| get_default_resource | | | | |
| set_default_resource | | | | |
| Type-erased allocator support for existing classes | | | | |
| function | | | | |
| packaged_task | | | | |
| promise | | | | |

|  |  |  |
| --- | --- | --- |
| promise(); | (1) | (library fundamentals TS) |
| template< class Alloc >  promise( std::allocator_arg_t, const Alloc& alloc ); | (2) | (library fundamentals TS) |
| promise( promise&& other ) noexcept; | (3) | (library fundamentals TS) |
| promise( const promise& other ) = delete; | (4) | (library fundamentals TS) |
|  |  |  |

Constructs a `std::experimental::promise` object.

1) Default constructor. Constructs the promise with an empty shared state.2) Constructs the promise with an empty shared state. The shared state is allocated using alloc, which is treated as a type-erased allocator (see below).3) Move constructor. Constructs the promise with the shared state of other using move semantics. After construction, other has no shared state.4) `std::experimental::promise` is not copyable.

### Type-erased allocator

The constructors of `promise` taking an allocator argument `alloc` treats that argument as a type-erased allocator. The memory resource pointer used by `promise` to allocate memory is determined using the allocator argument (if specified) as follows:

|  |  |
| --- | --- |
| Type of `alloc` | Value of the memory resource pointer |
| Non-existent (no allocator specified at time of construction) | The value of std::experimental::pmr::get_default_resource() at time of construction. |
| std::nullptr_t | The value of std::experimental::pmr::get_default_resource() at time of construction. |
| A pointer type convertible to std::experimental::pmr::memory_resource\* | static_cast<std::experimental::pmr::memory_resource\*>(alloc) |
| A specialization of std::experimental::pmr::polymorphic_allocator | alloc.resource() |
| Any other type meeting the Allocator requirements | A pointer to a value of type std::experimental::pmr::resource_adaptor<A>(alloc), where `A` is the type of `alloc`. The pointer remains valid only for the lifetime of the `promise` object. |
| None of the above | The program is ill-formed. |

### Parameters

|  |  |  |
| --- | --- | --- |
| alloc | - | allocator to use to allocate the shared state |
| other | - | another `std::experimental::promise` to acquire the state from |

### Exceptions

1,2) (none)
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/lib_extensions/promise/promise&oldid=157739>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 September 2023, at 22:33.