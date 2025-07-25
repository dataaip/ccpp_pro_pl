# std::experimental::sample

From cppreference.com
< cpp‎ | experimental
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
| ****experimental::sample**** | | | | |
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

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/algorithm>` |  |  |
| template< class PopulationIterator, class SampleIterator,  class Distance, class URBG >  SampleIterator sample( PopulationIterator first, PopulationIterator last,                         SampleIterator out, Distance n,                        URBG&& g ); | (1) | (library fundamentals TS) |
| template< class PopulationIterator, class SampleIterator, class Distance >  SampleIterator sample( PopulationIterator first, PopulationIterator last,                        SampleIterator out, Distance n ); | (2) | (library fundamentals TS v2) |
|  |  |  |

Selects n elements from the sequence ``first`,`last`)` such that each possible sample has equal probability of appearance, and writes those selected elements into the output iterator out.

If n is greater than the number of elements in the sequence, selects last - first elements.

The algorithm is stable only if `PopulationIterator` meets the requirements of [LegacyForwardIterator.

1) Random numbers are generated using the random number generator g.2) Random numbers are generated using the per-thread engine.

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | pair of iterators forming the range from which to make the sampling (the population) |
| out | - | the output iterator where the samples are written. Must not be in the range ``first`,`last`)` |
| n | - | number of samples to make |
| g | - | the random number generator used as the source of randomness |
| -`PopulationIterator` must meet the requirements of [LegacyInputIterator. | | |
| -`SampleIterator` must meet the requirements of LegacyOutputIterator. | | |
| -`SampleIterator` must also meet the requirements of LegacyRandomAccessIterator if `PopulationIterator` doesn't meet LegacyForwardIterator. | | |
| -`PopulationIterator`'s value type must be writeable to out. | | |
| -`Distance` must be an integer type. | | |
| -`URBG` must meet the requirements of UniformRandomBitGenerator and its return type must be convertible to `Distance`. | | |

### Return value

Returns a copy of out after the last sample that was output, that is, end of the sample range.

### Complexity

Linear in std::distance(first, last).

### Notes

This function may implement selection sampling or reservoir sampling.

### Example

Run this code

```
#include <experimental/algorithm>
#include <iostream>
#include <iterator>
#include <random>
#include <string>
 
int main()
{
    std::string in = "abcdefgh", out;
    std::experimental::sample(in.begin(), in.end(), std::back_inserter(out),
                              5, std::mt19937{std::random_device{}()});
    std::cout << "five random letters out of " << in << " : " << out << '\n';
}

```

Possible output:

```
five random letters out of abcdefgh : cdefg

```

### See also

|  |  |
| --- | --- |
| random_shuffleshuffle(until C++17)(C++11) | randomly re-orders elements in a range   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/sample&oldid=155685>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 July 2023, at 00:01.