# std::experimental::apply

From cppreference.com
< cpp‎ | experimental
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Library fundamentals

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::optional | | | | |
| experimental::any | | | | |
| experimental::basic_string_view | | | | |
| experimental::sample | | | | |
| experimental::shared_ptr | | | | |
| experimental::weak_ptr | | | | |
| ****experimental::apply**** | | | | |
| experimental::invocation_typeexperimental::raw_invocation_type | | | | |
| experimental::search | | | | |
| experimental::default_searcherexperimental::make_default_searcher | | | | |
| experimental::boyer_moore_searcherexperimental::make_boyer_moore_searcher | | | | |
| experimental::boyer_moore_horspool_searcherexperimental::make_boyer_moore_horspool_searcher | | | | |
| Type-erased and polymorphic allocators | | | | |
| Variable templates for type traits | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/tuple>` |  |  |
| template< class F, class Tuple >  constexpr decltype(auto) apply(F&& f, Tuple&& t); |  | (library fundamentals TS) |
|  |  |  |

Invoke the Callable object f with a tuple of arguments.

### Parameters

|  |  |  |
| --- | --- | --- |
| f | - | Callable object to be invoked |
| t | - | tuple whose elements to be used as arguments to f |

### Return value

What returned by f.

### Possible implementation

|  |
| --- |
| ```text namespace detail {     template<class F, class Tuple, std::size_t... I>     constexpr decltype(auto) apply_impl(F&& f, Tuple&& t, std::index_sequence<I...>)     {         return std::invoke(std::forward<F>(f), std::get<I>(std::forward<Tuple>(t))...);         // Note: std::invoke is a C++17 feature     } } // namespace detail   template<class F, class Tuple> constexpr decltype(auto) apply(F&& f, Tuple&& t) {     return detail::apply_impl(std::forward<F>(f), std::forward<Tuple>(t),         std::make_index_sequence<std::tuple_size_v<std::decay_t<Tuple>>>{}); } ``` |

### Example

Run this code

```
#include <iostream>
#include <tuple>
 
template<typename... Ts>
void print_tuple(const std::tuple<Ts...> &tuple)
{
    std::apply([](const auto&... elem) 
    {
        ((std::cout << elem << '\n'), ...); 
    }, tuple);
}
 
int main()
{
    const std::tuple<int, char> t = std::make_tuple(5, 'a');
    print_tuple(t);
}

```

Output:

```
5
a

```

### See also

|  |  |
| --- | --- |
| make_tuple(C++11) | creates a `tuple` object of the type defined by the argument types   (function template) |
| forward_as_tuple(C++11) | creates a `tuple` of forwarding references   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/apply&oldid=151588>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 May 2023, at 11:40.