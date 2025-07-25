# Library feature-test macros (since C++20)

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

Utilities library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | ****Library feature-test macros**** (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

Each of following macros is defined if the header <version> or one of the corresponding headers specified in the table is included.

| Macro name | Value | Header | Free- standing |
| --- | --- | --- | --- |
| `__cpp_lib_adaptor_iterator_pair_constructor` | 202106L | <stack> <queue> |  |
| `__cpp_lib_addressof_constexpr` | 201603L | <memory> | Yes |
| `__cpp_lib_algorithm_default_value_type` | 202403L | <algorithm> <ranges> <string> <deque> <list> <forward_list> <vector> |  |
| `__cpp_lib_algorithm_iterator_requirements` | 202207L | <algorithm> <numeric> <memory> |  |
| `__cpp_lib_aligned_accessor` | 202411L | <mdspan> |  |
| `__cpp_lib_allocate_at_least` | 202302L | <memory> |  |
| `__cpp_lib_allocator_traits_is_always_equal` | 201411L | <memory> <scoped_allocator> <string> <deque> <forward_list> <list> <vector> <map> <set> <unordered_map> <unordered_set> | Yes |
| `__cpp_lib_any` | 201606L | <any> |  |
| `__cpp_lib_apply` | 201603L | <tuple> | Yes |
| `__cpp_lib_array_constexpr` | 201811L | <iterator> <array> |  |
| `__cpp_lib_as_const` | 201510L | <utility> | Yes |
| `__cpp_lib_associative_heterogeneous_erasure` | 202110L | <map> <set> <unordered_map> <unordered_set> |  |
| `__cpp_lib_associative_heterogeneous_insertion` | 202306L | <map> <set> <unordered_map> <unordered_set> |  |
| `__cpp_lib_assume_aligned` | 201811L | <memory> | Yes |
| `__cpp_lib_atomic_flag_test` | 201907L | <atomic> | Yes |
| `__cpp_lib_atomic_float` | 201711L | <atomic> | Yes |
| `__cpp_lib_atomic_is_always_lock_free` | 201603L | <atomic> | Yes |
| `__cpp_lib_atomic_lock_free_type_aliases` | 201907L | <atomic> |  |
| `__cpp_lib_atomic_min_max` | 202403L | <atomic> | Yes |
| `__cpp_lib_atomic_ref` | 202411L | <atomic> | Yes |
| `__cpp_lib_atomic_shared_ptr` | 201711L | <memory> |  |
| `__cpp_lib_atomic_value_initialization` | 201911L | <atomic> <memory> | Yes |
| `__cpp_lib_atomic_wait` | 201907L | <atomic> | Yes |
| `__cpp_lib_barrier` | 202302L | <barrier> |  |
| `__cpp_lib_bind_back` | 202306L | <functional> | Yes |
| `__cpp_lib_bind_front` | 202306L | <functional> | Yes |
| `__cpp_lib_bit_cast` | 201806L | <bit> | Yes |
| `__cpp_lib_bitops` | 201907L | <bit> | Yes |
| `__cpp_lib_bitset` | 202306L | <bitset> |  |
| `__cpp_lib_bool_constant` | 201505L | <type_traits> | Yes |
| `__cpp_lib_bounded_array_traits` | 201902L | <type_traits> | Yes |
| `__cpp_lib_boyer_moore_searcher` | 201603L | <functional> |  |
| `__cpp_lib_byte` | 201603L | <cstddef> | Yes |
| `__cpp_lib_byteswap` | 202110L | <bit> | Yes |
| `__cpp_lib_char8_t` | 201907L | <atomic> <filesystem> <istream> <limits> <locale> <ostream> <string> <string_view> | Yes |
| `__cpp_lib_chrono` | 202306L | <chrono> |  |
| `__cpp_lib_chrono_udls` | 201304L | <chrono> |  |
| `__cpp_lib_clamp` | 201603L | <algorithm> |  |
| `__cpp_lib_common_reference` | 202302L | <type_traits> | Yes |
| `__cpp_lib_common_reference_wrapper` | 202302L | <functional> | Yes |
| `__cpp_lib_complex_udls` | 201309L | <complex> |  |
| `__cpp_lib_concepts` | 202207L | <concepts> <compare> | Yes |
| `__cpp_lib_constexpr_algorithms` | 202306L | <algorithm> <utility> |  |
| `__cpp_lib_constexpr_atomic` | 202411L | <atomic> |  |
| `__cpp_lib_constexpr_bitset` | 202207L | <bitset> |  |
| `__cpp_lib_constexpr_charconv` | 202207L | <charconv> | Yes |
| `__cpp_lib_constexpr_cmath` | 202306L | <cmath> <cstdlib> |  |
| `__cpp_lib_constexpr_complex` | 202306L | <complex> |  |
| `__cpp_lib_constexpr_dynamic_alloc` | 201907L | <memory> |  |
| `__cpp_lib_constexpr_exceptions` | 202411L | <exception> |  |
| `__cpp_lib_constexpr_functional` | 201907L | <functional> | Yes |
| `__cpp_lib_constexpr_iterator` | 201811L | <iterator> | Yes |
| `__cpp_lib_constexpr_memory` | 202202L | <memory> | Yes |
| `__cpp_lib_constexpr_new` | 202406L | <new> | Yes |
| `__cpp_lib_constexpr_numeric` | 201911L | <numeric> |  |
| `__cpp_lib_constexpr_string` | 201907L | <string> |  |
| `__cpp_lib_constexpr_string_view` | 201811L | <string_view> |  |
| `__cpp_lib_constexpr_tuple` | 201811L | <tuple> | Yes |
| `__cpp_lib_constexpr_typeinfo` | 202106L | <typeinfo> | Yes |
| `__cpp_lib_constexpr_utility` | 201811L | <utility> | Yes |
| `__cpp_lib_constexpr_vector` | 201907L | <vector> |  |
| `__cpp_lib_constrained_equality` | 202411L | <utility> <tuple> <optional> <variant> <expected> | Yes |
| `__cpp_lib_containers_ranges` | 202202L | <vector> <list> <forward_list> <map> <set> <unordered_map> <unordered_set> <deque> <queue> <stack> <string> |  |
| `__cpp_lib_copyable_function` | 202306L | <functional> |  |
| `__cpp_lib_coroutine` | 201902L | <coroutine> | Yes |
| `__cpp_lib_debugging` | 202403L | <debugging> | Yes |
| `__cpp_lib_destroying_delete` | 201806L | <new> | Yes |
| `__cpp_lib_enable_shared_from_this` | 201603L | <memory> |  |
| `__cpp_lib_endian` | 201907L | <bit> | Yes |
| `__cpp_lib_erase_if` | 202002L | <string> <deque> <forward_list> <list> <vector> <map> <set> <unordered_map> <unordered_set> |  |
| `__cpp_lib_exchange_function` | 201304L | <utility> | Yes |
| `__cpp_lib_execution` | 201902L | <execution> |  |
| `__cpp_lib_expected` | 202211L | <expected> |  |
| `__cpp_lib_filesystem` | 201703L | <filesystem> |  |
| `__cpp_lib_flat_map` | 202207L | <flat_map> |  |
| `__cpp_lib_flat_set` | 202207L | <flat_set> |  |
| `__cpp_lib_format` | 202311L | <format> |  |
| `__cpp_lib_format_ranges` | 202207L | <format> |  |
| `__cpp_lib_format_path` | 202403L | <filesystem> |  |
| `__cpp_lib_format_uchar` | 202311L | <format> |  |
| `__cpp_lib_formatters` | 202302L | <stacktrace> <thread> |  |
| `__cpp_lib_forward_like` | 202207L | <utility> | Yes |
| `__cpp_lib_freestanding_algorithm` | 202311L | <algorithm> | Yes |
| `__cpp_lib_freestanding_array` | 202311L | <array> | Yes |
| `__cpp_lib_freestanding_char_traits` | 202306L | <string> | Yes |
| `__cpp_lib_freestanding_charconv` | 202306L | <charconv> | Yes |
| `__cpp_lib_freestanding_cstdlib` | 202306L | <cstdlib> <cmath> | Yes |
| `__cpp_lib_freestanding_cstring` | 202311L | <cstring> | Yes |
| `__cpp_lib_freestanding_cwchar` | 202306L | <cwchar> | Yes |
| `__cpp_lib_freestanding_errc` | 202306L | <cerrno> <system_error> | Yes |
| `__cpp_lib_freestanding_expected` | 202311L | <expected> | Yes |
| `__cpp_lib_freestanding_feature_test_macros` | 202306L |  | Yes |
| `__cpp_lib_freestanding_functional` | 202306L | <functional> | Yes |
| `__cpp_lib_freestanding_iterator` | 202306L | <iterator> | Yes |
| `__cpp_lib_freestanding_mdspan` | 202311L | <mdspan> | Yes |
| `__cpp_lib_freestanding_memory` | 202306L | <memory> | Yes |
| `__cpp_lib_freestanding_numeric` | 202311L | <numeric> | Yes |
| `__cpp_lib_freestanding_optional` | 202311L | <optional> | Yes |
| `__cpp_lib_freestanding_ranges` | 202306L | <ranges> | Yes |
| `__cpp_lib_freestanding_ratio` | 202306L | <ratio> | Yes |
| `__cpp_lib_freestanding_string_view` | 202311L | <string_view> | Yes |
| `__cpp_lib_freestanding_tuple` | 202306L | <tuple> | Yes |
| `__cpp_lib_freestanding_utility` | 202306L | <utility> | Yes |
| `__cpp_lib_freestanding_variant` | 202311L | <variant> | Yes |
| `__cpp_lib_fstream_native_handle` | 202306L | <fstream> |  |
| `__cpp_lib_function_ref` | 202306L | <functional> |  |
| `__cpp_lib_gcd_lcm` | 201606L | <numeric> |  |
| `__cpp_lib_generator` | 202207L | <generator> |  |
| `__cpp_lib_generic_associative_lookup` | 201304L | <map> <set> |  |
| `__cpp_lib_generic_unordered_lookup` | 201811L | <unordered_map> <unordered_set> |  |
| `__cpp_lib_hardware_interference_size` | 201703L | <new> | Yes |
| `__cpp_lib_has_unique_object_representations` | 201606L | <type_traits> | Yes |
| `__cpp_lib_hazard_pointer` | 202306L | <hazard_pointer> |  |
| `__cpp_lib_hypot` | 201603L | <cmath> |  |
| `__cpp_lib_incomplete_container_elements` | 201505L | <forward_list> <list> <vector> |  |
| `__cpp_lib_inplace_vector` | 202406L | <inplace_vector> |  |
| `__cpp_lib_int_pow2` | 202002L | <bit> | Yes |
| `__cpp_lib_integer_comparison_functions` | 202002L | <utility> |  |
| `__cpp_lib_integer_sequence` | 201304L | <utility> | Yes |
| `__cpp_lib_integral_constant_callable` | 201304L | <type_traits> | Yes |
| `__cpp_lib_interpolate` | 201902L | <cmath> <numeric> |  |
| `__cpp_lib_invoke` | 201411L | <functional> | Yes |
| `__cpp_lib_invoke_r` | 202106L | <functional> | Yes |
| `__cpp_lib_ios_noreplace` | 202207L | <ios> |  |
| `__cpp_lib_is_aggregate` | 201703L | <type_traits> | Yes |
| `__cpp_lib_is_constant_evaluated` | 201811L | <type_traits> | Yes |
| `__cpp_lib_is_final` | 201402L | <type_traits> | Yes |
| `__cpp_lib_is_implicit_lifetime` | 202302L | <type_traits> | Yes |
| `__cpp_lib_is_invocable` | 201703L | <type_traits> | Yes |
| `__cpp_lib_is_layout_compatible` | 201907L | <type_traits> | Yes |
| `__cpp_lib_is_nothrow_convertible` | 201806L | <type_traits> | Yes |
| `__cpp_lib_is_null_pointer` | 201309L | <type_traits> | Yes |
| `__cpp_lib_is_pointer_interconvertible` | 201907L | <type_traits> | Yes |
| `__cpp_lib_is_scoped_enum` | 202011L | <type_traits> | Yes |
| `__cpp_lib_is_sufficiently_aligned` | 202411L | <memory> |  |
| `__cpp_lib_is_swappable` | 201603L | <type_traits> | Yes |
| `__cpp_lib_is_virtual_base_of` | 202406L | <type_traits> | Yes |
| `__cpp_lib_is_within_lifetime` | 202306L | <type_traits> | Yes |
| `__cpp_lib_jthread` | 201911L | <stop_token> <thread> |  |
| `__cpp_lib_latch` | 201907L | <latch> |  |
| `__cpp_lib_launder` | 201606L | <new> | Yes |
| `__cpp_lib_linalg` | 202412L | <linalg> |  |
| `__cpp_lib_list_remove_return_type` | 201806L | <forward_list> <list> |  |
| `__cpp_lib_logical_traits` | 201510L | <type_traits> | Yes |
| `__cpp_lib_make_from_tuple` | 201606L | <tuple> | Yes |
| `__cpp_lib_make_reverse_iterator` | 201402L | <iterator> | Yes |
| `__cpp_lib_make_unique` | 201304L | <memory> |  |
| `__cpp_lib_map_try_emplace` | 201411L | <map> |  |
| `__cpp_lib_math_constants` | 201907L | <numbers> |  |
| `__cpp_lib_math_special_functions` | 201603L | <cmath> |  |
| `__cpp_lib_mdspan` | 202406L | <mdspan> | Yes |
| `__cpp_lib_memory_resource` | 201603L | <memory_resource> |  |
| `__cpp_lib_modules` | 202207L |  | Yes |
| `__cpp_lib_move_iterator_concept` | 202207L | <iterator> | Yes |
| `__cpp_lib_move_only_function` | 202110L | <functional> |  |
| `__cpp_lib_node_extract` | 201606L | <map> <set> <unordered_map> <unordered_set> |  |
| `__cpp_lib_nonmember_container_access` | 201411L | <array> <deque> <forward_list> <iterator> <list> <map> <regex> <set> <string> <unordered_map> <unordered_set> <vector> | Yes |
| `__cpp_lib_not_fn` | 202306L | <functional> | Yes |
| `__cpp_lib_null_iterators` | 201304L | <iterator> | Yes |
| `__cpp_lib_optional` | 202110L | <optional> |  |
| `__cpp_lib_optional_range_support` | 202406L | <optional> | Yes |
| `__cpp_lib_out_ptr` | 202311L | <memory> | Yes |
| `__cpp_lib_parallel_algorithm` | 201603L | <algorithm> <numeric> |  |
| `__cpp_lib_philox_engine` | 202406L | <random> |  |
| `__cpp_lib_polymorphic_allocator` | 201902L | <memory_resource> |  |
| `__cpp_lib_print` | 202406L | <print> <ostream> |  |
| `__cpp_lib_quoted_string_io` | 201304L | <iomanip> |  |
| `__cpp_lib_ranges` | 202406L | <algorithm> <functional> <iterator> <memory> <ranges> |  |
| `__cpp_lib_ranges_as_const` | 202311L | <ranges> | Yes |
| `__cpp_lib_ranges_as_rvalue` | 202207L | <ranges> | Yes |
| `__cpp_lib_ranges_cache_latest` | 202411L | <ranges> |  |
| `__cpp_lib_ranges_cartesian_product` | 202207L | <ranges> | Yes |
| `__cpp_lib_ranges_chunk` | 202202L | <ranges> | Yes |
| `__cpp_lib_ranges_chunk_by` | 202202L | <ranges> | Yes |
| `__cpp_lib_ranges_concat` | 202403L | <ranges> | Yes |
| `__cpp_lib_ranges_contains` | 202207L | <algorithm> |  |
| `__cpp_lib_ranges_enumerate` | 202302L | <ranges> |  |
| `__cpp_lib_ranges_find_last` | 202207L | <algorithm> |  |
| `__cpp_lib_ranges_fold` | 202207L | <algorithm> |  |
| `__cpp_lib_ranges_generate_random` | 202403L | <random> |  |
| `__cpp_lib_ranges_iota` | 202202L | <numeric> |  |
| `__cpp_lib_ranges_join_with` | 202202L | <ranges> | Yes |
| `__cpp_lib_ranges_repeat` | 202207L | <ranges> | Yes |
| `__cpp_lib_ranges_slide` | 202202L | <ranges> | Yes |
| `__cpp_lib_ranges_starts_ends_with` | 202106L | <algorithm> |  |
| `__cpp_lib_ranges_stride` | 202207L | <ranges> | Yes |
| `__cpp_lib_ranges_to_container` | 202202L | <ranges> | Yes |
| `__cpp_lib_ranges_zip` | 202110L | <ranges> <tuple> <utility> | Yes |
| `__cpp_lib_ratio` | 202306L | <ratio> | Yes |
| `__cpp_lib_raw_memory_algorithms` | 202411L | <memory> |  |
| `__cpp_lib_rcu` | 202306L | <rcu> |  |
| `__cpp_lib_reference_from_temporary` | 202202L | <type_traits> | Yes |
| `__cpp_lib_reference_wrapper` | 202403L | <functional> | Yes |
| `__cpp_lib_remove_cvref` | 201711L | <type_traits> | Yes |
| `__cpp_lib_result_of_sfinae` | 201210L | <functional> <type_traits> | Yes |
| `__cpp_lib_robust_nonmodifying_seq_ops` | 201304L | <algorithm> |  |
| `__cpp_lib_sample` | 201603L | <algorithm> |  |
| `__cpp_lib_saturation_arithmetic` | 202311L | <numeric> |  |
| `__cpp_lib_scoped_lock` | 201703L | <mutex> |  |
| `__cpp_lib_semaphore` | 201907L | <semaphore> |  |
| `__cpp_lib_senders` | 202406L | <execution> |  |
| `__cpp_lib_shared_mutex` | 201505L | <shared_mutex> |  |
| `__cpp_lib_shared_ptr_arrays` | 201707L | <memory> |  |
| `__cpp_lib_shared_ptr_weak_type` | 201606L | <memory> |  |
| `__cpp_lib_shared_timed_mutex` | 201402L | <shared_mutex> |  |
| `__cpp_lib_shift` | 202202L | <algorithm> |  |
| `__cpp_lib_simd` | 202411L | <simd> |  |
| `__cpp_lib_smart_ptr_for_overwrite` | 202002L | <memory> |  |
| `__cpp_lib_smart_ptr_owner_equality` | 202306L | <memory> |  |
| `__cpp_lib_source_location` | 201907L | <source_location> | Yes |
| `__cpp_lib_span` | 202311L | <span> | Yes |
| `__cpp_lib_span_initializer_list` | 202311L | <span> | Yes |
| `__cpp_lib_spanstream` | 202106L | <spanstream> |  |
| `__cpp_lib_ssize` | 201902L | <iterator> | Yes |
| `__cpp_lib_sstream_from_string_view` | 202306L | <sstream> |  |
| `__cpp_lib_stacktrace` | 202011L | <stacktrace> |  |
| `__cpp_lib_start_lifetime_as` | 202207L | <memory> | Yes |
| `__cpp_lib_starts_ends_with` | 201711L | <string> <string_view> |  |
| `__cpp_lib_stdatomic_h` | 202011L | <stdatomic.h> |  |
| `__cpp_lib_string_contains` | 202011L | <string> <string_view> |  |
| `__cpp_lib_string_resize_and_overwrite` | 202110L | <string> |  |
| `__cpp_lib_string_udls` | 201304L | <string> |  |
| `__cpp_lib_string_view` | 202403L | <string> <string_view> |  |
| `__cpp_lib_submdspan` | 202411L | <mdspan> | Yes |
| `__cpp_lib_syncbuf` | 201803L | <syncstream> |  |
| `__cpp_lib_text_encoding` | 202306L | <text_encoding> |  |
| `__cpp_lib_three_way_comparison` | 201907L | <compare> | Yes |
| `__cpp_lib_to_address` | 201711L | <memory> | Yes |
| `__cpp_lib_to_array` | 201907L | <array> | Yes |
| `__cpp_lib_to_chars` | 202306L | <charconv> |  |
| `__cpp_lib_to_string` | 202306L | <string> |  |
| `__cpp_lib_to_underlying` | 202102L | <utility> | Yes |
| `__cpp_lib_transformation_trait_aliases` | 201304L | <type_traits> | Yes |
| `__cpp_lib_transparent_operators` | 201510L | <memory> <functional> | Yes |
| `__cpp_lib_tuple_element_t` | 201402L | <tuple> | Yes |
| `__cpp_lib_tuple_like` | 202311L | <utility> <tuple> <map> <unordered_map> |  |
| `__cpp_lib_tuples_by_type` | 201304L | <utility> <tuple> | Yes |
| `__cpp_lib_type_identity` | 201806L | <type_traits> | Yes |
| `__cpp_lib_type_trait_variable_templates` | 201510L | <type_traits> | Yes |
| `__cpp_lib_uncaught_exceptions` | 201411L | <exception> | Yes |
| `__cpp_lib_unordered_map_try_emplace` | 201411L | <unordered_map> |  |
| `__cpp_lib_unreachable` | 202202L | <utility> | Yes |
| `__cpp_lib_unwrap_ref` | 201811L | <type_traits> | Yes |
| `__cpp_lib_variant` | 202306L | <variant> |  |
| `__cpp_lib_void_t` | 201411L | <type_traits> | Yes |
| Total number of macros: 245 | | | |

### Notes

Each value in "Value" column follows the pattern: "yyyymmL", where "yyyy" is a year, and "mm" is a month when the corresponding feature-set was accepted for standardization. Some values where increased since the time of their introduction, if capabilities of given feature where extended. The table above contains only the most recent values (that is, taken from the latest C++ language draft standard). A full set of values, including the initial and intermediate ones, can be found in this table.

### See also

|  |  |
| --- | --- |
| ****Feature testing**** (C++20) | A set of preprocessor macros to test the corresponding to C++ language and library features |
| C++ documentation for Headers required for a freestanding implementation | |
| C++ documentation for Predefined Macro Symbols | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/feature_test&oldid=173833>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 July 2024, at 13:15.