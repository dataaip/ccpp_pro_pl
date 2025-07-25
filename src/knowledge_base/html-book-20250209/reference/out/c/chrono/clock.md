# clock

From cppreference.com
< c‎ | chrono
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

 Date and time utilities

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Time manipulation | | | | |
| difftime | | | | |
| time | | | | |
| ****clock**** | | | | |
| timespec_get(C11) | | | | |
| timespec_getres(C23) | | | | |
| Format conversions | | | | |
| asctimeasctime_s(deprecated in C23)(C11) | | | | |
| ctimectime_s(deprecated in C23)(C11) | | | | |
| strftime | | | | |
| wcsftime(C95) | | | | |
| gmtimegmtime_rgmtime_s(C23)(C11) | | | | |
| localtimelocaltime_rlocaltime_s(C23)(C11) | | | | |
| mktime | | | | |
| Constants | | | | |
| CLOCKS_PER_SEC | | | | |
| Types | | | | |
| tm | | | | |
| time_t | | | | |
| clock_t | | | | |
| timespec(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<time.h>` |  |  |
| clock_t clock(void); |  |  |
|  |  |  |

Returns the approximate processor time used by the process since the beginning of an implementation-defined era related to the program's execution. To convert result value to seconds, divide it by CLOCKS_PER_SEC.

Only the difference between two values returned by different calls to `clock` is meaningful, as the beginning of the `clock` era does not have to coincide with the start of the program.

`clock` time may advance faster or slower than the wall clock, depending on the execution resources given to the program by the operating system. For example, if the CPU is shared by other processes, `clock` time may advance slower than wall clock. On the other hand, if the current process is multithreaded and more than one execution core is available, `clock` time may advance faster than wall clock.

### Return value

Processor time used by the program so far.

- If the processor time used is not available, returns (clock_t)(-1).
- If the value of the processor time used cannot be represented by clock_t, returns an unspecified value.

### Notes

On POSIX-compatible systems, `clock_gettime` with clock id CLOCK_PROCESS_CPUTIME_ID offers better resolution.

The value returned by `clock()` may wrap around on some implementations. For example, on such an implementation, if clock_t is a signed 32-bit integer and CLOCKS_PER_SEC is 1000000, it will wrap after about 2147 seconds (about 36 minutes).

### Example

This example demonstrates the difference between `clock()` time and real time.

Run this code

```
#ifndef __STDC_NO_THREADS__
    #include <threads.h>
#else
    // POSIX alternative
    #define _POSIX_C_SOURCE 199309L
    #include <pthread.h>
#endif
 
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
 
// the function f() does some time-consuming work
int f(void* thr_data) // return void* in POSIX
{
    (void) thr_data;
    volatile double d = 0;
    for (int n = 0; n < 10000; ++n)
       for (int m = 0; m < 10000; ++m)
           d += d * n * m;
    return 0;
}
 
int main(void)
{
    struct timespec ts1, tw1; // both C11 and POSIX
    clock_gettime(CLOCK_PROCESS_CPUTIME_ID, &ts1); // POSIX
    clock_gettime(CLOCK_MONOTONIC, &tw1); // POSIX; use timespec_get in C11
    clock_t t1 = clock();
 
#ifndef __STDC_NO_THREADS__
    thrd_t thr1, thr2;  // C11; use pthread_t in POSIX
    thrd_create(&thr1, f, NULL); // C11; use pthread_create in POSIX
    thrd_create(&thr2, f, NULL);
    thrd_join(thr1, NULL); // C11; use pthread_join in POSIX
    thrd_join(thr2, NULL);
#endif
 
    struct timespec ts2, tw2;
    clock_gettime(CLOCK_PROCESS_CPUTIME_ID, &ts2);
    clock_gettime(CLOCK_MONOTONIC, &tw2);
    clock_t t2 = clock();
 
    double dur = 1000.0 * (t2 - t1) / CLOCKS_PER_SEC;
    double posix_dur = 1000.0 * ts2.tv_sec + 1e-6 * ts2.tv_nsec
                           - (1000.0 * ts1.tv_sec + 1e-6 * ts1.tv_nsec);
    double posix_wall = 1000.0 * tw2.tv_sec + 1e-6 * tw2.tv_nsec
                            - (1000.0 * tw1.tv_sec + 1e-6 * tw1.tv_nsec);
 
    printf("CPU time used (per clock()): %.2f ms\n", dur);
    printf("CPU time used (per clock_gettime()): %.2f ms\n", posix_dur);
    printf("Wall time passed: %.2f ms\n", posix_wall);
}

```

Possible output:

```
CPU time used (per clock()): 1580.00 ms
CPU time used (per clock_gettime()): 1582.76 ms
Wall time passed: 792.13 ms

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.27.2.1 The clock function (p: 285)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.27.2.1 The clock function (p: 389)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.23.2.1 The clock function (p: 339)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.12.2.1 The clock function

### See also

|  |  |
| --- | --- |
| ctimectime_s(deprecated in C23)(C11) | converts a time_t object to a textual representation   (function) |
| time | returns the current calendar time of the system as time since epoch   (function) |
| C++ documentation for clock | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/chrono/clock&oldid=180116>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 February 2025, at 00:52.