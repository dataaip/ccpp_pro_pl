# cnd_init

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Threads | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | thrd_create | | | | | | thrd_equal | | | | | | thrd_current | | | | | | thrd_sleep | | | | | | thrd_yield | | | | | | thrd_exit | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | thrd_detach | | | | | | thrd_join | | | | | | thrd_successthrd_timedoutthrd_busythrd_nomemthrd_error | | | | | | | Atomic operations | | | | | | atomic_init | | | | | | ATOMIC_VAR_INIT(until C23) | | | | | | ATOMIC_\*\*\*_LOCK_FREE | | | | | | atomic_is_lock_free | | | | | | atomic_store | | | | | | atomic_load | | | | | | atomic_exchange | | | | | | atomic_compare_exchange | | | | | | atomic_fetch_add | | | | | | atomic_fetch_sub | | | | | | atomic_fetch_or | | | | | | atomic_fetch_xor | | | | | | atomic_fetch_and | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Atomic flags | | | | | | atomic_flag | | | | | | ATOMIC_FLAG_INIT | | | | | | atomic_flag_test_and_set | | | | | | atomic_flag_clear | | | | | | Memory ordering | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memory_order | | | | | | kill_dependency | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | atomic_thread_fence | | | | | | atomic_signal_fence | | | | | | | Mutual exclusion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mtx_init | | | | | | mtx_lock | | | | | | mtx_timedlock | | | | | | mtx_trylock | | | | | | call_once | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mtx_unlock | | | | | | mtx_destroy | | | | | | mtx_plainmtx_recursivemtx_timed | | | | | | | Condition variables | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****cnd_init**** | | | | | | cnd_signal | | | | | | cnd_broadcast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cnd_wait | | | | | | cnd_timedwait | | | | | | cnd_destroy | | | | | | | Thread-local storage | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | thread_local | | | | | | TSS_DTOR_ITERATIONS | | | | | | tss_create | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tss_get | | | | | | tss_set | | | | | | tss_delete | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<threads.h>` |  |  |
| int cnd_init( cnd_t\* cond ); |  | (since C11) |
|  |  |  |

Initializes new condition variable. The object pointed to by `cond` will be set to value that identifies the condition variable.

### Parameters

|  |  |  |
| --- | --- | --- |
| cond | - | pointer to a variable to store identifier of the condition variable to |

### Return value

thrd_success if the condition variable was successfully created. Otherwise returns thrd_nomem if there was insufficient amount of memory or `thrd_error` if another error occurred.

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.26.3.3 The cnd_init function (p: 276)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.26.3.3 The cnd_init function (p: 379)

### See also

|  |  |
| --- | --- |
| C++ documentation for condition_variable | |
| C++ documentation for condition_variable_any | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/thread/cnd_init&oldid=138852>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 March 2022, at 05:21.