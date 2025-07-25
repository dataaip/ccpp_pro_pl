# std::flat_map<Key,T,Compare,KeyContainer,MappedContainer>::try_emplace

From cppreference.com
< cpp‎ | container‎ | flat map
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

std::flat_map

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_map::flat_map | | | | | | flat_map::operator= | | | | | | Element access | | | | | | flat_map::at | | | | | | [flat_map::operator[]](operator_at.html "cpp/container/flat map/operator at") | | | | | | Iterators | | | | | | flat_map::beginflat_map::cbegin | | | | | | flat_map::endflat_map::cend | | | | | | flat_map::rbeginflat_map::crbegin | | | | | | flat_map::rendflat_map::crend | | | | | | Lookup | | | | | | flat_map::count | | | | | | flat_map::find | | | | | | flat_map::contains | | | | | | flat_map::equal_range | | | | | | flat_map::lower_bound | | | | | | flat_map::upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | flat_map::size | | | | | | flat_map::max_size | | | | | | flat_map::empty | | | | | | Modifiers | | | | | | flat_map::clear | | | | | | flat_map::erase | | | | | | flat_map::swap | | | | | | flat_map::emplace | | | | | | flat_map::extract | | | | | | flat_map::replace | | | | | | flat_map::insert | | | | | | flat_map::insert_range | | | | | | flat_map::insert_or_assign | | | | | | flat_map::emplace_hint | | | | | | ****flat_map::try_emplace**** | | | | | | Observers | | | | | | flat_map::key_comp | | | | | | flat_map::keys | | | | | | flat_map::value_comp | | | | | | flat_map::values | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_map) | | | | | | erase_if(std::flat_map) | | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uses_allocator<std::flat_map> | | | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| template< class... Args >  std::pair<iterator, bool> try_emplace( const key_type& k, Args&&... args ); | (1) | (since C++23) |
| template< class... Args >  std::pair<iterator, bool> try_emplace( key_type&& k, Args&&... args ); | (2) | (since C++23) |
| template< class K, class... Args >  std::pair<iterator, bool> try_emplace( K&& k, Args&&... args ); | (3) | (since C++23) |
| template< class... Args >  iterator try_emplace( const_iterator hint, const key_type& k, Args&&... args ); | (4) | (since C++23) |
| template< class... Args >  iterator try_emplace( const_iterator hint, key_type&& k, Args&&... args ); | (5) | (since C++23) |
| template< class K, class... Args >  iterator try_emplace( const_iterator hint, K&& k, Args&&... args ); | (6) | (since C++23) |
|  |  |  |

If a key equivalent to k already exists in the container, does nothing. Otherwise, inserts a new element into the underlying containers `c` with key k and value constructed with args.

1,2,4,5) Equivalent to:

```
auto key_it = ranges::upper_bound(c.keys, k, compare);
auto value_it = c.values.begin() + std::distance(c.keys.begin(), key_it);
c.keys.insert(key_it, std::forward<decltype(k)>(k));
c.values.emplace(value_it, std::forward<Args>(args)...);

```

3,6) Equivalent to:

```
auto key_it = ranges::upper_bound(c.keys, k, compare);
auto value_it = c.values.begin() + std::distance(c.keys.begin(), key_it);
c.keys.emplace(key_it, std::forward<K>(k));
c.values.emplace(value_it, std::forward<Args>(args)...);

```

 The conversion from k into `key_type` must construct an object u, for which find(k) == find(u) is true. Otherwise, the behavior is undefined. These overloads participate in overload resolution only if :

- The qualified-id `Compare::is_transparent` is valid and denotes a type.
- std::is_constructible_v<key_type, K> is true.
- std::is_assignable_v<mapped_type&, Args...> is true.
- For (3) only, std::is_convertible_v<K&&, const_iterator> and std::is_convertible_v<K&&, iterator> are both false.

|  |  |
| --- | --- |
|  | Information on iterator invalidation is copied from here |

### Parameters

|  |  |  |
| --- | --- | --- |
| k | - | the key used both to look up and to insert if not found |
| hint | - | iterator to the position before which the new element will be inserted |
| args | - | arguments to forward to the constructor of the element |

### Return value

1-3) Same as for `emplace`.4-6) Same as for `emplace_hint`.

### Complexity

1-3) Same as for `emplace`.4-6) Same as for `emplace_hint`.

### Notes

Unlike `insert` or `emplace`, these functions do not move from rvalue arguments if the insertion does not happen, which makes it easy to manipulate maps whose values are move-only types, such as std::flat_map<std::string, std::unique_ptr<foo>>. In addition, `try_emplace` treats the key and the arguments to the `mapped_type` separately, unlike `emplace`, which requires the arguments to construct a `value_type` (that is, a std::pair).

Overloads (3,6) can be called without constructing an object of type `key_type`.

### Example

Run this code

```
#include <flat_map>
#include <iostream>
#include <string>
#include <utility>
 
void print_node(const auto& node)
{
    std::cout << '[' << node.first << "] = " << node.second << '\n';
}
 
void print_result(auto const& pair)
{
    std::cout << (pair.second ? "inserted: " : "ignored:  ");
    print_node(*pair.first);
}
 
int main()
{
    using namespace std::literals;
    std::map<std::string, std::string> m;
 
    print_result(m.try_emplace( "a", "a"s));
    print_result(m.try_emplace( "b", "abcd"));
    print_result(m.try_emplace( "c", 10, 'c'));
    print_result(m.try_emplace( "c", "Won't be inserted"));
 
    for (const auto& p : m)
        print_node(p);
}

```

Output:

```
inserted: [a] = a
inserted: [b] = abcd
inserted: [c] = cccccccccc
ignored:  [c] = cccccccccc
[a] = a
[b] = abcd
[c] = cccccccccc

```

### See also

|  |  |
| --- | --- |
| emplace | constructs element in-place   (public member function) |
| emplace_hint | constructs elements in-place using a hint   (public member function) |
| insert | inserts elements   (public member function) |
| insert_or_assign | inserts an element or assigns to the current element if the key already exists   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_map/try_emplace&oldid=171975>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 May 2024, at 22:29.