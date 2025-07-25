# std::ranges::views::chunk, std::ranges::chunk_view

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | ****chunk_viewviews::chunk****(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

****std::ranges::chunk_view****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| chunk_view::chunk_view | | | | |
| chunk_view::base | | | | |
| chunk_view::begin | | | | |
| chunk_view::end | | | | |
| chunk_view::size | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Classes for `input_range`s | | | | | | Deduction guides | | | | | | **outer-iterator** | | | | | | chunk_view::**outer-iterator**::**outer-iterator** | | | | | | chunk_view::**outer-iterator**::operator= | | | | | | chunk_view::**outer-iterator**::operator\* | | | | | | chunk_view::**outer-iterator**::operator++ chunk_view::**outer-iterator**::operator++(int) | | | | | | operator==(chunk_view::**outer-iterator**) | | | | | | operator-(chunk_view::**outer-iterator**) | | | | | | **outer-iterator**::value_type | | | | | | chunk_view::**outer-iterator**::value_type::value_type | | | | | | chunk_view::**outer-iterator**::value_type::begin | | | | | | chunk_view::**outer-iterator**::value_type::end | | | | | | chunk_view::**outer-iterator**::value_type::size | | | | | | **inner-iterator** | | | | | | chunk_view::**inner-iterator**::**inner-iterator** | | | | | | chunk_view::**inner-iterator**::operator= | | | | | | chunk_view::**inner-iterator**::base | | | | | | chunk_view::**inner-iterator**::operator\* | | | | | | chunk_view::**inner-iterator**::operator++ chunk_view::**inner-iterator**::operator++(int) | | | | | | operator==(chunk_view::**inner-iterator**) | | | | | | operator-(chunk_view::**inner-iterator**) | | | | | | iter_move(chunk_view::**inner-iterator**) | | | | | | iter_swap(chunk_view::**inner-iterator**) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template for `forward_range`s | | | | | | **iterator** | | | | | | chunk_view::**iterator**::**iterator** | | | | | | chunk_view::**iterator**::base | | | | | | chunk_view::**iterator**::operator\* | | | | | | [chunk_view::**iterator**::operator[]](chunk_view/iterator/operator_at.html "cpp/ranges/chunk view/iterator/operator at") | | | | | | chunk_view::**iterator**::operator++ chunk_view::**iterator**::operator++(int) chunk_view::**iterator**::operator-- chunk_view::**iterator**::operator--(int) chunk_view::**iterator**::operator+= chunk_view::**iterator**::operator-= | | | | | | operator==(chunk_view::**iterator**) operator<(chunk_view::**iterator**) operator>(chunk_view::**iterator**) operator<=(chunk_view::**iterator**) operator>=(chunk_view::**iterator**) operator<=>(chunk_view::**iterator**) | | | | | | operator+(chunk_view::**iterator**) operator-(chunk_view::**iterator**) | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template< ranges::view V >      requires ranges::input_range<V>  class chunk_view : public ranges::view_interface<chunk_view<V>> | (1) | (since C++23) |
| template< ranges::view V >      requires ranges::forward_range<V>  class chunk_view<V> : public ranges::view_interface<chunk_view<V>> | (2) | (since C++23) |
| namespace views {  inline constexpr /\* unspecified \*/ chunk = /\* unspecified \*/; } | (3) | (since C++23) |
| Call signature |  |  |
| template< ranges::viewable_range R >  constexpr ranges::view auto chunk( R&& r, ranges::range_difference_t<R> n ); |  | (since C++23) |
| template< class DifferenceType >  constexpr /\*range adaptor closure\*/ chunk( DifferenceType&& n ); |  | (since C++23) |
| Helper templates |  |  |
| template< class I >   constexpr I /\*div-ceil\*/( I num, I denom ); | (4) | (exposition only\*) |
|  |  |  |

`chunk_view` takes a `view` and a number n and produces a range of views (the **chunks**) of the original view, such that each **chunk**, except maybe the last one, has the size `n`. These **chunks** are non-overlapping, successive sub-ranges of the elements of the original view, in order.

Let `s` be the size of the original view. If `s` is not the multiple of n, the size of the **last** produced view is exactly s % n (the remainder). Otherwise, the size of each **chunk**, including the last one, is n.

The size of produced view is /\*div-ceil\*/(s).

If the n is not greater than ​0​ the behavior is undefined.

1) An implementation that supports the underlying view `V` that models only `input_range`.2) A partial specialization that supports the underlying view `V` that models `forward_range` or stronger. Models `common_range` if the underlying view `V` is `forward_range`, `common_range`, and either `sized_range` or non `bidirectional_range`.3) The name views::chunk denotes a RangeAdaptorObject. Given subexpressions e and n, the expression views::chunk(e, n) is expression-equivalent to chunk_view(e, n).4) Computes the smallest integer value that is not less than the quotient of dividing num by denom. Equivalent to:

