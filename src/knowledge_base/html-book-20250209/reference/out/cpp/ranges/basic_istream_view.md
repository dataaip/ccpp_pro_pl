# std::ranges::views::istream, std::ranges::basic_istream_view, std::ranges::istream_view, std::ranges::wistream_view

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty_viewviews::empty | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | single_viewviews::single | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****basic_istream_viewviews::istream**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota_viewviews::iota | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | repeat_viewviews::repeat(C++23)(C++23) | | | | | |

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

****std::ranges::basic_istream_view****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| basic_istream_view::basic_istream_view | | | | |
| basic_istream_view::begin | | | | |
| basic_istream_view::end | | | | |
| Iterator | | | | |
| basic_istream_view::**iterator**::**iterator** | | | | |
| basic_istream_view::**iterator**::operator= | | | | |
| basic_istream_view::**iterator**::operator++ | | | | |
| basic_istream_view::**iterator**::operator\* | | | | |
| operator==(basic_istream_view::**iterator**) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template< std::movable Val, class CharT,  class Traits = std::char_traits<CharT> >      requires std::default_initializable<Val> &&               /\*stream-extractable\*/<Val, CharT, Traits>  class basic_istream_view : public ranges::view_interface<basic_istream_view<Val, CharT, Traits>> | (1) | (since C++20) |
| Helper templates |  |  |
| template< class Val >  using istream_view = ranges::basic_istream_view<Val, char>; | (2) | (since C++20) |
| template< class Val >  using wistream_view = ranges::basic_istream_view<Val, wchar_t>; | (3) | (since C++20) |
| Customization point objects |  |  |
| namespace views {  template< class T >      constexpr /\* unspecified \*/ istream = /\* unspecified \*/; } | (4) | (since C++20) |
| Helper concepts |  |  |
| template< class Val, class CharT, class Traits >  concept /\*stream-extractable\*/ =      requires(std::basic_istream<CharT, Traits>& is, Val& t) {          is >> t; }; | (5) | (exposition only\*) |
|  |  |  |

1) A range factory that generates a sequence of elements by repeatedly calling operator>>.2,3) Convenience alias templates for character types char and wchar_t.4) views::istream<T>(e) is expression-equivalent to ranges::basic_istream_view<T, typename U::char_type, typename U::traits_type>(e) for any suitable subexpressions e, where `U` is std::remove_reference_t<decltype(e)>. The program is ill-formed if `U` is not both publicly and unambiguously derived from std::basic_istream<typename U::char_type, typename U::traits_type>, which may result in a substitution failure.5) The exposition-only concept /\*stream-extractable\*/<Val, CharT, Traits> is satisfied when lvalue of type `Val` can be extracted from lvalue of type std::basic_istream<CharT, Traits>.

The iterator type of `basic_istream_view` is move-only: it does not meet the LegacyIterator requirements, and thus does not work with pre-C++20 algorithms.

### Customization point objects

The name `views::istream<T>` denotes a **customization point object**, which is a const function object of a literal `semiregular` class type. For exposition purposes, the cv-unqualified version of its type is denoted as `__istream_fn<T>`.

All instances of `__istream_fn<T>` are equal. The effects of invoking different instances of type `__istream_fn<T>` on the same arguments are equivalent, regardless of whether the expression denoting the instance is an lvalue or rvalue, and is const-qualified or not (however, a volatile-qualified instance is not required to be invocable). Thus, `views::istream<T>` can be copied freely and its copies can be used interchangeably.

Given a set of types `Args...`, if std::declval<Args>()... meet the requirements for arguments to `views::istream<T>` above, `__istream_fn<T>` models

- std::invocable<__istream_fn<T>, Args...>,
- std::invocable<const __istream_fn<T>, Args...>,
- std::invocable<__istream_fn<T>&, Args...>, and
- std::invocable<const __istream_fn<T>&, Args...>.

Otherwise, no function call operator of `__istream_fn<T>` participates in overload resolution.

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| std::basic_istream<CharT, Traits>\* `stream_` | a pointer to the input stream (exposition-only member object\*) |
| `Val` `value_` | the stored value (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `basic_istream_view`   (public member function) |
| begin | returns an iterator   (public member function) |
| end | returns std::default_sentinel   (public member function) |
| Inherited from std::ranges::view_interface | |
| cbegin(C++23) | returns a constant iterator to the beginning of the range.   (public member function of `std::ranges::view_interface<D>`) |
| cend(C++23) | returns a sentinel for the constant iterator of the range.   (public member function of `std::ranges::view_interface<D>`) |

|  |  |
| --- | --- |
| Although `basic_istream_view` is derived from std::ranges::view_interface, it cannot use any of inherited member functions. | (until C++23) |

## std::ranges::basic_istream_view::basic_istream_view

|  |  |  |
| --- | --- | --- |
| constexpr explicit      basic_istream_view( std::basic_istream<CharT, Traits>& stream ); |  | (since C++20) |
|  |  |  |

Initializes `stream_` with std::addressof(stream), and value-initializes `value_` ﻿.

## std::ranges::basic_istream_view::begin

|  |  |  |
| --- | --- | --- |
| constexpr auto begin(); |  | (since C++20) |
|  |  |  |

Equivalent to \*`stream_`>>`value_` ﻿; return`iterator` ﻿{\*this};.

## std::ranges::basic_istream_view::end

|  |  |  |
| --- | --- | --- |
| constexpr std::default_sentinel_t end() const noexcept; |  | (since C++20) |
|  |  |  |

Returns std::default_sentinel.

### Nested classes

|  |  |
| --- | --- |
| **iterator** | the iterator type of `basic_istream_view` (exposition-only member class\*) |

### Example

Run this code

```
#include <algorithm>
#include <iomanip>
#include <iostream>
#include <iterator>
#include <ranges>
#include <sstream>
#include <string>
 
int main()
{
    auto words = std::istringstream{"today is yesterday’s tomorrow"};
    for (const auto& s : std::views::istream<std::string>(words))
        std::cout << std::quoted(s, '/') << ' ';
    std::cout << '\n';
 
    auto floats = std::istringstream{"1.1  2.2\t3.3\v4.4\f55\n66\r7.7  8.8"};
    std::ranges::copy
    (
        std::views::istream<float>(floats),
        std::ostream_iterator<float>{std::cout, ", "}
    );
    std::cout << '\n';
}

```

Output:

```
/today/ /is/ /yesterday’s/ /tomorrow/
1.1, 2.2, 3.3, 4.4, 55, 66, 7.7, 8.8,

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3568 | C++20 | P2325R3 accidentally made the stored value default-initialized | restored to value-initialization |
| P2325R3 | C++20 | default constructor was provided as `view` must be `default_initializable` | removed along with the requirement |
| P2432R1 | C++20 | `ranges::istream_view` was a function template and did not follow the naming convention | made an alias template; customization point objects added |

### See also

|  |  |
| --- | --- |
| istream_iterator | input iterator that reads from std::basic_istream   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/basic_istream_view&oldid=176950>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 October 2024, at 19:09.