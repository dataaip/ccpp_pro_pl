# std::experimental::ranges::Incrementable

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

Iterators library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Iterator concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Readable | | | | | | Writable | | | | | | WeaklyIncrementable | | | | | | ****Incrementable**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator | | | | | | Sentinel | | | | | | SizedSentinel | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | InputIterator | | | | | | ForwardIterator | | | | | | BidirectionalIterator | | | | | | RandomAccessIterator | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | OutputIterator | | | | | |  | | | | | |  | | | | | |  | | | | | |
| Indirect callable concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectUnaryInvocableIndirectRegularUnaryInvocable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectUnaryPredicate | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectRelation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectStrictWeakOrder | | | | | |  | | | | | |
| Common algorithm requirements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectlyMovable | | | | | | IndirectlyMovableStorable | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectlyCopyable | | | | | | IndirectlyCopyableStorable | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectlySwappable | | | | | | IndirectlyComparable | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Permutable | | | | | | Mergeable | | | | | | Sortable | | | | | |
| Concept utilities | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_result_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | projected | | | | | |
| Iterator utilities and operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iter_move") | | | | | | iter_swap") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | advance | | | | | | distance | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next | | | | | | prev | | | | | |
| Iterator traits | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | difference_type | | | | | | value_type | | | | | | reference_trvalue_reference_titer_common_reference_t | | | | | | iterator_category | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | input_iterator_tagoutput_iterator_tagforward_iterator_tagbidirectional_iterator_tagrandom_access_iterator_tag | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ranges::iterator_traits") | | | | | | std::iterator_traits<InputIterator>std::iterator_traits<OutputIterator>") | | | | | |  | | | | | |  | | | | | |  | | | | | |
| Iterator adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_iterator") | | | | | | move_iterator") | | | | | | move_sentinel") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | back_insert_iterator") | | | | | | front_insert_iterator") | | | | | | insert_iterator") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_iterator") | | | | | | counted_iterator") | | | | | | default_sentinel") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | danglingborrowed_iterator_t | | | | | | unreachable") | | | | | |
| Stream iterators | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | istream_iterator") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ostream_iterator") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istreambuf_iterator") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ostreambuf_iterator") | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/ranges/iterator>` |  |  |
| template< class I >  concept bool Incrementable =      Regular<I> &&      WeaklyIncrementable<I> &&      requires(I i) {          { i++ } -> Same<I>&&; }; |  | (ranges TS) |
|  |  |  |

The concept `Incrementable<I>` specifies the requirements on a type that can be incremented (with the pre- and post-increment operators). The increment operations (including those required by `WeaklyIncrementable`) are required to be equality-preserving, and the type is required to be `EqualityComparable`.

Let `a` and `b` be incrementable objects of type `I`. `Incrementable<I>` is satisfied only if:

- If bool(a == b) then bool(a++ == b).
- If bool(a == b) then bool(void(a++), a) == ++b).

### Equality preservation

An expression is **equality preserving** if it results in equal outputs given equal inputs.

- The inputs to an expression consist of its operands.
- The outputs of an expression consist of its result and all operands modified by the expression (if any).

Every expression required to be equality preserving is further required to be **stable**: two evaluations of such an expression with the same input objects must have equal outputs absent any explicit intervening modification of those input objects.

Unless noted otherwise, every expression used in a **requires-expression** is required to be equality preserving and stable, and the evaluation of the expression may only modify its non-constant operands. Operands that are constant must not be modified.

### Notes

The requirement that `a` equals `b` implies `++a` equals `++b` allows the use of multi-pass algorithms with `Incrementable` types.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/iterator/Incrementable&oldid=155452>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 July 2023, at 23:09.