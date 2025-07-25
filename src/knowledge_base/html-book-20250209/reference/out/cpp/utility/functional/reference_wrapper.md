# std::reference_wrapper

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function invocation | | | | | | invokeinvoke_r(C++17)(C++23) | | | | | | Identity function object | | | | | | identity(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Reference wrappers | | | | | | ****reference_wrapper****(C++11) | | | | | | refcref(C++11)(C++11) | | | | | | unwrap_referenceunwrap_ref_decay(C++20)(C++20) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Operator wrappers | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | plus | | | | | | minus | | | | | | negate | | | | | | multiplies | | | | | | divides | | | | | | modulus | | | | | | bit_and | | | | | | bit_or | | | | | | bit_not(C++14) | | | | | | bit_xor | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_to | | | | | | not_equal_to | | | | | | greater | | | | | | less | | | | | | greater_equal | | | | | | less_equal | | | | | | logical_and | | | | | | logical_or | | | | | | logical_not | | | | | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Transparent operator wrappers | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | plus<>(C++14) | | | | | | minus<>(C++14) | | | | | | negate<>(C++14) | | | | | | multiplies<>(C++14) | | | | | | divides<>(C++14) | | | | | | modulus<>(C++14) | | | | | | bit_and<>(C++14) | | | | | | bit_or<>(C++14) | | | | | | bit_not<>(C++14) | | | | | | bit_xor<>(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_to<>(C++14) | | | | | | not_equal_to<>(C++14) | | | | | | greater<>(C++14) | | | | | | less<>(C++14) | | | | | | greater_equal<>(C++14) | | | | | | less_equal<>(C++14) | | | | | | logical_and<>(C++14) | | | | | | logical_or<>(C++14) | | | | | | logical_not<>(C++14) | | | | | |  | | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Negators | | | | | | not_fn(C++17) | | | | | | Searchers | | | | | | default_searcher(C++17) | | | | | | boyer_moore_searcher(C++17) | | | | | | boyer_moore_horspool_searcher(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constrained comparators | | | | | | ranges::equal_to(C++20) | | | | | | ranges::not_equal_to(C++20) | | | | | | ranges::greater(C++20) | | | | | | ranges::less(C++20) | | | | | | ranges::greater_equal(C++20) | | | | | | ranges::less_equal(C++20) | | | | | | compare_three_way(C++20) | | | | | |
| Old binders and adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unary_function(until C++17\*) | | | | | | binary_function(until C++17\*) | | | | | | ptr_fun(until C++17\*) | | | | | | pointer_to_unary_function(until C++17\*) | | | | | | pointer_to_binary_function(until C++17\*) | | | | | | mem_fun(until C++17\*) | | | | | | mem_fun_tmem_fun1_tconst_mem_fun_tconst_mem_fun1_t(until C++17\*)(until C++17\*)(until C++17\*)(until C++17\*) | | | | | | not1(until C++20\*) | | | | | | not2(until C++20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | binder1stbinder2nd(until C++17\*)(until C++17\*) | | | | | | bind1stbind2nd(until C++17\*)(until C++17\*) | | | | | |  | | | | | | mem_fun_ref(until C++17\*) | | | | | | mem_fun_ref_tmem_fun1_ref_tconst_mem_fun_ref_tconst_mem_fun1_ref_t(until C++17\*)(until C++17\*)(until C++17\*)(until C++17\*) | | | | | | unary_negate(until C++20\*) | | | | | | binary_negate(until C++20\*) | | | | | |

****std::reference_wrapper****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| reference_wrapper::reference_wrapper | | | | |
| reference_wrapper::operator= | | | | |
| reference_wrapper::getreference_wrapper::operator T& | | | | |
| reference_wrapper::operator()") | | | | |
| Non-member functions | | | | |
| operator==operator<=>(C++26)(C++26) | | | | |
| Deduction guides (C++17) | | | | |
| Helper classes | | | | |
| basic_common_reference<std::reference_wrapper>(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<functional>` |  |  |
| template< class T >  class reference_wrapper; |  | (since C++11) |
|  |  |  |

`std::reference_wrapper` is a class template that wraps a reference in a copyable, assignable object.

Specifically, `std::reference_wrapper` is a CopyConstructible and CopyAssignable wrapper around a reference to object or reference to function of type `T`. Instances of `std::reference_wrapper` are objects (they can be copied or stored in containers) but they are implicitly convertible to T&, so that they can be used as arguments with the functions that take the underlying type by reference.

If the stored reference is Callable, `std::reference_wrapper` is callable with the same arguments.

Helper functions std::ref and std::cref are often used to generate `std::reference_wrapper` objects.

`std::reference_wrapper` is used to pass objects by reference to std::bind, the constructor of std::thread, or the helper functions std::make_pair and std::make_tuple. It can also be used as a mechanism to store references inside standard containers (like std::vector) that cannot normally hold references.

|  |  |
| --- | --- |
| `std::reference_wrapper` is guaranteed to be TriviallyCopyable. | (since C++17) |

|  |  |
| --- | --- |
| `T` may be an incomplete type. | (since C++20) |

### Member types

|  |  |
| --- | --- |
| type | definition |
| `type` | `T` |
| `result_type` (deprecated in C++17) (removed in C++20) | The return type of `T` if `T` is a function. Otherwise, not defined. |
| `argument_type` (deprecated in C++17) (removed in C++20) | - if `T` is a function or pointer to function that takes one argument of type `A1`, then `argument_type` is `A1` - if `T` is a pointer to member function of class `T0` that takes no arguments, then `argument_type` is T0\*, possibly cv-qualified - if `T` is a class type with a member type T::argument_type, then `argument_type` is an alias of that |
| `first_argument_type` (deprecated in C++17) (removed in C++20) | - if `T` is a function or pointer to function that takes two arguments of types `A1` and `A2`, then `first_argument_type` is `A1` - if `T` is a pointer to member function of class `T0` that takes one argument, then `first_argument_type` is T0\*, possibly cv-qualified - if `T` is a class type with a member type T::first_argument_type, then `first_argument_type` is an alias of that |
| `second_argument_type` (deprecated in C++17) (removed in C++20) | - if `T` is a function or pointer to function that takes two arguments of type s `A1` and `A2`, then `second_argument_type` is `A2` - if `T` is a pointer to member function of class `T0` that takes one argument `A1`, then `second_argument_type` is `A1`, possibly cv-qualified - if `T` is a class type with a member type T::second_argument_type, then `second_argument_type` is an alias of that |

### Member functions

|  |  |
| --- | --- |
| (constructor) | stores a reference in a new ****std::reference_wrapper**** object   (public member function) |
| operator= | rebinds a ****std::reference_wrapper****   (public member function) |
| getoperator T& | accesses the stored reference   (public member function) |
| operator()") | calls the stored function   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator<=>(C++26) | compares `reference_wrapper` objects as their stored references   (function) |

### Deduction guides(since C++17)

### Helper classes

|  |  |
| --- | --- |
| std::basic_common_reference<std::reference_wrapper>(C++23) | determines the common reference type of `reference_wrapper` and non-`reference_wrapper`   (class template specialization) |

### Possible implementation

|  |
| --- |
| ```text namespace detail {     template<class T> constexpr T& FUN(T& t) noexcept { return t; }     template<class T> void FUN(T&&) = delete; }   template<class T> class reference_wrapper { public:     // types     using type = T;       // construct/copy/destroy     template<class U, class = decltype(         detail::FUN<T>(std::declval<U>()),         std::enable_if_t<!std::is_same_v<reference_wrapper, std::remove_cvref_t<U>>>()     )>     constexpr reference_wrapper(U&& u)         noexcept(noexcept(detail::FUN<T>(std::forward<U>(u))))         : _ptr(std::addressof(detail::FUN<T>(std::forward<U>(u)))) {}       reference_wrapper(const reference_wrapper&) noexcept = default;       // assignment     reference_wrapper& operator=(const reference_wrapper& x) noexcept = default;       // access     constexpr operator T& () const noexcept { return *_ptr; }     constexpr T& get() const noexcept { return *_ptr; }       template<class... ArgTypes>     constexpr std::invoke_result_t<T&, ArgTypes...>         operator() (ArgTypes&&... args ) const             noexcept(std::is_nothrow_invocable_v<T&, ArgTypes...>)     {         return std::invoke(get(), std::forward<ArgTypes>(args)...);     }   private:     T* _ptr; };   // deduction guides template<class T> reference_wrapper(T&) -> reference_wrapper<T>; ``` |

### Example

Demonstrates the use of `std::reference_wrapper` as a container of references, which makes it possible to access the same container using multiple indices.

Run this code

```
#include <algorithm>
#include <functional>
#include <iostream>
#include <list>
#include <numeric>
#include <random>
#include <vector>
 
void println(auto const rem, std::ranges::range auto const& v)
{
    for (std::cout << rem; auto const& e : v)
        std::cout << e << ' ';
    std::cout << '\n';
}
 
int main()
{
    std::list<int> l(10);
    std::iota(l.begin(), l.end(), -4);
 
    // can't use shuffle on a list (requires random access), but can use it on a vector
    std::vector<std::reference_wrapper<int>> v(l.begin(), l.end());
 
    std::ranges::shuffle(v, std::mt19937{std::random_device{}()});
 
    println("Contents of the list: ", l);
    println("Contents of the list, as seen through a shuffled vector: ", v);
 
    std::cout << "Doubling the values in the initial list...\n";
    std::ranges::for_each(l, [](int& i) { i *= 2; });
 
    println("Contents of the list, as seen through a shuffled vector: ", v);
}

```

Possible output:

```
Contents of the list: -4 -3 -2 -1 0 1 2 3 4 5
Contents of the list, as seen through a shuffled vector: -1 2 -2 1 5 0 3 -3 -4 4
Doubling the values in the initial list...
Contents of the list, as seen through a shuffled vector: -2 4 -4 2 10 0 6 -6 -8 8

```

### See also

|  |  |
| --- | --- |
| refcref(C++11)(C++11) | creates a ****std::reference_wrapper**** with a type deduced from its argument   (function template) |
| bind(C++11) | binds one or more arguments to a function object   (function template) |
| unwrap_referenceunwrap_ref_decay(C++20)(C++20) | get the reference type wrapped in ****std::reference_wrapper****   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/functional/reference_wrapper&oldid=173390>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 July 2024, at 02:04.