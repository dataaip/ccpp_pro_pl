# std::search_n

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-modifying sequence operations | | | | | | Batch operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each_n(C++17) | | | | | | | Search operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of(C++11)                (C++11)(C++11) | | | | | | countcount_if | | | | | | mismatch | | | | | | equal | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not(C++11) | | | | | | find_end | | | | | | find_first_of | | | | | | adjacent_find | | | | | | search | | | | | | ****search_n**** | | | | | | | Modifying sequence operations | | | | | | Copy operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if(C++11) | | | | | | copy_backward | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copy_n(C++11) | | | | | | move(C++11) | | | | | | move_backward(C++11) | | | | | | | Swap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | iter_swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap_ranges | | | | | |  | | | | | | | Transformation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replacereplace_if | | | | | | transform | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replace_copyreplace_copy_if | | | | | |  | | | | | | | Generation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill | | | | | | fill_n | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | generate | | | | | | generate_n | | | | | | | Removing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if | | | | | | unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if | | | | | | unique_copy | | | | | | | Order-changing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse | | | | | | reverse_copy | | | | | | rotate | | | | | | rotate_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | random_shuffleshuffle(until C++17)(C++11) | | | | | | shift_leftshift_right(C++20)(C++20) | | | | | | | Sampling operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sample(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Sorting and related operations | | | | | | Partitioning operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition | | | | | | partition_copy(C++11) | | | | | | stable_partition | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned(C++11) | | | | | | partition_point(C++11) | | | | | |  | | | | | | | Sorting operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort | | | | | | partial_sort | | | | | | partial_sort_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted(C++11) | | | | | | is_sorted_until(C++11) | | | | | | nth_element | | | | | |  | | | | | | | Binary search operations (on partitioned ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound | | | | | | upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range | | | | | | binary_search | | | | | | | Set operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | includes | | | | | | set_union | | | | | | set_intersection | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference | | | | | | set_symmetric_difference | | | | | |  | | | | | | | Merge operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_merge | | | | | | | Heap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap | | | | | | pop_heap | | | | | | make_heap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort_heap | | | | | | is_heap(C++11) | | | | | | is_heap_until(C++11) | | | | | | | Minimum/maximum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max | | | | | | min | | | | | | minmax(C++11) | | | | | | clamp(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max_element | | | | | | min_element | | | | | | minmax_element(C++11) | | | | | |  | | | | | | | Lexicographical comparison operations | | | | | | lexicographical_compare | | | | | | lexicographical_compare_three_way(C++20) | | | | | | Permutation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation | | | | | | prev_permutation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation(C++11) | | | | | |  | | | | | |  | | | | | | | C library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | qsort | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bsearch | | | | | | |
| Numeric operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | adjacent_difference | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sum | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
| Operations on uninitialized memory | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n(C++11) | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_fill_n | | | | | |  | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | destroy(C++17) | | | | | | destroy_n(C++17) | | | | | | destroy_at(C++17) | | | | | | construct_at(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<algorithm>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| template< class ForwardIt, class Size, class T >  ForwardIt search_n( ForwardIt first, ForwardIt last,                     Size count, const T& value ); |  | (constexpr since C++20)  (until C++26) |
| template< class ForwardIt, class Size,  class T = typename std::iterator_traits                          <ForwardIt>::value_type >  constexpr ForwardIt search_n( ForwardIt first, ForwardIt last,                               Size count, const T& value ); |  | (since C++26) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| template< class ExecutionPolicy,  class ForwardIt, class Size, class T >  ForwardIt search_n( ExecutionPolicy&& policy,                      ForwardIt first, ForwardIt last,                     Size count, const T& value ); |  | (since C++17)  (until C++26) |
| template< class ExecutionPolicy,  class ForwardIt, class Size,            class T = typename std::iterator_traits                          <ForwardIt>::value_type >  ForwardIt search_n( ExecutionPolicy&& policy,                      ForwardIt first, ForwardIt last,                     Size count, const T& value ); |  | (since C++26) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| template< class ForwardIt, class Size, class T, class BinaryPred >  ForwardIt search_n( ForwardIt first, ForwardIt last,                     Size count, const T& value, BinaryPred p ); |  | (constexpr since C++20)  (until C++26) |
| template< class ForwardIt, class Size,  class T = typename std::iterator_traits                          <ForwardIt>::value_type,            class BinaryPred >  constexpr ForwardIt search_n( ForwardIt first, ForwardIt last,                     Size count, const T& value, BinaryPred p ); |  | (since C++26) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| template< class ExecutionPolicy, class ForwardIt, class Size,  class T, class BinaryPred >  ForwardIt search_n( ExecutionPolicy&& policy,                      ForwardIt first, ForwardIt last,                     Size count, const T& value, BinaryPred p ); |  | (since C++17)  (until C++26) |
| template< class ExecutionPolicy, class ForwardIt, class Size,  class T = typename std::iterator_traits                          <ForwardIt>::value_type,            class BinaryPred >  ForwardIt search_n( ExecutionPolicy&& policy,                      ForwardIt first, ForwardIt last,                     Size count, const T& value, BinaryPred p ); |  | (since C++26) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Searches the range ``first`,`last`)` for the first sequence of count identical elements, each equal to the given value.

1) Elements are compared using operator==.3) Elements are compared using the given binary predicate p.2,4) Same as (1,3), but executed according to policy. These overloads participate in overload resolution only if all following conditions are satisfied:

|  |  |
| --- | --- |
| [std::is_execution_policy_v<std::decay_t<ExecutionPolicy>> is true. | (until C++20) |
| std::is_execution_policy_v<std::remove_cvref_t<ExecutionPolicy>> is true. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | the range of elements to examine |
| count | - | the length of the sequence to search for |
| value | - | the value of the elements to search for |
| policy | - | the execution policy to use |
| p | - | binary predicate which returns ​true if the elements should be treated as equal.   The signature of the predicate function should be equivalent to the following:   bool pred(const Type1 &a, const Type2 &b);  While the signature does not need to have const &, the function must not modify the objects passed to it and must be able to accept all values of type (possibly const) `Type1` and `Type2` regardless of value category (thus, Type1 & is not allowed, nor is Type1 unless for `Type1` a move is equivalent to a copy(since C++11)).  The type Type1 must be such that an object of type ForwardIt can be dereferenced and then implicitly converted to Type1. The type Type2 must be such that an object of type T can be implicitly converted to Type2. ​ |
| Type requirements | | |
| -`ForwardIt` must meet the requirements of LegacyForwardIterator. | | |
| -`BinaryPred` must meet the requirements of BinaryPredicate. | | |
| -`Size` must be convertible to an integral type. | | |

### Return value

If count is positive, returns an iterator to the beginning of the first sequence found in the range ``first`,`last`)`. Each iterator it in the sequence should satisfy the following condition:

1,2) \*it == value is true.3,4) p(\*it, value) != false is true.

