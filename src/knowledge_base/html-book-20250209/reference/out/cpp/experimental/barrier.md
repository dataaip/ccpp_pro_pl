# std::experimental::barrier

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

Extensions for concurrency

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| std::future extensions | | | | |
| experimental::future | | | | |
| experimental::shared_future | | | | |
| experimental::when_all | | | | |
| experimental::when_any | | | | |
| experimental::make_ready_future | | | | |
| experimental::make_exceptional_future | | | | |
| Latches and barriers | | | | |
| experimental::latch | | | | |
| ****experimental::barrier**** | | | | |
| experimental::flex_barrier | | | | |
| Atomic smart pointers | | | | |
| experimental::atomic_shared_ptr | | | | |
| experimental::atomic_weak_ptr | | | | |

****std::experimental::barrier****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| barrier::barrier | | | | |
| barrier::~barrier | | | | |
| barrier::arrive_and_wait | | | | |
| barrier::arrive_and_drop | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/barrier>` |  |  |
| class barrier; |  | (concurrency TS) |
|  |  |  |

The class `std::experimental::barrier` provides a thread-coordination mechanism that allows a set of participating threads to block until an operation is completed. Unlike std::experimental::latch, barriers are reusable; once the participating threads are released from a barrier's synchronization point, they can reuse the same barrier.

A barrier has a completion phase, which is executed by one of the participating threads once all threads in the set of participating threads arrive at the synchronization point. The `arrive_and_wait` and `arrive_and_drop` calls synchronize with the start of the completion phase; the end of the completion phase synchronizes with the returns from all calls blocked by its completion.

For `std::experimental::barrier`, the completion phase is empty. std::experimental::flex_barrier allows the user to control the completion phase with a function object.

The set of participating threads for a `barrier` constructed for `num_threads` threads is the first `num_threads` threads to arrive at its synchronization point after construction. The same set of threads (except for threads that called `arrive_and_drop()`) must arrive at the `barrier` each cycle.

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `barrier`   (public member function) |
| (destructor) | destroys the barrier   (public member function) |
| operator=[deleted] | not copy-assignable   (public member function) |
| arrive_and_wait | arrive at the synchronization point and block   (public member function) |
| arrive_and_drop | arrive at the synchronization point and remove the current thread from the set of participating threads   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/barrier&oldid=163657>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 November 2023, at 06:17.