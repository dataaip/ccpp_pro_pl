# operator delete, operator delete[]

From cppreference.com
< cpp‎ | memory‎ | new
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

Memory management library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **voidify**(exposition only\*) | | | | | | Uninitialized memory algorithms | | | | | | uninitialized_copy | | | | | | uninitialized_fill | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | destroy(C++17) | | | | | | destroy_at(C++17) | | | | | | uninitialized_copy_n(C++11) | | | | | | uninitialized_fill_n | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | destroy_n(C++17) | | | | | | construct_at(C++20) | | | | | | Constrained uninitialized memory algorithms | | | | | | ranges::uninitialized_copy(C++20) | | | | | | ranges::uninitialized_fill(C++20) | | | | | | ranges::uninitialized_move(C++20) | | | | | | ranges::construct_at(C++20) | | | | | | ranges::destroy(C++20) | | | | | | ranges::destroy_n(C++20) | | | | | | ranges::destroy_at(C++20) | | | | | | ranges::uninitialized_copy_n(C++20) | | | | | | ranges::uninitialized_fill_n(C++20) | | | | | | ranges::uninitialized_move_n(C++20) | | | | | | ranges::uninitialized_default_construct(C++20) | | | | | | ranges::uninitialized_value_construct(C++20) | | | | | | ranges::uninitialized_default_construct_n(C++20) | | | | | | ranges::uninitialized_value_construct_n(C++20) | | | | | | C Library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | malloc | | | | | | calloc | | | | | | realloc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | aligned_alloc(C++17) | | | | | | free | | | | | |  | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Allocators | | | | | | allocator | | | | | | allocator_traits(C++11) | | | | | | allocation_result(C++23) | | | | | | allocator_arg(C++11) | | | | | | uses_allocator(C++11) | | | | | | uses_allocator_construction_args(C++20) | | | | | | make_obj_using_allocator(C++20) | | | | | | uninitialized_construct_using_allocator(C++20) | | | | | | scoped_allocator_adaptor(C++11) | | | | | | pmr::polymorphic_allocator(C++17) | | | | | | Memory resources | | | | | | pmr::memory_resource(C++17) | | | | | | pmr::get_default_resource(C++17) | | | | | | pmr::set_default_resource(C++17) | | | | | | pmr::new_delete_resource(C++17) | | | | | | pmr::null_memory_resource(C++17) | | | | | | pmr::synchronized_pool_resource(C++17) | | | | | | pmr::unsynchronized_pool_resource(C++17) | | | | | | pmr::monotonic_buffer_resource(C++17) | | | | | | pmr::pool_options(C++17) | | | | | | Garbage collection support | | | | | | declare_reachable(C++11)(until C++23) | | | | | | undeclare_reachable(C++11)(until C++23) | | | | | | declare_no_pointers(C++11)(until C++23) | | | | | | undeclare_no_pointers(C++11)(until C++23) | | | | | | pointer_safety(C++11)(until C++23) | | | | | | get_pointer_safety(C++11)(until C++23) | | | | | | Uninitialized storage | | | | | | raw_storage_iterator(until C++20\*) | | | | | | get_temporary_buffer(until C++20\*) | | | | | | return_temporary_buffer(until C++20\*) | | | | | | Explicit lifetime management | | | | | | start_lifetime_asstart_lifetime_as_array(C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Smart pointers | | | | | | unique_ptr(C++11) | | | | | | shared_ptr(C++11) | | | | | | weak_ptr(C++11) | | | | | | auto_ptr(until C++17\*) | | | | | | owner_less(C++11) | | | | | | owner_less<void>(C++17) | | | | | | owner_hash(C++26) | | | | | | owner_equal(C++26) | | | | | | enable_shared_from_this(C++11) | | | | | | bad_weak_ptr(C++11) | | | | | | default_delete(C++11) | | | | | | out_ptr_t(C++23) | | | | | | inout_ptr_t(C++23) | | | | | | Low level memory management | | | | | | operator new | | | | | | [operator new[]](operator_new.html "cpp/memory/new/operator new") | | | | | | ****operator delete**** | | | | | | ****operator delete[]**** | | | | | | get_new_handler(C++11) | | | | | | set_new_handler | | | | | | launder(C++17) | | | | | | bad_alloc | | | | | | bad_array_new_length(C++11) | | | | | | nothrow_t | | | | | | align_val_t(C++17) | | | | | | destroying_delete_t(C++20) | | | | | | new_handler | | | | | | nothrow | | | | | | Miscellaneous | | | | | | pointer_traits(C++11) | | | | | | to_address(C++20) | | | | | | addressof(C++11) | | | | | | align(C++11) | | | | | | assume_aligned(C++20) | | | | | | is_sufficiently_aligned(C++26) | | | | | |

Low level memory management

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| [operator newoperator new[]](operator_new.html "cpp/memory/new/operator new") | | | | |
| ****operator deleteoperator delete[]**** | | | | |
| get_new_handler(C++11) | | | | |
| set_new_handler | | | | |
| Classes | | | | |
| bad_alloc | | | | |
| bad_array_new_length(C++11) | | | | |
| align_val_t(C++17) | | | | |
| Types | | | | |
| new_handler | | | | |
| Objects | | | | |
| nothrow | | | | |
| destroying_delete(C++20) | | | | |
| Object access | | | | |
| launder(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<new>` |  |  |
| replaceable usual deallocation functions |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| void operator delete  ( void\* ptr ) throw(); |  | (until C++11) |
| void operator delete  ( void\* ptr ) noexcept; |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| void operator delete[]( void\* ptr ) throw(); |  | (until C++11) |
| void operator delete[]( void\* ptr ) noexcept; |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| void operator delete  ( void\* ptr, std::align_val_t al ) noexcept; | (3) | (since C++17) |
| void operator delete[]( void\* ptr, std::align_val_t al ) noexcept; | (4) | (since C++17) |
| void operator delete  ( void\* ptr, std::size_t sz ) noexcept; | (5) | (since C++14) |
| void operator delete[]( void\* ptr, std::size_t sz ) noexcept; | (6) | (since C++14) |
| void operator delete  ( void\* ptr, std::size_t sz,                          std::align_val_t al ) noexcept; | (7) | (since C++17) |
| void operator delete[]( void\* ptr, std::size_t sz,                          std::align_val_t al ) noexcept; | (8) | (since C++17) |
| replaceable placement deallocation functions |  |  |
|  |  |  |
| --- | --- | --- |
|  | (9) |  |
| void operator delete  ( void\* ptr, const std::nothrow_t& tag ) throw(); |  | (until C++11) |
| void operator delete  ( void\* ptr, const std::nothrow_t& tag ) noexcept; |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  | (10) |  |
| void operator delete[]( void\* ptr, const std::nothrow_t& tag ) throw(); |  | (until C++11) |
| void operator delete[]( void\* ptr, const std::nothrow_t& tag ) noexcept; |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| void operator delete  ( void\* ptr, std::align_val_t al,                          const std::nothrow_t& tag ) noexcept; | (11) | (since C++17) |
| void operator delete[]( void\* ptr, std::align_val_t al,                          const std::nothrow_t& tag ) noexcept; | (12) | (since C++17) |
| non-allocating placement deallocation functions |  |  |
|  |  |  |
| --- | --- | --- |
|  | (13) |  |
| void operator delete  ( void\* ptr, void\* place ) throw(); |  | (until C++11) |
| void operator delete  ( void\* ptr, void\* place ) noexcept; |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  | (14) |  |
| void operator delete[]( void\* ptr, void\* place ) throw(); |  | (until C++11) |
| void operator delete[]( void\* ptr, void\* place ) noexcept; |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| user-defined placement deallocation functions |  |  |
| void operator delete  ( void\* ptr, args... ); | (15) |  |
| void operator delete[]( void\* ptr, args... ); | (16) |  |
| class-specific usual deallocation functions |  |  |
| void T::operator delete  ( void\* ptr ); | (17) |  |
| void T::operator delete[]( void\* ptr ); | (18) |  |
| void T::operator delete  ( void\* ptr, std::align_val_t al ); | (19) | (since C++17) |
| void T::operator delete[]( void\* ptr, std::align_val_t al ); | (20) | (since C++17) |
| void T::operator delete  ( void\* ptr, std::size_t sz ); | (21) |  |
| void T::operator delete[]( void\* ptr, std::size_t sz ); | (22) |  |
| void T::operator delete  ( void\* ptr, std::size_t sz, std::align_val_t al ); | (23) | (since C++17) |
| void T::operator delete[]( void\* ptr, std::size_t sz, std::align_val_t al ); | (24) | (since C++17) |
| class-specific placement deallocation functions |  |  |
| void T::operator delete  ( void\* ptr, args... ); | (25) |  |
| void T::operator delete[]( void\* ptr, args... ); | (26) |  |
| class-specific usual destroying deallocation functions |  |  |
| void T::operator delete( T\* ptr, std::destroying_delete_t ); | (27) | (since C++20) |
| void T::operator delete( T\* ptr, std::destroying_delete_t,                           std::align_val_t al ); | (28) | (since C++20) |
| void T::operator delete( T\* ptr, std::destroying_delete_t, std::size_t sz ); | (29) | (since C++20) |
| void T::operator delete( T\* ptr, std::destroying_delete_t,                           std::size_t sz, std::align_val_t al ); | (30) | (since C++20) |
|  |  |  |

Deallocates storage previously allocated by a matching operator new. These deallocation functions are called by delete-expressions and by new-expressions to deallocate memory after destructing (or failing to construct) objects with dynamic storage duration. They may also be called using regular function call syntax.

1) Called by delete-expressions to deallocate storage previously allocated for a single object. The behavior of the standard library implementation of this function is undefined unless ptr is a null pointer or is a pointer previously obtained from the standard library implementation of operator new(std::size_t) or operator new(std::size_t, std::nothrow_t).2) Called by [delete[]-expressions](../../language/delete.html "cpp/language/delete") to deallocate storage previously allocated for an array of objects. The behavior of the standard library implementation of this function is undefined unless ptr is a null pointer or is a pointer previously obtained from the standard library implementation of operator new[](std::size_t) or operator new[](std::size_t, std::nothrow_t).3,4) Same as (1,2), except called if the alignment requirement exceeds __STDCPP_DEFAULT_NEW_ALIGNMENT__.5,6) Called instead of (1,2) if a user-defined replacement is provided, except that it's unspecified whether (1,2) or (5,6) is called when deleting objects of incomplete type and arrays of non-class and trivially-destructible class types. A memory allocator can use the given size to be more efficient. The standard library implementations are identical to (1,2).7,8) Same as (5,6), except called if the alignment requirement exceeds __STDCPP_DEFAULT_NEW_ALIGNMENT__.9) Called by the non-throwing single-object new-expressions if a constructor of the object throws an exception. The standard library implementation behaves the same as (1).10) Called by the non-throwing array [new[]-expressions](../../language/new.html "cpp/language/new") if a constructor of any object throws an exception (after executing the destructors of all objects in the array that were successfully constructed). The standard library implementation behaves the same as (2).11,12) Same as (9,10), except called if the alignment requirement exceeds __STDCPP_DEFAULT_NEW_ALIGNMENT__.13) Called by the standard single-object placement new expression if the object's constructor throws an exception. The standard library implementation of this function does nothing.14) Called by the standard array form of the [placement new[]](../../language/new.html "cpp/language/new") expression if any of the objects' constructors throws an exception (after executing the destructors of all objects that were constructed successfully). The standard library implementation of this function does nothing.15) If defined, called by the custom single-object placement new expression with the matching signature if the object's constructor throws an exception. If a class-specific version (25) is defined, it is called in preference to (9). If neither (25) nor (15) is provided by the user, no deallocation function is called.16) If defined, called by the custom array form of [placement new[]](../../language/new.html "cpp/language/new") expression with the matching signature if any of the objects' constructors throws an exception (after executing the destructors for all objects that were constructed successfully). If a class-specific version (26) is defined, it is called in preference to (10). If neither (26) nor (16) is provided by the user, no deallocation function is called.17) If defined, called by the usual single-object delete-expressions if deallocating an object of type `T`.18) If defined, called by the usual array [delete[]-expressions](../../language/delete.html "cpp/language/delete") if deallocating an array of objects of type `T`.19,20) If defined, called in preference to (17,18) if the alignment requirement exceeds __STDCPP_DEFAULT_NEW_ALIGNMENT__.21) If defined, and if (17) is not defined, called by the usual single-object delete-expressions if deallocating an object of type `T`.22) If defined, and if (18) is not defined, called by the usual array [delete[]-expressions](../../language/delete.html "cpp/language/delete") if deallocating an array of objects of type `T`.23,24) If defined, and if (19,20) are not defined, called in preference to allocator-unaware members if the alignment requirement exceeds __STDCPP_DEFAULT_NEW_ALIGNMENT__.25) If defined, called by the custom single-object placement new expression with the matching signature if the object's constructor throws an exception. If this function is not provided, and a matching (15) is not provided either, no deallocation function is called.26) If defined, called by the custom array form of [placement new[]](../../language/new.html "cpp/language/new") expression with the matching signature if any of the objects' constructors throws an exception (after executing the destructors for all objects that were constructed successfully). If this function is not provided, and a matching (16) is not provided either, no deallocation function is called.27-30) If defined, delete-expressions does not execute the destructor for \*p before placing a call to `operator delete`. Instead, direct invocation of the destructor such as by p->~T(); becomes the responsibility of this user-defined operator delete.

|  |  |
| --- | --- |
| See delete-expression for exact details on the overload resolution rules between alignment-aware and alignment-unaware overloads of usual (non-placement) deallocation functions. | (since C++17) |

In all cases, if ptr is a null pointer, the standard library deallocation functions do nothing. If the pointer passed to the standard library deallocation function was not obtained from the corresponding standard library allocation function, the behavior is undefined.

After the standard library deallocation function returns, all pointers referring to any part of the deallocated storage become invalid.

Indirection through a pointer that became invalid in this manner and passing it to a deallocation function (double-delete) is undefined behavior. Any other use is implementation-defined.

### Parameters

|  |  |  |
| --- | --- | --- |
| ptr | - | pointer to a memory block to deallocate or a null pointer |
| sz | - | the size that was passed to the matching allocation function |
| place | - | pointer used as the placement parameter in the matching placement new |
| tag | - | overload disambiguation tag matching the tag used by non-throwing operator new |
| al | - | alignment of the object or array element that was allocated |
| args | - | arbitrary parameters matching a placement allocation function (may include std::size_t and std::align_val_t) |

### Return value

(none)

### Exceptions

|  |  |
| --- | --- |
| All deallocation functions are noexcept(true) unless specified otherwise in the declaration. | (since C++11) |

If a deallocation function terminates by throwing an exception, the behavior is undefined, even if it is declared with noexcept(false)(since C++11).

### Global replacements

The replaceable deallocation functions (1-12) are implicitly declared in each translation unit even if the <new> header is not included. These functions are **replaceable**: a user-provided non-member function with the same signature defined anywhere in the program, in any source file, replaces the corresponding implicit version for the entire program. Its declaration does not need to be visible.

The program is ill-formed, no diagnostic required if more than one replacement is provided in the program or if a replacement is declared with the `inline` specifier. The program is ill-formed if a replacement is defined in namespace other than global namespace, or if it is defined as a static non-member function at global scope.

The standard library implementations of the nothrow versions (9,10) directly call the corresponding throwing versions (1,2). The standard library implementations of the size-aware deallocation functions (5-8) directly call the corresponding size-unaware deallocation functions (1-4). The standard library implementations of size-unaware throwing array forms (2,4) directly calls the corresponding single-object forms (1,3). Thus, replacing the throwing single object deallocation functions (1,3) is sufficient to handle all deallocations.

Global `operator`s new/delete replacement:

Run this code

```
#include <cstdio>
#include <cstdlib>
#include <new>
 
// no inline, required by [replacement.functions]/3
void* operator new(std::size_t sz)
{
    std::printf("1) new(size_t), size = %zu\n", sz);
    if (sz == 0)
        ++sz; // avoid std::malloc(0) which may return nullptr on success
 
    if (void *ptr = std::malloc(sz))
        return ptr;
 
    throw std::bad_alloc{}; // required by [new.delete.single]/3
}
 
// no inline, required by [replacement.functions]/3
void* operator new[](std::size_t sz)
{
    std::printf("2) new[](size_t), size = %zu\n", sz);
    if (sz == 0)
        ++sz; // avoid std::malloc(0) which may return nullptr on success
 
    if (void *ptr = std::malloc(sz))
        return ptr;
 
    throw std::bad_alloc{}; // required by [new.delete.single]/3
}
 
void operator delete(void* ptr) noexcept
{
    std::puts("3) delete(void*)");
    std::free(ptr);
}
 
void operator delete(void* ptr, std::size_t size) noexcept
{
    std::printf("4) delete(void*, size_t), size = %zu\n", size);
    std::free(ptr);
}
 
void operator delete[](void* ptr) noexcept
{
    std::puts("5) delete[](void* ptr)");
    std::free(ptr);
}
 
void operator delete[](void* ptr, std::size_t size) noexcept
{
    std::printf("6) delete[](void*, size_t), size = %zu\n", size);
    std::free(ptr);
}
 
int main()
{
    int* p1 = new int;
    delete p1;
 
    int* p2 = new int[10]; // guaranteed to call the replacement in C++11
    delete[] p2;
}

```

Possible output:

```
// Compiled with GCC-5 in C++17 mode to obtain the following:
1) op new(size_t), size = 4
4) op delete(void*, size_t), size = 4
2) op new[](size_t), size = 40
5) op delete[](void* ptr)

