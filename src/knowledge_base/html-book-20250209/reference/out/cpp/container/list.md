# std::list

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
| ****list**** | | | | |
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

****std::list****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | list::list | | | | | | list::~list | | | | | | list::operator= | | | | | | list::assign | | | | | | list::assign_range(C++23) | | | | | | list::get_allocator | | | | | | Element access | | | | | | list::front | | | | | | list::back | | | | | | Iterators | | | | | | list::beginlist::cbegin(C++11) | | | | | | list::endlist::cend(C++11) | | | | | | list::rbeginlist::crbegin(C++11) | | | | | | list::rendlist::crend(C++11) | | | | | | Capacity | | | | | | list::size | | | | | | list::empty | | | | | | list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | list::clear | | | | | | list::insert | | | | | | list::insert_range(C++23) | | | | | | list::emplace(C++11) | | | | | | list::erase | | | | | | list::push_front | | | | | | list::emplace_front(C++11) | | | | | | list::prepend_range(C++23) | | | | | | list::pop_front | | | | | | list::push_back | | | | | | list::emplace_back(C++11) | | | | | | list::append_range(C++23) | | | | | | list::pop_back | | | | | | list::resize | | | | | | list::swap | | | | | | Operations | | | | | | list::merge | | | | | | list::splice | | | | | | list::removelist::remove_if | | | | | | list::reverse | | | | | | list::unique | | | | | | list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::list) | | | | | | erase(std::list)erase_if(std::list)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<list>` |  |  |
| template<  class T,      class Allocator = std::allocator<T> > class list; | (1) |  |
| namespace pmr {  template< class T >      using list = std::list<T, std::pmr::polymorphic_allocator<T>>; } | (2) | (since C++17) |
|  |  |  |

`std::list` is a container that supports constant time insertion and removal of elements from anywhere in the container. Fast random access is not supported. It is usually implemented as a doubly-linked list. Compared to std::forward_list this container provides bidirectional iteration capability while being less space efficient.

Adding, removing and moving the elements within the list or across several lists does not invalidate the iterators or references. An iterator is invalidated only when the corresponding element is deleted.

`std::list` meets the requirements of Container, AllocatorAwareContainer, SequenceContainer and ReversibleContainer.

### Template parameters

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| T | - | The type of the elements.  |  |  | | --- | --- | | `T` must meet the requirements of CopyConstructible. `T` must meet the requirements of CopyAssignable if list::operator= or list::assign is instantiated with `T`. | (until C++11) | | The requirements that are imposed on the elements depend on the actual operations performed on the container. Generally, it is required that element type is a complete type and meets the requirements of Erasable, but many member functions impose stricter requirements. | (since C++11) (until C++17) | | The requirements that are imposed on the elements depend on the actual operations performed on the container. Generally, it is required that element type meets the requirements of Erasable, but many member functions impose stricter requirements. This container (but not its members) can be instantiated with an incomplete element type if the allocator satisfies the allocator completeness requirements.   | Feature-test macro | Value | Std | Feature | | --- | --- | --- | --- | | `__cpp_lib_incomplete_container_elements` | `201505L` | (C++17) | Minimal incomplete type support | | (since C++17) | |
| Allocator | - | An allocator that is used to acquire/release memory and to construct/destroy the elements in that memory. The type must meet the requirements of Allocator. The behavior is undefined(until C++20)The program is ill-formed(since C++20) if `Allocator::value_type` is not the same as `T`. |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `value_type` | `T` |
| `allocator_type` | `Allocator` |
| `size_type` | Unsigned integer type (usually std::size_t) |
| `difference_type` | Signed integer type (usually std::ptrdiff_t) |
| `reference` | value_type& |
| `const_reference` | const value_type& |
| `pointer` | |  |  | | --- | --- | | `Allocator::pointer` | (until C++11) | | std::allocator_traits<Allocator>::pointer | (since C++11) | |
| `const_pointer` | |  |  | | --- | --- | | `Allocator::const_pointer` | (until C++11) | | std::allocator_traits<Allocator>::const_pointer | (since C++11) | |
| `iterator` | LegacyBidirectionalIterator to `value_type` |
| `const_iterator` | LegacyBidirectionalIterator to const value_type |
| `reverse_iterator` | std::reverse_iterator<iterator> |
| `const_reverse_iterator` | std::reverse_iterator<const_iterator> |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the `list`   (public member function) |
| (destructor) | destructs the `list`   (public member function) |
| operator= | assigns values to the container   (public member function) |
| assign | assigns values to the container   (public member function) |
| assign_range(C++23) | assigns a range of values to the container   (public member function) |
| get_allocator | returns the associated allocator   (public member function) |
| Element access | |
| front | access the first element   (public member function) |
| back | access the last element   (public member function) |
| Iterators | |
| begincbegin(C++11) | returns an iterator to the beginning   (public member function) |
| endcend(C++11) | returns an iterator to the end   (public member function) |
| rbegincrbegin(C++11) | returns a reverse iterator to the beginning   (public member function) |
| rendcrend(C++11) | returns a reverse iterator to the end   (public member function) |
| Capacity | |
| empty | checks whether the container is empty   (public member function) |
| size | returns the number of elements   (public member function) |
| max_size | returns the maximum possible number of elements   (public member function) |
| Modifiers | |
| clear | clears the contents   (public member function) |
| insert | inserts elements   (public member function) |
| insert_range(C++23) | inserts a range of elements   (public member function) |
| emplace(C++11) | constructs element in-place   (public member function) |
| erase | erases elements   (public member function) |
| push_back | adds an element to the end   (public member function) |
| emplace_back(C++11) | constructs an element in-place at the end   (public member function) |
| append_range(C++23) | adds a range of elements to the end   (public member function) |
| pop_back | removes the last element   (public member function) |
| push_front | inserts an element to the beginning   (public member function) |
| emplace_front(C++11) | constructs an element in-place at the beginning   (public member function) |
| prepend_range(C++23) | adds a range of elements to the beginning   (public member function) |
| pop_front | removes the first element   (public member function) |
| resize | changes the number of elements stored   (public member function) |
| swap | swaps the contents   (public member function) |
| Operations | |
| merge | merges two sorted lists   (public member function) |
| splice | moves elements from another `list`   (public member function) |
| removeremove_if | removes elements satisfying specific criteria   (public member function) |
| reverse | reverses the order of the elements   (public member function) |
| unique | removes consecutive duplicate elements   (public member function) |
| sort | sorts the elements   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `list`s   (function template) |
| std::swap(std::list) | specializes the std::swap algorithm   (function template) |
| erase(std::list)erase_if(std::list)(C++20) | erases all elements satisfying specific criteria   (function template) |

|  |  |
| --- | --- |
| Deduction guides | (since C++17) |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges construction and insertion for containers |

### Example

Run this code

```
#include <algorithm>
#include <iostream>
#include <list>
 
int main()
{
    // Create a list containing integers
    std::list<int> l = {7, 5, 16, 8};
 
    // Add an integer to the front of the list
    l.push_front(25);
    // Add an integer to the back of the list
    l.push_back(13);
 
    // Insert an integer before 16 by searching
    auto it = std::find(l.begin(), l.end(), 16);
    if (it != l.end())
        l.insert(it, 42);
 
    // Print out the list
    std::cout << "l = { ";
    for (int n : l)
        std::cout << n << ", ";
    std::cout << "};\n";
}

```

Output:

```
l = { 25, 7, 5, 42, 16, 8, 13, };

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 230 | C++98 | `T` was not required to be CopyConstructible (an element of type `T` might not be able to be constructed) | `T` is also required to be CopyConstructible |
| LWG 276 | C++98 | `T` was always required to be CopyAssignable | only required if operator= or assign is instantiated with `T` |

### See also

|  |  |
| --- | --- |
| forward_list(C++11) | singly-linked list   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/list&oldid=174036>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 August 2024, at 20:56.