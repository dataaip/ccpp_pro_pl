# Standard library header <linalg> (C++26)

From cppreference.com
< cpp‎ | header
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

Standard library headers

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | ****<linalg>**** (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the numeric library.

|  |  |
| --- | --- |
| Classes | |
| Defined in namespace `std::linalg` | |
| layout_blas_packed")(C++26) | std::mdspan layout mapping policy that represents a square matrix that stores only the entries in one triangle, in a packed contiguous format   (class template) |
| scaled_accessor")(C++26) | std::mdspan accessor policy whose reference represents the product of a scaling factor that is fixed and its nested std::mdspan accessor's reference   (class template) |
| conjugated_accessor")(C++26) | std::mdspan accessor policy whose reference represents the complex conjugate of its nested std::mdspan accessor's reference   (class template) |
| layout_transpose")(C++26) | std::mdspan layout mapping policy that swaps the rightmost two indices, extents, and strides of any unique layout mapping policy   (class template) |
| Tags | |
| Defined in namespace `std::linalg` | |
| column_majorrow_majorcolumn_major_trow_major_t")(C++26) | describe the order of elements in an std::mdspan with linalg::layout_blas_packed layout (tag) |
| upper_trianglelower_triangleupper_triangle_tlower_triangle_t")(C++26) | specify whether algorithms and other users of a matrix should access the upper triangle or lower triangle of the matrix (tag) |
| implicit_unit_diagonalexplicit_diagonalimplicit_unit_diagonal_texplicit_diagonal_t")(C++26) | specify whether algorithms should access diagonal entries of the matrix (tag) |
| Functions | |
| Defined in namespace `std::linalg` | |
| In-place transformations | |
| scaled")(C++26) | returns a new read-only std::mdspan computed by the elementwise product of the scaling factor and the corresponding elements of the given std::mdspan   (function template) |
| conjugated")(C++26) | returns a new read-only std::mdspan whose elements are the complex conjugates of the corresponding elements of the given std::mdspan   (function template) |
| transposed")(C++26) | returns a new std::mdspan representing the transpose of the input matrix by the given std::mdspan   (function template) |
| conjugate_transposed")(C++26) | returns a conjugate transpose view of an object   (function template) |
| BLAS 1 functions | |
| setup_givens_rotation")(C++26) | generates plane rotation   (function template) |
| apply_givens_rotation")(C++26) | applies plane rotation to vectors   (function template) |
| swap_elements")(C++26) | swaps all corresponding elements of matrix or vector   (function template) |
| scale")(C++26) | overwrites matrix or vector with the result of computing the elementwise multiplication by a scalar   (function template) |
| copy")(C++26) | copies elements of one matrix or vector into another   (function template) |
| add")(C++26) | adds vectors or matrices elementwise   (function template) |
| dot")(C++26) | returns nonconjugated dot product of two vectors   (function template) |
| dotc")(C++26) | returns conjugated dot product of two vectors   (function template) |
| vector_sum_of_squares")(C++26) | returns scaled sum of squares of the vector elements   (function template) |
| vector_two_norm")(C++26) | returns Euclidean norm of a vector   (function template) |
| vector_abs_sum")(C++26) | returns sum of absolute values of the vector elements   (function template) |
| vector_idx_abs_max")(C++26) | returns index of maximum absolute value of vector elements   (function template) |
| matrix_frob_norm")(C++26) | returns Frobenius norm of a matrix   (function template) |
| matrix_one_norm")(C++26) | returns one norm of a matrix   (function template) |
| matrix_inf_norm")(C++26) | returns infinity norm of a matrix   (function template) |
| BLAS 2 functions | |
| matrix_vector_product")(C++26) | computes matrix-vector product   (function template) |
| symmetric_matrix_vector_product")(C++26) | computes symmetric matrix-vector product   (function template) |
| hermitian_matrix_vector_product")(C++26) | computes Hermitian matrix-vector product   (function template) |
| triangular_matrix_vector_product")(C++26) | computes triangular matrix-vector product   (function template) |
| triangular_matrix_vector_solve")(C++26) | solves a triangular linear system   (function template) |
| matrix_rank_1_update")(C++26) | performs nonsymmetric nonconjugated rank-1 update of a matrix   (function template) |
| matrix_rank_1_update_c")(C++26) | performs nonsymmetric conjugated rank-1 update of a matrix   (function template) |
| symmetric_matrix_rank_1_update")(C++26) | performs rank-1 update of a symmetric matrix   (function template) |
| hermitian_matrix_rank_1_update")(C++26) | performs rank-1 update of a Hermitian matrix   (function template) |
| hermitian_matrix_rank_2_update")(C++26) | performs rank-2 update of a symmetric matrix   (function template) |
| hermitian_matrix_rank_2_update")(C++26) | performs rank-2 update of a Hermitian matrix   (function template) |
| BLAS 3 functions | |
| matrix_product")(C++26) | computes matrix-matrix product   (function template) |
| symmetric_matrix_product")(C++26) | computes symmetric matrix-matrix product   (function template) |
| hermitian_matrix_product")(C++26) | computes Hermitian matrix-matrix product   (function template) |
| triangular_matrix_producttriangular_matrix_left_producttriangular_matrix_right_product")(C++26) | computes triangular matrix-matrix product   (function template) |
| symmetric_matrix_rank_k_update")(C++26) | performs rank-k update of a symmetric matrix   (function template) |
| hermitian_matrix_rank_k_update")(C++26) | performs rank-k update of a Hermitian matrix   (function template) |
| symmetric_matrix_rank_2k_update")(C++26) | performs rank-2k update of a symmetric matrix   (function template) |
| hermitian_matrix_rank_2k_update")(C++26) | performs rank-2k update of a Hermitian matrix   (function template) |
| triangular_matrix_matrix_left_solvetriangular_matrix_matrix_right_solve")(C++26) | solves multiple triangular linear systems   (function template) |

### Synopsis

```
namespace std::linalg {
 
// storage order tags
struct column_major_t;
inline constexpr column_major_t column_major;
struct row_major_t;
inline constexpr row_major_t row_major;
 
// triangle tags
struct upper_triangle_t;
inline constexpr upper_triangle_t upper_triangle;
struct lower_triangle_t;
inline constexpr lower_triangle_t lower_triangle;
 
// diagonal tags
struct implicit_unit_diagonal_t;
inline constexpr implicit_unit_diagonal_t implicit_unit_diagonal;
struct explicit_diagonal_t;
inline constexpr explicit_diagonal_t explicit_diagonal;
 
// class template layout_blas_packed
template<class Triangle, class StorageOrder>
class layout_blas_packed;
 
// exposition-only concepts and traits
template<class T>
struct __is_mdspan; // exposition only
 
template<class T>
concept __in_vector = /* see description */; // exposition only
 
template<class T>
concept __out_vector = /* see description */; // exposition only
 
template<class T>
concept __inout_vector = /* see description */; // exposition only
 
template<class T>
concept __in_matrix = /* see description */; // exposition only
 
template<class T>
concept __out_matrix = /* see description */; // exposition only
 
template<class T>
concept __inout_matrix = /* see description */; // exposition only
 
template<class T>
concept __possibly_packed_inout_matrix = /* see description */; // exposition only
 
template<class T>
concept __in_object = /* see description */; // exposition only
 
template<class T>
concept __out_object = /* see description */; // exposition only
 
template<class T>
concept __inout_object = /* see description */; // exposition only
 
// scaled in-place transformation
template<class ScalingFactor, class Accessor>
class scaled_accessor;
 
template<class ScalingFactor,
         class ElementType, class Extents, class Layout, class Accessor>
constexpr auto scaled(ScalingFactor scaling_factor,
                      mdspan<ElementType, Extents, Layout, Accessor> x);
 
// conjugated in-place transformation
template<class Accessor>
class conjugated_accessor;
 
template<class ElementType, class Extents, class Layout, class Accessor>
constexpr auto conjugated(mdspan<ElementType, Extents, Layout, Accessor> a);
 
// transposed in-place transformation
template<class Layout>
class layout_transpose;
 
template<class ElementType, class Extents, class Layout, class Accessor>
constexpr auto transposed(mdspan<ElementType, Extents, Layout, Accessor> a);
 
// conjugated transposed in-place transformation
template<class ElementType, class Extents, class Layout, class Accessor>
constexpr auto conjugate_transposed(mdspan<ElementType, Extents, Layout, Accessor> a);
 
// algorithms
// compute Givens rotation
 
template<class Real>
struct setup_givens_rotation_result {
  Real c;
  Real s;
  Real r;
};
 
template<class Real>
struct setup_givens_rotation_result<complex<Real>> {
  Real c;
  complex<Real> s;
  complex<Real> r;
};
 
template<class Real>
setup_givens_rotation_result<Real> setup_givens_rotation(Real a, Real b) noexcept;
 
template<class Real>
setup_givens_rotation_result<complex<Real>>
setup_givens_rotation(complex<Real> a, complex<Real> b) noexcept;
 
// apply computed Givens rotation
template<__inout_vector InOutVec1, __inout_vector InOutVec2, class Real>
void apply_givens_rotation(InOutVec1 x, InOutVec2 y, Real c, Real s);
 
template<class ExecutionPolicy,
         __inout_vector InOutVec1, __inout_vector InOutVec2, class Real>
void apply_givens_rotation(ExecutionPolicy&& exec,
                           InOutVec1 x, InOutVec2 y, Real c, Real s);
 
template<__inout_vector InOutVec1, __inout_vector InOutVec2, class Real>
void apply_givens_rotation(InOutVec1 x, InOutVec2 y, Real c, complex<Real> s);
 
template<class ExecutionPolicy,
         __inout_vector InOutVec1, __inout_vector InOutVec2, class Real>
void apply_givens_rotation(ExecutionPolicy&& exec,
                           InOutVec1 x, InOutVec2 y, Real c, complex<Real> s);
 
// swap elements
template<__inout_object InOutObj1, __inout_object InOutObj2>
void swap_elements(InOutObj1 x, InOutObj2 y);
 
template<class ExecutionPolicy, __inout_object InOutObj1, __inout_object InOutObj2>
void swap_elements(ExecutionPolicy&& exec, InOutObj1 x, InOutObj2 y);
 
// multiply elements by scalar
template<class Scalar, __inout_object InOutObj>
void scale(Scalar alpha, InOutObj x);
 
template<class ExecutionPolicy, class Scalar, __inout_object InOutObj>
void scale(ExecutionPolicy&& exec, Scalar alpha, InOutObj x);
 
// copy elements
template<__in_object InObj, __out_object OutObj>
void copy(InObj x, OutObj y);
 
template<class ExecutionPolicy, __in_object InObj, __out_object OutObj>
void copy(ExecutionPolicy&& exec, InObj x, OutObj y);
 
// add elementwise
template<__in_object InObj1, __in_object InObj2, __out_object OutObj>
void add(InObj1 x, InObj2 y, OutObj z);
 
template<class ExecutionPolicy,
         __in_object InObj1, __in_object InObj2, __out_object OutObj>
void add(ExecutionPolicy&& exec, InObj1 x, InObj2 y, OutObj z);
 
// nonconjugated dot product of two vectors
template<__in_vector InVec1, __in_vector InVec2, class Scalar>
Scalar dot(InVec1 v1, InVec2 v2, Scalar init);
 
template<class ExecutionPolicy,
         __in_vector InVec1, __in_vector InVec2, class Scalar>
Scalar dot(ExecutionPolicy&& exec, InVec1 v1, InVec2 v2, Scalar init);
 
template<__in_vector InVec1, __in_vector InVec2>
auto dot(InVec1 v1, InVec2 v2) -> /* see description */;
 
template<class ExecutionPolicy, __in_vector InVec1, __in_vector InVec2>
auto dot(ExecutionPolicy&& exec, InVec1 v1, InVec2 v2) -> /* see description */;
 
// conjugated dot product of two vectors
template<__in_vector InVec1, __in_vector InVec2, class Scalar>
Scalar dotc(InVec1 v1, InVec2 v2, Scalar init);
 
template<class ExecutionPolicy,
         __in_vector InVec1, __in_vector InVec2, class Scalar>
Scalar dotc(ExecutionPolicy&& exec, InVec1 v1, InVec2 v2, Scalar init);
 
template<__in_vector InVec1, __in_vector InVec2>
auto dotc(InVec1 v1, InVec2 v2) -> /* see description */;
 
template<class ExecutionPolicy, __in_vector InVec1, __in_vector InVec2>
auto dotc(ExecutionPolicy&& exec, InVec1 v1, InVec2 v2) -> /* see description */;
 
// Scaled sum of squares of a vector's elements
template<class Scalar>
struct sum_of_squares_result {
  Scalar scaling_factor;
  Scalar scaled_sum_of_squares;
};
 
template<__in_vector InVec, class Scalar>
sum_of_squares_result<Scalar>
vector_sum_of_squares(InVec v, sum_of_squares_result<Scalar> init);
 
template<class ExecutionPolicy, __in_vector InVec, class Scalar>
sum_of_squares_result<Scalar>
vector_sum_of_squares(ExecutionPolicy&& exec, InVec v,
                      sum_of_squares_result<Scalar> init);
 
// Euclidean norm of a vector
template<__in_vector InVec, class Scalar>
Scalar vector_two_norm(InVec v, Scalar init);
 
template<class ExecutionPolicy, __in_vector InVec, class Scalar>
Scalar vector_two_norm(ExecutionPolicy&& exec, InVec v, Scalar init);
 
template<__in_vector InVec>
auto vector_two_norm(InVec v) -> /* see description */;
 
template<class ExecutionPolicy, __in_vector InVec>
auto vector_two_norm(ExecutionPolicy&& exec, InVec v) -> /* see description */;
 
// sum of absolute values of vector elements
template<__in_vector InVec, class Scalar>
Scalar vector_abs_sum(InVec v, Scalar init);
template<class ExecutionPolicy, __in_vector InVec, class Scalar>
Scalar vector_abs_sum(ExecutionPolicy&& exec, InVec v, Scalar init);
 
template<__in_vector InVec>
auto vector_abs_sum(InVec v) -> /* see description */;
 
template<class ExecutionPolicy, __in_vector InVec>
auto vector_abs_sum(ExecutionPolicy&& exec, InVec v) -> /* see description */;
 
// index of maximum absolute value of vector elements
template<__in_vector InVec>
typename InVec::extents_type vector_idx_abs_max(InVec v);
 
template<class ExecutionPolicy, __in_vector InVec>
typename InVec::extents_type vector_idx_abs_max(ExecutionPolicy&& exec, InVec v);
 
// Frobenius norm of a matrix
template<__in_matrix InMat, class Scalar>
Scalar matrix_frob_norm(InMat A, Scalar init);
 
template<class ExecutionPolicy, __in_matrix InMat, class Scalar>
Scalar matrix_frob_norm(ExecutionPolicy&& exec,
                        InMat A, Scalar init);
 
template<__in_matrix InMat>
auto matrix_frob_norm(InMat A) -> /* see description */;
 
template<class ExecutionPolicy, __in_matrix InMat>
auto matrix_frob_norm(ExecutionPolicy&& exec, InMat A) -> /* see description */;
 
// One norm of a matrix
template<__in_matrix InMat, class Scalar>
Scalar matrix_one_norm(InMat A, Scalar init);
 
template<class ExecutionPolicy, __in_matrix InMat, class Scalar>
Scalar matrix_one_norm(ExecutionPolicy&& exec,
                       InMat A, Scalar init);
 
template<__in_matrix InMat>
auto matrix_one_norm(InMat A) -> /* see description */;
 
template<class ExecutionPolicy, __in_matrix InMat>
auto matrix_one_norm(ExecutionPolicy&& exec, InMat A) -> /* see description */;
 
// Infinity norm of a matrix
template<__in_matrix InMat, class Scalar>
Scalar matrix_inf_norm(InMat A, Scalar init);
 
template<class ExecutionPolicy, __in_matrix InMat, class Scalar>
Scalar matrix_inf_norm(ExecutionPolicy&& exec,
                       InMat A, Scalar init);
 
template<__in_matrix InMat>
auto matrix_inf_norm(InMat A) -> /* see description */;
 
template<class ExecutionPolicy, __in_matrix InMat>
auto matrix_inf_norm(ExecutionPolicy&& exec, InMat A) -> /* see description */;
 
// general matrix-vector product
template<__in_matrix InMat, __in_vector InVec, __out_vector OutVec>
void matrix_vector_product(InMat A, InVec x, OutVec y);
 
template<class ExecutionPolicy,
         __in_matrix InMat, __in_vector InVec, __out_vector OutVec>
void matrix_vector_product(ExecutionPolicy&& exec,
                           InMat A, InVec x, OutVec y);
 
template<__in_matrix InMat, __in_vector InVec1,
         __in_vector InVec2, __out_vector OutVec>
void matrix_vector_product(InMat A, InVec1 x, InVec2 y, OutVec z);
 
template<class ExecutionPolicy,
         __in_matrix InMat, __in_vector InVec1,
         __in_vector InVec2, __out_vector OutVec>
void matrix_vector_product(ExecutionPolicy&& exec,
                           InMat A, InVec1 x, InVec2 y, OutVec z);
 
// symmetric matrix-vector product
template<__in_matrix InMat, class Triangle,
         __in_vector InVec, __out_vector OutVec>
void symmetric_matrix_vector_product(InMat A, Triangle t,
                                     InVec x, OutVec y);
 
template<class ExecutionPolicy,
         __in_matrix InMat, class Triangle,
         __in_vector InVec, __out_vector OutVec>
void symmetric_matrix_vector_product(ExecutionPolicy&& exec,
                                     InMat A, Triangle t,
                                     InVec x, OutVec y);
 
template<__in_matrix InMat, class Triangle,
         __in_vector InVec1, __in_vector InVec2,
         __out_vector OutVec>
void symmetric_matrix_vector_product(InMat A, Triangle t,
                                     InVec1 x, InVec2 y, OutVec z);
 
template<class ExecutionPolicy,
         __in_matrix InMat, class Triangle,
         __in_vector InVec1, __in_vector InVec2,
         __out_vector OutVec>
void symmetric_matrix_vector_product(ExecutionPolicy&& exec,
                                     InMat A, Triangle t,
                                     InVec1 x, InVec2 y, OutVec z);
 
// Hermitian matrix-vector product
template<__in_matrix InMat, class Triangle,
         __in_vector InVec, __out_vector OutVec>
void hermitian_matrix_vector_product(InMat A, Triangle t,
                                     InVec x, OutVec y);
 
template<class ExecutionPolicy,
         __in_matrix InMat, class Triangle,
         __in_vector InVec, __out_vector OutVec>
void hermitian_matrix_vector_product(ExecutionPolicy&& exec,
                                     InMat A, Triangle t,
                                     InVec x, OutVec y);
 
template<__in_matrix InMat, class Triangle,
         __in_vector InVec1, __in_vector InVec2,
         __out_vector OutVec>
void hermitian_matrix_vector_product(InMat A, Triangle t,
                                     InVec1 x, InVec2 y, OutVec z);
 
template<class ExecutionPolicy,
         __in_matrix InMat, class Triangle,
         __in_vector InVec1, __in_vector InVec2,
         __out_vector OutVec>
void hermitian_matrix_vector_product(ExecutionPolicy&& exec,
                                     InMat A, Triangle t,
                                     InVec1 x, InVec2 y, OutVec z);
 
// Triangular matrix-vector product
// Overwriting triangular matrix-vector product
template<__in_matrix InMat, class Triangle, class DiagonalStorage,
         __in_vector InVec, __out_vector OutVec>
void triangular_matrix_vector_product(InMat A, Triangle t, DiagonalStorage d,
                                      InVec x, OutVec y);
 
template<class ExecutionPolicy,
         __in_matrix InMat, class Triangle, class DiagonalStorage,
         __in_vector InVec, __out_vector OutVec>
void triangular_matrix_vector_product(ExecutionPolicy&& exec,
                                      InMat A, Triangle t, DiagonalStorage d,
                                      InVec x, OutVec y);
 
// In-place triangular matrix-vector product
template<__in_matrix InMat, class Triangle, class DiagonalStorage,
         __inout_vector InOutVec>
void triangular_matrix_vector_product(InMat A, Triangle t, DiagonalStorage d,
                                      InOutVec y);
 
template<class ExecutionPolicy,
         __in_matrix InMat, class Triangle, class DiagonalStorage,
         __inout_vector InOutVec>
void triangular_matrix_vector_product(ExecutionPolicy&& exec,
                                      InMat A, Triangle t, DiagonalStorage d,
                                      InOutVec y);
 
// Updating triangular matrix-vector product
template<__in_matrix InMat, class Triangle, class DiagonalStorage,
         __in_vector InVec1, __in_vector InVec2,
         __out_vector OutVec>
void triangular_matrix_vector_product(InMat A, Triangle t, DiagonalStorage d,
                                      InVec1 x, InVec2 y, OutVec z);
 
template<class ExecutionPolicy,
         __in_matrix InMat, class Triangle, class DiagonalStorage,
         __in_vector InVec1, __in_vector InVec2,
         __out_vector OutVec>
void triangular_matrix_vector_product(ExecutionPolicy&& exec,
                                      InMat A, Triangle t, DiagonalStorage d,
                                      InVec1 x, InVec2 y, OutVec z);
 
// Solve a triangular linear system, not in place
template<__in_matrix InMat, class Triangle, class DiagonalStorage,
         __in_vector InVec, __out_vector OutVec, class BinaryDivideOp>
void triangular_matrix_vector_solve(InMat A, Triangle t, DiagonalStorage d,
                                    InVec b, OutVec x, BinaryDivideOp divide);
 
template<class ExecutionPolicy,
         __in_matrix InMat, class Triangle, class DiagonalStorage,
         __in_vector InVec, __out_vector OutVec, class BinaryDivideOp>
void triangular_matrix_vector_solve(ExecutionPolicy&& exec,
                                    InMat A, Triangle t, DiagonalStorage d,
                                    InVec b, OutVec x, BinaryDivideOp divide);
 
template<__in_matrix InMat, class Triangle, class DiagonalStorage,
         __in_vector InVec, __out_vector OutVec>
void triangular_matrix_vector_solve(InMat A, Triangle t, DiagonalStorage d,
                                    InVec b, OutVec x);
 
template<class ExecutionPolicy,
         __in_matrix InMat, class Triangle, class DiagonalStorage,
         __in_vector InVec, __out_vector OutVec>
void triangular_matrix_vector_solve(ExecutionPolicy&& exec,
                                    InMat A, Triangle t, DiagonalStorage d,
                                    InVec b, OutVec x);
 
// Solve a triangular linear system, in place
template<__in_matrix InMat, class Triangle, class DiagonalStorage,
         __inout_vector InOutVec, class BinaryDivideOp>
void triangular_matrix_vector_solve(InMat A, Triangle t, DiagonalStorage d,
                                    InOutVec b, BinaryDivideOp divide);
 
template<class ExecutionPolicy,
         __in_matrix InMat, class Triangle, class DiagonalStorage,
         __inout_vector InOutVec, class BinaryDivideOp>
void triangular_matrix_vector_solve(ExecutionPolicy&& exec,
                                    InMat A, Triangle t, DiagonalStorage d,
                                    InOutVec b, BinaryDivideOp divide);
 
template<__in_matrix InMat, class Triangle, class DiagonalStorage,
         __inout_vector InOutVec>
void triangular_matrix_vector_solve(InMat A, Triangle t, DiagonalStorage d,
                                    InOutVec b);
 
template<class ExecutionPolicy,
         __in_matrix InMat, class Triangle, class DiagonalStorage,
         __inout_vector InOutVec>
void triangular_matrix_vector_solve(ExecutionPolicy&& exec,
                                    InMat A, Triangle t, DiagonalStorage d,
                                    InOutVec b);
 
// nonconjugated rank-1 matrix update
template<__in_vector InVec1, __in_vector InVec2, __inout_matrix InOutMat>
void matrix_rank_1_update(InVec1 x, InVec2 y, InOutMat A);
 
template<class ExecutionPolicy,
         __in_vector InVec1, __in_vector InVec2, __inout_matrix InOutMat>
void matrix_rank_1_update(ExecutionPolicy&& exec,
                          InVec1 x, InVec2 y, InOutMat A);
 
// conjugated rank-1 matrix update
template<__in_vector InVec1, __in_vector InVec2, __inout_matrix InOutMat>
void matrix_rank_1_update_c(InVec1 x, InVec2 y, InOutMat A);
 
template<class ExecutionPolicy, 
         __in_vector InVec1, __in_vector InVec2, __inout_matrix InOutMat>
void matrix_rank_1_update_c(ExecutionPolicy&& exec,
                            InVec1 x, InVec2 y, InOutMat A);
 
// symmetric rank-1 matrix update
template<__in_vector InVec, __possibly_packed_inout_matrix InOutMat,
         class Triangle>
void symmetric_matrix_rank_1_update(InVec x, InOutMat A, Triangle t);
 
template<class ExecutionPolicy,
         __in_vector InVec, __possibly_packed_inout_matrix InOutMat,
         class Triangle>
void symmetric_matrix_rank_1_update(ExecutionPolicy&& exec,
                                    InVec x, InOutMat A, Triangle t);
 
template<class Scalar, __in_vector InVec,
         __possibly_packed_inout_matrix InOutMat, class Triangle>
void symmetric_matrix_rank_1_update(Scalar alpha, InVec x, InOutMat A,
                                    Triangle t);
 
template<class ExecutionPolicy,
         class Scalar, __in_vector InVec,
         __possibly_packed_inout_matrix InOutMat, class Triangle>
void symmetric_matrix_rank_1_update(ExecutionPolicy&& exec,
                                    Scalar alpha, InVec x, InOutMat A,
                                    Triangle t);
 
// Hermitian rank-1 matrix update
template<__in_vector InVec, __possibly_packed_inout_matrix InOutMat,
         class Triangle>
void hermitian_matrix_rank_1_update(InVec x, InOutMat A, Triangle t);
 
template<class ExecutionPolicy,
         __in_vector InVec, __possibly_packed_inout_matrix InOutMat,
         class Triangle>
void hermitian_matrix_rank_1_update(ExecutionPolicy&& exec,
                                    InVec x, InOutMat A, Triangle t);
 
template<class Scalar, __in_vector InVec,
         __possibly_packed_inout_matrix InOutMat,
         class Triangle>
void hermitian_matrix_rank_1_update(Scalar alpha, InVec x, InOutMat A,
                                    Triangle t);
 
template<class ExecutionPolicy,
         class Scalar, __in_vector InVec,
         __possibly_packed_inout_matrix InOutMat,
         class Triangle>
void hermitian_matrix_rank_1_update(ExecutionPolicy&& exec,
                                    Scalar alpha, InVec x, InOutMat A,
                                    Triangle t);
 
// symmetric rank-2 matrix update
template<__in_vector InVec1, __in_vector InVec2,
         __possibly_packed_inout_matrix InOutMat,
         class Triangle>
void symmetric_matrix_rank_2_update(InVec1 x, InVec2 y, InOutMat A,
                                    Triangle t);
 
template<class ExecutionPolicy,
         __in_vector InVec1, __in_vector InVec2,
         __possibly_packed_inout_matrix InOutMat,
         class Triangle>
void symmetric_matrix_rank_2_update(ExecutionPolicy&& exec,
                                    InVec1 x, InVec2 y, InOutMat A,
                                    Triangle t);
 
// Hermitian rank-2 matrix update
template<__in_vector InVec1, __in_vector InVec2,
         __possibly_packed_inout_matrix InOutMat,
         class Triangle>
void hermitian_matrix_rank_2_update(InVec1 x, InVec2 y, InOutMat A,
                                    Triangle t);
 
template<class ExecutionPolicy,
         __in_vector InVec1, __in_vector InVec2,
         __possibly_packed_inout_matrix InOutMat,
         class Triangle>
void hermitian_matrix_rank_2_update(ExecutionPolicy&& exec,
                                    InVec1 x, InVec2 y, InOutMat A,
                                    Triangle t);
 
// general matrix-matrix product
template<__in_matrix InMat1, __in_matrix InMat2, __out_matrix OutMat>
void matrix_product(InMat1 A, InMat2 B, OutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, __in_matrix InMat2, __out_matrix OutMat>
void matrix_product(ExecutionPolicy&& exec, InMat1 A, InMat2 B, OutMat C);
 
template<__in_matrix InMat1, __in_matrix InMat2, __in_matrix InMat3,
         __out_matrix OutMat>
void matrix_product(InMat1 A, InMat2 B, InMat3 E, OutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, __in_matrix InMat2, __in_matrix InMat3,
         __out_matrix OutMat>
void matrix_product(ExecutionPolicy&& exec,
                    InMat1 A, InMat2 B, InMat3 E, OutMat C);
 
 
// symmetric matrix-matrix product
// overwriting symmetric matrix-matrix left product
template<__in_matrix InMat1, class Triangle,
         __in_matrix InMat2, __out_matrix OutMat>
void symmetric_matrix_product(InMat1 A, Triangle t,
                              InMat2 B, OutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle,
         __in_matrix InMat2, __out_matrix OutMat>
void symmetric_matrix_product(ExecutionPolicy&& exec,
                              InMat1 A, Triangle t,
                              InMat2 B, OutMat C);
 
// overwriting symmetric matrix-matrix right product
template<__in_matrix InMat1, __in_matrix InMat2,
         class Triangle, __out_matrix OutMat>
void symmetric_matrix_product(InMat1 B, InMat2 A, Triangle t,
                              OutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, __in_matrix InMat2,
         class Triangle, __out_matrix OutMat>
void symmetric_matrix_product(ExecutionPolicy&& exec,
                              InMat1 B, InMat2 A, Triangle t,
                              OutMat C);
 
// updating symmetric matrix-matrix left product
template<__in_matrix InMat1, class Triangle,
         __in_matrix InMat2, __in_matrix InMat3,
         __out_matrix OutMat>
void symmetric_matrix_product(InMat1 A, Triangle t,
                              InMat2 B, InMat3 E,
                              OutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle,
         __in_matrix InMat2, __in_matrix InMat3,
         __out_matrix OutMat>
void symmetric_matrix_product(ExecutionPolicy&& exec,
                              InMat1 A, Triangle t,
                              InMat2 B, InMat3 E,
                              OutMat C);
 
// updating symmetric matrix-matrix right product
template<__in_matrix InMat1, __in_matrix InMat2, class Triangle,
         __in_matrix InMat3, __out_matrix OutMat>
void symmetric_matrix_product(InMat1 B, InMat2 A, Triangle t,
                              InMat3 E, OutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, __in_matrix InMat2, class Triangle,
         __in_matrix InMat3, __out_matrix OutMat>
void symmetric_matrix_product(ExecutionPolicy&& exec,
                              InMat1 B, InMat2 A, Triangle t,
                              InMat3 E, OutMat C);
 
// Hermitian matrix-matrix product
// overwriting Hermitian matrix-matrix left product
template<__in_matrix InMat1, class Triangle,
         __in_matrix InMat2, __out_matrix OutMat>
void hermitian_matrix_product(InMat1 A, Triangle t,
                              InMat2 B, OutMat C);
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle,
         __in_matrix InMat2, __out_matrix OutMat>
void hermitian_matrix_product(ExecutionPolicy&& exec,
                              InMat1 A, Triangle t,
                              InMat2 B, OutMat C);
 
// overwriting Hermitian matrix-matrix right product
template<__in_matrix InMat1, __in_matrix InMat2,
         class Triangle, __out_matrix OutMat>
void hermitian_matrix_product(InMat1 B, InMat2 A, Triangle t,
                              OutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, __in_matrix InMat2,
         class Triangle, __out_matrix OutMat>
void hermitian_matrix_product(ExecutionPolicy&& exec,
                              InMat1 B, InMat2 A, Triangle t,
                              OutMat C);
 
// updating Hermitian matrix-matrix left product
template<__in_matrix InMat1, class Triangle,
         __in_matrix InMat2, __in_matrix InMat3, __out_matrix OutMat>
void hermitian_matrix_product(InMat1 A, Triangle t,
                              InMat2 B, InMat3 E, OutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle,
         __in_matrix InMat2, __in_matrix InMat3, __out_matrix OutMat>
void hermitian_matrix_product(ExecutionPolicy&& exec,
                              InMat1 A, Triangle t,
                              InMat2 B, InMat3 E, OutMat C);
 
// updating Hermitian matrix-matrix right product
template<__in_matrix InMat1, __in_matrix InMat2, class Triangle,
         __in_matrix InMat3, __out_matrix OutMat>
void hermitian_matrix_product(InMat1 B, InMat2 A, Triangle t,
                              InMat3 E, OutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, __in_matrix InMat2, class Triangle,
         __in_matrix InMat3, __out_matrix OutMat>
void hermitian_matrix_product(ExecutionPolicy&& exec,
                              InMat1 B, InMat2 A, Triangle t,
                              InMat3 E, OutMat C);
 
// triangular matrix-matrix product
// overwriting triangular matrix-matrix left product
template<__in_matrix InMat1, class Triangle, class DiagonalStorage,
         __in_matrix InMat2, __out_matrix OutMat>
void triangular_matrix_product(InMat1 A, Triangle t, DiagonalStorage d,
                               InMat2 B, OutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle, class DiagonalStorage,
         __in_matrix InMat2, __out_matrix OutMat>
void triangular_matrix_product(ExecutionPolicy&& exec,
                               InMat1 A, Triangle t, DiagonalStorage d,
                               InMat2 B, OutMat C);
 
template<__in_matrix InMat1, class Triangle, class DiagonalStorage,
         __inout_matrix InOutMat>
void triangular_matrix_left_product(InMat1 A, Triangle t, DiagonalStorage d,
                                    InOutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle, class DiagonalStorage,
         __inout_matrix InOutMat>
void triangular_matrix_left_product(ExecutionPolicy&& exec,
                                    InMat1 A, Triangle t, DiagonalStorage d,
                                    InOutMat C);
 
// overwriting triangular matrix-matrix right product
template<__in_matrix InMat1, __in_matrix InMat2,
         class Triangle, class DiagonalStorage,
         __out_matrix OutMat>
void triangular_matrix_product(InMat1 B, InMat2 A,
                               Triangle t, DiagonalStorage d,
                               OutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, __in_matrix InMat2,
         class Triangle, class DiagonalStorage,
         __out_matrix OutMat>
void triangular_matrix_product(ExecutionPolicy&& exec,
                               InMat1 B, InMat2 A,
                               Triangle t, DiagonalStorage d,
                               OutMat C);
 
template<__in_matrix InMat1, class Triangle, class DiagonalStorage,
         __inout_matrix InOutMat>
void triangular_matrix_right_product(InMat1 A, Triangle t, DiagonalStorage d,
                                     InOutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle, class DiagonalStorage,
         __inout_matrix InOutMat>
void triangular_matrix_right_product(ExecutionPolicy&& exec,
                                     InMat1 A, Triangle t, DiagonalStorage d,
                                     InOutMat C);
 
// updating triangular matrix-matrix left product
template<__in_matrix InMat1, class Triangle, class DiagonalStorage,
         __in_matrix InMat2, __in_matrix InMat3,
         __out_matrix OutMat>
void triangular_matrix_product(InMat1 A, Triangle t, DiagonalStorage d,
                               InMat2 B, InMat3 E, OutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle, class DiagonalStorage,
         __in_matrix InMat2, __in_matrix InMat3,
         __out_matrix OutMat>
void triangular_matrix_product(ExecutionPolicy&& exec,
                               InMat1 A, Triangle t, DiagonalStorage d,
                               InMat2 B, InMat3 E, OutMat C);
 
// updating triangular matrix-matrix right product
template<__in_matrix InMat1, __in_matrix InMat2,
         class Triangle, class DiagonalStorage,
         __in_matrix InMat3, __out_matrix OutMat>
void triangular_matrix_product(InMat1 B, InMat2 A,
                               Triangle t, DiagonalStorage d,
                               InMat3 E, OutMat C);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, __in_matrix InMat2,
         class Triangle, class DiagonalStorage,
         __in_matrix InMat3, __out_matrix OutMat>
void triangular_matrix_product(ExecutionPolicy&& exec,
                               InMat1 B, InMat2 A,
                               Triangle t, DiagonalStorage d,
                               InMat3 E, OutMat C);
 
// rank-k symmetric matrix update
template<class Scalar, __in_matrix InMat1,
         __possibly_packed_inout_matrix InOutMat, class Triangle>
void symmetric_matrix_rank_k_update(Scalar alpha, InMat1 A, InOutMat C,
                                    Triangle t);
 
template<class Scalar,
         class ExecutionPolicy,
         ___in_matrix InMat1,
         __possibly_packed_inout_matrix InOutMat, class Triangle>
void symmetric_matrix_rank_k_update(ExecutionPolicy&& exec,
                                    Scalar alpha, InMat1 A, InOutMat C,
                                    Triangle t);
 
template<__in_matrix InMat1,
         __possibly_packed_inout_matrix InOutMat, class Triangle>
void symmetric_matrix_rank_k_update(InMat1 A, InOutMat C, Triangle t);
 
template<class ExecutionPolicy,
         __in_matrix InMat1,
         __possibly_packed_inout_matrix InOutMat, class Triangle>
void symmetric_matrix_rank_k_update(ExecutionPolicy&& exec,
                                    InMat1 A, InOutMat C, Triangle t);
 
// rank-k Hermitian matrix update
template<class Scalar, __in_matrix InMat1,
         __possibly_packed_inout_matrix InOutMat, class Triangle>
void hermitian_matrix_rank_k_update(Scalar alpha, InMat1 A, InOutMat C,
                                    Triangle t);
 
template<class ExecutionPolicy,
         class Scalar, __in_matrix InMat1,
         __possibly_packed_inout_matrix InOutMat, class Triangle
void hermitian_matrix_rank_k_update(ExecutionPolicy&& exec,
                                    Scalar alpha, InMat1 A, InOutMat C,
                                    Triangle t);
 
template<__in_matrix InMat1,
         __possibly_packed_inout_matrix InOutMat, class Triangle>
void hermitian_matrix_rank_k_update(InMat1 A, InOutMat C, Triangle t);
 
template<class ExecutionPolicy,
         __in_matrix InMat1,
         __possibly_packed_inout_matrix InOutMat, class Triangle>
void hermitian_matrix_rank_k_update(ExecutionPolicy&& exec,
                                    InMat1 A, InOutMat C, Triangle t);
 
// rank-2k symmetric matrix update
template<__in_matrix InMat1, __in_matrix InMat2,
         __possibly_packed_inout_matrix InOutMat, class Triangle>
void symmetric_matrix_rank_2k_update(InMat1 A, InMat2 B, InOutMat C,
                                     Triangle t);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, __in_matrix InMat2,
         __possibly_packed_inout_matrix InOutMat, class Triangle>
void symmetric_matrix_rank_2k_update(ExecutionPolicy&& exec,
                                     InMat1 A, InMat2 B, InOutMat C,
                                     Triangle t);
 
// rank-2k Hermitian matrix update
template<__in_matrix InMat1, __in_matrix InMat2,
         __possibly_packed_inout_matrix InOutMat, class Triangle>
void hermitian_matrix_rank_2k_update(InMat1 A, InMat2 B, InOutMat C,
                                     Triangle t);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, __in_matrix InMat2,
         __possibly_packed_inout_matrix InOutMat, class Triangle>
void hermitian_matrix_rank_2k_update(ExecutionPolicy&& exec,
                                     InMat1 A, InMat2 B, InOutMat C,
                                     Triangle t);
 
// solve multiple triangular linear systems
// with triangular matrix on the left
template<__in_matrix InMat1, class Triangle, class DiagonalStorage,
         __in_matrix InMat2, __out_matrix OutMat, class BinaryDivideOp>
void triangular_matrix_matrix_left_solve(InMat1 A,
                                         Triangle t, DiagonalStorage d,
                                         InMat2 B, OutMat X,
                                         BinaryDivideOp divide);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle, class DiagonalStorage,
         __in_matrix InMat2, __out_matrix OutMat, class BinaryDivideOp>
void triangular_matrix_matrix_left_solve(ExecutionPolicy&& exec,
                                         InMat1 A,
                                         Triangle t, DiagonalStorage d,
                                         InMat2 B, OutMat X,
                                         BinaryDivideOp divide);
 
template<__in_matrix InMat1, class Triangle, class DiagonalStorage,
         __inout_matrix InOutMat, class BinaryDivideOp>
void triangular_matrix_matrix_left_solve(InMat1 A, Triangle t, DiagonalStorage d,
                                         InOutMat B, BinaryDivideOp divide);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle, class DiagonalStorage,
         __inout_matrix InOutMat, class BinaryDivideOp>
void triangular_matrix_matrix_left_solve(ExecutionPolicy&& exec,
                                         InMat1 A, Triangle t, DiagonalStorage d,
                                         InOutMat B, BinaryDivideOp divide);
 
template<__in_matrix InMat1, class Triangle, class DiagonalStorage,
         __in_matrix InMat2, __out_matrix OutMat>
void triangular_matrix_matrix_left_solve(InMat1 A, Triangle t, DiagonalStorage d,
                                         InMat2 B, OutMat X);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle, class DiagonalStorage,
         __in_matrix InMat2, __out_matrix OutMat>
void triangular_matrix_matrix_left_solve(ExecutionPolicy&& exec,
                                         InMat1 A, Triangle t, DiagonalStorage d,
                                         InMat2 B, OutMat X);
 
template<__in_matrix InMat1, class Triangle, class DiagonalStorage,
         __inout_matrix InOutMat>
void triangular_matrix_matrix_left_solve(InMat1 A, Triangle t, DiagonalStorage d,
                                         InOutMat B);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle, class DiagonalStorage,
         __inout_matrix InOutMat>
void triangular_matrix_matrix_left_solve(ExecutionPolicy&& exec,
                                         InMat1 A, Triangle t, DiagonalStorage d,
                                         InOutMat B);
 
// solve multiple triangular linear systems
// with triangular matrix on the right
template<__in_matrix InMat1, class Triangle, class DiagonalStorage,
         __in_matrix InMat2, __out_matrix OutMat, class BinaryDivideOp>
void triangular_matrix_matrix_right_solve(InMat1 A, Triangle t, DiagonalStorage d,
                                          InMat2 B, OutMat X, BinaryDivideOp divide);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle, class DiagonalStorage,
         __in_matrix InMat2, __out_matrix OutMat, class BinaryDivideOp>
void triangular_matrix_matrix_right_solve(ExecutionPolicy&& exec,
                                          InMat1 A, Triangle t, DiagonalStorage d,
                                          InMat2 B, OutMat X, BinaryDivideOp divide);
 
template<__in_matrix InMat1, class Triangle, class DiagonalStorage,
         __inout_matrix InOutMat, class BinaryDivideOp>
void triangular_matrix_matrix_right_solve(InMat1 A, Triangle t, DiagonalStorage d,
                                          InOutMat B, BinaryDivideOp divide);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle, class DiagonalStorage,
         __inout_matrix InOutMat, class BinaryDivideOp>
void triangular_matrix_matrix_right_solve(ExecutionPolicy&& exec,
                                          InMat1 A, Triangle t, DiagonalStorage d,
                                          InOutMat B, BinaryDivideOp divide));
 
template<__in_matrix InMat1, class Triangle, class DiagonalStorage,
         __in_matrix InMat2, __out_matrix OutMat>
void triangular_matrix_matrix_right_solve(InMat1 A, Triangle t, DiagonalStorage d,
                                          InMat2 B, OutMat X);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle, class DiagonalStorage,
         __in_matrix InMat2, __out_matrix OutMat>
void triangular_matrix_matrix_right_solve(ExecutionPolicy&& exec,
                                          InMat1 A, Triangle t, DiagonalStorage d,
                                          InMat2 B, OutMat X);
 
template<__in_matrix InMat1, class Triangle, class DiagonalStorage,
         __inout_matrix InOutMat>
void triangular_matrix_matrix_right_solve(InMat1 A, Triangle t, DiagonalStorage d,
                                          InOutMat B);
 
template<class ExecutionPolicy,
         __in_matrix InMat1, class Triangle, class DiagonalStorage,
         __inout_matrix InOutMat>
void triangular_matrix_matrix_right_solve(ExecutionPolicy&& exec,
                                          InMat1 A, Triangle t, DiagonalStorage d,
                                          InOutMat B);
}

```

#### Tags

```
namespace std::linalg {
  struct column_major_t {
    explicit column_major_t() = default;
  };
  inline constexpr column_major_t column_major = { };
 
  struct row_major_t {
    explicit row_major_t() = default;
  };
  inline constexpr row_major_t row_major = { };
 
  struct upper_triangle_t {
    explicit upper_triangle_t() = default;
  };
  inline constexpr upper_triangle_t upper_triangle = { };
 
  struct lower_triangle_t {
    explicit lower_triangle_t() = default;
  };
  inline constexpr lower_triangle_t lower_triangle = { };
 
  struct implicit_unit_diagonal_t {
    explicit implicit_unit_diagonal_t() = default;
  };
  inline constexpr implicit_unit_diagonal_t implicit_unit_diagonal = { };
 
  struct explicit_diagonal_t {
    explicit explicit_diagonal_t() = default;
  };
  inline constexpr explicit_diagonal_t explicit_diagonal = { };
}

```

#### Class template std::linalg::layout_blas_packed

```
namespace std::linalg {
  template<class Triangle, class StorageOrder>
  class layout_blas_packed {
   public:
    using triangle_type = Triangle;
    using storage_order_type = StorageOrder;
 
    template<class Extents>
    struct mapping {
     public:
      using extents_type = Extents;
      using index_type = typename extents_type::index_type;
      using size_type = typename extents_type::size_type;
      using rank_type = typename extents_type::rank_type;
      using layout_type = layout_blas_packed<Triangle, StorageOrder>;
 
     private:
      Extents __the_extents{}; // exposition only
 
     public:
      constexpr mapping() noexcept = default;
      constexpr mapping(const mapping&) noexcept = default;
      constexpr mapping(const extents_type& e) noexcept;
      template<class OtherExtents>
      constexpr explicit(!is_convertible_v<OtherExtents, extents_type>)
      mapping(const mapping<OtherExtents>& other) noexcept;
 
      constexpr mapping& operator=(const mapping&) noexcept = default;
 
      constexpr extents_type extents() const noexcept { return __the_extents; }
 
      constexpr size_type required_span_size() const noexcept;
 
      template<class Index0, class Index1>
      constexpr index_type operator() (Index0 ind0, Index1 ind1) const noexcept;
 
      static constexpr bool is_always_unique() {
        return (extents_type::static_extent(0) != dynamic_extent &&
                extents_type::static_extent(0) < 2) ||
               (extents_type::static_extent(1) != dynamic_extent &&
                extents_type::static_extent(1) < 2);
      }
      static constexpr bool is_always_exhaustive() { return true; }
      static constexpr bool is_always_strided() {
        return is_always_unique();
      }
 
      constexpr bool is_unique() const noexcept {
        return __the_extents.extent(0) < 2;
      }
      constexpr bool is_exhaustive() const noexcept { return true; }
      constexpr bool is_strided() const noexcept {
        return __the_extents.extent(0) < 2;
      }
 
      constexpr index_type stride(rank_type) const noexcept;
 
      template<class OtherExtents>
      friend constexpr bool
      operator==(const mapping&, const mapping<OtherExtents>&) noexcept;
 
    };
  };
}

```

#### Class template std::linalg::scaled_accessor

```
namespace std::linalg {
  template<class ScalingFactor, class NestedAccessor>
  class scaled_accessor {
   public:
    using element_type = 
      add_const_t<decltype(declval<ScalingFactor>() * 
                           declval<NestedAccessor::element_type>())>;
    using reference = remove_const_t<element_type>;
    using data_handle_type = NestedAccessor::data_handle_type;
    using offset_policy = scaled_accessor<ScalingFactor, NestedAccessor::offset_policy>;
 
    constexpr scaled_accessor() = default;
    template<class OtherNestedAccessor>
      explicit(!is_convertible_v<OtherNestedAccessor, NestedAccessor>)
    constexpr scaled_accessor(const scaled_accessor<ScalingFactor, OtherNestedAccessor>&);
    constexpr scaled_accessor(const ScalingFactor& s, const Accessor& a);
 
    constexpr reference access(data_handle_type p, size_t i) const noexcept;
    constexpr 
      offset_policy::data_handle_type offset(data_handle_type p, size_t i) const noexcept;
 
    constexpr const ScalingFactor& scaling_factor() const noexcept 
      { return __scaling_factor; } 
    constexpr const NestedAccessor& nested_accessor() const noexcept
      { return __nested_accessor; }
 
   private:
    ScalingFactor __scaling_factor; // exposition only
    NestedAccessor __nested_accessor; // exposition only
  };
}

```

#### Class template std::linalg::conjugated_accessor

```
namespace std::linalg {
  template<class NestedAccessor>
  class conjugated_accessor {
   private:
    NestedAccessor __nested_accessor; // exposition only
 
   public:
    using element_type =
      add_const_t<decltype(/*conj-if-needed*/(declval<NestedAccessor::element_type>()))>;
    using reference = remove_const_t<element_type>;
    using data_handle_type = typename NestedAccessor::data_handle_type;
    using offset_policy = conjugated_accessor<NestedAccessor::offset_policy>;
 
    constexpr conjugated_accessor() = default;
    template<class OtherNestedAccessor>
      explicit(!is_convertible_v<OtherNestedAccessor, NestedAccessor>)
      constexpr conjugated_accessor(const conjugated_accessor<OtherNestedAccessor>& other);
 
    constexpr reference access(data_handle_type p, size_t i) const;
 
    constexpr typename offset_policy::data_handle_type
      offset(data_handle_type p, size_t i) const;
 
    constexpr const NestedAccessor& nested_accessor() const noexcept
      { return __nested_accessor; }
  };
}

```

#### Class template std::linalg::layout_transpose

```
namespace std::linalg {
  template<class InputExtents>
  using __transpose_extents_t = /* see description */; // exposition only
 
  template<class Layout>
  class layout_transpose {
   public:
    using nested_layout_type = Layout;
 
    template<class Extents>
    struct mapping {
     private:
      using __nested_mapping_type =
        typename Layout::template mapping<
          __transpose_extents_t<Extents>>;    // exposition only
 
      __nested_mapping_type __nested_mapping; // exposition only
        extents_type __extents;               // exposition only
 
     public:
      using extents_type = Extents;
      using index_type = typename extents_type::index_type;
      using size_type = typename extents_type::size_type;
      using rank_type = typename extents_type::rank_type;
      using layout_type = layout_transpose;
 
      constexpr explicit mapping(const __nested_mapping_type& map);
 
      constexpr const extents_type& extents() const noexcept { return __extents; }
 
      constexpr index_type required_span_size() const
        { return __nested_mapping.required_span_size(); }
 
      template<class Index0, class Index1>
        constexpr index_type operator()(Index0 ind0, Index1 ind1) const
        { return __nested_mapping(ind1, ind0); }
 
      constexpr const __nested_mapping_type& nested_mapping() const noexcept
        { return __nested_mapping; }
 
      static constexpr bool is_always_unique() noexcept
        { return __nested_mapping_type::is_always_unique(); }
      static constexpr bool is_always_exhaustive() noexcept
        { return __nested_mapping_type::is_always_exhaustive(); }
      static constexpr bool is_always_strided() noexcept
        { return __nested_mapping_type::is_always_strided(); }
 
      constexpr bool is_unique() const 
        { return __nested_mapping.is_unique(); }
      constexpr bool is_exhaustive() const 
        { return __nested_mapping.is_exhaustive(); }
      constexpr bool is_strided() const 
        { return __nested_mapping.is_strided(); }
 
      constexpr index_type stride(size_t r) const;
 
      template<class OtherExtents>
      friend constexpr bool
        operator==(const mapping& x, const mapping<OtherExtents>& y);
    };
  };
}

```

#### Helper concepts and traits

```
namespace std::linalg {
  template<class T>
  struct __is_mdspan : false_type {}; // exposition only
 
  template<class ElementType, class Extents, class Layout, class Accessor>
  struct __is_mdspan<mdspan<ElementType, Extents, Layout, Accessor>>
  : true_type {}; // exposition only
 
  template<class T>
  concept __in_vector = // exposition only
    __is_mdspan<T>::value &&
    T::rank() == 1;
 
  template<class T>
  concept __out_vector = // exposition only
    __is_mdspan<T>::value &&
    T::rank() == 1 &&
    is_assignable_v<typename T::reference, typename T::element_type> &&
    T::is_always_unique();
 
  template<class T>
  concept __inout_vector = // exposition only
    __is_mdspan<T>::value &&
    T::rank() == 1 &&
    is_assignable_v<typename T::reference, typename T::element_type> &&
    T::is_always_unique();
 
  template<class T>
  concept __in_matrix = // exposition only
    __is_mdspan<T>::value &&
    T::rank() == 2;
 
  template<class T>
  concept __out_matrix = // exposition only
    __is_mdspan<T>::value &&
    T::rank() == 2 &&
    is_assignable_v<typename T::reference, typename T::element_type> &&
   T::is_always_unique();
 
  template<class T>
  concept __inout_matrix = // exposition only
    __is_mdspan<T>::value &&
    T::rank() == 2 &&
    is_assignable_v<typename T::reference, typename T::element_type> &&
    T::is_always_unique();
 
  template<class T>
  concept __possibly_packed_inout_matrix = // exposition only
    __is_mdspan<T>::value &&
    T::rank() == 2 &&
    is_assignable_v<typename T::reference, typename T::element_type> &&
    (T::is_always_unique() || is_same_v<typename T::layout_type, layout_blas_packed>);
 
  template<class T>
  concept __in_object = // exposition only
    __is_mdspan<T>::value &&
    (T::rank() == 1 || T::rank() == 2);
 
  template<class T>
  concept __out_object = // exposition only
    __is_mdspan<T>::value &&
    (T::rank() == 1 || T::rank() == 2) &&
    is_assignable_v<typename T::reference, typename T::element_type> &&
    T::is_always_unique();
 
  template<class T>
  concept __inout_object = // exposition only
    __is_mdspan<T>::value &&
    (T::rank() == 1 || T::rank() == 2) &&
    is_assignable_v<typename T::reference, typename T::element_type> &&
    T::is_always_unique();
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/linalg&oldid=166372>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 December 2023, at 07:13.