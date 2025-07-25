# Iterator library

From cppreference.com
< cpp
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
| ****Iterators library**** | | | | |
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

****Iterator library****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Iterator concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_readable(C++20) | | | | | | indirectly_writable(C++20) | | | | | | weakly_incrementable(C++20) | | | | | | incrementable(C++20) | | | | | | **is-integer-like** **is-signed-integer-like**(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sentinel_for(C++20) | | | | | | sized_sentinel_for(C++20) | | | | | | input_iterator(C++20) | | | | | | output_iterator(C++20) | | | | | | input_or_output_iterator(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_iterator(C++20) | | | | | | bidirectional_iterator(C++20) | | | | | | random_access_iterator(C++20) | | | | | | contiguous_iterator(C++20) | | | | | |  | | | | | |  | | | | | |
| Iterator primitives | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | input_iterator_tagoutput_iterator_tagforward_iterator_tagbidirectional_iterator_tagrandom_access_iterator_tagcontiguous_iterator_tag(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iter_value_titer_difference_titer_reference_titer_const_reference_titer_rvalue_reference_titer_common_reference_t(C++20)(C++20)(C++20)(C++23)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iterator(deprecated in C++17) | | | | | | iterator_traits | | | | | | incrementable_traits(C++20) | | | | | | indirectly_readable_traits(C++20) | | | | | |  | | | | | |  | | | | | |
| Algorithm concepts and utilities | | | | |
| Indirect callable concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_unary_invocableindirectly_regular_unary_invocable(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_unary_predicate(C++20) | | | | | | indirect_binary_predicate(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_equivalence_relation(C++20) | | | | | | indirect_strict_weak_order(C++20) | | | | | |
| Common algorithm requirements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_movable(C++20) | | | | | | indirectly_movable_storable(C++20) | | | | | | indirectly_copyable(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_copyable_storable(C++20) | | | | | | indirectly_swappable(C++20) | | | | | | indirectly_comparable(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | permutable(C++20) | | | | | | mergeable(C++20) | | | | | | sortable(C++20) | | | | | |
| Utilities | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_result_t(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | projected(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | projected_value_t(C++26) | | | | | |
| Iterator adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_iterator | | | | | | make_reverse_iterator(C++14) | | | | | | move_iterator(C++11) | | | | | | make_move_iterator(C++11) | | | | | | default_sentinel_tdefault_sentinel(C++20)(C++20) | | | | | | unreachable_sentinel_tunreachable_sentinel(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | front_insert_iterator | | | | | | back_insert_iterator | | | | | | inserter | | | | | | insert_iterator | | | | | | front_inserter | | | | | | back_inserter | | | | | | move_sentinel(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_iterator(C++20) | | | | | | counted_iterator(C++20) | | | | | | basic_const_iterator(C++23) | | | | | | const_iterator(C++23) | | | | | | const_sentinel(C++23) | | | | | | make_const_iterator(C++23) | | | | | | make_const_sentinel(C++23) | | | | | |  | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Stream iterators | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istream_iterator | | | | | | ostream_iterator | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istreambuf_iterator | | | | | | ostreambuf_iterator | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator customization points | | | | | | ranges::iter_move(C++20) | | | | | | ranges::iter_swap(C++20) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator operations | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | advance | | | | | | distance | | | | | | prev(C++11) | | | | | | next(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ranges::advance(C++20) | | | | | | ranges::distance(C++20) | | | | | | ranges::prev(C++20) | | | | | | ranges::next(C++20) | | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | begincbegin(C++11)(C++14) | | | | | | rbegincrbegin(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | endcend(C++11)(C++14) | | | | | | rendcrend(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sizessize(C++17)(C++20) | | | | | | empty(C++17) | | | | | | data(C++17) | | | | | | | |

Iterators are a generalization of pointers that allow a C++ program to work with different data structures (for example, containers and ranges(since C++20)) in a uniform manner. The iterator library provides definitions for iterators, as well as iterator traits, adaptors, and utility functions.

Since iterators are an abstraction of pointers, their semantics are a generalization of most of the semantics of pointers in C++. This ensures that every function template that takes iterators works as well with regular pointers.

### Iterator categories

There are five(until C++17)six(since C++17) kinds of iterators: LegacyInputIterator, LegacyOutputIterator, LegacyForwardIterator, LegacyBidirectionalIterator, LegacyRandomAccessIterator, and LegacyContiguousIterator(since C++17). (See also LegacyIterator for the most basic kind of iterator.)

Instead of being defined by specific types, each category of iterator is defined by the operations that can be performed on it. This definition means that any type that supports the necessary operations can be used as an iterator -- for example, a pointer supports all of the operations required by LegacyRandomAccessIterator, so a pointer can be used anywhere a LegacyRandomAccessIterator is expected.

All of the iterator categories (except LegacyOutputIterator) can be organized into a hierarchy, where more powerful iterator categories (e.g. LegacyRandomAccessIterator) support the operations of less powerful categories (e.g. LegacyInputIterator). If an iterator falls into one of these categories and also satisfies the requirements of LegacyOutputIterator, then it is called a **mutable** iterator and supports **both** input and output. Non-mutable iterators are called **constant** iterators.

|  |  |
| --- | --- |
| Iterators are called **constexpr** iterators if all operations provided to meet iterator category requirements are constexpr functions. | (since C++20) |

| Iterator category | Operations and storage requirement | | | | | | |
| --- | --- | --- | --- | --- | --- | --- | --- |
| write | read | increment | | decrement | random    access | contiguous  storage |
| without    multiple    passes | with    multiple    passes |
| LegacyIterator |  |  | Required |  |  |  |  |
| LegacyOutputIterator | Required |  | Required |  |  |  |  |
| LegacyInputIterator (mutable if supports write operation) |  | Required | Required |  |  |  |  |
| LegacyForwardIterator (also satisfies LegacyInputIterator) |  | Required | Required | Required |  |  |  |
| LegacyBidirectionalIterator (also satisfies LegacyForwardIterator) |  | Required | Required | Required | Required |  |  |
| LegacyRandomAccessIterator (also satisfies LegacyBidirectionalIterator) |  | Required | Required | Required | Required | Required |  |
| LegacyContiguousIterator[[1]](iterator.html#cite_note-1) (also satisfies LegacyRandomAccessIterator) |  | Required | Required | Required | Required | Required | Required |

1. ↑ LegacyContiguousIterator category was only formally specified in C++17, but the iterators of std::vector, std::basic_string, std::array, and std::valarray, as well as pointers into C arrays are often treated as a separate category in pre-C++17 code.

Note: A type supporting the required operations in a row of the table above does not necessarily fall into the corresponding category, see the category page for the complete list of requirements.

### Definitions

#### Types and writability

An input iterator i supports the expression \*i, resulting in a value of some object type `T`, called the **value type** of the iterator.

An output iterator i has a non-empty set of types that are **writable**(until C++20)indirectly_writable(since C++20) to the iterator; for each such type `T`, the expression \*i = o is valid where o is a value of type `T`.

For every iterator type `X` for which equality is defined(until C++20), there is a corresponding signed integer(until C++20)integer-like(since C++20) type called the **difference type** of the iterator.

#### Dereferenceability and validity

Just as a regular pointer to an array guarantees that there is a pointer value pointing past the last element of the array, so for any iterator type there is an iterator value that points past the last element of a corresponding sequence. Such a value is called a **past-the-end** value.

Values of an iterator i for which the expression \*i is defined are called **dereferenceable**. The standard library never assumes that past-the-end values are dereferenceable.

Iterators can also have **singular** values that are not associated with any sequence. Results of most expressions are undefined for singular values; the only exceptions are

- the assignment of a non-singular value to an iterator that holds a singular value,
- destroying an iterator that holds a singular value, and,
- for iterators that meet the DefaultConstructible requirements, using a value-initialized iterator as the source of a copy or move(since C++11) operation.

In these cases the singular value is overwritten the same way as any other value. Dereferenceable values are always non-singular.

An **invalid** iterator is an iterator that may be singular.

#### Ranges

Most of the standard library’s algorithmic templates that operate on data structures have interfaces that use ranges.

|  |  |
| --- | --- |
| An iterator j is called **reachable** from an iterator i if and only if there is a finite sequence of applications of the expression ++i that makes i == j. If j is reachable from i, they refer to elements of the same sequence.  A **range** is a pair of iterators that designate the beginning and end of the computation. A range ``i`,`i`)` is an empty range; in general, a range `[`i`,`j`)` refers to the elements in the data structure starting with the element pointed to by i and up to but not including the element pointed to by j.  Range `[`i`,`j`)` is **valid** if and only if j is reachable from i. | (until C++20) |
| A **range** can be denoted by either   - `[`i`,`s`)`, with an iterator i and a **sentinel** s that designate the beginning and end of the computation (i and s can have different types), or - i`+``[`​0​`,`n`)`, with an iterator i and a count n that designate the beginning and the number of elements to which the computation is to be applied.  Iterator-sentinel range An iterator and a sentinel denoting a range are comparable. `[`i`,`s`)` is empty if i == s; otherwise, `[`i`,`s`)` refers to the elements in the data structure starting with the element pointed to by i and up to but not including the element, if any, pointed to by the first iterator j such that j == s.  A sentinel s is called **reachable** from an iterator i if and only if there is a finite sequence of applications of the expression ++i that makes i == s.  If s is reachable from i, `[`i`,`s`)` denotes a **valid** range. Counted range A **counted range** i`+``[`​0​`,`n`)` is empty if n == 0; otherwise, i`+``[`​0​`,`n`)` refers to the n elements in the data structure starting with the element pointed to by i and up to but not including the element, if any, pointed to by the result of n applications of ++i.  A counted range i`+``[`​0​`,`n`)` is **valid** if and only if   - n == 0; or - all of the following conditions are satisfied:   - n is positive,   - i is dereferenceable, and   - ++i`+``[`​0​`,`--n`)` is valid. | (since C++20) |

The result of the application of functions in the standard library to invalid ranges is undefined.

### Iterator concepts (since C++20)

A new system of iterators based on [concepts that are different from C++17 iterators. While the basic taxonomy remains similar, the requirements for individual iterator categories are somewhat different.

|  |  |
| --- | --- |
| Defined in namespace `std` | |
| indirectly_readable(C++20) | specifies that a type is indirectly readable by applying operator `*`   (concept) |
| indirectly_writable(C++20) | specifies that a value can be written to an iterator's referenced object   (concept) |
| weakly_incrementable(C++20) | specifies that a `semiregular` type can be incremented with pre- and post-increment operators   (concept) |
| incrementable(C++20) | specifies that the increment operation on a `weakly_incrementable` type is equality-preserving and that the type is `equality_comparable`   (concept) |
| **is-integer-likeis-signed-integer-like**(C++20)(C++20) | specifies that a type behaves as a (signed) integer type (exposition-only concept\*) |
| input_or_output_iterator(C++20) | specifies that objects of a type can be incremented and dereferenced   (concept) |
| sentinel_for(C++20) | specifies a type is a sentinel for an `input_or_output_iterator` type   (concept) |
| sized_sentinel_for(C++20) | specifies that the - operator can be applied to an iterator and a sentinel to calculate their difference in constant time   (concept) |
| input_iterator(C++20) | specifies that a type is an input iterator, that is, its referenced values can be read and it can be both pre- and post-incremented   (concept) |
| output_iterator(C++20) | specifies that a type is an output iterator for a given value type, that is, values of that type can be written to it and it can be both pre- and post-incremented   (concept) |
| forward_iterator(C++20) | specifies that an `input_iterator` is a forward iterator, supporting equality comparison and multi-pass   (concept) |
| bidirectional_iterator(C++20) | specifies that a `forward_iterator` is a bidirectional iterator, supporting movement backwards   (concept) |
| random_access_iterator(C++20) | specifies that a `bidirectional_iterator` is a random-access iterator, supporting advancement in constant time and subscripting   (concept) |
| contiguous_iterator(C++20) | specifies that a `random_access_iterator` is a contiguous iterator, referring to elements that are contiguous in memory   (concept) |

### Iterator associated types (since C++20)

|  |  |
| --- | --- |
| Defined in namespace `std` | |
| incrementable_traits(C++20) | computes the difference type of a `weakly_incrementable` type   (class template) |
| indirectly_readable_traits(C++20) | computes the value type of an `indirectly_readable` type   (class template) |
| iter_value_titer_reference_titer_const_reference_titer_difference_titer_rvalue_reference_titer_common_reference_t(C++20)(C++20)(C++23)(C++20)(C++20)(C++20) | computes the associated types of an iterator (alias template) |

### Iterator primitives

|  |  |
| --- | --- |
| iterator_traits | provides uniform interface to the properties of an iterator   (class template) |
| input_iterator_tagoutput_iterator_tagforward_iterator_tagbidirectional_iterator_tagrandom_access_iterator_tagcontiguous_iterator_tag(C++20) | empty class types used to indicate iterator categories   (class) |
| iterator(deprecated in C++17) | base class to ease the definition of required types for simple iterators   (class template) |

### Iterator customization points (since C++20)

|  |  |
| --- | --- |
| Defined in namespace `std::ranges` | |
| iter_move(C++20) | casts the result of dereferencing an object to its associated rvalue reference type (customization point object) |
| iter_swap(C++20) | swaps the values referenced by two dereferenceable objects (customization point object) |

### Algorithm concepts and utilities (since C++20)

A set of concepts and related utility templates designed to ease constraining common algorithm operations.

|  |  |
| --- | --- |
| Defined in header `<iterator>` | |
| Defined in namespace `std` | |
| Indirect callable concepts | |
| indirectly_unary_invocableindirectly_regular_unary_invocable(C++20)(C++20) | specifies that a callable type can be invoked with the result of dereferencing an `indirectly_readable` type   (concept) |
| indirect_unary_predicate(C++20) | specifies that a callable type, when invoked with the result of dereferencing an `indirectly_readable` type, satisfies `predicate`   (concept) |
| indirect_binary_predicate(C++20) | specifies that a callable type, when invoked with the result of dereferencing two `indirectly_readable` types, satisfies `predicate`   (concept) |
| indirect_equivalence_relation(C++20) | specifies that a callable type, when invoked with the result of dereferencing two `indirectly_readable` types, satisfies `equivalence_relation`   (concept) |
| indirect_strict_weak_order(C++20) | specifies that a callable type, when invoked with the result of dereferencing two `indirectly_readable` types, satisfies `strict_weak_order`   (concept) |
| Common algorithm requirements | |
| indirectly_movable(C++20) | specifies that values may be moved from an `indirectly_readable` type to an `indirectly_writable` type   (concept) |
| indirectly_movable_storable(C++20) | specifies that values may be moved from an `indirectly_readable` type to an `indirectly_writable` type and that the move may be performed via an intermediate object   (concept) |
| indirectly_copyable(C++20) | specifies that values may be copied from an `indirectly_readable` type to an `indirectly_writable` type   (concept) |
| indirectly_copyable_storable(C++20) | specifies that values may be copied from an `indirectly_readable` type to an `indirectly_writable` type and that the copy may be performed via an intermediate object   (concept) |
| indirectly_swappable(C++20) | specifies that the values referenced by two `indirectly_readable` types can be swapped   (concept) |
| indirectly_comparable(C++20) | specifies that the values referenced by two `indirectly_readable` types can be compared   (concept) |
| permutable(C++20) | specifies the common requirements of algorithms that reorder elements in place   (concept) |
| mergeable(C++20) | specifies the requirements of algorithms that merge sorted sequences into an output sequence by copying elements   (concept) |
| sortable(C++20) | specifies the common requirements of algorithms that permute sequences into ordered sequences   (concept) |
| Utilities | |
| indirect_result_t(C++20) | computes the result of invoking a callable object on the result of dereferencing some set of `indirectly_readable` types (alias template) |
| projected(C++20) | helper template for specifying the constraints on algorithms that accept projections   (class template) |
| projected_value_t(C++26) | computes the value type of an `indirectly_readable` type by projection (alias template) |

### Iterator adaptors

|  |  |
| --- | --- |
| reverse_iterator | iterator adaptor for reverse-order traversal   (class template) |
| make_reverse_iterator(C++14) | creates a std::reverse_iterator of type inferred from the argument   (function template) |
| back_insert_iterator | iterator adaptor for insertion at the end of a container   (class template) |
| back_inserter | creates a std::back_insert_iterator of type inferred from the argument   (function template) |
| front_insert_iterator | iterator adaptor for insertion at the front of a container   (class template) |
| front_inserter | creates a std::front_insert_iterator of type inferred from the argument   (function template) |
| insert_iterator | iterator adaptor for insertion into a container   (class template) |
| inserter | creates a std::insert_iterator of type inferred from the argument   (function template) |
| basic_const_iterator(C++23) | iterator adaptor that converts an iterator into a constant iterator   (class template) |
| const_iterator(C++23) | computes a constant iterator type for a given type (alias template) |
| const_sentinel(C++23) | computes a sentinel type to be used with constant iterators (alias template) |
| make_const_iterator(C++23) | creates a std::const_iterator of type inferred from the argument   (function template) |
| make_const_sentinel(C++23) | creates a std::const_sentinel of type inferred from the argument   (function template) |
| move_iterator(C++11) | iterator adaptor which dereferences to an rvalue   (class template) |
| move_sentinel(C++20) | sentinel adaptor for std::move_iterator   (class template) |
| make_move_iterator(C++11) | creates a std::move_iterator of type inferred from the argument   (function template) |
| common_iterator(C++20) | adapts an iterator type and its sentinel into a common iterator type   (class template) |
| default_sentinel_t(C++20) | default sentinel for use with iterators that know the bound of their range   (class) |
| counted_iterator(C++20) | iterator adaptor that tracks the distance to the end of the range   (class template) |
| unreachable_sentinel_t(C++20) | sentinel that always compares unequal to any `weakly_incrementable` type   (class) |

### Stream iterators

|  |  |
| --- | --- |
| istream_iterator | input iterator that reads from std::basic_istream   (class template) |
| ostream_iterator | output iterator that writes to std::basic_ostream   (class template) |
| istreambuf_iterator | input iterator that reads from std::basic_streambuf   (class template) |
| ostreambuf_iterator | output iterator that writes to std::basic_streambuf   (class template) |

### Iterator operations

|  |  |
| --- | --- |
| Defined in header `<iterator>` | |
| advance | advances an iterator by given distance   (function template) |
| distance | returns the distance between two iterators   (function template) |
| next(C++11) | increment an iterator   (function template) |
| prev(C++11) | decrement an iterator   (function template) |
| ranges::advance(C++20) | advances an iterator by given distance or to a given bound (algorithm function object) |
| ranges::distance(C++20) | returns the distance between an iterator and a sentinel, or between the beginning and end of a range (algorithm function object) |
| ranges::next(C++20) | increment an iterator by a given distance or to a bound (algorithm function object) |
| ranges::prev(C++20) | decrement an iterator by a given distance or to a bound (algorithm function object) |

### Range access (since C++11)

These non-member function templates provide a generic interface for containers, plain arrays, and std::initializer_list.

|  |  |
| --- | --- |
| Defined in header `<array>` | |
| Defined in header `<deque>` | |
| Defined in header `<flat_map>` | |
| Defined in header `<flat_set>` | |
| Defined in header `<forward_list>` | |
| Defined in header `<inplace_vector>` | |
| Defined in header `<iterator>` | |
| Defined in header `<list>` | |
| Defined in header `<map>` | |
| Defined in header `<regex>` | |
| Defined in header `<set>` | |
| Defined in header `<span>` | |
| Defined in header `<string>` | |
| Defined in header `<string_view>` | |
| Defined in header `<unordered_map>` | |
| Defined in header `<unordered_set>` | |
| Defined in header `<vector>` | |
| Defined in namespace `std` | |
| begincbegin(C++11)(C++14) | returns an iterator to the beginning of a container or array   (function template) |
| endcend(C++11)(C++14) | returns an iterator to the end of a container or array   (function template) |
| rbegincrbegin(C++14) | returns a reverse iterator to the beginning of a container or array   (function template) |
| rendcrend(C++14) | returns a reverse end iterator for a container or array   (function template) |
| sizessize(C++17)(C++20) | returns the size of a container or array   (function template) |
| empty(C++17) | checks whether the container is empty   (function template) |
| data(C++17) | obtains the pointer to the underlying array   (function template) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 1181 | C++98 | array types could not be value types | they can |
| LWG 208 | C++98 | past-the-end iterators were always non-singular | they can be singular |
| LWG 278 | C++98 | the validity of an iterator was not defined | defined to be always non-singular |
| LWG 324 | C++98 | output iterators had value types | output iterators have writable types instead |
| LWG 407 | C++98 | singular iterators could not be destroyed | allowed |
| LWG 408 (N3066) | C++98 | singular iterators could not be copied | allowed if they are value-initialized |
| LWG 1185 (N3066) | C++98 | LegacyForwardIterator, LegacyBidirectionalIterator and LegacyRandomAccessIterator always satisfy LegacyOutputIterator | they might not satisfy LegacyOutputIterator |
| LWG 1210 (N3066) | C++98 | the definition of iterator singularity and reachability depended on containers | depend on sequences instead |
| LWG 3009 | C++17 | <string_view> did not provide the range access function templates | provides these templates |
| LWG 3987 | C++23 | <flat_map> and <flat_set> did not provide the range access function templates | provide these templates |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator&oldid=179898>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 January 2025, at 10:31.