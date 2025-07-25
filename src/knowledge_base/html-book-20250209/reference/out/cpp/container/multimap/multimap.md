# std::multimap<Key,T,Compare,Allocator>::multimap

From cppreference.com
< cpp‎ | container‎ | multimap
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

std::multimap

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****multimap::multimap**** | | | | | | multimap::~multimap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multimap::operator= | | | | | | multimap::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | multimap::beginmultimap::cbegin(C++11) | | | | | | multimap::endmultimap::cend(C++11) | | | | | | multimap::rbeginmultimap::crbegin(C++11) | | | | | | multimap::rendmultimap::crend(C++11) | | | | | | Capacity | | | | | | multimap::size | | | | | | multimap::max_size | | | | | | multimap::empty | | | | | | Observers | | | | | | multimap::key_comp | | | | | | multimap::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | multimap::clear | | | | | | multimap::insert | | | | | | multimap::erase | | | | | | multimap::swap | | | | | | multimap::merge(C++17) | | | | | | multimap::insert_range(C++23) | | | | | | multimap::emplace(C++11) | | | | | | multimap::emplace_hint(C++11) | | | | | | multimap::extract(C++17) | | | | | | Lookup | | | | | | multimap::count | | | | | | multimap::find | | | | | | multimap::contains(C++20) | | | | | | multimap::equal_range | | | | | | multimap::lower_bound | | | | | | multimap::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | std::swap(std::multimap) | | | | | | erase_if(std::multimap)(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| multimap(); |  | (until C++11) |
| multimap()      : multimap(Compare()) {} |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| explicit multimap( const Compare& comp,                     const Allocator& alloc = Allocator() ); | (2) |  |
| explicit multimap( const Allocator& alloc ); | (3) | (since C++11) |
|  |  |  |
| --- | --- | --- |
| template< class InputIt >  multimap( InputIt first, InputIt last,            const Compare& comp = Compare(), const Allocator& alloc = Allocator() ); | (4) |  |
| template< class InputIt >  multimap( InputIt first, InputIt last,            const Allocator& alloc ) : multimap(first, last, Compare(), alloc) {} | (5) | (since C++14) |
|  |  |  |
| --- | --- | --- |
| multimap( const multimap& other ); | (6) |  |
| multimap( const multimap& other, const Allocator& alloc ); | (7) | (since C++11) |
|  |  |  |
| --- | --- | --- |
| multimap( multimap&& other ); | (8) | (since C++11) |
| multimap( multimap&& other, const Allocator& alloc ); | (9) | (since C++11) |
|  |  |  |
| --- | --- | --- |
| multimap( std::initializer_list<value_type> init,  const Compare& comp = Compare(), const Allocator& alloc = Allocator() ); | (10) | (since C++11) |
| multimap( std::initializer_list<value_type> init,  const Allocator& alloc ) : multimap(init, Compare(), alloc) {} | (11) | (since C++14) |
|  |  |  |
| --- | --- | --- |
| template< container-compatible-range<value_type> R >  multimap( std::from_range_t, R&& rg,            const Compare& comp = Compare(), const Allocator& alloc = Allocator() ); | (12) | (since C++23) |
| template< container-compatible-range<value_type> R >  multimap( std::from_range_t, R&& rg,            const Allocator& alloc ) : multimap(std::from_range, std::forward<R>(rg), Compare(), alloc) {} | (13) | (since C++23) |
|  |  |  |

Constructs new container from a variety of data sources and optionally using user supplied allocator alloc or comparison function object comp.

1-3) Constructs an empty container.4,5) Constructs the container with the contents of the range ``first`,`last`)`. If `[`first`,`last`)` is not a [valid range, the behavior is undefined.6,7) Copy constructor. Constructs the container with the copy of the contents of other.

|  |  |
| --- | --- |
| If alloc is not provided, allocator is obtained by calling std::allocator_traits<allocator_type>::     select_on_container_copy_construction(other.get_allocator()). | (since C++11) |
| During class template argument deduction, only the first argument contributes to the deduction of the container's `Allocator` template parameter. | (since C++23) |

8,9) Move constructor. Constructs the container with the contents of other using move semantics. If alloc is not provided, allocator is obtained by move-construction from the allocator belonging to other.

|  |  |
| --- | --- |
| During class template argument deduction, only the first argument contributes to the deduction of the container's `Allocator` template parameter. | (since C++23) |

10,11) Initializer-list constructor. Constructs the container with the contents of the initializer list init.12,13) Constructs the container with the contents of rg.

