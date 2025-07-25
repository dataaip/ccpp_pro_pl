# std::experimental::unique_resource

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

Library fundamentals v3

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::scope_exit | | | | |
| experimental::scope_fail | | | | |
| experimental::scope_success | | | | |
| ****experimental::unique_resource**** | | | | |

****std::experimental::unique_resource****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| unique_resource::unique_resource | | | | |
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
| Defined in header `<experimental/scope>` |  |  |
| template< class R, class D >  class unique_resource; |  | (library fundamentals TS v3) |
|  |  |  |

`unique_resource` is universal RAII wrapper for resource handles that owns and manages a resource through a handle and disposes of that resource when the `unique_resource` is destroyed.

The resource is disposed of using the deleter of type `D` when either of the following happens:

- the managing `unique_resource` object is destroyed,
- the managing `unique_resource` object is assigned from another resource via operator= or reset().

Let type `RS` be `R` if `R` is an object type, or std::reference_wrapper<std::remove_reference_t<R>> otherwise:

- `unique_resource` effectively holds a subobject of type `RS` which is or wraps the resource handle, a deleter of type `D` and a bool flag indicating whether the wrapper is owning the resource.
- For explanatory purpose, the subobject of type `RS` is called **stored resource handle**, and the stored (if `R` is an object type) or wrapped (if `R` is a reference type) `R` is called **underlying resource handle**. These two terms are not used by the LFTS.

### Template parameters

|  |  |  |
| --- | --- | --- |
| R | - | resource handle type |
| D | - | deleter type |
| Type requirements | | |
| -`R` shall be an object type or an lvalue reference to an object type. Let `UnrefR` be std::remove_reference_t<R>, `UnrefR` shall be MoveConstructible, and if `UnrefR` is not CopyConstructible, std::is_nothrow_move_constructible_v<UnrefR> shall be true. | | |
| -`D` shall be a Destructible and MoveConstructible FunctionObject type, and if `D` is not CopyConstructible, std::is_nothrow_move_constructible_v<D> shall be true. Given an lvalue `d` of type `D` and an lvalue `r` of type `UnrefR`, the expression d(r) shall be well-formed. | | |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new `unique_resource`   (public member function) |
| (destructor) | disposes the managed resource if such is present   (public member function) |
| operator= | assigns a `unique_resource`   (public member function) |
| Modifiers | |
| release | releases the ownership   (public member function) |
| reset | disposes or replaces the managed resource   (public member function) |
| Observers | |
| get | accesses the underlying resource handle   (public member function) |
| get_deleter | accesses the deleter used for disposing of the managed resource   (public member function) |
| operator\*operator-> | accesses the pointee if the resource handle is a pointer   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| make_unique_resource_checked | creates a `unique_resource`, checking invalid value   (function template) |

### Deduction guides

### Notes

Resource handle types satisfying NullablePointer can also be managed by std::unique_ptr. Unlike `unique_ptr`, `unique_resource` does not require NullablePointer.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| unique_ptr(C++11) | smart pointer with unique object ownership semantics   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/unique_resource&oldid=156343>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 August 2023, at 05:43.