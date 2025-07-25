# std::experimental::simd<T,Abi>::operator==,!=,<,<=,>,>=

From cppreference.com
< cpp‎ | experimental‎ | simd‎ | simd
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Extensions for parallelism v2

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Parallel exceptions | | | | |
| exception_list") | | | | |
| Additional execution policies | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | execution::vector_policy") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | execution::unsequenced_policy") | | | | | |
| Algorithms | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | induction") | | | | | | reductionreduction_plusreduction_minusreduction_multiplies") | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reduction_bit_andreduction_bit_orreduction_bit_xorreduction_minreduction_max") | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_loopfor_loop_stridedfor_loop_nfor_loop_n_strided") | | | | | |  | | | | | |  | | | | | |
| execution::no_vec") | | | | |
| execution::ordered_update_t") | | | | |
| Task blocks | | | | |
| task_block") | | | | |
| task_cancelled_exception") | | | | |
| define_task_blockdefine_task_block_restore_thread") | | | | |
| Data-parallel vectors | | | | |

SIMD library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Main classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | simd | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | simd_mask | | | | | |
| ABI tags | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | simd_abi::scalar | | | | | | simd_abi::fixed_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | simd_abi::native | | | | | | simd_abi::compatible | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | simd_abi::max_fixed_size | | | | | | simd_abi::deduce | | | | | |
| Alignment tags | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | element_aligned_tagelement_aligned | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vector_aligned_tagvector_aligned | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | overaligned_tagoveraligned | | | | | |
| Where expression | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | where | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | where_expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | const_where_expression | | | | | |
| Casts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | simd_caststatic_simd_cast | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | to_fixed_sizeto_compatibleto_native | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | splitsplit_by | | | | | | concat | | | | | |
| Algorithms | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | min | | | | | | max | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | minmax | | | | | | clamp | | | | | |
| Reduction | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | reducehminhmax | | | | | |
| Mask reduction | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_ofsome_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | popcount | | | | | | find_first_setfind_last_set | | | | | |  | | | | | |
| Traits | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_simdis_simd_mask | | | | | | is_abi_tag | | | | | | is_simd_flag_type | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | simd_size | | | | | | memory_alignment | | | | | | rebind_simdresize_simd | | | | | |
| Math functions | | | | |

std::experimental::simd

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | simd | | | | | | copy_from | | | | | | copy_to | | | | | | size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!operator~operator+operator- | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | [operator[]](operator_at.html "cpp/experimental/simd/simd/operator at") | | | | | | operator++operator-- | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+operator-operator\*operator/operator%operator&operator|operator^operator<<operator>> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+=operator-=operator\*=operator/=operator%=operator&=operator|=operator^=operator<<=operator>>= | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****operator==operator!=operator>=operator<=operator>operator<**** | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| friend simd_mask operator==( const simd& lhs, const simd& rhs ) noexcept; | (1) | (parallelism TS v2) |
| friend simd_mask operator!=( const simd& lhs, const simd& rhs ) noexcept; | (2) | (parallelism TS v2) |
| friend simd_mask operator<( const simd& lhs, const simd& rhs ) noexcept; | (3) | (parallelism TS v2) |
| friend simd_mask operator<=( const simd& lhs, const simd& rhs ) noexcept; | (4) | (parallelism TS v2) |
| friend simd_mask operator>( const simd& lhs, const simd& rhs ) noexcept; | (5) | (parallelism TS v2) |
| friend simd_mask operator>=( const simd& lhs, const simd& rhs ) noexcept; | (6) | (parallelism TS v2) |
|  |  |  |

Applies the given comparison element-wise to each corresponding element of the operands.
Returns a simd_mask such that for all i in the range of ``​0​`,`[`size()``)` the ith element equals:

1) lhs[i] == rhs[i].2) lhs[i] != rhs[i].3) lhs[i] <  rhs[i].4) lhs[i] <= rhs[i].5) lhs[i] >  rhs[i].6) lhs[i] >= rhs[i].

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs | - | left operands |
| rhs | - | right operands |

### Example

Run this code

```
#include <cassert>
#include <iostream>
#include <initializer_list>
#include <iterator>
 
#include <experimental/simd>
namespace stdx = std::experimental;
 
int main()
{
    using V = stdx::fixed_size_simd<int, 4>;
    using M = stdx::fixed_size_simd_mask<int, 4>;
 
    auto assert_equivalence = [](M&& x, std::initializer_list<int>&& y)
    {
        for (decltype(M::size()) i{}; i != M::size(); ++i)
            assert(x[i] == std::cbegin(y)[i]);
    };
 
    V a{2}, b, c{3};
    b[0] = 1, b[1] = 2, b[2] = 3, b[3] = 4;
 
    // a == {2, 2, 2, 2}
    // b == {1, 2, 3, 4}
    // c == {3, 3, 3, 3}
 
    assert_equivalence(a == a, {1, 1, 1, 1});
    assert_equivalence(a == b, {0, 1, 0, 0});
    assert_equivalence(b == c, {0, 0, 1, 0});
    assert_equivalence(a == c, {0, 0, 0, 0});
 
    assert_equivalence(a != a, {0, 0, 0, 0});
    assert_equivalence(a != b, {1, 0, 1, 1});
    assert_equivalence(b != c, {1, 1, 0, 1});
    assert_equivalence(a != c, {1, 1, 1, 1});
 
    assert_equivalence(a < a, {0, 0, 0, 0});
    assert_equivalence(a < b, {0, 0, 1, 1});
    assert_equivalence(b < c, {1, 1, 0, 0});
    assert_equivalence(a < c, {1, 1, 1, 1});
}

```

### See also

|  |  |
| --- | --- |
| all_ofany_ofnone_ofsome_of(parallelism TS v2) | reductions of simd_mask to bool   (function template) |
| popcount(parallelism TS v2) | reduction of simd_mask to the number of true values   (function template) |
| find_first_setfind_last_set(parallelism TS v2) | reductions of simd_mask to the index of the first or last true value   (function template) |
| simd_mask(parallelism TS v2) | data-parallel type with the element type bool   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/simd/simd/operator_cmp&oldid=158187>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 September 2023, at 02:11.