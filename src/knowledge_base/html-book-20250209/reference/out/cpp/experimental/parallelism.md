# Extensions for parallelism

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
| ****Extensions for parallelism**** (parallelism TS) | | | | |
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

****Extensions for parallelism****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Execution policies") | | | | |
| parallel::execution_policy") | | | | |
| parallel::sequential_execution_policyparallel::parallel_execution_policyparallel::parallel_vector_execution_policy | | | | |
| parallel::seqparallel::parparallel::par_vec | | | | |
| Parallel algorithms") | | | | |
| Parallel exceptions | | | | |
| parallel::exception_list") | | | | |
| Parallelized version of existing algorithms | | | | |
| New algorithms | | | | |
| parallel::for_eachparallel::for_each_n") | | | | |
| parallel::reduce | | | | |
| parallel::exclusive_scan") | | | | |
| parallel::inclusive_scan") | | | | |
| parallel::transform_reduce | | | | |
| parallel::transform_exclusive_scan") | | | | |
| parallel::transform_inclusive_scan") | | | | |

The C++ Extensions for Parallelism, ISO/IEC TS 19570:2015 defines the following new components for the C++ standard library:

### Execution policies

The parallelism TS describes three execution policies: sequential"), parallel"), and parallel+vector"), and provides corresponding execution policy types and objects. Users may select an execution policy statically by invoking a parallel algorithm with the an execution policy object of the corresponding type, or dynamically by using the type-erasing `execution_policy` class.

Implementations may define additional execution policies as an extension. The semantics of parallel algorithms invoked with an execution policy object of implementation-defined type is implementation-defined.

|  |  |
| --- | --- |
| Defined in header `<experimental/execution_policy>` | |
| sequential_execution_policyparallel_execution_policyparallel_vector_execution_policy | execution policy types   (class) |
| seqparpar_vec | global execution policy objects   (constant) |
| execution_policy") | dynamic execution policy   (class) |
| is_execution_policy | test whether a class represents an execution policy   (class template) |

### Exception lists

|  |  |
| --- | --- |
| Defined in header `<experimental/exception_list>` | |
| exception_list") | exceptions raised during parallel executions   (class) |

### Parallelized versions of existing algorithms

The TS provides parallelized versions of the following 69 algorithms from <algorithm>, <numeric> and <memory>:

| Standard library algorithms for which parallelized versions are provided |
| --- |
| - std::adjacent_difference - std::adjacent_find - std::all_of - std::any_of - std::copy - std::copy_if - std::copy_n - std::count - std::count_if - std::equal - std::fill - std::fill_n - std::find - std::find_end - std::find_first_of - std::find_if - std::find_if_not - std::generate - std::generate_n - std::includes - std::inner_product - std::inplace_merge - std::is_heap - std::is_heap_until - std::is_partitioned - std::is_sorted - std::is_sorted_until - std::lexicographical_compare - std::max_element - std::merge - std::min_element - std::minmax_element - std::mismatch - std::move - std::none_of - std::nth_element - std::partial_sort - std::partial_sort_copy - std::partition - std::partition_copy - std::remove - std::remove_copy - std::remove_copy_if - std::remove_if - std::replace - std::replace_copy - std::replace_copy_if - std::replace_if - std::reverse - std::reverse_copy - std::rotate - std::rotate_copy - std::search - std::search_n - std::set_difference - std::set_intersection - std::set_symmetric_difference - std::set_union - std::sort - std::stable_partition - std::stable_sort - std::swap_ranges - std::transform - std::uninitialized_copy - std::uninitialized_copy_n - std::uninitialized_fill - std::uninitialized_fill_n - std::unique - std::unique_copy |

### New algorithms

|  |  |
| --- | --- |
| Defined in header `<experimental/algorithm>` | |
| for_each") | similar to std::for_each except returns void   (function template) |
| for_each_n") | applies a function object to the first n elements of a sequence   (function template) |
| Defined in header `<experimental/numeric>` | |
| reduce(parallelism TS) | similar to std::accumulate, except out of order   (function template) |
| exclusive_scan") | similar to std::partial_sum, excludes the ith input element from the ith sum   (function template) |
| inclusive_scan") | similar to std::partial_sum, includes the ith input element in the ith sum   (function template) |
| transform_reduce(parallelism TS) | applies a functor, then reduces out of order   (function template) |
| transform_exclusive_scan") | applies a functor, then calculates exclusive scan   (function template) |
| transform_inclusive_scan") | applies a functor, then calculates inclusive scan   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/parallelism&oldid=164226>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 November 2023, at 02:11.