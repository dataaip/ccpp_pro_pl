# std::all_of, std::any_of, std::none_of

From cppreference.com
< cpp‎ | algorithm
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

Algorithm library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Constrained algorithms and algorithms on ranges (C++20) | | | | |
| Constrained algorithms, e.g. ranges::copy, ranges::sort, ... | | | | |
| Execution policies (C++17) | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_execution_policy(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | execution::seqexecution::parexecution::par_unseqexecution::unseq(C++17)    (C++17)(C++17)(C++20) | | | | | | | |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | execution::sequenced_policyexecution::parallel_policyexecution::parallel_unsequenced_policyexecution::parallel_unsequenced(C++17)(C++17)(C++17)(C++20) | | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-modifying sequence operations | | | | | | Batch operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each_n(C++17) | | | | | | | Search operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****all_ofany_ofnone_of****(C++11)                (C++11)(C++11) | | | | | | countcount_if | | | | | | mismatch | | | | | | equal | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not(C++11) | | | | | | find_end | | | | | | find_first_of | | | | | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | | Modifying sequence operations | | | | | | Copy operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if(C++11) | | | | | | copy_backward | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copy_n(C++11) | | | | | | move(C++11) | | | | | | move_backward(C++11) | | | | | | | Swap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | iter_swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap_ranges | | | | | |  | | | | | | | Transformation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replacereplace_if | | | | | | transform | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replace_copyreplace_copy_if | | | | | |  | | | | | | | Generation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill | | | | | | fill_n | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | generate | | | | | | generate_n | | | | | | | Removing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if | | | | | | unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if | | | | | | unique_copy | | | | | | | Order-changing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse | | | | | | reverse_copy | | | | | | rotate | | | | | | rotate_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | random_shuffleshuffle(until C++17)(C++11) | | | | | | shift_leftshift_right(C++20)(C++20) | | | | | | | Sampling operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sample(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Sorting and related operations | | | | | | Partitioning operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition | | | | | | partition_copy(C++11) | | | | | | stable_partition | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned(C++11) | | | | | | partition_point(C++11) | | | | | |  | | | | | | | Sorting operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort | | | | | | partial_sort | | | | | | partial_sort_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted(C++11) | | | | | | is_sorted_until(C++11) | | | | | | nth_element | | | | | |  | | | | | | | Binary search operations (on partitioned ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound | | | | | | upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range | | | | | | binary_search | | | | | | | Set operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | includes | | | | | | set_union | | | | | | set_intersection | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference | | | | | | set_symmetric_difference | | | | | |  | | | | | | | Merge operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_merge | | | | | | | Heap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap | | | | | | pop_heap | | | | | | make_heap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort_heap | | | | | | is_heap(C++11) | | | | | | is_heap_until(C++11) | | | | | | | Minimum/maximum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max | | | | | | min | | | | | | minmax(C++11) | | | | | | clamp(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max_element | | | | | | min_element | | | | | | minmax_element(C++11) | | | | | |  | | | | | | | Lexicographical comparison operations | | | | | | lexicographical_compare | | | | | | lexicographical_compare_three_way(C++20) | | | | | | Permutation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation | | | | | | prev_permutation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation(C++11) | | | | | |  | | | | | |  | | | | | | | C library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | qsort | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bsearch | | | | | | |
| Numeric operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | adjacent_difference | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sum | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
| Operations on uninitialized memory | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n(C++11) | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_fill_n | | | | | |  | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | destroy(C++17) | | | | | | destroy_n(C++17) | | | | | | destroy_at(C++17) | | | | | | construct_at(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<algorithm>` |  |  |
| template< class InputIt, class UnaryPred >  bool all_of( InputIt first, InputIt last, UnaryPred p ); | (1) | (since C++11)  (constexpr since C++20) |
| template< class ExecutionPolicy, class ForwardIt, class UnaryPred >  bool all_of( ExecutionPolicy&& policy,              ForwardIt first, ForwardIt last, UnaryPred p ); | (2) | (since C++17) |
| template< class InputIt, class UnaryPred >  bool any_of( InputIt first, InputIt last, UnaryPred p ); | (3) | (since C++11)  (constexpr since C++20) |
| template< class ExecutionPolicy, class ForwardIt, class UnaryPred >  bool any_of( ExecutionPolicy&& policy,              ForwardIt first, ForwardIt last, UnaryPred p ); | (4) | (since C++17) |
| template< class InputIt, class UnaryPred >  bool none_of( InputIt first, InputIt last, UnaryPred p ); | (5) | (since C++11)  (constexpr since C++20) |
| template< class ExecutionPolicy, class ForwardIt, class UnaryPred >  bool none_of( ExecutionPolicy&& policy,               ForwardIt first, ForwardIt last, UnaryPred p ); | (6) | (since C++17) |
|  |  |  |

1) Checks if unary predicate p returns false for at least one element in the range ``first`,`last`)`.3) Checks if unary predicate p returns true for at least one element in the range `[`first`,`last`)`.5) Checks if unary predicate p returns true for none of the elements in the range `[`first`,`last`)`.2,4,6) Same as (1,3,5), but executed according to policy. These overloads participate in overload resolution only if all following conditions are satisfied:

|  |  |
| --- | --- |
| [std::is_execution_policy_v<std::decay_t<ExecutionPolicy>> is true. | (until C++20) |
| std::is_execution_policy_v<std::remove_cvref_t<ExecutionPolicy>> is true. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | the range of elements to examine |
| policy | - | the execution policy to use |
| p | - | unary predicate .   The expression p(v) must be convertible to bool for every argument `v` of type (possibly const) `VT`, where `VT` is the value type of `InputIt`, regardless of value category, and must not modify `v`. Thus, a parameter type of VT&is not allowed, nor is VT unless for `VT` a move is equivalent to a copy(since C++11). ​ |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |
| -`ForwardIt` must meet the requirements of LegacyForwardIterator. | | |
| -`UnaryPred` must meet the requirements of Predicate. | | |

### Return value

| Has true element | Yes | | No | |
| --- | --- | --- | --- | --- |
| Has false element | Yes | No | Yes | No[[1]](all_any_none_of.html#cite_note-1) |
| `all_of` | false | true | false | true |
| `any_of` | true | true | false | false |
| `none_of` | false | false | true | true |

1. ↑ The range is empty in this case.

### Complexity

1-6) At most std::distance(first, last) applications of the predicate p.

### Exceptions

The overloads with a template parameter named `ExecutionPolicy` report errors as follows:

- If execution of a function invoked as part of the algorithm throws an exception and `ExecutionPolicy` is one of the standard policies, std::terminate is called. For any other `ExecutionPolicy`, the behavior is implementation-defined.
- If the algorithm fails to allocate memory, std::bad_alloc is thrown.

### Possible implementation

See also the implementations of

- `all_of` in libstdc++ and libc++.
- `any_of` in libstdc++ and libc++.
- `none_of` in libstdc++ and libc++.

| all_of |
| --- |
| ```text template<class InputIt, class UnaryPred> constexpr bool all_of(InputIt first, InputIt last, UnaryPred p) {     return std::find_if_not(first, last, p) == last; } ``` |
| any_of |
| ```text template<class InputIt, class UnaryPred> constexpr bool any_of(InputIt first, InputIt last, UnaryPred p) {     return std::find_if(first, last, p) != last; } ``` |
| none_of |
| ```text template<class InputIt, class UnaryPred> constexpr bool none_of(InputIt first, InputIt last, UnaryPred p) {     return std::find_if(first, last, p) == last; } ``` |

### Example

Run this code

```
#include <algorithm>
#include <functional>
#include <iostream>
#include <iterator>
#include <numeric>
#include <vector>
 
int main()
{
    std::vector<int> v(10, 2);
    std::partial_sum(v.cbegin(), v.cend(), v.begin());
    std::cout << "Among the numbers: ";
    std::copy(v.cbegin(), v.cend(), std::ostream_iterator<int>(std::cout, " "));
    std::cout << '\n';
 
    if (std::all_of(v.cbegin(), v.cend(), [](int i) { return i % 2 == 0; }))
        std::cout << "All numbers are even\n";
 
    if (std::none_of(v.cbegin(), v.cend(), std::bind(std::modulus<>(),
                                                     std::placeholders::_1, 2)))
        std::cout << "None of them are odd\n";
 
    struct DivisibleBy
    {
        const int d;
        DivisibleBy(int n) : d(n) {}
        bool operator()(int n) const { return n % d == 0; }
    };
 
    if (std::any_of(v.cbegin(), v.cend(), DivisibleBy(7)))
        std::cout << "At least one number is divisible by 7\n";
}

```

Output:

```
Among the numbers: 2 4 6 8 10 12 14 16 18 20
All numbers are even
None of them are odd
At least one number is divisible by 7

```

### See also

|  |  |
| --- | --- |
| ranges::all_ofranges::any_ofranges::none_of(C++20)(C++20)(C++20) | checks if a predicate is true for all, any or none of the elements in a range (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/all_any_none_of&oldid=179679>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 January 2025, at 10:19.