# mtx_timedlock

From cppreference.com
< c‎ | thread
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 Concurrency support library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Threads | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | thrd_create | | | | | | thrd_equal | | | | | | thrd_current | | | | | | thrd_sleep | | | | | | thrd_yield | | | | | | thrd_exit | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | thrd_detach | | | | | | thrd_join | | | | | | thrd_successthrd_timedoutthrd_busythrd_nomemthrd_error | | | | | | | Atomic operations | | | | | | atomic_init | | | | | | ATOMIC_VAR_INIT(until C23) | | | | | | ATOMIC_\*\*\*_LOCK_FREE | | | | | | atomic_is_lock_free | | | | | | atomic_store | | | | | | atomic_load | | | | | | atomic_exchange | | | | | | atomic_compare_exchange | | | | | | atomic_fetch_add | | | | | | atomic_fetch_sub | | | | | | atomic_fetch_or | | | | | | atomic_fetch_xor | | | | | | atomic_fetch_and | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Atomic flags | | | | | | atomic_flag | | | | | | ATOMIC_FLAG_INIT | | | | | | atomic_flag_test_and_set | | | | | | atomic_flag_clear | | | | | | Memory ordering | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memory_order | | | | | | kill_dependency | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | atomic_thread_fence | | | | | | atomic_signal_fence | | | | | | | Mutual exclusion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mtx_init | | | | | | mtx_lock | | | | | | ****mtx_timedlock**** | | | | | | mtx_trylock | | | | | | call_once | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mtx_unlock | | | | | | mtx_destroy | | | | | | mtx_plainmtx_recursivemtx_timed | | | | | | | Condition variables | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cnd_init | | | | | | cnd_signal | | | | | | cnd_broadcast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cnd_wait | | | | | | cnd_timedwait | | | | | | cnd_destroy | | | | | | | Thread-local storage | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | thread_local | | | | | | TSS_DTOR_ITERATIONS | | | | | | tss_create | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tss_get | | | | | | tss_set | | | | | | tss_delete | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<threads.h>` |  |  |
| int mtx_timedlock( mtx_t \*restrict mutex,                     const struct timespec \*restrict time_point ); |  | (since C11) |
|  |  |  |

Blocks the current thread until the mutex pointed to by `mutex` is locked or until the TIME_UTC based absolute calendar time point pointed to by `time_point` has been reached.

Since this function takes an absolute time, if a duration is required, the calendar time point must be calculated manually.

The behavior is undefined if the current thread has already locked the mutex and the mutex is not recursive.

The behavior is undefined if the mutex does not support timeout.

Prior calls to mtx_unlock on the same mutex **synchronize-with** this operation (if this operation succeeds), and all lock/unlock operations on any given mutex form a single total order (similar to the modification order of an atomic)

### Parameters

|  |  |  |
| --- | --- | --- |
| mutex | - | pointer to the mutex to lock |
| time_point | - | pointer to the absolute calendar time until which to wait for the timeout |

### Return value

thrd_success if successful, thrd_timedout if the timeout time has been reached before the mutex is locked, thrd_error if an error occurs.

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.26.4.4 The mtx_timedlock function (p: 278)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.26.4.4 The mtx_timedlock function (p: 381-382)

### See also

|  |  |
| --- | --- |
| timespec(C11) | time in seconds and nanoseconds  (struct) |
| mtx_lock(C11) | blocks until locks a mutex   (function) |
| mtx_trylock(C11) | locks a mutex or returns without blocking if already locked   (function) |
| mtx_unlock(C11) | unlocks a mutex   (function) |
| C++ documentation for timed_mutex::try_lock_until | |
| C++ documentation for recursive_timed_mutex::try_lock_until | |

### External links

|  |
| --- |
| GNU GCC Libc Manual: ISO-C-Mutexes |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/thread/mtx_timedlock&oldid=146842>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 January 2023, at 10:45.