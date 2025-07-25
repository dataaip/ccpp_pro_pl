# std::erase, std::erase_if(std::forward_list)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_list::forward_list | | | | | | forward_list::~forward_list | | | | | | forward_list::operator= | | | | | | forward_list::assign | | | | | | forward_list::assign_range(C++23) | | | | | | forward_list::get_allocator | | | | | | Element access | | | | | | forward_list::front | | | | | | Iterators | | | | | | forward_list::before_beginforward_list::cbefore_begin | | | | | | forward_list::beginforward_list::cbegin | | | | | | forward_list::endforward_list::cend | | | | | | Capacity | | | | | | forward_list::empty | | | | | | forward_list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | forward_list::clear | | | | | | forward_list::emplace_front | | | | | | forward_list::push_front | | | | | | forward_list::insert_after | | | | | | forward_list::emplace_after | | | | | | forward_list::erase_after | | | | | | forward_list::insert_range_after(C++23) | | | | | | forward_list::prepend_range(C++23) | | | | | | forward_list::pop_front | | | | | | forward_list::resize | | | | | | forward_list::swap | | | | | | Operations | | | | | | forward_list::merge | | | | | | forward_list::splice_after | | | | | | forward_list::removeforward_list::remove_if | | | | | | forward_list::reverse | | | | | | forward_list::unique | | | | | | forward_list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::forward_list) | | | | | | ****erase(std::forward_list)erase_if(std::forward_list)****(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<forward_list>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| template< class T, class Alloc, class U >  std::forward_list<T, Alloc>::size_type     erase( std::forward_list<T, Alloc>& c, const U& value ); |  | (since C++20)  (until C++26) |
| template< class T, class Alloc, class U = T >  std::forward_list<T, Alloc>::size_type     erase( std::forward_list<T, Alloc>& c, const U& value ); |  | (since C++26) |
|  |  |  |
| --- | --- | --- |
| template< class T, class Alloc, class Pred >  std::forward_list<T, Alloc>::size_type     erase_if( std::forward_list<T, Alloc>& c, Pred pred ); | (2) | (since C++20) |
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

Unlike std::forward_list::remove, `erase` accepts heterogeneous types and does not force a conversion to the container's value type before invoking the == operator.

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
#include <forward_list>
 
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
    std::forward_list<char> cnt(10);
    std::iota(cnt.begin(), cnt.end(), '0');
    println("Initially, cnt = ", cnt);
 
    std::erase(cnt, '3');
    println("After erase '3', cnt = ", cnt);
 
    auto erased = std::erase_if(cnt, [](char x) { return (x - '0') % 2 == 0; });
    println("After erase all even numbers, cnt = ", cnt);
    std::cout << "Erased even numbers: " << erased << '\n';
 
    std::forward_list<std::complex<double>> nums{{2, 2}, {4, 2}, {4, 8}, {4, 2}};
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

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/forward_list/erase2&oldid=159709>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 September 2023, at 09:16.