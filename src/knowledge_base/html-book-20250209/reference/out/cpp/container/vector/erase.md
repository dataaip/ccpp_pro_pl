# std::vector<T,Allocator>::erase

From cppreference.com
< cpp‎ | container‎ | vector
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

std::vector

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | vector::vector | | | | | | vector::~vector | | | | | | vector::operator= | | | | | | vector::assign | | | | | | vector::assign_range(C++23) | | | | | | vector::get_allocator | | | | | | Element access | | | | | | [vector::operator[]](operator_at.html "cpp/container/vector/operator at") | | | | | | vector::at | | | | | | vector::data | | | | | | vector::front | | | | | | vector::back | | | | | | Iterators | | | | | | vector::beginvector::cbegin(C++11) | | | | | | vector::endvector::cend(C++11) | | | | | | vector::rbeginvector::crbegin(C++11) | | | | | | vector::rendvector::crend(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | vector::empty | | | | | | vector::size | | | | | | vector::max_size | | | | | | vector::reserve | | | | | | vector::capacity | | | | | | vector::shrink_to_fit(DR\*) | | | | | | Modifiers | | | | | | vector::clear | | | | | | ****vector::erase**** | | | | | | vector::insert | | | | | | vector::insert_range(C++23) | | | | | | vector::append_range(C++23) | | | | | | vector::emplace(C++11) | | | | | | vector::emplace_back(C++11) | | | | | | vector::push_back | | | | | | vector::pop_back | | | | | | vector::resize | | | | | | vector::swap | | | | | |  | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::vector) | | | | | | erase(std::vector)erase_if(std::vector)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| iterator erase( iterator pos ); |  | (until C++11) |
| iterator erase( const_iterator pos ); |  | (since C++11)  (constexpr since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| iterator erase( iterator first, iterator last ); |  | (until C++11) |
| iterator erase( const_iterator first, const_iterator last ); |  | (since C++11)  (constexpr since C++20) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Erases the specified elements from the container.

1) Removes the element at pos.2) Removes the elements in the range ``first`,`last`)`.

Iterators (including the [`end()` iterator) and references to the elements at or after the point of the erase are invalidated.

The iterator pos must be valid and dereferenceable. Thus the end() iterator (which is valid, but is not dereferenceable) cannot be used as a value for pos.

The iterator first does not need to be dereferenceable if first == last: erasing an empty range is a no-op.

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | iterator to the element to remove |
| first, last | - | range of elements to remove |
| Type requirements | | |
| -`T` must meet the requirements of MoveAssignable. | | |

### Return value

Iterator following the last removed element.

1) If pos refers to the last element, then the end() iterator is returned.2) If last == end() prior to removal, then the updated end() iterator is returned. If ``first`,`last`)` is an empty range, then last is returned.

### Exceptions

Does not throw unless an exception is thrown by the assignment operator of `T`.

### Complexity

Linear: the number of calls to the destructor of `T` is the same as the number of elements erased, the assignment operator of `T` is called the number of times equal to the number of elements in the vector after the erased elements.

### Notes

When container elements need to be erased based on a predicate, rather than iterating the container and calling unary `erase`, the iterator range overload is generally used with [std::remove()/std::remove_if() to minimise the number of moves of the remaining (non-removed) elements, — this is the erase-remove idiom.
`std::erase_if()` replaces the erase-remove idiom.(since C++20)

### Example

Run this code

```
#include <vector>
#include <iostream>
 
 
void print_container(const std::vector<int>& c)
{
    for (int i : c)
        std::cout << i << ' ';
    std::cout << '\n';
}
 
int main()
{
    std::vector<int> c{0, 1, 2, 3, 4, 5, 6, 7, 8, 9};
    print_container(c);
 
    c.erase(c.begin());
    print_container(c);
 
    c.erase(c.begin() + 2, c.begin() + 5);
    print_container(c);
 
    // Erase all even numbers
    for (std::vector<int>::iterator it = c.begin(); it != c.end();)
    {
        if (*it % 2 == 0)
            it = c.erase(it);
        else
            ++it;
    }
    print_container(c);
}

```

Output:

```
0 1 2 3 4 5 6 7 8 9
1 2 3 4 5 6 7 8 9
1 2 6 7 8 9
1 7 9

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 151 | C++98 | first was required to be dereferenceable, which made the behavior of clearing an empty `vector` undefined | not required if first == last |
| LWG 414 | C++98 | iterators at the point of erase were not invalidated | they are also invalidated |

### See also

|  |  |
| --- | --- |
| erase(std::vector)erase_if(std::vector)(C++20) | erases all elements satisfying specific criteria   (function template) |
| clear | clears the contents   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/vector/erase&oldid=119433>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 June 2020, at 12:42.