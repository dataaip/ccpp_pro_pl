# std::unordered_multimap<Key,T,Hash,KeyEqual,Allocator>::swap

From cppreference.com
< cpp‎ | container‎ | unordered multimap
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

`std::unordered_multimap`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_multimap::unordered_multimap | | | | | | unordered_multimap::~unordered_multimap | | | | | | unordered_multimap::operator= | | | | | | unordered_multimap::get_allocator | | | | | | Iterators | | | | | | unordered_multimap::beginunordered_multimap::cbegin | | | | | | unordered_multimap::endunordered_multimap::cend | | | | | | Capacity | | | | | | unordered_multimap::size | | | | | | unordered_multimap::max_size | | | | | | unordered_multimap::empty | | | | | | Modifiers | | | | | | unordered_multimap::clear | | | | | | unordered_multimap::insert | | | | | | unordered_multimap::insert_range(C++23) | | | | | | unordered_multimap::emplace | | | | | | unordered_multimap::emplace_hint | | | | | | unordered_multimap::erase | | | | | | ****unordered_multimap::swap**** | | | | | | unordered_multimap::extract(C++17) | | | | | | unordered_multimap::merge(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_multimap::count | | | | | | unordered_multimap::find | | | | | | unordered_multimap::contains(C++20) | | | | | | unordered_multimap::equal_range | | | | | | Bucket interface | | | | | | unordered_multimap::begin(size_type)unordered_multimap::cbegin(size_type) | | | | | | unordered_multimap::end(size_type)unordered_multimap::cend(size_type) | | | | | | unordered_multimap::bucket_count | | | | | | unordered_multimap::max_bucket_count | | | | | | unordered_multimap::bucket_size | | | | | | unordered_multimap::bucket | | | | | | Hash policy | | | | | | unordered_multimap::load_factor | | | | | | unordered_multimap::max_load_factor | | | | | | unordered_multimap::rehash | | | | | | unordered_multimap::reserve | | | | | | Observers | | | | | | unordered_multimap::hash_function | | | | | | unordered_multimap::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_multimap) | | | | | | erase_if(std::unordered_multimap)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| void swap( unordered_multimap& other ); |  | (since C++11)  (until C++17) |
| void swap( unordered_multimap& other ) noexcept(/\* see below \*/); |  | (since C++17) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Exchanges the contents of the container with those of other. Does not invoke any move, copy, or swap operations on individual elements.

All iterators and references remain valid. The `end()` iterator is invalidated.
The `Hash` and `KeyEqual` objects must be Swappable, and they are exchanged using unqualified calls to non-member `swap`.

|  |  |
| --- | --- |
| If std::allocator_traits<allocator_type>::propagate_on_container_swap::value is true, then the allocators are exchanged using an unqualified call to non-member `swap`. Otherwise, they are not swapped (and if get_allocator() != other.get_allocator(), the behavior is undefined). | (since C++11) |

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | container to exchange the contents with |

### Exceptions

|  |  |
| --- | --- |
| Any exception thrown by the swap of the `Hash` or `KeyEqual` objects. | (until C++17) |
| noexcept specification:noexcept(std::allocator_traits<Allocator>::is_always_equal::value  && std::is_nothrow_swappable<Hash>::value && std::is_nothrow_swappable<key_equal>::value) | (since C++17) |

### Complexity

Constant.

### Example

Run this code

```
#include <iostream>
#include <string>
#include <utility>
#include <unordered_map>
 
// print out a std::pair
template<class Os, class U, class V>
Os& operator<<(Os& os, const std::pair<U, V>& p)
{
    return os << p.first << ':' << p.second;
}
 
// print out a container
template<class Os, class Co>
Os& operator<<(Os& os, const Co& co)
{
    os << '{';
    for (auto const& i : co)
        os << ' ' << i;
    return os << " }\n";
}
 
int main()
{
    std::unordered_multimap<std::string, std::string>
        m1{{"γ", "gamma"}, {"β", "beta"}, {"α", "alpha"}, {"γ", "gamma"}},
        m2{{"ε", "epsilon"}, {"δ", "delta"}, {"ε", "epsilon"}};
 
    const auto& ref = *(m1.begin());
    const auto iter = std::next(m1.cbegin());
 
    std::cout << "──────── before swap ────────\n"
              << "m1: " << m1 << "m2: " << m2 << "ref: " << ref
              << "\niter: " << *iter << '\n';
 
    m1.swap(m2);
 
    std::cout << "──────── after swap ────────\n"
              << "m1: " << m1 << "m2: " << m2 << "ref: " << ref
              << "\niter: " << *iter << '\n';
 
    // Note that every iterator referring to an element in one container before
    // the swap refers to the same element in the other container after the swap.
    // Same is true for references.
}

```

Possible output:

```
──────── before swap ────────
m1: { α:alpha β:beta γ:gamma γ:gamma }
m2: { δ:delta ε:epsilon ε:epsilon }
ref: α:alpha
iter: β:beta
──────── after swap ────────
m1: { δ:delta ε:epsilon ε:epsilon }
m2: { α:alpha β:beta γ:gamma γ:gamma }
ref: α:alpha
iter: β:beta

```

### See also

|  |  |
| --- | --- |
| std::swap(std::unordered_multimap)(C++11) | specializes the std::swap algorithm   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_multimap/swap&oldid=136068>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 December 2021, at 10:53.