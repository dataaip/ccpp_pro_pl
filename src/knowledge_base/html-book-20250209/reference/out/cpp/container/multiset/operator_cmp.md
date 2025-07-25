# operator==,!=,<,<=,>,>=,<=>(std::multiset)

From cppreference.com
< cpp‎ | container‎ | multiset
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

std::multiset

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multiset::multiset | | | | | | multiset::~multiset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multiset::operator= | | | | | | multiset::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | multiset::beginmultiset::cbegin(C++11) | | | | | | multiset::endmultiset::cend(C++11) | | | | | | multiset::rbeginmultiset::crbegin(C++11) | | | | | | multiset::rendmultiset::crend(C++11) | | | | | | Capacity | | | | | | multiset::size | | | | | | multiset::max_size | | | | | | multiset::empty | | | | | | Observers | | | | | | multiset::key_comp | | | | | | multiset::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | multiset::clear | | | | | | multiset::erase | | | | | | multiset::swap | | | | | | multiset::extract(C++17) | | | | | | multiset::merge(C++17) | | | | | | multiset::insert | | | | | | multiset::insert_range(C++23) | | | | | | multiset::emplace(C++11) | | | | | | multiset::emplace_hint(C++11) | | | | | | Lookup | | | | | | multiset::count | | | | | | multiset::find | | | | | | multiset::contains(C++20) | | | | | | multiset::equal_range | | | | | | multiset::lower_bound | | | | | | multiset::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::multiset) | | | | | | erase_if(std::multiset)(C++20) | | | | | | ****operator==operator<=>****(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****operator!=operator<operator>operator<=operator>=****(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<set>` |  |  |
| template< class Key, class Compare, class Alloc >  bool operator==( const std::multiset<Key, Compare, Alloc>& lhs, const std::multiset<Key, Compare, Alloc>& rhs ); | (1) |  |
| template< class Key, class Compare, class Alloc >  bool operator!=( const std::multiset<Key, Compare, Alloc>& lhs, const std::multiset<Key, Compare, Alloc>& rhs ); | (2) | (until C++20) |
| template< class Key, class Compare, class Alloc >  bool operator<( const std::multiset<Key, Compare, Alloc>& lhs, const std::multiset<Key, Compare, Alloc>& rhs ); | (3) | (until C++20) |
| template< class Key, class Compare, class Alloc >  bool operator<=( const std::multiset<Key, Compare, Alloc>& lhs, const std::multiset<Key, Compare, Alloc>& rhs ); | (4) | (until C++20) |
| template< class Key, class Compare, class Alloc >  bool operator>( const std::multiset<Key, Compare, Alloc>& lhs, const std::multiset<Key, Compare, Alloc>& rhs ); | (5) | (until C++20) |
| template< class Key, class Compare, class Alloc >  bool operator>=( const std::multiset<Key, Compare, Alloc>& lhs, const std::multiset<Key, Compare, Alloc>& rhs ); | (6) | (until C++20) |
| template< class Key, class Compare, class Alloc >  synth-three-way-result<T>      operator<=>( const std::multiset<Key, Compare, Alloc>& lhs, const std::multiset<Key, Compare, Alloc>& rhs ); | (7) | (since C++20) |
|  |  |  |

Compares the contents of two `multiset`s.

1,2) Checks if the contents of lhs and rhs are equal, that is, they have the same number of elements and each element in lhs compares equal with the element in rhs at the same position.3-6) Compares the contents of lhs and rhs lexicographically. The comparison is performed by a function equivalent to std::lexicographical_compare. This comparison ignores the `multiset`'s ordering Compare.7) Compares the contents of lhs and rhs lexicographically. The comparison is performed as if by calling std::lexicographical_compare_three_way(lhs.begin(), lhs.end(),  
rhs.begin(), rhs.end(),**synth-three-way**).This comparison ignores the `multiset`'s ordering Compare. The return type is the return type of **synth-three-way** (i.e., **synth-three-way-result** ﻿<T>). If none of the following conditions is satisfied, the behavior is undefined:

- `T` models `three_way_comparable`.
- `<` is defined for values of type (possibly const-qualified) `T`, and `<` is a total ordering relationship.

|  |  |
| --- | --- |
| The `<`, `<=`, `>`, `>=`, and `!=` operators are synthesized from operator<=> and operator== respectively. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | `multiset`s whose contents to compare |
| -`Key` must meet the requirements of EqualityComparable in order to use overloads (1,2). | | |

### Return value

1) true if the contents of the `multiset`s are equal, false otherwise.2) true if the contents of the `multiset`s are not equal, false otherwise.3) true if the contents of the lhs are lexicographically **less** than the contents of rhs, false otherwise.4) true if the contents of the lhs are lexicographically **less** than or **equal** to the contents of rhs, false otherwise.5) true if the contents of the lhs are lexicographically **greater** than the contents of rhs, false otherwise.6) true if the contents of the lhs are lexicographically **greater** than or **equal** to the contents of rhs, false otherwise.7) The relative order of the first pair of non-equivalent elements in lhs and rhs if there are such elements, lhs.size() <=> rhs.size() otherwise.

### Complexity

1,2) Constant if lhs and rhs are of different size, otherwise linear in the size of the `multiset`.3-7) Linear in the size of the `multiset`.

### Notes

|  |  |
| --- | --- |
| The relational operators are defined in terms of the element type's operator<. | (until C++20) |
| The relational operators are defined in terms of **synth-three-way**, which uses operator<=> if possible, or operator< otherwise.  Notably, if the element does not itself provide operator<=>, but is implicitly convertible to a three-way comparable type, that conversion will be used instead of operator<. | (since C++20) |

### Example

Run this code

```
#include <cassert>
#include <compare>
#include <set>
 
int main()
{
    const std::multiset
        a{1, 2, 3},
        b{1, 2, 3},
        c{7, 8, 9, 10};
 
    assert
    (""
        "Compare equal containers:" &&
        (a != b) == false &&
        (a == b) == true &&
        (a < b) == false &&
        (a <= b) == true &&
        (a > b) == false &&
        (a >= b) == true &&
        (a <=> b) != std::weak_ordering::less &&
        (a <=> b) != std::weak_ordering::greater &&
        (a <=> b) == std::weak_ordering::equivalent &&
        (a <=> b) >= 0 &&
        (a <=> b) <= 0 &&
        (a <=> b) == 0 &&
 
        "Compare non equal containers:" &&
        (a != c) == true &&
        (a == c) == false &&
        (a < c) == true &&
        (a <= c) == true &&
        (a > c) == false &&
        (a >= c) == false &&
        (a <=> c) == std::weak_ordering::less &&
        (a <=> c) != std::weak_ordering::equivalent &&
        (a <=> c) != std::weak_ordering::greater &&
        (a <=> c) < 0 &&
        (a <=> c) != 0 &&
        (a <=> c) <= 0 &&
    "");
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3431 | C++20 | operator<=> did not require `T` to model `three_way_comparable` | requires |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/multiset/operator_cmp&oldid=135952>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 November 2021, at 19:36.