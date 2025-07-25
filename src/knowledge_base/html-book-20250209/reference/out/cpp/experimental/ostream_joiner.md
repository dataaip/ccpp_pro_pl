# std::experimental::ostream_joiner

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

Library fundamentals v2

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::propagate_const | | | | |
| experimental::not_fn | | | | |
| experimental::observer_ptr | | | | |
| experimental::make_array | | | | |
| experimental::to_array | | | | |
| ****experimental::ostream_joiner**** | | | | |
| experimental::gcd | | | | |
| experimental::lcm | | | | |
| experimental::source_location | | | | |
| experimental::randint | | | | |
| detection idiom | | | | |
| uniform container erasure | | | | |
| logical operator type traits | | | | |

****std::experimental::ostream_joiner****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ostream_joiner::ostream_joiner | | | | |
| ostream_joiner::operator= | | | | |
| ostream_joiner::operator\* | | | | |
| ostream_joiner::operator++ostream_joiner::operator++(int) | | | | |
| Non-member functions | | | | |
| make_ostream_joiner | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/iterator>` |  |  |
| template<  class DelimT,      class CharT = char,      class Traits = std::char_traits<CharT>  > class ostream_joiner; |  | (library fundamentals TS v2) |
|  |  |  |

`std::experimental::ostream_joiner` is a single-pass LegacyOutputIterator that writes successive objects into the std::basic_ostream object for which it was constructed, using `operator<<`, separated by a delimiter. The delimiter is written to the output stream between every two objects that are written. The write operation is performed when the iterator (whether dereferenced or not) is assigned to. Incrementing the `ostream_joiner` is a no-op.

In a typical implementation, the only data members of `ostream_joiner` are a pointer to the associated std::basic_ostream, the delimiter, and a bool member that indicates whether the next write is for the first element in the sequence.

Compared to std::ostream_iterator, `ostream_joiner` prints the delimiter sequence one fewer time, and is not templated on the type of the object to be printed.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `char_type` | `CharT` |
| `traits_type` | `Traits` |
| `ostream_type` | std::basic_ostream<CharT, Traits> |
| `value_type` | void |
| `difference_type` | void |
| `pointer` | void |
| `reference` | void |
| `iterator_category` | std::output_iterator_tag |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new `ostream_joiner`   (public member function) |
| (destructor)(implicitly declared) | destructs an `ostream_joiner`   (public member function) |
| operator= | writes an object to the associated output sequence   (public member function) |
| operator\* | no-op   (public member function) |
| operator++operator++(int) | no-op   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| make_ostream_joiner | creates an `ostream_joiner` object, deducing the template's type arguments from the function arguments   (function template) |

### Example

Run this code

```
#include <algorithm>
#include <experimental/iterator>
#include <iostream>
#include <iterator>
 
int main()
{
    int i[] = {1, 2, 3, 4, 5};
    std::copy(std::begin(i),
              std::end(i),
              std::experimental::make_ostream_joiner(std::cout, ", "));
}

```

Output:

```
1, 2, 3, 4, 5

```

### See also

|  |  |
| --- | --- |
| ostreambuf_iterator | output iterator that writes to std::basic_streambuf   (class template) |
| ostream_iterator | output iterator that writes to std::basic_ostream   (class template) |
| istream_iterator | input iterator that reads from std::basic_istream   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ostream_joiner&oldid=148791>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 March 2023, at 14:46.