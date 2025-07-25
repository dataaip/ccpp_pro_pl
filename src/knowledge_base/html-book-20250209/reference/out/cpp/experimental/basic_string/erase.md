# std::experimental::erase (std::basic_string)

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
| experimental::ostream_joiner | | | | |
| experimental::gcd | | | | |
| experimental::lcm | | | | |
| experimental::source_location | | | | |
| experimental::randint | | | | |
| detection idiom | | | | |
| uniform container erasure | | | | |
| logical operator type traits | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/string>` |  |  |
| template< class CharT, class Traits, class A, class U >  void erase( std::basic_string<CharT, Traits, A>& c, const U& value ); |  | (library fundamentals TS v2) |
|  |  |  |

Erases all elements that compare equal to value from the container. Equivalent to c.erase(std::remove(c.begin(), c.end(), value), c.end());.

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | container from which to erase |
| value | - | value to be removed |

### Complexity

Linear.

### Example

Run this code

```
#include <experimental/string>
#include <iostream>
 
int main()
{
    std::string data{"$$P$A$S$S$$W$O$R$$D$"};
    std::cout << data << '\n';
    auto crack{'$'};
    std::experimental::erase(data, crack);
    std::cout << data << '\n';
}

```

Output:

```
$$P$A$S$S$$W$O$R$$D$
PASSWORD

```

### See also

|  |  |
| --- | --- |
| removeremove_if | removes elements satisfying specific criteria   (function template) |
| erase_if (std::basic_string)(library fundamentals 2 TS) | erases all elements satisfying a predicate from a std::basic_string   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/basic_string/erase&oldid=98549>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 January 2018, at 20:12.