# std::unordered_multimap<Key,T,Hash,KeyEqual,Allocator>::merge

From cppreference.com
< cpp‎ | container‎ | unordered multimap
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

`std::unordered_multimap`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_multimap::unordered_multimap | | | | | | unordered_multimap::~unordered_multimap | | | | | | unordered_multimap::operator= | | | | | | unordered_multimap::get_allocator | | | | | | Iterators | | | | | | unordered_multimap::beginunordered_multimap::cbegin | | | | | | unordered_multimap::endunordered_multimap::cend | | | | | | Capacity | | | | | | unordered_multimap::size | | | | | | unordered_multimap::max_size | | | | | | unordered_multimap::empty | | | | | | Modifiers | | | | | | unordered_multimap::clear | | | | | | unordered_multimap::insert | | | | | | unordered_multimap::insert_range(C++23) | | | | | | unordered_multimap::emplace | | | | | | unordered_multimap::emplace_hint | | | | | | unordered_multimap::erase | | | | | | unordered_multimap::swap | | | | | | unordered_multimap::extract(C++17) | | | | | | ****unordered_multimap::merge****(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_multimap::count | | | | | | unordered_multimap::find | | | | | | unordered_multimap::contains(C++20) | | | | | | unordered_multimap::equal_range | | | | | | Bucket interface | | | | | | unordered_multimap::begin(size_type)unordered_multimap::cbegin(size_type) | | | | | | unordered_multimap::end(size_type)unordered_multimap::cend(size_type) | | | | | | unordered_multimap::bucket_count | | | | | | unordered_multimap::max_bucket_count | | | | | | unordered_multimap::bucket_size | | | | | | unordered_multimap::bucket | | | | | | Hash policy | | | | | | unordered_multimap::load_factor | | | | | | unordered_multimap::max_load_factor | | | | | | unordered_multimap::rehash | | | | | | unordered_multimap::reserve | | | | | | Observers | | | | | | unordered_multimap::hash_function | | | | | | unordered_multimap::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_multimap) | | | | | | erase_if(std::unordered_multimap)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| template< class H2, class P2 >  void merge( std::unordered_map<Key, T, H2, P2, Allocator>& source ); | (1) | (since C++17) |
| template< class H2, class P2 >  void merge( std::unordered_map<Key, T, H2, P2, Allocator>&& source ); | (2) | (since C++17) |
| template< class H2, class P2 >  void merge( std::unordered_multimap<Key, T, H2, P2, Allocator>& source ); | (3) | (since C++17) |
| template< class H2, class P2 >  void merge( std::unordered_multimap<Key, T, H2, P2, Allocator>&& source ); | (4) | (since C++17) |
|  |  |  |

Attempts to extract ("splice") each element in source and insert it into \*this using the hash function and key equality predicate of \*this.

No elements are copied or moved, only the internal pointers of the container nodes are repointed. All pointers and references to the transferred elements remain valid, but now refer into \*this, not into source. Iterators referring to the transferred elements and all iterators referring to \*this are invalidated.

The behavior is undefined if get_allocator() != source.get_allocator().

### Parameters

|  |  |  |
| --- | --- | --- |
| source | - | compatible container to transfer the nodes from |

### Return value

(none)

### Complexity

Average case O(N), worst case O(N \* size() + N), where N is source.size().

### Example

Run this code

```
#include <iostream>
#include <string>
#include <unordered_map>
#include <utility>
 
// print out a std::pair
template<class Os, class U, class V>
Os& operator<<(Os& os, const std::pair<U,V>& p)
{
    return os << '{' << p.first << ", " << p.second << '}';
}
 
// print out an associative container
template<class Os, class K, class V>
Os& operator<<(Os& os, const std::unordered_multimap<K, V>& v)
{
    os << '[' << v.size() << "] {";
    bool o{};
    for (const auto& e : v)
        os << (o ? ", " : (o = 1, "")) << e;
    return os << "}\n";
}
 
int main()
{
    std::unordered_multimap<std::string, int>
        p{{"C", 3}, {"B", 2}, {"A", 1}, {"A", 0}},
        q{{"E", 6}, {"E", 7}, {"D", 5}, {"A", 4}};
 
    std::cout << "p: " << p << "q: " << q;
 
    p.merge(q);
 
    std::cout << "p.merge(q);\n" << "p: " << p << "q: " << q;
}

```

Possible output:

```
p: [4] {{A, 1}, {A, 0}, {B, 2}, {C, 3}}
q: [4] {{A, 4}, {D, 5}, {E, 6}, {E, 7}}
p.merge(q);
p: [8] {{E, 6}, {E, 7}, {C, 3}, {A, 1}, {A, 0}, {A, 4}, {D, 5}, {B, 2}}
q: [0] {}

```

### See also

|  |  |
| --- | --- |
| extract(C++17) | extracts nodes from the container   (public member function) |
| insert | inserts elements or nodes(since C++17)   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_multimap/merge&oldid=162052>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 November 2023, at 09:56.