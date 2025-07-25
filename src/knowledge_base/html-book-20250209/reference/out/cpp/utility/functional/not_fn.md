# std::not_fn

From cppreference.com
< cpp‎ | utility‎ | functional
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Negators | | | | | | ****not_fn****(C++17) | | | | | | Searchers | | | | | | default_searcher(C++17) | | | | | | boyer_moore_searcher(C++17) | | | | | | boyer_moore_horspool_searcher(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constrained comparators | | | | | | ranges::equal_to(C++20) | | | | | | ranges::not_equal_to(C++20) | | | | | | ranges::greater(C++20) | | | | | | ranges::less(C++20) | | | | | | ranges::greater_equal(C++20) | | | | | | ranges::less_equal(C++20) | | | | | | compare_three_way(C++20) | | | | | |
| Old binders and adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unary_function(until C++17\*) | | | | | | binary_function(until C++17\*) | | | | | | ptr_fun(until C++17\*) | | | | | | pointer_to_unary_function(until C++17\*) | | | | | | pointer_to_binary_function(until C++17\*) | | | | | | mem_fun(until C++17\*) | | | | | | mem_fun_tmem_fun1_tconst_mem_fun_tconst_mem_fun1_t(until C++17\*)(until C++17\*)(until C++17\*)(until C++17\*) | | | | | | not1(until C++20\*) | | | | | | not2(until C++20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | binder1stbinder2nd(until C++17\*)(until C++17\*) | | | | | | bind1stbind2nd(until C++17\*)(until C++17\*) | | | | | |  | | | | | | mem_fun_ref(until C++17\*) | | | | | | mem_fun_ref_tmem_fun1_ref_tconst_mem_fun_ref_tconst_mem_fun1_ref_t(until C++17\*)(until C++17\*)(until C++17\*)(until C++17\*) | | | | | | unary_negate(until C++20\*) | | | | | | binary_negate(until C++20\*) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<functional>` |  |  |
| template< class F >  /\* unspecified \*/ not_fn( F&& f ); | (1) | (since C++17)  (constexpr since C++20) |
| template< auto ConstFn >  constexpr /\* unspecified \*/ not_fn() noexcept; | (2) | (since C++26) |
|  |  |  |

1) Creates a forwarding call wrapper that returns the negation of the callable object it holds.2) Creates a forwarding call wrapper that returns the negation of the statically determined callable target. The program is ill-formed if `ConstFn` is a null pointer or null pointer-to-member.

### Parameters

|  |  |  |
| --- | --- | --- |
| f | - | the object from which the Callable object held by the wrapper is constructed |
| Type requirements | | |
| -`std::decay_t<F>` must meet the requirements of Callable and MoveConstructible. | | |
| -std::is_constructible_v<std::decay_t<F>, F> is required to be true. | | |

### Return value

1) A function object of unspecified type `T`. It has the following members.

## std::not_fn **return type**

#### Member objects

The return type of `std::not_fn` holds a member object of type std::decay_t<F>.

#### Constructors

|  |  |  |
| --- | --- | --- |
| explicit T( F&& f ); | (1) | (since C++17)  (constexpr since C++20) (exposition only\*) |
| T( T&& f ) = default;  T( const T& f ) = default; | (2) | (since C++17) |
|  |  |  |

1) The constructor direct-non-list-initializes the member object (of type std::decay_t<F>) from std::forward<F>(f). Throws any exception thrown by the constructor selected.2) Because std::decay_t<F> is required to be MoveConstructible, the returned call wrapper is always MoveConstructible, and is CopyConstructible if std::decay_t<F> is CopyConstructible.

|  |  |
| --- | --- |
| The explicitly defaulted definitions make the return type not assignable. | (until C++20) |
| It is unspecified whether these constructors are explicitly defaulted and whether the return type is assignable. | (since C++20) |

#### Member function operator()

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| template< class... Args >  auto operator()( Args&&... args ) &  -> decltype(!std::declval<      std::invoke_result_t<std::decay_t<F>&, Args...>>());  template< class... Args >  auto operator()( Args&&... args ) const&  -> decltype(!std::declval< std::invoke_result_t<std::decay_t<F> const&, Args...>>()); |  | (since C++17)  (until C++20) |
| template< class... Args >  constexpr auto operator()( Args&&... args ) &      noexcept(/\* see below \*/)  -> decltype(!std::invoke(      std::declval<std::decay_t<F>&>(), std::declval<Args>()...));  template< class... Args >  constexpr auto operator()( Args&&... args ) const&      noexcept(/\* see below \*/)  -> decltype(!std::invoke( std::declval<std::decay_t<F> const&>(), std::declval<Args>()...)); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| template< class... Args >  auto operator()( Args&&... args ) &&  -> decltype(!std::declval<      std::invoke_result_t<std::decay_t<F>, Args...>>());  template< class... Args >  auto operator()( Args&&... args ) const&&  -> decltype(!std::declval< std::invoke_result_t<std::decay_t<F> const, Args...>>()); |  | (since C++17)  (until C++20) |
| template< class... Args >  constexpr auto operator()( Args&&... args ) &&      noexcept(/\* see below \*/)  -> decltype(!std::invoke(      std::declval<std::decay_t<F>>(), std::declval<Args>()...));  template< class... Args >  constexpr auto operator()( Args&&... args ) const&&      noexcept(/\* see below \*/)  -> decltype(!std::invoke( std::declval<std::decay_t<F> const>(), std::declval<Args>()...)); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Let fd be the member object of type std::decay_t<F>.

|  |  |
| --- | --- |
| 1) Equivalent to return !std::invoke(fd, std::forward<Args>(args)...);2) Equivalent to return !std::invoke(std::move(fd), std::forward<Args>(args)...); While invoking the result, if the substitution into the return type of the originally selected operator() overload fails, another overload may be selected. | (since C++17) (until C++20) |
| 1) Expression-equivalent to !std::invoke(fd, std::forward<Args>(args)...)2) Expression-equivalent to !std::invoke(std::move(fd), std::forward<Args>(args)...) While invoking the result, if the substitution into the return type of the originally selected operator() overload fails, the invocation is ill-formed, which can also be a substitution failure. | (since C++20) |

2) A value of the following type.

## std::not_fn **stateless return type**

The return type is a CopyConstructible stateless class. It is unspecified whether the return type is assignable.

#### Member function operator()

|  |  |  |
| --- | --- | --- |
| template< class... Args >  constexpr auto operator()( Args&&... args ) const      noexcept(/\* see below \*/) -> decltype(!std::invoke(ConstFn, std::declval<Args>()...)); |  | (since C++26) |
|  |  |  |

Expression-equivalent to !std::invoke(ConstFn, std::forward<Args>(args)...).

### Exceptions

1) Throws no exceptions, unless the construction of fd throws.

### Possible implementation

| (1) not_fn |
| --- |
| ```text namespace detail {     template<class V, class F, class... Args>     constexpr bool negate_invocable_impl = false;     template<class F, class... Args>     constexpr bool negate_invocable_impl<std::void_t<decltype(         !std::invoke(std::declval<F>(), std::declval<Args>()...))>, F, Args...> = true;       template<class F, class... Args>     constexpr bool negate_invocable_v = negate_invocable_impl<void, F, Args...>;       template<class F>     struct not_fn_t     {         F f;           template<class... Args,             std::enable_if_t<negate_invocable_v<F&, Args...>, int> = 0>         constexpr decltype(auto) operator()(Args&&... args) &             noexcept(noexcept(!std::invoke(f, std::forward<Args>(args)...)))         {             return !std::invoke(f, std::forward<Args>(args)...);         }           template<class... Args,             std::enable_if_t<negate_invocable_v<const F&, Args...>, int> = 0>         constexpr decltype(auto) operator()(Args&&... args) const&             noexcept(noexcept(!std::invoke(f, std::forward<Args>(args)...)))         {             return !std::invoke(f, std::forward<Args>(args)...);         }           template<class... Args,             std::enable_if_t<negate_invocable_v<F, Args...>, int> = 0>         constexpr decltype(auto) operator()(Args&&... args) &&             noexcept(noexcept(!std::invoke(std::move(f), std::forward<Args>(args)...)))         {             return !std::invoke(std::move(f), std::forward<Args>(args)...);         }           template<class... Args,             std::enable_if_t<negate_invocable_v<const F, Args...>, int> = 0>         constexpr decltype(auto) operator()(Args&&... args) const&&             noexcept(noexcept(!std::invoke(std::move(f), std::forward<Args>(args)...)))         {             return !std::invoke(std::move(f), std::forward<Args>(args)...);         }           // Deleted overloads are needed since C++20         // for preventing a non-equivalent but well-formed overload to be selected.           template<class... Args,             std::enable_if_t<!negate_invocable_v<F&, Args...>, int> = 0>         void operator()(Args&&...) & = delete;           template<class... Args,             std::enable_if_t<!negate_invocable_v<const F&, Args...>, int> = 0>         void operator()(Args&&...) const& = delete;           template<class... Args,             std::enable_if_t<!negate_invocable_v<F, Args...>, int> = 0>         void operator()(Args&&...) && = delete;           template<class... Args,             std::enable_if_t<!negate_invocable_v<const F, Args...>, int> = 0>         void operator()(Args&&...) const&& = delete;     }; }   template<class F> constexpr detail::not_fn_t<std::decay_t<F>> not_fn(F&& f) {     return {std::forward<F>(f)}; } ``` |
| (2) not_fn |
| ```text namespace detail {     template<auto ConstFn>     struct stateless_not_fn     {         template<class... Args>         constexpr auto operator()(Args&&... args) const             noexcept(noexcept(!std::invoke(ConstFn, std::forward<Args>(args)...)))             -> decltype(!std::invoke(ConstFn, std::forward<Args>(args)...))         {             return !std::invoke(ConstFn, std::forward<Args>(args)...);         }     }; }   template<auto ConstFn> constexpr detail::stateless_not_fn<ConstFn> not_fn() noexcept {     if constexpr (std::is_pointer_v<decltype(ConstFn)> ||                   std::is_member_pointer_v<decltype(ConstFn)>)         static_assert(ConstFn != nullptr);       return {}; } ``` |

### Notes

`std::not_fn` is intended to replace the C++03-era negators std::not1 and std::not2.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_not_fn` | `201603L` | (C++17) | `std::not_fn()`, (1) |
| `202306L` | (C++26) | Allow passing callable objects as non-type template arguments to `std::not_fn`, (2) |

### Example

Run this code

```
#include <cassert>
#include <functional>
 
bool is_same(int a, int b) noexcept
{
    return a == b;
}
 
struct S
{
    int val;
    bool is_same(int arg) const noexcept { return val == arg; }
};
 
int main()
{
    // Using with a free function:
    auto is_differ = std::not_fn(is_same);
    assert(is_differ(8, 8) == false); // equivalent to: !is_same(8, 8) == false
    assert(is_differ(6, 9) == true); // equivalent to: !is_same(8, 0) == true
 
    // Using with a member function:
    auto member_differ = std::not_fn(&S::is_same);
    assert(member_differ(S{3}, 3) == false); //: S tmp{6}; !tmp.is_same(6) == false
 
    // Noexcept-specification is preserved:
    static_assert(noexcept(is_differ) == noexcept(is_same));
    static_assert(noexcept(member_differ) == noexcept(&S::is_same));
 
    // Using with a function object:
    auto same = [](int a, int b) { return a == b; };
    auto differ = std::not_fn(same);
    assert(differ(1, 2) == true); //: !same(1, 2) == true
    assert(differ(2, 2) == false); //: !same(2, 2) == false
 
#if __cpp_lib_not_fn >= 202306L
    auto is_differ_cpp26 = std::not_fn<is_same>();
    assert(is_differ_cpp26(8, 8) == false);
    assert(is_differ_cpp26(6, 9) == true);
 
    auto member_differ_cpp26 = std::not_fn<&S::is_same>();
    assert(member_differ_cpp26(S{3}, 3) == false);
 
    auto differ_cpp26 = std::not_fn<same>();
    static_assert(differ_cpp26(1, 2) == true);
    static_assert(differ_cpp26(2, 2) == false);
#endif
}

```

### See also

|  |  |
| --- | --- |
| not1(deprecated in C++17)(removed in C++20) | constructs custom std::unary_negate object   (function template) |
| not2(deprecated in C++17)(removed in C++20) | constructs custom std::binary_negate object   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/functional/not_fn&oldid=168656>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 January 2024, at 03:02.