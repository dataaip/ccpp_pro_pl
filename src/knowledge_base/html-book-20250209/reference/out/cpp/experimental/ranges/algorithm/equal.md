# std::experimental::ranges::equal

From cppreference.com
< cpp‎ | experimental‎ | ranges
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

Ranges

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Concepts | | | | |
| General utilities | | | | |
| Iterators | | | | |
| Ranges | | | | |
| Algorithms | | | | |

Algorithms library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Non-modifying sequence operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of | | | | | | countcount_if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not | | | | | | find_end | | | | | | find_first_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | mismatch | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****equal**** | | | | | | for_each | | | | | | lexicographical_compare | | | | | |  | | | | | |  | | | | | |
| Modifying sequence operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if | | | | | | copy_n") | | | | | | copy_backward") | | | | | | move") | | | | | | move_backward") | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill") | | | | | | fill_n") | | | | | | generate") | | | | | | generate_n") | | | | | | swap_ranges") | | | | | | shuffle") | | | | | | transform") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if") | | | | | | replacereplace_if") | | | | | | reverse") | | | | | | rotate") | | | | | | unique") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if") | | | | | | replace_copyreplace_copy_if") | | | | | | reverse_copy") | | | | | | rotate_copy") | | | | | | unique_copy") | | | | | |
| Partitioning operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned") | | | | | | partition_point") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition") | | | | | | partition_copy") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stable_partition") | | | | | |  | | | | | |
| Sorting operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted") | | | | | | is_sorted_until") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sort") | | | | | | partial_sort_copy") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | nth_element") | | | | | |  | | | | | |
| Binary search operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | upper_bound") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | binary_search") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range") | | | | | |
| Set operations (on sorted ranges) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge") | | | | | | inplace_merge") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | includes") | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference") | | | | | | set_intersection") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_symmetric_difference") | | | | | | set_union") | | | | | |
| Heap operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_heap") | | | | | | is_heap_until") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | make_heap") | | | | | | sort_heap") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap") | | | | | | pop_heap") | | | | | |
| Minimum/maximum operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | max") | | | | | | max_element") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | min") | | | | | | min_element") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | minmax") | | | | | | minmax_element") | | | | | |
| Permutations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | prev_permutation") | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/ranges/algorithm>` |  |  |
| template< InputIterator I1, Sentinel<I1> S1, InputIterator I2, Sentinel<I2> S2,  class Pred = ranges::equal_to<>,             class Proj1 = ranges::identity, class Proj2 = ranges::identity >      requires IndirectlyComparable<I1, I2, Pred, Proj1, Proj2>  bool equal( I1 first1, S1 last1, I2 first2, S2 last2, Pred pred = Pred{},             Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{} ); | (1) | (ranges TS) |
| template< InputRange R1, InputRange R2, class Pred = ranges::equal_to<>,  class Proj1 = ranges::identity, class Proj2 = ranges::identity >      requires IndirectlyComparable<ranges::iterator_t<R1>, ranges::iterator_t<R2>,                                    Pred, Proj1, Proj2>  bool equal( R1&& r1, R2&& r2, Pred pred = Pred{},             Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{} ); | (2) | (ranges TS) |
| template< InputIterator I1, Sentinel<I1> S1, class I2,  class Pred = ranges::equal_to<>,             class Proj1 = ranges::identity, class Proj2 = ranges::identity >      requires InputIterator<std::decay_t<I2>> && !Range<I2> &&               IndirectlyComparable<I1, std::decay_t<I2>, Pred, Proj1, Proj2>  bool equal( I1 first1, S1 last1, I2&& first2_, Pred pred = Pred{},             Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{} ); | (3) | (ranges TS)  (deprecated) |
| template< InputRange R1, class I2, class Pred = ranges::equal_to<>,  class Proj1 = ranges::identity, class Proj2 = ranges::identity >      requires InputIterator<std::decay_t<I2>> && !Range<I2> &&               IndirectlyComparable<ranges::iterator_t<R1>, std::decay_t<I2>, Pred, Proj1, Proj2>  bool equal( R1&& r1, I2&& first2_, Pred pred = Pred{},             Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{} ); | (4) | (ranges TS)  (deprecated) |
|  |  |  |