If no such sequence is found, last is returned.

If count is zero or negative, first is returned.

### Complexity

Given \(\scriptsize N\)N as [std::distance(first, last):

1,2) At most \(\scriptsize N\)N comparisons using operator==.3,4) At most \(\scriptsize N\)N applications of the predicate p.

### Exceptions

The overloads with a template parameter named `ExecutionPolicy` report errors as follows:

- If execution of a function invoked as part of the algorithm throws an exception and `ExecutionPolicy` is one of the standard policies, std::terminate is called. For any other `ExecutionPolicy`, the behavior is implementation-defined.
- If the algorithm fails to allocate memory, std::bad_alloc is thrown.

### Possible implementation

| search_n (1) |
| --- |
| ```text template<class ForwardIt, class Size,          class T = typename std::iterator_traits<ForwardIt>::value_type> ForwardIt search_n(ForwardIt first, ForwardIt last, Size count, const T& value) {     if (count <= 0)         return first;       for (; first != last; ++first)     {         if (!(*first == value))             continue;           ForwardIt candidate = first;           for (Size cur_count = 1; true; ++cur_count)         {             if (cur_count >= count)                 return candidate; // success               ++first;             if (first == last)                 return last; // exhausted the list               if (!(*first == value))                 break; // too few in a row         }     }     return last; } ``` |
| search_n (3) |
| ```text template<class ForwardIt, class Size,          class T = typename std::iterator_traits<ForwardIt>::value_type,          class BinaryPred> ForwardIt search_n(ForwardIt first, ForwardIt last, Size count, const T& value,                    BinaryPred p) {     if (count <= 0)         return first;       for (; first != last; ++first)     {         if (!p(*first, value))             continue;           ForwardIt candidate = first;           for (Size cur_count = 1; true; ++cur_count)         {             if (cur_count >= count)                 return candidate; // success               ++first;             if (first == last)                 return last; // exhausted the list               if (!p(*first, value))                 break; // too few in a row         }     }     return last; } ``` |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_algorithm_default_value_type` | `202403` | (C++26) | List-initialization for algorithms (1-4) |

### Example

Run this code

```
#include <algorithm>
#include <cassert>
#include <complex>
#include <iostream>
#include <iterator>
#include <vector>
 
template<class Container, class Size, class T>
constexpr bool consecutive_values(const Container& c, Size count, const T& v)
{
    return std::search_n(std::begin(c), std::end(c), count, v) != std::end(c);
}
 
int main()
{
    constexpr char sequence[] = ".0_0.000.0_0.";
 
    static_assert(consecutive_values(sequence, 3, '0'));
 
    for (int n : {4, 3, 2})
        std::cout << std::boolalpha
                  << "Has " << n << " consecutive zeros: "
                  << consecutive_values(sequence, n, '0') << '\n';
 
    std::vector<std::complex<double>> nums{{4, 2}, {4, 2}, {1, 3}};
    #ifdef __cpp_lib_algorithm_default_value_type
        auto it = std::search_n(nums.cbegin(), nums.cend(), 2, {4, 2});
    #else
        auto it = std::search_n(nums.cbegin(), nums.cend(), 2, std::complex<double>{4, 2});
    #endif
    assert(it == nums.begin());
}

```

Output:

```
Has 4 consecutive zeros: false
Has 3 consecutive zeros: true
Has 2 consecutive zeros: true

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 283 | C++98 | `T` was required to be EqualityComparable, but the value type of `InputIt` is not always `T` | removed the requirement |
| LWG 426 | C++98 | the complexity upper limit was `N·count`, it is negative if count is negative | the upper limit is ​0​ if count is non-positive |
| LWG 714 | C++98 | if count > 0, the complexity upper limit was `N·count`, but in the worst case the number of comparisons/operations is always `N` | changed the upper limit to `N` in this case |
| LWG 2150 | C++98 | the condition of “sequence occurence” was incorrect | corrected |

### See also

|  |  |
| --- | --- |
| find_end | finds the last sequence of elements in a certain range   (function template) |
| findfind_iffind_if_not(C++11) | finds the first element satisfying specific criteria   (function template) |
| search | searches for the first occurrence of a range of elements   (function template) |
| ranges::search_n(C++20) | searches for the first occurrence of a number consecutive copies of an element in a range (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/search_n&oldid=171912>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 May 2024, at 21:19.