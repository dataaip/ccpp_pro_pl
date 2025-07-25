# std::experimental::optional<T>::operator=

From cppreference.com
< cpp‎ | experimental‎ | optional
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

Library fundamentals

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::optional | | | | |
| experimental::any | | | | |
| experimental::basic_string_view | | | | |
| experimental::sample | | | | |
| experimental::shared_ptr | | | | |
| experimental::weak_ptr | | | | |
| experimental::apply | | | | |
| experimental::invocation_typeexperimental::raw_invocation_type | | | | |
| experimental::search | | | | |
| experimental::default_searcherexperimental::make_default_searcher | | | | |
| experimental::boyer_moore_searcherexperimental::make_boyer_moore_searcher | | | | |
| experimental::boyer_moore_horspool_searcherexperimental::make_boyer_moore_horspool_searcher | | | | |
| Type-erased and polymorphic allocators | | | | |
| Variable templates for type traits | | | | |

std::experimental::optional

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| optional::optional | | | | |
| optional::~optional | | | | |
| ****optional::operator=**** | | | | |
| Observers | | | | |
| optional::operator->optional::operator\* | | | | |
| optional::operator bool | | | | |
| optional::value | | | | |
| optional::value_or | | | | |
| Modifiers | | | | |
| optional::emplace | | | | |
| optional::swap | | | | |
| Non-member functions | | | | |
| operator==operator!=operator<operator<=operator>operator>= | | | | |
| make_optional | | | | |
| swap | | | | |
| Helper classes | | | | |
| hash | | | | |
| nullopt_t | | | | |
| in_place_t | | | | |
| bad_optional_access | | | | |
| Helper objects | | | | |
| nullopt | | | | |
| in_place | | | | |

|  |  |  |
| --- | --- | --- |
| optional& operator=( std::experimental::nullopt_t ) noexcept; | (1) | (library fundamentals TS) |
| optional& operator=( const optional& other ); | (2) | (library fundamentals TS) |
| optional& operator=( optional&& other ) noexcept(/\* see below \*/); | (3) | (library fundamentals TS) |
| template< class U >   optional& operator=( U&& value ); | (4) | (library fundamentals TS) |
|  |  |  |

Replaces contents of \*this with the contents of other.

1) If \*this contains a value before the call, the contained value is destroyed by calling its destructor as if by val->T::~T(). \*this does not contain a value after this call.2,3) Assigns the state of other.  

- If both \*this and other do not contain a value, the function has no effect.
- If \*this contains a value, but other does not, then the contained value is destroyed by calling its destructor. \*this does not contain a value after the call.
- If other contains a value, then depending on whether \*this contains a value, the contained value is either direct-initialized or assigned from \*other (2) or std::move(\*other) (3). Note that a moved-from optional still **contains a value**.
4) Decay-only perfect-forwarded assignment: depending on whether \*this contains a value before the call, the contained value is either direct-initialized from std::forward<U>(value) or assigned from std::forward<U>(value). The function does not participate in overload resolution unless std::is_same<std::decay_t<U>, T>::value is true.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another `optional` object whose contained value to assign |
| value | - | value to assign to the contained value |
| Type requirements | | |
| -`T` must meet the requirements of CopyAssignable and CopyConstructible in order to use overload (2). | | |
| -`T` must meet the requirements of MoveAssignable and MoveConstructible in order to use overload (3). | | |

### Return value

\*this

### Exceptions

2-4) Throws any exception thrown by the constructor or assignment operator of `T`. If an exception is thrown, the initialization state of \*this (and of other in case of (2)) is unchanged, i.e. if the object contained a value, it still contains a value, and the other way round. The contents of value and the contained values of \*this and other depend on the exception safety guarantees of the operation from which the exception originates (copy-constructor, move-assignment, etc.).  
(3) has the following `noexcept` declaration:noexcept specification:noexcept(std::is_nothrow_move_assignable<T>::value && std::is_nothrow_move_constructible<T>::value)

### Notes

An optional object `op` may be turned into an empty optional with both op = {}; and op = nullopt;.

### Example

Run this code

```
#include <experimental/optional>
#include <iostream>
 
int main()
{
    std::experimental::optional<const char*> s1 = "abc", s2; // constructor
    s2 = s1; // assignment
    s1 = "def"; // decaying assignment (U = char[4], T = const char*)
    std::cout << *s2 << ' ' << *s1 << '\n';
}

```

Output:

```
abc def

```

### See also

|  |  |
| --- | --- |
| emplace | constructs the contained value in-place   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/optional/operator%3D&oldid=157744>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 September 2023, at 23:01.