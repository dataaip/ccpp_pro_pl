# std::experimental::ranges::common_reference

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_swappable_withis_swappable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_nothrow_swappable_withis_nothrow_swappable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****common_reference**** | | | | | | common_type | | | | | |
| Tagged pairs and tuples | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | TagSpecifier | | | | | | TaggedType | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged | | | | | | tag specifiers | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged_pair | | | | | | make_tagged_pair | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged_tuple | | | | | | make_tagged_tuple | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/ranges/type_traits>` |  |  |
| template< class... T >  struct common_reference; |  | (ranges TS) |
|  |  |  |

Determines the common reference type of the types `T...`, that is, the type to which all the types in `T...` can be converted or bound. If such a type exists (as determined according to the rules below), the member `type` names that type. Otherwise, there is no member `type`. The behavior is undefined if any of the types in `T...` is an incomplete type other than (possibly cv-qualified) void.

When given reference types, `common_reference` attempts to find a reference type to which the supplied reference types can all be bound, but may return a non-reference type if it cannot find such a reference type.

- If sizeof...(T) is zero, there is no member `type`.
- If sizeof...(T) is one (i.e., `T...` contains only one type `T0`), the member `type` names the same type as T0.
- If sizeof...(T) is two (i.e., `T...` contains two types `T1` and `T2`):
  - If `T1` and `T2` are both reference types, and the **simple common reference type** `S` of `T1` and `T2` (as defined below) exists, then the member type `type` names `S`;
  - Otherwise, if basic_common_reference<T1R, T2R, T1Q, T2Q>::type exists, where `TiR` is std::remove_cv_t<std::remove_reference_t<Ti>> and `TiQ` is an alias template such that TiQ<TiR> is Ti, then the member type `type` names that type;
  - Otherwise, if decltype(false? val<T1>() : val<T2>()), where `val` is a function template template<class T> T val();, denotes a valid type, then the member type `type` names that type;
  - Otherwise, if ranges::common_type_t<T1, T2> is a valid type, then the member type `type` names that type;
  - Otherwise, there is no member type.
- If sizeof...(T) is greater than two (i.e., `T...` consists of the types `T1, T2, R...`), then if ranges::common_reference_t<T1, T2> exists, the member `type` denotes ranges::common_reference_t<ranges::common_reference_t<T1, T2>, R...> if such a type exists. In all other cases, there is no member `type`.

The **simple common reference type** of two reference types `T1` and `T2` is defined as follows:

- If `T1` is `cv1 X &` and `T2` is `cv2 Y &` (i.e., both are lvalue reference types): their simple common reference type is decltype(false? std::declval<cv12 X &>() : std::declval<cv12 Y &>()), where **cv12** is the union of **cv1** and **cv2**, if that type exists and is a reference type.
- If `T1` and `T2` are both rvalue reference types: if the simple common reference type of `T1 &` and `T2 &` (determined according to the previous bullet) exists, then let `C` denote that type's corresponding rvalue reference type. If std::is_convertible<T1, C>::value and std::is_convertible<T2, C>::value are both `true`, then the simple common reference type of `T1` and `T2` is `C`.
- Otherwise, one of the two types must be an lvalue reference type `A &` and the other must be an rvalue reference type `B &&` (`A` and `B` might be cv-qualified). Let `D` denote the simple common reference type of A & and B const &, if any. If D exists and std::is_convertible<B &&, D>::value is `true`, then the simple common reference type is `D`.
- Otherwise, there's no simple common reference type.

### Member types

|  |  |
| --- | --- |
| Name | Definition |
| `type` | the common reference type for all `T...` |

### Helper types

|  |  |  |
| --- | --- | --- |
| template< class... T >  using common_reference_t = typename common_reference<T...>::type; |  |  |
| template< class T, class U, template<class> class TQual, template<class> class UQual >  struct basic_common_reference {}; |  |  |
|  |  |  |

The class template `basic_common_reference` is a customization point that allows users to influence the result of `common_reference` for user-defined types (typically proxy references). The primary template is empty.

### Specializations

A program may specialize `basic_common_reference<T, U, TQual, UQual>` on the first two parameters `T` and `U` if std::is_same<T, std::decay_t<T>> and std::is_same<U, std::decay_t<U>> are both true and at least one of them depends on a program-defined type.

If such a specialization has a member named `type`, it must be a public and unambiguous member type that names a type to which both TQual<T> and UQual<U> are convertible. Additionally, ranges::basic_common_reference<T, U, TQual, UQual>::type and ranges::basic_common_reference<U, T, UQual, TQual>::type must denote the same type.

A program may not specialize `basic_common_reference` on the third or fourth parameters, nor may it specialize `common_reference` itself. A program that adds specializations in violation of these rules has undefined behavior.

### Notes

|  |  |
| --- | --- |
|  | This section is incomplete |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| common_type(C++11) | determines the common type of a group of types   (class template) |
| common_type | determine the common type of a set of types   (class template) |
| CommonReference | specifies that two types share a common reference type   (concept) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/type_traits/common_reference&oldid=159307>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 September 2023, at 01:51.