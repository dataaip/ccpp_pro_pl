# std::mismatch

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-modifying sequence operations | | | | | | Batch operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each_n(C++17) | | | | | | | Search operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of(C++11)                (C++11)(C++11) | | | | | | countcount_if | | | | | | ****mismatch**** | | | | | | equal | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not(C++11) | | | | | | find_end | | | | | | find_first_of | | | | | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | | Modifying sequence operations | | | | | | Copy operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if(C++11) | | | | | | copy_backward | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copy_n(C++11) | | | | | | move(C++11) | | | | | | move_backward(C++11) | | | | | | | Swap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | iter_swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap_ranges | | | | | |  | | | | | | | Transformation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replacereplace_if | | | | | | transform | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replace_copyreplace_copy_if | | | | | |  | | | | | | | Generation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill | | | | | | fill_n | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | generate | | | | | | generate_n | | | | | | | Removing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if | | | | | | unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if | | | | | | unique_copy | | | | | | | Order-changing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse | | | | | | reverse_copy | | | | | | rotate | | | | | | rotate_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | random_shuffleshuffle(until C++17)(C++11) | | | | | | shift_leftshift_right(C++20)(C++20) | | | | | | | Sampling operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sample(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Sorting and related operations | | | | | | Partitioning operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition | | | | | | partition_copy(C++11) | | | | | | stable_partition | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned(C++11) | | | | | | partition_point(C++11) | | | | | |  | | | | | | | Sorting operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort | | | | | | partial_sort | | | | | | partial_sort_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted(C++11) | | | | | | is_sorted_until(C++11) | | | | | | nth_element | | | | | |  | | | | | | | Binary search operations (on partitioned ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound | | | | | | upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range | | | | | | binary_search | | | | | | | Set operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | includes | | | | | | set_union | | | | | | set_intersection | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference | | | | | | set_symmetric_difference | | | | | |  | | | | | | | Merge operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_merge | | | | | | | Heap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap | | | | | | pop_heap | | | | | | make_heap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort_heap | | | | | | is_heap(C++11) | | | | | | is_heap_until(C++11) | | | | | | | Minimum/maximum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max | | | | | | min | | | | | | minmax(C++11) | | | | | | clamp(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max_element | | | | | | min_element | | | | | | minmax_element(C++11) | | | | | |  | | | | | | | Lexicographical comparison operations | | | | | | lexicographical_compare | | | | | | lexicographical_compare_three_way(C++20) | | | | | | Permutation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation | | | | | | prev_permutation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation(C++11) | | | | | |  | | | | | |  | | | | | | | C library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | qsort | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bsearch | | | | | | |
| Numeric operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | adjacent_difference | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sum | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
| Operations on uninitialized memory | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n(C++11) | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_fill_n | | | | | |  | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | destroy(C++17) | | | | | | destroy_n(C++17) | | | | | | destroy_at(C++17) | | | | | | construct_at(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<algorithm>` |  |  |
| template< class InputIt1, class InputIt2 >  std::pair<InputIt1, InputIt2>      mismatch( InputIt1 first1, InputIt1 last1,               InputIt2 first2 ); | (1) | (constexpr since C++20) |
| template< class ExecutionPolicy, class ForwardIt1, class ForwardIt2 >  std::pair<ForwardIt1, ForwardIt2>      mismatch( ExecutionPolicy&& policy,                ForwardIt1 first1, ForwardIt1 last1,               ForwardIt2 first2 ); | (2) | (since C++17) |
| template< class InputIt1, class InputIt2, class BinaryPred >  std::pair<InputIt1, InputIt2>      mismatch( InputIt1 first1, InputIt1 last1,               InputIt2 first2, BinaryPred p ); | (3) | (constexpr since C++20) |
| template< class ExecutionPolicy,  class ForwardIt1, class ForwardIt2, class BinaryPred >  std::pair<ForwardIt1, ForwardIt2>      mismatch( ExecutionPolicy&& policy,                ForwardIt1 first1, ForwardIt1 last1,               ForwardIt2 first2, BinaryPred p ); | (4) | (since C++17) |
| template< class InputIt1, class InputIt2 >  std::pair<InputIt1, InputIt2>      mismatch( InputIt1 first1, InputIt1 last1,               InputIt2 first2, InputIt2 last2 ); | (5) | (since C++14)  (constexpr since C++20) |
| template< class ExecutionPolicy, class ForwardIt1, class ForwardIt2 >  std::pair<ForwardIt1, ForwardIt2>      mismatch( ExecutionPolicy&& policy,                ForwardIt1 first1, ForwardIt1 last1,               ForwardIt2 first2, ForwardIt2 last2 ); | (6) | (since C++17) |
| template< class InputIt1, class InputIt2, class BinaryPred >  std::pair<InputIt1, InputIt2>      mismatch( InputIt1 first1, InputIt1 last1,               InputIt2 first2, InputIt2 last2, BinaryPred p ); | (7) | (since C++14)  (constexpr since C++20) |
| template< class ExecutionPolicy,  class ForwardIt1, class ForwardIt2, class BinaryPred >  std::pair<ForwardIt1, ForwardIt2>      mismatch( ExecutionPolicy&& policy,                ForwardIt1 first1, ForwardIt1 last1,               ForwardIt2 first2, ForwardIt2 last2, BinaryPred p ); | (8) | (since C++17) |
|  |  |  |

Returns a pair of iterators to the first mismatching of elements from ``first1`,`last1`)` and a range starting from first2:

- For overloads (1-4), the second range has [std::distance(first1, last1) elements.
- For overloads (5-8), the second range is ``first2`,`last2`)`.

:   - If [std::distance(first1, last1) and std::distance(first2, last2) are different, the comparison stops when last1 or last2 is reached.

1,5) Elements are compared using operator==.3,7) Elements are compared using the given binary predicate p.2,4,6,8) Same as (1,3,5,7), but executed according to policy. These overloads participate in overload resolution only if all following conditions are satisfied:

|  |  |
| --- | --- |
| std::is_execution_policy_v<std::decay_t<ExecutionPolicy>> is true. | (until C++20) |
| std::is_execution_policy_v<std::remove_cvref_t<ExecutionPolicy>> is true. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| first1, last1 | - | the first range of the elements |
| first2, last2 | - | the second range of the elements |
| policy | - | the execution policy to use |
| p | - | binary predicate which returns ​true if the elements should be treated as equal.   The signature of the predicate function should be equivalent to the following:   bool pred(const Type1 &a, const Type2 &b);  While the signature does not need to have const &, the function must not modify the objects passed to it and must be able to accept all values of type (possibly const) `Type1` and `Type2` regardless of value category (thus, Type1 & is not allowed, nor is Type1 unless for `Type1` a move is equivalent to a copy(since C++11)).  The types Type1 and Type2 must be such that objects of types InputIt1 and InputIt2 can be dereferenced and then implicitly converted to Type1 and Type2 respectively. ​ |
| Type requirements | | |
| -`InputIt1` must meet the requirements of LegacyInputIterator. | | |
| -`InputIt2` must meet the requirements of LegacyInputIterator. | | |
| -`ForwardIt1` must meet the requirements of LegacyForwardIterator. | | |
| -`ForwardIt2` must meet the requirements of LegacyForwardIterator. | | |
| -`BinaryPred` must meet the requirements of BinaryPredicate. | | |

### Return value

std::pair with iterators to the first two non-equal elements.

If last1 is reached, the second iterator in the pair is the std::distance(first1, last1)th iterator after first2.

For overloads (5-8), if last2 is reached, the first iterator in the pair is the std::distance(first2, last2)th iterator after first1.

### Complexity

Given \(\scriptsize N_1\)N1 as std::distance(first1, last1) and \(\scriptsize N_2\)N2 as std::distance(first2, last2):

1,2) At most \(\scriptsize N_1\)N1 comparisons using operator==.3,4) At most \(\scriptsize N_1\)N1 applications of the predicate p.5,6) At most \(\scriptsize \min(N_1,N_2)\)min(N1,N2) comparisons using operator==.7,8) At most \(\scriptsize \min(N_1,N_2)\)min(N1,N2) applications of the predicate p.

### Exceptions

The overloads with a template parameter named `ExecutionPolicy` report errors as follows:

- If execution of a function invoked as part of the algorithm throws an exception and `ExecutionPolicy` is one of the standard policies, std::terminate is called. For any other `ExecutionPolicy`, the behavior is implementation-defined.
- If the algorithm fails to allocate memory, std::bad_alloc is thrown.

### Possible implementation

| mismatch (1) |
| --- |
| ```text template<class InputIt1, class InputIt2> std::pair<InputIt1, InputIt2>     mismatch(InputIt1 first1, InputIt1 last1, InputIt2 first2) {     while (first1 != last1 && *first1 == *first2)         ++first1, ++first2;       return std::make_pair(first1, first2); } ``` |
| mismatch (3) |
| ```text template<class InputIt1, class InputIt2, class BinaryPred> std::pair<InputIt1, InputIt2>     mismatch(InputIt1 first1, InputIt1 last1, InputIt2 first2, BinaryPred p) {     while (first1 != last1 && p(*first1, *first2))         ++first1, ++first2;       return std::make_pair(first1, first2); } ``` |
| mismatch (5) |
| ```text template<class InputIt1, class InputIt2> std::pair<InputIt1, InputIt2>     mismatch(InputIt1 first1, InputIt1 last1, InputIt2 first2, InputIt2 last2) {     while (first1 != last1 && first2 != last2 && *first1 == *first2)         ++first1, ++first2;       return std::make_pair(first1, first2); } ``` |
| mismatch (7) |
| ```text template<class InputIt1, class InputIt2, class BinaryPred> std::pair<InputIt1, InputIt2>     mismatch(InputIt1 first1, InputIt1 last1,              InputIt2 first2, InputIt2 last2, BinaryPred p) {     while (first1 != last1 && first2 != last2 && p(*first1, *first2))         ++first1, ++first2;       return std::make_pair(first1, first2); } ``` |

### Example

This program determines the longest substring that is simultaneously found at the very beginning of the given string and at the very end of it, in reverse order (possibly overlapping).

Run this code

```
#include <algorithm>
#include <iostream>
#include <string>
 
std::string mirror_ends(const std::string& in)
{
    return std::string(in.begin(),
                       std::mismatch(in.begin(), in.end(), in.rbegin()).first);
}
 
int main()
{
    std::cout << mirror_ends("abXYZba") << '\n'
              << mirror_ends("abca") << '\n'
              << mirror_ends("aba") << '\n';
}

```

Output:

```
ab
a
aba

```

### See also

|  |  |
| --- | --- |
| equal | determines if two sets of elements are the same   (function template) |
| findfind_iffind_if_not(C++11) | finds the first element satisfying specific criteria   (function template) |
| lexicographical_compare | returns true if one range is lexicographically less than another   (function template) |
| search | searches for the first occurrence of a range of elements   (function template) |
| ranges::mismatch(C++20) | finds the first position where two ranges differ (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/mismatch&oldid=170579>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 April 2024, at 01:37.