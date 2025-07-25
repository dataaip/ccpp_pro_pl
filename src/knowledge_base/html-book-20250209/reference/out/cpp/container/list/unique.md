# std::list<T,Allocator>::unique

From cppreference.com
< cpp‎ | container‎ | list
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

std::list

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | list::list | | | | | | list::~list | | | | | | list::operator= | | | | | | list::assign | | | | | | list::assign_range(C++23) | | | | | | list::get_allocator | | | | | | Element access | | | | | | list::front | | | | | | list::back | | | | | | Iterators | | | | | | list::beginlist::cbegin(C++11) | | | | | | list::endlist::cend(C++11) | | | | | | list::rbeginlist::crbegin(C++11) | | | | | | list::rendlist::crend(C++11) | | | | | | Capacity | | | | | | list::size | | | | | | list::empty | | | | | | list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | list::clear | | | | | | list::insert | | | | | | list::insert_range(C++23) | | | | | | list::emplace(C++11) | | | | | | list::erase | | | | | | list::push_front | | | | | | list::emplace_front(C++11) | | | | | | list::prepend_range(C++23) | | | | | | list::pop_front | | | | | | list::push_back | | | | | | list::emplace_back(C++11) | | | | | | list::append_range(C++23) | | | | | | list::pop_back | | | | | | list::resize | | | | | | list::swap | | | | | | Operations | | | | | | list::merge | | | | | | list::splice | | | | | | list::removelist::remove_if | | | | | | list::reverse | | | | | | ****list::unique**** | | | | | | list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::list) | | | | | | erase(std::list)erase_if(std::list)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| void unique(); |  | (until C++20) |
| size_type unique(); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| template< class BinaryPredicate >  void unique( BinaryPredicate p ); |  | (until C++20) |
| template< class BinaryPredicate >  size_type unique( BinaryPredicate p ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Removes all **consecutive** duplicate elements from the container. Only the first element in each group of equal elements is left. Invalidates only the iterators and references to the
removed elements.

1) Uses operator== to compare the elements.2) Uses p to compare the elements.

The behavior is undefined if the corresponding comparator does not establish an equivalence relation.

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | binary predicate which returns ​true if the elements should be treated as equal.   The signature of the predicate function should be equivalent to the following:   bool pred(const Type1 &a, const Type2 &b);  While the signature does not need to have const &, the function must not modify the objects passed to it and must be able to accept all values of type (possibly const) `Type1` and `Type2` regardless of value category (thus, Type1 & is not allowed, nor is Type1 unless for `Type1` a move is equivalent to a copy(since C++11)).  The types Type1 and Type2 must be such that an object of type list<T,Allocator>::const_iterator can be dereferenced and then implicitly converted to both of them. ​ |
| Type requirements | | |
| -`BinaryPredicate` must meet the requirements of BinaryPredicate. | | |

### Return value

|  |  |
| --- | --- |
| (none) | (until C++20) |
| The number of elements removed. | (since C++20) |

### Complexity

If empty() is true, no comparison is performed.

Otherwise, given \(\scriptsize N\)N as std::distance(begin(), end()):

1) Exactly \(\scriptsize N-1\)N-1 comparisons using operator==.2) Exactly \(\scriptsize N-1\)N-1 applications of the predicate p.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_list_remove_return_type` | `201806L` | (C++20) | Change the return type |

### Example

Run this code

```
#include <iostream>
#include <list>
 
std::ostream& operator<< (std::ostream& os, std::list<int> const& container)
{
    for (int val : container)
        os << val << ' ';
    return os << '\n';
}
 
int main()
{
    std::list<int> c{1, 2, 2, 3, 3, 2, 1, 1, 2};
    std::cout << "Before unique(): " << c;
    const auto count1 = c.unique();
    std::cout << "After unique():  " << c
              << count1 << " elements were removed\n";
 
    c = {1, 2, 12, 23, 3, 2, 51, 1, 2, 2};
    std::cout << "\nBefore unique(pred): " << c;
 
    const auto count2 = c.unique(mod = 10
    {
        return (x % mod) == (y % mod);
    });
 
    std::cout << "After unique(pred):  " << c
              << count2 << " elements were removed\n";
}

```

Output:

```
Before unique(): 1 2 2 3 3 2 1 1 2
After unique():  1 2 3 2 1 2
3 elements were removed
 
Before unique(pred): 1 2 12 23 3 2 51 1 2 2
After unique(pred):  1 2 23 2 51 2
4 elements were removed

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 1207 | C++98 | it was unclear whether iterators and/or references will be invalidated | only invalidates iterators and references to the removed elements |

### See also

|  |  |
| --- | --- |
| unique | removes consecutive duplicate elements in a range   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/list/unique&oldid=130404>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 June 2021, at 03:44.