# std::function_ref::function_ref

From cppreference.com
< cpp‎ | utility‎ | functional‎ | function ref
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

Function objects

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function wrappers | | | | | | function(C++11) | | | | | | move_only_function(C++23) | | | | | | copyable_function(C++26) | | | | | | function_ref(C++26) | | | | | | mem_fn(C++11) | | | | | | bad_function_call(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Partial function application | | | | | | bind_frontbind_back(C++20)(C++23) | | | | | | bind(C++11) | | | | | | is_bind_expression(C++11) | | | | | | is_placeholder(C++11) | | | | | | _1, _2, _3, ...(C++11) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function invocation | | | | | | invokeinvoke_r(C++17)(C++23) | | | | | | Identity function object | | | | | | identity(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Reference wrappers | | | | | | reference_wrapper(C++11) | | | | | | refcref(C++11)(C++11) | | | | | | unwrap_referenceunwrap_ref_decay(C++20)(C++20) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Operator wrappers | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | plus | | | | | | minus | | | | | | negate | | | | | | multiplies | | | | | | divides | | | | | | modulus | | | | | | bit_and | | | | | | bit_or | | | | | | bit_not(C++14) | | | | | | bit_xor | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_to | | | | | | not_equal_to | | | | | | greater | | | | | | less | | | | | | greater_equal | | | | | | less_equal | | | | | | logical_and | | | | | | logical_or | | | | | | logical_not | | | | | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Transparent operator wrappers | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | plus<>(C++14) | | | | | | minus<>(C++14) | | | | | | negate<>(C++14) | | | | | | multiplies<>(C++14) | | | | | | divides<>(C++14) | | | | | | modulus<>(C++14) | | | | | | bit_and<>(C++14) | | | | | | bit_or<>(C++14) | | | | | | bit_not<>(C++14) | | | | | | bit_xor<>(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_to<>(C++14) | | | | | | not_equal_to<>(C++14) | | | | | | greater<>(C++14) | | | | | | less<>(C++14) | | | | | | greater_equal<>(C++14) | | | | | | less_equal<>(C++14) | | | | | | logical_and<>(C++14) | | | | | | logical_or<>(C++14) | | | | | | logical_not<>(C++14) | | | | | |  | | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Negators | | | | | | not_fn(C++17) | | | | | | Searchers | | | | | | default_searcher(C++17) | | | | | | boyer_moore_searcher(C++17) | | | | | | boyer_moore_horspool_searcher(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constrained comparators | | | | | | ranges::equal_to(C++20) | | | | | | ranges::not_equal_to(C++20) | | | | | | ranges::greater(C++20) | | | | | | ranges::less(C++20) | | | | | | ranges::greater_equal(C++20) | | | | | | ranges::less_equal(C++20) | | | | | | compare_three_way(C++20) | | | | | |
| Old binders and adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unary_function(until C++17\*) | | | | | | binary_function(until C++17\*) | | | | | | ptr_fun(until C++17\*) | | | | | | pointer_to_unary_function(until C++17\*) | | | | | | pointer_to_binary_function(until C++17\*) | | | | | | mem_fun(until C++17\*) | | | | | | mem_fun_tmem_fun1_tconst_mem_fun_tconst_mem_fun1_t(until C++17\*)(until C++17\*)(until C++17\*)(until C++17\*) | | | | | | not1(until C++20\*) | | | | | | not2(until C++20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | binder1stbinder2nd(until C++17\*)(until C++17\*) | | | | | | bind1stbind2nd(until C++17\*)(until C++17\*) | | | | | |  | | | | | | mem_fun_ref(until C++17\*) | | | | | | mem_fun_ref_tmem_fun1_ref_tconst_mem_fun_ref_tconst_mem_fun1_ref_t(until C++17\*)(until C++17\*)(until C++17\*)(until C++17\*) | | | | | | unary_negate(until C++20\*) | | | | | | binary_negate(until C++20\*) | | | | | |

std::function_ref

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****function_ref::function_ref**** | | | | |
| function_ref::operator= | | | | |
| function_ref::operator()") | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| template< class F >  function_ref( F\* f ) noexcept; | (1) | (since C++26) |
| template< class F >  function_ref( F&& f ) noexcept; | (2) | (since C++26) |
| template< auto f >  function_ref( std::nontype_t<f> ) noexcept; | (3) | (since C++26) |
| template< auto f, class U >  function_ref( std::nontype_t<f>, U&& obj ) noexcept; | (4) | (since C++26) |
| template< auto f, class T >  function_ref( std::nontype_t<f>, /\*cv\*/ T\* obj ) noexcept; | (5) | (since C++26) |
| function_ref( const function_ref& other ) = default; | (6) | (since C++26) |
|  |  |  |

Creates a new `std::function_ref`.

1) Initializes `bound-entity` with f, and `thunk-ptr` with the address of a function `thunk`. The behavior is undefined if f is a null pointer.

- This overload participates in overload resolution only if both std::is_function_v<F> and /\*is-invocable-using\*/<F> are true.
2) Initializes `bound-entity` with std::addressof(f), and `thunk-ptr` with the address of a function `thunk`.

- Let T be std::remove_reference_t<F>. This overload participates in overload resolution only if :
  - std::remove_cvref_t<F> is not the same type as `function_ref`,
  - std::is_member_pointer_v<T> is false, and
  - /\*is-invocable-using\*/</\*cv\*/ T&> is true.
3) Initializes `bound-entity` with a pointer to an unspecified object or null pointer value, and `thunk-ptr` with the address of a function `thunk`.

- Let F be decltype(f). This overload participates in overload resolution only if /\*is-invocable-using\*/<F> is true.
- The program is ill-formed if f != nullptr is false when std::is_pointer_v<F> || std::is_member_pointer_v<F> is true.
4) Initializes `bound-entity` with std::addressof(obj), and `thunk-ptr` with the address of a function `thunk`.

- Let T be std::remove_reference_t<U> and F be decltype(f). This overload participates in overload resolution only if :
  - std::is_rvalue_reference_v<U&&> is false, and
  - /\*is-invocable-using\*/<F, /\*cv\*/ T&> is true.
- The program is ill-formed if f != nullptr is false when std::is_pointer_v<F> || std::is_member_pointer_v<F> is true.
5) Initializes `bound-entity` with obj, and `thunk-ptr` with the address of a function `thunk`. The behavior is undefined if obj is a null pointer when std::is_member_pointer_v<F> is true.