```

Overloads of `operator delete` and `operator delete[]` with additional user-defined parameters ("placement forms", (15,16)) may be declared at global scope as usual, and are called by the matching placement forms of **new-expressions** if a constructor of the object that is being allocated throws an exception.

The standard library placement forms of `operator delete` (13,14) cannot be replaced and can only be customized if the placement new-expression did not use the ::new syntax, by providing a class-specific placement delete (25,26) with matching signature: void T::operator delete(void\*, void\*) or void T::operator delete[](void\*, void\*).

### Class-specific overloads

Deallocation functions (17-24) may be defined as static member functions of a class. These deallocation functions, if provided, are called by delete-expressions when deleting objects (17,19,21) and arrays (18,20,22) of this class, unless the delete expression used the form ::delete which bypasses class-scope lookup. The keyword static is optional for these function declarations: whether the keyword is used or not, the deallocation function is always a static member function.

The delete expression looks for appropriate deallocation function's name starting from the class scope (array form looks in the scope of the array element class) and proceeds to the global scope if no members are found as usual. Note, that as per name lookup rules, any deallocation functions declared in class scope hides all global deallocation functions.

If the static type of the object that is being deleted differs from its dynamic type (such as when deleting a polymorphic object through a pointer to base), and if the destructor in the static type is virtual, the single object form of delete begins lookup of the deallocation function's name starting from the point of definition of the final overrider of its virtual destructor. Regardless of which deallocation function would be executed at run time, the statically visible version of operator delete must be accessible in order to compile. In other cases, when deleting an array through a pointer to base, or when deleting through pointer to base with non-virtual destructor, the behavior is undefined.

If the single-argument overload (17,18) is not provided, but the size-aware overload taking std::size_t as the second parameter (21,22) is provided, the size-aware form is called for normal deallocation, and the C++ runtime passes the size of the object to be deallocated as the second argument. If both forms are defined, the size-unaware version is called.

Run this code

```
#include <cstddef>
#include <iostream>
 
