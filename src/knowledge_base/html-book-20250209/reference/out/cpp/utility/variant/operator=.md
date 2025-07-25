# std::variant<Types...>::operator=

From cppreference.com
< cpp‎ | utility‎ | variant
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

std::variant

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| variant::variant | | | | |
| variant::~variant | | | | |
| ****variant::operator=**** | | | | |
| Observers | | | | |
| variant::index | | | | |
| variant::valueless_by_exception | | | | |
| Modifiers | | | | |
| variant::emplace | | | | |
| variant::swap | | | | |
| Visitation | | | | |
| variant::visit(C++26) | | | | |
| Non-member functions | | | | |
| visit(std::variant) | | | | |
| holds_alternative | | | | |
| get(std::variant) | | | | |
| get_if | | | | |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++20) | | | | |
| swap(std::variant) | | | | |
| Helper classes | | | | |
| monostate | | | | |
| bad_variant_access | | | | |
| variant_size | | | | |
| variant_alternative | | | | |
| hash<std::variant> | | | | |
| Helper objects | | | | |
| variant_npos | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr variant& operator=( const variant& rhs ); | (1) | (since C++17) |
| constexpr variant& operator=( variant&& rhs ) noexcept(/\* see below \*/); | (2) | (since C++17) |
| template< class T >  variant& operator=( T&& t ) noexcept(/\* see below \*/); | (3) | (since C++17)  (constexpr since C++20) |
|  |  |  |

Assigns a new value to an existing `variant` object.

1) Copy-assignment:

- If both \*this and rhs are valueless by exception, does nothing.
- Otherwise, if rhs is valueless, but \*this is not, destroys the value contained in \*this and makes it valueless.
- Otherwise, if rhs holds the same alternative as \*this, assigns the value contained in rhs to the value contained in \*this. If an exception is thrown, \*this does not become valueless: the value depends on the exception safety guarantee of the alternative's copy assignment.
- Otherwise, if the alternative held by rhs is either nothrow copy constructible or **not** nothrow move constructible (as determined by std::is_nothrow_copy_constructible and std::is_nothrow_move_constructible, respectively), equivalent to this->emplace<rhs.index()>(\*std::get_if<rhs.index()>(std::addressof(rhs))). \*this may become `valueless_by_exception` if an exception is thrown on the copy-construction inside `emplace`.
- Otherwise, equivalent to this->operator=(variant(rhs)).
 This overload is defined as deleted unless std::is_copy_constructible_v<T_i> and std::is_copy_assignable_v<T_i> are both true for all `T_i` in `Types...`. This overload is trivial if std::is_trivially_copy_constructible_v<T_i>,std::is_trivially_copy_assignable_v<T_i> and std::is_trivially_destructible_v<T_i> are all true for all `T_i` in `Types...`.2) Move-assignment:

- If both \*this and rhs are valueless by exception, does nothing.
- Otherwise, if rhs is valueless, but \*this is not, destroys the value contained in \*this and makes it valueless.
- Otherwise, if rhs holds the same alternative as \*this, assigns std::move(\*std::get_if<j>(std::addressof(rhs))) to the value contained in \*this, with `j` being `index()`. If an exception is thrown, \*this does not become valueless: the value depends on the exception safety guarantee of the alternative's move assignment.
- Otherwise (if rhs and \*this hold different alternatives), equivalent to this->emplace<rhs.index()>(std::move(\*std::get_if<rhs.index()>(std::addressof(rhs)))). If an exception is thrown by `T_i`'s move constructor, \*this becomes `valueless_by_exception`.
 This overload participates in overload resolution only if std::is_move_constructible_v<T_i> and std::is_move_assignable_v<T_i> are both true for all `T_i` in `Types...`. This overload is trivial if std::is_trivially_move_constructible_v<T_i>, std::is_trivially_move_assignable_v<T_i>, and std::is_trivially_destructible_v<T_i> are all true for all `T_i` in `Types...`.3) Converting assignment.

- Determines the alternative type `T_j` that would be selected by overload resolution for the expression F(std::forward<T>(t)) if there was an overload of imaginary function F(T_i) for every `T_i` from `Types...` in scope at the same time, except that:

:   - An overload F(T_i) is only considered if the declaration T_i x[] = { std::forward<T>(t) }; is valid for some invented variable `x`;