- Let F be decltype(f). This overload participates in overload resolution only if /\*is-invocable-using\*/<F, /\*cv\*/ T\*> is true.
- The program is ill-formed if f != nullptr is false when std::is_pointer_v<F> || std::is_member_pointer_v<F> is true.
6) Defaulted copy constructor copies the `bound-entity` and `thunk-ptr` of other.

The address of a function `thunk` is used to initialize `thunk-ptr` such that a call to `thunk`(`bound-entity`, `call-args`...) is expression-equivalent to:

| Overloads | Expression-equivalence |
| --- | --- |
| (1,3) | std::invoke_r<R>(f, `call-args`...) |
| (2) | std::invoke_r<R>(static_cast<cv T&>(f), `call-args`...) |
| (4) | std::invoke_r<R>(f, static_cast<cv T&>(obj), `call-args`...) |
| (5) | std::invoke_r<R>(f, obj, `call-args`...) |

/\*is-invocable-using\*/<T...> is true if and only if:

- std::is_nothrow_invocable_r_v<R, T..., Args...> is true if noex is true, or
- std::is_invocable_r_v<R, T..., Args...> is true

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another `function_ref` to copy from |
| f | - | a function or a Callable object to wrap |
| obj | - | an object or pointer to bound |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a new `std::move_only_function` object   (public member function of `std::move_only_function`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/functional/function_ref/function_ref&oldid=178019>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 November 2024, at 07:44.