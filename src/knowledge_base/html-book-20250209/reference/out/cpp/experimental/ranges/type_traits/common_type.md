# std::experimental::ranges::common_type

From cppreference.com
< cpp‎ | experimental‎ | ranges
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

Ranges

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Concepts | | | | |
| General utilities | | | | |
| Iterators | | | | |
| Ranges | | | | |
| Algorithms | | | | |

General utilities library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Utility components | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | exchange | | | | | |
| Function objects | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | invoke | | | | | | identity | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_to | | | | | | not_equal_to | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | greater | | | | | | less | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | greater_equal | | | | | | less_equal | | | | | |
| Metaprogramming and type traits | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_swappable_withis_swappable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_nothrow_swappable_withis_nothrow_swappable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_reference | | | | | | ****common_type**** | | | | | |
| Tagged pairs and tuples | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | TagSpecifier | | | | | | TaggedType | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged | | | | | | tag specifiers | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged_pair | | | | | | make_tagged_pair | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged_tuple | | | | | | make_tagged_tuple | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/ranges/type_traits>` |  |  |
| template< class... T >  struct common_type; |  | (ranges TS) |
|  |  |  |

Determines the common type among all types `T...`, that is the type all `T...` can be implicitly converted to. If such a type exists (as determined according to the rules below), the member `type` names that type. Otherwise, there is no member `type`. The behavior is undefined if any of the types in `T...` is an incomplete type other than (possibly cv-qualified) void.

- If sizeof...(T) is zero, there is no member `type`.
- If sizeof...(T) is one (i.e., `T...` contains only one type `T0`), the member `type` names the same type as std::decay_t<T0>.
- If sizeof...(T) is two (i.e., `T...` contains exactly two types `T1` and `T2`),

:   - If applying std::decay to at least one of `T1` and `T2` produces a different type, the member `type` names the same type as ranges::common_type_t<std::decay_t<T1>, std::decay_t<T2>>, if it exists; if not, there is no member `type`;
    - Otherwise, (and unless there is a user specialization for ranges::common_type<T1, T2>), if std::common_type_t<T1, T2> is well-formed, then the member `type` denotes that type;
    - Otherwise, the member `type` denotes the type std::decay_t<decltype(false ? std::declval<const T1&>() : std::declval<const T2&>())>, if that conditional expression is well-formed; if not, there is no member `type`.

- If sizeof...(T) is greater than two (i.e., `T...` consists of the types `T1, T2, R...`), then if ranges::common_type_t<T1, T2> exists, the member `type` denotes ranges::common_type_t<ranges::common_type_t<T1, T2>, R...> if such a type exists. In all other cases, there is no member `type`.

### Member types

|  |  |
| --- | --- |
| Name | Definition |
| `type` | the common type for all `T...` |

### Helper types

|  |  |  |
| --- | --- | --- |
| template< class... T >  using common_type_t = typename common_type<T...>::type; |  |  |
|  |  |  |

### Specializations

Users may specialize `common_type` for types `T1` and `T2` if

- At least one of `T1` and `T2` depends on a user-defined type, and
- std::decay is an identity transformation for both `T1` and `T2`.

If such a specialization has a member named `type`, it must be a public and unambiguous member type that names a cv-unqualified non-reference type to which both `T1` and `T2` are explicitly convertible. Additionally, ranges::common_type_t<T1, T2> and ranges::common_type_t<T2, T1> must denote the same type.

A program that adds `common_type` specializations in violation of these rules has undefined behavior.

### Notes

For arithmetic types not subject to promotion, the common type may be viewed as the type of the (possibly mixed-mode) arithmetic expression such as T0() + T1() + ... + Tn().

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| common_type(C++11) | determines the common type of a group of types   (class template) |
| common_reference | determine the common reference type of a set of types   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/type_traits/common_type&oldid=159306>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 September 2023, at 01:50.