- If \*this already holds a `T_j`, assigns std::forward<T>(t) to the value contained in \*this. If an exception is thrown, \*this does not become valueless: the value depends on the exception safety guarantee of the assignment called.
- Otherwise, if std::is_nothrow_constructible_v<T_j, T> || !std::is_nothrow_move_constructible_v<T_j> is true, equivalent to this->emplace<j>(std::forward<T>(t)). \*this may become `valueless_by_exception` if an exception is thrown on the initialization inside `emplace`.
- Otherwise, equivalent to this->emplace<j>(T_j(std::forward<T>(t))).

This overload participates in overload resolution only if std::decay_t<T>(until C++20)std::remove_cvref_t<T>(since C++20) is not the same type as `variant` and std::is_assignable_v<T_j&, T> is true and std::is_constructible_v<T_j, T> is true and the expression F(std::forward<T>(t)) (with F being the above-mentioned set of imaginary functions) is well formed.

```
std::variant<std::string> v1;
v1 = "abc"; // OK
std::variant<std::string, std::string> v2;
v2 = "abc"; // Error
std::variant <std::string, bool> v3;
v3 = "abc"; // OK, chooses string; bool is not a candidate
std::variant<float, long, double> v4; // holds float
v4 = 0; // OK, holds long; float and double are not candidates

```

### Parameters

|  |  |  |
| --- | --- | --- |
| rhs | - | another `variant` |
| t | - | a value convertible to one of the variant's alternatives |

### Return value

\*this

### Exceptions

1) May throw any exception thrown by assignment and copy/move initialization of any alternative.2)noexcept specification:noexcept(((std::is_nothrow_move_constructible_v<Types> &&  
           std::is_nothrow_move_assignable_v<Types>) && ...))3)noexcept specification:noexcept(std::is_nothrow_assignable_v<T_j&, T> &&  
         std::is_nothrow_constructible_v<T_j, T>)

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_variant` | `202106L` | (C++20) (DR) | Fully constexpr `std::variant` (3) |

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <string>
#include <type_traits>
#include <variant>
 
std::ostream& operator<<(std::ostream& os, std::variant<int, std::string> const& va)
{
    os << ": { ";
 
    std::visit(&
    {
        using T = std::decay_t<decltype(arg)>;
        if constexpr (std::is_same_v<T, int>)
            os << arg;
        else if constexpr (std::is_same_v<T, std::string>)
            os << std::quoted(arg);
    }, va);
 
    return os << " };\n";
}
 
int main()
{
    std::variant<int, std::string> a{2017}, b{"CppCon"};
    std::cout << "a" << a << "b" << b << '\n';
 
    std::cout << "(1) operator=( const variant& rhs )\n";
    a = b;
    std::cout << "a" << a << "b" << b << '\n';
 
    std::cout << "(2) operator=( variant&& rhs )\n";
    a = std::move(b);
    std::cout << "a" << a << "b" << b << '\n';
 
    std::cout << "(3) operator=( T&& t ), where T is int\n";
    a = 2019;
    std::cout << "a" << a << '\n';
 
    std::cout << "(3) operator=( T&& t ), where T is std::string\n";
    std::string s{"CppNow"};
    std::cout << "s: " << std::quoted(s) << '\n';
    a = std::move(s);
    std::cout << "a" << a << "s: " << std::quoted(s) << '\n';
}

```

Possible output:

```
a: { 2017 };
b: { "CppCon" };
 
(1) operator=( const variant& rhs )
a: { "CppCon" };
b: { "CppCon" };
 
(2) operator=( variant&& rhs )
a: { "CppCon" };
b: { "" };
 
(3) operator=( T&& t ), where T is int
a: { 2019 };
 
(3) operator=( T&& t ), where T is std::string
s: "CppNow"
a: { "CppNow" };
s: ""

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3024 | C++17 | copy assignment operator doesn't participate in overload resolution if any member type is not copyable | defined as deleted instead |
| LWG 3585 | C++17 | converting assignment was sometimes unexpectedly ill-formed because there was no available move assignment | made well-formed |
| P0602R4 | C++17 | copy/move assignment may not be trivial even if underlying operations are trivial | required to propagate triviality |
| P0608R3 | C++17 | converting assignment blindly assembles an overload set, leading to unintended conversions | narrowing and boolean conversions not considered |
| P2231R1 | C++20 | converting assignment (3) was not constexpr while the required operations can be constexpr in C++20 | made constexpr |

### See also

|  |  |
| --- | --- |
| emplace | constructs a value in the `variant`, in place   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/variant/operator%3D&oldid=172844>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 June 2024, at 15:15.