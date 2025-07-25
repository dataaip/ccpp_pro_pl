# std::ranges::owning_view

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | ****owning_view**** | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template< ranges::range R >      requires std::movable<R> && (!/\*is-initializer-list\*/<R>)  class owning_view : public ranges::view_interface<owning_view<R>> |  | (since C++20) |
|  |  |  |

`owning_view` is a `view` that has unique ownership of a `range`. It is move-only and stores that `range` within it.

The constant /\*is-initializer-list\*/<R> in the requires-clause is true if and only if std::remove_cvref_t<R> is a specialization of std::initializer_list.

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| `r_` (private) | The underlying range of type `R`. (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs an `owning_view` by value-initializing or move-constructing the stored range   (public member function) |
| operator= | move-assigns the stored range   (public member function) |
| base | returns a reference to the stored range   (public member function) |
| begin | returns the beginning iterator of the stored range   (public member function) |
| end | returns the sentinel of the stored range   (public member function) |
| empty | checks whether the stored range is empty   (public member function) |
| size | returns the size of the stored `sized_range`   (public member function) |
| data | returns the pointer to the beginning of the stored `contiguous_range`   (public member function) |
| Inherited from std::ranges::view_interface | |
| cbegin(C++23) | returns a constant iterator to the beginning of the range.   (public member function of `std::ranges::view_interface<D>`) |
| cend(C++23) | returns a sentinel for the constant iterator of the range.   (public member function of `std::ranges::view_interface<D>`) |
| operator bool | returns whether the derived view is not empty. Provided if ranges::empty is applicable to it.   (public member function of `std::ranges::view_interface<D>`) |
| front | returns the first element in the derived view. Provided if it satisfies `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| back | returns the last element in the derived view. Provided if it satisfies `bidirectional_range` and `common_range`.   (public member function of `std::ranges::view_interface<D>`) |
| [operator[]](view_interface/operator_at.html "cpp/ranges/view interface/operator at") | returns the `n`th element in the derived view. Provided if it satisfies `random_access_range`.   (public member function of `std::ranges::view_interface<D>`) |

## std::ranges::owning_view::owning_view

|  |  |  |
| --- | --- | --- |
| owning_view() requires std::default_initializable<R> = default; | (1) | (since C++20) |
| owning_view( owning_view&& other ) = default; | (2) | (since C++20) |
| constexpr owning_view( R&& t ); | (3) | (since C++20) |
| owning_view( const owning_view& ) = delete; | (4) | (since C++20) |
|  |  |  |

1) Default constructor. Value-initializes the stored range by its default member initializer (= R()).2) Move constructor. Move constructs the stored range from that of other.3) Move constructs the stored range from t.4) Copy constructor is deleted. `owning_view` is move-only.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another `owning_view` to move from |
| t | - | range to move from |

## std::ranges::owning_view::operator=

|  |  |  |
| --- | --- | --- |
| owning_view& operator=( owning_view&& other ) = default; | (1) | (since C++20) |
| owning_view& operator=( const owning_view& ) = delete; | (2) | (since C++20) |
|  |  |  |

1) Move assignment operator. Move assigns the stored range from that of other.2) Copy assignment operator is deleted. `owning_view` is move-only.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another `owning_view` to move from |

### Return value

\*this

## std::ranges::owning_view::base

|  |  |  |
| --- | --- | --- |
| constexpr R& base() & noexcept; | (1) | (since C++20) |
| constexpr const R& base() const & noexcept; | (2) | (since C++20) |
| constexpr R&& base() && noexcept; | (3) | (since C++20) |
| constexpr const R&& base() const && noexcept; | (4) | (since C++20) |
|  |  |  |

Returns a reference to the stored range, keeping value category and const-qualification.

1,2) Equivalent to return r_;.3,4) Equivalent to return std::move(r_);.

## std::ranges::owning_view::begin

|  |  |  |
| --- | --- | --- |
| constexpr ranges::iterator_t<R> begin(); | (1) | (since C++20) |
| constexpr auto begin() const requires ranges::range<const R>; | (2) | (since C++20) |
|  |  |  |

Equivalent to return ranges::begin(r_);.

## std::ranges::owning_view::end

|  |  |  |
| --- | --- | --- |
| constexpr ranges::sentinel_t<R> end(); | (1) | (since C++20) |
| constexpr auto end() const requires ranges::range<const R>; | (2) | (since C++20) |
|  |  |  |

Equivalent to return ranges::end(r_);.

## std::ranges::owning_view::empty

|  |  |  |
| --- | --- | --- |
| constexpr bool empty() requires requires { ranges::empty(r_); }; | (1) | (since C++20) |
| constexpr bool empty() const requires requires { ranges::empty(r_); }; | (2) | (since C++20) |
|  |  |  |

Equivalent to return ranges::empty(r_);.

## std::ranges::owning_view::size

|  |  |  |
| --- | --- | --- |
| constexpr auto size() requires ranges::sized_range<R>; | (1) | (since C++20) |
| constexpr auto size() const requires ranges::sized_range<const R>; | (2) | (since C++20) |
|  |  |  |

Equivalent to return ranges::size(r_);.

## std::ranges::owning_view::data

|  |  |  |
| --- | --- | --- |
| constexpr auto data() requires ranges::contiguous_range<R>; | (1) | (since C++20) |
| constexpr auto data() const requires ranges::contiguous_range<const R>; | (2) | (since C++20) |
|  |  |  |

Equivalent to return ranges::data(r_);.

### Helper templates

|  |  |  |
| --- | --- | --- |
| template< class T >  constexpr bool enable_borrowed_range<std::ranges::owning_view<T>> = ranges::enable_borrowed_range<T>; |  | (since C++20) |
|  |  |  |

This specialization of ranges::enable_borrowed_range makes `owning_view` satisfy `borrowed_range` when the underlying range satisfies it.

### Example

Run this code

```
#include <cassert>
#include <iostream>
#include <ranges>
#include <string>
 
int main()
{
    using namespace std::literals;
    std::ranges::owning_view ov{"cosmos"s}; // the deduced type of R is std::string;
                                            // `ov` is the only owner of this string
    assert(
        ov.empty() == false &&
        ov.size() == 6 &&
        ov.size() == ov.base().size() &&
        ov.front() == 'c' &&
        ov.front() == *ov.begin() &&
        ov.back() == 's' &&
        ov.back() == *(ov.end() - 1) &&
        ov.data() == ov.base()
    );
 
    std::cout << "sizeof(ov): " << sizeof ov << '\n' // typically equal to sizeof(R)
              << "range-for: ";
    for (const char ch : ov)
        std::cout << ch;
    std::cout << '\n';
 
    std::ranges::owning_view<std::string> ov2;
    assert(ov2.empty());
//  ov2 = ov; // compile-time error: copy assignment operator is deleted
    ov2 = std::move(ov); // OK
    assert(ov2.size() == 6);
}

```

Possible output:

```
sizeof(ov): 32
range-for: cosmos

```

### See also

|  |  |
| --- | --- |
| ranges::ref_view(C++20) | a `view` of the elements of some other `range`   (class template) |
| views::all_tviews::all(C++20) | a `view` that includes all elements of a `range` (alias template) (range adaptor object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/owning_view&oldid=172704>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 June 2024, at 23:23.