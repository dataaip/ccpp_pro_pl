# std::priority_queue<T,Container,Compare>::priority_queue

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
| ****priority_queue::priority_queue**** | | | | |
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
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| priority_queue() : priority_queue(Compare(), Container()) {} | (1) | (since C++11) |
| explicit priority_queue( const Compare& compare )      : priority_queue(compare, Container()) {} | (2) | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| explicit priority_queue( const Compare& compare = Compare(),                           const Container& cont = Container() ); |  | (until C++11) |
| priority_queue( const Compare& compare, const Container& cont ); |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| priority_queue( const Compare& compare, Container&& cont ); | (4) | (since C++11) |
| priority_queue( const priority_queue& other ); | (5) |  |
| priority_queue( priority_queue&& other ); | (6) | (since C++11) |
| template< class InputIt >  priority_queue( InputIt first, InputIt last, const Compare& compare = Compare() ); | (7) | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  | (8) |  |
| template< class InputIt >  priority_queue( InputIt first, InputIt last,                  const Compare& compare = Compare(), const Container& cont = Container() ); |  | (until C++11) |
| template< class InputIt >  priority_queue( InputIt first, InputIt last, const Compare& compare, const Container& cont ); |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| template< class InputIt >  priority_queue( InputIt first, InputIt last, const Compare& compare, Container&& cont ); | (9) | (since C++11) |
| template< class Alloc >  explicit priority_queue( const Alloc& alloc ); | (10) | (since C++11) |
| template< class Alloc >  priority_queue( const Compare& compare, const Alloc& alloc ); | (11) | (since C++11) |
| template< class Alloc >  priority_queue( const Compare& compare, const Container& cont, const Alloc& alloc ); | (12) | (since C++11) |
| template< class Alloc >  priority_queue( const Compare& compare, Container&& cont, const Alloc& alloc ); | (13) | (since C++11) |
| template< class Alloc >  priority_queue( const priority_queue& other, const Alloc& alloc ); | (14) | (since C++11) |
| template< class Alloc >  priority_queue( priority_queue&& other, const Alloc& alloc ); | (15) | (since C++11) |
| template< class InputIt, class Alloc >  priority_queue( InputIt first, InputIt last, const Alloc& alloc ); | (16) | (since C++11) |
| template< class InputIt, class Alloc >  priority_queue( InputIt first, InputIt last, const Compare& compare, const Alloc& alloc ); | (17) | (since C++11) |
| template< class InputIt, class Alloc >  priority_queue( InputIt first, InputIt last, const Compare& compare, const Container& cont, const Alloc& alloc ); | (18) | (since C++11) |
| template< class InputIt, class Alloc >  priority_queue( InputIt first, InputIt last, const Compare& compare,                 Container&& cont, const Alloc& alloc ); | (19) | (since C++11) |
| template< container-compatible-range<T> R >  priority_queue( std::from_range_t, R&& rg, const Compare& compare = Compare() ); | (20) | (since C++23) |
| template< container-compatible-range<T> R, class Alloc >  priority_queue( std::from_range_t, R&& rg, const Compare& compare, const Alloc& alloc ); | (21) | (since C++23) |
| template< container-compatible-range<T> R, class Alloc >  priority_queue( std::from_range_t, R&& rg, const Alloc& alloc ); | (22) | (since C++23) |
|  |  |  |

Constructs new underlying container of the container adaptor from a variety of data sources.

