# std::erase, std::erase_if(std::list)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | list::list | | | | | | list::~list | | | | | | list::operator= | | | | | | list::assign | | | | | | list::assign_range(C++23) | | | | | | list::get_allocator | | | | | | Element access | | | | | | list::front | | | | | | list::back | | | | | | Iterators | | | | | | list::beginlist::cbegin(C++11) | | | | | | list::endlist::cend(C++11) | | | | | | list::rbeginlist::crbegin(C++11) | | | | | | list::rendlist::crend(C++11) | | | | | | Capacity | | | | | | list::size | | | | | | list::empty | | | | | | list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | list::clear | | | | | | list::insert | | | | | | list::insert_range(C++23) | | | | | | list::emplace(C++11) | | | | | | list::erase | | | | | | list::push_front | | | | | | list::emplace_front(C++11) | | | | | | list::prepend_range(C++23) | | | | | | list::pop_front | | | | | | list::push_back | | | | | | list::emplace_back(C++11) | | | | | | list::append_range(C++23) | | | | | | list::pop_back | | | | | | list::resize | | | | | | list::swap | | | | | | Operations | | | | | | list::merge | | | | | | list::splice | | | | | | list::removelist::remove_if | | | | | | list::reverse | | | | | | list::unique | | | | | | list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::list) | | | | | | ****erase(std::list)erase_if(std::list)****(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<list>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| template< class T, class Alloc, class U >  std::list<T, Alloc>::size_type     erase( std::list<T, Alloc>& c, const U& value ); |  | (since C++20)  (until C++26) |
| template< class T, class Alloc, class U = T >  std::list<T, Alloc>::size_type     erase( std::list<T, Alloc>& c, const U& value ); |  | (since C++26) |
|  |  |  |
| --- | --- | --- |
| template< class T, class Alloc, class Pred >  std::list<T, Alloc>::size_type     erase_if( std::list<T, Alloc>& c, Pred pred ); | (2) | (since C++20) |
|  |  |  |

1) Erases all elements that compare equal to value from the container. Equivalent to return c.remove_if(& -> bool { return elem == value; });.2) Erases all elements that satisfy the predicate pred from the container. Equivalent to return c.remove_if(pred);.

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | container from which to erase |
| value | - | value to be removed |
| pred | - | unary predicate which returns ​true if the element should be erased.   The expression pred(v) must be convertible to bool for every argument `v` of type (possibly const) `T`, regardless of value category, and must not modify `v`. Thus, a parameter type of T&is not allowed, nor is T unless for `T` a move is equivalent to a copy(since C++11). ​ |

### Return value

The number of erased elements.

### Complexity

Linear.

### Notes

Unlike std::list::remove, `erase` accepts heterogeneous types and does not force a conversion to the container's value type before invoking the == operator.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_algorithm_default_value_type` | `202403` | (C++26) | List-initialization for algorithm (1) |

### Example

Run this code

```
#include <complex>
#include <iostream>
#include <numeric>
#include <string_view>
#include <list>
 
void println(std::string_view comment, const auto& c)
{
    std::cout << comment << '[';
    bool first{true};
    for (const auto& x : c)
        std::cout << (first ? first = false, "" : ", ") << x;
    std::cout << "]\n";
}
 
int main()
{
    std::list<char> cnt(10);
    std::iota(cnt.begin(), cnt.end(), '0');
    println("Initially, cnt = ", cnt);
 
    std::erase(cnt, '3');
    println("After erase '3', cnt = ", cnt);
 
    auto erased = std::erase_if(cnt, [](char x) { return (x - '0') % 2 == 0; });
    println("After erase all even numbers, cnt = ", cnt);
    std::cout << "Erased even numbers: " << erased << '\n';
 
    std::list<std::complex<double>> nums{{2, 2}, {4, 2}, {4, 8}, {4, 2}};
    #ifdef __cpp_lib_algorithm_default_value_type
        std::erase(nums, {4, 2});
    #else
        std::erase(nums, std::complex<double>{4, 2});
    #endif
    println("After erase {4, 2}, nums = ", nums);
}

```

Output:

```
Initially, cnt = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
After erase '3', cnt = [0, 1, 2, 4, 5, 6, 7, 8, 9]
After erase all even numbers, cnt = [1, 5, 7, 9]
Erased even numbers: 5
After erase {4, 2}, nums = [(2,2), (4,8)]

```

### See also

|  |  |
| --- | --- |
| removeremove_if | removes elements satisfying specific criteria   (function template) |
| ranges::removeranges::remove_if(C++20)(C++20) | removes elements satisfying specific criteria (algorithm function object) |
| removeremove_if | removes elements satisfying specific criteria   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/list/erase2&oldid=161908>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 November 2023, at 06:21.