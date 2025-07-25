# std::experimental::any_cast

From cppreference.com
< cpp‎ | experimental‎ | any
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

std::experimental::any

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| any::any | | | | |
| any::operator= | | | | |
| Modifiers | | | | |
| any::clear | | | | |
| any::swap | | | | |
| Observers | | | | |
| any::empty | | | | |
| any::type | | | | |
| Non-member functions | | | | |
| swap(std::experimental::any) | | | | |
| ****any_cast**** | | | | |

|  |  |  |
| --- | --- | --- |
| template<class ValueType>      ValueType any_cast(const any& operand); | (1) | (library fundamentals TS) |
| template<class ValueType>      ValueType any_cast(any& operand); | (2) | (library fundamentals TS) |
| template<class ValueType>      ValueType any_cast(any&& operand); | (3) | (library fundamentals TS) |
| template<class ValueType>      const ValueType\* any_cast(const any\* operand) noexcept; | (4) | (library fundamentals TS) |
| template<class ValueType>      ValueType\* any_cast(any\* operand) noexcept; | (5) | (library fundamentals TS) |
|  |  |  |

Performs type-safe access to the contained object.

For (1-3), the program is ill-formed if `ValueType` is not a reference and std::is_copy_constructible<ValueType>::value is false.

### Parameters

|  |  |  |
| --- | --- | --- |
| operand | - | target `any` object |

### Return value

1) Returns \*any_cast<std::add_const_t<std::remove_reference_t<ValueType>>>(&operand).2,3) Returns \*any_cast<std::remove_reference_t<ValueType>>(&operand).4,5) If operand is not a null pointer, and the `typeid` of the requested `ValueType` matches that of the contents of operand, a pointer to the value contained by operand, otherwise a null pointer.

### Exceptions

1-3) Throws `bad_any_cast` if the `typeid` of the requested `ValueType` does not match that of the contents of operand.
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/any/any_cast&oldid=157714>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 September 2023, at 22:30.