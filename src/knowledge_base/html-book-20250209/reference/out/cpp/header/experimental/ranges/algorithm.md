# Experimental library header <experimental/ranges/algorithm>

From cppreference.com
< cpp‎ | header‎ | experimental
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

Experimental library headers

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Execution P2300 | | | | |
| <experimental/execution> | | | | |
| Filesystem TS | | | | |
| <experimental/filesystem> | | | | |
| Parallelism TS (v1, v2) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/algorithm` | | | | | | `experimental/execution_policy` | | | | | | `experimental/exception_list` | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/numeric` | | | | | | <experimental/simd> | | | | | | `experimental/task_block` | | | | | |
| Library Fundamentals TS (v1, v2, v3) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/algorithm` | | | | | | <experimental/any> | | | | | | `experimental/array` | | | | | | `experimental/chrono` | | | | | | `experimental/deque` | | | | | | `experimental/forward_list` | | | | | | <experimental/functional> | | | | | | `experimental/future` | | | | | | `experimental/iterator` | | | | | | `experimental/list` | | | | | | `experimental/map` | | | | | | `experimental/memory` | | | | | | <experimental/memory_resource> | | | | | | `experimental/numeric` | | | | | | <experimental/optional> | | | | | | `experimental/propagate_const` | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/random` | | | | | | `experimental/ratio` | | | | | | `experimental/regex` | | | | | | `experimental/scope` | | | | | | `experimental/set` | | | | | | `experimental/source_location` | | | | | | `experimental/string` | | | | | | <experimental/string_view> | | | | | | `experimental/system_error` | | | | | | `experimental/tuple` | | | | | | `experimental/type_traits` | | | | | | `experimental/unordered_map` | | | | | | `experimental/unordered_set` | | | | | | `experimental/utility` | | | | | | `experimental/vector` | | | | | |  | | | | | |
| Concurrency TS | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/atomic` | | | | | | `experimental/barrier` | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/future` | | | | | | `experimental/latch` | | | | | |
| Ranges TS | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****<experimental/ranges/algorithm>**** | | | | | | <experimental/ranges/concepts> | | | | | | <experimental/ranges/functional> | | | | | | <experimental/ranges/iterator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | <experimental/ranges/random> | | | | | | <experimental/ranges/tuple> | | | | | | <experimental/ranges/type_traits> | | | | | | <experimental/ranges/utility> | | | | | |
| Coroutines TS | | | | |
| `experimental/coroutine` | | | | |
| Networking TS | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/buffer` | | | | | | `experimental/executor` | | | | | | `experimental/internet` | | | | | | `experimental/io_context` | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | <experimental/net> | | | | | | `experimental/netfwd` | | | | | | `experimental/socket` | | | | | | `experimental/timer` | | | | | |
| Reflection TS | | | | |
| <experimental/reflect> | | | | |

This header is part of the ranges library.

### Tag specifiers

|  |  |
| --- | --- |
| Defined in namespace `std::experimental::ranges::tag` | |
| inin1in2outout1out2funminmaxbeginend | tag specifiers for use with ranges::tagged   (class) |

### Non-modifying sequence operations

|  |  |
| --- | --- |
| Defined in namespace `std::experimental::ranges` | |
| all_ofany_ofnone_of | checks if a predicate is true for all, any or none of the elements in a range   (function template) |
| for_each | applies a function to a range of elements   (function template) |
| countcount_if | returns the number of elements satisfying specific criteria   (function template) |
| mismatch | finds the first position where two ranges differ   (function template) |
| equal | determines if two sets of elements are the same   (function template) |
| lexicographical_compare | returns true if one range is lexicographically less than another   (function template) |
| findfind_iffind_if_not | finds the first element satisfying specific criteria   (function template) |
| find_end | finds the last sequence of elements in a certain range   (function template) |
| find_first_of | searches for any one of a set of elements   (function template) |
| adjacent_find | finds the first two adjacent items that are equal (or satisfy a given predicate)   (function template) |
| search | searches for a range of elements   (function template) |
| search_n | searches for a number consecutive copies of an element in a range   (function template) |

### Modifying sequence operations

|  |  |
| --- | --- |
| Defined in namespace `std::experimental::ranges` | |
| copycopy_if | copies a range of elements to a new location   (function template) |
| copy_n") | copies a number of elements to a new location   (function template) |
| copy_backward") | copies a range of elements in backwards order   (function template) |
| move") | moves a range of elements to a new location   (function template) |
| move_backward") | moves a range of elements to a new location in backwards order   (function template) |
| fill") | assigns a range of elements a certain value   (function template) |
| fill_n") | assigns a value to a number of elements   (function template) |
| transform") | applies a function to a range of elements   (function template) |
| generate") | saves the result of a function in a range   (function template) |
| generate_n") | saves the result of N applications of a function   (function template) |
| removeremove_if") | removes elements satisfying specific criteria   (function template) |
| remove_copyremove_copy_if") | copies a range of elements omitting those that satisfy specific criteria   (function template) |
| replacereplace_if") | replaces all values satisfying specific criteria with another value   (function template) |
| replace_copyreplace_copy_if") | copies a range, replacing elements satisfying specific criteria with another value   (function template) |
| swap_ranges") | swaps two ranges of elements   (function template) |
| reverse") | reverses the order of elements in a range   (function template) |
| reverse_copy") | creates a copy of a range that is reversed   (function template) |
| rotate") | rotates the order of elements in a range   (function template) |
| rotate_copy") | copies and rotate a range of elements   (function template) |
| shuffle") | randomly re-orders elements in a range   (function template) |
| unique") | removes consecutive duplicate elements in a range   (function template) |
| unique_copy") | creates a copy of some range of elements that contains no consecutive duplicates   (function template) |

### Partitioning operations

|  |  |
| --- | --- |
| Defined in namespace `std::experimental::ranges` | |
| is_partitioned") | determines if the range is partitioned by the given predicate   (function template) |
| partition") | divides a range of elements into two groups   (function template) |
| partition_copy") | copies a range dividing the elements into two groups   (function template) |
| stable_partition") | divides elements into two groups while preserving their relative order   (function template) |
| partition_point") | locates the partition point of a partitioned range   (function template) |

### Sorting operations

|  |  |
| --- | --- |
| Defined in namespace `std::experimental::ranges` | |
| is_sorted") | checks whether a range is sorted into ascending order   (function template) |
| is_sorted_until") | finds the largest sorted subrange   (function template) |
| sort | sorts a range into ascending order   (function template) |
| partial_sort") | sorts the first N elements of a range   (function template) |
| partial_sort_copy") | copies and partially sorts a range of elements   (function template) |
| stable_sort") | sorts a range of elements while preserving order between equal elements   (function template) |
| nth_element") | partially sorts the given range making sure that it is partitioned by the given element   (function template) |

### Binary search operations (on sorted ranges)

|  |  |
| --- | --- |
| Defined in namespace `std::experimental::ranges` | |
| lower_bound") | returns an iterator to the first element **not less** than the given value   (function template) |
| upper_bound") | returns an iterator to the first element **greater** than a certain value   (function template) |
| binary_search") | determines if an element exists in a certain range   (function template) |
| equal_range") | returns range of elements matching a specific key   (function template) |

### Set operations (on sorted ranges)

|  |  |
| --- | --- |
| Defined in namespace `std::experimental::ranges` | |
| merge") | merges two sorted ranges   (function template) |
| inplace_merge") | merges two ordered ranges in-place   (function template) |
| includes") | returns true if one set is a subset of another   (function template) |
| set_difference") | computes the difference between two sets   (function template) |
| set_intersection") | computes the intersection of two sets   (function template) |
| set_symmetric_difference") | computes the symmetric difference between two sets   (function template) |
| set_union") | computes the union of two sets   (function template) |

### Heap operations

|  |  |
| --- | --- |
| Defined in namespace `std::experimental::ranges` | |
| is_heap") | checks if the given range is a max heap   (function template) |
| is_heap_until") | finds the largest subrange that is a max heap   (function template) |
| make_heap") | creates a max heap out of a range of elements   (function template) |
| push_heap") | adds an element to a max heap   (function template) |
| pop_heap") | removes the largest element from a max heap   (function template) |
| sort_heap") | turns a max heap into a range of elements sorted in ascending order   (function template) |

### Minimum/maximum operations

|  |  |
| --- | --- |
| Defined in namespace `std::experimental::ranges` | |
| max") | returns the greater of the given values   (function template) |
| max_element") | returns the largest element in a range   (function template) |
| min") | returns the smaller of the given values   (function template) |
| min_element") | returns the smallest element in a range   (function template) |
| minmax") | returns the smaller and larger of two elements   (function template) |
| minmax_element") | returns the smallest and the largest elements in a range   (function template) |

### Permutation operations

|  |  |
| --- | --- |
| Defined in namespace `std::experimental::ranges` | |
| is_permutation | determines if a sequence is a permutation of another sequence   (function template) |
| next_permutation") | generates the next greater lexicographic permutation of a range of elements   (function template) |
| prev_permutation") | generates the next smaller lexicographic permutation of a range of elements   (function template) |

### Synopsis

```
#include <initializer_list>
 
