# std::experimental::pmr::monotonic_buffer_resource::do_is_equal

From cppreference.com
< cpp‎ | experimental‎ | monotonic buffer resource
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

std::experimental::pmr::monotonic_buffer_resource

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| monotonic_buffer_resource::monotonic_buffer_resource | | | | |
| monotonic_buffer_resource::~monotonic_buffer_resource | | | | |
| Public member functions | | | | |
| monotonic_buffer_resource::release | | | | |
| monotonic_buffer_resource::upstream_resource | | | | |
| Protected member functions | | | | |
| monotonic_buffer_resource::do_allocate | | | | |
| monotonic_buffer_resource::do_deallocate | | | | |
| ****monotonic_buffer_resource::do_is_equal**** | | | | |

|  |  |  |
| --- | --- | --- |
| virtual bool do_is_equal( const memory_resource& other ) const noexcept; |  | (library fundamentals TS) |
|  |  |  |

Compare \*this with other for identity - memory allocated using a `monotonic_buffer_resource` can only be deallocated using that same resource.

### Return value

this == dynamic_cast<const monotonic_buffer_resource\*>(&other)

### See also

|  |  |
| --- | --- |
| do_is_equal[virtual] | compare for equality with another `memory_resource`   (virtual protected member function of `std::experimental::pmr::memory_resource`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/monotonic_buffer_resource/do_is_equal&oldid=155002>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 July 2023, at 06:27.