# std::flat_set

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
| unordered_set(C++11) | | | | |
| unordered_multiset(C++11) | | | | |
| unordered_map(C++11) | | | | |
| unordered_multimap(C++11) | | | | |
| Adaptors | | | | |
| stack | | | | |
| queue | | | | |
| priority_queue | | | | |
| ****flat_set****(C++23) | | | | |
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

****std::flat_set****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_set::flat_set | | | | | | flat_set::operator= | | | | | | Iterators | | | | | | flat_set::beginflat_set::cbegin | | | | | | flat_set::endflat_set::cend | | | | | | flat_set::rbeginflat_set::crbegin | | | | | | flat_set::rendflat_set::crend | | | | | | Capacity | | | | | | flat_set::size | | | | | | flat_set::max_size | | | | | | flat_set::empty | | | | | | Observers | | | | | | flat_set::key_comp | | | | | | flat_set::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | flat_set::clear | | | | | | flat_set::insert | | | | | | flat_set::insert_range | | | | | | flat_set::emplace | | | | | | flat_set::emplace_hint | | | | | | flat_set::erase | | | | | | flat_set::swap | | | | | | flat_set::extract | | | | | | flat_set::replace | | | | | | Lookup | | | | | | flat_set::count | | | | | | flat_set::find | | | | | | flat_set::contains | | | | | | flat_set::equal_range | | | | | | flat_set::lower_bound | | | | | | flat_set::upper_bound | | | | | | | Non-member functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_set) | | | | | | erase_if(std::flat_set) | | | | | | |
| Helper classes | | | | |
| uses_allocator<std::flat_set> | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<flat_set>` |  |  |
| template<  class Key,      class Compare = std::less<Key>,      class KeyContainer = std::vector<Key> > class flat_set; |  | (since C++23) |
|  |  |  |

The flat set is a container adaptor that gives the functionality of an associative container that stores a sorted set of unique objects of type `Key`. Sorting is done using the key comparison function `Compare`.

The class template `flat_set` acts as a wrapper to the underlying sorted container passed as object of type `KeyContainer`.

Everywhere the standard library uses the Compare requirements, uniqueness is determined by using the equivalence relation. Informally, two objects a and b are considered equivalent if neither compares less than the other: !comp(a, b) && !comp(b, a).

`std::flat_set` meets the requirements of Container, ReversibleContainer, optional container requirements, and all requirements of AssociativeContainer (including logarithmic search complexity), except that:

- requirements related to nodes are not applicable,
- iterator invalidation requirements differ,
- the complexity of insertion and erasure operations is linear.

A flat set supports most AssociativeContainer's operations that use unique keys.

### Iterator invalidation

|  |  |
| --- | --- |
|  | This section is incomplete |

### Template parameters

|  |  |  |
| --- | --- | --- |
| Key | - | The type of the stored elements. The program is ill-formed if `Key` is not the same type as `KeyContainer::value_type`. |
| Compare | - | A Compare type providing a strict weak ordering. |
| KeyContainer | - | The type of the underlying SequenceContainer to store the elements. The iterators of such container should satisfy LegacyRandomAccessIterator or model `random_access_iterator`. The standard containers std::vector and std::deque satisfy these requirements. |

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `container_type` | `Key``Container` |
| `key_type` | `Key` |
| `value_type` | `Key` |
| `key_compare` | `Compare` |
| `value_compare` | `Compare` |
| `reference` | value_type& |
| `const_reference` | const value_type& |
| `size_type` | typename KeyContainer::size_type |
| `difference_type` | typename KeyContainer::difference_type |
| `iterator` | implementation-defined LegacyRandomAccessIterator and `random_access_iterator` to `value_type` |
| `const_iterator` | implementation-defined LegacyRandomAccessIterator and `random_access_iterator` to const value_type |
| `reverse_iterator` | std::reverse_iterator<iterator> |
| `const_reverse_iterator` | std::reverse_iterator<const_iterator> |

### Member objects

|  |  |
| --- | --- |
| Member | Description |
| `container_type` `c` (private) | the adapted container (exposition-only member object\*) |
| `key_compare` `compare` (private) | the comparison function object (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the `flat_set`   (public member function) |
| (destructor)(implicitly declared) | destroys every element of the container adaptor   (public member function) |
| operator= | assigns values to the container adaptor   (public member function) |
| Iterators | |
| begincbegin | returns an iterator to the beginning   (public member function) |
| endcend | returns an iterator to the end   (public member function) |
| rbegincrbegin | returns a reverse iterator to the beginning   (public member function) |
| rendcrend | returns a reverse iterator to the end   (public member function) |
| Capacity | |
| empty | checks whether the container adaptor is empty   (public member function) |
| size | returns the number of elements   (public member function) |
| max_size | returns the maximum possible number of elements   (public member function) |
| Modifiers | |
| emplace | constructs element in-place   (public member function) |
| emplace_hint | constructs elements in-place using a hint   (public member function) |
| insert | inserts elements   (public member function) |
| insert_range | inserts a range of elements   (public member function) |
| extract | extracts the underlying container   (public member function) |
| replace | replaces the underlying container   (public member function) |
| erase | erases elements   (public member function) |
| swap | swaps the contents   (public member function) |
| clear | clears the contents   (public member function) |
| Lookup | |
| find | finds element with specific key   (public member function) |
| count | returns the number of elements matching specific key   (public member function) |
| contains | checks if the container contains element with specific key   (public member function) |
| lower_bound | returns an iterator to the first element **not less** than the given key   (public member function) |
| upper_bound | returns an iterator to the first element **greater** than the given key   (public member function) |
| equal_range | returns range of elements matching a specific key   (public member function) |
| Observers | |
| key_comp | returns the function that compares keys   (public member function) |
| value_comp | returns the function that compares keys in objects of type `value_type`   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator<=>(C++23) | lexicographically compares the values of two `flat_set`s   (function template) |
| std::swap(std::flat_set)(C++23) | specializes the std::swap algorithm   (function template) |
| erase_if(std::flat_set)(C++23) | erases all elements satisfying specific criteria   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::uses_allocator<std::flat_set>(C++23) | specializes the std::uses_allocator type trait   (class template specialization) |

### Tags

|  |  |
| --- | --- |
| sorted_uniquesorted_unique_t(C++23) | indicates that elements of a range are sorted and unique (tag) |

### Deduction guides

### Notes

The member types `iterator` and `const_iterator` may be aliases to the same type. This means defining a pair of function overloads using the two types as parameter types may violate the One Definition Rule. Since `iterator` is convertible to `const_iterator`, a single function with a `const_iterator` as parameter type will work instead.

Some advantages of flat set over other standard container adaptors are:

- Potentially faster lookup (even though search operations have logarithmic complexity).
- Much faster iteration: random access iterators instead of bidirectional iterators.
- Less memory consumption for small objects (and for big objects if KeyContainer::shrink_to_fit() is available).
- Better cache performance (depending on `KeyContainer`, keys are stored in a contiguous block(s) of memory).

Some disadvantages of flat set are:

- Non-stable iterators (iterators are invalidated when inserting and erasing elements).
- Non-copyable and non-movable type values can not be stored.
- Weaker exception safety (copy/move constructors can throw when shifting values in erasures and insertions).
- Slower (i.e. linear) insertion and erasure, especially for non-movable types.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_flat_set` | `202207L` | (C++23) | `std::flat_set` and std::flat_multiset |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| flat_multiset(C++23) | adapts a container to provide a collection of keys, sorted by keys   (class template) |
| set | collection of unique keys, sorted by keys   (class template) |
| unordered_set(C++11) | collection of unique keys, hashed by keys   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_set&oldid=177443>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 November 2024, at 14:53.