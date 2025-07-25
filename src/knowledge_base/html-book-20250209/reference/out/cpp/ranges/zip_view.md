# std::ranges::views::zip, std::ranges::zip_view

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | ****zip_viewviews::zip****(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

****std::ranges::zip_view****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| zip_view::zip_view | | | | |
| zip_view::begin | | | | |
| zip_view::end | | | | |
| zip_view::size | | | | |
| Deduction guides | | | | |
| Iterator | | | | |
| Member functions | | | | |
| zip_view::**iterator**::**iterator** | | | | |
| zip_view::**iterator**::operator\* | | | | |
| [zip_view::**iterator**::operator[]](zip_view/iterator/operator_at.html "cpp/ranges/zip view/iterator/operator at") | | | | |
| zip_view::**iterator**::operator++ zip_view::**iterator**::operator++(int) zip_view::**iterator**::operator-- zip_view::**iterator**::operator--(int) zip_view::**iterator**::operator+= zip_view::**iterator**::operator-= | | | | |
| Non-member functions | | | | |
| operator==(zip_view::**iterator**) operator<(zip_view::**iterator**) operator>(zip_view::**iterator**) operator<=(zip_view::**iterator**) operator>=(zip_view::**iterator**) operator<=>(zip_view::**iterator**) | | | | |
| operator+(zip_view::**iterator**) operator-(zip_view::**iterator**) | | | | |
| iter_move(zip_view::**iterator**) | | | | |
| iter_swap(zip_view::**iterator**) | | | | |
| Sentinel | | | | |
| Member functions | | | | |
| zip_view::**sentinel**::**sentinel** | | | | |
| Non-member functions | | | | |
| operator==(zip_view::**iterator**,zip_view::**sentinel**) | | | | |
| operator-(zip_view::**iterator**,zip_view::**sentinel**) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template< ranges::input_range... Views >      requires (ranges::view<Views> && ...) && (sizeof...(Views) > 0)  class zip_view : public ranges::view_interface<zip_view<Views...>> | (1) | (since C++23) |
| namespace views {  inline constexpr /\*unspecified\*/ zip = /\*unspecified\*/; } | (2) | (since C++23) |
| Call signature |  |  |
| template< ranges::viewable_range... Rs >      requires /\* see below \*/ constexpr ranges::view auto zip( Rs&&... rs ); |  | (since C++23) |
|  |  |  |

1) `zip_view` is a range adaptor that takes one or more `view`s, and produces a `view` whose `i`th element is a tuple-like value consisting of the `i`th elements of all views. The size of produced view is the minimum of sizes of all adapted views.2) `views::zip` is a customization point object.  

When calling with no argument, views::zip() is expression-equivalent to auto(views::empty<std::tuple<>>).

Otherwise, views::zip(rs...) is **expression-equivalent** to ranges::zip_view<views::all_t<decltype((rs))>...>(rs...).

`zip_view` always models `input_range`, and models `forward_range`, `bidirectional_range`, `random_access_range`, or `sized_range` if all adapted `view` types model the corresponding concept.

`zip_view` models `common_range` if

- sizeof...(Views) is equal to 1, and the only adapted view type models `common_range`, or
- at least one adapted view type does not model `bidirectional_range`, and every adapted view type models `common_range`, or
- every adapted view type models both `random_access_range` and `sized_range`.

### Customization point objects

The name `views::zip` denotes a **customization point object**, which is a const function object of a literal `semiregular` class type. For exposition purposes, the cv-unqualified version of its type is denoted as `__zip_fn`.

All instances of `__zip_fn` are equal. The effects of invoking different instances of type `__zip_fn` on the same arguments are equivalent, regardless of whether the expression denoting the instance is an lvalue or rvalue, and is const-qualified or not (however, a volatile-qualified instance is not required to be invocable). Thus, `views::zip` can be copied freely and its copies can be used interchangeably.

Given a set of types `Args...`, if std::declval<Args>()... meet the requirements for arguments to `views::zip` above, `__zip_fn` models

- std::invocable<__zip_fn, Args...>,
- std::invocable<const __zip_fn, Args...>,
- std::invocable<__zip_fn&, Args...>, and
- std::invocable<const __zip_fn&, Args...>.

Otherwise, no function call operator of `__zip_fn` participates in overload resolution.

### Data members

|  |  |
| --- | --- |
| Member | Description |
| std::tuple<Views...> `views_` | all adapted view objects (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `zip_view`   (public member function) |
| begin | returns an iterator to the beginning   (public member function) |
| end | returns an iterator or a sentinel to the end   (public member function) |
| size | returns the number of elements. Provided only if each underlying (adapted) range satisfies `sized_range`.   (public member function) |
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
| **iterator** | the iterator type (exposition-only member class template\*) |
| **sentinel** | the sentinel type used when `zip_view` is not a `common_range` (exposition-only member class template\*) |

### Helper templates

|  |  |  |
| --- | --- | --- |
| template< class... Views >  constexpr bool enable_borrowed_range<ranges::zip_view<Views...>> = (ranges::enable_borrowed_range<Views> && ...); |  | (since C++23) |
|  |  |  |

This specialization of ranges::enable_borrowed_range makes `zip_view` satisfy `borrowed_range` when each underlying view satisfies it.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_ranges_zip` | `202110L` | (C++23) | `ranges::zip_view`, ranges::zip_transform_view, ranges::adjacent_view, ranges::adjacent_transform_view |

### Example

Run this code

```
#include <array>
#include <iostream>
#include <list>
#include <ranges>
#include <string>
#include <tuple>
#include <vector>
 
void print(auto const rem, auto const& range)
{
    for (std::cout << rem; auto const& elem : range)
        std::cout << elem << ' ';
    std::cout << '\n';
}
 
int main()
{
    auto x = std::vector{1, 2, 3, 4};
    auto y = std::list<std::string>{"α", "β", "γ", "δ", "ε"};
    auto z = std::array{'A', 'B', 'C', 'D', 'E', 'F'};
 
    print("Source views:", "");
    print("x: ", x);
    print("y: ", y);
    print("z: ", z);
 
    print("\nzip(x,y,z):", "");
 
    for (std::tuple<int&, std::string&, char&> elem : std::views::zip(x, y, z))
    {
        std::cout << std::get<0>(elem) << ' '
                  << std::get<1>(elem) << ' '
                  << std::get<2>(elem) << '\n';
 
        std::get<char&>(elem) += ('a' - 'A'); // modifies the element of z
    }
 
    print("\nAfter modification, z: ", z);
}

```

Output:

```
Source views:
x: 1 2 3 4
y: α β γ δ ε
z: A B C D E F
 
zip(x,y,z):
1 α A
2 β B
3 γ C
4 δ D
 
After modification, z: a b c d E F

```

### See also

|  |  |
| --- | --- |
| ranges::zip_transform_viewviews::zip_transform(C++23) | a `view` consisting of results of application of a transformation function to corresponding elements of the adapted views (class template) (customization point object) |
| ranges::elements_viewviews::elements(C++20) | takes a `view` consisting of **tuple-like** values and a number N and produces a `view` of Nth element of each tuple (class template) (range adaptor object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/zip_view&oldid=177009>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 October 2024, at 01:13.