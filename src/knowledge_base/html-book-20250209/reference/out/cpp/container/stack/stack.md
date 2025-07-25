# std::stack<T,Container>::stack

From cppreference.com
< cpp‎ | container‎ | stack
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

`std::stack`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****stack::stack**** | | | | |
| stack::~stack | | | | |
| stack::operator= | | | | |
| Element access | | | | |
| stack::top | | | | |
| Capacity | | | | |
| stack::empty | | | | |
| stack::size | | | | |
| Modifiers | | | | |
| stack::push | | | | |
| stack::push_range(C++23) | | | | |
| stack::emplace(C++11) | | | | |
| stack::pop | | | | |
| stack::swap(C++11) | | | | |
| Non-member functions | | | | |
| swap(std::stack)(C++11) | | | | |
| operator==operator!=operator<operator>operator<=operator>=operator<=>(C++20) | | | | |
| Helper classes | | | | |
| uses_allocator<std::stack>(C++11) | | | | |
| formatter<std::stack>(C++23) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| stack() : stack(Container()) {} | (1) | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| explicit stack( const Container& cont = Container() ); |  | (until C++11) |
| explicit stack( const Container& cont ); |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| explicit stack( Container&& cont ); | (3) | (since C++11) |
| stack( const stack& other ); | (4) | (implicitly declared) |
| stack( stack&& other ); | (5) | (since C++11)  (implicitly declared) |
| template< class InputIt >  stack( InputIt first, InputIt last ); | (6) | (since C++23) |
| template< class Alloc >  explicit stack( const Alloc& alloc ); | (7) | (since C++11) |
| template< class Alloc >  stack( const Container& cont, const Alloc& alloc ); | (8) | (since C++11) |
| template< class Alloc >  stack( Container&& cont, const Alloc& alloc ); | (9) | (since C++11) |
| template< class Alloc >  stack( const stack& other, const Alloc& alloc ); | (10) | (since C++11) |
| template< class Alloc >  stack( stack&& other, const Alloc& alloc ); | (11) | (since C++11) |
| template< class InputIt, class Alloc >  stack( InputIt first, InputIt last, const Alloc& alloc ); | (12) | (since C++23) |
| template< container-compatible-range<T> R>  stack( std::from_range_t, R&& rg ); | (13) | (since C++23) |
| template< container-compatible-range<T> R, class Alloc >  stack( std::from_range_t, R&& rg, const Alloc& alloc ); | (14) | (since C++23) |
|  |  |  |

Constructs new underlying container of the container adaptor from a variety of data sources.

1) Default constructor. Value-initializes the container.2) Copy-constructs the underlying container c with the contents of cont. This is also the default constructor.(until C++11)3) Move-constructs the underlying container c with std::move(cont).4) Copy constructor. The adaptor is copy-constructed with the contents of other.c.5) Move constructor. The adaptor is constructed with std::move(other.c).6) Constructs the underlying container c with the contents of the range ``first`,`last`)`. This overload participates in overload resolution only if `InputIt` satisfies [LegacyInputIterator.7-12) These constructors participate in overload resolution only if std::uses_allocator<Container, Alloc>::value is true, that is, if the underlying container is an allocator-aware container (true for all standard library containers that can be used with `stack`).7) Constructs the underlying container using alloc as allocator, as if by c(alloc).8) Constructs the underlying container with the contents of cont and using alloc as allocator, as if by c(cont, alloc).9) Constructs the underlying container with the contents of cont using move semantics while utilizing alloc as allocator, as if by c(std::move(cont), alloc).10) Constructs the adaptor with the contents of other.c and using alloc as allocator, as if by c(other.c, alloc).11) Constructs the adaptor with the contents of other using move semantics while utilizing alloc as allocator, as if by c(std::move(other.c), alloc).12) Constructs the underlying container with the contents of the range ``first`,`last`)` using alloc as allocator, as if by c(first, last, alloc). This overload participates in overload resolution only if `InputIt` satisfies [LegacyInputIterator.13) Constructs the underlying container with ranges::to<Container>(std::forward<R>(rg)).14) Constructs the underlying container with ranges::to<Container>(std::forward<R>(rg), alloc).

### Parameters

|  |  |  |
| --- | --- | --- |
| alloc | - | allocator to use for all memory allocations of the underlying container |
| other | - | another container adaptor to be used as source to initialize the underlying container |
| cont | - | container to be used as source to initialize the underlying container |
| first, last | - | range of elements ``first`,`last`)` to initialize with |
| rg | - | a [container compatible range, that is, an `input_range` whose elements are convertible to `T` |
| Type requirements | | |
| -`Alloc` must meet the requirements of Allocator. | | |
| -`Container` must meet the requirements of Container. The constructors taking an allocator parameter participate in overload resolution only if `Container` meets the requirements of AllocatorAwareContainer. | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |

### Complexity

Same as the corresponding operation on the wrapped container.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_adaptor_iterator_pair_constructor` | `202106L` | (C++23) | Iterator pair constructors for std::queue and std::stack; overloads (6) and (12) |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges-aware construction and insertion; overloads (13) and (14) |

### Example

Run this code

```
#include <cassert>
#include <deque>
#include <iostream>
#include <memory>
#include <ranges>
#include <stack>
 
int main()
{
    std::stack<int> c1;
    c1.push(5);
    assert(c1.size() == 1);
 
    std::stack<int> c2(c1);
    assert(c2.size() == 1);
 
    std::deque<int> deq{3, 1, 4, 1, 5};
    std::stack<int> c3(deq); // overload (2)
    assert(c3.size() == 5);
 
# ifdef __cpp_lib_adaptor_iterator_pair_constructor
    const auto il = {2, 7, 1, 8, 2};
    std::stack<int> c4{il.begin(), il.end()}; // C++23, (6)
    assert(c4.size() == 5);
# endif
 
# if __cpp_lib_containers_ranges >= 202202L
    // C++23, overload (13)
    auto c5 = std::stack(std::from_range_t, std::ranges::iota(0, 42));
    assert(c5.size() == 42);
 
    // the same effect with pipe syntax, internally uses overload (13)
    auto c6 = std::ranges::iota(0, 42) | std::ranges::to<std::stack>();
    assert(c6.size() == 42);
 
    std::allocator<int> alloc;
 
    // C++23, overload (14)
    auto c7 = std::stack(std::from_range_t, std::ranges::iota(0, 42), alloc);
    assert(c7.size() == 42);
 
    // the same effect with pipe syntax, internally uses overload (14)
    auto c8 = std::ranges::iota(0, 42) | std::ranges::to<std::stack>(alloc);
    assert(c8.size() == 42);
# endif
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P0935R0 | C++11 | default constructor was explicit | made implicit |

### See also

|  |  |
| --- | --- |
| operator= | assigns values to the container adaptor   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/stack/stack&oldid=129996>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 June 2021, at 02:58.