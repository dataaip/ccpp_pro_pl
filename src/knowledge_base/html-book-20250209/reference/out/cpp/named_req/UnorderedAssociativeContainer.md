# C++ named requirements: UnorderedAssociativeContainer (since C++11)

From cppreference.com
< cpp‎ | named req
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

C++ named requirements

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Basic | | | | | | DefaultConstructible | | | | | | MoveConstructible(C++11) | | | | | | CopyConstructible | | | | | | CopyAssignable | | | | | | MoveAssignable(C++11) | | | | | | Destructible | | | | | | Type properties | | | | | | ScalarType | | | | | | PODType | | | | | | TriviallyCopyable(C++11) | | | | | | TrivialType(C++11) | | | | | | StandardLayoutType(C++11) | | | | | | ImplicitLifetimeType | | | | | | Library-wide | | | | | | BooleanTestable | | | | | | EqualityComparable | | | | | | LessThanComparable | | | | | | Swappable | | | | | | ValueSwappable(C++11) | | | | | | NullablePointer(C++11) | | | | | | Hash(C++11) | | | | | | Allocator | | | | | | FunctionObject | | | | | | Callable | | | | | | Predicate | | | | | | BinaryPredicate | | | | | | Compare | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Container | | | | | | Container | | | | | | ReversibleContainer | | | | | | AllocatorAwareContainer | | | | | | SequenceContainer | | | | | | ContiguousContainer(C++17) | | | | | | AssociativeContainer | | | | | | ****UnorderedAssociativeContainer****(C++11) | | | | | | Container element | | | | | | DefaultInsertable(C++11) | | | | | | CopyInsertable(C++11) | | | | | | MoveInsertable(C++11) | | | | | | EmplaceConstructible(C++11) | | | | | | Erasable(C++11) | | | | | | Iterator | | | | | | LegacyIterator | | | | | | LegacyInputIterator | | | | | | LegacyOutputIterator | | | | | | LegacyForwardIterator | | | | | | LegacyBidirectionalIterator | | | | | | LegacyRandomAccessIterator | | | | | | LegacyContiguousIterator(C++17) | | | | | | ConstexprIterator(C++20) | | | | | | Stream I/O | | | | | | FormattedInputFunction | | | | | | UnformattedInputFunction | | | | | | FormattedOutputFunction | | | | | | UnformattedOutputFunction | | | | | | Formatters | | | | | | BasicFormatter(C++20) | | | | | | Formatter(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random Numbers | | | | | | SeedSequence(C++11) | | | | | | RandomNumberEngine(C++11) | | | | | | RandomNumberDistribution(C++11) | | | | | | UniformRandomBitGenerator(C++11) | | | | | | RandomNumberEngineAdaptor(C++11) | | | | | | Concurrency | | | | | | BasicLockable(C++11) | | | | | | Lockable(C++11) | | | | | | TimedLockable(C++11) | | | | | | SharedLockable(C++14) | | | | | | SharedTimedLockable(C++14) | | | | | | Mutex(C++11) | | | | | | TimedMutex(C++11) | | | | | | SharedMutex(C++17) | | | | | | SharedTimedMutex(C++14) | | | | | | Ranges | | | | | | RangeAdaptorObject(C++20) | | | | | | RangeAdaptorClosureObject(C++20) | | | | | | Multidimensional View | | | | | | LayoutMapping(C++23) | | | | | | LayoutMappingPolicy(C++23) | | | | | | AccessorPolicy(C++23) | | | | | | Other | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | CharTraits | | | | | | RegexTraits(C++11) | | | | | | BitmaskType | | | | | | LiteralType(C++11) | | | | | | NumericType | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | UnaryTypeTrait(C++11) | | | | | | BinaryTypeTrait(C++11) | | | | | | TransformationTrait(C++11) | | | | | | Clock(C++11) | | | | | | TrivialClock(C++11) | | | | | | |  | | | | | |

Unordered associative containers are Containers that provide fast lookup of objects based on keys.
Worst case complexity is linear but on average much faster for most of the operations.

Unordered associative containers are parametrized by `Key`; `Hash`, a Hash function object which acts as hash function on `Key`; and `Pred`, a BinaryPredicate evaluating equivalence between `Key`s.
std::unordered_map and std::unordered_multimap also have a mapped type `T` associated with the `Key`.

If two `Key`s are equal according to `Pred`, `Hash` must return the same value for both keys.

|  |  |
| --- | --- |
| If both `Hash::is_transparent` and `Pred::is_transparent` exist and each names a type, member functions `find`, `contains`, `count`, `equal_range`, and `bucket` accept arguments of types other than `Key` and expect that `Hash` is callable with values of those types, and that `Pred` is a transparent comparison function such as std::equal_to<>. | (since C++20) |

std::unordered_map and std::unordered_set can contain at most one element with a given key, std::unordered_multiset and std::unordered_multimap instead can have multiple elements with the same key (which must always be adjacent on iterations).

For std::unordered_set and std::unordered_multiset the value type is the same as the key type and both `iterator` and `const_iterator` are constant iterators.
For std::unordered_map and std::unordered_multimap the value type is std::pair<const Key, T>.

Elements in an unordered associative container are organized into buckets, keys with the same hash will end up in the same bucket.
The number of buckets is increased when the size of the container increases to keep the average number of elements in each bucket under a certain value.

Rehashing invalidates iterator and might cause the elements to be re-arranged in different buckets but it does not invalidate references to the elements.

Unordered associative containers meet the requirements of AllocatorAwareContainer.
For std::unordered_map and std::unordered_multimap the requirements of `value_type` in AllocatorAwareContainer apply to `key_type` and
`mapped_type` (not to `value_type`).

### Requirements

|  |  |
| --- | --- |
| Legend | |
| `X` | An unordered associative container class |
| a | A value of type `X` |
| a2 | A value of a type with nodes compatible with type `X` |
| b | A value of type `X` or `const X` |
| a_uniq | A value of type `X` when `X` supports unique keys |
| a_eq | A value of type `X` when `X` supports equivalent keys |
| a_tran | A value of type `X` or const X when the qualified identifiers `X::key_equal::is_transparent` and `X::hasher::is_transparent` are both valid and denote types |
| i, j | Input iterators that refer to `value_type` |
| ``i`,`j`)` | A valid range |
| rg (since C++23) | A value of a type `R` that models [**container-compatible-range**`<value_type>` |
| p, q2 | Valid constant iterators to a |
| q, q1 | Valid dereferenceable constant iterators to a |
| r | A valid dereferenceable iterator to a |
| ``q1`,`q2`)` | A valid range in a |
| il | A value of type [std::initializer_list<value_type> |
| t | A value of type `X::value_type` |
| k | A value of type `key_type` |
| hf | A value of type `hasher` or const hasher |
| eq | A value of type `key_equal` or const key_equal |
| ke | A value such that  - eq(r1, ke) == eq(ke, r1), - hf(r1) == hf(ke) if eq(r1, ke) is true, and - if any two of eq(r1, ke), eq(r2, ke), and eq(r1, r2) are true, then all three are true,   where r1 and r2 are keys of elements in a_tran |
| kx (since C++23) | A value such that  - eq(r1, kx) == eq(kx, r1), - hf(r1) == hf(kx) if eq(r1, kx) is true, - if any two of eq(r1, kx), eq(r2, kx), and eq(r1, r2) are true, then all three are true, and - kx is not convertible to either `iterator` or `const_iterator`,   where r1 and r2 are keys of elements in a_tran |
| n | A value of type `size_type` |
| z | A value of type float |
| nh (since C++17) | An rvalue of type X::node_type |

#### Member types

| Name | Type | Requirements | Notes |
| --- | --- | --- | --- |
| `X::key_type` | `Key` |  |  |
| `X::mapped_type` | `T` | std::unordered_map and std::unordered_multimap only |  |
| `X::value_type` | `Key` | std::unordered_set and std::unordered_multiset only. Erasable in `X` |  |
| std::pair<const Key, T> | std::unordered_map and std::unordered_multimap only. Erasable in `X` |  |
| `X::hasher` | `Hash` | Hash |  |
| `X::key_equal` | `Pred` | CopyConstructible; BinaryPredicate that takes two arguments of type `Key` and expresses an equivalence relation |  |
| `X::local_iterator` | LegacyIterator | Category and types are the same as `X::iterator` | Can be used to iterate through a single bucket, but not across buckets |
| `X::const_local_iterator` | LegacyIterator | Category and types are the same as `X::const_iterator` |
| `X::node_type` (since C++17) | A specialization of node-handle class template | The public nested types are the same as the corresponding types in `X` |  |

#### Member functions and operators

| Expression | Result | Preconditions | Effects | Returns | Complexity |
| --- | --- | --- | --- | --- | --- |
| X(n, hf, eq) |  |  | Constructs an empty container with at least n buckets, using hf as the hash function and eq as the key equality predicate |  | O(n) |
| X(n, hf) |  | `key_equal` is DefaultConstructible | Constructs an empty container with at least n buckets, using hf as the hash function and key_equal() as the key equality predicate |  | O(n) |
| X(n) |  | `hasher` and `key_equal` are DefaultConstructible | Constructs an empty container with at least n buckets, using hasher() as the hash function and key_equal() as the key equality predicate |  | O(n) |
| X a = X(); X a; |  | `hasher` and `key_equal` are DefaultConstructible | Constructs an empty container with an unspecified number of buckets, using hasher() as the hash function and key_equal() as the key equality predicate |  | Constant |
| X(i, j, n, hf, eq) |  | `value_type` is EmplaceConstructible into `X` from \*i | Constructs an empty container with at least n buckets, using hf as the hash function and eq as the key equality predicate, and inserts elements from ``i`,`j`)` into it |  | Average case O(N) (N is [std::distance(i, j)), worst case O(N2) |
| X(i, j, n, hf) |  | `key_equal` is the DefaultConstructible. `value_type` is EmplaceConstructible into `X` from \*i | Constructs an empty container with at least n buckets, using hf as the hash function and key_equal() as the key equality predicate, and inserts elements from ``i`,`j`)` into it |  | Average case O(N) (N is [std::distance(i, j)), worst case O(N2) |
| X(i, j, n) |  | `hasher` and `key_equal` are DefaultConstructible. `value_type` is EmplaceConstructible into `X` from \*i | Constructs an empty container with at least n buckets, using hasher() as the hash function and key_equal() as the key equality predicate, and inserts elements from ``i`,`j`)` into it |  | Average case O(N) (N is [std::distance(i, j)), worst case O(N2) |
| X(i, j) |  | `hasher` and `key_equal` are DefaultConstructible. `value_type` is EmplaceConstructible into `X` from \*i | Constructs an empty container with an unspecified number of buckets, using hasher() as the hash function and key_equal() as the key equality predicate, and inserts elements from ``i`,`j`)` into it |  | Average case O(N) (N is [std::distance(i, j)), worst case O(N2) |
| X(std::from_range,   rg, n, hf, eq) (since C++23) |  | `value_type` is EmplaceConstructible into `X` from \*ranges::begin(rg) | Constructs an empty container with at least n buckets, using hf as the hash function and eq as the key equality predicate, and inserts elements from rg into it |  | Average case O(N) (N is ranges::distance(rg)), worst case O(N2) |
| X(std::from_range,   rg, n, hf) (since C++23) |  | `key_equal` is DefaultConstructible. `value_type` is EmplaceConstructible into `X` from \*ranges::begin(rg) | Constructs an empty container with at least n buckets, using hf as the hash function and key_equal() as the key equality predicate, and inserts elements from rg into it |  | Average case O(N) (N is ranges::distance(rg)), worst case O(N2) |
| X(std::from_range,   rg, n) (since C++23) |  | `hasher` and `key_equal` are DefaultConstructible. `value_type` is EmplaceConstructible into `X` from \*ranges::begin(rg) | Constructs an empty container with at least n buckets, using hasher() as the hash function and key_equal() as the key equality predicate, and inserts elements from rg into it |  | Average case O(N) (N is ranges::distance(rg)), worst case O(N2) |
| X(std::from_range,   rg) (since C++23) |  | `hasher` and `key_equal` are DefaultConstructible. `value_type` is EmplaceConstructible into `X` from \*ranges::begin(rg) | Constructs an empty container with an unspecified number of buckets, using hasher() as the hash function and key_equal() as the key equality predicate, and inserts elements from rg into it |  | Average case O(N) (N is ranges::distance(rg)), worst case O(N2) |
| X(il) |  |  | X(il.begin(), il.end()) |  |  |
| X(il, n) |  |  | X(il.begin(), il.end(), n) |  |  |
| X(il, n, hf) |  |  | X(il.begin(), il.end(), n, hf) |  |  |
| X(il, n, hf, eq) |  |  | X(il.begin(), il.end(), n, hf, eq) |  |  |
| X(b) |  |  | Container; Copies the hash function, predicate, and maximum load factor |  | Average case linear in b.size(), worst case O(N2) |
| a = b | `X&` |  | Container; copies the hash function, predicate, and maximum load factor |  | Average case linear in b.size(), worst case O(N2) |
| a = il | `X&` | `value_type` is CopyInsertable into `X` and CopyAssignable | Assigns the range ``il.begin()`,`il.end()`)` into a. All existing elements of a are either assigned to or destroyed |  | Average case linear in il.size(), worst case O(N2) |
| b.hash_function() | `hasher` |  |  | b's hash function | Constant |
| b.key_eq() | `key_equal` |  |  | b's key equality predicate | Constant |
| a_uniq.emplace(args) | [std::pair<   iterator,   bool> | `value_type` is EmplaceConstructible into `X` from args | Inserts a `value_type` object t constructed with std::forward<Args>(args)... if and only if there is no element in the container with key equivalent to the key of t | The bool component of the returned pair is true if and only if the insertion takes place, and the iterator component of the pair points to the element with key equivalent to the key of t | Average case O(1), worst case O(a_uniq.size()) |
| a_eq.emplace(args) | `iterator` | `value_type` is EmplaceConstructible into `X` from args | Inserts a `value_type` object t constructed with std::forward<Args>(args)... | An iterator pointing to the newly inserted element | Average case O(1), worst case O(a_eq.size()) |
| a.emplace_hint(p, args) | `iterator` | `value_type` is EmplaceConstructible into `X` from args | a.emplace(   std::forward<Args>(args)...) | An iterator pointing to the element with the key equivalent to the newly inserted element. The `const_iterator` p is a hint pointing to where the search should start. Implementations are permitted to ignore the hint | Average case O(1), worst case O(a.size()) |
| a_uniq.insert(t) | std::pair<   iterator,   bool> | If t is a non-const rvalue, `value_type` is MoveInsertable into `X`; otherwise, `value_type` is CopyInsertable into `X` | Inserts t if and only if there is no element in the container with key equivalent to the key of t | The bool component of the returned pair indicates whether the insertion takes place, and the `iterator` component points to the element with key equivalent to the key of t | Average case O(1), worst case O(a_uniq.size()) |
| a_eq.insert(t) | `iterator` | If t is a non-const rvalue, `value_type` is MoveInsertable into `X`; otherwise, `value_type` is CopyInsertable into `X` | Inserts t | An iterator pointing to the newly inserted element | Average case O(1), worst case O(a_eq.size()) |
| a.insert(p, t) | `iterator` | If t is a non-const rvalue, `value_type` is MoveInsertable into `X`; otherwise, `value_type` is CopyInsertable into `X` | a.insert(t). The iterator p is a hint pointing to where the search should start. Implementations are permitted to ignore the hint | An iterator pointing to the element with the key equivalent to that of t | Average case O(1), worst case O(a.size()) |
| a.insert(i, j) | void | `value_type` is EmplaceConstructible into `X` from \*i. Neither i nor j are iterators into a | a.insert(t) for each element in ``i`,`j`)` |  | Average case O(N), where N is [std::distance(i, j), worst case O(N·(a.size() + 1)) |
| a.insert_range(rg) (since C++23) | void | `value_type` is EmplaceConstructible into `X` from \*ranges::begin(rg). rg and a do not overlap | a.insert(t) for each element t in rg |  | Average case O(N), where N is ranges::distance(rg), worst case O(N·(a.size() + 1)) |
| a.insert(il) |  |  | a.insert(il.begin(), il.end()) |  |  |
| a_uniq.insert(nh) (since C++17) | `insert_return_type` | nh is empty or a_uniq.get_allocator() == nh.get_allocator() is true | If nh is empty, has no effect. Otherwise, inserts the element owned by nh if and only if there is no element in the container with a key equivalent to nh.key(). Ensures: If nh is empty, inserted is false, position is end(), and node is empty. Otherwise if the insertion took place, inserted is true, position points to the inserted element, and node is empty; if the insertion failed, inserted is false, node has the previous value of nh, and position points to an element with a key equivalent to nh.key() |  | Average case O(1), worst case O(a_uniq.size()) |
| a_eq.insert(nh) (since C++17) | `iterator` | nh is empty or a_eq.get_allocator() == nh.get_allocator() is true | If nh is empty, has no effect and returns a_eq.end(). Otherwise, inserts the element owned by nh and returns an iterator pointing to the newly inserted element. Ensures: nh is empty |  | Average case O(1), worst case O(a_eq.size()) |
| a.insert(q, nh) (since C++17) | `iterator` | nh is empty or a.get_allocator() == nh.get_allocator() is true | If nh is empty, has no effect and returns a.end(). Otherwise, inserts the element owned by nh if and only if there is no element with key equivalent to nh.key() in containers with unique keys; always inserts the element owned by nh in containers with equivalent keys. The iterator q is a hint pointing to where the search should start. Implementations are permitted to ignore the hint. Ensures: nh is empty if insertion succeeds, unchanged if insertion fails | An iterator pointing to the element with key equivalent to nh.key() | Average case O(1), worst case O(a.size()) |
| a.extract(k) (since C++17) | `node_type` |  | Removes an element in the container with key equivalent to k | A `node_type` owning the element if found, otherwise an empty `node_type` | Average case O(1), worst case O(a.size()) |
| a_tran.extract(kx) (since C++23) | `node_type` |  | Removes an element in the container with key equivalent to kx | A `node_type` owning the element if found, otherwise an empty `node_type` | Average case O(1), worst case O(a_tran.size()) |
| a.extract(q) (since C++17) | `node_type` |  | Removes the element pointed to by q | A `node_type` owning that element | Average case O(1), worst case O(a.size()) |
| a.merge(a2) (since C++17) | void | a.get_allocator() == a2.get_allocator() | Attempts to extract each element in a2 and insert it into a using the hash function and key equality predicate of a. In containers with unique keys, if there is an element in a with key equivalent to the key of an element from a2, then that element is not extracted from a2. Ensures: Pointers and references to the transferred elements of a2 refer to those same elements but as members of a. Iterators referring to the transferred elements and all iterators referring to a will be invalidated, but iterators to elements remaining in a2 will remain valid |  | Average case O(N), where N is a2.size(), worst case O(N·(a.size() + 1)) |
| a.erase(k) | `size_type` |  | Erases all elements with key equivalent to k | The number of elements erased | Average case O(a.count(k)), worst case O(a.size()) |
| a_tran.erase(kx) (since C++23) | `size_type` |  | Erases all elements with key equivalent to kx | The number of elements erased | Average case O(a_tran.count(kx)), worst case O(a_tran.size()) |
| a.erase(q) | `iterator` |  | Erases the element pointed to by q | The iterator immediately following q prior to the erasure | Average case O(1), worst case O(a.size()) |
| a.erase(r) (since C++17) | `iterator` |  | Erases the element pointed to by r | The iterator immediately following r prior to the erasure | Average case O(1), worst case O(a.size()) |
| a.erase(q1, q2) | `iterator` |  | Erases all elements in the range ``q1`,`q2`)` | The iterator immediately following the erased elements prior to the erasure | Average case linear in [std::distance(q1, q2), worst case O(a.size()) |
| a.clear() | void |  | Erases all elements in the container. Ensures: a.empty() is true |  | Linear in a.size() |
| b.find(k) | `iterator`; `const_iterator` for constant b |  |  | An iterator pointing to an element with key equivalent to k, or b.end() if no such element exists | Average case O(1), worst case O(b.size()) |
| a_tran.find(ke) (since C++17)? | `iterator`; `const_iterator` for constant a_tran |  |  | An iterator pointing to an element with key equivalent to ke, or a_tran.end() if no such element exists | Average case O(1), worst case O(a_tran.size()) |
| b.count(k) | `size_type` |  |  | The number of elements with key equivalent to k | Average case O(b.count(k)), worst case O(b.size()) |
| a_tran.count(ke) (since C++17)? | `size_type` |  |  | The number of elements with key equivalent to ke | Average case O(a_tran.count(ke)), worst case O(a_tran.size()) |
| b.contains(k) (since C++20)? |  |  | b.find(k) != b.end() |  |  |
| a_tran.contains(ke) (since C++20)? |  |  | a_tran.find(ke) != a_tran.end() |  |  |
| b.equal_range(k) | std::pair<   iterator,   iterator>; std::pair<   const_iterator,   const_iterator> for constant b |  |  | A range containing all elements with keys equivalent to k. Returns std::make_pair(   b.end(), b.end()) if no such elements exist | Average case O(b.count(k)), worst case O(b.size()) |
| a_tran.equal_range(ke) (since C++20)? | std::pair<   iterator,   iterator>; std::pair<   const_iterator,   const_iterator> for constant a_tran |  |  | A range containing all elements with keys equivalent to ke. Returns std::make_pair(   a_tran.end(),   a_tran.end()) if no such elements exist | Average case O(a_tran.count(ke)), worst case O(a_tran.size()) |
| b.bucket_count() | `size_type` |  |  | The number of buckets that b contains | Constant |
| b.max_bucket_count() | `size_type` |  |  | An upper bound on the number of buckets that b can ever contain | Constant |
| b.bucket(k) | `size_type` | b.bucket_count() > 0 |  | The index of the bucket in which elements with keys equivalent to k would be found, if any such element existed. The return value is in ``​0​`,`b.bucket_count()`)` | Constant |
| a_tran.bucket(ke) | `size_type` | a_tran. bucket_count() > 0 |  | The index of the bucket in which elements with keys equivalent to ke would be found, if any such element existed. The return value must be in the range `[`​0​`,`a_tran.bucket_count()`)` | Constant |
| b.bucket_size(n) | `size_type` | n is in `[`​0​`,`b.bucket_count()`)` |  | The number of elements in the nth bucket | O(b.bucket_size(n)) |
| b.begin(n) | `local_iterator`; `const_local_iterator` for constant b | n is in `[`​0​`,`b.bucket_count()`)` |  | An iterator referring to the first element in the bucket. If the bucket is empty, then b.begin(n) == b.end(n) | Constant |
| b.end(n) | `local_iterator`; `const_local_iterator` for constant b | n is in `[`​0​`,`b.bucket_count()`)` |  | An iterator which is the past-the-end value for the bucket | Constant |
| b.cbegin(n) | `const_local_iterator` | n is in `[`​0​`,`b.bucket_count()`)` |  | An iterator referring to the first element in the bucket. If the bucket is empty, then b.cbegin(n) == b.cend(n) | Constant |
| b.cend(n) | `const_local_iterator` | n is in `[`​0​`,`b.bucket_count()`)` |  | An iterator which is the past-the-end value for the bucket | Constant |
| b.load_factor() | float |  |  | The average number of elements per bucket | Constant |
| b.max_load_factor() | float |  |  | A positive number that the container attempts to keep the load factor less than or equal to. The container automatically increases the number of buckets as necessary to keep the load factor below this number | Constant |
| a.max_load_factor(z) | void | z is positive. May change the container's maximum load factor, using z as a hint |  |  | Constant |
| a.rehash(n) | void |  | Ensures: a.bucket_count() >=   a.size() / a.max_load_factor() and a.bucket_count() >= n |  | Average case linear in a.size(), worst case O(N2) |
| a.reserve(n) |  |  | a.rehash([std::ceil(   n / a.max_load_factor())) |  |  |

|  |  |
| --- | --- |
|  | This section is incomplete Reason: Requirements regarding member functions. |

### Standard library

The following standard library containers satisfy the UnorderedAssociativeContainer requirements:

|  |  |
| --- | --- |
| unordered_set(C++11) | collection of unique keys, hashed by keys   (class template) |
| unordered_multiset(C++11) | collection of keys, hashed by keys   (class template) |
| unordered_map(C++11) | collection of key-value pairs, hashed by keys, keys are unique   (class template) |
| unordered_multimap(C++11) | collection of key-value pairs, hashed by keys   (class template) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2156 | C++11 | the load factor after rehashing could only be strictly lower than the maximum load factor | allowed to be equal |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/named_req/UnorderedAssociativeContainer&oldid=177778>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 November 2024, at 11:15.