# std::size, std::ssize

From cppreference.com
< cpp‎ | iterator
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

Iterator library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Iterator concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_readable(C++20) | | | | | | indirectly_writable(C++20) | | | | | | weakly_incrementable(C++20) | | | | | | incrementable(C++20) | | | | | | **is-integer-like** **is-signed-integer-like**(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sentinel_for(C++20) | | | | | | sized_sentinel_for(C++20) | | | | | | input_iterator(C++20) | | | | | | output_iterator(C++20) | | | | | | input_or_output_iterator(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_iterator(C++20) | | | | | | bidirectional_iterator(C++20) | | | | | | random_access_iterator(C++20) | | | | | | contiguous_iterator(C++20) | | | | | |  | | | | | |  | | | | | |
| Iterator primitives | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | input_iterator_tagoutput_iterator_tagforward_iterator_tagbidirectional_iterator_tagrandom_access_iterator_tagcontiguous_iterator_tag(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iter_value_titer_difference_titer_reference_titer_const_reference_titer_rvalue_reference_titer_common_reference_t(C++20)(C++20)(C++20)(C++23)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iterator(deprecated in C++17) | | | | | | iterator_traits | | | | | | incrementable_traits(C++20) | | | | | | indirectly_readable_traits(C++20) | | | | | |  | | | | | |  | | | | | |
| Algorithm concepts and utilities | | | | |
| Indirect callable concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_unary_invocableindirectly_regular_unary_invocable(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_unary_predicate(C++20) | | | | | | indirect_binary_predicate(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_equivalence_relation(C++20) | | | | | | indirect_strict_weak_order(C++20) | | | | | |
| Common algorithm requirements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_movable(C++20) | | | | | | indirectly_movable_storable(C++20) | | | | | | indirectly_copyable(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_copyable_storable(C++20) | | | | | | indirectly_swappable(C++20) | | | | | | indirectly_comparable(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | permutable(C++20) | | | | | | mergeable(C++20) | | | | | | sortable(C++20) | | | | | |
| Utilities | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_result_t(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | projected(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | projected_value_t(C++26) | | | | | |
| Iterator adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_iterator | | | | | | make_reverse_iterator(C++14) | | | | | | move_iterator(C++11) | | | | | | make_move_iterator(C++11) | | | | | | default_sentinel_tdefault_sentinel(C++20)(C++20) | | | | | | unreachable_sentinel_tunreachable_sentinel(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | front_insert_iterator | | | | | | back_insert_iterator | | | | | | inserter | | | | | | insert_iterator | | | | | | front_inserter | | | | | | back_inserter | | | | | | move_sentinel(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_iterator(C++20) | | | | | | counted_iterator(C++20) | | | | | | basic_const_iterator(C++23) | | | | | | const_iterator(C++23) | | | | | | const_sentinel(C++23) | | | | | | make_const_iterator(C++23) | | | | | | make_const_sentinel(C++23) | | | | | |  | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Stream iterators | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istream_iterator | | | | | | ostream_iterator | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istreambuf_iterator | | | | | | ostreambuf_iterator | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator customization points | | | | | | ranges::iter_move(C++20) | | | | | | ranges::iter_swap(C++20) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator operations | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | advance | | | | | | distance | | | | | | prev(C++11) | | | | | | next(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ranges::advance(C++20) | | | | | | ranges::distance(C++20) | | | | | | ranges::prev(C++20) | | | | | | ranges::next(C++20) | | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | begincbegin(C++11)(C++14) | | | | | | rbegincrbegin(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | endcend(C++11)(C++14) | | | | | | rendcrend(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****sizessize****(C++17)(C++20) | | | | | | empty(C++17) | | | | | | data(C++17) | | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<array>` |  |  |
| Defined in header `<deque>` |  |  |
| Defined in header `<flat_map>` |  |  |
| Defined in header `<flat_set>` |  |  |
| Defined in header `<forward_list>` |  |  |
| Defined in header `<inplace_vector>` |  |  |
| Defined in header `<iterator>` |  |  |
| Defined in header `<list>` |  |  |
| Defined in header `<map>` |  |  |
| Defined in header `<regex>` |  |  |
| Defined in header `<set>` |  |  |
| Defined in header `<span>` |  |  |
| Defined in header `<string>` |  |  |
| Defined in header `<string_view>` |  |  |
| Defined in header `<unordered_map>` |  |  |
| Defined in header `<unordered_set>` |  |  |
| Defined in header `<vector>` |  |  |
| template< class C >  constexpr auto size( const C& c ) -> decltype(c.size()); | (1) | (since C++17) |
| template< class C >  constexpr auto ssize( const C& c )      -> std::common_type_t<std::ptrdiff_t, std::make_signed_t<decltype(c.size())>>; | (2) | (since C++20) |
| template< class T, std::size_t N >  constexpr std::size_t size( const T (&array)[N] ) noexcept; | (3) | (since C++17) |
| template< class T, std::ptrdiff_t N >  constexpr std::ptrdiff_t ssize( const T (&array)[N] ) noexcept; | (4) | (since C++20) |
|  |  |  |

Returns the size of the given range.

1,2) Returns c.size(), converted to the return type if necessary.3,4) Returns N.

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | a container or view with a `size` member function |
| array | - | an array of arbitrary type |

### Return value

1) c.size()2) static_cast<std::common_type_t<std::ptrdiff_t,  
                               std::make_signed_t<decltype(c.size())>>>(c.size())3,4) N

### Exceptions

1,2) May throw implementation-defined exceptions.

### Overloads

Custom overloads of `size` may be provided for classes and enumerations that do not expose a suitable `size()` member function, yet can be detected.

|  |  |
| --- | --- |
| Overloads of `size` found by argument-dependent lookup can be used to customize the behavior of std::ranges::size, std::ranges::ssize, and std::ranges::empty. | (since C++20) |

### Possible implementation

| size (1) |
| --- |
| ```text template<class C> constexpr auto size(const C& c) -> decltype(c.size()) {     return c.size(); } ``` |
| ssize (2) |
| ```text template<class C> constexpr auto ssize(const C& c)     -> std::common_type_t<std::ptrdiff_t,                           std::make_signed_t<decltype(c.size())>> {     using R = std::common_type_t<std::ptrdiff_t,                                  std::make_signed_t<decltype(c.size())>>;     return static_cast<R>(c.size()); } ``` |
| size (3) |
| ```text template<class T, std::size_t N> constexpr std::size_t size(const T (&array)[N]) noexcept {     return N; } ``` |
| ssize (4) |
| ```text template<class T, std::ptrdiff_t N> constexpr std::ptrdiff_t ssize(const T (&array)[N]) noexcept {     return N; } ``` |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_nonmember_container_access` | `201411L` | (C++17) | `std::size()`, std::data and std::empty |
| `__cpp_lib_ssize` | `201902L` | (C++20) | `std::ssize()` (2,4) and unsigned std::span::size() |

### Example

Run this code

```
#include <cassert>
#include <cstring>
#include <iostream>
#include <vector>
 
int main()
{
    // Works with containers
    std::vector<int> v{3, 1, 4};
    assert(std::size(v) == 3);
 
    // And works with built-in arrays too
    int a[]{-5, 10, 15};
    // Returns the number of elements (not bytes) as opposed to sizeof
    assert(std::size(a) == 3);
    std::cout << "size of a[]: " << sizeof a << '\n'; // 12, if sizeof(int) == 4
 
    // Provides a safe way (compared to sizeof) of getting string buffer size
    const char str[] = "12345";
    // These are fine and give the correct result
    assert(std::size(str) == 6);
    assert(sizeof(str) == 6);
 
    // But use of sizeof here is a common source of bugs
    const char* str_decayed = "12345";
    // std::cout << std::size(str_decayed) << '\n'; // Usefully fails to compile
    std::cout << sizeof(str_decayed) << '\n'; // Prints the size of the pointer!
 
    // Since C++20 the signed size (std::ssize) is available
    auto i = std::ssize(v);
    for (--i; i != -1; --i)
        std::cout << v[i] << (i ? ' ' : '\n');
    assert(i == -1);
 
    // Note that the string literal includes the ending null character, which
    // will be part of the constructed characters array. This makes std::size
    // behave differently from std::strlen and std::string::size:
    constexpr char symbols[] = "0123456789";
 
    static_assert(std::size(symbols) == 11);
    static_assert(std::string(symbols).size() == 10);
    assert(std::strlen(symbols) == 10);
}

```

Possible output:

```
size of a[]: 12
8
4 1 3

```

### See also

|  |  |
| --- | --- |
| ptrdiff_t | signed integer type returned when subtracting two pointers   (typedef) |
| size_t | unsigned integer type returned by the sizeof operator   (typedef) |
| ranges::size(C++20) | returns an integer equal to the size of a range (customization point object) |
| ranges::ssize(C++20) | returns a signed integer equal to the size of a range (customization point object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator/size&oldid=177485>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 November 2024, at 22:02.