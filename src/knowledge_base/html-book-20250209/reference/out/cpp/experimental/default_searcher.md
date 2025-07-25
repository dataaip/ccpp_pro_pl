# std::experimental::default_searcher, std::experimental::make_default_searcher

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
| experimental::sample | | | | |
| experimental::shared_ptr | | | | |
| experimental::weak_ptr | | | | |
| experimental::apply | | | | |
| experimental::invocation_typeexperimental::raw_invocation_type | | | | |
| experimental::search | | | | |
| ****experimental::default_searcherexperimental::make_default_searcher**** | | | | |
| experimental::boyer_moore_searcherexperimental::make_boyer_moore_searcher | | | | |
| experimental::boyer_moore_horspool_searcherexperimental::make_boyer_moore_horspool_searcher | | | | |
| Type-erased and polymorphic allocators | | | | |
| Variable templates for type traits | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/functional>` |  |  |
| template< class ForwardIterator1, class BinaryPredicate = std::equal_to<> >  class default_searcher; |  | (library fundamentals TS) |
|  |  |  |

A class suitable for use with std::experimental::search that delegates the search operation to the standard library's std::search.

`default_searcher` is CopyConstructible and CopyAssignable.

### Member functions

## std::experimental::default_searcher::default_searcher

|  |  |  |
| --- | --- | --- |
| default_searcher( ForwardIterator pat_first,                    ForwardIterator pat_last,                   BinaryPredicate pred = BinaryPredicate() ); |  |  |
|  |  |  |

Constructs a `default_searcher` by storing copies of pat_first, pat_last, and pred.

### Parameters

|  |  |  |
| --- | --- | --- |
| pat_first, pat_last | - | a pair of iterators designating the string to be searched for |
| pred | - | a callable object used to determine equality |

### Exceptions

Any exceptions thrown by the copy constructors of `BinaryPredicate` or `ForwardIterator`.

## std::experimental::default_searcher::operator()

|  |  |  |
| --- | --- | --- |
| template< class ForwardIterator2 >  ForwardIterator2 operator()( ForwardIterator2 first, ForwardIterator2 last ) const; |  | (until C++17) |
| template< class ForwardIterator2 >  std::pair<ForwardIterator2, ForwardIterator2>     operator()( ForwardIterator2 first, ForwardIterator2 last ) const; |  | (since C++17) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

The member function called by std::experimental::search to perform a search with this searcher.

|  |  |
| --- | --- |
| Equivalent to std::search(first, last, pat_first, pat_last, pred);. | (until C++17) |
| Returns a pair of iterators `i, j`, where `i` is std::search(first, last, pat_first, pat_last, pred) and `j` is std::next(i, std::distance(pat_first, pat_last)) unless `std::search` returned last (no match), in which case `j` equals last as well. | (until C++17) |

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | a pair of iterators designating the string to be examined |

### Return value

|  |  |
| --- | --- |
| Iterator to the first position in ``first`,`last`)` where a subsequence that compares equal to `[`pat_first`,`pat_last`)` as defined by pred is located, or a copy of last otherwise. | (until C++17) |
| A pair of iterators to the first and one past last positions in `[`first`,`last`)` where a subsequence that compares equal to `[`pat_first`,`pat_last`)` as defined by pred is located, or a pair of copies of last otherwise. | (since C++17) |

### Helper Functions

|  |  |  |
| --- | --- | --- |
| template< class ForwardIterator, class BinaryPredicate = [std::equal_to<> >  default_searcher<ForwardIterator, BinaryPredicate> make_default_searcher(      ForwardIterator pat_first,      ForwardIterator pat_last,     BinaryPredicate pred = BinaryPredicate()); |  | (library fundamentals TS) |
|  |  |  |

Helper function that constructs a `std::experimental::default_searcher` using template argument deduction. Equivalent to return default_searcher<ForwardIterator, BinaryPredicate>(pat_first, pat_last, pred);

### Parameters

|  |  |  |
| --- | --- | --- |
| pat_first, pat_last | - | a pair of iterators designating the string to be searched for |
| pred | - | a callable object used to determine equality |

### Return value

A `default_searcher` constructed with the arguments pat_first, pat_last, pred.

### Example

Run this code

```
#include <experimental/algorithm>
#include <experimental/functional>
#include <iostream>
#include <string>
 
int main()
{
    std::string in = "Lorem ipsum dolor sit amet, consectetur adipiscing elit,"
                     " sed do eiusmod tempor incididunt ut labore et dolore magna aliqua";
    std::string needle = "pisci";
    auto it = std::experimental::search(in.begin(), in.end(),
                  std::experimental::make_default_searcher(
                      needle.begin(), needle.end()));
    if (it != in.end())
        std::cout << "The string " << needle << " found at offset "
                  << it - in.begin() << '\n';
    else
        std::cout << "The string " << needle << " not found\n";
}

```

Output:

```
The string pisci found at offset 43

```

### See also

|  |  |
| --- | --- |
| search | searches for the first occurrence of a range of elements   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/default_searcher&oldid=154735>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 July 2023, at 03:21.