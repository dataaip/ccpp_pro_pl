# std::experimental::pmr::polymorphic_allocator

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
| ****polymorphic_allocator**** | | | | |
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

****std::experimental::pmr::polymorphic_allocator****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| polymorphic_allocator::polymorphic_allocator | | | | |
| polymorphic_allocator::operator= | | | | |
| polymorphic_allocator::allocate | | | | |
| polymorphic_allocator::deallocate | | | | |
| polymorphic_allocator::construct | | | | |
| polymorphic_allocator::destroy | | | | |
| polymorphic_allocator::select_on_container_copy_construction | | | | |
| polymorphic_allocator::resource | | | | |
| Non-member functions | | | | |
| operator==operator!= | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/memory_resource>` |  |  |
| template< class T >  class polymorphic_allocator; |  | (library fundamentals TS) |
|  |  |  |

The class template `std::experimental::pmr::polymorphic_allocator` is an Allocator whose allocation behavior depends on the memory resource it is constructed with. Thus, different instances of `polymorphic_allocator` can exhibit entirely different allocation behavior. This runtime polymorphism allows objects using `polymorphic_allocator` to behave as if they used different allocator types at run time despite the identical static allocator type.

### Member types

|  |  |
| --- | --- |
| Member type | definition |
| `value_type` | `T` |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `polymorphic_allocator`   (public member function) |
| (destructor)(implicitly declared) | implicitly declared destructor   (public member function) |
| operator= | copy assignment operator   (public member function) |
| Public member functions | |
| allocate | allocate memory   (public member function) |
| deallocate | deallocate memory   (public member function) |
| construct | constructs an object in allocated storage   (public member function) |
| destroy | destroys an object in allocated storage   (public member function) |
| select_on_container_copy_construction | create a new `polymorphic_allocator` for use by a container's copy constructor   (public member function) |
| resource | returns a pointer to the underlying memory resource   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!= | compare two `polymorphic_allocator`s   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/polymorphic_allocator&oldid=164234>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 November 2023, at 07:29.