1) Default constructor. Value-initializes the comparator and the underlying container.2) Copy-constructs the comparison functor comp with the contents of compare. Value-initializes the underlying container c.3) Copy-constructs the underlying container c with the contents of cont. Copy-constructs the comparison functor comp with the contents of compare. Calls std::make_heap(c.begin(), c.end(), comp). This is also the default constructor.(until C++11)4) Move-constructs the underlying container c with std::move(cont). Copy-constructs the comparison functor comp with compare. Calls std::make_heap(c.begin(), c.end(), comp).5) Copy constructor. The underlying container is copy-constructed with other.c. The comparison functor is copy-constructed with other.comp. (implicitly declared)6) Move constructor. The underlying container is constructed with std::move(other.c). The comparison functor is constructed with std::move(other.comp). (implicitly declared)7-9) Iterator-pair constructors. These overloads participate in overload resolution only if `InputIt` satisfies LegacyInputIterator.7) Constructs c as if by c(first, last) and comp from compare. Then calls std::make_heap(c.begin(), c.end(), comp);.8) Copy-constructs c from cont and comp from compare. Then calls c.insert(c.end(), first, last);, and then calls std::make_heap(c.begin(), c.end(), comp);.9) Move-constructs c from std::move(cont) and copy-constructs comp from compare. Then calls c.insert(c.end(), first, last);, and then calls std::make_heap(c.begin(), c.end(), comp);.10-15) Allocator-extended constructors. These overloads participate in overload resolution only if std::uses_allocator<container_type, Alloc>::value is true, that is, if the underlying container is an allocator-aware container (true for all standard library containers).10) Constructs the underlying container using alloc as allocator. Effectively calls c(alloc). comp is value-initialized.11) Constructs the underlying container using alloc as allocator. Effectively calls c(alloc). Copy-constructs comp from compare.12) Constructs the underlying container with the contents of cont and using alloc as allocator, as if by c(cont, alloc). Copy-constructs comp from compare. Then calls std::make_heap(c.begin(), c.end(), comp).13) Constructs the underlying container with the contents of cont using move semantics while using alloc as allocator, as if by c(std::move(cont), alloc). Copy-constructs comp from compare. Then calls std::make_heap(c.begin(), c.end(), comp).14) Constructs the underlying container with the contents of other.c and using alloc as allocator. Effectively calls c(other.c, alloc). Copy-constructs comp from other.comp.15) Constructs the underlying container with the contents of other using move semantics while utilizing alloc as allocator. Effectively calls c(std::move(other.c), alloc). Move-constructs comp from other.comp.16-19) Allocator-extended iterator-pair constructors. Same as (7-9), except that alloc is used for constructing the underlying container. These overloads participate in overload resolution only if std::uses_allocator<container_type, Alloc>::value is true and InputIt satisfies LegacyInputIterator.20) Initializes comp with compare and c with ranges::to<Container>(std::forward<R>(rg)). Then calls std::make_heap(c.begin(), c.end(), comp).21) Initializes comp with compare and c with ranges::to<Container>(std::forward<R>(rg), alloc). Then calls std::make_heap(c.begin(), c.end(), comp).22) Initializes c with ranges::to<Container>(std::forward<R>(rg), alloc). Then calls std::make_heap(c.begin(), c.end(), comp).

Note that how an implementation checks whether a type satisfies LegacyInputIterator is unspecified, except that integral types are required to be rejected.

### Parameters

