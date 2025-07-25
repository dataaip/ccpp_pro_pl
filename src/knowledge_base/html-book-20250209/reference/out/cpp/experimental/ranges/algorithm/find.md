# std::experimental::ranges::find, std::experimental::ranges::find_if, std::experimental::ranges::find_if_not

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of | | | | | | countcount_if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****findfind_iffind_if_not**** | | | | | | find_end | | | | | | find_first_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | mismatch | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal | | | | | | for_each | | | | | | lexicographical_compare | | | | | |  | | | | | |  | | | | | |
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
| template< InputIterator I, Sentinel<I> S, class T, class Proj = ranges::identity >      requires IndirectRelation<ranges::equal_to<>, projected<I, Proj>, const T\*> I find( I first, S last, const T& value, Proj proj = Proj{} ); | (1) | (ranges TS) |
| template< InputRange R, class T, class Proj = ranges::identity >      requires IndirectRelation<ranges::equal_to<>,                                 projected<ranges::iterator_t<R>, Proj>, const T\*> ranges::safe_iterator_t<R> find( R&& r, const T& value, Proj proj = Proj{} ); | (2) | (ranges TS) |
| template< InputIterator I, Sentinel<I> S, class Proj = ranges::identity,            IndirectUnaryPredicate<projected<I, Proj>> Pred > I find_if( I first, S last, Pred pred, Proj proj = Proj{} ); | (3) | (ranges TS) |
| template< InputRange R, class Proj = ranges::identity,            IndirectUnaryPredicate<projected<ranges::iterator_t<R>, Proj>> Pred > ranges::safe_iterator_t<R> find_if( R&& r, Pred pred, Proj proj = Proj{} ); | (4) | (ranges TS) |
| template< InputIterator I, Sentinel<I> S, class Proj = ranges::identity,            IndirectUnaryPredicate<projected<I, Proj>> Pred > I find_if_not( I first, S last, Pred pred, Proj proj = Proj{} ); | (5) | (ranges TS) |
| template< InputRange R, class Proj = ranges::identity,            IndirectUnaryPredicate<projected<ranges::iterator_t<R>, Proj>> Pred > ranges::safe_iterator_t<R> find_if_not( R&& r, Pred pred, Proj proj = Proj{} ); | (6) | (ranges TS) |
|  |  |  |

Returns the first element in the range ``first`,`last`)` that satisfies specific criteria:

1) `find` searches for an element whose projected value is equal to value (i.e., value == [ranges::invoke(proj, \*i)).3) `find_if` searches for an element for whose projected value predicate p returns true (i.e., ranges::invoke(pred, ranges::invoke(proj, \*i))) is true).5) `find_if_not` searches for an element for whose projected value predicate q returns false (i.e., ranges::invoke(pred, ranges::invoke(proj, \*i))) is false).2,4,6) Same as (1,3,5), but uses r as the source range, as if using ranges::begin(r) as first and ranges::end(r) as last.

Notwithstanding the declarations depicted above, the actual number and order of template parameters for algorithm declarations is unspecified. Thus, if explicit template arguments are used when calling an algorithm, the program is probably non-portable.

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | the range of elements to examine |
| r | - | the range of elements to examine |
| value | - | value to compare the projected elements to |
| pred | - | predicate to apply to the projected elements |
| proj | - | projection to apply to the elements |

### Return value

Iterator to the first element satisfying the condition. If no such element is found, returns an iterator that compares equal to last.

### Complexity

At most last - first applications of the predicate and projection.

### Possible implementation

| First version |
| --- |
| ```text template<InputIterator I, Sentinel<I> S, class T, class Proj = ranges::identity>     requires IndirectRelation<ranges::equal_to<>, projected<I, Proj>, const T*> I find(I first, S last, const T& value, Proj proj = Proj{}) {     for (; first != last; ++first)         if (ranges::invoke(proj, *first) == value)             break;     return first; } ``` |
| Second version |
| ```text template<InputIterator I, Sentinel<I> S, class Proj = ranges::identity,          IndirectUnaryPredicate<projected<I, Proj>> Pred> I find_if(I first, S last, Pred pred, Proj proj = Proj{}) {     for (; first != last; ++first)         if (ranges::invoke(pred, ranges::invoke(proj, *first)))             break;     return first; } ``` |
| Third version |
| ```text template<InputIterator I, Sentinel<I> S, class Proj = ranges::identity,          IndirectUnaryPredicate<projected<I, Proj>> Pred> I find_if_not(I first, S last, Pred pred, Proj proj = Proj{}) {     for (; first != last; ++first)         if (!ranges::invoke(pred, ranges::invoke(proj, *first)))             break;     return first; } ``` |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| findfind_iffind_if_not(C++11) | finds the first element satisfying specific criteria   (function template) |
| adjacent_find | finds the first two adjacent items that are equal (or satisfy a given predicate)   (function template) |
| find_end | finds the last sequence of elements in a certain range   (function template) |
| find_first_of | searches for any one of a set of elements   (function template) |
| mismatch | finds the first position where two ranges differ   (function template) |
| search | searches for a range of elements   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/algorithm/find&oldid=155244>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 July 2023, at 01:47.