1) Returns true if the range ``first1`,`last1`)` is equal to the range `[`first2`,`last2`)`, and false otherwise.2) Same as (1), but uses r1 as the first source range and r2 as the second source range, as if using [ranges::begin(r1) as first1, ranges::end(r1) as last1, ranges::begin(r2) as first2, and ranges::end(r2) as last2.3) Same as (1), except that the second range is considered to end when either the first range is exhausted or the first mismatch is detected. Equivalent to return last1 == ranges::mismatch(first1, last1, std::forward<I2>(first2_), comp, proj1, proj2).in1();4) Same as (3), but uses r1 as the first source range, as if using ranges::begin(r1) as first1 and ranges::end(r1) as last1.

Two ranges are considered equal if they have the same number of elements and, for every iterator `i` in the range ``first1`,`last1`)`, [ranges::invoke(pred, ranges::invoke(proj1, \*i), ranges::invoke(proj2, \*(first2 + (i - first1)))) is true.

Notwithstanding the declarations depicted above, the actual number and order of template parameters for algorithm declarations is unspecified. Thus, if explicit template arguments are used when calling an algorithm, the program is probably non-portable.

### Parameters

|  |  |  |
| --- | --- | --- |
| first1, last1 | - | the first range of the elements |
| r1 | - | the first range of the elements |
| first2, last2 | - | the second range of the elements |
| r2 | - | the second range of the elements |
| first2_ | - | the beginning of the second range of the elements |
| pred | - | predicate to apply to the projected elements |
| proj1 | - | projection to apply to the elements in the first range |
| proj2 | - | projection to apply to the elements in the second range |

### Return value

true if the two ranges are equal, otherwise returns false.

### Notes

`ranges::equal` should not be used to compare the ranges formed by the iterators from std::unordered_set, std::unordered_multiset, std::unordered_map, or std::unordered_multimap because the order in which the elements are stored in those containers may be different even if the two containers store the same elements.

When comparing entire containers for equality, `operator==` for the corresponding container are usually preferred.

### Complexity

1,2) If SizedSentinel<S1, I1> && SizedSentinel<S2, I2> is satisfied and last1 - first1 != last2 - first2, no applications of the predicate and projections. Otherwise, at most min(last1 - first1, last2 - first2) applications of the predicate and each projection.3,4) At most last1 - first1 applications of the predicate and each projection.

### Possible implementation

|  |
| --- |
| ```text namespace detail  {     template<InputIterator I1, SizedSentinel<I1> S1,              InputIterator I2, SizedSentinel<I1> S2>     bool check_size(I1& first1, S1& last1, I2& first2, S2& last2)     {         return last1 - first1 != last2 - first2;     }       template<InputIterator I1, Sentinel<I1> S1, InputIterator I2, Sentinel<I1> S2>     bool check_size(I1& first1, S1& last1, I2& first2, S2& last2)     {         return false;     } }   template<InputIterator I1, Sentinel<I1> S1, InputIterator I2, Sentinel<I2> S2,          class Pred = ranges::equal_to<>,           class Proj1 = ranges::identity, class Proj2 = ranges::identity>     requires IndirectlyComparable<I1, I2, Pred, Proj1, Proj2> bool equal(I1 first1, S1 last1, I2 first2, S2 last2, Pred pred = Pred{},            Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{})  {     if (detail::check_size(first1, last1, first2, last2))         return false;     for (; first1 != last1 && first2 != last2; (void) ++first1, (void)++first2)         if (!ranges::invoke(pred, ranges::invoke(proj1, *first1),                                    ranges::invoke(proj2, *first2)))             return false;     return first1 == last1 && first2 == last2; } ``` |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| equal | determines if two sets of elements are the same   (function template) |
| findfind_iffind_if_not | finds the first element satisfying specific criteria   (function template) |
| lexicographical_compare | returns true if one range is lexicographically less than another   (function template) |
| mismatch | finds the first position where two ranges differ   (function template) |
| search | searches for a range of elements   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/algorithm/equal&oldid=157769>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 September 2023, at 09:12.