# std::ranges::split_view<V,Pattern>::**iterator**

From cppreference.com
< cpp‎ | ranges‎ | split view
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

std::ranges::split_view

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| split_view::split_view | | | | |
| split_view::base | | | | |
| split_view::begin | | | | |
| split_view::end | | | | |
| split_view::**find_next** | | | | |
| Nested classes | | | | |
| ****split_view::**iterator****** | | | | |
| split_view::**sentinel** | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| class /\*iterator\*/; |  | (since C++20)  (exposition only\*) |
|  |  |  |

The return type of split_view::begin. This is a `forward_iterator`, so it is expected that `V` models at least `forward_range`.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `iterator_concept` | std::forward_iterator_tag |
| `iterator_category` | std::input_iterator_tag |
| `value_type` | ranges::subrange<ranges::iterator_t<V>> |
| `difference_type` | ranges::range_difference_t<V> |

### Data members

|  |  |
| --- | --- |
| Member | Description |
| ranges::split_view<V, Pattern>\* `parent_` (private) | a pointer to the parent split_view object (exposition-only member object\*) |
| ranges::iterator_t<V> `cur_` (private) | an iterator into the underlying `view` that points to the begin of a current subrange (exposition-only member object\*) |
| ranges::subrange<ranges::iterator_t<V>> `next_` (private) | a subrange to the position of the pattern next to the current subrange (exposition-only member object\*) |
| bool `trailing_empty_` (private) | a flag that indicates whether an empty trailing subrange (if any) was reached (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor)(C++20) | constructs an iterator   (public member function) |
| base(C++20) | returns the underlying iterator   (public member function) |
| operator\*(C++20) | returns the current subrange   (public member function) |
| operator++operator++(int)(C++20) | advances the iterator   (public member function) |

## std::ranges::split_view::**iterator**::**iterator**

|  |  |  |
| --- | --- | --- |
| /\*iterator\*/() = default; | (1) | (since C++20) |
| constexpr /\*iterator\*/( split_view& parent, ranges::iterator_t<V> current,                          ranges::subrange<ranges::iterator_t<V>> next ); | (2) | (since C++20) |
|  |  |  |

1) Value-initializes non-static data members with their default member initializers, that is

- ranges::split_view\* parent_ = nullptr;,
- ranges::iterator_t<V> cur_ = ranges::iterator_t<V>();,
- ranges::subrange<ranges::iterator_t<V>> next_ = ranges::subrange<ranges::iterator_t<V>>();, and
- bool trailing_empty_ = false;.
2) Initializes non-static data members:

- ranges::split_view\* parent_ = std::addressof(parent);,
- ranges::iterator_t<V> cur_ = std::move(current);,
- ranges::subrange<ranges::iterator_t<V>> next_ = std::move(next);, and
- bool trailing_empty_ = false;.

## std::ranges::split_view::**iterator**::base

|  |  |  |
| --- | --- | --- |
| constexpr const ranges::iterator_t<V> base() const; |  | (since C++20) |
|  |  |  |

Equivalent to return cur_;.

## std::ranges::split_view::**iterator**::operator\*

|  |  |  |
| --- | --- | --- |
| constexpr value_type operator\*() const; |  | (since C++20) |
|  |  |  |

Equivalent to return {cur_, next_.begin()};.

## std::ranges::split_view::**iterator**::operator++

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/& operator++(); | (1) | (since C++20) |
| constexpr void operator++( int ); | (2) | (since C++20) |
|  |  |  |

1) Equivalent to  
cur_ = next_.begin();  

if (cur_ != ranges::end(parent_->base_))  
{  
    if (cur_ = next_.end(); cur_ == ranges::end(parent_->base_))  
    {  
        trailing_empty_ = true;  
        next_ = {cur_, cur_};  
    }  
    else  
        next_ = parent_->find_next(cur_);  
}  
else  
    trailing_empty_ = false;

return \*this;2) Equivalent to auto tmp = \*this; ++\*this; return tmp;.

### Non-member functions

|  |  |
| --- | --- |
| operator==(C++20) | compares the underlying iterators   (function) |

## operator==(std::ranges::split_view::**iterator**, std::ranges::split_view::**iterator**)

|  |  |  |
| --- | --- | --- |
| friend constexpr bool operator==( const /\*iterator\*/& x, const /\*iterator\*/& y ); |  | (since C++20) |
|  |  |  |

Equivalent to return x.cur_ == y.cur_ and x.trailing_empty_ == y.trailing_empty_;.

The `!=` operator is synthesized from `operator==`.

This function is not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when `std::ranges::split_view::iterator` is an associated class of the arguments.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/split_view/iterator&oldid=179947>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 January 2025, at 23:39.