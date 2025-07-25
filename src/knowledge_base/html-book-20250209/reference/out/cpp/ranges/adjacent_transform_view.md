# std::ranges::views::adjacent_transform, std::ranges::adjacent_transform_view, std::ranges::views::pairwise_transform

From cppreference.com
< cpp‎ | ranges
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

Ranges library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | begin | | | | | | cbegin | | | | | | end | | | | | | cend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rbegin | | | | | | crbegin | | | | | | rend | | | | | | crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | size | | | | | | ssize | | | | | | data | | | | | | cdata | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty | | | | | |  | | | | | |  | | | | | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range conversions | | | | | | std::from_range_t std::from_range(C++23)(C++23) | | | | | | to(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Dangling iterator handling | | | | | | dangling | | | | | | borrowed_iterator_t | | | | | | borrowed_subrange_t | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range primitives | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | range_size_trange_difference_trange_value_t | | | | | | elements_of(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iterator_tconst_iterator_tsentinel_tconst_sentinel_t(C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | range_reference_trange_const_reference_trange_rvalue_reference_trange_common_reference_t(C++23) | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | range | | | | | | borrowed_range | | | | | | sized_range | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_range | | | | | | view | | | | | | viewable_range | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | input_range | | | | | | output_range | | | | | | forward_range | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bidirectional_range | | | | | | random_access_range | | | | | | contiguous_range | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | constant_range(C++23) | | | | | |  | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Views | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | view_interface | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | subrange | | | | | |  | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range factories | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty_viewviews::empty | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | single_viewviews::single | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | basic_istream_viewviews::istream | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota_viewviews::iota | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | repeat_viewviews::repeat(C++23)(C++23) | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | ****adjacent_transform_viewviews::adjacent_transform****(C++23)(C++23) | | | | | | ****views::pairwise_transform****(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

****std::ranges::adjacent_transform_view****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| adjacent_transform_view::adjacent_transform_view | | | | |
| adjacent_transform_view::begin | | | | |
| adjacent_transform_view::end | | | | |
| adjacent_transform_view::size | | | | |
| Iterator | | | | |
| Member functions | | | | |
| adjacent_transform_view::**iterator**::**iterator** | | | | |
| adjacent_transform_view::**iterator**::operator\* | | | | |
| [adjacent_transform_view::**iterator**::operator[]](adjacent_transform_view/iterator/operator_at.html "cpp/ranges/adjacent transform view/iterator/operator at") | | | | |
| adjacent_transform_view::**iterator**::operator++ adjacent_transform_view::**iterator**::operator++(int) adjacent_transform_view::**iterator**::operator-- adjacent_transform_view::**iterator**::operator--(int) adjacent_transform_view::**iterator**::operator+= adjacent_transform_view::**iterator**::operator-= | | | | |
| Non-member functions | | | | |
| operator==(adjacent_transform_view::**iterator**) operator<(adjacent_transform_view::**iterator**) operator>(adjacent_transform_view::**iterator**) operator<=(adjacent_transform_view::**iterator**) operator>=(adjacent_transform_view::**iterator**) operator<=>(adjacent_transform_view::**iterator**) | | | | |
| operator+(adjacent_transform_view::**iterator**) operator-(adjacent_transform_view::**iterator**) | | | | |
| Sentinel | | | | |
| Member functions | | | | |
| adjacent_transform_view::**sentinel**::**sentinel** | | | | |
| Non-member functions | | | | |
| operator==(adjacent_transform_view::**iterator**,adjacent_transform_view::**sentinel**) | | | | |
| operator-(adjacent_transform_view::**iterator**,adjacent_transform_view::**sentinel**) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template< ranges::forward_range V, std::move_constructible F, std::size_t N >    requires ranges::view<V> && (N > 0) && std::is_object_v<F> &&             std::regular_invocable<F&,                 /\*REPEAT\*/(ranges::range_reference_t<V>, N)...> &&             /\*can-reference\*/<std::invoke_result_t<F&,                 /\*REPEAT\*/(ranges::range_reference_t<V>, N)...>>  class adjacent_transform_view : public ranges::view_interface<adjacent_transform_view<V, F, N>> | (1) | (since C++23) |
| namespace views {  template< std::size_t N >      constexpr /\* unspecified \*/ adjacent_transform = /\* unspecified \*/; } | (2) | (since C++23) |
| namespace views {  inline constexpr auto pairwise_transform = adjacent_transform<2>; } | (3) | (since C++23) |
| Call signature |  |  |
| template< ranges::viewable_range R, class F >      requires /\* see below \*/ constexpr ranges::view auto adjacent_transform<N>( R&& r, F&& fun ); |  | (since C++23) |
| template< class F >  constexpr /\*range adaptor closure\*/ adjacent_transform<N>( F&& fun ); |  | (since C++23) |
|  |  |  |

1) `adjacent_transform_view` is a range adaptor that takes a `view` and an invocable object fun, and produces a `view` whose `i`th element is a value that is the result of applying fun to each element in ``i`,`i + N`)` of the original view. `F` always has [arity `N`. Let `S` be the size of the original view. Then the size of produced view is:

- S - N + 1, if S >= N,
- ​0​ otherwise, and the resulting view is empty.
2) The name views::adjacent_transform<N> denotes a RangeAdaptorObject. Given subexpressions e and f, and a constant expression `N`, the expression views::adjacent_transform<N>(e, f) is expression-equivalent to:

- ((void)e, views::zip_transform(f)), if `N` is equal to ​0​ and decltype((e)) models `forward_range` (except that the evaluations of e and f are indeterminately sequenced),
- adjacent_transform_view<views::all_t<decltype((e))>, std::decay_t<decltype((f))>, N>(e, f) otherwise.
3) The name views::pairwise_transform denotes a RangeAdaptorObject that behaves exactly as views::adjacent_transform<2>. In particular, the arity of `F` is also 2 and fun is a binary invocable object.

`adjacent_transform_view` always models `forward_range`, and models `bidirectional_range`, `random_access_range`, or `sized_range`, if adapted `view` type models the corresponding concept.

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `adjacent_transform_view`   (public member function) |
| begin | returns an iterator to the beginning   (public member function) |
| end | returns an iterator or a sentinel to the end   (public member function) |
| size | returns the number of elements. Provided only if the underlying (adapted) range satisfies `sized_range`.   (public member function) |
| Inherited from std::ranges::view_interface | |
| empty | returns whether the derived view is empty. Provided if it satisfies `sized_range` or `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| cbegin(C++23) | returns a constant iterator to the beginning of the range.   (public member function of `std::ranges::view_interface<D>`) |
| cend(C++23) | returns a sentinel for the constant iterator of the range.   (public member function of `std::ranges::view_interface<D>`) |
| operator bool | returns whether the derived view is not empty. Provided if ranges::empty is applicable to it.   (public member function of `std::ranges::view_interface<D>`) |
| front | returns the first element in the derived view. Provided if it satisfies `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| back | returns the last element in the derived view. Provided if it satisfies `bidirectional_range` and `common_range`.   (public member function of `std::ranges::view_interface<D>`) |
| [operator[]](view_interface/operator_at.html "cpp/ranges/view interface/operator at") | returns the `n`th element in the derived view. Provided if it satisfies `random_access_range`.   (public member function of `std::ranges::view_interface<D>`) |

### Deduction guides

(none)

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `InnerView` (private) | ranges::adjacent_view<V, N>. (exposition-only member type\*) |
| `inner_iterator` (private) | - ranges::iterator_t<const InnerView>, if `Const` is true. Otherwise, - ranges::iterator_t<InnerView>. (exposition-only member type\*) |
| `inner_sentinel` (private) | - ranges::sentinel_t<const InnerView>, if `Const` is true. Otherwise, - ranges::sentinel_t<InnerView>. (exposition-only member type\*) |

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| `fun_` (private) | /\*movable-box\*/<F> (exposition-only member object\*) |
| `inner_` (private) | ranges::adjacent_view<V,N> (exposition-only member object\*) |

### Nested classes

|  |  |
| --- | --- |
| **iterator** | the iterator type (exposition-only member class template\*) |
| **sentinel** | the sentinel type used when `adjacent_transform_view` is not a `common_range` (exposition-only member class template\*) |

### Notes

views::adjacent_transform only accepts foward ranges even when `N` is `0`.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_ranges_zip` | `202110L` | (C++23) | ranges::zip_view, ranges::zip_transform_view, ranges::adjacent_view, `ranges::adjacent_transform_view` |

### Example

Run this code

```
#include <array>
#include <iostream>
#include <ranges>
 
int main()
{
    constexpr static std::array data{1, 2, 3, 4, 5, 6};
    constexpr int window{3};
 
    auto Fun = [](auto... ints) { return (... + ints); };
    // Alternatively, the Fun could be any ternary (if window == 3) callable, e.g.:
    // auto Fun = [](int x, int y, int z) { return x + y + z; };
 
    constexpr auto view = data | std::views::adjacent_transform<window>(Fun);
 
    static_assert(
        view.size() == (data.size() - window + 1)
        && std::array{6, 9, 12, 15}
        == std::array{view[0], view[1], view[2], view[3]}
        && view[0] == Fun(data[0], data[1], data[2])
        && view[1] == Fun(data[1], data[2], data[3])
        && view[2] == Fun(data[2], data[3], data[4])
        && view[3] == Fun(data[3], data[4], data[5])
    );
 
    for (int x : view)
        std::cout << x << ' ';
    std::cout << '\n';
}

```

Output:

```
6 9 12 15

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 4098 | C++23 | views::adjacent_transform<0> used to accept input-only ranges | made rejected |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 26.7.27 Adjacent transform view [range.adjacent.transform]

### See also

|  |  |
| --- | --- |
| ranges::adjacent_viewviews::adjacent(C++23) | a `view` consisting of tuples of references to adjacent elements of the adapted view (class template) (range adaptor object) |
| ranges::transform_viewviews::transform(C++20) | a `view` of a sequence that applies a transformation function to each element (class template) (range adaptor object) |
| ranges::zip_transform_viewviews::zip_transform(C++23) | a `view` consisting of results of application of a transformation function to corresponding elements of the adapted views (class template) (customization point object) |
| ranges::transform(C++20) | applies a function to a range of elements (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/adjacent_transform_view&oldid=173369>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 July 2024, at 18:04.