# signal

From cppreference.com
< c‎ | program
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

 Program support utilities

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Program termination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | abort | | | | | | exit | | | | | | quick_exit(C11) | | | | | | _Exit(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | atexit | | | | | | at_quick_exit(C11) | | | | | | EXIT_SUCCESSEXIT_FAILURE | | | | | |
| Unreachable control flow | | | | |
| unreachable(C23) | | | | |
| Communicating with the environment | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | getenvgetenv_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | system | | | | | |  | | | | | |
| Memory alignment query | | | | |
| memalignment(C23) | | | | |
| Signals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****signal**** | | | | | | raise | | | | | | sig_atomic_t | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIG_DFLSIG_IGN | | | | | | SIG_ERR | | | | | |
| Signal types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGABRTSIGFPESIGILL | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGINTSIGSEGVSIGTERM | | | | | |
| Non-local jumps | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setjmp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | longjmp | | | | | |
| Types | | | | |
| jmp_buf | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<signal.h>` |  |  |
| void (\*signal( int sig, void (\*handler) (int))) (int); |  |  |
|  |  |  |

Sets the error handler for signal `sig`. The signal handler can be set so that default handling will occur, signal is ignored, or a user-defined function is called.

When signal handler is set to a function and a signal occurs, it is implementation defined whether signal(sig, SIG_DFL) will be executed immediately before the start of signal handler. Also, the implementation can prevent some implementation-defined set of signals from occurring while the signal handler runs.

### Parameters

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| sig | - | the signal to set the signal handler to. It can be an implementation-defined value or one of the following values:  |  |  | | --- | --- | | SIGABRTSIGFPESIGILLSIGINTSIGSEGVSIGTERM | defines signal types   (macro constant) | |
| handler | - | the signal handler. This must be one of the following:  - SIG_DFL macro. The signal handler is set to default signal handler. - SIG_IGN macro. The signal is ignored. - pointer to a function. The signature of the function must be equivalent to the following:  |  |  |  | | --- | --- | --- | | void fun(int sig); |  |  | |  |  |  | |

### Return value

Previous signal handler on success or SIG_ERR on failure (setting a signal handler can be disabled on some implementations).

### Signal handler

The following limitations are imposed on the user-defined function that is installed as a signal handler.

If the user defined function returns when handling SIGFPE, SIGILL or SIGSEGV, the behavior is undefined.

If the signal handler is called as a result of abort or raise, the behavior is undefined if the signal handler calls raise.

If the signal handler is called NOT as a result of abort or raise (in other words, the signal handler is **asynchronous**), the behavior is undefined if

- the signal handler calls any function within the standard library, except

:   - abort
    - _Exit
    - quick_exit
    - `signal` with the first argument being the number of the signal currently handled (async handler can re-register itself, but not other signals).
    - atomic functions from `<stdatomic.h>` if the atomic arguments are lock-free
    - atomic_is_lock_free (with any kind of atomic arguments)

- the signal handler refers to any object with static or thread-local(since C11) storage duration that is not a lock-free atomic(since C11) other than by assigning to a static volatile sig_atomic_t.

On entry to the signal handler, the state of the floating-point environment and the values of all objects is unspecified, except for

- objects of type volatile sig_atomic_t
- objects of lock-free atomic types (since C11)
- side effects made visible through atomic_signal_fence (since C11)

On return from a signal handler, the value of any object modified by the signal handler that is not volatile sig_atomic_t or lock-free atomic(since C11) is undefined.

The behavior is undefined if signal is used in a multithreaded program. It is not required to be thread-safe.

### Notes

POSIX requires that `signal` is thread-safe, and specifies a list of async-signal-safe library functions that may be called from any signal handler.

Besides `abort` and `raise`, POSIX specifies that `kill`, `pthread_kill`, and `sigqueue` generate synchronous signals.

POSIX recommends `sigaction` instead of `signal`, due to its underspecified behavior and significant implementation variations, regarding signal delivery while a signal handler is executed.

### Example

Run this code

```
#include <signal.h>
#include <stdio.h>
 
volatile sig_atomic_t gSignalStatus;
 
void signal_handler(int signal)
{
  gSignalStatus = signal;
}
 
int main(void)
{
  signal(SIGINT, signal_handler);
 
  printf("SignalValue: %d\n", gSignalStatus);
  printf("Sending signal: %d\n", SIGINT);
  raise(SIGINT);
  printf("SignalValue: %d\n", gSignalStatus);
}

```

Output:

```
SignalValue: 0
Sending signal: 2
SignalValue: 2

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.14.1.1 The signal function (p: 193-194)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.14.1.1 The signal function (p: 266-267)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.14.1.1 The signal function (p: 247-248)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.7.1.1 The signal function

### See also

|  |  |
| --- | --- |
| raise | runs the signal handler for particular signal   (function) |
| C++ documentation for signal | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/program/signal&oldid=140330>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 June 2022, at 07:06.