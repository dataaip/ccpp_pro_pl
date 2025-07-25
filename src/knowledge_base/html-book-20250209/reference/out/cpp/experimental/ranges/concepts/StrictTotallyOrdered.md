# std::experimental::ranges::StrictTotallyOrdered, std::experimental::ranges::StrictTotallyOrderedWith

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

Concepts library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Core language concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Same | | | | | | DerivedFrom | | | | | | ConvertibleTo | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | CommonReference | | | | | | Common | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Integral | | | | | | SignedIntegral | | | | | | UnsignedIntegral | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignable | | | | | | SwappableSwappableWith | | | | | |
| Object concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Destructible | | | | | | Constructible | | | | | | DefaultConstructible | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MoveConstructible | | | | | | CopyConstructible | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Movable | | | | | | Copyable | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Semiregular | | | | | | Regular | | | | | |  | | | | | |
| Comparison concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Boolean | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | WeaklyEqualityComparableWith | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | EqualityComparableEqualityComparableWith | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****StrictTotallyOrderedStrictTotallyOrderedWith**** | | | | | |
| Callable concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | InvocableRegularInvocable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Predicate | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Relation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | StrictWeakOrder | | | | | |  | | | | | |
| URNG concept | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | UniformRandomNumberGenerator | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/ranges/concepts>` |  |  |
| template< class T >  concept bool StrictTotallyOrdered =      EqualityComparable<T> &&      requires(const std::remove_reference_t<T>& a,               const std::remove_reference_t<T>& b) {          { a < b }  -> Boolean&&;          { a > b }  -> Boolean&&;          { a <= b } -> Boolean&&;          { a >= b } -> Boolean&&; }; | (1) | (ranges TS) |
| template< class T, class U >  concept bool StrictTotallyOrderedWith =      StrictTotallyOrdered<T> &&      StrictTotallyOrdered<U> &&      CommonReference<          const std::remove_reference_t<T>&,          const std::remove_reference_t<U>&> &&      StrictTotallyOrdered<          ranges::common_reference_t<              const std::remove_reference_t<T>&,              const std::remove_reference_t<U>&>> &&      EqualityComparableWith<T, U> &&      requires(const std::remove_reference_t<T>& t,               const std::remove_reference_t<U>& u) {          { t < u }  -> Boolean&&;          { t > u }  -> Boolean&&;          { t <= u } -> Boolean&&;          { t >= u } -> Boolean&&;          { u < t }  -> Boolean&&;          { u > t }  -> Boolean&&;          { u <= t } -> Boolean&&;          { u >= t } -> Boolean&&; }; | (2) | (ranges TS) |
|  |  |  |

1) The concept `StrictTotallyOrdered<T>` specifies that the comparison operators `==,!=,<,>,<=,>=` on `T` yield results consistent with a strict total order on `T`.

`StrictTotallyOrdered<T>` is satisfied only if, given lvalues `a`, `b` and `c` of type const std::remove_reference_t<T>:

- Exactly one of bool(a < b), bool(a > b) and bool(a == b) is true;
- If bool(a < b) and bool(b < c) are both true, then bool(a < c) is true;
- bool(a > b) == bool(b < a)
- bool(a >= b) == !bool(a < b)
- bool(a <= b) == !bool(b < a)
2) The concept `StrictTotallyOrderedWith<T, U>` specifies that the comparison operators `==,!=,<,>,<=,>=` on (possibly mixed) `T` and `U` operands yield results consistent with a strict total order. Comparing mixed operands yields results equivalent to comparing the operands converted to their common type.

Formally, `StrictTotallyOrderedWith<T, U>` is satisfied only if, given any lvalue `t` of type const std::remove_reference_t<T> and any lvalue `u` of type const std::remove_reference_t<U>, and let `C` be ranges::common_reference_t<const std::remove_reference_t<T>&, const std::remove_reference_t<U>&>:

- bool(t < u) == bool(C(t) < C(u))
- bool(t > u) == bool(C(t) > C(u))
- bool(t <= u) == bool(C(t) <= C(u))
- bool(t >= u) == bool(C(t) >= C(u))
- bool(u < t) == bool(C(u) < C(t))
- bool(u > t) == bool(C(u) > C(t))
- bool(u <= t) == bool(C(u) <= C(t))
- bool(u >= t) == bool(C(u) >= C(t))

### Equality preservation

An expression is **equality preserving** if it results in equal outputs given equal inputs.

- The inputs to an expression consist of its operands.
- The outputs of an expression consist of its result and all operands modified by the expression (if any).

Every expression required to be equality preserving is further required to be **stable**: two evaluations of such an expression with the same input objects must have equal outputs absent any explicit intervening modification of those input objects.

Unless noted otherwise, every expression used in a **requires-expression** is required to be equality preserving and stable, and the evaluation of the expression may only modify its non-constant operands. Operands that are constant must not be modified.

### Implicit expression variations

A **requires-expression** that uses an expression that is non-modifying for some constant lvalue operand also implicitly requires additional variations of that expression that accept a non-constant lvalue or (possibly constant) rvalue for the given operand unless such an expression variation is explicitly required with differing semantics. These **implicit expression variations** must meet the same semantic requirements of the declared expression. The extent to which an implementation validates the syntax of the variations is unspecified.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/concepts/StrictTotallyOrdered&oldid=155316>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 July 2023, at 09:38.