// sized class-specific deallocation functions
struct X
{
    static void operator delete(void* ptr, std::size_t sz)
    {
        std::cout << "custom delete for size " << sz << '\n';
        ::operator delete(ptr);
    }
 
    static void operator delete[](void* ptr, std::size_t sz)
    {
        std::cout << "custom delete for size " << sz << '\n';
        ::operator delete[](ptr);
    }
};
 
int main()
{
    X* p1 = new X;
    delete p1;
 
    X* p2 = new X[10];
    delete[] p2;
}

```

Possible output:

```
custom delete for size 1
custom delete for size 18

```

Overloads of `operator delete` and `operator delete[]` with additional user-defined parameters ("placement forms", (25,26)) may also be defined as class members. When the failed placement new expression looks for the corresponding placement delete function to call, it begins lookup at class scope before examining the global scope, and looks for the function with the signature matching the placement new:

Run this code

```
#include <cstddef>
#include <iostream>
#include <stdexcept>
 
struct X
{
    X() { throw std::runtime_error("X(): std::runtime_error"); }
 
    // custom placement new
    static void* operator new(std::size_t sz, bool b)
    {
        std::cout << "custom placement new called, b = " << b << '\n';
        return ::operator new(sz);
    }
 
    // custom placement delete
    static void operator delete(void* ptr, bool b)
    {
        std::cout << "custom placement delete called, b = " << b << '\n';
        ::operator delete(ptr);
    }
};
 
