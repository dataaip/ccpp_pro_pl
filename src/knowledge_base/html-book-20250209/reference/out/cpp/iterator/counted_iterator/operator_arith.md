# std::counted_iterator<I>::operator++,+,+=,--,-,-=

From cppreference.com
< cpp‎ | iterator‎ | counted iterator
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

Iterator library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Iterator concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_readable(C++20) | | | | | | indirectly_writable(C++20) | | | | | | weakly_incrementable(C++20) | | | | | | incrementable(C++20) | | | | | | **is-integer-like** **is-signed-integer-like**(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sentinel_for(C++20) | | | | | | sized_sentinel_for(C++20) | | | | | | input_iterator(C++20) | | | | | | output_iterator(C++20) | | | | | | input_or_output_iterator(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_iterator(C++20) | | | | | | bidirectional_iterator(C++20) | | | | | | random_access_iterator(C++20) | | | | | | contiguous_iterator(C++20) | | | | | |  | | | | | |  | | | | | |
| Iterator primitives | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | input_iterator_tagoutput_iterator_tagforward_iterator_tagbidirectional_iterator_tagrandom_access_iterator_tagcontiguous_iterator_tag(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iter_value_titer_difference_titer_reference_titer_const_reference_titer_rvalue_reference_titer_common_reference_t(C++20)(C++20)(C++20)(C++23)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iterator(deprecated in C++17) | | | | | | iterator_traits | | | | | | incrementable_traits(C++20) | | | | | | indirectly_readable_traits(C++20) | | | | | |  | | | | | |  | | | | | |
| Algorithm concepts and utilities | | | | |
| Indirect callable concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_unary_invocableindirectly_regular_unary_invocable(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_unary_predicate(C++20) | | | | | | indirect_binary_predicate(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_equivalence_relation(C++20) | | | | | | indirect_strict_weak_order(C++20) | | | | | |
| Common algorithm requirements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_movable(C++20) | | | | | | indirectly_movable_storable(C++20) | | | | | | indirectly_copyable(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_copyable_storable(C++20) | | | | | | indirectly_swappable(C++20) | | | | | | indirectly_comparable(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | permutable(C++20) | | | | | | mergeable(C++20) | | | | | | sortable(C++20) | | | | | |
| Utilities | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_result_t(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | projected(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | projected_value_t(C++26) | | | | | |
| Iterator adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_iterator | | | | | | make_reverse_iterator(C++14) | | | | | | move_iterator(C++11) | | | | | | make_move_iterator(C++11) | | | | | | default_sentinel_tdefault_sentinel(C++20)(C++20) | | | | | | unreachable_sentinel_tunreachable_sentinel(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | front_insert_iterator | | | | | | back_insert_iterator | | | | | | inserter | | | | | | insert_iterator | | | | | | front_inserter | | | | | | back_inserter | | | | | | move_sentinel(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_iterator(C++20) | | | | | | counted_iterator(C++20) | | | | | | basic_const_iterator(C++23) | | | | | | const_iterator(C++23) | | | | | | const_sentinel(C++23) | | | | | | make_const_iterator(C++23) | | | | | | make_const_sentinel(C++23) | | | | | |  | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Stream iterators | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istream_iterator | | | | | | ostream_iterator | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istreambuf_iterator | | | | | | ostreambuf_iterator | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator customization points | | | | | | ranges::iter_move(C++20) | | | | | | ranges::iter_swap(C++20) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator operations | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | advance | | | | | | distance | | | | | | prev(C++11) | | | | | | next(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ranges::advance(C++20) | | | | | | ranges::distance(C++20) | | | | | | ranges::prev(C++20) | | | | | | ranges::next(C++20) | | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | begincbegin(C++11)(C++14) | | | | | | rbegincrbegin(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | endcend(C++11)(C++14) | | | | | | rendcrend(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sizessize(C++17)(C++20) | | | | | | empty(C++17) | | | | | | data(C++17) | | | | | | | |

std::counted_iterator

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| counted_iterator::counted_iterator | | | | |
| counted_iterator::operator= | | | | |
| counted_iterator::base | | | | |
| counted_iterator::count | | | | |
| counted_iterator::operator\*counted_iterator::operator-> | | | | |
| [counted_iterator::operator[]](operator_at.html "cpp/iterator/counted iterator/operator at") | | | | |
| ****counted_iterator::operator++counted_iterator::operator++(int)counted_iterator::operator+counted_iterator::operator+=counted_iterator::operator--counted_iterator::operator--(int)counted_iterator::operator-counted_iterator::operator-=**** | | | | |
| Non-member functions | | | | |
| operator==operator<=>(C++20)(C++20) | | | | |
| operator==(default_sentinel_t)(C++20) | | | | |
| operator+(C++20) | | | | |
| operator-(C++20) | | | | |
| operator-(default_sentinel_t)(C++20) | | | | |
| iter_move(C++20) | | | | |
| iter_swap(C++20) | | | | |
| Helper classes | | | | |
| iterator_traits<std::counted_iterator>(C++20) | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr counted_iterator& operator++(); | (1) | (since C++20) |
| constexpr decltype(auto) operator++( int ); | (2) | (since C++20) |
| constexpr counted_iterator operator++( int )      requires std::forward_iterator<I>; | (3) | (since C++20) |
| constexpr counted_iterator& operator--()      requires std::bidirectional_iterator<I>; | (4) | (since C++20) |
| constexpr counted_iterator operator--( int )      requires std::bidirectional_iterator<I>; | (5) | (since C++20) |
| constexpr counted_iterator operator+( std::iter_difference_t<I> n ) const      requires std::random_access_iterator<I>; | (6) | (since C++20) |
| constexpr counted_iterator& operator+=( std::iter_difference_t<I> n )      requires std::random_access_iterator<I>; | (7) | (since C++20) |
| constexpr counted_iterator operator-( std::iter_difference_t<I> n ) const      requires std::random_access_iterator<I>; | (8) | (since C++20) |
| constexpr counted_iterator& operator-=( std::iter_difference_t<I> n )      requires std::random_access_iterator<I>; | (9) | (since C++20) |
|  |  |  |

Increments or decrements the underlying iterator `current` and the distance to the end `length`.

The behavior of these functions is undefined if the `length` would be set to a minus value.

1) Pre-increments by one. Equivalent to ++current; --length; return \*this;.2) Post-increments by one. Equivalent to --length; try { return current++; } catch(...) { ++length; throw; }.3) Post-increments by one. Equivalent to counted_iterator temp{\*this}; ++\*this; return temp;.4) Pre-decrements by one. Equivalent to --current; ++length; return \*this;.5) Post-decrements by one. Equivalent to counted_iterator temp{\*this}; --\*this; return temp;.6) Returns an iterator adaptor which is advanced by n. Equivalent to return counted_iterator(current + n, length - n);.7) Advances the iterator adaptor by n. Equivalent to current += n; length -= n; return \*this;.8) Returns an iterator adaptor which is advanced by -n. Equivalent to return counted_iterator(current - n, length + n);.9) Advances the iterator adaptor by -n. Equivalent to current -= n; length += n; return \*this;.

### Parameters

|  |  |  |
| --- | --- | --- |
| n | - | the number of positions to increment or decrement the iterator adaptor |

### Return value

1) \*this2,3) A copy of \*this that was made before the change.4) \*this5) A copy of \*this that was made before the change.6) An iterator adaptor which is advanced by n.7) \*this8) An iterator adaptor which is advanced by -n.9) \*this

### Example

Run this code

```
#include <cassert>
#include <initializer_list>
#include <iterator>
 
int main()
{
    const auto v = {1, 2, 3, 4, 5, 6};
    std::counted_iterator<std::initializer_list<int>::iterator> it1{v.begin(), 5};
 
    ++it1;              assert(*it1 == 2 && it1.count() == 4); // (1)
    auto it2 = it1++;   assert(*it2 == 2 && *it1 == 3);        // (3)
    --it1;              assert(*it1 == 2 && it1.count() == 4); // (4)
    auto it3 = it1--;   assert(*it3 == 2 && *it1 == 1);        // (5)
    auto it4 = it1 + 3; assert(*it4 == 4 && it4.count() == 2); // (6)
    auto it5 = it4 - 3; assert(*it5 == 1 && it5.count() == 5); // (8)
    it1 += 3;           assert(*it1 == 4 && it1.count() == 2); // (7)
    it1 -= 3;           assert(*it1 == 1 && it1.count() == 5); // (9)
}

```

### See also

|  |  |
| --- | --- |
| operator+(C++20) | advances the iterator   (function template) |
| operator-(C++20) | computes the distance between two iterator adaptors   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator/counted_iterator/operator_arith&oldid=159836>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 September 2023, at 23:22.