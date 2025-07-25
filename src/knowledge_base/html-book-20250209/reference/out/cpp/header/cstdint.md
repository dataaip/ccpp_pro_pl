# Standard library header <cstdint> (C++11)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | ****<cstdint>**** (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header was originally in the C standard library as <stdint.h>.

This header is part of the type support library, providing fixed width integer types and part of C numeric limits interface.

|  |  |
| --- | --- |
| Types | |
| int8_tint16_tint32_tint64_t(optional) | signed integer type with width of exactly 8, 16, 32 and 64 bits respectively with no padding bits and using 2's complement for negative values (provided if and only if the implementation directly supports the type)   (typedef) |
| int_fast8_tint_fast16_tint_fast32_tint_fast64_t | fastest signed integer type with width of at least 8, 16, 32 and 64 bits respectively   (typedef) |
| int_least8_tint_least16_tint_least32_tint_least64_t | smallest signed integer type with width of at least 8, 16, 32 and 64 bits respectively   (typedef) |
| intmax_t | maximum-width signed integer type   (typedef) |
| intptr_t(optional) | signed integer type capable of holding a pointer to void   (typedef) |
| uint8_tuint16_tuint32_tuint64_t(optional) | unsigned integer type with width of exactly 8, 16, 32 and 64 bits respectively  (provided if and only if the implementation directly supports the type)   (typedef) |
| uint_fast8_tuint_fast16_tuint_fast32_tuint_fast64_t | fastest unsigned integer type with width of at least 8, 16, 32 and 64 bits respectively   (typedef) |
| uint_least8_tuint_least16_tuint_least32_tuint_least64_t | smallest unsigned integer type with width of at least 8, 16, 32 and 64 bits respectively   (typedef) |
| uintmax_t | maximum-width unsigned integer type   (typedef) |
| uintptr_t(optional) | unsigned integer type capable of holding a pointer to void   (typedef) |
| Macros | |
| Signed integers : minimum value | |
| INT8_MININT16_MININT32_MININT64_MIN(optional) | minimum value of `std::int8_t`, `std::int16_t`, `std::int32_t` and `std::int64_t` respectively   (macro constant) |
| INT_FAST8_MININT_FAST16_MININT_FAST32_MININT_FAST64_MIN | minimum value of `std::int_fast8_t`, `std::int_fast16_t`, `std::int_fast32_t` and `std::int_fast64_t` respectively   (macro constant) |
| INT_LEAST8_MININT_LEAST16_MININT_LEAST32_MININT_LEAST64_MIN | minimum value of `std::int_least8_t`, `std::int_least16_t`, `std::int_least32_t` and `std::int_least64_t` respectively   (macro constant) |
| INTPTR_MIN(optional) | minimum value of `std::intptr_t`   (macro constant) |
| INTMAX_MIN | minimum value of `std::intmax_t`   (macro constant) |
| Signed integers : maximum value | |
| INT8_MAXINT16_MAXINT32_MAXINT64_MAX(optional) | maximum value of `std::int8_t`, `std::int16_t`, `std::int32_t` and `std::int64_t` respectively   (macro constant) |
| INT_FAST8_MAXINT_FAST16_MAXINT_FAST32_MAXINT_FAST64_MAX | maximum value of `std::int_fast8_t`, `std::int_fast16_t`, `std::int_fast32_t` and `std::int_fast64_t` respectively   (macro constant) |
| INT_LEAST8_MAXINT_LEAST16_MAXINT_LEAST32_MAXINT_LEAST64_MAX | maximum value of `std::int_least8_t`, `std::int_least16_t`, `std::int_least32_t` and `std::int_least64_t` respectively   (macro constant) |
| INTPTR_MAX(optional) | maximum value of `std::intptr_t`   (macro constant) |
| INTMAX_MAX | maximum value of `std::intmax_t`   (macro constant) |
| Unsigned integers : maximum value | |
| UINT8_MAXUINT16_MAXUINT32_MAXUINT64_MAX(optional) | maximum value of `std::uint8_t`, `std::uint16_t`, `std::uint32_t` and `std::uint64_t` respectively   (macro constant) |
| UINT_FAST8_MAXUINT_FAST16_MAXUINT_FAST32_MAXUINT_FAST64_MAX | maximum value of `std::uint_fast8_t`, `std::uint_fast16_t`, `std::uint_fast32_t` and `std::uint_fast64_t` respectively   (macro constant) |
| UINT_LEAST8_MAXUINT_LEAST16_MAXUINT_LEAST32_MAXUINT_LEAST64_MAX | maximum value of `std::uint_least8_t`, `std::uint_least16_t`, `std::uint_least32_t` and `std::uint_least64_t` respectively   (macro constant) |
| UINTPTR_MAX(optional) | maximum value of `std::uintptr_t`   (macro constant) |
| UINTMAX_MAX | maximum value of `std::uintmax_t`   (macro constant) |
| Limits of other integer types | |
| PTRDIFF_MIN(C++11) | minimum value of std::ptrdiff_t   (macro constant) |
| PTRDIFF_MAX(C++11) | maximum value of std::ptrdiff_t   (macro constant) |
| SIZE_MAX(C++11) | maximum value of std::size_t   (macro constant) |
| SIG_ATOMIC_MIN(C++11) | minimum value of std::sig_atomic_t   (macro constant) |
| SIG_ATOMIC_MAX(C++11) | maximum value of std::sig_atomic_t   (macro constant) |
| WCHAR_MIN(C++11) | minimum value of wchar_t   (macro constant) |
| WCHAR_MAX(C++11) | maximum value of wchar_t   (macro constant) |
| WINT_MIN(C++11) | minimum value of `std::wint_t`   (macro constant) |
| WINT_MAX(C++11) | maximum value of `std::wint_t`   (macro constant) |
| Function macros for integer constants | |
| INT8_CINT16_CINT32_CINT64_C | expands to an integer constant expression having the value specified by its argument and whose type is the promoted type of `std::int_least8_t`, `std::int_least16_t`, `std::int_least32_t` and `std::int_least64_t` respectively   (function macro) |
| INTMAX_C | expands to an integer constant expression having the value specified by its argument and the type `std::intmax_t`   (function macro) |
| UINT8_CUINT16_CUINT32_CUINT64_C | expands to an integer constant expression having the value specified by its argument and whose type is the promoted type of `std::uint_least8_t`, `std::uint_least16_t`, `std::uint_least32_t` and `std::uint_least64_t` respectively   (function macro) |
| UINTMAX_C | expands to an integer constant expression having the value specified by its argument and the type `std::uintmax_t`   (function macro) |

