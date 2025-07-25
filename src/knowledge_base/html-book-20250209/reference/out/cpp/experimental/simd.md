# SIMD library

From cppreference.com
< cpp‎ | experimental
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
| ****Data-parallel vectors**** | | | | |

****SIMD library****

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

The SIMD library provides portable types for explicitly stating data-parallelism and structuring data for more efficient SIMD access.

An object of type simd<T> behaves analogue to objects of type `T`. But while `T` stores and manipulates one value, `simd<T>` stores and manipulates multiple values (called **width** but identified as size for consistency with the rest of the standard library; cf. simd_size).

Every operator and operation on `simd<T>` acts **element-wise** (except for **horizontal** operations, which are clearly marked as such). This simple rule expresses data-parallelism and will be used by the compiler to generate SIMD instructions and/or independent execution streams.

The width of the types `simd<T>` and native_simd<T> is determined by the implementation at compile-time. In contrast, the width of the type fixed_size_simd<T, N> is fixed by the developer to a certain size.

A recommended pattern for using a mix of different SIMD types with high efficiency uses native_simd and rebind_simd:

```
#include <experimental/simd>
namespace stdx = std::experimental;
 
using floatv  = stdx::native_simd<float>;
using doublev = stdx::rebind_simd_t<double, floatv>;
using intv    = stdx::rebind_simd_t<int, floatv>;

```

This ensures that the set of types all have the same width and thus can be interconverted. A conversion with mismatching width is not defined because it would either drop values or have to invent values. For resizing operations, the SIMD library provides the split and concat functions.

|  |  |
| --- | --- |
| Defined in header `<experimental/simd>` | |

### Main classes

|  |  |
| --- | --- |
| simd(parallelism TS v2) | data-parallel vector type   (class template) |
| simd_mask(parallelism TS v2) | data-parallel type with the element type bool   (class template) |

### ABI tags

|  |  |
| --- | --- |
| Defined in namespace `std::experimental::simd_abi` | |
| scalar(parallelism TS v2) | tag type for storing a single element   (typedef) |
| fixed_size(parallelism TS v2) | tag type for storing specified number of elements (alias template) |
| compatible(parallelism TS v2) | tag type that ensures ABI compatibility (alias template) |
| native(parallelism TS v2) | tag type that is most efficient (alias template) |
| max_fixed_size(parallelism TS v2) | the maximum number of elements guaranteed to be supported by fixed   (constant) |
| deducededuce_t(parallelism TS v2) | obtains an ABI type for given element type and number of elements   (class template) |

### Alignment tags

|  |  |
| --- | --- |
| element_aligned_tagelement_aligned(parallelism TS v2) | flag indicating alignment of the load/store address to element alignment   (class) |
| vector_aligned_tagvector_aligned(parallelism TS v2) | flag indicating alignment of the load/store address to vector alignment   (class) |
| overaligned_tagoveraligned(parallelism TS v2) | flag indicating alignment of the load/store address to the specified alignment   (class template) |

### Where expression

|  |  |
| --- | --- |
| const_where_expression(parallelism TS v2) | selected elements with non-mutating operations   (class template) |
| where_expression(parallelism TS v2) | selected elements with mutating operations   (class template) |
| where(parallelism TS v2) | produces const_where_expression and where_expression   (function template) |

### Casts

|  |  |
| --- | --- |
| simd_caststatic_simd_cast(parallelism TS v2) | element-wise static_cast   (function template) |
| to_fixed_sizeto_compatibleto_native(parallelism TS v2) | element-wise ABI cast   (function template) |
| splitsplit_by(parallelism TS v2) | splits single simd object to multiple ones   (function template) |
| concat(parallelism TS v2) | concatenates multiple simd objects to a single one   (function template) |

### Algorithms

|  |  |
| --- | --- |
| min(parallelism TS v2) | element-wise min operation   (function template) |
| max(parallelism TS v2) | element-wise max operation   (function template) |
| minmax(parallelism TS v2) | element-wise minmax operation   (function template) |
| clamp(parallelism TS v2) | element-wise clamp operation   (function template) |

### Reduction

|  |  |
| --- | --- |
| reducehminhmax(parallelism TS v2) | reduces the vector to a single element   (function template) |

### Mask reduction

|  |  |
| --- | --- |
| all_ofany_ofnone_ofsome_of(parallelism TS v2) | reductions of simd_mask to bool   (function template) |
| popcount(parallelism TS v2) | reduction of simd_mask to the number of true values   (function template) |
| find_first_setfind_last_set(parallelism TS v2) | reductions of simd_mask to the index of the first or last true value   (function template) |

### Traits

|  |  |
| --- | --- |
| is_simdis_simd_mask(parallelism TS v2) | checks if a type is a simd or simd_mask type   (class template) |
| is_abi_tag(parallelism TS v2) | checks if a type is an ABI tag type   (class template) |
| is_simd_flag_type(parallelism TS v2) | checks if a type is a simd flag type   (class template) |
| simd_size(parallelism TS v2) | obtains the number of elements of a given element type and ABI tag   (class template) |
| memory_alignment(parallelism TS v2) | obtains an appropriate alignment for vector_aligned   (class template) |
| rebind_simdresize_simd(parallelism TS v2) | change element type or the number of elements of simd or simd_mask   (class template) |

### Math functions

All functions in <cmath>, except for the special math functions, are overloaded for `simd`.

### Example

Run this code

```
#include <experimental/simd>
#include <iostream>
#include <string_view>
namespace stdx = std::experimental;
 
void println(std::string_view name, auto const& a)
{
    std::cout << name << ": ";
    for (std::size_t i{}; i != std::size(a); ++i)
        std::cout << a[i] << ' ';
    std::cout << '\n';
}
 
template<class A>
stdx::simd<int, A> my_abs(stdx::simd<int, A> x)
{
    where(x < 0, x) = -x;
    return x;
}
 
int main()
{
    const stdx::native_simd<int> a = 1;
    println("a", a);
 
    const stdx::native_simd<int> b([](int i) { return i - 2; });
    println("b", b);
 
    const auto c = a + b;
    println("c", c);
 
    const auto d = my_abs(c);
    println("d", d);
 
    const auto e = d * d;
    println("e", e);
 
    const auto inner_product = stdx::reduce(e);
    std::cout << "inner product: " << inner_product << '\n';
 
    const stdx::fixed_size_simd<long double, 16> x([](int i) { return i; });
    println("x", x);
    println("cos²(x) + sin²(x)", stdx::pow(stdx::cos(x), 2) + stdx::pow(stdx::sin(x), 2));
}

```

Output:

```
a: 1 1 1 1 
b: -2 -1 0 1 
c: -1 0 1 2 
d: 1 0 1 2 
e: 1 0 1 4 
inner product: 6
x: 0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 
cos²(x) + sin²(x): 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1

```

### See also

|  |  |
| --- | --- |
| valarray | numeric arrays, array masks and array slices   (class template) |

### External links

|  |  |
| --- | --- |
| 1. | The implementation of ISO/IEC TS 19570:2018 Section 9 "Data-Parallel Types" — github.com |
| 2. | TS implementation reach for GCC/libstdc++ (`std::experimental::simd` is shipping with GCC-11) — gcc.gnu.org |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/simd&oldid=178593>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 December 2024, at 14:04.