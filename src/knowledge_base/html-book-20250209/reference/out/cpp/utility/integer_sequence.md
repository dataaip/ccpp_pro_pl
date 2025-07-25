# std::integer_sequence

From cppreference.com
< cpp‎ | utility
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

Metaprogramming library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Type traits | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Type categories | | | | | | is_void(C++11) | | | | | | is_null_pointer(C++11)(DR\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_array(C++11) | | | | | | is_pointer(C++11) | | | | | | is_enum(C++11) | | | | | | is_union(C++11) | | | | | | is_class(C++11) | | | | | | is_function(C++11) | | | | | | is_reference(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_object(C++11) | | | | | | is_scalar(C++11) | | | | | | is_compound(C++11) | | | | | | is_integral(C++11) | | | | | | is_floating_point(C++11) | | | | | | is_fundamental(C++11) | | | | | | is_arithmetic(C++11) | | | | | | | is_lvalue_reference(C++11) | | | | | | is_rvalue_reference(C++11) | | | | | | is_member_pointer(C++11) | | | | | | is_member_object_pointer(C++11) | | | | | | is_member_function_pointer(C++11) | | | | | | Type properties | | | | | | is_const(C++11) | | | | | | is_volatile(C++11) | | | | | | is_empty(C++11) | | | | | | is_polymorphic(C++11) | | | | | | is_final(C++14) | | | | | | is_abstract(C++11) | | | | | | is_aggregate(C++17) | | | | | | is_implicit_lifetime(C++23) | | | | | | is_trivial(C++11)(deprecated in C++26) | | | | | | is_trivially_copyable(C++11) | | | | | | is_standard_layout(C++11) | | | | | | is_literal_type(C++11)(until C++20\*) | | | | | | is_pod(C++11)(deprecated in C++20) | | | | | | is_signed(C++11) | | | | | | is_unsigned(C++11) | | | | | | is_bounded_array(C++20) | | | | | | is_unbounded_array(C++20) | | | | | | is_scoped_enum(C++23) | | | | | | has_unique_object_representations(C++17) | | | | | | Type trait constants | | | | | | integral_constantbool_constanttrue_typefalse_type(C++11)(C++17)(C++11)(C++11) | | | | | | Metafunctions | | | | | | conjunction(C++17) | | | | | | disjunction(C++17) | | | | | | negation(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Supported operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_constructibleis_trivially_constructibleis_nothrow_constructible(C++11)(C++11)(C++11) | | | | | | is_default_constructibleis_trivially_default_constructibleis_nothrow_default_constructible(C++11)(C++11)(C++11) | | | | | | is_copy_constructibleis_trivially_copy_constructibleis_nothrow_copy_constructible(C++11)(C++11)(C++11) | | | | | | is_move_constructibleis_trivially_move_constructibleis_nothrow_move_constructible(C++11)(C++11)(C++11) | | | | | | is_assignableis_trivially_assignableis_nothrow_assignable(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_copy_assignableis_trivially_copy_assignableis_nothrow_copy_assignable(C++11)(C++11)(C++11) | | | | | | is_move_assignableis_trivially_move_assignableis_nothrow_move_assignable(C++11)(C++11)(C++11) | | | | | | is_destructibleis_trivially_destructibleis_nothrow_destructible(C++11)(C++11)(C++11) | | | | | | has_virtual_destructor(C++11) | | | | | | is_swappable_withis_swappableis_nothrow_swappable_withis_nothrow_swappable(C++17)(C++17)(C++17)(C++17) | | | | | |  | | | | | | | Relationships and property queries | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_same(C++11) | | | | | | is_convertibleis_nothrow_convertible(C++11)(C++20) | | | | | | is_layout_compatible(C++20) | | | | | | is_pointer_interconvertible_base_of(C++20) | | | | | | is_pointer_interconvertible_with_class(C++20) | | | | | | is_corresponding_member(C++20) | | | | | | reference_constructs_from_temporary(C++23) | | | | | | reference_converts_from_temporary(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_base_of(C++11) | | | | | | is_virtual_base_of(C++26) | | | | | | alignment_of(C++11) | | | | | | rank(C++11) | | | | | | extent(C++11) | | | | | | is_invocableis_invocable_ris_nothrow_invocableis_nothrow_invocable_r(C++17)(C++17)(C++17)(C++17) | | | | | | | Type modifications | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_cvremove_constremove_volatile(C++11)(C++11)(C++11) | | | | | | add_cvadd_constadd_volatile(C++11)(C++11)(C++11) | | | | | | make_signed(C++11) | | | | | | make_unsigned(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_reference(C++11) | | | | | | add_lvalue_referenceadd_rvalue_reference(C++11)(C++11) | | | | | | remove_pointer(C++11) | | | | | | add_pointer(C++11) | | | | | | remove_extent(C++11) | | | | | | remove_all_extents(C++11) | | | | | |  | | | | | | | Type transformations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | aligned_storage(C++11)(deprecated in C++23) | | | | | | aligned_union(C++11)(deprecated in C++23) | | | | | | decay(C++11) | | | | | | remove_cvref(C++20) | | | | | | result_ofinvoke_result(C++11)(until C++20\*)(C++17) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | conditional(C++11) | | | | | | common_type(C++11) | | | | | | common_reference(C++20) | | | | | | underlying_type(C++11) | | | | | | type_identity(C++20) | | | | | | enable_if(C++11) | | | | | | void_t(C++17) | | | | | | |
| Compile-time rational arithmetic | | | | |
| Compile-time integer sequences | | | | |
| ****integer_sequence****(C++14) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<utility>` |  |  |
| template< class T, T... Ints >  class integer_sequence; |  | (since C++14) |
|  |  |  |

The class template `std::integer_sequence` represents a compile-time sequence of integers. When used as an argument to a function template, the parameter pack `Ints` can be deduced and used in pack expansion.

### Template parameters

|  |  |  |
| --- | --- | --- |
| T | - | an integer type to use for the elements of the sequence |
| ...Ints | - | a non-type parameter pack representing the sequence |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `value_type` | `T` |

### Member functions

|  |  |
| --- | --- |
| ****size****[static] | returns the number of elements in `Ints`   (public static member function) |

## std::integer_sequence::size

|  |  |  |
| --- | --- | --- |
| static constexpr std::size_t size() noexcept; |  |  |
|  |  |  |

Returns the number of elements in `Ints`. Equivalent to sizeof...(Ints).

### Parameters

(none)

### Return value

The number of elements in `Ints`.

### Helper templates

A helper alias template `std::index_sequence` is defined for the common case where `T` is std::size_t:

|  |  |  |
| --- | --- | --- |
| template< std::size_t... Ints >  using index_sequence = std::integer_sequence<std::size_t, Ints...>; |  |  |
|  |  |  |

Helper alias templates `std::make_integer_sequence` and `std::make_index_sequence` are defined to simplify creation of `std::integer_sequence` and `std::index_sequence` types, respectively, with ​0​, 1, 2, `...`, N - 1 as `Ints`:

|  |  |  |
| --- | --- | --- |
| template< class T, T N >  using make_integer_sequence = std::integer_sequence<T, /\* a sequence 0, 1, 2, ..., N-1 \*/>; |  |  |
| template< std::size_t N >  using make_index_sequence = std::make_integer_sequence<std::size_t, N>; |  |  |
|  |  |  |

The program is ill-formed if `N` is negative. If `N` is zero, the indicated type is `integer_sequence<T>`.

A helper alias template `std::index_sequence_for` is defined to convert any type parameter pack into an index sequence of the same length:

|  |  |  |
| --- | --- | --- |
| template< class... T >  using index_sequence_for = std::make_index_sequence<sizeof...(T)>; |  |  |
|  |  |  |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_integer_sequence` | `201304L` | (C++14) | Compile-time integer sequences |

### Example

See also std::apply possible implementation for another example.

Run this code

```
#include <array>
#include <cstddef>
#include <iostream>
#include <tuple>
#include <utility>
 
namespace details {
template <typename Array, std::size_t... I>
constexpr auto array_to_tuple_impl(const Array& a, std::index_sequence<I...>)
{
    return std::make_tuple(a[I]...);
}
 
template <class Ch, class Tr, class Tuple, std::size_t... Is>
void print_tuple_impl(std::basic_ostream<Ch, Tr>& os,
                      const Tuple& t,
                      std::index_sequence<Is...>)
{
    ((os << (Is ? ", " : "") << std::get<Is>(t)), ...);
}
}
 
template <typename T, T... ints>
void print_sequence(int id, std::integer_sequence<T, ints...> int_seq)
{
    std::cout << id << ") The sequence of size " << int_seq.size() << ": ";
    ((std::cout << ints << ' '), ...);
    std::cout << '\n';
}
 
template <typename T, std::size_t N, typename Indx = std::make_index_sequence<N>>
constexpr auto array_to_tuple(const std::array<T, N>& a)
{
    return details::array_to_tuple_impl(a, Indx{});
}
 
template <class Ch, class Tr, class... Args>
auto& operator<<(std::basic_ostream<Ch, Tr>& os, const std::tuple<Args...>& t)
{
    os << '(';
    details::print_tuple_impl(os, t, std::index_sequence_for<Args...>{});
    return os << ')';
}
 
int main()
{
    print_sequence(1, std::integer_sequence<unsigned, 9, 2, 5, 1, 9, 1, 6>{});
    print_sequence(2, std::make_integer_sequence<int, 12>{});
    print_sequence(3, std::make_index_sequence<10>{});
    print_sequence(4, std::index_sequence_for<std::ios, float, signed>{});
 
    constexpr std::array<int, 4> array{1, 2, 3, 4};
 
    auto tuple1 = array_to_tuple(array);
    static_assert(std::is_same_v<decltype(tuple1),
                                 std::tuple<int, int, int, int>>, "");
    std::cout << "5) tuple1: " << tuple1 << '\n';
 
    constexpr auto tuple2 = array_to_tuple<int, 4,
        std::integer_sequence<std::size_t, 1, 0, 3, 2>>(array);
    std::cout << "6) tuple2: " << tuple2 << '\n';
}

```

Output:

```
1) The sequence of size 7: 9 2 5 1 9 1 6 
2) The sequence of size 12: 0 1 2 3 4 5 6 7 8 9 10 11 
3) The sequence of size 10: 0 1 2 3 4 5 6 7 8 9 
4) The sequence of size 3: 0 1 2 
5) tuple1: (1, 2, 3, 4)
6) tuple2: (2, 1, 4, 3)

```

### See also

|  |  |
| --- | --- |
| to_array(C++20) | creates a `std::array` object from a built-in array   (function template) |
| integral_constantbool_constant(C++11)(C++17) | compile-time constant of specified type with specified value   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/integer_sequence&oldid=173649>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 July 2024, at 05:38.