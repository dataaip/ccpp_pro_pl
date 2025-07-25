# std::input_iterator_tag, std::output_iterator_tag, std::forward_iterator_tag, std::bidirectional_iterator_tag, std::random_access_iterator_tag, std::contiguous_iterator_tag

From cppreference.com
< cpp‎ | iterator
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

Iterator library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Iterator concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_readable(C++20) | | | | | | indirectly_writable(C++20) | | | | | | weakly_incrementable(C++20) | | | | | | incrementable(C++20) | | | | | | **is-integer-like** **is-signed-integer-like**(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sentinel_for(C++20) | | | | | | sized_sentinel_for(C++20) | | | | | | input_iterator(C++20) | | | | | | output_iterator(C++20) | | | | | | input_or_output_iterator(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_iterator(C++20) | | | | | | bidirectional_iterator(C++20) | | | | | | random_access_iterator(C++20) | | | | | | contiguous_iterator(C++20) | | | | | |  | | | | | |  | | | | | |
| Iterator primitives | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****input_iterator_tagoutput_iterator_tagforward_iterator_tagbidirectional_iterator_tagrandom_access_iterator_tagcontiguous_iterator_tag****(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iter_value_titer_difference_titer_reference_titer_const_reference_titer_rvalue_reference_titer_common_reference_t(C++20)(C++20)(C++20)(C++23)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iterator(deprecated in C++17) | | | | | | iterator_traits | | | | | | incrementable_traits(C++20) | | | | | | indirectly_readable_traits(C++20) | | | | | |  | | | | | |  | | | | | |
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

|  |  |  |
| --- | --- | --- |
| Defined in header `<iterator>` |  |  |
| struct input_iterator_tag {}; | (1) |  |
| struct output_iterator_tag {}; | (2) |  |
| struct forward_iterator_tag : public input_iterator_tag {}; | (3) |  |
| struct bidirectional_iterator_tag : public forward_iterator_tag {}; | (4) |  |
| struct random_access_iterator_tag : public bidirectional_iterator_tag {}; | (5) |  |
| struct contiguous_iterator_tag : public random_access_iterator_tag {}; | (6) | (since C++20) |
|  |  |  |

Defines the category of an iterator. Each tag is an empty type.

### Iterator category

For every LegacyIterator type `It`, a `typedef` std::iterator_traits<It>::iterator_category must be defined to be an alias to one of these tag types, to indicate the most specific category that `It` is in.

1. `input_iterator_tag` corresponds to LegacyInputIterator.
2. `output_iterator_tag` corresponds to LegacyOutputIterator.
3. `forward_iterator_tag` corresponds to LegacyForwardIterator.
4. `bidirectional_iterator_tag` corresponds to LegacyBidirectionalIterator.
5. `random_access_iterator_tag` corresponds to LegacyRandomAccessIterator.

Iterator category tags carry information that can be used to select the most efficient algorithms for the specific requirement set that is implied by the category.

|  |  |
| --- | --- |
| Iterator concept For every `input_iterator` type `It`, either It::iterator_concept (if std::iterator_traits<It> is generated from primary template) or std::iterator_traits<It>::iterator_concept (if std::iterator_traits<It> is specialized) may be declared as an alias to one of these tags, to indicate the strongest iterator concept that `It` intends to model.   1. `input_iterator_tag` corresponds to `input_iterator`. 2. `forward_iterator_tag` corresponds to `forward_iterator`. 3. `bidirectional_iterator_tag` corresponds to `bidirectional_iterator`. 4. `random_access_iterator_tag` corresponds to `random_access_iterator`. 5. `contiguous_iterator_tag` corresponds to `contiguous_iterator`.   If `iterator_concept` is not provided, `iterator_category` is used as a fallback. If `iterator_category` is not provided either (i.e. `It` is not a LegacyIterator), and std::iterator_traits<It> is not specialized, `random_access_iterator_tag` is assumed.  In any case, each concept is not satisfied if the required operations are not supported, regardless of the tag. | (since C++20) |

### Notes

There is no separate tag for LegacyContiguousIterator. That is, it is not possible to tell a LegacyContiguousIterator based on its `iterator_category`. To define specialized algorithm for contiguous iterators, use the `contiguous_iterator` concept.(since C++20)

There are no correspondences between `output_iterator_tag` and the `output_iterator` concept. Setting `iterator_concept` to `output_iterator_tag` only indicates that the type does not model `input_iterator`.

### Example

Common technique for algorithm selection based on iterator category tags is to use a dispatcher function (the alternative is std::enable_if). The iterator tag classes are also used in the corresponding concepts definitions to denote the requirements, which can't be expressed in terms of usage patterns alone.(since C++20)

Run this code

```
#include <iostream>
#include <iterator>
#include <list>
#include <vector>
 
// Using concepts (tag checking is part of the concepts themselves)
 
template<std::bidirectional_iterator BDIter>
void alg(BDIter, BDIter)
{
    std::cout << "1. alg() \t called for bidirectional iterator\n";
}
 
template<std::random_access_iterator RAIter>
void alg(RAIter, RAIter)
{
    std::cout << "2. alg() \t called for random-access iterator\n";
}
 
// Legacy, using tag dispatch
 
namespace legacy
{
    // Quite often implementation details are hidden in a dedicated namespace
    namespace implementation_details
    {
        template<class BDIter>
        void alg(BDIter, BDIter, std::bidirectional_iterator_tag)
        {
            std::cout << "3. legacy::alg() called for bidirectional iterator\n";
        }
 
        template<class RAIter>
        void alg(RAIter, RAIter, std::random_access_iterator_tag)
        {
            std::cout << "4. legacy::alg() called for random-access iterator\n";
        }
    } // namespace implementation_details
 
    template<class Iter>
    void alg(Iter first, Iter last)
    {
        implementation_details::alg(first, last,
            typename std::iterator_traits<Iter>::iterator_category());
    }
} // namespace legacy
 
int main()
{
    std::list<int> l;
    alg(l.begin(), l.end()); // 1.
    legacy::alg(l.begin(), l.end()); // 3.
 
    std::vector<int> v;
    alg(v.begin(), v.end()); // 2.
    legacy::alg(v.begin(), v.end()); // 4.
 
//  std::istreambuf_iterator<char> i1(std::cin), i2;
//  alg(i1, i2);         // compile error: no matching function for call
//  legacy::alg(i1, i2); // compile error: no matching function for call
}

```

Output:

```
1. alg() 	 called for bidirectional iterator
3. legacy::alg() called for bidirectional iterator
2. alg() 	 called for random-access iterator
4. legacy::alg() called for random-access iterator

```

### See also

|  |  |
| --- | --- |
| iterator(deprecated in C++17) | base class to ease the definition of required types for simple iterators   (class template) |
| iterator_traits | provides uniform interface to the properties of an iterator   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator/iterator_tags&oldid=159922>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 October 2023, at 00:24.