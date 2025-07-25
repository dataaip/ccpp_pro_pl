# std::experimental::pmr::polymorphic_allocator<T>::allocate

From cppreference.com
< cpp‎ | experimental‎ | polymorphic allocator
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

std::experimental::pmr::polymorphic_allocator

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| polymorphic_allocator::polymorphic_allocator | | | | |
| polymorphic_allocator::operator= | | | | |
| ****polymorphic_allocator::allocate**** | | | | |
| polymorphic_allocator::deallocate | | | | |
| polymorphic_allocator::construct | | | | |
| polymorphic_allocator::destroy | | | | |
| polymorphic_allocator::select_on_container_copy_construction | | | | |
| polymorphic_allocator::resource | | | | |
| Non-member functions | | | | |
| operator==operator!= | | | | |

|  |  |  |
| --- | --- | --- |
| T\* allocate( std::size_t n ); |  | (library fundamentals TS) |
|  |  |  |

Allocates storage for n objects of type `T` using the underlying memory resource. Equivalent to

return static_cast<T\*>(this->resource()->allocate(n \* sizeof(T), alignof(T)));.

### Parameters

|  |  |  |
| --- | --- | --- |
| n | - | the number of objects to allocate storage for |

### Return value

A pointer to the allocated storage.

### See also

|  |  |
| --- | --- |
| allocate[static] | allocates uninitialized storage using the allocator   (public static member function of `std::allocator_traits<Alloc>`) |
| deallocate | deallocates memory   (public member function of `std::experimental::pmr::memory_resource`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/polymorphic_allocator/allocate&oldid=155171>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 July 2023, at 02:52.