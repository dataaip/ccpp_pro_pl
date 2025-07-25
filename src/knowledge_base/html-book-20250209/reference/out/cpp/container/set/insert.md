# std::set<Key,Compare,Allocator>::insert

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set::set | | | | | | set::~set | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set::operator= | | | | | | set::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | set::beginset::cbegin(C++11) | | | | | | set::endset::cend(C++11) | | | | | | set::rbeginset::crbegin(C++11) | | | | | | set::rendset::crend(C++11) | | | | | | Capacity | | | | | | set::size | | | | | | set::max_size | | | | | | set::empty | | | | | | Observers | | | | | | set::key_comp | | | | | | set::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | set::clear | | | | | | set::erase | | | | | | set::swap | | | | | | set::extract(C++17) | | | | | | set::merge(C++17) | | | | | | ****set::insert**** | | | | | | set::insert_range(C++23) | | | | | | set::emplace(C++11) | | | | | | set::emplace_hint(C++11) | | | | | | Lookup | | | | | | set::count | | | | | | set::find | | | | | | set::contains(C++20) | | | | | | set::equal_range | | | | | | set::lower_bound | | | | | | set::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | std::swap(std::set) | | | | | | erase_if(std::set)(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| std::pair<iterator, bool> insert( const value_type& value ); | (1) |  |
| std::pair<iterator, bool> insert( value_type&& value ); | (2) | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| iterator insert( iterator pos, const value_type& value ); |  | (until C++11) |
| iterator insert( const_iterator pos, const value_type& value ); |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| iterator insert( const_iterator pos, value_type&& value ); | (4) | (since C++11) |
| template< class InputIt >  void insert( InputIt first, InputIt last ); | (5) |  |
| void insert( std::initializer_list<value_type> ilist ); | (6) | (since C++11) |
| insert_return_type insert( node_type&& nh ); | (7) | (since C++17) |
| iterator insert( const_iterator pos, node_type&& nh ); | (8) | (since C++17) |
| template< class K >  std::pair<iterator, bool> insert( K&& x ); | (9) | (since C++23) |
| template< class K >  iterator insert( const_iterator pos, K&& x ); | (10) | (since C++23) |
|  |  |  |

Inserts element(s) into the container, if the container doesn't already contain an element with an equivalent key.

1,2) Inserts value.3,4) Inserts value in the position as close as possible to the position just prior to pos.5) Inserts elements from range ``first`,`last`)`. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending [LWG2844).6) Inserts elements from initializer list ilist. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending LWG2844).7) If nh is an empty node handle, does nothing. Otherwise, inserts the element owned by nh into the container , if the container doesn't already contain an element with a key equivalent to nh.key(). The behavior is undefined if nh is not empty and get_allocator() != nh.get_allocator().8) If nh is an empty node handle, does nothing and returns the end iterator. Otherwise, inserts the element owned by nh into the container, if the container doesn't already contain an element with a key equivalent to nh.key(), and returns the iterator pointing to the element with key equivalent to nh.key()(regardless of whether the insert succeeded or failed). If the insertion succeeds, nh is moved from, otherwise it retains ownership of the element. The element is inserted as close as possible to the position just prior to pos. The behavior is undefined if nh is not empty and get_allocator() != nh.get_allocator().9) If \*this already contains an element which transparently compares **equivalent** to x, does nothing. Otherwise, constructs an object `u` of the `value_type` with std::forward<K>(x) and then inserts `u` into \*this. If equal_range(u) == equal_range(x) is false, the behavior is undefined. The `value_type` must be EmplaceConstructible into `set` from std::forward<K>(x). This overload participates in overload resolution only if the qualified-id Compare::is_transparent is valid and denotes a type. It allows calling this function without constructing an instance of `Key`.10) If \*this already contains an element which transparently compares **equivalent** to x, does nothing. Otherwise, constructs an object `u` of the `value_type` with std::forward<K>(x) and then inserts `u` into \*this in the position as close as possible to the position just prior to pos. If equal_range(u) == equal_range(x) is false, the behavior is undefined. The `value_type` must be EmplaceConstructible into `set` from std::forward<K>(x). This overload participates in overload resolution only if:

