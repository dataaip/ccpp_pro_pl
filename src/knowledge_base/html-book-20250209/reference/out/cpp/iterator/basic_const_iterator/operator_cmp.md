# std::basic_const_iterator<Iter>::operator==,<,<=,>,>=,<=>

From cppreference.com
< cpp‎ | iterator‎ | basic const iterator
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

std::basic_const_iterator

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| basic_const_iterator::basic_const_iterator | | | | |
| basic_const_iterator::base | | | | |
| basic_const_iterator::operator\*basic_const_iterator::operator-> | | | | |
| [basic_const_iterator::operator[]](operator_at.html "cpp/iterator/basic const iterator/operator at") | | | | |
| basic_const_iterator::operator++basic_const_iterator::operator+=basic_const_iterator::operator--basic_const_iterator::operator-= | | | | |
| ****basic_const_iterator::operator==basic_const_iterator::operator<basic_const_iterator::operator<=basic_const_iterator::operator>basic_const_iterator::operator>=basic_const_iterator::operator<=>**** | | | | |
| basic_const_iterator::operator **constant-iterator** | | | | |
| Non-member functions | | | | |
| operator<operator<=operator>operator>=(C++23)(C++23)(C++23)(C++23) | | | | |
| operator+(C++23) | | | | |
| operator-(C++23) | | | | |
| iter_move(std::basic_const_iterator)(C++23) | | | | |
| Helper classes | | | | |
| common_type<std::basic_const_iterator>(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| Equality comparison |  |  |
| template< std::sentinel_for<Iter> S >  constexpr bool operator==( const S& s ) const; | (1) | (since C++23) |
| Relational comparisons between two `basic_const_iterator`s |  |  |
| constexpr bool operator<( const basic_const_iterator& y ) const      requires std::random_access_iterator<Iter>; | (2) | (since C++23) |
| constexpr bool operator>( const basic_const_iterator& y ) const      requires std::random_access_iterator<Iter>; | (3) | (since C++23) |
| constexpr bool operator<=( const basic_const_iterator& y ) const      requires std::random_access_iterator<Iter>; | (4) | (since C++23) |
| constexpr bool operator>=( const basic_const_iterator& y ) const      requires std::random_access_iterator<Iter>; | (5) | (since C++23) |
| constexpr auto operator<=>( const basic_const_iterator& y ) const      requires std::random_access_iterator<Iter> && std::three_way_comparable<Iter>; | (6) | (since C++23) |
| Relational comparisons between `basic_const_iterator` and another type |  |  |
| template< /\*different-from\*/<basic_const_iterator> I >  constexpr bool operator<( const I& y ) const     requires std::random_access_iterator<Iter> && std::totally_ordered_with<Iter, I>; | (7) | (since C++23) |
| template< /\*different-from\*/<basic_const_iterator> I >  constexpr bool operator>( const I& y ) const     requires std::random_access_iterator<Iter> && std::totally_ordered_with<Iter, I>; | (8) | (since C++23) |
| template< /\*different-from\*/<basic_const_iterator> I >  constexpr bool operator<=( const I& y ) const     requires std::random_access_iterator<Iter> && std::totally_ordered_with<Iter, I>; | (9) | (since C++23) |
| template< /\*different-from\*/<basic_const_iterator> I >  constexpr bool operator>=( const I& y ) const     requires std::random_access_iterator<Iter> && std::totally_ordered_with<Iter, I>; | (10) | (since C++23) |
| template< /\*different-from\*/<basic_const_iterator> I >  constexpr auto operator<=>( const I& y ) const      requires std::random_access_iterator<Iter> &&          std::totally_ordered_with<Iter, I> && std::three_way_comparable_with<Iter, I>; | (11) | (since C++23) |
|  |  |  |

Compares a `basic_const_iterator` with another value.

The `!=` operator is synthesized from `operator==`.

I satisfies /\*different-from\*/<basic_const_iterator> if std::same_as<I, basic_const_iterator<Iter>> is false.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | a sentinel for `Iter` |
| y | - | a value to compare with |

### Return value

1) base() == s2) base() < y.base()3) base() > y.base()4) base() <= y.base()5) base() >= y.base()6) base() <=> y.base()7) base() < y8) base() > y9) base() <= y10) base() >= y11) base() <=> y

### Notes

Overload (1) can be used to compare two `basic_const_iterator<Iter>` values if `Iter` models sentinel_for<Iter>.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |  |  |
| --- | --- | --- | --- |
| |  |  | | --- | --- | |  | This section is incomplete | | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator/basic_const_iterator/operator_cmp&oldid=171074>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 April 2024, at 13:34.