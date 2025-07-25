# std::unordered_set

From cppreference.com
< cpp‎ | container
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
| ****unordered_set****(C++11) | | | | |
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

`std::unordered_set`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_set::unordered_set | | | | | | unordered_set::~unordered_set | | | | | | unordered_set::operator= | | | | | | unordered_set::get_allocator | | | | | | Iterators | | | | | | unordered_set::beginunordered_set::cbegin | | | | | | unordered_set::endunordered_set::cend | | | | | | Capacity | | | | | | unordered_set::size | | | | | | unordered_set::max_size | | | | | | unordered_set::empty | | | | | | Modifiers | | | | | | unordered_set::clear | | | | | | unordered_set::erase | | | | | | unordered_set::swap | | | | | | unordered_set::extract(C++17) | | | | | | unordered_set::merge(C++17) | | | | | | unordered_set::insert | | | | | | unordered_set::insert_range(C++23) | | | | | | unordered_set::emplace | | | | | | unordered_set::emplace_hint | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_set::count | | | | | | unordered_set::find | | | | | | unordered_set::contains(C++20) | | | | | | unordered_set::equal_range | | | | | | Bucket interface | | | | | | unordered_set::begin(size_type)unordered_set::cbegin(size_type) | | | | | | unordered_set::end(size_type)unordered_set::cend(size_type) | | | | | | unordered_set::bucket_count | | | | | | unordered_set::max_bucket_count | | | | | | unordered_set::bucket_size | | | | | | unordered_set::bucket | | | | | | Hash policy | | | | | | unordered_set::load_factor | | | | | | unordered_set::max_load_factor | | | | | | unordered_set::rehash | | | | | | unordered_set::reserve | | | | | | Observers | | | | | | unordered_set::hash_function | | | | | | unordered_set::key_eq | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_set) | | | | | | erase_if(std::unordered_set)(C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<unordered_set>` |  |  |
| template<  class Key,      class Hash = std::hash<Key>,      class KeyEqual = std::equal_to<Key>,      class Allocator = std::allocator<Key> > class unordered_set; | (1) | (since C++11) |
| namespace pmr {  template<          class Key,          class Hash = std::hash<Key>,          class Pred = std::equal_to<Key>      > using unordered_set = std::unordered_set<Key, Hash, Pred,                                  std::pmr::polymorphic_allocator<Key>>; } | (2) | (since C++17) |
|  |  |  |

`std::unordered_set` is an associative container that contains a set of unique objects of type `Key`. Search, insertion, and removal have average constant-time complexity.

Internally, the elements are not sorted in any particular order, but organized into buckets. Which bucket an element is placed into depends entirely on the hash of its value. This allows fast access to individual elements, since once a hash is computed, it refers to the exact bucket the element is placed into.

Container elements may not be modified (even by non const iterators) since modification could change an element's hash and corrupt the container.

`std::unordered_set` meets the requirements of Container, AllocatorAwareContainer, UnorderedAssociativeContainer.

### Iterator invalidation

| Operations | Invalidated |
| --- | --- |
| All read only operations, swap, std::swap | Never |
| clear, rehash, reserve, operator= | Always |
| insert, emplace, emplace_hint | Only if causes rehash |
| erase | Only to the element erased |

#### Notes

- The swap functions do not invalidate any of the iterators inside the container, but they do invalidate the iterator marking the end of the swap region.

- References and pointers to data stored in the container are only invalidated by erasing that element, even when the corresponding iterator is invalidated.

- After container move assignment, unless elementwise move assignment is forced by incompatible allocators, references, pointers, and iterators (other than the past-the-end iterator) to moved-from container remain valid, but refer to elements that are now in \*this.

### Template parameters

|  |  |
| --- | --- |
|  | This section is incomplete Reason: Add descriptions of the template parameters. |

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `key_type` | `Key` |
| `value_type` | `Key` |
| `size_type` | Unsigned integer type (usually std::size_t) |
| `difference_type` | Signed integer type (usually std::ptrdiff_t) |
| `hasher` | `Hash` |
| `key_equal` | `KeyEqual` |
| `allocator_type` | `Allocator` |
| `reference` | value_type& |
| `const_reference` | const value_type& |
| `pointer` | std::allocator_traits<Allocator>::pointer |
| `const_pointer` | std::allocator_traits<Allocator>::const_pointer |
| `iterator` | Constant LegacyForwardIterator to `value_type` |
| `const_iterator` | LegacyForwardIterator to const value_type |
| `local_iterator` | An iterator type whose category, value, difference, pointer and reference types are the same as `iterator`. This iterator can be used to iterate through a single bucket but not across buckets |
| `const_local_iterator` | An iterator type whose category, value, difference, pointer and reference types are the same as `const_iterator`. This iterator can be used to iterate through a single bucket but not across buckets |
| `node_type` (since C++17) | a specialization of node handle representing a container node |
| `insert_return_type` (since C++17) | type describing the result of inserting a `node_type`, a specialization of  template<class Iter, class NodeType>  struct /\*unspecified\*/  {      Iter     position;      bool     inserted;      NodeType node;  };  instantiated with template arguments `iterator` and `node_type`. |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the `unordered_set`   (public member function) |
| (destructor) | destructs the `unordered_set`   (public member function) |
| operator= | assigns values to the container   (public member function) |
| get_allocator | returns the associated allocator   (public member function) |
| Iterators | |
| begincbegin | returns an iterator to the beginning   (public member function) |
| endcend | returns an iterator to the end   (public member function) |
| Capacity | |
| empty | checks whether the container is empty   (public member function) |
| size | returns the number of elements   (public member function) |
| max_size | returns the maximum possible number of elements   (public member function) |
| Modifiers | |
| clear | clears the contents   (public member function) |
| insert | inserts elements or nodes(since C++17)   (public member function) |
| insert_range(C++23) | inserts a range of elements   (public member function) |
| emplace | constructs element in-place   (public member function) |
| emplace_hint | constructs elements in-place using a hint   (public member function) |
| erase | erases elements   (public member function) |
| swap | swaps the contents   (public member function) |
| extract(C++17) | extracts nodes from the container   (public member function) |
| merge(C++17) | splices nodes from another container   (public member function) |
| Lookup | |
| count | returns the number of elements matching specific key   (public member function) |
| find | finds element with specific key   (public member function) |
| contains(C++20) | checks if the container contains element with specific key   (public member function) |
| equal_range | returns range of elements matching a specific key   (public member function) |
| Bucket interface | |
| begin(size_type)cbegin(size_type) | returns an iterator to the beginning of the specified bucket   (public member function) |
| end(size_type)cend(size_type) | returns an iterator to the end of the specified bucket   (public member function) |
| bucket_count | returns the number of buckets   (public member function) |
| max_bucket_count | returns the maximum number of buckets   (public member function) |
| bucket_size | returns the number of elements in specific bucket   (public member function) |
| bucket | returns the bucket for specific key   (public member function) |
| Hash policy | |
| load_factor | returns average number of elements per bucket   (public member function) |
| max_load_factor | manages maximum average number of elements per bucket   (public member function) |
| rehash | reserves at least the specified number of buckets and regenerates the hash table   (public member function) |
| reserve | reserves space for at least the specified number of elements and regenerates the hash table   (public member function) |
| Observers | |
| hash_function | returns function used to hash the keys   (public member function) |
| key_eq | returns the function used to compare keys for equality   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=(C++11)(C++11)(removed in C++20) | compares the values in the unordered_set   (function template) |
| std::swap(std::unordered_set)(C++11) | specializes the std::swap algorithm   (function template) |
| erase_if(std::unordered_set)(C++20) | erases all elements satisfying specific criteria   (function template) |

|  |  |
| --- | --- |
| Deduction guides | (since C++17) |

### Notes

The member types `iterator` and `const_iterator` may be aliases to the same type. This means defining a pair of function overloads using the two types as parameter types may violate the One Definition Rule. Since `iterator` is convertible to `const_iterator`, a single function with a `const_iterator` as parameter type will work instead.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges construction and insertion for containers |

### Example

Run this code

```
#include <iostream>
#include <unordered_set>
 
void print(const auto& set)
{
    for (const auto& elem : set)
        std::cout << elem << ' ';
    std::cout << '\n';
}
 
int main()
{
    std::unordered_set<int> mySet{2, 7, 1, 8, 2, 8}; // creates a set of ints
    print(mySet);
 
    mySet.insert(5); // puts an element 5 in the set
    print(mySet);
 
    if (auto iter = mySet.find(5); iter != mySet.end())
        mySet.erase(iter); // removes an element pointed to by iter
    print(mySet);
 
    mySet.erase(7); // removes an element 7
    print(mySet);
}

```

Possible output:

```
8 1 7 2
5 8 1 7 2
8 1 7 2
8 1 2

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2050 | C++11 | the definitions of `reference`, `const_reference`, `pointer` and `const_pointer` were based on `allocator_type` | based on `value_type` and std::allocator_traits |

### See also

|  |  |
| --- | --- |
| unordered_multiset(C++11) | collection of keys, hashed by keys   (class template) |
| set | collection of unique keys, sorted by keys   (class template) |
| flat_set(C++23) | adapts a container to provide a collection of unique keys, sorted by keys   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_set&oldid=177449>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 November 2024, at 15:44.