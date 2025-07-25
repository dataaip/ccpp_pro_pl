# std::unordered_map<Key,T,Hash,KeyEqual,Allocator>::try_emplace

From cppreference.com
< cpp‎ | container‎ | unordered map
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

std::unordered_map

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_map::unordered_map | | | | | | unordered_map::~unordered_map | | | | | | unordered_map::operator= | | | | | | unordered_map::get_allocator | | | | | | Iterators | | | | | | unordered_map::beginunordered_map::cbegin | | | | | | unordered_map::endunordered_map::cend | | | | | | Capacity | | | | | | unordered_map::size | | | | | | unordered_map::max_size | | | | | | unordered_map::empty | | | | | | Modifiers | | | | | | unordered_map::clear | | | | | | unordered_map::erase | | | | | | unordered_map::swap | | | | | | unordered_map::extract(C++17) | | | | | | unordered_map::merge(C++17) | | | | | | unordered_map::insert | | | | | | unordered_map::insert_range(C++23) | | | | | | unordered_map::insert_or_assign(C++17) | | | | | | unordered_map::emplace | | | | | | unordered_map::emplace_hint | | | | | | ****unordered_map::try_emplace****(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_map::at | | | | | | [unordered_map::operator[]](operator_at.html "cpp/container/unordered map/operator at") | | | | | | unordered_map::count | | | | | | unordered_map::find | | | | | | unordered_map::contains(C++20) | | | | | | unordered_map::equal_range | | | | | | Bucket interface | | | | | | unordered_map::begin(size_type)unordered_map::cbegin(size_type) | | | | | | unordered_map::end(size_type)unordered_map::cend(size_type) | | | | | | unordered_map::bucket_count | | | | | | unordered_map::max_bucket_count | | | | | | unordered_map::bucket_size | | | | | | unordered_map::bucket | | | | | | Hash policy | | | | | | unordered_map::load_factor | | | | | | unordered_map::max_load_factor | | | | | | unordered_map::rehash | | | | | | unordered_map::reserve | | | | | | Observers | | | | | | unordered_map::hash_function | | | | | | unordered_map::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_map) | | | | | | erase_if(std::unordered_map)(C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| template< class... Args >  std::pair<iterator, bool> try_emplace( const Key& k, Args&&... args ); | (1) | (since C++17) |
| template< class... Args >  std::pair<iterator, bool> try_emplace( Key&& k, Args&&... args ); | (2) | (since C++17) |
| template< class K, class... Args >  std::pair<iterator, bool> try_emplace( K&& k, Args&&... args ); | (3) | (since C++26) |
| template< class... Args >  iterator try_emplace( const_iterator hint, const Key& k, Args&&... args ); | (4) | (since C++17) |
| template< class... Args >  iterator try_emplace( const_iterator hint, Key&& k, Args&&... args ); | (5) | (since C++17) |
| template< class K, class... Args >  iterator try_emplace( const_iterator hint, K&& k, Args&&... args ); | (6) | (since C++26) |
|  |  |  |

If a key equivalent to k already exists in the container, does nothing. Otherwise, inserts a new element into the container with key k and value constructed with args. In such case:

1) Behaves like `emplace` except that the element is constructed as  
value_type(std::piecewise_construct,  

std::forward_as_tuple(k),

std::forward_as_tuple(std::forward<Args>(args)...))2) Behaves like `emplace` except that the element is constructed as  
value_type(std::piecewise_construct,  

std::forward_as_tuple(std::move(k)),

std::forward_as_tuple(std::forward<Args>(args)...))3) Behaves like `emplace` except that the element is constructed as  
value_type(std::piecewise_construct,  

std::forward_as_tuple(std::forward<K>(k)),

std::forward_as_tuple(std::forward<Args>(args)...))4) Behaves like `emplace_hint` except that the element is constructed as  
value_type(std::piecewise_construct,  

std::forward_as_tuple(k),

std::forward_as_tuple(std::forward<Args>(args)...))5) Behaves like `emplace_hint` except that the element is constructed as  
value_type(std::piecewise_construct,  

std::forward_as_tuple(std::move(k)),

std::forward_as_tuple(std::forward<Args>(args)...))6) Behaves like `emplace_hint` except that the element is constructed as  
value_type(std::piecewise_construct,  

std::forward_as_tuple(std::forward<K>(k)),

std::forward_as_tuple(std::forward<Args>(args)...))1-6) If `value_type` is not EmplaceConstructible into `unordered_map` from the corresponding expression, the behavior is undefined.3) This overload participates in overload resolution only if all following conditions are satisfied:

- std::is_convertible_v<K&&, const_iterator> and std::is_convertible_v<K&&, iterator> are both false.
- Hash::is_transparent and KeyEqual::is_transparent are valid and each denotes a type.
 If hash_function()(u.first) != hash_function()(k) || contains(u.first) is true, the behavior is undefined, where u is the new element to be inserted.6) This overload participates in overload resolution only if Hash::is_transparent and KeyEqual::is_transparent are both valid and each denotes a type. If hash_function()(u.first) != hash_function()(k) || contains(u.first) is true, the behavior is undefined, where u is the new element to be inserted.

If after the operation the new number of elements is greater than old `max_load_factor()` `*``bucket_count()` a rehashing takes place.  
If rehashing occurs (due to the insertion), all iterators are invalidated. Otherwise (no rehashing), iterators are not invalidated.

### Parameters

|  |  |  |
| --- | --- | --- |
| k | - | the key used both to look up and to insert if not found |
| hint | - | iterator to the position before which the new element will be inserted |
| args | - | arguments to forward to the constructor of the element |

### Return value

1-3) Same as for `emplace`:  
A pair consisting of an iterator to the inserted element (or to the element that prevented the insertion) and a bool value set to true if and only if the insertion took place.4-6) Same as for `emplace_hint`:  
An iterator to the inserted element, or to the element that prevented the insertion.

### Complexity

1-3) Same as for `emplace`:  
Amortized constant on average, worst case linear in the size of the container.4-6) Same as for `emplace_hint`:  
Amortized constant on average, worst case linear in the size of the container.

### Notes

Unlike `insert` or `emplace`, these functions do not move from rvalue arguments if the insertion does not happen, which makes it easy to manipulate maps whose values are move-only types, such as std::unordered_map<std::string, std::unique_ptr<foo>>. In addition, `try_emplace` treats the key and the arguments to the `mapped_type` separately, unlike `emplace`, which requires the arguments to construct a `value_type` (that is, a std::pair).

Overloads (3,6) can be called without constructing an object of type `Key`.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_unordered_map_try_emplace` | `201411L` | (C++17) | `std::unordered_map::try_emplace`, std::unordered_map::insert_or_assign |
| `__cpp_lib_associative_heterogeneous_insertion` | `202311L` | (C++26) | Heterogeneous overloads for the remaining member functions in ordered and unordered associative containers. Overloads (3) and (6). |

### Example

Run this code

```
#include <iostream>
#include <string>
#include <unordered_map>
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
    std::unordered_map<std::string, std::string> m;
 
    print_result(m.try_emplace("a", "a"s));
    print_result(m.try_emplace("b", "abcd"));
    print_result(m.try_emplace("c", 10, 'c'));
    print_result(m.try_emplace("c", "Won't be inserted"));
 
    for (const auto& p : m)
        print_node(p);
}

```

Possible output:

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
| insert | inserts elements or nodes(since C++17)   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_map/try_emplace&oldid=135904>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 November 2021, at 13:10.