namespace std { namespace experimental { namespace ranges { inline namespace v1 {
 
namespace tag {
  struct in;
  struct in1;
  struct in2;
  struct out;
  struct out1;
  struct out2;
  struct fun;
  struct min;
  struct max;
  struct begin;
  struct end;
}
 
template <InputIterator I, Sentinel<I> S, class Proj = identity,
    IndirectUnaryPredicate<projected<I, Proj>> Pred>
  bool all_of(I first, S last, Pred pred, Proj proj = Proj{});
 
template <InputRange Rng, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  bool all_of(Rng&& rng, Pred pred, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, class Proj = identity,
    IndirectUnaryPredicate<projected<I, Proj>> Pred>
  bool any_of(I first, S last, Pred pred, Proj proj = Proj{});
 
template <InputRange Rng, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  bool any_of(Rng&& rng, Pred pred, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, class Proj = identity,
    IndirectUnaryPredicate<projected<I, Proj>> Pred>
  bool none_of(I first, S last, Pred pred, Proj proj = Proj{});
 
template <InputRange Rng, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  bool none_of(Rng&& rng, Pred pred, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, class Proj = identity,
    IndirectUnaryInvocable<projected<I, Proj>> Fun>
  tagged_pair<tag::in(I), tag::fun(Fun)>
    for_each(I first, S last, Fun f, Proj proj = Proj{});
 
template <InputRange Rng, class Proj = identity,
    IndirectUnaryInvocable<projected<iterator_t<Rng>, Proj>> Fun>
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::fun(Fun)>
    for_each(Rng&& rng, Fun f, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, class T, class Proj = identity>
  requires IndirectRelation<equal_to<>, projected<I, Proj>, const T*>
  I find(I first, S last, const T& value, Proj proj = Proj{});
 
template <InputRange Rng, class T, class Proj = identity>
  requires IndirectRelation<equal_to<>, projected<iterator_t<Rng>, Proj>, const T*>
  safe_iterator_t<Rng>
    find(Rng&& rng, const T& value, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, class Proj = identity,
    IndirectUnaryPredicate<projected<I, Proj>> Pred>
  I find_if(I first, S last, Pred pred, Proj proj = Proj{});
 
template <InputRange Rng, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  safe_iterator_t<Rng>
    find_if(Rng&& rng, Pred pred, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, class Proj = identity,
    IndirectUnaryPredicate<projected<I, Proj>> Pred>
  I find_if_not(I first, S last, Pred pred, Proj proj = Proj{});
 
template <InputRange Rng, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  safe_iterator_t<Rng>
    find_if_not(Rng&& rng, Pred pred, Proj proj = Proj{});
 
template <ForwardIterator I1, Sentinel<I1> S1, ForwardIterator I2,
    Sentinel<I2> S2, class Proj = identity,
    IndirectRelation<I2, projected<I1, Proj>> Pred = equal_to<>>
  I1
    find_end(I1 first1, S1 last1, I2 first2, S2 last2,
             Pred pred = Pred{}, Proj proj = Proj{});
 
template <ForwardRange Rng1, ForwardRange Rng2, class Proj = identity,
    IndirectRelation<iterator_t<Rng2>,
      projected<iterator_t<Rng>, Proj>> Pred = equal_to<>>
  safe_iterator_t<Rng1>
    find_end(Rng1&& rng1, Rng2&& rng2, Pred pred = Pred{}, Proj proj = Proj{});
 
template <InputIterator I1, Sentinel<I1> S1, ForwardIterator I2, Sentinel<I2> S2,
    class Proj1 = identity, class Proj2 = identity,
    IndirectRelation<projected<I1, Proj1>, projected<I2, Proj2>> Pred = equal_to<>>
  I1
    find_first_of(I1 first1, S1 last1, I2 first2, S2 last2,
                  Pred pred = Pred{},
                  Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputRange Rng1, ForwardRange Rng2, class Proj1 = identity,
    class Proj2 = identity,
    IndirectRelation<projected<iterator_t<Rng1>, Proj1>,
      projected<iterator_t<Rng2>, Proj2>> Pred = equal_to<>>
  safe_iterator_t<Rng1>
    find_first_of(Rng1&& rng1, Rng2&& rng2,
                  Pred pred = Pred{},
                  Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <ForwardIterator I, Sentinel<I> S, class Proj = identity,
    IndirectRelation<projected<I, Proj>> Pred = equal_to<>>
  I
    adjacent_find(I first, S last, Pred pred = Pred{},
                  Proj proj = Proj{});
 
template <ForwardRange Rng, class Proj = identity,
    IndirectRelation<projected<iterator_t<Rng>, Proj>> Pred = equal_to<>>
  safe_iterator_t<Rng>
    adjacent_find(Rng&& rng, Pred pred = Pred{}, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, class T, class Proj = identity>
  requires IndirectRelation<equal_to<>, projected<I, Proj>, const T*>
  difference_type_t<I>
    count(I first, S last, const T& value, Proj proj = Proj{});
 
template <InputRange Rng, class T, class Proj = identity>
  requires IndirectRelation<equal_to<>, projected<iterator_t<Rng>, Proj>, const T*>
  difference_type_t<iterator_t<Rng>>
    count(Rng&& rng, const T& value, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, class Proj = identity,
    IndirectUnaryPredicate<projected<I, Proj>> Pred>
  difference_type_t<I>
    count_if(I first, S last, Pred pred, Proj proj = Proj{});
 
template <InputRange Rng, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  difference_type_t<iterator_t<Rng>>
    count_if(Rng&& rng, Pred pred, Proj proj = Proj{});
 
template <InputIterator I1, Sentinel<I1> S1, InputIterator I2, Sentinel<I2> S2,
    class Proj1 = identity, class Proj2 = identity,
    IndirectRelation<projected<I1, Proj1>, projected<I2, Proj2>> Pred = equal_to<>>
  tagged_pair<tag::in1(I1), tag::in2(I2)>
    mismatch(I1 first1, S1 last1, I2 first2, S2 last2, Pred pred = Pred{},
             Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputRange Rng1, InputRange Rng2,
    class Proj1 = identity, class Proj2 = identity,
    IndirectRelation<projected<iterator_t<Rng1>, Proj1>,
      projected<iterator_t<Rng2>, Proj2>> Pred = equal_to<>>
  tagged_pair<tag::in1(safe_iterator_t<Rng1>),
              tag::in2(safe_iterator_t<Rng2>)>
    mismatch(Rng1&& rng1, Rng2&& rng2, Pred pred = Pred{},
             Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputIterator I1, Sentinel<I1> S1, InputIterator I2, Sentinel<I2> S2,
    class Pred = equal_to<>, class Proj1 = identity, class Proj2 = identity>
  requires IndirectlyComparable<I1, I2, Pred, Proj1, Proj2>
  bool equal(I1 first1, S1 last1, I2 first2, S2 last2,
             Pred pred = Pred{},
             Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputRange Rng1, InputRange Rng2, class Pred = equal_to<>,
    class Proj1 = identity, class Proj2 = identity>
  requires IndirectlyComparable<iterator_t<Rng1>, iterator_t<Rng2>, Pred, Proj1, Proj2>
  bool equal(Rng1&& rng1, Rng2&& rng2, Pred pred = Pred{},
             Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <ForwardIterator I1, Sentinel<I1> S1, ForwardIterator I2,
    Sentinel<I2> S2, class Pred = equal_to<>, class Proj1 = identity,
    class Proj2 = identity>
  requires IndirectlyComparable<I1, I2, Pred, Proj1, Proj2>
  bool is_permutation(I1 first1, S1 last1, I2 first2, S2 last2,
                      Pred pred = Pred{},
                      Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <ForwardRange Rng1, ForwardRange Rng2, class Pred = equal_to<>,
    class Proj1 = identity, class Proj2 = identity>
  requires IndirectlyComparable<iterator_t<Rng1>, iterator_t<Rng2>, Pred, Proj1, Proj2>
  bool is_permutation(Rng1&& rng1, Rng2&& rng2, Pred pred = Pred{},
                      Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <ForwardIterator I1, Sentinel<I1> S1, ForwardIterator I2,
    Sentinel<I2> S2, class Pred = equal_to<>,
    class Proj1 = identity, class Proj2 = identity>
  requires IndirectlyComparable<I1, I2, Pred, Proj1, Proj2>
  I1
    search(I1 first1, S1 last1, I2 first2, S2 last2,
           Pred pred = Pred{},
           Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <ForwardRange Rng1, ForwardRange Rng2, class Pred = equal_to<>,
    class Proj1 = identity, class Proj2 = identity>
  requires IndirectlyComparable<iterator_t<Rng1>, iterator_t<Rng2>, Pred, Proj1, Proj2>
  safe_iterator_t<Rng1>
    search(Rng1&& rng1, Rng2&& rng2, Pred pred = Pred{},
           Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <ForwardIterator I, Sentinel<I> S, class T,
    class Pred = equal_to<>, class Proj = identity>
  requires IndirectlyComparable<I, const T*, Pred, Proj>
  I
    search_n(I first, S last, difference_type_t<I> count,
             const T& value, Pred pred = Pred{},
             Proj proj = Proj{});
 
template <ForwardRange Rng, class T, class Pred = equal_to<>,
    class Proj = identity>
  requires IndirectlyComparable<iterator_t<Rng>, const T*, Pred, Proj>
  safe_iterator_t<Rng>
    search_n(Rng&& rng, difference_type_t<iterator_t<Rng>> count,
             const T& value, Pred pred = Pred{}, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, WeaklyIncrementable O>
  requires IndirectlyCopyable<I, O>
  tagged_pair<tag::in(I), tag::out(O)>
    copy(I first, S last, O result);
 
template <InputRange Rng, WeaklyIncrementable O>
  requires IndirectlyCopyable<iterator_t<Rng>, O>
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::out(O)>
    copy(Rng&& rng, O result);
 
template <InputIterator I, WeaklyIncrementable O>
  requires IndirectlyCopyable<I, O>
  tagged_pair<tag::in(I), tag::out(O)>
    copy_n(I first, difference_type_t<I> n, O result);
 
template <InputIterator I, Sentinel<I> S, WeaklyIncrementable O, class Proj = identity,
    IndirectUnaryPredicate<projected<I, Proj>> Pred>
  requires IndirectlyCopyable<I, O>
  tagged_pair<tag::in(I), tag::out(O)>
    copy_if(I first, S last, O result, Pred pred, Proj proj = Proj{});
 
template <InputRange Rng, WeaklyIncrementable O, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  requires IndirectlyCopyable<iterator_t<Rng>, O>
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::out(O)>
    copy_if(Rng&& rng, O result, Pred pred, Proj proj = Proj{});
 
template <BidirectionalIterator I1, Sentinel<I1> S1, BidirectionalIterator I2>
  requires IndirectlyCopyable<I1, I2>
  tagged_pair<tag::in(I1), tag::out(I2)>
    copy_backward(I1 first, S1 last, I2 result);
 
template <BidirectionalRange Rng, BidirectionalIterator I>
  requires IndirectlyCopyable<iterator_t<Rng>, I>
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::out(I)>
    copy_backward(Rng&& rng, I result);
 
template <InputIterator I, Sentinel<I> S, WeaklyIncrementable O>
  requires IndirectlyMovable<I, O>
  tagged_pair<tag::in(I), tag::out(O)>
    move(I first, S last, O result);
 
template <InputRange Rng, WeaklyIncrementable O>
  requires IndirectlyMovable<iterator_t<Rng>, O>
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::out(O)>
    move(Rng&& rng, O result);
 
template <BidirectionalIterator I1, Sentinel<I1> S1, BidirectionalIterator I2>
  requires IndirectlyMovable<I1, I2>
  tagged_pair<tag::in(I1), tag::out(I2)>
    move_backward(I1 first, S1 last, I2 result);
 
template <BidirectionalRange Rng, BidirectionalIterator I>
  requires IndirectlyMovable<iterator_t<Rng>, I>
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::out(I)>
    move_backward(Rng&& rng, I result);
 
template <ForwardIterator I1, Sentinel<I1> S1, ForwardIterator I2, Sentinel<I2> S2>
  requires IndirectlySwappable<I1, I2>
  tagged_pair<tag::in1(I1), tag::in2(I2)>
    swap_ranges(I1 first1, S1 last1, I2 first2, S2 last2);
 
template <ForwardRange Rng1, ForwardRange Rng2>
  requires IndirectlySwappable<iterator_t<Rng1>, iterator_t<Rng2>>
  tagged_pair<tag::in1(safe_iterator_t<Rng1>), tag::in2(safe_iterator_t<Rng2>)>
    swap_ranges(Rng1&& rng1, Rng2&& rng2);
 
template <InputIterator I, Sentinel<I> S, WeaklyIncrementable O,
    CopyConstructible F, class Proj = identity>
  requires Writable<O, indirect_result_of_t<F&(projected<I, Proj>)>>
  tagged_pair<tag::in(I), tag::out(O)>
    transform(I first, S last, O result, F op, Proj proj = Proj{});
 
template <InputRange Rng, WeaklyIncrementable O, CopyConstructible F,
    class Proj = identity>
  requires Writable<O, indirect_result_of_t<F&(
    projected<iterator_t<R>, Proj>)>>
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::out(O)>
    transform(Rng&& rng, O result, F op, Proj proj = Proj{});
 
template <InputIterator I1, Sentinel<I1> S1, InputIterator I2, Sentinel<I2> S2,
    WeaklyIncrementable O, CopyConstructible F, class Proj1 = identity,
    class Proj2 = identity>
  requires Writable<O, indirect_result_of_t<F&(projected<I1, Proj1>,
    projected<I2, Proj2>)>>
  tagged_tuple<tag::in1(I1), tag::in2(I2), tag::out(O)>
    transform(I1 first1, S1 last1, I2 first2, S2 last2, O result,
              F binary_op, Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputRange Rng1, InputRange Rng2, WeaklyIncrementable O,
    CopyConstructible F, class Proj1 = identity, class Proj2 = identity>
  requires Writable<O, indirect_result_of_t<F&(
    projected<iterator_t<Rng1>, Proj1>, projected<iterator_t<Rng2>, Proj2>)>>
  tagged_tuple<tag::in1(safe_iterator_t<Rng1>),
               tag::in2(safe_iterator_t<Rng2>),
               tag::out(O)>
    transform(Rng1&& rng1, Rng2&& rng2, O result,
              F binary_op, Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputIterator I, Sentinel<I> S, class T1, class T2, class Proj = identity>
  requires Writable<I, const T2&> &&
    IndirectRelation<equal_to<>, projected<I, Proj>, const T1*>
  I
    replace(I first, S last, const T1& old_value, const T2& new_value, Proj proj = Proj{});
 
template <InputRange Rng, class T1, class T2, class Proj = identity>
  requires Writable<iterator_t<Rng>, const T2&> &&
    IndirectRelation<equal_to<>, projected<iterator_t<Rng>, Proj>, const T1*>
  safe_iterator_t<Rng>
    replace(Rng&& rng, const T1& old_value, const T2& new_value, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, class T, class Proj = identity,
    IndirectUnaryPredicate<projected<I, Proj>> Pred>
  requires Writable<I, const T&>
  I
    replace_if(I first, S last, Pred pred, const T& new_value, Proj proj = Proj{});
 
template <InputRange Rng, class T, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  requires Writable<iterator_t<Rng>, const T&>
  safe_iterator_t<Rng>
    replace_if(Rng&& rng, Pred pred, const T& new_value, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, class T1, class T2, OutputIterator<const T2&> O,
    class Proj = identity>
  requires IndirectlyCopyable<I, O> &&
    IndirectRelation<equal_to<>, projected<I, Proj>, const T1*>
  tagged_pair<tag::in(I), tag::out(O)>
    replace_copy(I first, S last, O result, const T1& old_value, const T2& new_value,
                 Proj proj = Proj{});
 
template <InputRange Rng, class T1, class T2, OutputIterator<const T2&> O,
    class Proj = identity>
  requires IndirectlyCopyable<iterator_t<Rng>, O> &&
    IndirectRelation<equal_to<>, projected<iterator_t<Rng>, Proj>, const T1*>
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::out(O)>
    replace_copy(Rng&& rng, O result, const T1& old_value, const T2& new_value,
                 Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, class T, OutputIterator<const T&> O,
    class Proj = identity, IndirectUnaryPredicate<projected<I, Proj>> Pred>
  requires IndirectlyCopyable<I, O>
  tagged_pair<tag::in(I), tag::out(O)>
    replace_copy_if(I first, S last, O result, Pred pred, const T& new_value,
                    Proj proj = Proj{});
 
template <InputRange Rng, class T, OutputIterator<const T&> O, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  requires IndirectlyCopyable<iterator_t<Rng>, O>
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::out(O)>
    replace_copy_if(Rng&& rng, O result, Pred pred, const T& new_value,
                    Proj proj = Proj{});
 
template <class T, OutputIterator<const T&> O, Sentinel<O> S>
  O fill(O first, S last, const T& value);
 
template <class T, OutputRange<const T&> Rng>
  safe_iterator_t<Rng>
    fill(Rng&& rng, const T& value);
 
template <class T, OutputIterator<const T&> O>
  O fill_n(O first, difference_type_t<O> n, const T& value);
 
template <Iterator O, Sentinel<O> S, CopyConstructible F>
  requires Invocable<F&> && Writable<O, result_of_t<F&()>>
  O generate(O first, S last, F gen);
 
template <class Rng, CopyConstructible F>
  requires Invocable<F&> && OutputRange<Rng, result_of_t<F&()>>
  safe_iterator_t<Rng>
    generate(Rng&& rng, F gen);
 
template <Iterator O, CopyConstructible F>
  requires Invocable<F&> && Writable<O, result_of_t<F&()>>
  O generate_n(O first, difference_type_t<O> n, F gen);
 
template <ForwardIterator I, Sentinel<I> S, class T, class Proj = identity>
  requires Permutable<I> &&
    IndirectRelation<equal_to<>, projected<I, Proj>, const T*>
  I remove(I first, S last, const T& value, Proj proj = Proj{});
 
template <ForwardRange Rng, class T, class Proj = identity>
  requires Permutable<iterator_t<Rng>> &&
    IndirectRelation<equal_to<>, projected<iterator_t<Rng>, Proj>, const T*>
  safe_iterator_t<Rng>
    remove(Rng&& rng, const T& value, Proj proj = Proj{});
 
template <ForwardIterator I, Sentinel<I> S, class Proj = identity,
    IndirectUnaryPredicate<projected<I, Proj>> Pred>
  requires Permutable<I>
    I remove_if(I first, S last, Pred pred, Proj proj = Proj{});
 
template <ForwardRange Rng, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  requires Permutable<iterator_t<Rng>>
  safe_iterator_t<Rng>
    remove_if(Rng&& rng, Pred pred, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, WeaklyIncrementable O, class T,
    class Proj = identity>
  requires IndirectlyCopyable<I, O> &&
    IndirectRelation<equal_to<>, projected<I, Proj>, const T*>
  tagged_pair<tag::in(I), tag::out(O)>
    remove_copy(I first, S last, O result, const T& value, Proj proj = Proj{});
 
template <InputRange Rng, WeaklyIncrementable O, class T, class Proj = identity>
  requires IndirectlyCopyable<iterator_t<Rng>, O> &&
    IndirectRelation<equal_to<>, projected<iterator_t<Rng>, Proj>, const T*>
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::out(O)>
    remove_copy(Rng&& rng, O result, const T& value, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, WeaklyIncrementable O,
    class Proj = identity, IndirectUnaryPredicate<projected<I, Proj>> Pred>
  requires IndirectlyCopyable<I, O>
  tagged_pair<tag::in(I), tag::out(O)>
    remove_copy_if(I first, S last, O result, Pred pred, Proj proj = Proj{});
 
template <InputRange Rng, WeaklyIncrementable O, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  requires IndirectlyCopyable<iterator_t<Rng>, O>
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::out(O)>
    remove_copy_if(Rng&& rng, O result, Pred pred, Proj proj = Proj{});
 
template <ForwardIterator I, Sentinel<I> S, class Proj = identity,
    IndirectRelation<projected<I, Proj>> R = equal_to<>>
  requires Permutable<I>
  I unique(I first, S last, R comp = R{}, Proj proj = Proj{});
 
template <ForwardRange Rng, class Proj = identity,
    IndirectRelation<projected<iterator_t<Rng>, Proj>> R = equal_to<>>
  requires Permutable<iterator_t<Rng>>
  safe_iterator_t<Rng>
    unique(Rng&& rng, R comp = R{}, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, WeaklyIncrementable O,
    class Proj = identity, IndirectRelation<projected<I, Proj>> R = equal_to<>>
  requires IndirectlyCopyable<I, O> &&
    (ForwardIterator<I> ||
    (InputIterator<O> && Same<value_type_t<I>, value_type_t<O>>) ||
    IndirectlyCopyableStorable<I, O>)
  tagged_pair<tag::in(I), tag::out(O)>
    unique_copy(I first, S last, O result, R comp = R{}, Proj proj = Proj{});
 
template <InputRange Rng, WeaklyIncrementable O, class Proj = identity,
    IndirectRelation<projected<iterator_t<Rng>, Proj>> R = equal_to<>>
  requires IndirectlyCopyable<iterator_t<Rng>, O> &&
    (ForwardIterator<iterator_t<Rng>> ||
    (InputIterator<O> && Same<value_type_t<iterator_t<Rng>>, value_type_t<O>>) ||
    IndirectlyCopyableStorable<iterator_t<Rng>, O>)
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::out(O)>
    unique_copy(Rng&& rng, O result, R comp = R{}, Proj proj = Proj{});
 
template <BidirectionalIterator I, Sentinel<I> S>
  requires Permutable<I>
  I reverse(I first, S last);
 
template <BidirectionalRange Rng>
  requires Permutable<iterator_t<Rng>>
  safe_iterator_t<Rng>
    reverse(Rng&& rng);
 
template <BidirectionalIterator I, Sentinel<I> S, WeaklyIncrementable O>
  requires IndirectlyCopyable<I, O>
  tagged_pair<tag::in(I), tag::out(O)> reverse_copy(I first, S last, O result);
 
template <BidirectionalRange Rng, WeaklyIncrementable O>
  requires IndirectlyCopyable<iterator_t<Rng>, O>
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::out(O)>
    reverse_copy(Rng&& rng, O result);
 
template <ForwardIterator I, Sentinel<I> S>
  requires Permutable<I>
  tagged_pair<tag::begin(I), tag::end(I)>
    rotate(I first, I middle, S last);
 
template <ForwardRange Rng>
  requires Permutable<iterator_t<Rng>>
  tagged_pair<tag::begin(safe_iterator_t<Rng>),
              tag::end(safe_iterator_t<Rng>)>
    rotate(Rng&& rng, iterator_t<Rng> middle);
 
template <ForwardIterator I, Sentinel<I> S, WeaklyIncrementable O>
  requires IndirectlyCopyable<I, O>
  tagged_pair<tag::in(I), tag::out(O)>
    rotate_copy(I first, I middle, S last, O result);
 
template <ForwardRange Rng, WeaklyIncrementable O>
  requires IndirectlyCopyable<iterator_t<Rng>, O>
  tagged_pair<tag::in(safe_iterator_t<Rng>), tag::out(O)>
    rotate_copy(Rng&& rng, iterator_t<Rng> middle, O result);
 
template <RandomAccessIterator I, Sentinel<I> S, class Gen>
  requires Permutable<I> &&
    UniformRandomNumberGenerator<remove_reference_t<Gen>> &&
    ConvertibleTo<result_of_t<Gen&()>, difference_type_t<I>>
  I shuffle(I first, S last, Gen&& g);
 
template <RandomAccessRange Rng, class Gen>
  requires Permutable<I> &&
    UniformRandomNumberGenerator<remove_reference_t<Gen>> &&
    ConvertibleTo<result_of_t<Gen&()>, difference_type_t<I>>
  safe_iterator_t<Rng>
    shuffle(Rng&& rng, Gen&& g);
 
template <InputIterator I, Sentinel<I> S, class Proj = identity,
    IndirectUnaryPredicate<projected<I, Proj>> Pred>
  bool is_partitioned(I first, S last, Pred pred, Proj proj = Proj{});
 
template <InputRange Rng, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  bool
    is_partitioned(Rng&& rng, Pred pred, Proj proj = Proj{});
 
template <ForwardIterator I, Sentinel<I> S, class Proj = identity,
    IndirectUnaryPredicate<projected<I, Proj>> Pred>
  requires Permutable<I>
    I partition(I first, S last, Pred pred, Proj proj = Proj{});
 
template <ForwardRange Rng, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  requires Permutable<iterator_t<Rng>>
  safe_iterator_t<Rng>
    partition(Rng&& rng, Pred pred, Proj proj = Proj{});
 
template <BidirectionalIterator I, Sentinel<I> S, class Proj = identity,
    IndirectUnaryPredicate<projected<I, Proj>> Pred>
  requires Permutable<I>
  I stable_partition(I first, S last, Pred pred, Proj proj = Proj{});
 
template <BidirectionalRange Rng, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  requires Permutable<iterator_t<Rng>>
  safe_iterator_t<Rng>
    stable_partition(Rng&& rng, Pred pred, Proj proj = Proj{});
 
template <InputIterator I, Sentinel<I> S, WeaklyIncrementable O1, WeaklyIncrementable O2,
    class Proj = identity, IndirectUnaryPredicate<projected<I, Proj>> Pred>
  requires IndirectlyCopyable<I, O1> && IndirectlyCopyable<I, O2>
  tagged_tuple<tag::in(I), tag::out1(O1), tag::out2(O2)>
    partition_copy(I first, S last, O1 out_true, O2 out_false, Pred pred,
                   Proj proj = Proj{});
 
template <InputRange Rng, WeaklyIncrementable O1, WeaklyIncrementable O2,
    class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  requires IndirectlyCopyable<iterator_t<Rng>, O1> &&
    IndirectlyCopyable<iterator_t<Rng>, O2>
  tagged_tuple<tag::in(safe_iterator_t<Rng>), tag::out1(O1), tag::out2(O2)>
    partition_copy(Rng&& rng, O1 out_true, O2 out_false, Pred pred, Proj proj = Proj{});
 
template <ForwardIterator I, Sentinel<I> S, class Proj = identity,
    IndirectUnaryPredicate<projected<I, Proj>> Pred>
  I partition_point(I first, S last, Pred pred, Proj proj = Proj{});
 
template <ForwardRange Rng, class Proj = identity,
    IndirectUnaryPredicate<projected<iterator_t<Rng>, Proj>> Pred>
  safe_iterator_t<Rng>
    partition_point(Rng&& rng, Pred pred, Proj proj = Proj{});
 
template <RandomAccessIterator I, Sentinel<I> S, class Comp = less<>,
    class Proj = identity>
  requires Sortable<I, Comp, Proj>
    I sort(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessRange Rng, class Comp = less<>, class Proj = identity>
  requires Sortable<iterator_t<Rng>, Comp, Proj>
  safe_iterator_t<Rng>
    sort(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessIterator I, Sentinel<I> S, class Comp = less<>,
    class Proj = identity>
  requires Sortable<I, Comp, Proj>
    I stable_sort(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessRange Rng, class Comp = less<>, class Proj = identity>
  requires Sortable<iterator_t<Rng>, Comp, Proj>
  safe_iterator_t<Rng>
    stable_sort(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessIterator I, Sentinel<I> S, class Comp = less<>,
    class Proj = identity>
  requires Sortable<I, Comp, Proj>
    I partial_sort(I first, I middle, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessRange Rng, class Comp = less<>, class Proj = identity>
  requires Sortable<iterator_t<Rng>, Comp, Proj>
  safe_iterator_t<Rng>
    partial_sort(Rng&& rng, iterator_t<Rng> middle, Comp comp = Comp{},
                 Proj proj = Proj{});
 
template <InputIterator I1, Sentinel<I1> S1, RandomAccessIterator I2, Sentinel<I2> S2,
    class Comp = less<>, class Proj1 = identity, class Proj2 = identity>
  requires IndirectlyCopyable<I1, I2> && Sortable<I2, Comp, Proj2> &&
    IndirectStrictWeakOrder<Comp, projected<I1, Proj1>, projected<I2, Proj2>>
  I2
    partial_sort_copy(I1 first, S1 last, I2 result_first, S2 result_last,
                      Comp comp = Comp{}, Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputRange Rng1, RandomAccessRange Rng2, class Comp = less<>,
    class Proj1 = identity, class Proj2 = identity>
  requires IndirectlyCopyable<iterator_t<Rng1>, iterator_t<Rng2>> &&
    Sortable<iterator_t<Rng2>, Comp, Proj2> &&
    IndirectStrictWeakOrder<Comp, projected<iterator_t<Rng1>, Proj1>,
      projected<iterator_t<Rng2>, Proj2>>
  safe_iterator_t<Rng2>
    partial_sort_copy(Rng1&& rng, Rng2&& result_rng, Comp comp = Comp{},
                      Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <ForwardIterator I, Sentinel<I> S, class Proj = identity,
    IndirectStrictWeakOrder<projected<I, Proj>> Comp = less<>>
  bool is_sorted(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardRange Rng, class Proj = identity,
    IndirectStrictWeakOrder<projected<iterator_t<Rng>, Proj>> Comp = less<>>
  bool
    is_sorted(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardIterator I, Sentinel<I> S, class Proj = identity,
    IndirectStrictWeakOrder<projected<I, Proj>> Comp = less<>>
  I is_sorted_until(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardRange Rng, class Proj = identity,
    IndirectStrictWeakOrder<projected<iterator_t<Rng>, Proj>> Comp = less<>>
  safe_iterator_t<Rng>
    is_sorted_until(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessIterator I, Sentinel<I> S, class Comp = less<>,
    class Proj = identity>
  requires Sortable<I, Comp, Proj>
    I nth_element(I first, I nth, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessRange Rng, class Comp = less<>, class Proj = identity>
  requires Sortable<iterator_t<Rng>, Comp, Proj>
  safe_iterator_t<Rng>
    nth_element(Rng&& rng, iterator_t<Rng> nth, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardIterator I, Sentinel<I> S, class T, class Proj = identity,
    IndirectStrictWeakOrder<const T*, projected<I, Proj>> Comp = less<>>
  I
    lower_bound(I first, S last, const T& value, Comp comp = Comp{},
                Proj proj = Proj{});
 
template <ForwardRange Rng, class T, class Proj = identity,
    IndirectStrictWeakOrder<const T*, projected<iterator_t<Rng>, Proj>> Comp = less<>>
  safe_iterator_t<Rng>
    lower_bound(Rng&& rng, const T& value, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardIterator I, Sentinel<I> S, class T, class Proj = identity,
    IndirectStrictWeakOrder<const T*, projected<I, Proj>> Comp = less<>>
  I
    upper_bound(I first, S last, const T& value, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardRange Rng, class T, class Proj = identity,
    IndirectStrictWeakOrder<const T*, projected<iterator_t<Rng>, Proj>> Comp = less<>>
  safe_iterator_t<Rng>
    upper_bound(Rng&& rng, const T& value, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardIterator I, Sentinel<I> S, class T, class Proj = identity,
    IndirectStrictWeakOrder<const T*, projected<I, Proj>> Comp = less<>>
  tagged_pair<tag::begin(I), tag::end(I)>
    equal_range(I first, S last, const T& value, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardRange Rng, class T, class Proj = identity,
    IndirectStrictWeakOrder<const T*, projected<iterator_t<Rng>, Proj>> Comp = less<>>
  tagged_pair<tag::begin(safe_iterator_t<Rng>),
              tag::end(safe_iterator_t<Rng>)>
    equal_range(Rng&& rng, const T& value, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardIterator I, Sentinel<I> S, class T, class Proj = identity,
    IndirectStrictWeakOrder<const T*, projected<I, Proj>> Comp = less<>>
  bool
    binary_search(I first, S last, const T& value, Comp comp = Comp{},
                  Proj proj = Proj{});
 
template <ForwardRange Rng, class T, class Proj = identity,
    IndirectStrictWeakOrder<const T*, projected<iterator_t<Rng>, Proj>> Comp = less<>>
  bool
    binary_search(Rng&& rng, const T& value, Comp comp = Comp{},
                  Proj proj = Proj{});
 
template <InputIterator I1, Sentinel<I1> S1, InputIterator I2, Sentinel<I2> S2,
    WeaklyIncrementable O, class Comp = less<>, class Proj1 = identity,
    class Proj2 = identity>
  requires Mergeable<I1, I2, O, Comp, Proj1, Proj2>
  tagged_tuple<tag::in1(I1), tag::in2(I2), tag::out(O)>
    merge(I1 first1, S1 last1, I2 first2, S2 last2, O result,
          Comp comp = Comp{}, Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputRange Rng1, InputRange Rng2, WeaklyIncrementable O, class Comp = less<>,
    class Proj1 = identity, class Proj2 = identity>
  requires Mergeable<iterator_t<Rng1>, iterator_t<Rng2>, O, Comp, Proj1, Proj2>
  tagged_tuple<tag::in1(safe_iterator_t<Rng1>),
               tag::in2(safe_iterator_t<Rng2>),
               tag::out(O)>
    merge(Rng1&& rng1, Rng2&& rng2, O result,
          Comp comp = Comp{}, Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <BidirectionalIterator I, Sentinel<I> S, class Comp = less<>,
    class Proj = identity>
  requires Sortable<I, Comp, Proj>
  I
    inplace_merge(I first, I middle, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <BidirectionalRange Rng, class Comp = less<>, class Proj = identity>
  requires Sortable<iterator_t<Rng>, Comp, Proj>
  safe_iterator_t<Rng>
    inplace_merge(Rng&& rng, iterator_t<Rng> middle, Comp comp = Comp{},
                  Proj proj = Proj{});
 
template <InputIterator I1, Sentinel<I1> S1, InputIterator I2, Sentinel<I2> S2,
    class Proj1 = identity, class Proj2 = identity,
    IndirectStrictWeakOrder<projected<I1, Proj1>, projected<I2, Proj2>> Comp = less<>>
  bool
    includes(I1 first1, S1 last1, I2 first2, S2 last2, Comp comp = Comp{},
             Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputRange Rng1, InputRange Rng2, class Proj1 = identity,
    class Proj2 = identity,
    IndirectStrictWeakOrder<projected<iterator_t<Rng1>, Proj1>,
      projected<iterator_t<Rng2>, Proj2>> Comp = less<>>
  bool
    includes(Rng1&& rng1, Rng2&& rng2, Comp comp = Comp{},
             Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputIterator I1, Sentinel<I1> S1, InputIterator I2, Sentinel<I2> S2,
    WeaklyIncrementable O, class Comp = less<>,
    class Proj1 = identity, class Proj2 = identity>
  requires Mergeable<I1, I2, O, Comp, Proj1, Proj2>
  tagged_tuple<tag::in1(I1), tag::in2(I2), tag::out(O)>
    set_union(I1 first1, S1 last1, I2 first2, S2 last2, O result, Comp comp = Comp{},
              Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputRange Rng1, InputRange Rng2, WeaklyIncrementable O,
    class Comp = less<>, class Proj1 = identity, class Proj2 = identity>
  requires Mergeable<iterator_t<Rng1>, iterator_t<Rng2>, O, Comp, Proj1, Proj2>
  tagged_tuple<tag::in1(safe_iterator_t<Rng1>),
               tag::in2(safe_iterator_t<Rng2>),
               tag::out(O)>
    set_union(Rng1&& rng1, Rng2&& rng2, O result, Comp comp = Comp{},
              Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputIterator I1, Sentinel<I1> S1, InputIterator I2, Sentinel<I2> S2,
    WeaklyIncrementable O, class Comp = less<>,
    class Proj1 = identity, class Proj2 = identity>
  requires Mergeable<I1, I2, O, Comp, Proj1, Proj2>
  O
    set_intersection(I1 first1, S1 last1, I2 first2, S2 last2, O result,
                     Comp comp = Comp{}, Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputRange Rng1, InputRange Rng2, WeaklyIncrementable O,
    class Comp = less<>, class Proj1 = identity, class Proj2 = identity>
  requires Mergeable<iterator_t<Rng1>, iterator_t<Rng2>, O, Comp, Proj1, Proj2>
  O
    set_intersection(Rng1&& rng1, Rng2&& rng2, O result,
                     Comp comp = Comp{}, Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputIterator I1, Sentinel<I1> S1, InputIterator I2, Sentinel<I2> S2,
    WeaklyIncrementable O, class Comp = less<>,
    class Proj1 = identity, class Proj2 = identity>
  requires Mergeable<I1, I2, O, Comp, Proj1, Proj2>
  tagged_pair<tag::in1(I1), tag::out(O)>
    set_difference(I1 first1, S1 last1, I2 first2, S2 last2, O result,
                   Comp comp = Comp{}, Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputRange Rng1, InputRange Rng2, WeaklyIncrementable O,
    class Comp = less<>, class Proj1 = identity, class Proj2 = identity>
  requires Mergeable<iterator_t<Rng1>, iterator_t<Rng2>, O, Comp, Proj1, Proj2>
  tagged_pair<tag::in1(safe_iterator_t<Rng1>), tag::out(O)>
    set_difference(Rng1&& rng1, Rng2&& rng2, O result,
                   Comp comp = Comp{}, Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputIterator I1, Sentinel<I1> S1, InputIterator I2, Sentinel<I2> S2,
    WeaklyIncrementable O, class Comp = less<>,
    class Proj1 = identity, class Proj2 = identity>
  requires Mergeable<I1, I2, O, Comp, Proj1, Proj2>
  tagged_tuple<tag::in1(I1), tag::in2(I2), tag::out(O)>
    set_symmetric_difference(I1 first1, S1 last1, I2 first2, S2 last2, O result,
                             Comp comp = Comp{}, Proj1 proj1 = Proj1{},
                             Proj2 proj2 = Proj2{});
 
template <InputRange Rng1, InputRange Rng2, WeaklyIncrementable O,
    class Comp = less<>, class Proj1 = identity, class Proj2 = identity>
  requires Mergeable<iterator_t<Rng1>, iterator_t<Rng2>, O, Comp, Proj1, Proj2>
  tagged_tuple<tag::in1(safe_iterator_t<Rng1>),
               tag::in2(safe_iterator_t<Rng2>),
               tag::out(O)>
    set_symmetric_difference(Rng1&& rng1, Rng2&& rng2, O result, Comp comp = Comp{},
                             Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <RandomAccessIterator I, Sentinel<I> S, class Comp = less<>,
    class Proj = identity>
  requires Sortable<I, Comp, Proj>
  I push_heap(I first, S last, Comp comp = Comp{}, Proj proj == Proj{});
 
template <RandomAccessRange Rng, class Comp = less<>, class Proj = identity>
  requires Sortable<iterator_t<Rng>, Comp, Proj>
  safe_iterator_t<Rng>
    push_heap(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessIterator I, Sentinel<I> S, class Comp = less<>,
    class Proj = identity>
  requires Sortable<I, Comp, Proj>
  I pop_heap(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessRange Rng, class Comp = less<>, class Proj = identity>
  requires Sortable<iterator_t<Rng>, Comp, Proj>
  safe_iterator_t<Rng>
    pop_heap(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessIterator I, Sentinel<I> S, class Comp = less<>,
    class Proj = identity>
  requires Sortable<I, Comp, Proj>
  I make_heap(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessRange Rng, class Comp = less<>, class Proj = identity>
  requires Sortable<iterator_t<Rng>, Comp, Proj>
  safe_iterator_t<Rng>
    make_heap(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessIterator I, Sentinel<I> S, class Comp = less<>,
    class Proj = identity>
  requires Sortable<I, Comp, Proj>
  I sort_heap(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessRange Rng, class Comp = less<>, class Proj = identity>
  requires Sortable<iterator_t<Rng>, Comp, Proj>
  safe_iterator_t<Rng>
    sort_heap(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessIterator I, Sentinel<I> S, class Proj = identity,
    IndirectStrictWeakOrder<projected<I, Proj>> Comp = less<>>
  bool is_heap(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessRange Rng, class Proj = identity,
    IndirectStrictWeakOrder<projected<iterator_t<Rng>, Proj>> Comp = less<>>
  bool
    is_heap(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessIterator I, Sentinel<I> S, class Proj = identity,
    IndirectStrictWeakOrder<projected<I, Proj>> Comp = less<>>
  I is_heap_until(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <RandomAccessRange Rng, class Proj = identity,
    IndirectStrictWeakOrder<projected<iterator_t<Rng>, Proj>> Comp = less<>>
  safe_iterator_t<Rng>
    is_heap_until(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <class T, class Proj = identity,
    IndirectStrictWeakOrder<projected<const T*, Proj>> Comp = less<>>
  constexpr const T& min(const T& a, const T& b, Comp comp = Comp{}, Proj proj = Proj{});
 
template <Copyable T, class Proj = identity,
    IndirectStrictWeakOrder<projected<const T*, Proj>> Comp = less<>>
  constexpr T min(initializer_list<T> t, Comp comp = Comp{}, Proj proj = Proj{});
 
template <InputRange Rng, class Proj = identity,
    IndirectStrictWeakOrder<projected<iterator_t<Rng>, Proj>> Comp = less<>>
  requires Copyable<value_type_t<iterator_t<Rng>>>
  value_type_t<iterator_t<Rng>>
    min(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <class T, class Proj = identity,
    IndirectStrictWeakOrder<projected<const T*, Proj>> Comp = less<>>
  constexpr const T& max(const T& a, const T& b, Comp comp = Comp{}, Proj proj = Proj{});
 
template <Copyable T, class Proj = identity,
    IndirectStrictWeakOrder<projected<const T*, Proj>> Comp = less<>>
  constexpr T max(initializer_list<T> t, Comp comp = Comp{}, Proj proj = Proj{});
 
template <InputRange Rng, class Proj = identity,
    IndirectStrictWeakOrder<projected<iterator_t<Rng>, Proj>> Comp = less<>>
  requires Copyable<value_type_t<iterator_t<Rng>>>
  value_type_t<iterator_t<Rng>>
    max(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <class T, class Proj = identity,
    IndirectStrictWeakOrder<projected<const T*, Proj>> Comp = less<>>
  constexpr tagged_pair<tag::min(const T&), tag::max(const T&)>
    minmax(const T& a, const T& b, Comp comp = Comp{}, Proj proj = Proj{});
 
template <Copyable T, class Proj = identity,
    IndirectStrictWeakOrder<projected<const T*, Proj>> Comp = less<>>
  constexpr tagged_pair<tag::min(T), tag::max(T)>
    minmax(initializer_list<T> t, Comp comp = Comp{}, Proj proj = Proj{});
 
template <InputRange Rng, class Proj = identity,
    IndirectStrictWeakOrder<projected<iterator_t<Rng>, Proj>> Comp = less<>>
  requires Copyable<value_type_t<iterator_t<Rng>>>
  tagged_pair<tag::min(value_type_t<iterator_t<Rng>>),
              tag::max(value_type_t<iterator_t<Rng>>)>
    minmax(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardIterator I, Sentinel<I> S, class Proj = identity,
    IndirectStrictWeakOrder<projected<I, Proj>> Comp = less<>>
  I min_element(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardRange Rng, class Proj = identity,
    IndirectStrictWeakOrder<projected<iterator_t<Rng>, Proj>> Comp = less<>>
  safe_iterator_t<Rng>
    min_element(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardIterator I, Sentinel<I> S, class Proj = identity,
    IndirectStrictWeakOrder<projected<I, Proj>> Comp = less<>>
  I max_element(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardRange Rng, class Proj = identity,
    IndirectStrictWeakOrder<projected<iterator_t<Rng>, Proj>> Comp = less<>>
  safe_iterator_t<Rng>
    max_element(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardIterator I, Sentinel<I> S, class Proj = identity,
    IndirectStrictWeakOrder<projected<I, Proj>> Comp = less<>>
  tagged_pair<tag::min(I), tag::max(I)>
    minmax_element(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <ForwardRange Rng, class Proj = identity,
    IndirectStrictWeakOrder<projected<iterator_t<Rng>, Proj>> Comp = less<>>
  tagged_pair<tag::min(safe_iterator_t<Rng>),
              tag::max(safe_iterator_t<Rng>)>
    minmax_element(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <InputIterator I1, Sentinel<I1> S1, InputIterator I2, Sentinel<I2> S2,
    class Proj1 = identity, class Proj2 = identity,
    IndirectStrictWeakOrder<projected<I1, Proj1>, projected<I2, Proj2>> Comp = less<>>
  bool
    lexicographical_compare(I1 first1, S1 last1, I2 first2, S2 last2,
                            Comp comp = Comp{},
                            Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <InputRange Rng1, InputRange Rng2, class Proj1 = identity,
    class Proj2 = identity,
    IndirectStrictWeakOrder<projected<iterator_t<Rng1>, Proj1>,
      projected<iterator_t<Rng2>, Proj2>> Comp = less<>>
  bool
    lexicographical_compare(Rng1&& rng1, Rng2&& rng2, Comp comp = Comp{},
                            Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{});
 
template <BidirectionalIterator I, Sentinel<I> S, class Comp = less<>,
    class Proj = identity>
  requires Sortable<I, Comp, Proj>
  bool next_permutation(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <BidirectionalRange Rng, class Comp = less<>,
    class Proj = identity>
  requires Sortable<iterator_t<Rng>, Comp, Proj>
  bool
    next_permutation(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
template <BidirectionalIterator I, Sentinel<I> S, class Comp = less<>,
    class Proj = identity>
  requires Sortable<I, Comp, Proj>
  bool prev_permutation(I first, S last, Comp comp = Comp{}, Proj proj = Proj{});
 
template <BidirectionalRange Rng, class Comp = less<>,
    class Proj = identity>
  requires Sortable<iterator_t<Rng>, Comp, Proj>
  bool
    prev_permutation(Rng&& rng, Comp comp = Comp{}, Proj proj = Proj{});
 
}}}}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/experimental/ranges/algorithm&oldid=112229>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 August 2019, at 03:31.