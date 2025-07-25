# std::forward_list<T,Allocator>::insert_after

From cppreference.com
< cpp‎ | container‎ | forward list
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

std::forward_list

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_list::forward_list | | | | | | forward_list::~forward_list | | | | | | forward_list::operator= | | | | | | forward_list::assign | | | | | | forward_list::assign_range(C++23) | | | | | | forward_list::get_allocator | | | | | | Element access | | | | | | forward_list::front | | | | | | Iterators | | | | | | forward_list::before_beginforward_list::cbefore_begin | | | | | | forward_list::beginforward_list::cbegin | | | | | | forward_list::endforward_list::cend | | | | | | Capacity | | | | | | forward_list::empty | | | | | | forward_list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | forward_list::clear | | | | | | forward_list::emplace_front | | | | | | forward_list::push_front | | | | | | ****forward_list::insert_after**** | | | | | | forward_list::emplace_after | | | | | | forward_list::erase_after | | | | | | forward_list::insert_range_after(C++23) | | | | | | forward_list::prepend_range(C++23) | | | | | | forward_list::pop_front | | | | | | forward_list::resize | | | | | | forward_list::swap | | | | | | Operations | | | | | | forward_list::merge | | | | | | forward_list::splice_after | | | | | | forward_list::removeforward_list::remove_if | | | | | | forward_list::reverse | | | | | | forward_list::unique | | | | | | forward_list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::forward_list) | | | | | | erase(std::forward_list)erase_if(std::forward_list)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| iterator insert_after( const_iterator pos, const T& value ); | (1) | (since C++11) |
| iterator insert_after( const_iterator pos, T&& value ); | (2) | (since C++11) |
| iterator insert_after( const_iterator pos, size_type count, const T& value ); | (3) | (since C++11) |
| template< class InputIt >  iterator insert_after( const_iterator pos, InputIt first, InputIt last ); | (4) | (since C++11) |
| iterator insert_after( const_iterator pos, std::initializer_list<T> ilist ); | (5) | (since C++11) |
|  |  |  |

Inserts elements after the specified position in the container.

1,2) Inserts value after the element pointed to by pos.3) Inserts count copies of the value after the element pointed to by pos.4) Inserts elements from range ``first`,`last`)` after the element pointed to by pos.
The behavior is undefined if first and last are iterators into \*this.5) Inserts elements from initializer list ilist.

No iterators or references are invalidated.

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | iterator after which the content will be inserted |
| value | - | element value to insert |
| count | - | number of copies to insert |
| first, last | - | the range of elements to insert |
| ilist | - | initializer list to insert the values from |
| Type requirements | | |
| -`InputIt` must meet the requirements of [LegacyInputIterator. | | |

### Return value

1,2) Iterator to the inserted element.3) Iterator to the last element inserted, or pos if count == 0.4) Iterator to the last element inserted, or pos if first == last.5) Iterator to the last element inserted, or pos if ilist is empty.

### Exceptions

If an exception is thrown for any reason, these functions have no effect (strong exception safety guarantee).

### Complexity

1,2) Constant.3) Linear in count.4) Linear in std::distance(first, last).5) Linear in ilist.size().

### Example

Run this code

```
#include <forward_list>
#include <iostream>
#include <string>
#include <vector>
 
void print(const std::forward_list<int>& list)
{
    std::cout << "list: {";
    for (char comma[3] = {'\0', ' ', '\0'}; int i : list)
    {
        std::cout << comma << i;
        comma[0] = ',';
    }
    std::cout << "}\n";
}
 
int main()
{
    std::forward_list<int> ints{1, 2, 3, 4, 5};
    print(ints);
 
    // insert_after (2)
    auto beginIt = ints.begin();
    ints.insert_after(beginIt, -6);
    print(ints);
 
    // insert_after (3)
    auto anotherIt = beginIt;
    ++anotherIt;
    anotherIt = ints.insert_after(anotherIt, 2, -7);
    print(ints);
 
    // insert_after (4)
    const std::vector<int> v = {-8, -9, -10};
    anotherIt = ints.insert_after(anotherIt, v.cbegin(), v.cend());
    print(ints);
 
    // insert_after (5)
    ints.insert_after(anotherIt, {-11, -12, -13, -14});
    print(ints);
}

```

Output:

```
list: {1, 2, 3, 4, 5}
list: {1, -6, 2, 3, 4, 5}
list: {1, -6, -7, -7, 2, 3, 4, 5}
list: {1, -6, -7, -7, -8, -9, -10, 2, 3, 4, 5}
list: {1, -6, -7, -7, -8, -9, -10, -11, -12, -13, -14, 2, 3, 4, 5}

```

### See also

|  |  |
| --- | --- |
| emplace_after | constructs elements in-place after an element   (public member function) |
| push_front | inserts an element to the beginning   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/forward_list/insert_after&oldid=157554>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 August 2023, at 01:22.