### Parameters

|  |  |  |
| --- | --- | --- |
| alloc | - | allocator to use for all memory allocations of this container |
| comp | - | comparison function object to use for all comparisons of keys |
| first, last | - | the range to copy the elements from |
| other | - | another container to be used as source to initialize the elements of the container with |
| init | - | initializer list to initialize the elements of the container with |
| rg | - | a container compatible range, that is, an `input_range` whose elements are convertible to `value_type` |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |
| -`Compare` must meet the requirements of Compare. | | |
| -`Allocator` must meet the requirements of Allocator. | | |

### Complexity

1-3) Constant.4,5) \(\scriptsize N \cdot log(N)\)N·log(N) where \(\scriptsize N\)N is std::distance(first, last) in general, linear in \(\scriptsize N\)N if ``first`,`last`)` is already sorted by value_comp().6,7) Linear in size of other.8,9) Constant. If alloc is given and alloc != other.get_allocator(), then linear.10,11) \(\scriptsize N \cdot log(N)\)N·log(N) where \(\scriptsize N\)N is init.size() in general, linear in \(\scriptsize N\)N if init is already sorted by value_comp().12,13) \(\scriptsize N \cdot log(N)\)N·log(N) where \(\scriptsize N\)N is [ranges::distance(rg) in general, linear in \(\scriptsize N\)N if rg is already sorted by value_comp().

### Exceptions

Calls to `Allocator::allocate` may throw.

### Notes

After container move construction (overload (8,9)), references, pointers, and iterators (other than the end iterator) to `other` remain valid, but refer to elements that are now in \*this. The current standard makes this guarantee via the blanket statement in [[container.reqmts]/67](https://eel.is/c++draft/container.reqmts#67), and a more direct guarantee is under consideration via LWG issue 2321.

Although not formally required until C++23, some implementations has already put the template parameter `Allocator` into non-deduced contexts in earlier modes.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges-aware construction and insertion; overloads (12,13) |

### Example

Run this code

```
#include <iostream>
#include <map>
#include <utility>
 
struct Point { double x, y; };
 
struct PointCmp
{
    bool operator()(const Point& lhs, const Point& rhs) const
    {
        return lhs.x < rhs.x; // NB. ignores y on purpose
    }
};
 
template <typename Key, typename Value, typename Cmp>
void println(auto rem, std::multimap<Key, Value, Cmp> const& map)
{
    std::cout << rem << "{ ";
    for (auto n{map.size()}; auto const& p : map)
        std::cout << '[' << p.first << ":" << p.second << (--n ? "], " : "]");
    std::cout << " }\n";
}
 
int main()
{
    std::multimap<int, int> m1 =
    {
        {1, 1}, {2, 2}, {3, 3}, {4, 4}, {4, 4}, {3, 3}, {2, 2}, {1, 1}
    };
    println("m1 = ", m1);
 
    // Custom comparison
    std::multimap<Point, double, PointCmp> mag
    {
        {{5, 12}, 13},
        {{3, 4}, 5},
        {{8, 15}, 17},
        {{3, -3}, -1}
    };
    for (auto p : mag)
        std::cout << "The magnitude of (" << p.first.x << ", " << p.first.y << ")"
                     " is " << p.second << '\n';
 
    std::cout << "Construction from a range:\n";
    using PS = std::pair<int, std::string>;
    const auto rg = {PS{3, "Earth"}, {2, "Venus"}, {1, "Mercury"}, {3, "Moon"}};
#if __cpp_lib_containers_ranges
    std::multimap<int, std::string> m2(std::from_range, rg); // overload (12)
#else
    std::multimap<int, std::string> m2(rg.begin(), rg.end()); // fallback to (4)
#endif
    println("m2 = ", m2);
}

```

Output:

```
m1 = { [1:1], [1:1], [2:2], [2:2], [3:3], [3:3], [4:4], [4:4] }
The magnitude of (3, 4) is 5
The magnitude of (3, -3) is -1
The magnitude of (5, 12) is 13
The magnitude of (8, 15) is 17
Construction from a range:
m2 = { [1:Mercury], [2:Venus], [3:Earth], [3:Moon] }

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2076 | C++11 | overload (4) conditionally required `Key`and `T` to be CopyInsertable into \*this | not required |
| LWG 2193 | C++11 | the default constructor was explicit | made non-explicit |

### See also

|  |  |
| --- | --- |
| operator= | assigns values to the container   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/multimap/multimap&oldid=135727>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 November 2021, at 07:32.