|  |  |  |
| --- | --- | --- |
| alloc | - | allocator to use for all memory allocations of the underlying container |
| other | - | another container adaptor to be used as source to initialize the underlying container |
| cont | - | container to be used as source to initialize the underlying container |
| compare | - | the comparison function object to initialize the underlying comparison functor |
| first, last | - | a range ``first`,`last`)` of elements to initialize with |
| rg | - | a [container compatible range, that is, an `input_range` whose elements are convertible to `T` |
| Type requirements | | |
| -`Alloc` must meet the requirements of Allocator. | | |
| -`Compare` must meet the requirements of Compare. | | |
| -`Container` must meet the requirements of Container. The allocator-extended constructors are only defined if `Container` meets the requirements of AllocatorAwareContainer. | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |

### Complexity

1,2) Constant.3,5,12) \(\scriptsize \mathcal{O}{(N)}\)O(N) comparisons and \(\scriptsize \mathcal{O}{(N)}\)O(N) calls to the constructor of `value_type`, where \(\scriptsize N\)N is cont.size().4) \(\scriptsize \mathcal{O}{(N)}\)O(N) comparisons, where \(\scriptsize N\)N is cont.size().6) Constant.7,16,17) \(\scriptsize \mathcal{O}{(M)}\)O(M) comparisons, where \(\scriptsize M\)M is std::distance(first, last).8,18) \(\scriptsize \mathcal{O}{(N + M)}\)O(N + M) comparisons and \(\scriptsize \mathcal{O}{(N)}\)O(N) calls to the constructor of `value_type`, where \(\scriptsize N\)N is cont.size() and \(\scriptsize M\)M is std::distance(first, last).9) \(\scriptsize \mathcal{O}{(N + M)}\)O(N + M) comparisons, where \(\scriptsize N\)N is cont.size() and \(\scriptsize M\)M is std::distance(first, last).10,11) Constant.13) \(\scriptsize \mathcal{O}{(N)}\)O(N) comparisons, where \(\scriptsize N\)N is cont.size().14) Linear in size of other.15) Constant if `Alloc` compares equal to the allocator of other. Linear in size of other otherwise.19) \(\scriptsize \mathcal{O}{(N + M)}\)O(N + M) comparisons and possibly \(\scriptsize \mathcal{O}{(N)}\)O(N) calls to the constructor of `value_type` (present if `Alloc` does not compare equal to the allocator of other), where \(\scriptsize N\)N is cont.size() and \(\scriptsize M\)M is std::distance(first, last).20) \(\scriptsize \mathcal{O}{(N)}\)O(N) comparisons and \(\scriptsize \mathcal{O}{(N)}\)O(N) calls to the constructor of `value_type`, where \(\scriptsize N\)N is ranges::distance(rg).21,22)

|  |  |
| --- | --- |
|  | This section is incomplete |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges-aware construction and insertion; overloads (20-22) |

### Example

Run this code

```
#include <complex>
#include <functional>
#include <iostream>
#include <queue>
#include <vector>
 
int main()
{
    std::priority_queue<int> pq1;
    pq1.push(5);
    std::cout << "pq1.size() = " << pq1.size() << '\n';
 
    std::priority_queue<int> pq2 {pq1};
    std::cout << "pq2.size() = " << pq2.size() << '\n';
 
    std::vector<int> vec {3, 1, 4, 1, 5};
    std::priority_queue<int> pq3 {std::less<int>(), vec};
    std::cout << "pq3.size() = " << pq3.size() << '\n';
 
    for (std::cout << "pq3 : "; !pq3.empty(); pq3.pop())
        std::cout << pq3.top() << ' ';
    std::cout << '\n';
 
    // Demo With Custom Comparator:
 
    using my_value_t = std::complex<double>;
    using my_container_t = std::vector<my_value_t>;
 
    auto my_comp = [](const my_value_t& z1, const my_value_t& z2)
    {
        return z2.real() < z1.real();
    };
 
    std::priority_queue<my_value_t,
                        my_container_t,
                        decltype(my_comp)> pq4{my_comp};
 
    using namespace std::complex_literals;
    pq4.push(5.0 + 1i);
    pq4.push(3.0 + 2i);
    pq4.push(7.0 + 3i);
 
    for (; !pq4.empty(); pq4.pop())
    {
        const auto& z = pq4.top();
        std::cout << "pq4.top() = " << z << '\n';
    }
 
    // TODO: C++23 range-aware ctors
}

```

Output:

```
pq1.size() = 1
pq2.size() = 1
pq3.size() = 5
pq3 : 5 4 3 1 1
pq4.top() = (3,2)
pq4.top() = (5,1)
pq4.top() = (7,3)

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P0935R0 | C++11 | default constructor and constructor (4) were explicit | made implicit |
| LWG 3506 | C++11 | allocator-extended iterator-pair constructors were missing | added |
| LWG 3522 | C++11 | constraints on iterator-pair constructors were missing | added |
| LWG 3529 | C++11 | construction from a pair of iterators called `insert` | constructs the container from them |

### See also

|  |  |
| --- | --- |
| operator= | assigns values to the container adaptor   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/priority_queue/priority_queue&oldid=161969>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 November 2023, at 01:28.