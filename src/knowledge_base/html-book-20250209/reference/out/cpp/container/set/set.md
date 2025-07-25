# std::set<Key,Compare,Allocator>::set

From cppreference.com
< cpp‎ | container‎ | set
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

std::set

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****set::set**** | | | | | | set::~set | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set::operator= | | | | | | set::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | set::beginset::cbegin(C++11) | | | | | | set::endset::cend(C++11) | | | | | | set::rbeginset::crbegin(C++11) | | | | | | set::rendset::crend(C++11) | | | | | | Capacity | | | | | | set::size | | | | | | set::max_size | | | | | | set::empty | | | | | | Observers | | | | | | set::key_comp | | | | | | set::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | set::clear | | | | | | set::erase | | | | | | set::swap | | | | | | set::extract(C++17) | | | | | | set::merge(C++17) | | | | | | set::insert | | | | | | set::insert_range(C++23) | | | | | | set::emplace(C++11) | | | | | | set::emplace_hint(C++11) | | | | | | Lookup | | | | | | set::count | | | | | | set::find | | | | | | set::contains(C++20) | | | | | | set::equal_range | | | | | | set::lower_bound | | | | | | set::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | std::swap(std::set) | | | | | | erase_if(std::set)(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| set(); |  | (until C++11) |
| set()      : set(Compare()) {} |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| explicit set( const Compare& comp,                const Allocator& alloc = Allocator() ); | (2) |  |
| explicit set( const Allocator& alloc ); | (3) | (since C++11) |
|  |  |  |
| --- | --- | --- |
| template< class InputIt >  set( InputIt first, InputIt last,       const Compare& comp = Compare(), const Allocator& alloc = Allocator() ); | (4) |  |
| template< class InputIt >  set( InputIt first, InputIt last,       const Allocator& alloc ) : set(first, last, Compare(), alloc) {} | (5) | (since C++14) |
|  |  |  |
| --- | --- | --- |
| set( const set& other ); | (6) |  |
| set( const set& other, const Allocator& alloc ); | (7) | (since C++11) |
|  |  |  |
| --- | --- | --- |
| set( set&& other ); | (8) | (since C++11) |
| set( set&& other, const Allocator& alloc ); | (9) | (since C++11) |
|  |  |  |
| --- | --- | --- |
| set( std::initializer_list<value_type> init,  const Compare& comp = Compare(), const Allocator& alloc = Allocator() ); | (10) | (since C++11) |
| set( std::initializer_list<value_type> init,  const Allocator& alloc ) : set(init, Compare(), alloc) {} | (11) | (since C++14) |
|  |  |  |
| --- | --- | --- |
| template< container-compatible-range<value_type> R >  set( std::from_range_t, R&& rg,       const Compare& comp = Compare(), const Allocator& alloc = Allocator() ); | (12) | (since C++23) |
| template< container-compatible-range<value_type> R >  set( std::from_range_t, R&& rg,       const Allocator& alloc ) : set(std::from_range, std::forward<R>(rg), Compare(), alloc) {} | (13) | (since C++23) |
|  |  |  |

Constructs new container from a variety of data sources and optionally using user supplied allocator alloc or comparison function object comp.

1-3) Constructs an empty container.4,5) Constructs the container with the contents of the range ``first`,`last`)`. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending [LWG2844). If ``first`,`last`)` is not a [valid range, the behavior is undefined.6,7) Copy constructor. Constructs the container with the copy of the contents of other.

|  |  |
| --- | --- |
| If alloc is not provided, allocator is obtained by calling std::allocator_traits<allocator_type>::     select_on_container_copy_construction(other.get_allocator()). | (since C++11) |
| During class template argument deduction, only the first argument contributes to the deduction of the container's `Allocator` template parameter. | (since C++23) |

8,9) Move constructor. Constructs the container with the contents of other using move semantics. If alloc is not provided, allocator is obtained by move-construction from the allocator belonging to other.

|  |  |
| --- | --- |
| During class template argument deduction, only the first argument contributes to the deduction of the container's `Allocator` template parameter. | (since C++23) |

10,11) Initializer-list constructor. Constructs the container with the contents of the initializer list init.If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending LWG2844).12,13) Constructs the container with the contents of rg. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending LWG2844).

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
#include <cmath>
#include <iostream>
#include <set>
#include <string>
 
struct Point { double x, y; };
 
struct PointCmp
{
    bool operator()(const Point& lhs, const Point& rhs) const
    {
        return std::hypot(lhs.x, lhs.y) < std::hypot(rhs.x, rhs.y);
    }
};
 
std::ostream& operator<<(std::ostream& os, Point pt)
{
    return os << '(' << pt.x << ',' << pt.x << ')';
}
 
void println(auto rem, const auto& seq)
{
    std::cout << rem << '{';
    for (auto n{seq.size()}; const auto& elm : seq)
        std::cout << elm << (--n ? ", " : "");
    std::cout << "}\n";
}
 
int main()
{
    // (1) Default constructor
    std::set<std::string> a;
    a.insert("horse");
    a.insert("cat");
    a.insert("dog");
    println("1) a: ", a);
 
    // (4) Range constructor
    std::set<std::string> b(a.find("dog"), a.end());
    println("2) b: ", b);
 
    // (6) Copy constructor
    std::set<std::string> c(a);
    c.insert("another horse");
    println("3) c: ", c);
 
    // (8) Move constructor
    std::set<std::string> d(std::move(a));
    println("4) d: ", d);
    println("5) a: ", a);
 
    // (10) Initializer list constructor
    std::set<std::string> e{"one", "two", "three", "five", "eight"};
    println("6) e: ", e);
 
    // Custom comparison
    std::set<Point, PointCmp> f = {{2, 5}, {3, 4}, {1, 1}};
    f.insert({1, -1}); // This fails because the magnitude of (1,-1) equals (1,1)
    println("7) f: ", f);
 
    // (12) Range constructor
    const auto w = {"Eurybia", "Theia", "Rhea", "Aura", "Mnemosyne", "Mnemosyne"};
#if __cpp_lib_containers_ranges
    std::set<std::string> g(std::from_range, w); // overload (12)
#else
    std::set<std::string> g(w.begin(), w.end()); // fallback to (4)
#endif
    println("8) g: ", g);
}

```

Possible output:

```
1) a: {cat, dog, horse}
2) b: {dog, horse}
3) c: {another horse, cat, dog, horse}
4) d: {cat, dog, horse}
5) a: {}
6) e: {eight, five, one, three, two}
7) f: {(1,1), (3,3), (2,2)}
8) g: {Aura, Eurybia, Mnemosyne, Rhea, Theia}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2076 | C++11 | overload (4) conditionally required `Key` to be CopyInsertable into \*this | not required |
| LWG 2193 | C++11 | the default constructor was explicit | made non-explicit |

### See also

|  |  |
| --- | --- |
| operator= | assigns values to the container   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/set/set&oldid=154696>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 July 2023, at 06:49.