# std::experimental::function<R(Args...)>::operator=

From cppreference.com
< cpp‎ | experimental‎ | function
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
| function& operator=( const function& other ); | (1) | (library fundamentals TS) |
| function& operator=( function&& other ); | (2) | (library fundamentals TS) |
| function& operator=( std::nullptr_t ) noexcept; | (3) | (library fundamentals TS) |
| template< class F >  function& operator=( F&& f ); | (4) | (library fundamentals TS) |
|  |  |  |
| --- | --- | --- |
|  | (5) |  |
| template< class F >  function& operator=( std::reference_wrapper<F> f ); |  | (library fundamentals TS) |
| template< class F >  function& operator=( std::reference_wrapper<F> f ) noexcept; |  | (library fundamentals TS v3) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Assigns a new **target** to `std::experimental::function`. In the description below, let ALLOCATOR_OF(f) be the allocator specified in the construction of f, or the value of std::experimental::pmr::get_default_resource()(until library fundamentals TS v3)the default-constructed std::pmr::polymorphic_allocator<> value(library fundamentals TS v3) at the time of construction if no allocator was specified.

1) Assigns a copy of **target** of other, as if by executing function(std::allocator_arg, ALLOCATOR_OF(\*this), other).swap(\*this);.2) Moves the **target** of other to \*this, as if by executing function(std::allocator_arg, ALLOCATOR_OF(\*this), std::move(other)).swap(\*this);. other is in a valid state with an unspecified value.3) Destroys the **target** of \*this. \*this is **empty** after the call. The memory resource returned by `get_memory_resource()` after the assignment is equivalent to the memory resource before the assignment, but the address may change.4) Sets the **target** of \*this to the callable f, as if by executing function(std::allocator_arg, ALLOCATOR_OF(\*this),std::forward<F>(f)).swap(\*this);. This operator does not participate in overload resolution unless f is Callable for argument types `Args...` and return type `R`.5) Sets the **target** of \*this to a copy of f, as if by executing function(std::allocator_arg, ALLOCATOR_OF(\*this), f).swap(\*this);.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another `std::experimental::function` object to copy or move from |
| f | - | a callable to initialize the **target** with |
| Type requirements | | |
| -`F` must meet the requirements of Callable. | | |

### Return value

\*this

### Exceptions

1,2,4) Exception thrown on needed allocation of the storage or initialization of the target of \*this, if any.5) (none)

### Notes

The move assignment operator may need to allocate storage if get_memory_resource() != other.get_memory_resource()(until library fundamentals TS v3)get_allocator() != other.get_allocator()(library fundamentals TS v3)

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/function/operator%3D&oldid=154959>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 July 2023, at 23:19.