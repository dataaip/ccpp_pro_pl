# std::multimap<Key,T,Compare,Allocator>::insert_range

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | multimap::beginmultimap::cbegin(C++11) | | | | | | multimap::endmultimap::cend(C++11) | | | | | | multimap::rbeginmultimap::crbegin(C++11) | | | | | | multimap::rendmultimap::crend(C++11) | | | | | | Capacity | | | | | | multimap::size | | | | | | multimap::max_size | | | | | | multimap::empty | | | | | | Observers | | | | | | multimap::key_comp | | | | | | multimap::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | multimap::clear | | | | | | multimap::insert | | | | | | multimap::erase | | | | | | multimap::swap | | | | | | multimap::merge(C++17) | | | | | | ****multimap::insert_range****(C++23) | | | | | | multimap::emplace(C++11) | | | | | | multimap::emplace_hint(C++11) | | | | | | multimap::extract(C++17) | | | | | | Lookup | | | | | | multimap::count | | | | | | multimap::find | | | | | | multimap::contains(C++20) | | | | | | multimap::equal_range | | | | | | multimap::lower_bound | | | | | | multimap::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | std::swap(std::multimap) | | | | | | erase_if(std::multimap)(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| template< container-compatible-range<value_type> R >  void insert_range( R&& rg ); |  | (since C++23) |
|  |  |  |

Inserts a copy of each element in the range rg.

Each iterator in the range rg is dereferenced exactly once.
The behavior is undefined if rg overlaps with the container.

No iterators or references are invalidated.

### Parameters

|  |  |  |
| --- | --- | --- |
| rg | - | a container compatible range, that is, an `input_range` whose elements are convertible to `T` |
| Type requirements | | |
| -`value_type` must be EmplaceConstructible into `multimap` from \*ranges::begin(rg). Otherwise, the behavior is undefined. | | |

### Return value

(none)

### Complexity

N·log(a.size() + N), where `N` is ranges::distance(rg).

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges-aware construction and insertion |

### Example

Run this code

```
#include <iostream>
#include <map>
#include <utility>
 
void println(auto, auto const& container)
{
    for (const auto& [key, value] : container)
        std::cout << '{' << key << ',' << value << '}' << ' ';
    std::cout << '\n';
}
 
int main()
{
    auto container = std::multimap{std::pair{1, 11}, {3, 33}, {2, 22}, {4, 44}};
    const auto rg = {std::pair{-1, -11}, {3, -33}, {-2, -22}};
#ifdef __cpp_lib_containers_ranges
    container.insert_range(rg);
#else
    container.insert(rg.begin(), rg.end());
#endif
    println("{}", container);
}

```

Output:

```
{-2,-22} {-1,-11} {1,11} {2,22} {3,33} {3,-33} {4,44}

```

### See also

|  |  |
| --- | --- |
| insert | inserts elements or nodes(since C++17)   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/multimap/insert_range&oldid=156367>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 August 2023, at 01:45.