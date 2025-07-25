# std::experimental::reduce, std::experimental::hmin, std::experimental::hmax

From cppreference.com
< cpp‎ | experimental‎ | simd
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****reducehminhmax**** | | | | | |
| Mask reduction | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_ofsome_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | popcount | | | | | | find_first_setfind_last_set | | | | | |  | | | | | |
| Traits | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_simdis_simd_mask | | | | | | is_abi_tag | | | | | | is_simd_flag_type | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | simd_size | | | | | | memory_alignment | | | | | | rebind_simdresize_simd | | | | | |
| Math functions | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/simd>` |  |  |
| template< class T, class Abi, class BinaryOperation = std::plus<> >  T reduce( const simd<T, Abi>& v, BinaryOperation binary_op = {} ); | (1) | (parallelism TS v2) |
| template< class M, class V, class BinaryOperation >  typename V::value_type  reduce( const const_where_expression<M, V>& x, typename V::value_type identity_element, BinaryOperation binary_op = {} ); | (2) | (parallelism TS v2) |
| template< class M, class V >  typename V::value_type reduce( const const_where_expression<M, V>& x, std::plus<> binary_op ) noexcept; | (3) | (parallelism TS v2) |
| template< class M, class V >  typename V::value_type reduce( const const_where_expression<M, V>& x, std::multiplies<> binary_op ) noexcept; | (4) | (parallelism TS v2) |
| template< class M, class V >  typename V::value_type reduce( const const_where_expression<M, V>& x, std::bit_and<> binary_op ) noexcept; | (5) | (parallelism TS v2) |
| template< class M, class V >  typename V::value_type reduce( const const_where_expression<M, V>& x, std::bit_or<> binary_op ) noexcept; | (6) | (parallelism TS v2) |
| template< class M, class V >  typename V::value_type reduce( const const_where_expression<M, V>& x, std::bit_xor<> binary_op ) noexcept; | (7) | (parallelism TS v2) |
| template< class T, class Abi >  T hmin( const simd<T, Abi>& v ) noexcept; | (8) | (parallelism TS v2) |
| template< class M, class V >  typename V::value_type hmin( const const_where_expression<M, V>& x ) noexcept; | (9) | (parallelism TS v2) |
| template< class T, class Abi >  T hmax( const simd<T, Abi>& v ) noexcept; | (10) | (parallelism TS v2) |
| template< class M, class V >  typename V::value_type hmax( const const_where_expression<M, V>& x ) noexcept; | (11) | (parallelism TS v2) |
|  |  |  |

1) Reduces all values in v over binary_op.2) Reduces the values in x where the associated mask element is true over binary_op.3) Returns the sum of all values in x where the associated mask element is true.4) Returns the product of all values in x where the associated mask element is true.5) Returns the aggregation using bitwise-and of all values in x where the associated mask element is true.6) Returns the aggregation using bitwise-or of all values in x where the associated mask element is true.7) Returns the aggregation using bitwise-xor of all values in x where the associated mask element is true.8) Reduces all values in v over std::min.9) Reduces all values in x where the associated mask element is true over std::min.10) Reduces all values in v over std::max.11) Reduces all values in x where the associated mask element is true over std::max.

The behavior is non-deterministic if binary_op is not associative or not commutative.

### Parameters

|  |  |  |
| --- | --- | --- |
| v | - | the `simd` vector to apply the reduction to |
| x | - | the return value of a `where` expression to apply the reduction to |
| identity_element | - | a value that acts as identity element for binary_op; binary_op(identity_element, a) == a must hold for all finite a of type V::value_type |
| binary_op | - | binary FunctionObject that will be applied in unspecified order to arguments of type V::value_type or simd<V::value_type, A>, with unspecified ABI tag `A`. binary_op(v, v) must be convertible to `V` |

### Return value

The result of operation of the type:

1,8,10) `T`2-7,9,11) V::value_type

### Example

Run this code

```
#include <array>
#include <cassert>
#include <cstddef>
#include <experimental/simd>
#include <functional>
#include <iostream>
#include <numeric>
namespace stdx = std::experimental;
 
int main()
{
    using V = stdx::native_simd<double>;
 
    alignas(stdx::memory_alignment_v<V>) std::array<V::value_type, 1024> data;
    std::iota(data.begin(), data.end(), 0);
 
    V::value_type acc{};
    for (std::size_t i = 0; i < data.size(); i += V::size())
        acc += stdx::reduce(V(&data[i], stdx::vector_aligned), std::plus{});
    std::cout << "sum of data = " << acc << '\n';
 
    using W = stdx::fixed_size_simd<int, 4>;
    alignas(stdx::memory_alignment_v<W>) std::array<int, 4> arr{2, 5, 4, 1};
    auto w = W(&arr[0], stdx::vector_aligned);
    assert(stdx::hmin(w) == 1 and stdx::hmax(w) == 5);
}

```

Output:

```
sum of data = 523776

```

### See also

|  |  |
| --- | --- |
| reduce(C++17) | similar to std::accumulate, except out of order   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/simd/reduce&oldid=159775>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 September 2023, at 09:51.