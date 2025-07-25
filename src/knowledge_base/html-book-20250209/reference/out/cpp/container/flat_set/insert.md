# std::flat_set<Key,Compare,KeyContainer>::insert

From cppreference.com
< cpp‎ | container‎ | flat set
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

std::flat_set

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_set::flat_set | | | | | | flat_set::operator= | | | | | | Iterators | | | | | | flat_set::beginflat_set::cbegin | | | | | | flat_set::endflat_set::cend | | | | | | flat_set::rbeginflat_set::crbegin | | | | | | flat_set::rendflat_set::crend | | | | | | Capacity | | | | | | flat_set::size | | | | | | flat_set::max_size | | | | | | flat_set::empty | | | | | | Observers | | | | | | flat_set::key_comp | | | | | | flat_set::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | flat_set::clear | | | | | | ****flat_set::insert**** | | | | | | flat_set::insert_range | | | | | | flat_set::emplace | | | | | | flat_set::emplace_hint | | | | | | flat_set::erase | | | | | | flat_set::swap | | | | | | flat_set::extract | | | | | | flat_set::replace | | | | | | Lookup | | | | | | flat_set::count | | | | | | flat_set::find | | | | | | flat_set::contains | | | | | | flat_set::equal_range | | | | | | flat_set::lower_bound | | | | | | flat_set::upper_bound | | | | | | | Non-member functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_set) | | | | | | erase_if(std::flat_set) | | | | | | |
| Helper classes | | | | |
| uses_allocator<std::flat_set> | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| std::pair<iterator, bool> insert( const value_type& value ); | (1) | (since C++23) |
| std::pair<iterator, bool> insert( value_type&& value ); | (2) | (since C++23) |
| iterator insert( const_iterator pos, const value_type& value ); | (3) | (since C++23) |
| iterator insert( const_iterator pos, value_type&& value ); | (4) | (since C++23) |
| template< class K >  iterator insert( const_iterator pos, K&& x ); | (5) | (since C++23) |
| template< class InputIt >  void insert( InputIt first, InputIt last ); | (6) | (since C++23) |
| template< class K >  std::pair<iterator, bool> insert( K&& x ); | (7) | (since C++23) |
| template< class InputIt >  void insert( std::sorted_unique_t, InputIt first, InputIt last ); | (8) | (since C++23) |
| void insert( std::initializer_list<key_type> ilist ); | (9) | (since C++23) |
| void insert( std::sorted_unique_t s, std::initializer_list<key_type> ilist ); | (10) | (since C++23) |
|  |  |  |

Inserts element(s) into the container, if the container does not already contain an element with an equivalent key.

1) Inserts value. Equivalent to return emplace(value);.2) Inserts value. Equivalent to return emplace(std::move(value));.3) Inserts value in the position as close as possible to the position just prior to pos. Equivalent to return emplace_hint(pos, value);.4) Inserts value in the position as close as possible to the position just prior to pos. Equivalent to return emplace_hint(pos, std::move(value));.5,7) If \*this already contains an element which transparently compares equivalent to x, does nothing. Otherwise, inserts a new element as if by:

- (5) emplace(pos, std::forward<K>(x)) (in the position as close as possible to the position just prior to pos);
- (7) emplace(std::forward<K>(x)).
 The conversion from x into `key_type` must construct an object u, for which find(k) == find(u) is true. Otherwise, the behavior is undefined. These overloads participate in overload resolution only if

- The qualified-id `Compare::is_transparent` is valid and denotes a type, and
- std::is_constructible_v<value_type, K> is true,

which together allows calling this function without constructing an instance of `Key`.6) Equivalent to the sequence of operations:

1. Inserts elements from range ``first`,`last`)` as if by c.insert(c.end(), first, last);.
2. Sorts the range of newly inserted elements with respect to [`compare`.
3. Merges the resulting sorted range and the sorted range of pre-existing elements into a single sorted range. (Note: the merge operation may allocate memory).
4. Erases all but the first element from each group of consecutive equivalent elements.
 If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending LWG2844).8) Inserts elements from range ``first`,`last`)`. Equivalent to insert(first, last);. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending [LWG2844).9) Inserts elements from initializer list ilist. Equivalent to insert(ilist.begin(), ilist.end());. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending LWG2844).10) Inserts elements from initializer list ilist. Equivalent to insert(s, ilist.begin(), ilist.end());. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending LWG2844).

|  |  |
| --- | --- |
|  | Information on iterator invalidation is copied from here |

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | iterator to the position before which the new element will be inserted |
| value | - | element value to insert |
| first, last | - | range of elements to insert |
| ilist | - | initializer list to insert the values from |
| x | - | a value of any type that can be transparently compared with a key |
| s | - | a disambiguation tag indicating that the input sequence is sorted (with respect to `compare`) and contains only unique elements |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |

### Return value

1,2) A pair consisting of an iterator to the inserted element (or to the element that prevented the insertion) and a bool value set to true if and only if the insertion took place.3-5) An iterator to the inserted element, or to the element that prevented the insertion.6) (none)7) A pair consisting of an iterator to the inserted element (or to the element that prevented the insertion) and a bool value set to true if and only if the insertion took place.8-10) (none)

### Exceptions

1-5,7) If an exception is thrown by any operation, the insertion has no effect.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: cases 6,8-10 |

### Complexity

1-5) Linear in `size()`.6) N + M·log(M), where `N` is the `size()` before the operation and `M` is std::distance(first, last).7) Linear in `size()`.8) Linear in `N`, where `N` is `size()` after the operation.9) N + M·log(M), where `N` is the `size()` before the operation and `M` is ilist.size().10) Linear in `N`, where `N` is `size()` after the operation.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: recheck the complexity: 1-5, 7, 9, 10. The lookup is log(N), but insertion in underlying container is N/2 on average => Linear. |

### Notes

The hinted insert (3-5) does not return a boolean in order to be signature-compatible with positional insert on sequential containers, such as std::vector::insert. This makes it possible to create generic inserters such as std::inserter. One way to check success of a hinted insert is to compare `size()` before and after.

### Example

Run this code

```
#include <cassert>
#include <flat_set>
#include <iostream>
 
int main()
{
    std::flat_set<int> set;
 
    auto result_1 = set.insert(3);
    assert(result_1.first != set.end()); // it is a valid iterator
    assert(*result_1.first == 3);
    if (result_1.second)
        std::cout << "insert done\n";
 
    auto result_2 = set.insert(3);
    assert(result_2.first == result_1.first); // the same iterator
    assert(*result_2.first == 3);
    if (!result_2.second)
        std::cout << "no insertion\n";
}

```

Output:

```
insert done
no insertion

```

### See also

|  |  |
| --- | --- |
| emplace | constructs element in-place   (public member function) |
| emplace_hint | constructs elements in-place using a hint   (public member function) |
| inserter | creates a std::insert_iterator of type inferred from the argument   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_set/insert&oldid=171974>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 May 2024, at 22:14.