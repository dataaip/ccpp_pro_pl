# std::ranges::all_of, std::ranges::any_of, std::ranges::none_of

From cppreference.com
< cpp‎ | algorithm‎ | ranges
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-modifying sequence operations | | | | | | Batch operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each_n(C++17) | | | | | | | Search operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of(C++11)                (C++11)(C++11) | | | | | | countcount_if | | | | | | mismatch | | | | | | equal | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not(C++11) | | | | | | find_end | | | | | | find_first_of | | | | | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | | Modifying sequence operations | | | | | | Copy operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if(C++11) | | | | | | copy_backward | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copy_n(C++11) | | | | | | move(C++11) | | | | | | move_backward(C++11) | | | | | | | Swap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | iter_swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap_ranges | | | | | |  | | | | | | | Transformation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replacereplace_if | | | | | | transform | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replace_copyreplace_copy_if | | | | | |  | | | | | | | Generation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill | | | | | | fill_n | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | generate | | | | | | generate_n | | | | | | | Removing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if | | | | | | unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if | | | | | | unique_copy | | | | | | | Order-changing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse | | | | | | reverse_copy | | | | | | rotate | | | | | | rotate_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | random_shuffleshuffle(until C++17)(C++11) | | | | | | shift_leftshift_right(C++20)(C++20) | | | | | | | Sampling operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sample(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Sorting and related operations | | | | | | Partitioning operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition | | | | | | partition_copy(C++11) | | | | | | stable_partition | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned(C++11) | | | | | | partition_point(C++11) | | | | | |  | | | | | | | Sorting operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort | | | | | | partial_sort | | | | | | partial_sort_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted(C++11) | | | | | | is_sorted_until(C++11) | | | | | | nth_element | | | | | |  | | | | | | | Binary search operations (on partitioned ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound | | | | | | upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range | | | | | | binary_search | | | | | | | Set operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | includes | | | | | | set_union | | | | | | set_intersection | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference | | | | | | set_symmetric_difference | | | | | |  | | | | | | | Merge operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_merge | | | | | | | Heap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap | | | | | | pop_heap | | | | | | make_heap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort_heap | | | | | | is_heap(C++11) | | | | | | is_heap_until(C++11) | | | | | | | Minimum/maximum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max | | | | | | min | | | | | | minmax(C++11) | | | | | | clamp(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max_element | | | | | | min_element | | | | | | minmax_element(C++11) | | | | | |  | | | | | | | Lexicographical comparison operations | | | | | | lexicographical_compare | | | | | | lexicographical_compare_three_way(C++20) | | | | | | Permutation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation | | | | | | prev_permutation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation(C++11) | | | | | |  | | | | | |  | | | | | | | C library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | qsort | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bsearch | | | | | | |
| Numeric operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | adjacent_difference | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sum | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
| Operations on uninitialized memory | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n(C++11) | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_fill_n | | | | | |  | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | destroy(C++17) | | | | | | destroy_n(C++17) | | | | | | destroy_at(C++17) | | | | | | construct_at(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | |

Constrained algorithmsAll names in this menu belong to namespace `std::ranges`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Non-modifying sequence operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****all_ofany_ofnone_of**** | | | | | | for_each | | | | | | for_each_n | | | | | | countcount_if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_find | | | | | | mismatch | | | | | | equal | | | | | | lexicographical_compare | | | | | | containscontains_subrange(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not | | | | | | find_lastfind_last_iffind_last_if_not(C++23)(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | find_end | | | | | | find_first_of | | | | | | search | | | | | | search_n | | | | | | starts_with(C++23) | | | | | | ends_with(C++23) | | | | | |  | | | | | | |
| Modifying sequence operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if | | | | | | copy_n | | | | | | copy_backward | | | | | | move | | | | | | move_backward | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | shift_leftshift_right(C++23)(C++23) | | | | | | fill | | | | | | fill_n | | | | | | generate | | | | | | generate_n | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform | | | | | | swap_ranges | | | | | | shuffle | | | | | | sample | | | | | | removeremove_if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replacereplace_if | | | | | | reverse | | | | | | rotate | | | | | | remove_copyremove_copy_if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | unique | | | | | | replace_copyreplace_copy_if | | | | | | reverse_copy | | | | | | rotate_copy | | | | | | unique_copy | | | | | | |
| Partitioning operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition_point | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stable_partition | | | | | | |
| Sorting operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted | | | | | | is_sorted_until | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sort | | | | | | nth_element | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sort_copy | | | | | |  | | | | | | |
| Binary search operations (on sorted ranges) | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | binary_search | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range | | | | | | |
| Set operations (on sorted ranges) | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge | | | | | | inplace_merge | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference | | | | | | set_intersection | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_union | | | | | | includes | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_symmetric_difference | | | | | |  | | | | | | |
| Heap operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_heap | | | | | | is_heap_until | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | make_heap | | | | | | sort_heap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap | | | | | | pop_heap | | | | | | |
| Minimum/maximum operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max | | | | | | max_element | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | min | | | | | | min_element | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | minmax | | | | | | minmax_element | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clamp | | | | | |  | | | | | | |
| Permutation operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | prev_permutation | | | | | | |
| Fold operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fold_left(C++23) | | | | | | fold_left_first(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fold_right(C++23) | | | | | | fold_right_last(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fold_left_with_iter(C++23) | | | | | | fold_left_first_with_iter(C++23) | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Numeric operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++23) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random number generation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | generate_random(C++26) | | | | | | | |
| Operations on uninitialized storage | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | construct_at | | | | | | destroy | | | | | | destroy_n | | | | | | destroy_at | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n | | | | | | uninitialized_move_n | | | | | | uninitialized_fill_n | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct | | | | | | uninitialized_default_construct_n | | | | | | uninitialized_value_construct | | | | | | uninitialized_value_construct_n | | | | | | |
| Return types | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | in_fun_result | | | | | | in_in_result | | | | | | in_found_result | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | in_out_result | | | | | | in_in_out_result | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | in_out_out_result | | | | | | min_max_result | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | out_value_result(C++23) | | | | | | in_value_result(C++23) | | | | | |  | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<algorithm>` |  |  |
| Call signature |  |  |
| template< std::input_iterator I, std::sentinel_for<I> S,  class Proj = std::identity,            std::indirect_unary_predicate<std::projected<I, Proj>> Pred > constexpr bool all_of( I first, S last, Pred pred, Proj proj = {} ); | (1) | (since C++20) |
| template< ranges::input_range R, class Proj = std::identity,  std::indirect_unary_predicate<                std::projected<ranges::iterator_t<R>,Proj>> Pred > constexpr bool all_of( R&& r, Pred pred, Proj proj = {} ); | (2) | (since C++20) |
| template< std::input_iterator I, std::sentinel_for<I> S,  class Proj = std::identity,            std::indirect_unary_predicate<std::projected<I, Proj>> Pred > constexpr bool any_of( I first, S last, Pred pred, Proj proj = {} ); | (3) | (since C++20) |
| template< ranges::input_range R, class Proj = std::identity,  std::indirect_unary_predicate<                std::projected<ranges::iterator_t<R>,Proj>> Pred > constexpr bool any_of( R&& r, Pred pred, Proj proj = {} ); | (4) | (since C++20) |
| template< std::input_iterator I, std::sentinel_for<I> S,  class Proj = std::identity,            std::indirect_unary_predicate<std::projected<I, Proj>> Pred > constexpr bool none_of( I first, S last, Pred pred, Proj proj = {} ); | (5) | (since C++20) |
| template< ranges::input_range R, class Proj = std::identity,  std::indirect_unary_predicate<                std::projected<ranges::iterator_t<R>,Proj>> Pred > constexpr bool none_of( R&& r, Pred pred, Proj proj = {} ); | (6) | (since C++20) |
|  |  |  |

1) Checks if unary predicate pred returns false for at least one element in the range ``first`,`last`)` (after projecting with the projection proj).3) Checks if unary predicate pred returns true for at least one element in the range `[`first`,`last`)` (after projecting with the projection proj).5) Checks if unary predicate pred returns true for none of the elements in the range `[`first`,`last`)` (after projecting with the projection proj).2,4,6) Same as (1,3,5), but uses r as the source range, as if using [ranges::begin(r) as first and ranges::end(r) as last.

The function-like entities described on this page are **algorithm function objects** (informally known as **niebloids**), that is:

- Explicit template argument lists cannot be specified when calling any of them.
- None of them are visible to argument-dependent lookup.
- When any of them are found by normal unqualified lookup as the name to the left of the function-call operator, argument-dependent lookup is inhibited.

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | the range of the elements to examine |
| r | - | the range of the elements to examine |
| pred | - | predicate to apply to the projected elements |
| proj | - | projection to apply to the elements |

### Return value

1,2) true if std::invoke(pred, std::invoke(proj, \*i)) != false for every iterator i in the range, false otherwise. Returns true if the range is empty.3,4) true if std::invoke(pred, std::invoke(proj, \*i)) != false for at least one iterator i in the range, false otherwise. Returns false if the range is empty.5,6) true if std::invoke(pred, std::invoke(proj, \*i)) == false for every iterator i in the range, false otherwise. Returns true if the range is empty.

| Has true element | Yes | | No | |
| --- | --- | --- | --- | --- |
| Has false element | Yes | No | Yes | No[[1]](all_any_none_of.html#cite_note-1) |
| `all_of` | false | true | false | true |
| `any_of` | true | true | false | false |
| `none_of` | false | false | true | true |

1. ↑ The range is empty in this case.

### Complexity

At most last - first applications of the predicate and the projection.

### Possible implementation

| all_of (1,2) |
| --- |
| ```text struct all_of_fn {     template<std::input_iterator I, std::sentinel_for<I> S, class Proj = std::identity,              std::indirect_unary_predicate<std::projected<I, Proj>> Pred>     constexpr bool operator()(I first, S last, Pred pred, Proj proj = {}) const     {         return ranges::find_if_not(first, last, std::ref(pred), std::ref(proj)) == last;     }       template<ranges::input_range R, class Proj = std::identity,              std::indirect_unary_predicate<                  std::projected<ranges::iterator_t<R>,Proj>> Pred>     constexpr bool operator()(R&& r, Pred pred, Proj proj = {}) const     {         return operator()(ranges::begin(r), ranges::end(r),                           std::ref(pred), std::ref(proj));     } };   inline constexpr all_of_fn all_of; ``` |
| any_of (3,4) |
| ```text struct any_of_fn {     template<std::input_iterator I, std::sentinel_for<I> S, class Proj = std::identity,              std::indirect_unary_predicate<std::projected<I, Proj>> Pred>     constexpr bool operator()(I first, S last, Pred pred, Proj proj = {}) const     {         return ranges::find_if(first, last, std::ref(pred), std::ref(proj)) != last;     }       template<ranges::input_range R, class Proj = std::identity,              std::indirect_unary_predicate<                  std::projected<ranges::iterator_t<R>,Proj>> Pred>     constexpr bool operator()(R&& r, Pred pred, Proj proj = {}) const     {         return operator()(ranges::begin(r), ranges::end(r),                           std::ref(pred), std::ref(proj));     } };   inline constexpr any_of_fn any_of; ``` |
| none_of (5,6) |
| ```text struct none_of_fn {     template<std::input_iterator I, std::sentinel_for<I> S, class Proj = std::identity,              std::indirect_unary_predicate<std::projected<I, Proj>> Pred>     constexpr bool operator()(I first, S last, Pred pred, Proj proj = {}) const     {         return ranges::find_if(first, last, std::ref(pred), std::ref(proj)) == last;     }       template<ranges::input_range R, class Proj = std::identity,              std::indirect_unary_predicate<                  std::projected<ranges::iterator_t<R>,Proj>> Pred>     constexpr bool operator()(R&& r, Pred pred, Proj proj = {}) const     {         return operator()(ranges::begin(r), ranges::end(r),                           std::ref(pred), std::ref(proj));     } };   inline constexpr none_of_fn none_of; ``` |

### Example

Run this code

```
#include <algorithm>
#include <functional>
#include <iostream>
#include <iterator>
#include <numeric>
#include <vector>
 
namespace ranges = std::ranges;
 
constexpr bool some_of(auto&& r, auto&& pred) // some but not all
{
    return not (ranges::all_of(r, pred) or ranges::none_of(r, pred));
}
 
constexpr auto w = {1, 2, 3};
static_assert(!some_of(w, [](int x) { return x < 1; }));
static_assert( some_of(w, [](int x) { return x < 2; }));
static_assert(!some_of(w, [](int x) { return x < 4; }));
 
int main()
{
    std::vector<int> v(10, 2);
    std::partial_sum(v.cbegin(), v.cend(), v.begin());
    std::cout << "Among the numbers: ";
    ranges::copy(v, std::ostream_iterator<int>(std::cout, " "));
    std::cout << '\n';
 
    if (ranges::all_of(v.cbegin(), v.cend(), [](int i) { return i % 2 == 0; }))
        std::cout << "All numbers are even\n";
 
    if (ranges::none_of(v, std::bind(std::modulus<int>(), std::placeholders::_1, 2)))
        std::cout << "None of them are odd\n";
 
    auto DivisibleBy = [](int d)
    {
        return d { return m % d == 0; };
    };
 
    if (ranges::any_of(v, DivisibleBy(7)))
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
| all_ofany_ofnone_of(C++11)(C++11)(C++11) | checks if a predicate is true for all, any or none of the elements in a range   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/ranges/all_any_none_of&oldid=179678>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 January 2025, at 10:17.