```
I r = num / denom;
if (num % denom)
    ++r;
return r;

```

### Data members

|  |  |
| --- | --- |
| Member object | Definition |
| `base_` (private) | The underlying `view` of type `V`. (exposition-only member object\*) |
| `n_` (private) | The "chunk size" of type ranges::range_difference_t<V>. (exposition-only member object\*) |

|  |  |
| --- | --- |
| If `V` models exactly `input_range` (1) | |
| `remainder_` (private)  (conditionally present) | The number of elements left in the current chunk, of type ranges::range_difference_t<V>. (exposition-only member object\*) |
| `current_` (private)  (conditionally present) | An **optional-like** object of type /\*non-propagating-cache\*/<ranges::iterator_t<V>> that caches current underlying iterator. (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `chunk_view`   (public member function) |
| base | returns a copy of the underlying (adapted) view   (public member function) |
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

### Nested classes

|  |  |
| --- | --- |
| **outer_iterator**(C++23) | the output ("chunk-wise") iterator type when `V` models `input_range` (1) (exposition-only member class\*) |
| **inner_iterator**(C++23) | the inner ("element-wise") iterator type when `V` models `input_range` (1) (exposition-only member class\*) |
| **iterator**(C++23) | the iterator type when `V` models `forward_range` (2) (exposition-only member class template\*) |

### Helper templates

|  |  |  |
| --- | --- | --- |
| template< class V >  constexpr bool ranges::enable_borrowed_range<chunk_view<V>> = ranges::forward_range<V> && ranges::enable_borrowed_range<V>; |  | (since C++23) |
|  |  |  |

This specialization of ranges::enable_borrowed_range makes `chunk_view` satisfy `borrowed_range` when the underlying view `V` satisfies both, the `forward_range` and the `borrowed_range`.

### Notes

If `V` models `input_range` (1), `chunk_view`'s iterator has a dedicated type: `outer_iterator::value_type` that is itself an input view.

If `V` models `forward_range` or stronger (2), `chunk_view` defers to views::take for its `value_type`.

If `V` models `bidirectional_range` or stronger ranges (2), the need to calculate size the last chunk correctly (from the end iterator) requires the underlying range type `V` to be `sized_range`.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_ranges_chunk` | `202202L` | (C++23) | `std::ranges::chunk_view` |

### Example

Run this code

```
#include <algorithm>
#include <iostream>
#include <ranges>
 
auto print_subrange = [](std::ranges::viewable_range auto&& r)
{
    std::cout << '[';
    for (int pos{}; auto elem : r)
        std::cout << (pos++ ? " " : "") << elem;
    std::cout << "] ";
};
 
int main()
{
    const auto v = {1, 2, 3, 4, 5, 6};
 
    for (const unsigned width : std::views::iota(1U, 2U + v.size()))
    {
        auto const chunks = v | std::views::chunk(width);
        std::cout << "chunk(" << width << "): ";
        std::ranges::for_each(chunks, print_subrange);
        std::cout << '\n';
    }
}

```

Output:

```
chunk(1): [1] [2] [3] [4] [5] [6]
chunk(2): [1 2] [3 4] [5 6]
chunk(3): [1 2 3] [4 5 6]
chunk(4): [1 2 3 4] [5 6]
chunk(5): [1 2 3 4 5] [6]
chunk(6): [1 2 3 4 5 6]
chunk(7): [1 2 3 4 5 6]

```

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 26.7.28 Chunk view [range.chunk]

### See also

|  |  |
| --- | --- |
| ranges::chunk_by_viewviews::chunk_by(C++23) | splits the `view` into subranges between each pair of adjacent elements for which the given predicate returns false (class template) (range adaptor object) |
| ranges::adjacent_viewviews::adjacent(C++23) | a `view` consisting of tuples of references to adjacent elements of the adapted view (class template) (range adaptor object) |
| ranges::slide_viewviews::slide(C++23) | a `view` whose Mth element is a `view` over the Mth through (M + N - 1)th elements of another `view` (class template) (range adaptor object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/chunk_view&oldid=173593>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 July 2024, at 11:24.