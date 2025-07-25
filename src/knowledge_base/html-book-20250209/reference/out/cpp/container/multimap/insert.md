# std::multimap<Key,T,Compare,Allocator>::insert

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multimap::multimap | | | | | | multimap::~multimap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multimap::operator= | | | | | | multimap::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | multimap::beginmultimap::cbegin(C++11) | | | | | | multimap::endmultimap::cend(C++11) | | | | | | multimap::rbeginmultimap::crbegin(C++11) | | | | | | multimap::rendmultimap::crend(C++11) | | | | | | Capacity | | | | | | multimap::size | | | | | | multimap::max_size | | | | | | multimap::empty | | | | | | Observers | | | | | | multimap::key_comp | | | | | | multimap::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | multimap::clear | | | | | | ****multimap::insert**** | | | | | | multimap::erase | | | | | | multimap::swap | | | | | | multimap::merge(C++17) | | | | | | multimap::insert_range(C++23) | | | | | | multimap::emplace(C++11) | | | | | | multimap::emplace_hint(C++11) | | | | | | multimap::extract(C++17) | | | | | | Lookup | | | | | | multimap::count | | | | | | multimap::find | | | | | | multimap::contains(C++20) | | | | | | multimap::equal_range | | | | | | multimap::lower_bound | | | | | | multimap::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | std::swap(std::multimap) | | | | | | erase_if(std::multimap)(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| iterator insert( const value_type& value ); | (1) |  |
| iterator insert( value_type&& value ); | (2) | (since C++17) |
| template< class P >  iterator insert( P&& value ); | (3) | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| iterator insert( iterator pos, const value_type& value ); |  | (until C++11) |
| iterator insert( const_iterator pos, const value_type& value ); |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| iterator insert( const_iterator pos, value_type&& value ); | (5) | (since C++17) |
| template< class P >  iterator insert( const_iterator pos, P&& value ); | (6) | (since C++11) |
| template< class InputIt >  void insert( InputIt first, InputIt last ); | (7) |  |
| void insert( std::initializer_list<value_type> ilist ); | (8) | (since C++11) |
| iterator insert( node_type&& nh ); | (9) | (since C++17) |
| iterator insert( const_iterator pos, node_type&& nh ); | (10) | (since C++17) |
|  |  |  |

Inserts element(s) into the container.

1-3) Inserts value. If the container has elements with equivalent key, inserts at the upper bound of that range. Overload (3) is equivalent to emplace(std::forward<P>(value)) and only participates in overload resolution if std::is_constructible<value_type, P&&>::value == true.4-6) Inserts value in the position as close as possible to the position just prior to pos. Overload (6) is equivalent to emplace_hint(hint, std::forward<P>(value)) and only participates in overload resolution if std::is_constructible<value_type, P&&>::value == true.7) Inserts elements from range ``first`,`last`)`.8) Inserts elements from initializer list ilist.9) If nh is an empty [node handle, does nothing. Otherwise, inserts the element owned by nh into the container and returns an iterator pointing at the inserted element. If a range containing elements with keys equivalent to nh.key() exists in the container, the element is inserted at the end of that range. The behavior is undefined if nh is not empty and get_allocator() != nh.get_allocator().10) If nh is an empty node handle, does nothing and returns the end iterator. Otherwise, inserts the element owned by nh into the container, and returns the iterator pointing to the element with key equivalent to nh.key(). The element is inserted as close as possible to the position just prior to pos. The behavior is undefined if nh is not empty and get_allocator() != nh.get_allocator().

No iterators or references are invalidated. If the insertion is successful, pointers and references to the element obtained while it is held in the node handle are invalidated, and pointers and references obtained to that element before it was extracted become valid.(since C++17)

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | iterator to the position before which the new element will be inserted |
| value | - | element value to insert |
| first, last | - | range of elements to insert |
| ilist | - | initializer list to insert the values from |
| nh | - | a compatible node handle |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |

### Return value

1-6) An iterator to the inserted element.7,8) (none)9,10) End iterator if nh was empty, iterator pointing to the inserted element otherwise.

### Exceptions

1-6) If an exception is thrown by any operation, the insertion has no effect.7,8) No exception safety guarantee.9,10) If an exception is thrown by any operation, the insertion has no effect.

### Complexity

1-3) `O(log(size()))`4-6) Amortized constant if the insertion happens in the position just before pos, `O(log(size()))` otherwise.7,8) `O(N·log(size() + N))`, where `N` is the number of elements to insert.9) `O(log(size()))`10) Amortized constant if the insertion happens in the position just before pos, `O(log(size()))` otherwise.

### Example

Run this code

```
#include <functional>
#include <iostream>
#include <map>
#include <string>
#include <string_view>
#include <utility>
 
template<class M>
void print(const std::string_view rem, const M& mmap)
{
    std::cout << rem << ' ';
    for (const auto& e : mmap)
        std::cout << '{' << e.first << ',' << e.second << "} ";
    std::cout << '\n';
}
 
int main()
{
    // list-initialize
    std::multimap<int, std::string, std::greater<int>> mmap
        {{2, "foo"}, {2, "bar"}, {3, "baz"}, {1, "abc"}, {5, "def"}};
    print("#1", mmap);
 
    // insert using value_type
    mmap.insert(decltype(mmap)::value_type(5, "pqr"));
    print("#2", mmap);
 
    // insert using pair
    mmap.insert(std::pair{6, "uvw"});
    print("#3", mmap);
 
    mmap.insert({7, "xyz"});
    print("#4", mmap);
 
    // insert using initializer_list
    mmap.insert({{5, "one"}, {5, "two"}});
    print("#5", mmap);
 
    // insert using a pair of iterators
    mmap.clear();
    const auto il = {std::pair{1, "ä"}, {2, "ё"}, {2, "ö"}, {3, "ü"}};
    mmap.insert(il.begin(), il.end());
    print("#6", mmap);
}

```

Output:

```
#1 {5,def} {3,baz} {2,foo} {2,bar} {1,abc}
#2 {5,def} {5,pqr} {3,baz} {2,foo} {2,bar} {1,abc}
#3 {6,uvw} {5,def} {5,pqr} {3,baz} {2,foo} {2,bar} {1,abc}
#4 {7,xyz} {6,uvw} {5,def} {5,pqr} {3,baz} {2,foo} {2,bar} {1,abc}
#5 {7,xyz} {6,uvw} {5,def} {5,pqr} {5,one} {5,two} {3,baz} {2,foo} {2,bar} {1,abc}
#6 {3,ü} {2,ё} {2,ö} {1,ä}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 233 | C++98 | pos was just a hint, it could be totally ignored | the insertion is required to be as close as possible to the position just prior to pos |
| LWG 264 | C++98 | the complexity of overload (5) was required to be linear if the range ``first`,`last`)` is sorted according to `Compare` | removed the linear requirement in this special case |
| [LWG 371 | C++98 | the order of equivalent elements was not guaranteed to be preserved | required to be preserved |
| LWG 2005 | C++11 | overloads (3,6) were poorly described | improved the description |

### See also

|  |  |
| --- | --- |
| emplace(C++11) | constructs element in-place   (public member function) |
| emplace_hint(C++11) | constructs elements in-place using a hint   (public member function) |
| inserter | creates a std::insert_iterator of type inferred from the argument   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/multimap/insert&oldid=168637>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 January 2024, at 13:53.