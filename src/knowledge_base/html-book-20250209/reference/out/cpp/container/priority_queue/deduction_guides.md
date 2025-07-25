# deduction guides for `std::priority_queue`

From cppreference.com
< cpp‎ | container‎ | priority queue
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

Containers library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Sequence | | | | |
| array(C++11) | | | | |
| vector | | | | |
| vector<bool> | | | | |
| inplace_vector(C++26) | | | | |
| deque | | | | |
| forward_list(C++11) | | | | |
| list | | | | |
| Associative | | | | |
| set | | | | |
| multiset | | | | |
| map | | | | |
| multimap | | | | |
| Unordered associative | | | | |
| unordered_set(C++11) | | | | |
| unordered_multiset(C++11) | | | | |
| unordered_map(C++11) | | | | |
| unordered_multimap(C++11) | | | | |
| Adaptors | | | | |
| stack | | | | |
| queue | | | | |
| priority_queue | | | | |
| flat_set(C++23) | | | | |
| flat_multiset(C++23) | | | | |
| flat_map(C++23) | | | | |
| flat_multimap(C++23) | | | | |
| Views | | | | |
| span(C++20) | | | | |
| mdspan(C++23) | | | | |
| Tables | | | | |
| Iterator invalidation | | | | |
| Member function table | | | | |
| Non-member function table | | | | |

`std::priority_queue`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| priority_queue::priority_queue | | | | |
| priority_queue::~priority_queue | | | | |
| priority_queue::operator= | | | | |
| Element access | | | | |
| priority_queue::top | | | | |
| Capacity | | | | |
| priority_queue::empty | | | | |
| priority_queue::size | | | | |
| Modifiers | | | | |
| priority_queue::push | | | | |
| priority_queue::push_range(C++23) | | | | |
| priority_queue::emplace(C++11) | | | | |
| priority_queue::pop | | | | |
| priority_queue::swap(C++11) | | | | |
| Non-member functions | | | | |
| swap(std::priority_queue)(C++11) | | | | |
| Helper classes | | | | |
| uses_allocator<std::priority_queue>(C++11) | | | | |
| formatter<std::priority_queue>(C++23) | | | | |
| ****Deduction guides****(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<queue>` |  |  |
| template< class Comp, class Container >  priority_queue( Comp, Container ) -> priority_queue<typename Container::value_type, Container, Comp>; | (1) | (since C++17) |
| template< class InputIt,  class Comp = std::less</\*iter-value-type\*/<InputIt>>,            class Container = std::vector</\*iter-value-type\*/<InputIt> >  priority_queue( InputIt, InputIt, Comp = Comp(), Container = Container() ) -> priority_queue</\*iter-value-type\*/<InputIt>, Container, Comp>; | (2) | (since C++17) |
| template< class Comp, class Container, class Alloc >  priority_queue( Comp, Container, Alloc ) -> priority_queue<typename Container::value_type, Container, Comp>; | (3) | (since C++17) |
| template< class InputIt, class Alloc >  priority_queue( InputIt, InputIt, Alloc )      -> priority_queue</\*iter-value-type\*/<InputIt>,                        std::vector</\*iter-value-type\*/<InputIt>, Alloc>, std::less</\*iter-value-type\*/<InputIt>>>; | (4) | (since C++17) |
| template< class InputIt, class Comp, class Alloc >  priority_queue( InputIt, InputIt, Comp, Alloc )      -> priority_queue</\*iter-value-type\*/<InputIt>, std::vector</\*iter-value-type\*/<InputIt>, Alloc>, Comp>; | (5) | (since C++17) |
| template< class InputIt, class Comp, class Container, class Alloc >  priority_queue( InputIt, InputIt, Comp, Container, Alloc ) -> priority_queue<typename Container::value_type, Container, Comp>; | (6) | (since C++17) |
| template< ranges::input_range R,  class Comp = std::less<ranges::range_value_t<R>> >  priority_queue( std::from_range_t, R&&, Comp = Comp() )      -> priority_queue<ranges::range_value_t<R>, std::vector<ranges::range_value_t<R>>, Comp>; | (7) | (since C++23) |
| template< ranges::input_range R, class Comp, class Alloc >  priority_queue( std::from_range_t, R&&, Comp, Alloc )      -> priority_queue<ranges::range_value_t<R>, std::vector<ranges::range_value_t<R>, Alloc>, Comp>; | (8) | (since C++23) |
| template< ranges::input_range R, class Alloc >  priority_queue( std::from_range_t, R&&, Alloc )      -> priority_queue<ranges::range_value_t<R>, std::vector<ranges::range_value_t<R>, Alloc>>; | (9) | (since C++23) |
|  |  |  |

The following deduction guides are provided for std::priority_queue:

1-6) Allow deduction from underlying container type and from an iterator range. /\*iter-value-type\*/<It> denotes typename std::iterator_traits<It>::value_type for any type `It`.7-9) Allow deduction from a std::from_range_t tag and an input_range.

These overloads participate in overload resolution only if

- `InputIt` satisfies LegacyInputIterator,
- `Comp` does not satisfy Allocator,
- `Container` does not satisfy Allocator,
- for overloads (4,5),(since C++23) `Alloc` satisfies Allocator, and
- for overloads (3,6), std::uses_allocator_v<Container, Alloc> is true.

Note: the extent to which the library determines that a type does not satisfy LegacyInputIterator is unspecified, except that as a minimum integral types do not qualify as input iterators. Likewise, the extent to which it determines that a type does not satisfy Allocator is unspecified, except that as a minimum the member type `Alloc::value_type` must exist and the expression std::declval<Alloc&>().allocate(std::size_t{}) must be well-formed when treated as an unevaluated operand.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges-aware construction and insertion; overloads (7-9) |

### Example

Run this code

```
#include <functional>
#include <iostream>
#include <queue>
#include <vector>
 
int main()
{
    const std::vector<int> v = {1, 2, 3, 4};
    std::priority_queue pq1{std::greater<int>{}, v}; // deduces std::priority_queue<
                                                     //     int, std::vector<int>,
                                                     //     std::greater<int>>
    for (; !pq1.empty(); pq1.pop())
        std::cout << pq1.top() << ' ';
    std::cout << '\n';
 
    std::priority_queue pq2{v.begin(), v.end()}; // deduces std::priority_queue<int>
 
    for (; !pq2.empty(); pq2.pop())
        std::cout << pq2.top() << ' ';
    std::cout << '\n';
}

```

Output:

```
1 2 3 4
4 3 2 1

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3506 | C++17 | deduction guides from iterator and allocator were missing | added |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/priority_queue/deduction_guides&oldid=159748>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 September 2023, at 23:25.