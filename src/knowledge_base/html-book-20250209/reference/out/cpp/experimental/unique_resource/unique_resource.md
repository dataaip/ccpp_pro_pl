# std::experimental::unique_resource<R, D>::unique_resource

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
| ****unique_resource::unique_resource**** | | | | |
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
| make_unique_resource_checked | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| unique_resource(); | (1) | (library fundamentals TS v3) |
| template< class RR, class DD >  unique_resource( RR&& r, DD&& d ) noexcept(/\*see below\*/) | (2) | (library fundamentals TS v3) |
| unique_resource( unique_resource&& other ); | (3) | (library fundamentals TS v3) |
|  |  |  |

Follow items are used for explanatory purpose:

- `RS` is the type of stored resource handle.
- The expression res_ refers the underlying resource handle.
- `del_` refers the deleter object.

1) Default constructor. Value-initializes the stored resource handle and the deleter. The constructed `unique_resource` does not own the resource. This overload participates in overload resolution only if both std::is_default_constructible_v<R> and std::is_default_constructible_v<D> are true.2) The stored resource handle is initialized with std::forward<RR>(r) if std::is_nothrow_constructible_v<RS, RR> is true, otherwise r. If initialization of the stored resource handle throws an exception, calls d(r).  
Then, the deleter is initialized with std::forward<DD>(d) if std::is_nothrow_constructible_v<D, DD> is true, otherwise d. If initialization of deleter throws an exception, calls d(res_).  
The constructed `unique_resource` owns the resource. This overload participates in overload resolution only if all of std::is_constructible_v<RS, RR>, std::is_constructible_v<D, DD>, std::is_nothrow_constructible_v<RS, RR> || std::is_constructible_v<RS, RR&> and std::is_nothrow_constructible_v<D, DD> || std::is_constructible_v<D, DD&> are true. The program is ill-formed if any of the expressions d(r), d(res_) and del_(res_) is ill-formed. The behavior is undefined if any of the expressions d(r), d(res_) and del_(res_) results in undefined behavior or throws an exception.3) Move constructor. The stored resource handle is initialized from the one of other, using `std::move` if std::is_nothrow_move_constructible_v<RS> is true. If initialization of the stored resource handle throws an exception, other is not modified.  
Then, the deleter is initialized with the one of other, using `std::move` if std::is_nothrow_move_constructible_v<D> is true. If initialization of the deleter throws an exception and std::is_nothrow_move_constructible_v<RS> is true and other owns the resource, calls the deleter of other with res_ to dispose the resource, then calls other.release().  
After construction, the constructed `unique_resource` owns its resource if and only if other owned the resource before the construction, and other is set to not own the resource.

### Parameters

|  |  |  |
| --- | --- | --- |
| r | - | a resource handle |
| d | - | a deleter to use to dispose the resource |
| other | - | another `unique_resource` to acquire the ownership from |

### Exceptions

Any exception thrown during initialization of the stored resource handle or the deleter.

2)noexcept specification:noexcept((  

std::is_nothrow_constructible_v<RS, RR> || std::is_nothrow_constructible_v<RS, RR&>  
) &&  
(  
    std::is_nothrow_constructible_v<D, DD> || std::is_nothrow_constructible_v<D, DD&>

))3)noexcept specification:noexcept(  

std::is_nothrow_move_constructible_v<R1> && std::is_nothrow_move_constructible_v<D>

)

### Notes

The mechanism of these constructors ensures no leaking of resources.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a new `unique_ptr`   (public member function of `std::unique_ptr<T,Deleter>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/unique_resource/unique_resource&oldid=156352>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 August 2023, at 23:04.