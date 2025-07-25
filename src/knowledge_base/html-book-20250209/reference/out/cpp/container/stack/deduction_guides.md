# deduction guides for `std::stack`

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
| stack::stack | | | | |
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
| ****Deduction guides****(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stack>` |  |  |
| template< class Container >  stack( Container ) -> stack<typename Container::value_type, Container>; | (1) | (since C++17) |
| template< class Container, class Alloc >  stack( Container, Alloc ) -> stack<typename Container::value_type, Container>; | (2) | (since C++17) |
| template< class InputIt >  stack( InputIt, InputIt ) -> stack<typename std::iterator_traits<InputIt>::value_type>; | (3) | (since C++23) |
| template< class InputIt, class Alloc >  stack( InputIt, InputIt, Alloc )      -> stack<typename std::iterator_traits<InputIt>::value_type, std::deque<typename std::iterator_traits<InputIt>::value_type, Alloc>>; | (4) | (since C++23) |
| template< ranges::input_range R >  stack( std::from_range_t, R&& ) -> stack<ranges::range_value_t<R>>; | (5) | (since C++23) |
| template< ranges::input_range R, class Allocator >  stack( std::from_range_t, R&&, Allocator )      -> stack<ranges::range_value_t<R>, std::deque<ranges::range_value_t<R>, Allocator>>; | (6) | (since C++23) |
|  |  |  |

These deduction guides are provided for `stack` to allow deduction from underlying container type.

1) Deduces underlying container type from the argument.2) Same as (1), except that the allocator is provided.3) Deduces the element type from the iterator, using std::deque<typename std::iterator_traits<InputIt>::value_type> as the underlying container type.4) Same as (3), except that the allocator is provided.5) Deduces the element type from a std::from_range_t tag and an input_range.6) Same as (5), except that the allocator is provided.

These overloads participate in overload resolution only if

- `InputIt` (if exists) satisfies LegacyInputIterator,
- `Container` (if exists) does not satisfy Allocator,
- for (3)(until C++23)(4)(since C++23), `Alloc` satisfies Allocator, and
- std::uses_allocator_v<Container, Alloc> is true if both `Container` and `Alloc` exist.

Note: the extent to which the library determines that a type does not satisfy LegacyInputIterator is unspecified, except that as a minimum integral types do not qualify as input iterators. Likewise, the extent to which it determines that a type does not satisfy Allocator is unspecified, except that as a minimum the member type `Alloc::value_type` must exist and the expression std::declval<Alloc&>().allocate(std::size_t{}) must be well-formed when treated as an unevaluated operand.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_adaptor_iterator_pair_constructor` | `202106L` | (C++23) | Iterator pair constructors for std::queue and std::stack; overloads (2) and (4) |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges-aware construction and insertion; overloads (5) and (6) |

### Example

Run this code

```
#include <stack>
#include <vector>
 
int main()
{
    std::vector<int> v = {1, 2, 3, 4};
    std::stack s{v}; // guide #1 deduces std::stack<int, vector<int>>
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/stack/deduction_guides&oldid=129992>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 June 2021, at 02:55.