# std::deque

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
| ****deque**** | | | | |
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

****std::deque****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | deque::deque | | | | | | deque::~deque | | | | | | deque::operator= | | | | | | deque::assign | | | | | | deque::assign_range(C++23) | | | | | | deque::get_allocator | | | | | | Element access | | | | | | deque::at | | | | | | [deque::operator[]](deque/operator_at.html "cpp/container/deque/operator at") | | | | | | deque::front | | | | | | deque::back | | | | | | Iterators | | | | | | deque::begindeque::cbegin(C++11) | | | | | | deque::enddeque::cend(C++11) | | | | | | deque::rbegindeque::crbegin(C++11) | | | | | | deque::renddeque::crend(C++11) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | deque::empty | | | | | | deque::size | | | | | | deque::max_size | | | | | | deque::shrink_to_fit(DR\*) | | | | | | Modifiers | | | | | | deque::clear | | | | | | deque::insert | | | | | | deque::insert_range(C++23) | | | | | | deque::emplace | | | | | | deque::erase | | | | | | deque::push_front | | | | | | deque::emplace_front(C++11) | | | | | | deque::prepend_range(C++23) | | | | | | deque::pop_front | | | | | | deque::push_back | | | | | | deque::emplace_back(C++11) | | | | | | deque::append_range(C++23) | | | | | | deque::pop_back | | | | | | deque::resize | | | | | | deque::swap | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::deque) | | | | | | erase(std::deque)erase_if(std::deque)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<deque>` |  |  |
| template<  class T,      class Allocator = std::allocator<T> > class deque; | (1) |  |
| namespace pmr {  template< class T >      using deque = std::deque<T, std::pmr::polymorphic_allocator<T>>; } | (2) | (since C++17) |
|  |  |  |

`std::deque` (double-ended queue) is an indexed sequence container that allows fast insertion and deletion at both its beginning and its end. In addition, insertion and deletion at either end of a deque never invalidates pointers or references to the rest of the elements.

As opposed to std::vector, the elements of a deque are not stored contiguously: typical implementations use a sequence of individually allocated fixed-size arrays, with additional bookkeeping, which means indexed access to deque must perform two pointer dereferences, compared to vector's indexed access which performs only one.

The storage of a deque is automatically expanded and contracted as needed. Expansion of a deque is cheaper than the expansion of a std::vector because it does not involve copying of the existing elements to a new memory location. On the other hand, deques typically have large minimal memory cost; a deque holding just one element has to allocate its full internal array (e.g. 8 times the object size on 64-bit libstdc++; 16 times the object size or 4096 bytes, whichever is larger, on 64-bit libc++).

The complexity (efficiency) of common operations on deques is as follows:

- Random access - constant O(1).
- Insertion or removal of elements at the end or beginning - constant O(1).
- Insertion or removal of elements - linear O(n).

`std::deque` meets the requirements of Container, AllocatorAwareContainer, SequenceContainer and ReversibleContainer.

### Template parameters

|  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| T | - | The type of the elements.  |  |  | | --- | --- | | `T` must meet the requirements of CopyAssignable and CopyConstructible. | (until C++11) | | The requirements that are imposed on the elements depend on the actual operations performed on the container. Generally, it is required that element type is a complete type and meets the requirements of Erasable, but many member functions impose stricter requirements. | (since C++11) | |
| Allocator | - | An allocator that is used to acquire/release memory and to construct/destroy the elements in that memory. The type must meet the requirements of Allocator. The behavior is undefined(until C++20)The program is ill-formed(since C++20) if `Allocator::value_type` is not the same as `T`. |

### Iterator invalidation

|  |  |
| --- | --- |
|  | This section is incomplete Reason: There are still a few inaccuracies in this section, refer to individual member function pages for more detail |

| Operations | Invalidated |
| --- | --- |
| All read only operations. | Never. |
| swap, std::swap | The past-the-end iterator may be invalidated (implementation defined). |
| shrink_to_fit, clear, insert, emplace, push_front, push_back, emplace_front, emplace_back | Always. |
| erase | If erasing at begin - only erased elements.  If erasing at end - only erased elements and the past-the-end iterator.  Otherwise - all iterators are invalidated.   It is unspecified when the past-the-end iterator is invalidated.(until C++11)   The past-the-end iterator is also invalidated unless the erased  elements are at the beginning of the container and the last element is not erased.(since C++11) |
| resize | If the new size is smaller than the old one - only erased elements and the  past-the-end iterator.  If the new size is bigger than the old one - all iterators are invalidated.  Otherwise - none iterators are invalidated. |
| pop_front, pop_back | To the element erased.  The past-the-end iterator  may be invalidated (implementation defined)(until C++11)  is also invalidated.(since C++11) |

#### Invalidation notes

- When inserting at either end of the deque, references are not invalidated by insert and emplace.
- push_front, push_back, emplace_front and emplace_back do not invalidate any references to elements of the deque.
- When erasing at either end of the deque, references to non-erased elements are not invalidated by erase, pop_front and pop_back.
- A call to resize with a smaller size does not invalidate any references to non-erased elements.
- A call to resize with a bigger size does not invalidate any references to elements of the deque.

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
| `iterator` | LegacyRandomAccessIterator to `value_type` |
| `const_iterator` | LegacyRandomAccessIterator to const value_type |
| `reverse_iterator` | std::reverse_iterator<iterator> |
| `const_reverse_iterator` | std::reverse_iterator<const_iterator> |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the `deque`   (public member function) |
| (destructor) | destructs the `deque`   (public member function) |
| operator= | assigns values to the container   (public member function) |
| assign | assigns values to the container   (public member function) |
| assign_range(C++23) | assigns a range of values to the container   (public member function) |
| get_allocator | returns the associated allocator   (public member function) |
| Element access | |
| at | access specified element with bounds checking   (public member function) |
| [operator[]](deque/operator_at.html "cpp/container/deque/operator at") | access specified element   (public member function) |
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
| shrink_to_fit(DR\*) | reduces memory usage by freeing unused memory   (public member function) |
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

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `deque`s   (function template) |
| std::swap(std::deque) | specializes the std::swap algorithm   (function template) |
| erase(std::deque)erase_if(std::deque)(C++20) | erases all elements satisfying specific criteria   (function template) |

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
#include <deque>
#include <iostream>
 
int main()
{
    // Create a deque containing integers
    std::deque<int> d = {7, 5, 16, 8};
 
    // Add an integer to the beginning and end of the deque
    d.push_front(13);
    d.push_back(25);
 
    // Iterate and print values of deque
    for (int n : d)
        std::cout << n << ' ';
    std::cout << '\n';
}

```

Output:

```
13 7 5 16 8 25

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 230 | C++98 | `T` was not required to be CopyConstructible (an element of type `T` might not be able to be constructed) | `T` is also required to be CopyConstructible |

### See also

|  |  |
| --- | --- |
| queue | adapts a container to provide queue (FIFO data structure)   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/deque&oldid=162739>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 November 2023, at 22:51.