# deduction guides for `std::span`

From cppreference.com
< cpp‎ | container‎ | span
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

Containers library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Sequence | | | | |
| array(C++11) | | | | |
| vector | | | | |
| vector<bool> | | | | |
| inplace_vector(C++26) | | | | |
| deque | | | | |
| forward_list(C++11) | | | | |
| list | | | | |
| Associative | | | | |
| set | | | | |
| multiset | | | | |
| map | | | | |
| multimap | | | | |
| Unordered associative | | | | |
| unordered_set(C++11) | | | | |
| unordered_multiset(C++11) | | | | |
| unordered_map(C++11) | | | | |
| unordered_multimap(C++11) | | | | |
| Adaptors | | | | |
| stack | | | | |
| queue | | | | |
| priority_queue | | | | |
| flat_set(C++23) | | | | |
| flat_multiset(C++23) | | | | |
| flat_map(C++23) | | | | |
| flat_multimap(C++23) | | | | |
| Views | | | | |
| span(C++20) | | | | |
| mdspan(C++23) | | | | |
| Tables | | | | |
| Iterator invalidation | | | | |
| Member function table | | | | |
| Non-member function table | | | | |

std::span

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| span::span | | | | |
| span::operator= | | | | |
| Element access | | | | |
| span::front | | | | |
| span::back | | | | |
| span::at(C++26) | | | | |
| [span::operator[]](operator_at.html "cpp/container/span/operator at") | | | | |
| span::data | | | | |
| Iterators | | | | |
| span::beginspan::cbegin(C++23) | | | | |
| span::endspan::cend(C++23) | | | | |
| span::rbeginspan::crbegin(C++23) | | | | |
| span::rendspan::crend(C++23) | | | | |
| Observers | | | | |
| span::empty | | | | |
| span::size | | | | |
| span::size_bytes | | | | |
| Subviews | | | | |
| span::first | | | | |
| span::last | | | | |
| span::subspan | | | | |
| Non-member functions | | | | |
| as_bytesas_writable_bytes | | | | |
| Non-member constant | | | | |
| dynamic_extent | | | | |
| ****Deduction guides**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<span>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| template< class It, class EndOrSize >  span( It, EndOrSize ) -> span<std::remove_reference_t<std::iter_reference_t<It>>>; |  | (since C++20)  (until C++26) |
| template< class It, class EndOrSize >  span( It, EndOrSize ) -> span<std::remove_reference_t<std::iter_reference_t<It>>, /\*maybe-static-ext\*/<EndOrSize>>; |  | (since C++26) |
|  |  |  |
| --- | --- | --- |
| template< class T, std::size_t N >  span( T (&)[N] ) -> span<T, N>; | (2) | (since C++20) |
| template< class T, std::size_t N >  span( std::array<T, N>& ) -> span<T, N>; | (3) | (since C++20) |
| template< class T, std::size_t N >  span( const std::array<T, N>& ) -> span<const T, N>; | (4) | (since C++20) |
| template< class R >  span( R&& ) -> span<std::remove_reference_t<std::ranges::range_reference_t<R>>>; | (5) | (since C++20) |
|  |  |  |

The following deduction guides are provided for `span`.

1) Allows the element type to be deduced from the iterator-sentinel pair. It also allows the static extent to be deduced if `EndOrSize` satisfies **integral-constant-like**.(since C++26). This overload participates in overload resolution only if `It` satisfies `contiguous_iterator`.2-4) Allows the static extent to be deduced from built-in arrays and std::array.5) Allows the element type to be deduced from ranges. This overload participates in overload resolution only if `R` satisfies `contiguous_range`.

### Example

Run this code

```
#include <array>
#include <cstddef>
#include <iomanip>
#include <iostream>
#include <span>
#include <string_view>
#include <vector>
 
void print(std::string_view rem = "", std::size_t size_of = 0, std::size_t extent = 0)
{
    if (rem.empty())
    {
        std::cout << "name │ sizeof │ extent\n"
                     "─────┼────────┼────────\n";
        return;
    }
    std::cout << std::setw(4) << rem << " │ " << std::setw(6) << size_of << " │ ";
    if (extent == std::dynamic_extent)
        std::cout << "dynamic";
    else
        std::cout << extent;
    std::cout << '\n';
}
 
int main()
{
    int a[]{1, 2, 3, 4, 5};
 
    print();
    std::span s1{std::begin(a), std::end(a)}; // guide (1)
    print("s1", sizeof s1, s1.extent);
 
    std::span s2{std::begin(a), 3}; // guide (1)
    print("s2", sizeof s2, s2.extent);
 
#if __cplusplus > 202302L
    std::span s3{std::begin(a), std::integral_constant<std::size_t, 2>{}}; // guide (1)
    print("s3", sizeof s3, s3.extent);
#endif // C++26
 
    std::span s4{a}; // guide (2)
    print("s4", sizeof s4, s4.extent);
 
    std::span<int> s5{a}; // does not use a guide, makes a dynamic span
    print("s5", sizeof s5, s5.extent);
 
    std::array arr{6, 7, 8};
    std::span s6{arr}; // guide (3)
    print("s6", sizeof s6, s6.extent);
    s6[0] = 42; // OK, element_type is 'int'
 
    const std::array arr2{9, 10, 11};
    std::span s7{arr2}; // guide (4)
    print("s7", sizeof s7, s7.extent);
    // s7[0] = 42; // Error: element_type is 'const int'
 
    std::vector v{66, 69, 99};
    std::span s8{v}; // guide (5)
    print("s8", sizeof s8, s8.extent);
}

```

Possible output:

```
name │ sizeof │ extent
─────┼────────┼────────
  s1 │     16 │ dynamic
  s2 │     16 │ dynamic
  s3 │      8 │ 2
  s4 │      8 │ 5
  s5 │     16 │ dynamic
  s6 │      8 │ 3
  s7 │      8 │ 3
  s8 │     16 │ dynamic

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/span/deduction_guides&oldid=171290>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 April 2024, at 07:29.