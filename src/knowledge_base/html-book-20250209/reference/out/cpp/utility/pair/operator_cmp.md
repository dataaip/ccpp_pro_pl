# operator==,!=,<,<=,>,>=,<=>(std::pair)

From cppreference.com
< cpp‎ | utility‎ | pair
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

std::pair

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| pair::pair | | | | |
| pair::operator= | | | | |
| pair::swap(C++11) | | | | |
| Non-member functions | | | | |
| make_pair | | | | |
| ****operator==operator!=operator<operator<=operator>operator>=operator<=>****(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | |
| swap(std::pair)(C++11) | | | | |
| get(std::pair)(C++11) | | | | |
| Helper classes | | | | |
| tuple_size<std::pair>(C++11) | | | | |
| tuple_element<std::pair>(C++11) | | | | |
| basic_common_reference<std::pair>(C++23) | | | | |
| common_type<std::pair>(C++23) | | | | |
| formatter<std::pair>(C++23) | | | | |
| piecewise_construct_t(C++11) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<utility>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| template< class T1, class T2, class U1, class U2 >  bool operator==( const std::pair<T1, T2>& lhs, const std::pair<U1, U2>& rhs ); |  | (until C++14) |
| template< class T1, class T2, class U1, class U2 >  constexpr bool operator==( const std::pair<T1, T2>& lhs, const std::pair<U1, U2>& rhs ); |  | (since C++14) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| template< class T1, class T2, class U1, class U2 >  bool operator!=( const std::pair<T1, T2>& lhs, const std::pair<U1, U2>& rhs ); |  | (until C++14) |
| template< class T1, class T2, class U1, class U2 >  constexpr bool operator!=( const std::pair<T1, T2>& lhs, const std::pair<U1, U2>& rhs ); |  | (since C++14)  (until C++20) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| template< class T1, class T2, class U1, class U2 >  bool operator<( const std::pair<T1, T2>& lhs, const std::pair<U1, U2>& rhs ); |  | (until C++14) |
| template< class T1, class T2, class U1, class U2 >  constexpr bool operator<( const std::pair<T1, T2>& lhs, const std::pair<U1, U2>& rhs ); |  | (since C++14)  (until C++20) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| template< class T1, class T2, class U1, class U2 >  bool operator<=( const std::pair<T1, T2>& lhs, const std::pair<U1, U2>& rhs ); |  | (until C++14) |
| template< class T1, class T2, class U1, class U2 >  constexpr bool operator<=( const std::pair<T1, T2>& lhs, const std::pair<U1, U2>& rhs ); |  | (since C++14)  (until C++20) |
|  |  |  |
| --- | --- | --- |
|  | (5) |  |
| template< class T1, class T2, class U1, class U2 >  bool operator>( const std::pair<T1, T2>& lhs, const std::pair<U1, U2>& rhs ); |  | (until C++14) |
| template< class T1, class T2, class U1, class U2 >  constexpr bool operator>( const std::pair<T1, T2>& lhs, const std::pair<U1, U2>& rhs ); |  | (since C++14)  (until C++20) |
|  |  |  |
| --- | --- | --- |
|  | (6) |  |
| template< class T1, class T2, class U1, class U2 >  bool operator>=( const std::pair<T1, T2>& lhs, const std::pair<U1, U2>& rhs ); |  | (until C++14) |
| template< class T1, class T2, class U1, class U2 >  constexpr bool operator>=( const std::pair<T1, T2>& lhs, const std::pair<U1, U2>& rhs ); |  | (since C++14)  (until C++20) |
|  |  |  |
| --- | --- | --- |
| template< class T1, class T2, class U1, class U2 >  constexpr std::common_comparison_category_t<synth-three-way-result<T1, U1>,                                              synth-three-way-result<T2, U2>>     operator<=>( const std::pair<T1, T2>& lhs, const std::pair<U1, U2>& rhs ); | (7) | (since C++20) |
|  |  |  |

1,2) Tests if both elements of lhs and rhs are equal, that is, compares lhs.first with rhs.first and lhs.second with rhs.second.  

|  |  |
| --- | --- |
| The behavior is undefined if the type and value category of either lhs.first == rhs.first or lhs.second == rhs.second do not meet the BooleanTestable requirements. | (until C++26) |
| This overload participates in overload resolution only if both decltype(lhs.first == rhs.first) and decltype(lhs.second == rhs.second) model `boolean-testable`. | (since C++26) |

3-6) Compares lhs and rhs lexicographically by operator<, that is, compares the first elements and only if they are equivalent, compares the second elements. The behavior is undefined if the type and value category of any of lhs.first < rhs.first, rhs.first < lhs.first, or lhs.second < rhs.second do not meet the BooleanTestable requirements.7) Compares lhs and rhs lexicographically by **synth-three-way**, that is, compares the first elements and only if they are equivalent, compares the second elements. **synth-three-way-result** is the return type of `synth-three-way`.

|  |  |
| --- | --- |
| The `<`, `<=`, `>`, `>=`, and `!=` operators are synthesized from operator<=> and operator== respectively. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | pairs to compare |

### Return value

1) true if both lhs.first == rhs.first and lhs.second == rhs.second, otherwise false.2) !(lhs == rhs)3) If lhs.first < rhs.first, returns true. Otherwise, if rhs.first < lhs.first, returns false. Otherwise, if lhs.second < rhs.second, returns true. Otherwise, returns false.4) !(rhs < lhs)5) rhs < lhs6) !(lhs < rhs)7) **synth-three-way**(lhs.first, rhs.first) if it is not equal to ​0​, otherwise **synth-three-way**(lhs.second, rhs.second).

### Notes

|  |  |
| --- | --- |
| The relational operators are defined in terms of each element's operator<. | (until C++20) |
| The relational operators are defined in terms of **synth-three-way**, which uses operator<=> if possible, or operator< otherwise.  Notably, if an element type does not itself provide operator<=>, but is implicitly convertible to a three-way comparable type, that conversion will be used instead of operator<. | (since C++20) |

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_constrained_equality` | `202403L` | (C++26) | Constrained operator== for std::pair |

### Example

Because operator< is defined for pairs, containers of pairs can be sorted.

Run this code

```
#include <algorithm>
#include <iomanip>
#include <iostream>
#include <string>
#include <utility>
#include <vector>
 
int main()
{
    std::vector<std::pair<int, std::string>> v = {{2, "baz"}, {2, "bar"}, {1, "foo"}};
    std::sort(v.begin(), v.end());
 
    for (auto p : v)
        std::cout << '{' << p.first << ", " << std::quoted(p.second) << "}\n";
}

```

Output:

```
{1, "foo"}
{2, "bar"}
{2, "baz"}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 296 | C++98 | the descriptions of operators other than `==` and `<` were missing | added |
| LWG 2114 (P2167R3) | C++98 | type preconditions for boolean operations were missing | added |
| LWG 3865 | C++98 | comparison operators only accepted `pair`s of the same type | accept `pair`s of different types |

### See also

|  |  |
| --- | --- |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values in the tuple   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/pair/operator_cmp&oldid=175970>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 September 2024, at 07:15.