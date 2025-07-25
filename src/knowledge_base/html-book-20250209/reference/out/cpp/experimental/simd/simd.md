# std::experimental::simd

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****simd**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | simd_mask | | | | | |
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

****std::experimental::simd****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | simd | | | | | | copy_from | | | | | | copy_to | | | | | | size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!operator~operator+operator- | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | [operator[]](simd/operator_at.html "cpp/experimental/simd/simd/operator at") | | | | | | operator++operator-- | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+operator-operator\*operator/operator%operator&operator|operator^operator<<operator>> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+=operator-=operator\*=operator/=operator%=operator&=operator|=operator^=operator<<=operator>>= | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=operator>=operator<=operator>operator< | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/simd>` |  |  |
| template< class T, class Abi = simd_abi::compatible<T> >  class simd; |  | (parallelism TS v2) |
|  |  |  |

The class template `simd` is a data-parallel type. The width of a given `simd` instantiation is a constant expression, determined by the template parameters.

An ABI tag is a type in the `simd_abi` namespace that indicates a choice of size and binary representation for objects of data-parallel type.

### Template parameters

|  |  |  |
| --- | --- | --- |
| T | - | element type; an arithmetic type other than bool |
| Abi | - | tag type used to determine the number of elements and storage |

### Helper alias templates

|  |  |  |
| --- | --- | --- |
| template< class T, int N >  using fixed_size_simd = std::experimental::simd<T, std::experimental::simd_abi::fixed_size<N>>; |  |  |
| template< class T >  using native_simd = std::experimental::simd<T, std::experimental::simd_abi::native<T>>; |  |  |
|  |  |  |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `value_type` | T |
| `reference` | implementation-defined |
| `mask_type` | simd_mask<T, Abi> |
| `abi_type` | Abi |

### Member functions

|  |  |
| --- | --- |
| (constructor)(parallelism TS v2) | constructs a ****simd**** object   (public member function) |
| copy_from(parallelism TS v2) | loads ****simd**** elements from contiguous memory   (public member function) |
| copy_to(parallelism TS v2) | stores ****simd**** elements to contiguous memory   (public member function) |
| [operator[]](simd/operator_at.html "cpp/experimental/simd/simd/operator at")(parallelism TS v2) | accesses specified element   (public member function) |
| operator++  operator--(parallelism TS v2) | element-wise increment and decrement   (public member function) |
| operator!  operator~  operator+  operator-(parallelism TS v2) | element-wise unary operators   (public member function) |
| size[static] (parallelism TS v2) | returns the width / number of elements   (public static member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator+  operator-  operator\*  operator/  operator%  operator&  operator|  operator^  operator<<  operator>>(parallelism TS v2) | element-wise binary operators   (function) |
| operator+=  operator-=  operator\*=  operator/=  operator%=  operator&=  operator|=  operator^=  operator<<=  operator>>=(parallelism TS v2) | element-wise compound binary operators   (function) |
| operator==  operator!=  operator>=  operator<=  operator>  operator<(parallelism TS v2) | element-wise relational operators   (function) |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| simd_mask(parallelism TS v2) | data-parallel type with the element type bool   (class template) |
| valarray | numeric arrays, array masks and array slices   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/simd/simd&oldid=161477>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 October 2023, at 15:06.