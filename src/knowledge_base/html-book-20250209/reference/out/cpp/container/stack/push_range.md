# std::stack<T,Container>::push_range

From cppreference.com
< cpp‎ | container‎ | stack
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

`std::stack`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| stack::stack | | | | |
| stack::~stack | | | | |
| stack::operator= | | | | |
| Element access | | | | |
| stack::top | | | | |
| Capacity | | | | |
| stack::empty | | | | |
| stack::size | | | | |
| Modifiers | | | | |
| stack::push | | | | |
| ****stack::push_range****(C++23) | | | | |
| stack::emplace(C++11) | | | | |
| stack::pop | | | | |
| stack::swap(C++11) | | | | |
| Non-member functions | | | | |
| swap(std::stack)(C++11) | | | | |
| operator==operator!=operator<operator>operator<=operator>=operator<=>(C++20) | | | | |
| Helper classes | | | | |
| uses_allocator<std::stack>(C++11) | | | | |
| formatter<std::stack>(C++23) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| template< container-compatible-range<value_type> R >  void push_range( R&& rg ); |  | (since C++23) |
|  |  |  |

Inserts a copy of each element of rg in `stack`, as if by:

- c.append_range(std::forward<R>(rg)) if that is a valid expression (i.e. the underlying container c has an appropriate `append_range` member function), or
- ranges::copy(rg, std::back_inserter(c)) otherwise.

Each iterator in the range rg is dereferenced exactly once.

### Parameters

|  |  |  |
| --- | --- | --- |
| rg | - | a container compatible range, that is, an `input_range` whose elements are convertible to `T` |

### Return value

(none)

### Complexity

Identical to the complexity of c.append_range or ranges::copy(rg, std::back_inserter(c)) (depending on what function is used internally).

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges-aware construction and insertion |

### Example

Run this code

```
#include <algorithm>
#include <iostream>
#include <ranges>
#include <stack>
 
template<typename Adaptor>
requires (std::ranges::input_range<typename Adaptor::container_type>)
void println(auto, const Adaptor& adaptor)
{
    struct Container : Adaptor // gain access to protected Adaptor::Container c;
    {
        auto const& container() const { return this->c; }
    };
 
    for (auto const& elem : static_cast<const Container&>(adaptor).container())
        std::cout << elem << ' ';
    std::cout << '\n';
}
 
int main()
{
    std::stack<int> adaptor;
    const auto rg = {1, 3, 2, 4};
 
#ifdef __cpp_lib_containers_ranges
    adaptor.push_range(rg);
#else
    std::ranges::for_each(rg, &adaptor{ adaptor.push(e); });
#endif
 
    println("{}", adaptor);
}

```

Output:

```
1 3 2 4

```

### See also

|  |  |
| --- | --- |
| push | inserts element at the top   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/stack/push_range&oldid=156412>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 August 2023, at 23:38.