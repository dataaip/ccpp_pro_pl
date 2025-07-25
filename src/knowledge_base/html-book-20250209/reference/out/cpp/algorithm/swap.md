# std::swap

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-modifying sequence operations | | | | | | Batch operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each_n(C++17) | | | | | | | Search operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of(C++11)                (C++11)(C++11) | | | | | | countcount_if | | | | | | mismatch | | | | | | equal | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not(C++11) | | | | | | find_end | | | | | | find_first_of | | | | | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | | Modifying sequence operations | | | | | | Copy operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if(C++11) | | | | | | copy_backward | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copy_n(C++11) | | | | | | move(C++11) | | | | | | move_backward(C++11) | | | | | | | Swap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****swap**** | | | | | | iter_swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap_ranges | | | | | |  | | | | | | | Transformation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replacereplace_if | | | | | | transform | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replace_copyreplace_copy_if | | | | | |  | | | | | | | Generation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill | | | | | | fill_n | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | generate | | | | | | generate_n | | | | | | | Removing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if | | | | | | unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if | | | | | | unique_copy | | | | | | | Order-changing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse | | | | | | reverse_copy | | | | | | rotate | | | | | | rotate_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | random_shuffleshuffle(until C++17)(C++11) | | | | | | shift_leftshift_right(C++20)(C++20) | | | | | | | Sampling operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sample(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Sorting and related operations | | | | | | Partitioning operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition | | | | | | partition_copy(C++11) | | | | | | stable_partition | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned(C++11) | | | | | | partition_point(C++11) | | | | | |  | | | | | | | Sorting operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort | | | | | | partial_sort | | | | | | partial_sort_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted(C++11) | | | | | | is_sorted_until(C++11) | | | | | | nth_element | | | | | |  | | | | | | | Binary search operations (on partitioned ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound | | | | | | upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range | | | | | | binary_search | | | | | | | Set operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | includes | | | | | | set_union | | | | | | set_intersection | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference | | | | | | set_symmetric_difference | | | | | |  | | | | | | | Merge operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_merge | | | | | | | Heap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap | | | | | | pop_heap | | | | | | make_heap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort_heap | | | | | | is_heap(C++11) | | | | | | is_heap_until(C++11) | | | | | | | Minimum/maximum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max | | | | | | min | | | | | | minmax(C++11) | | | | | | clamp(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max_element | | | | | | min_element | | | | | | minmax_element(C++11) | | | | | |  | | | | | | | Lexicographical comparison operations | | | | | | lexicographical_compare | | | | | | lexicographical_compare_three_way(C++20) | | | | | | Permutation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation | | | | | | prev_permutation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation(C++11) | | | | | |  | | | | | |  | | | | | | | C library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | qsort | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bsearch | | | | | | |
| Numeric operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | adjacent_difference | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sum | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
| Operations on uninitialized memory | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n(C++11) | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_fill_n | | | | | |  | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | destroy(C++17) | | | | | | destroy_n(C++17) | | | | | | destroy_at(C++17) | | | | | | construct_at(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<algorithm>` |  | (until C++11) |
| Defined in header `<utility>` |  | (since C++11) |
| Defined in header `<string_view>` |  |  |
| template< class T >  void swap( T& a, T& b ); | (1) | (conditionally noexcept since C++11) (constexpr since C++20) |
| template< class T2, std::size_t N >  void swap( T2 (&a)[N], T2 (&b)[N] ); | (2) | (conditionally noexcept since C++11) (constexpr since C++20) |
|  |  |  |

Exchanges the given values.

1) Swaps the values a and b.

|  |  |
| --- | --- |
| This overload participates in overload resolution only if std::is_move_constructible_v<T> && std::is_move_assignable_v<T> is true. | (since C++17) |

2) Swaps the arrays a and b. Equivalent to std::swap_ranges(a, a + N, b).

|  |  |
| --- | --- |
| This overload participates in overload resolution only if std::is_swappable_v<T2> is true. | (since C++17) |

### Parameters

|  |  |  |
| --- | --- | --- |
| a, b | - | the values to be swapped |
| Type requirements | | |
| -`T` must meet the requirements of CopyConstructible and CopyAssignable(until C++11)MoveConstructible and MoveAssignable(since C++11). | | |
| -`T2` must meet the requirements of Swappable. | | |

### Return value

(none)

### Exceptions

1)

|  |  |
| --- | --- |
| (none) | (until C++11) |
| noexcept specification:noexcept(  std::is_nothrow_move_constructible<T>::value &&      std::is_nothrow_move_assignable<T>::value ) | (since C++11) |

2)

|  |  |
| --- | --- |
| noexcept specification:noexcept(noexcept(swap(\*a, \*b)))The lookup for the identifier `swap` in the exception specification finds this function template in addition to anything found by the usual lookup rules, making the exception specification equivalent to C++17 std::is_nothrow_swappable. | (since C++11) (until C++17) |
| noexcept specification:noexcept(std::is_nothrow_swappable_v<T2>) | (since C++17) |

### Complexity

1) Constant.2) Linear in N.

### Specializations

|  |  |
| --- | --- |
| `std::swap` may be specialized in namespace std for program-defined types, but such specializations are not found by ADL (the namespace std is not the associated namespace for the program-defined type). | (until C++20) |

The expected way to make a program-defined type swappable is to provide a non-member function swap in the same namespace as the type: see Swappable for details.

The following overloads are already provided by the standard library:

|  |  |
| --- | --- |
| std::swap(std::pair)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::tuple)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::shared_ptr)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::weak_ptr)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::unique_ptr)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::function)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_string) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::array)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::deque) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::forward_list)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::list) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::vector) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::map) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::multimap) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::set) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::multiset) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::unordered_map)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::unordered_multimap)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::unordered_set)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::unordered_multiset)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::queue)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::priority_queue)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::stack)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::valarray)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_stringbuf)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_istringstream)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_ostringstream)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_stringstream)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_filebuf)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_ifstream)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_ofstream)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_fstream)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_syncbuf)(C++20) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_spanbuf)(C++23) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_ispanstream)(C++23) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_ospanstream)(C++23) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_spanstream)(C++23) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_regex)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::match_results)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::thread)(C++11) | specializes the ****std::swap**** algorithm   (function) |
| std::swap(std::unique_lock)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::shared_lock)(C++14) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::promise)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::packaged_task)(C++11) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::optional)(C++17) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::any)(C++17) | specializes the ****std::swap**** algorithm   (function) |
| std::swap(std::variant)(C++17) | specializes the ****std::swap**** algorithm   (function template) |
| std::swap(std::basic_stacktrace)(C++23) | specializes the ****std::swap**** algorithm   (function template) |
| swap(std::filesystem::path)(C++17) | specializes the ****std::swap**** algorithm   (function) |
| swap(std::expected)(C++23) | specializes the ****std::swap**** algorithm   (function) |
| swap(std::jthread)(C++20) | specializes the ****std::swap**** algorithm   (function) |
| swap(std::move_only_function)(C++23) | specializes the ****std::swap**** algorithm   (function) |
| swap(std::stop_source)(C++20) | specializes the ****std::swap**** algorithm   (function) |
| swap(std::stop_token)(C++20) | specializes the ****std::swap**** algorithm   (function) |

### Example

Run this code

```
#include <algorithm>
#include <iostream>
 
namespace Ns
{
    class A
    {
        int id {};
 
        friend void swap(A& lhs, A& rhs)
        {
            std::cout << "swap(" << lhs << ", " << rhs << ")\n";
            std::swap(lhs.id, rhs.id);
        }
 
        friend std::ostream& operator<<(std::ostream& os, A const& a)
        {
            return os << "A::id=" << a.id;
        }
 
    public:
        A(int i) : id {i} {}
        A(A const&) = delete;
        A& operator = (A const&) = delete;
    };
}
 
int main()
{
    int a = 5, b = 3;
    std::cout << a << ' ' << b << '\n';
    std::swap(a, b);
    std::cout << a << ' ' << b << '\n';
 
    Ns::A p {6}, q {9};
    std::cout << p << ' ' << q << '\n';
//  std::swap(p, q); // error, type requirements are not satisfied
    swap(p, q);      // OK, ADL finds the appropriate friend `swap`
    std::cout << p << ' ' << q << '\n';
}

```

Output:

```
5 3
3 5
A::id=6 A::id=9
swap(A::id=6, A::id=9)
A::id=9 A::id=6

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 227 | C++98 | `T` was not required to be CopyConstructible or DefaultConstructible (a temporary object of type `T` might not be able to be constructed) | `T` is also required to be CopyConstructible |
| LWG 809 | C++98 | arrays could not be swapped | added overload (2) |
| LWG 2554 | C++11 | swapping multi-dimensional arrays can never be noexcept due to name lookup problems | made to work |

### See also

|  |  |
| --- | --- |
| ranges::swap(C++20) | swaps the values of two objects (customization point object) |
| iter_swap | swaps the elements pointed to by two iterators   (function template) |
| swap_ranges | swaps two ranges of elements   (function template) |
| exchange(C++14) | replaces the argument with a new value and returns its previous value   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/swap&oldid=175679>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 September 2024, at 19:32.