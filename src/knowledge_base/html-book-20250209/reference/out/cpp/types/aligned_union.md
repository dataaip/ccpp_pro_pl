# std::aligned_union

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Type categories | | | | | | is_void(C++11) | | | | | | is_null_pointer(C++11)(DR\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_array(C++11) | | | | | | is_pointer(C++11) | | | | | | is_enum(C++11) | | | | | | is_union(C++11) | | | | | | is_class(C++11) | | | | | | is_function(C++11) | | | | | | is_reference(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_object(C++11) | | | | | | is_scalar(C++11) | | | | | | is_compound(C++11) | | | | | | is_integral(C++11) | | | | | | is_floating_point(C++11) | | | | | | is_fundamental(C++11) | | | | | | is_arithmetic(C++11) | | | | | | | is_lvalue_reference(C++11) | | | | | | is_rvalue_reference(C++11) | | | | | | is_member_pointer(C++11) | | | | | | is_member_object_pointer(C++11) | | | | | | is_member_function_pointer(C++11) | | | | | | Type properties | | | | | | is_const(C++11) | | | | | | is_volatile(C++11) | | | | | | is_empty(C++11) | | | | | | is_polymorphic(C++11) | | | | | | is_final(C++14) | | | | | | is_abstract(C++11) | | | | | | is_aggregate(C++17) | | | | | | is_implicit_lifetime(C++23) | | | | | | is_trivial(C++11)(deprecated in C++26) | | | | | | is_trivially_copyable(C++11) | | | | | | is_standard_layout(C++11) | | | | | | is_literal_type(C++11)(until C++20\*) | | | | | | is_pod(C++11)(deprecated in C++20) | | | | | | is_signed(C++11) | | | | | | is_unsigned(C++11) | | | | | | is_bounded_array(C++20) | | | | | | is_unbounded_array(C++20) | | | | | | is_scoped_enum(C++23) | | | | | | has_unique_object_representations(C++17) | | | | | | Type trait constants | | | | | | integral_constantbool_constanttrue_typefalse_type(C++11)(C++17)(C++11)(C++11) | | | | | | Metafunctions | | | | | | conjunction(C++17) | | | | | | disjunction(C++17) | | | | | | negation(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Supported operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_constructibleis_trivially_constructibleis_nothrow_constructible(C++11)(C++11)(C++11) | | | | | | is_default_constructibleis_trivially_default_constructibleis_nothrow_default_constructible(C++11)(C++11)(C++11) | | | | | | is_copy_constructibleis_trivially_copy_constructibleis_nothrow_copy_constructible(C++11)(C++11)(C++11) | | | | | | is_move_constructibleis_trivially_move_constructibleis_nothrow_move_constructible(C++11)(C++11)(C++11) | | | | | | is_assignableis_trivially_assignableis_nothrow_assignable(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_copy_assignableis_trivially_copy_assignableis_nothrow_copy_assignable(C++11)(C++11)(C++11) | | | | | | is_move_assignableis_trivially_move_assignableis_nothrow_move_assignable(C++11)(C++11)(C++11) | | | | | | is_destructibleis_trivially_destructibleis_nothrow_destructible(C++11)(C++11)(C++11) | | | | | | has_virtual_destructor(C++11) | | | | | | is_swappable_withis_swappableis_nothrow_swappable_withis_nothrow_swappable(C++17)(C++17)(C++17)(C++17) | | | | | |  | | | | | | | Relationships and property queries | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_same(C++11) | | | | | | is_convertibleis_nothrow_convertible(C++11)(C++20) | | | | | | is_layout_compatible(C++20) | | | | | | is_pointer_interconvertible_base_of(C++20) | | | | | | is_pointer_interconvertible_with_class(C++20) | | | | | | is_corresponding_member(C++20) | | | | | | reference_constructs_from_temporary(C++23) | | | | | | reference_converts_from_temporary(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_base_of(C++11) | | | | | | is_virtual_base_of(C++26) | | | | | | alignment_of(C++11) | | | | | | rank(C++11) | | | | | | extent(C++11) | | | | | | is_invocableis_invocable_ris_nothrow_invocableis_nothrow_invocable_r(C++17)(C++17)(C++17)(C++17) | | | | | | | Type modifications | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_cvremove_constremove_volatile(C++11)(C++11)(C++11) | | | | | | add_cvadd_constadd_volatile(C++11)(C++11)(C++11) | | | | | | make_signed(C++11) | | | | | | make_unsigned(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_reference(C++11) | | | | | | add_lvalue_referenceadd_rvalue_reference(C++11)(C++11) | | | | | | remove_pointer(C++11) | | | | | | add_pointer(C++11) | | | | | | remove_extent(C++11) | | | | | | remove_all_extents(C++11) | | | | | |  | | | | | | | Type transformations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | aligned_storage(C++11)(deprecated in C++23) | | | | | | ****aligned_union****(C++11)(deprecated in C++23) | | | | | | decay(C++11) | | | | | | remove_cvref(C++20) | | | | | | result_ofinvoke_result(C++11)(until C++20\*)(C++17) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | conditional(C++11) | | | | | | common_type(C++11) | | | | | | common_reference(C++20) | | | | | | underlying_type(C++11) | | | | | | type_identity(C++20) | | | | | | enable_if(C++11) | | | | | | void_t(C++17) | | | | | | |
| Compile-time rational arithmetic | | | | |
| Compile-time integer sequences | | | | |
| integer_sequence(C++14) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<type_traits>` |  |  |
| template< std::size_t Len, class... Types >  struct aligned_union; |  | (since C++11)  (deprecated in C++23) |
|  |  |  |

Provides the nested type `type`, which is a trivial standard-layout type of a size and alignment suitable for use as uninitialized storage for an object of any of the types listed in `Types`. The size of the storage is at least `Len`. `std::aligned_union` also determines the strictest (largest) alignment requirement among all `Types` and makes it available as the constant `alignment_value`.

If sizeof...(Types) == 0 or if any of the types in `Types` is not a complete object type, the behavior is undefined.

It is implementation-defined whether any extended alignment is supported.

If the program adds specializations for `std::aligned_union`, the behavior is undefined.

### Member types

|  |  |
| --- | --- |
| Name | Definition |
| `type` | a trivial and standard-layout type suitable for storage of any type from `Types` |

### Helper types

|  |  |  |
| --- | --- | --- |
| template< std::size_t Len, class... Types >  using aligned_union_t = typename aligned_union<Len,Types...>::type; |  | (since C++14)  (deprecated in C++23) |
|  |  |  |

### Member constants

|  |  |
| --- | --- |
| alignment_value[static] | the strictest alignment requirement of all `Types`   (public static member constant) |

### Possible implementation

|  |
| --- |
| ```text #include <algorithm>   template<std::size_t Len, class... Types> struct aligned_union {     static constexpr std::size_t alignment_value = std::max({alignof(Types)...});       struct type     {         alignas(alignment_value) char _s[std::max({Len, sizeof(Types)...})];     }; }; ``` |

### Example

Run this code

```
#include <iostream>
#include <string>
#include <type_traits>
 
int main()
{
    std::cout << sizeof(std::aligned_union_t<0, char>) << ' ' // 1
              << sizeof(std::aligned_union_t<2, char>) << ' ' // 2
              << sizeof(std::aligned_union_t<2, char[3]>) << ' ' // 3 (!)
              << sizeof(std::aligned_union_t<3, char[4]>) << ' ' // 4
              << sizeof(std::aligned_union_t<1, char, int, double>) << ' '    // 8
              << sizeof(std::aligned_union_t<12, char, int, double>) << '\n'; // 16 (!)
 
    using var_t = std::aligned_union<16, int, std::string>;
 
    std::cout << "var_t::alignment_value = " << var_t::alignment_value << '\n'
              << "sizeof(var_t::type) = " << sizeof(var_t::type) << '\n';
 
    var_t::type aligned_storage;
    int* int_ptr = new(&aligned_storage) int(42); // placement new
    std::cout << "*int_ptr = " << *int_ptr << '\n';
 
    std::string* string_ptr = new(&aligned_storage) std::string("bar");
    std::cout << "*string_ptr = " << *string_ptr << '\n';
    *string_ptr = "baz";
    std::cout << "*string_ptr = " << *string_ptr << '\n';
    string_ptr->~basic_string();
}

```

Possible output:

```
1 2 3 4 8 16
var_t::alignment_value = 8
sizeof(var_t::type) = 32
*int_ptr = 42
*string_ptr = bar
*string_ptr = baz

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2979 | C++11 | complete type was not required | requires complete types |

### See also

|  |  |
| --- | --- |
| alignment_of(C++11) | obtains the type's alignment requirements   (class template) |
| aligned_storage(since C++11)(deprecated in C++23) | defines the type suitable for use as uninitialized storage for types of given size   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/types/aligned_union&oldid=155465>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 July 2023, at 01:46.