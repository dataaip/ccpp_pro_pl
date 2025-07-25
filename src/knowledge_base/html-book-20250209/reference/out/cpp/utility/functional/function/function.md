# std::function<R(Args...)>::function

From cppreference.com
< cpp‎ | utility‎ | functional‎ | function
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

std::function

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****function::function**** | | | | |
| function::~function | | | | |
| function::operator= | | | | |
| function::swap | | | | |
| function::assign(until C++17) | | | | |
| function::operator bool | | | | |
| function::operator()") | | | | |
| function::target_type | | | | |
| function::target | | | | |
| Non-member functions | | | | |
| operator==operator!=(until C++20) | | | | |
| swap(std::function) | | | | |
| Helper classes | | | | |
| uses_allocator<std::function>(until C++17) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| function() noexcept; | (1) | (since C++11) |
| function( std::nullptr_t ) noexcept; | (2) | (since C++11) |
| function( const function& other ); | (3) | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| function( function&& other ); |  | (since C++11)  (until C++20) |
| function( function&& other ) noexcept; |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
| template< class F >   function( F&& f ); | (5) | (since C++11) |
| template< class Alloc >   function( std::allocator_arg_t, const Alloc& alloc ) noexcept; | (6) | (since C++11)  (removed in C++17) |
| template< class Alloc >   function( std::allocator_arg_t, const Alloc& alloc, std::nullptr_t ) noexcept; | (7) | (since C++11)  (removed in C++17) |
| template< class Alloc >   function( std::allocator_arg_t, const Alloc& alloc, const function& other ); | (8) | (since C++11)  (removed in C++17) |
| template< class Alloc >   function( std::allocator_arg_t, const Alloc& alloc,           function&& other ); | (9) | (since C++11)  (removed in C++17) |
| template< class F, class Alloc >   function( std::allocator_arg_t, const Alloc& alloc, F f ); | (10) | (since C++11)  (removed in C++17) |
|  |  |  |

Constructs a `std::function` from a variety of sources.

1,2) Creates an empty `std::function`.3) Copies the target of other to the target of \*this. If other is empty, \*this will be empty right after the call too.4) Moves the target of other to the target of \*this. If other is empty, \*this will be empty right after the call too. other is in a valid but unspecified state right after the call.5) Initializes the target with std::forward<F>(f). The target is of type std::decay<F>::type. If f is a null pointer to function, a null pointer to member, or an empty value of some `std::function` specialization, \*this will be empty right after the call. This overload participates in overload resolution only if all following conditions are satisfied:

|  |  |
| --- | --- |
| - std::is_same_v<std::remove_cvref_t<F>, std::function<R(Args...)> is false. | (since C++23) |

- An lvalue of type std::decay<F>::type is callable for argument types `Args...` and return type `R`.

|  |  |
| --- | --- |
| If std::is_copy_constructible_v<std::decay_t<F>> or std::is_constructible_v<std::decay_t<F>, F> is false, the program is ill-formed. | (since C++23) |

 If `F` is not CopyConstructible, the behavior is undefined.6-10) Same as (1-5) except that alloc is used to allocate memory for any internal data structures that the `std::function` might use.

When the target is a function pointer or a std::reference_wrapper, small object optimization is guaranteed, that is, these targets are always directly stored inside the std::function object, no dynamic allocation takes place. Other large objects may be constructed in dynamic allocated storage and accessed by the std::function object through a pointer.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | the function object used to initialize \*this |
| f | - | a callable object used to initialize \*this |
| alloc | - | an Allocator used for internal memory allocation |
| Type requirements | | |
| -`Alloc` must meet the requirements of Allocator. | | |

### Exceptions

3,8,9) Does not throw if other's target is a function pointer or a std::reference_wrapper, otherwise may throw std::bad_alloc or any exception thrown by the constructor used to copy or move the stored callable object.

|  |  |
| --- | --- |
| 4) Does not throw if other's target is a function pointer or a std::reference_wrapper, otherwise may throw std::bad_alloc or any exception thrown by the constructor used to copy or move the stored callable object. | (until C++20) |

5,10) Does not throw if f is a function pointer or a std::reference_wrapper, otherwise may throw std::bad_alloc or any exception thrown by the copy constructor of the stored callable object.

### Notes

`std::function`'s allocator support was poorly specified and inconsistently implemented. Some implementations do not provide overloads (6-10) at all, some provide the overloads but ignore the supplied allocator argument, and some provide the overloads and use the supplied allocator for construction but not when the `std::function` is reassigned. As a result, allocator support was removed in C++17.

### Example

Run this code

```
#include <functional>
#include <iostream>
#include <utility>
 
void print_num(int i) { std::cout << "print_num(" << i << ")\n"; }
 
int main()
{
    std::function<void(int)> func1; // (1) empty constructor
    try
    {
        func1(333 << 1);
    }
    catch (const std::bad_function_call& ex)
    {
        std::cout << "1) " << ex.what() << '\n';
    }
 
    std::function<void(int)> func2{nullptr}; // (2) empty constructor
    try
    {
        func1(222 * 3);
    }
    catch (const std::bad_function_call& ex)
    {
        std::cout << "2) " << ex.what() << '\n';
    }
 
    func1 = print_num; // initializes func1 using assignment operator
 
    std::function<void(int)> func3{func1}; // (3) copy constructor
    func3(33);
 
    std::function<void(int)> func4{std::move(func3)}; // (4) move constructor,
                                                      // func3 in unspecified state
    func4(44);
 
    std::function<void(int)> func5{print_num}; // (5) constructor with function
    func5(55);
 
    // (5) constructor with lambda
    std::function<void(int)> func6([](int i) { std::cout << "lambda(" << i << ")\n"; });
    func6(66);
}

```

Possible output:

```
1) bad_function_call
2) bad_function_call
print_num(33)
print_num(44)
print_num(55)
lambda(66)

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2132 | C++11 | overloads (5,10) might be ambiguous | constrained |
| LWG 2774 | C++11 | (5,10) performed an additional move | eliminated |

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a new `std::move_only_function` object   (public member function of `std::move_only_function`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/functional/function/function&oldid=176891>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 October 2024, at 09:04.