### Synopsis

```
namespace std {
  using int8_t         = /* signed integer type */;   // optional
  using int16_t        = /* signed integer type */;   // optional
  using int32_t        = /* signed integer type */;   // optional
  using int64_t        = /* signed integer type */;   // optional
  using intN_t         = /* see description */;       // optional, see description
 
  using int_fast8_t    = /* signed integer type */;
  using int_fast16_t   = /* signed integer type */;
  using int_fast32_t   = /* signed integer type */;
  using int_fast64_t   = /* signed integer type */;
  using int_fastN_t    = /* see description */;       // optional, see description
 
  using int_least8_t   = /* signed integer type */;
  using int_least16_t  = /* signed integer type */;
  using int_least32_t  = /* signed integer type */;
  using int_least64_t  = /* signed integer type */;
  using int_leastN_t   = /* see description */;       // optional, see description
 
  using intmax_t       = /* signed integer type */;
  using intptr_t       = /* signed integer type */;   // optional
 
  using uint8_t        = /* unsigned integer type */; // optional
  using uint16_t       = /* unsigned integer type */; // optional
  using uint32_t       = /* unsigned integer type */; // optional
  using uint64_t       = /* unsigned integer type */; // optional
  using uintN_t        = /* see description */;       // optional, see description
 
  using uint_fast8_t   = /* unsigned integer type */;
  using uint_fast16_t  = /* unsigned integer type */;
  using uint_fast32_t  = /* unsigned integer type */;
  using uint_fast64_t  = /* unsigned integer type */;
  using uint_fastN_t   = /* see description */;       // optional, see description
 
  using uint_least8_t  = /* unsigned integer type */;
  using uint_least16_t = /* unsigned integer type */;
  using uint_least32_t = /* unsigned integer type */;
  using uint_least64_t = /* unsigned integer type */;
  using uint_leastN_t  = /* see description */;       // optional, see description
 
  using uintmax_t      = /* unsigned integer type */;
  using uintptr_t      = /* unsigned integer type */; // optional
}
 
#define INTN_MIN         /* see description */
#define INTN_MAX         /* see description */
#define UINTN_MAX        /* see description */
 
#define INT_FASTN_MIN    /* see description */
#define INT_FASTN_MAX    /* see description */
#define UINT_FASTN_MAX   /* see description */
 
#define INT_LEASTN_MIN   /* see description */
#define INT_LEASTN_MAX   /* see description */
#define UINT_LEASTN_MAX  /* see description */
 
#define INTMAX_MIN       /* see description */
#define INTMAX_MAX       /* see description */
#define UINTMAX_MAX      /* see description */
 
#define INTPTR_MIN       /* see description */        // optional
#define INTPTR_MAX       /* see description */        // optional
#define UINTPTR_MAX      /* see description */        // optional
 
#define PTRDIFF_MIN      /* see description */
#define PTRDIFF_MAX      /* see description */
#define SIZE_MAX         /* see description */
 
#define SIG_ATOMIC_MIN   /* see description */
#define SIG_ATOMIC_MAX   /* see description */
 
#define WCHAR_MIN        /* see description */
#define WCHAR_MAX        /* see description */
 
#define WINT_MIN         /* see description */
#define WINT_MAX         /* see description */
 
#define INTN_C(value)    /* see description */
#define UINTN_C(value)   /* see description */
#define INTMAX_C(value)  /* see description */
#define UINTMAX_C(value) /* see description */

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/cstdint&oldid=143432>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 September 2022, at 10:33.