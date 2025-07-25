# std::experimental::ranges::all_of, std::experimental::ranges::any_of, std::experimental::ranges::none_of

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****all_ofany_ofnone_of**** | | | | | | countcount_if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not | | | | | | find_end | | | | | | find_first_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | mismatch | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal | | | | | | for_each | | | | | | lexicographical_compare | | | | | |  | | | | | |  | | | | | |
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
| template< InputIterator I, Sentinel<I> S, class Proj = ranges::identity,            IndirectUnaryPredicate<projected<I, Proj>> Pred > bool all_of( I first, S last, Pred pred, Proj proj = Proj{} ); | (1) | (ranges TS) |
| template< InputRange R, class Proj = ranges::identity,            IndirectUnaryPredicate<projected<ranges::iterator_t<R>, Proj>> Pred > bool all_of( R&& r, Pred pred, Proj proj = Proj{} ); | (2) | (ranges TS) |
| template< InputIterator I, Sentinel<I> S, class Proj = ranges::identity,            IndirectUnaryPredicate<projected<I, Proj>> Pred > bool any_of( I first, S last, Pred pred, Proj proj = Proj{} ); | (3) | (ranges TS) |
| template< InputRange R, class Proj = ranges::identity,            IndirectUnaryPredicate<projected<ranges::iterator_t<R>, Proj>> Pred > bool any_of( R&& r, Pred pred, Proj proj = Proj{} ); | (4) | (ranges TS) |
| template< InputIterator I, Sentinel<I> S, class Proj = identity,            IndirectUnaryPredicate<projected<I, Proj>> Pred > bool none_of( I first, S last, Pred pred, Proj proj = Proj{} ); | (5) | (ranges TS) |
| template< InputRange R, class Proj = ranges::identity,            IndirectUnaryPredicate<projected<ranges::iterator_t<R>, Proj>> Pred > bool none_of( R&& r, Pred pred, Proj proj = Proj{} ); | (6) | (ranges TS) |
|  |  |  |

1) Checks if unary predicate pred returns true for all elements in the range ``first`,`last`)`.3) Checks if unary predicate pred returns true for at least one element in the range `[`first`,`last`)`.5) Checks if unary predicate pred returns true for no elements in the range `[`first`,`last`)`.2,4,6) Same as (1,3,5), but uses r as the source range, as if using [ranges::begin(r) as first and ranges::end(r) as last.

Notwithstanding the declarations depicted above, the actual number and order of template parameters for algorithm declarations is unspecified. Thus, if explicit template arguments are used when calling an algorithm, the program is probably non-portable.

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | the range of the elements to examine |
| r | - | the range of the elements to examine |
| pred | - | predicate to apply to the projected elements |
| proj | - | projection to apply to the elements |

### Return value

1,2) true if pred returns true for all elements in the range, false otherwise. Returns true if the range is empty.3,4) true if pred returns true for at least one element in the range, false otherwise. Returns false if the range is empty.5,6) true if pred returns true for no elements in the range, false otherwise. Returns true if the range is empty.

### Complexity

1-6) At most last - first applications of the predicate and last - first applications of the projection.

### Possible implementation

| First version |
| --- |
| ```text template<InputIterator I, Sentinel<I> S, class Proj = ranges::identity,          IndirectUnaryPredicate<projected<I, Proj>> Pred> bool all_of(I first, S last, Pred pred, Proj proj = Proj{}) {     return ranges::find_if_not(first, last, std::ref(pred), std::ref(proj)) == last; }   template<InputRange R, class Proj = ranges::identity,          IndirectUnaryPredicate<projected<ranges::iterator_t<R>, Proj>> Pred> bool all_of(R&& r, Pred pred, Proj proj = Proj{}) {     return ranges::all_of(ranges::begin(r), ranges::end(r),                           std::ref(pred), std::ref(proj)); } ``` |
| Second version |
| ```text template<InputIterator I, Sentinel<I> S, class Proj = ranges::identity,          IndirectUnaryPredicate<projected<I, Proj>> Pred> bool any_of(I first, S last, Pred pred, Proj proj = Proj{}) {     return ranges::find_if(first, last, std::ref(pred), std::ref(proj)) != last; }   template<InputRange R, class Proj = ranges::identity,          IndirectUnaryPredicate<projected<ranges::iterator_t<R>, Proj>> Pred> bool any_of(R&& r, Pred pred, Proj proj = Proj{}) {     return ranges::any_of(ranges::begin(r), ranges::end(r),                           std::ref(pred), std::ref(proj)); } ``` |
| Third version |
| ```text template<InputIterator I, Sentinel<I> S, class Proj = identity,          IndirectUnaryPredicate<projected<I, Proj>> Pred> bool none_of(I first, S last, Pred pred, Proj proj = Proj{}) {     return ranges::find_if(first, last, std::ref(pred), std::ref(proj)) == last; }   template<InputRange R, class Proj = ranges::identity,          IndirectUnaryPredicate<projected<ranges::iterator_t<R>, Proj>> Pred> bool none_of(R&& r, Pred pred, Proj proj = Proj{}) {     return ranges::none_of(ranges::begin(r), ranges::end(r),                            std::ref(pred), std::ref(proj)); } ``` |

### Example

Run this code

```
#include <experimental/ranges/algorithm>
#include <experimental/ranges/iterator>
#include <functional>
#include <iostream>
#include <iterator>
#include <numeric>
#include <vector>
 
namespace ranges = std::experimental::ranges;
 
int main()
{
    std::vector<int> v(10, 2);
    std::partial_sum(v.cbegin(), v.cend(), v.begin());
    std::cout << "Among the numbers: ";
    ranges::copy(v, ranges::ostream_iterator<int>(std::cout, " "));
    std::cout << '\n';
 
    if (ranges::all_of(v.cbegin(), v.cend(), [](int i) { return i % 2 == 0; }))
        std::cout << "All numbers are even\n";
    if (ranges::none_of(v, std::bind(std::modulus<int>(), std::placeholders::_1, 2)))
        std::cout << "None of them are odd\n";
 
    struct DivisibleBy
    {
        const int d;
        DivisibleBy(int n) : d(n) {}
        bool operator()(int n) const { return n % d == 0; }
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

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/algorithm/all_any_none_of&oldid=157768>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 September 2023, at 09:06.