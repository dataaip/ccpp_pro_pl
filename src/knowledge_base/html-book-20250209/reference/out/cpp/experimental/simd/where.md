# std::experimental::where

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****where**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | where_expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | const_where_expression | | | | | |
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

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/simd>` |  |  |
| template< class T, class Abi >  where_expression<simd_mask<T, Abi>, simd<T, Abi>>      where( const typename simd<T, Abi>::mask_type& mask,            simd<T, Abi>& value ) noexcept; | (1) | (parallelism TS v2) |
| template< class T, class Abi >  const_where_expression<simd_mask<T, Abi>, const simd<T, Abi>>      where( const typename simd<T, Abi>::mask_type& mask, const simd<T, Abi>& value ) noexcept; | (2) | (parallelism TS v2) |
| template< class T, class Abi >  where_expression<simd_mask<T, Abi>, simd_mask<T, Abi>>      where( const type_identity_t<simd_mask<T, Abi>>& mask,            simd_mask<T, Abi>& value ) noexcept; | (3) | (parallelism TS v2) |
| template< class T, class Abi >  const_where_expression<simd_mask<T, Abi>, const simd_mask<T, Abi>>      where( const type_identity_t<simd_mask<T, Abi>>& mask, const simd_mask<T, Abi>& value ) noexcept; | (4) | (parallelism TS v2) |
| template< class T >  where_expression<bool, T>     where( /\*see below\*/ mask, T& value ) noexcept; | (5) | (parallelism TS v2) |
| template< class T >  const_where_expression<bool, const T>     where( /\*see below\*/ mask, const T& value ) noexcept; | (6) | (parallelism TS v2) |
|  |  |  |

Constructs a new `const_where_expression` or `where_expression`.

1-6) Constructs a **where_expression** from given mask and value parameters.

### Parameters

1-4)

|  |  |  |
| --- | --- | --- |
| mask | - | the `simd_mask` object |
| value | - | reference to the `simd` object that mask applies on |

5,6)

|  |  |  |
| --- | --- | --- |
| mask | - | the mask of type bool |
| value | - | reference to the scalar that mask applies on |

### Return value

The constructed `const_where_expression` or `where_expression`.

### Notes

5,6) Uses implementation defined type of mask, so that implicit conversions from other types to bool is disabled.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/simd/where&oldid=159994>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 October 2023, at 07:05.