# std::flat_multimap<Key,T,Compare,KeyContainer,MappedContainer>::begin, std::flat_multimap<Key,T,Compare,KeyContainer,MappedContainer>::cbegin

From cppreference.com
< cpp‎ | container‎ | flat multimap
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

std::flat_multimap

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_multimap::flat_multimap | | | | | | flat_multimap::operator= | | | | | | Modifiers | | | | | | flat_multimap::clear | | | | | | flat_multimap::erase | | | | | | flat_multimap::swap | | | | | | flat_multimap::extract | | | | | | flat_multimap::replace | | | | | | flat_multimap::insert | | | | | | flat_multimap::insert_range | | | | | | flat_multimap::emplace | | | | | | flat_multimap::emplace_hint | | | | | | Lookup | | | | | | flat_multimap::count | | | | | | flat_multimap::find | | | | | | flat_multimap::contains | | | | | | flat_multimap::equal_range | | | | | | flat_multimap::lower_bound | | | | | | flat_multimap::upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | ****flat_multimap::beginflat_multimap::cbegin**** | | | | | | flat_multimap::endflat_multimap::cend | | | | | | flat_multimap::rbeginflat_multimap::crbegin | | | | | | flat_multimap::rendflat_multimap::crend | | | | | | Capacity | | | | | | flat_multimap::size | | | | | | flat_multimap::max_size | | | | | | flat_multimap::empty | | | | | | Observers | | | | | | flat_multimap::key_comp | | | | | | flat_multimap::keys | | | | | | flat_multimap::value_comp | | | | | | flat_multimap::values | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_multimap) | | | | | | erase_if(std::flat_multimap) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uses_allocator<std::flat_multimap> | | | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_equivalent_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| iterator begin() noexcept; | (1) | (since C++23) |
| const_iterator begin() const noexcept; | (2) | (since C++23) |
| const_iterator cbegin() const noexcept; | (3) | (since C++23) |
|  |  |  |

Returns an iterator to the first element of the `flat_multimap`.

If the `flat_multimap` is empty, the returned iterator will be equal to end().

!range-begin-end.svg

### Parameters

(none)

### Return value

Iterator to the first element.

### Complexity

Constant.

### Example

Run this code

```
#include <iostream>
#include <flat_map>
 
int main()
{
    std::flat_multimap<int, int> map{{4, 13}, {9, 94}, {1, 19}, {4, 42}};
 
    for (auto it = map.cbegin(); it != map.cend(); ++it)
        std::cout << '[' << it->first << "] = " << it->second << '\n';
 
    // Unlike std::multimap's bidirectional iterators, the std::flat_multimap
    // iterators are random-access, so they can be used with the operator[]:
    auto it = map.cbegin();
    assert(it[1] == 19);
    assert(it[4] == 13);
    assert(it[4] == 42);
    assert(it[9] == 94);
}

```

Output:

```
[1] = 19
[4] = 13
[4] = 42
[9] = 94

```

### See also

|  |  |
| --- | --- |
| endcend | returns an iterator to the end   (public member function) |
| begincbegin(C++11)(C++14) | returns an iterator to the beginning of a container or array   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_multimap/begin&oldid=168821>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 January 2024, at 11:15.