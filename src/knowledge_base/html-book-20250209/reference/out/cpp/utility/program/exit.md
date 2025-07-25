# std::exit

From cppreference.com
< cpp‎ | utility‎ | program
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

Program support utilities

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Program termination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | abort | | | | | | ****exit**** | | | | | | quick_exit(C++11) | | | | | | _Exit(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | atexit | | | | | | at_quick_exit(C++11) | | | | | | EXIT_SUCCESSEXIT_FAILURE | | | | | |
| Unreachable control flow | | | | |
| unreachable(C++23) | | | | |
| Communicating with the environment | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | system | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | getenv | | | | | |
| Signals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | signal | | | | | | raise | | | | | | sig_atomic_t | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIG_DFLSIG_IGN | | | | | | SIG_ERR | | | | | |
| Signal types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGABRTSIGFPESIGILL | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGINTSIGSEGVSIGTERM | | | | | |
| Non-local jumps | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setjmp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | longjmp | | | | | |
| Types | | | | |
| jmp_buf | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstdlib>` |  |  |
|  |  |  |
| --- | --- | --- |
| void exit( int exit_code ); |  | (until C++11) |
| [[noreturn]] void exit( int exit_code ); |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Causes normal program termination to occur.

Several cleanup steps are performed:

|  |  |
| --- | --- |
| 1) Objects with static storage duration are destroyed and functions registered by calling std::atexit are called:a) Non-local objects with static storage duration are destroyed in the reverse order of the completion of their constructor.b) Functions registered with std::atexit are called in the reverse order of their registration, except that a function is called after any previously registered functions that had already been called at the time it was registered.c) For each function f registered with std::atexit and each non-local object obj of static storage duration, - if f is registered before the initialization of obj, f will only be called after the destruction of obj; - if f is registered after the initialization of obj, f will only be called before the destruction of obj. d) For each local object obj with static storage duration, obj is destroyed as if a function calling the destructor of obj were registered with std::atexit at the completion of the constructor of obj. | (until C++11) |
| 1) The destructors of objects with thread local storage duration that are associated with the current thread, the destructors of objects with static storage duration, and the functions registered with std::atexit are executed concurrently, while maintaining the following guarantees:a) The last destructor for thread-local objects is sequenced-before the first destructor for a static object.b) If the completion of the constructor or dynamic initialization for thread-local or static object A was sequenced-before thread-local or static object B, the completion of the destruction of B is sequenced-before the start of the destruction of A.c) If the completion of the initialization of a static object A was sequenced-before the call to std::atexit for some function F, the call to F during termination is sequenced-before the start of the destruction of A.d) If the call to std::atexit for some function F was sequenced-before the completion of initialization of a static object A, the start of the destruction of A is sequenced-before the call to F during termination.e) If a call to std::atexit for some function F1 was sequenced-before the call to std::atexit for some function F2, then the call to F2 during termination is sequenced-before the call to F1. | (since C++11) |

:   - In the above,

    :   - If any function registered with `atexit` or any destructor of static/thread-local object throws an exception, std::terminate is called.
        - If the compiler opted to lift dynamic initialization of an object to the static initialization phase of non-local initialization, the sequencing of destruction honors its would-be dynamic initialization.
        - If a function-local (block-scope) static object was destroyed and then that function is called from the destructor of another static object and the control flow passes through the definition of that object (or if it is used indirectly, via pointer or reference), the behavior is undefined.
        - If a function-local (block-scope) static object was initialized during construction of a subobject of a class or array, it is only destroyed after all subobjects of that class or all elements of that array were destroyed.

2) All C streams are flushed and closed.3) Files created by std::tmpfile are removed.4) Control is returned to the host environment. If `exit_code` is 0 or EXIT_SUCCESS, an implementation-defined status indicating successful termination is returned. If `exit_code` is EXIT_FAILURE, an implementation-defined status indicating unsuccessful termination is returned. In other cases implementation-defined status value is returned.

Stack is not unwound: destructors of variables with automatic storage duration are not called.

### Relationship with the main function

Returning from the main function, either by a `return` statement or by reaching the end of the function performs the normal function termination (calls the destructors of the variables with automatic storage durations) and then executes `std::exit`, passing the argument of the return statement (or ​0​ if implicit return was used) as `exit_code`.

### Parameters

|  |  |  |
| --- | --- | --- |
| exit_code | - | exit status of the program |

### Return value

(none)

### Example

Run this code

```
#include <cstdlib>
#include <iostream>
 
struct Static
{
    ~Static() 
    {
        std::cout << "Static destructor\n";
    }
};
 
struct Local
{
    ~Local() 
    {
        std::cout << "Local destructor\n";
    }
};
 
Static static_variable; // Destructor of this object *will* be called
 
void atexit_handler()
{
    std::cout << "atexit handler\n";
}
 
int main()
{
    Local local_variable; // Destructor of this object will *not* be called
    const int result = std::atexit(atexit_handler); // Handler will be called
 
    if (result != 0)
    {
        std::cerr << "atexit registration failed\n";
        return EXIT_FAILURE;
    }
 
    std::cout << "test\n";
    std::exit(EXIT_FAILURE);
 
    std::cout << "this line will *not* be executed\n";
}

```

Output:

```
test
atexit handler
Static destructor

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3 | C++98 | during cleanup, the behavior was unclear when (1) a function is registered with std::atexit or (2) a static local object is initialized | made clear |

### See also

|  |  |
| --- | --- |
| abort | causes abnormal program termination (without cleaning up)   (function) |
| atexit | registers a function to be called on ****std::exit()**** invocation   (function) |
| quick_exit(C++11) | causes quick program termination without completely cleaning up   (function) |
| at_quick_exit(C++11) | registers a function to be called on std::quick_exit invocation   (function) |
| C documentation for exit | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/program/exit&oldid=161404>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 October 2023, at 21:44.