- std::is_convertible_v<K&&, const_iterator> and std::is_convertible_v<K&&, iterator> are both false, and
- the qualified-id Compare::is_transparent is valid and denotes a type,

which together allows calling this function without constructing an instance of `Key`.

No iterators or references are invalidated. If the insertion is successful, pointers and references to the element obtained while it is held in the node handle are invalidated, and pointers and references obtained to that element before it was extracted become valid.(since C++17)

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | iterator to the position before which the new element will be inserted |
| value | - | element value to insert |
| first, last | - | range of elements to insert |
| ilist | - | initializer list to insert the values from |
| nh | - | a compatible node handle |
| x | - | a value of any type that can be transparently compared with a key |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |

### Return value

1,2) A pair consisting of an iterator to the inserted element (or to the element that prevented the insertion) and a bool value set to true if and only if the insertion took place.3,4) An iterator to the inserted element, or to the element that prevented the insertion.5,6) (none)7) An object of `insert_return_type` with the members initialized as follows:

- If nh is empty, `inserted` is false, `position` is end(), and `node` is empty.
- Otherwise if the insertion took place, `inserted` is true, `position` points to the inserted element, and `node` is empty.
- If the insertion failed, `inserted` is false, `node` has the previous value of nh, and `position` points to an element with a key equivalent to nh.key().
8) End iterator if nh was empty, iterator pointing to the inserted element if insertion took place, and iterator pointing to an element with a key equivalent to nh.key() if it failed.9) A pair consisting of an iterator to the inserted element (or to the element that prevented the insertion) and a bool value set to true if and only if the insertion took place.10) An iterator to the inserted element, or to the element that prevented the insertion.

### Exceptions

1-4) If an exception is thrown by any operation, the insertion has no effect.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: cases 5-8, 9, 10 |

### Complexity

1,2) Logarithmic in the size of the container, `O(log(size()))`.3,4) Amortized constant if the insertion happens in the position just **after**(until C++11)**before**(since C++11) pos, logarithmic in the size of the container otherwise.5,6) `O(N·log(size() + N))`, where `N` is the number of elements to insert.7) Logarithmic in the size of the container, `O(log(size()))`.8) Amortized constant if the insertion happens in the position just **before** pos, logarithmic in the size of the container otherwise.9) Logarithmic in the size of the container, `O(log(size()))`.10) Amortized constant if the insertion happens in the position just **before** pos, logarithmic in the size of the container otherwise.

### Notes

The hinted insert (3,4) does not return a boolean in order to be signature-compatible with positional insert on sequential containers, such as std::vector::insert. This makes it possible to create generic inserters such as std::inserter. One way to check success of a hinted insert is to compare `size()` before and after.

The overloads (5,6) are often implemented as a loop that calls the overload (3) with end() as the hint; they are optimized for appending a sorted sequence (such as another std::set) whose smallest element is greater than the last element in \*this.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_associative_heterogeneous_insertion` | `202311L` | (C++26) | Heterogeneous overloads for the remaining member functions in ordered and unordered associative containers. (9,10) |

### Example

Run this code

```
#include <cassert>
#include <iostream>
#include <set>
 
int main()
{
    std::set<int> set;
 
    auto result_1 = set.insert(3);
    assert(result_1.first != set.end()); // it is a valid iterator
    assert(*result_1.first == 3);
    if (result_1.second)
        std::cout << "insert done\n";
 
    auto result_2 = set.insert(3);
    assert(result_2.first == result_1.first); // same iterator
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

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 233 | C++98 | pos was just a hint, it could be totally ignored | the insertion is required to be as close as possible to the position just prior to pos |
| LWG 264 | C++98 | the complexity of overload (5) was required to be linear if the range ``first`,`last`)` is sorted according to `Compare` | removed the linear requirement in this special case |
| [LWG 316 | C++98 | in the return value of overload (1), it was not specified which bool value indicates a successful insertion | success is indicated by true |

### See also

|  |  |
| --- | --- |
| emplace(C++11) | constructs element in-place   (public member function) |
| emplace_hint(C++11) | constructs elements in-place using a hint   (public member function) |
| inserter | creates a std::insert_iterator of type inferred from the argument   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/set/insert&oldid=170187>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 March 2024, at 10:31.