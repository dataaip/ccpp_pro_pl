# std::void_t

From cppreference.com
< cpp‎ | types
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Type categories | | | | | | is_void(C++11) | | | | | | is_null_pointer(C++11)(DR\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_array(C++11) | | | | | | is_pointer(C++11) | | | | | | is_enum(C++11) | | | | | | is_union(C++11) | | | | | | is_class(C++11) | | | | | | is_function(C++11) | | | | | | is_reference(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_object(C++11) | | | | | | is_scalar(C++11) | | | | | | is_compound(C++11) | | | | | | is_integral(C++11) | | | | | | is_floating_point(C++11) | | | | | | is_fundamental(C++11) | | | | | | is_arithmetic(C++11) | | | | | | | is_lvalue_reference(C++11) | | | | | | is_rvalue_reference(C++11) | | | | | | is_member_pointer(C++11) | | | | | | is_member_object_pointer(C++11) | | | | | | is_member_function_pointer(C++11) | | | | | | Type properties | | | | | | is_const(C++11) | | | | | | is_volatile(C++11) | | | | | | is_empty(C++11) | | | | | | is_polymorphic(C++11) | | | | | | is_final(C++14) | | | | | | is_abstract(C++11) | | | | | | is_aggregate(C++17) | | | | | | is_implicit_lifetime(C++23) | | | | | | is_trivial(C++11)(deprecated in C++26) | | | | | | is_trivially_copyable(C++11) | | | | | | is_standard_layout(C++11) | | | | | | is_literal_type(C++11)(until C++20\*) | | | | | | is_pod(C++11)(deprecated in C++20) | | | | | | is_signed(C++11) | | | | | | is_unsigned(C++11) | | | | | | is_bounded_array(C++20) | | | | | | is_unbounded_array(C++20) | | | | | | is_scoped_enum(C++23) | | | | | | has_unique_object_representations(C++17) | | | | | | Type trait constants | | | | | | integral_constantbool_constanttrue_typefalse_type(C++11)(C++17)(C++11)(C++11) | | | | | | Metafunctions | | | | | | conjunction(C++17) | | | | | | disjunction(C++17) | | | | | | negation(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Supported operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_constructibleis_trivially_constructibleis_nothrow_constructible(C++11)(C++11)(C++11) | | | | | | is_default_constructibleis_trivially_default_constructibleis_nothrow_default_constructible(C++11)(C++11)(C++11) | | | | | | is_copy_constructibleis_trivially_copy_constructibleis_nothrow_copy_constructible(C++11)(C++11)(C++11) | | | | | | is_move_constructibleis_trivially_move_constructibleis_nothrow_move_constructible(C++11)(C++11)(C++11) | | | | | | is_assignableis_trivially_assignableis_nothrow_assignable(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_copy_assignableis_trivially_copy_assignableis_nothrow_copy_assignable(C++11)(C++11)(C++11) | | | | | | is_move_assignableis_trivially_move_assignableis_nothrow_move_assignable(C++11)(C++11)(C++11) | | | | | | is_destructibleis_trivially_destructibleis_nothrow_destructible(C++11)(C++11)(C++11) | | | | | | has_virtual_destructor(C++11) | | | | | | is_swappable_withis_swappableis_nothrow_swappable_withis_nothrow_swappable(C++17)(C++17)(C++17)(C++17) | | | | | |  | | | | | | | Relationships and property queries | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_same(C++11) | | | | | | is_convertibleis_nothrow_convertible(C++11)(C++20) | | | | | | is_layout_compatible(C++20) | | | | | | is_pointer_interconvertible_base_of(C++20) | | | | | | is_pointer_interconvertible_with_class(C++20) | | | | | | is_corresponding_member(C++20) | | | | | | reference_constructs_from_temporary(C++23) | | | | | | reference_converts_from_temporary(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_base_of(C++11) | | | | | | is_virtual_base_of(C++26) | | | | | | alignment_of(C++11) | | | | | | rank(C++11) | | | | | | extent(C++11) | | | | | | is_invocableis_invocable_ris_nothrow_invocableis_nothrow_invocable_r(C++17)(C++17)(C++17)(C++17) | | | | | | | Type modifications | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_cvremove_constremove_volatile(C++11)(C++11)(C++11) | | | | | | add_cvadd_constadd_volatile(C++11)(C++11)(C++11) | | | | | | make_signed(C++11) | | | | | | make_unsigned(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_reference(C++11) | | | | | | add_lvalue_referenceadd_rvalue_reference(C++11)(C++11) | | | | | | remove_pointer(C++11) | | | | | | add_pointer(C++11) | | | | | | remove_extent(C++11) | | | | | | remove_all_extents(C++11) | | | | | |  | | | | | | | Type transformations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | aligned_storage(C++11)(deprecated in C++23) | | | | | | aligned_union(C++11)(deprecated in C++23) | | | | | | decay(C++11) | | | | | | remove_cvref(C++20) | | | | | | result_ofinvoke_result(C++11)(until C++20\*)(C++17) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | conditional(C++11) | | | | | | common_type(C++11) | | | | | | common_reference(C++20) | | | | | | underlying_type(C++11) | | | | | | type_identity(C++20) | | | | | | enable_if(C++11) | | | | | | ****void_t****(C++17) | | | | | | |
| Compile-time rational arithmetic | | | | |
| Compile-time integer sequences | | | | |
| integer_sequence(C++14) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<type_traits>` |  |  |
| template< class... >  using void_t = void; |  | (since C++17) |
|  |  |  |

Utility metafunction that maps a sequence of any types to the type void. This metafunction is a convenient way to leverage SFINAE prior to C++20's concepts, in particular for conditionally removing functions from the candidate set based on whether an expression is valid in the unevaluated context (such as operand to decltype expression), allowing to exist separate function overloads or specializations based on supported operations.

### Notes

This metafunction is used in template metaprogramming to detect ill-formed types in SFINAE context:

```
// primary template handles types that have no nested ::type member:
template<class, class = void>
struct has_type_member : std::false_type {};
 
// specialization recognizes types that do have a nested ::type member:
template<class T>
struct has_type_member<T, std::void_t<typename T::type>> : std::true_type {};

```

It can also be used to detect validity of an expression:

```
// primary template handles types that do not support pre-increment:
template<class, class = void>
struct has_pre_increment_member : std::false_type {};
 
// specialization recognizes types that do support pre-increment:
template<class T>
struct has_pre_increment_member<T,
           std::void_t<decltype( ++std::declval<T&>() )>
       > : std::true_type {};

```

Until the resolution of CWG issue 1558 (a C++11 defect), unused parameters in alias templates were not guaranteed to ensure SFINAE and could be ignored, so earlier compilers require a more complex definition of `void_t`, such as

```
template<typename... Ts>
struct make_void { typedef void type; };
 
template<typename... Ts>
using void_t = typename make_void<Ts...>::type;

```

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_void_t` | `201411L` | (C++17) | `std::void_t` |

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <map>
#include <type_traits>
#include <vector>
 
// Variable template that checks if a type has begin() and end() member functions
template<typename, typename = void>
constexpr bool is_iterable = false;
 
template<typename T>
constexpr bool is_iterable<
    T,
    std::void_t<decltype(std::declval<T>().begin()),
                decltype(std::declval<T>().end())
    >
> = true;
 
// An iterator trait those value_type is the value_type of the iterated container,
// supports even back_insert_iterator (where value_type is void)
 
template<typename T, typename = void>
struct iterator_trait : std::iterator_traits<T> {};
 
template<typename T>
struct iterator_trait<T, std::void_t<typename T::container_type>>
    : std::iterator_traits<typename T::container_type::iterator> {};
 
class A {};
 
#define SHOW(...) std::cout << std::setw(34) << #__VA_ARGS__ \
                            << " == " << __VA_ARGS__ << '\n'
 
int main()
{
    std::cout << std::boolalpha << std::left;
    SHOW(is_iterable<std::vector<double>>);
    SHOW(is_iterable<std::map<int, double>>);
    SHOW(is_iterable<double>);
    SHOW(is_iterable<A>);
 
    using container_t = std::vector<int>;
    container_t v;
 
    static_assert(std::is_same_v<
        container_t::value_type,
        iterator_trait<decltype(std::begin(v))>::value_type
    >);
 
    static_assert(std::is_same_v<
        container_t::value_type,
        iterator_trait<decltype(std::back_inserter(v))>::value_type
    >);
}

```

Output:

```
is_iterable<std::vector<double>>   == true
is_iterable<std::map<int, double>> == true
is_iterable<double>                == false
is_iterable<A>                     == false

```

### See also

|  |  |
| --- | --- |
| enable_if(C++11) | conditionally removes a function overload or template specialization from overload resolution   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/types/void_t&oldid=170602>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 April 2024, at 03:55.