int main()
{
    try
    {
        [[maybe_unused]] X* p1 = new (true) X;
    }
    catch (const std::exception& ex)
    {
        std::cout << ex.what() << '\n';
    }
}

```

Output:

```
custom placement new called, b = 1
custom placement delete called, b = 1
X(): std::runtime_error

```

If class-level `operator delete` is a template function, it must have the return type of void, the first argument void\*, and it must have two or more parameters. In other words, only placement forms can be templates. A template instance is never a usual deallocation function, regardless of its signature. The specialization of the template operator delete is chosen with template argument deduction.

### Notes

The call to the class-specific T::operator delete on a polymorphic class is the only case where a static member function is called through dynamic dispatch.

If the behavior of a deallocation function does not satisfy the default constraints, the behavior is undefined.

|  |  |
| --- | --- |
| The following functions are required to be thread-safe:   - The library versions of operator new and ****operator delete**** - User replacement versions of global operator new and ****operator delete**** - std::calloc, std::malloc, std::realloc, std::aligned_alloc(since C++17), std::free   Calls to these functions that allocate or deallocate a particular unit of storage occur in a single total order, and each such deallocation call happens-before the next allocation (if any) in this order. | (since C++11) |

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_sized_deallocation` | `201309L` | (C++14) | Sized deallocation |
| `__cpp_impl_destroying_delete` | `201806L` | (C++20) | Destroying operator delete (compiler support) |
| `__cpp_lib_destroying_delete` | `201806L` | (C++20) | Destroying operator delete (library support) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 220 | C++98 | user-defined deallocation functions were permitted to throw | throwing from a deallocation function results in undefined behavior |
| CWG 1438 | C++98 | any use of an invalid pointer value was undefined behavior | only indirection and deallocation are |
| LWG 206 | C++98 | replacing (2) did not affect the default behavior of (10) | the default behavior changes accordingly |
| LWG 298 | C++98 | replacing (1) did not affect the default behavior of (9) | the default behavior changes accordingly |
| LWG 404 | C++98 | replacements of the replaceable deallocation functions could be declared inline | prohibited, no diagnostic required |
| LWG 2458 | C++14 | overloads taking (void\*, std::size_t, const std::nothrow_t&) were specified, but could never be called | removed spurious overloads |

### See also

|  |  |
| --- | --- |
| operator delete[static] (C++23) | deallocates memory previously obtained from `operator new`   (public static member function of `std::generator<Ref,V,Allocator>::promise_type`) |
| [operator newoperator new[]](operator_new.html "cpp/memory/new/operator new") | allocation functions   (function) |
| return_temporary_buffer(deprecated in C++17)(removed in C++20) | frees uninitialized storage   (function template) |
| free | deallocates previously allocated memory   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/memory/new/operator_delete&oldid=175091>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 August 2024, at 02:00.