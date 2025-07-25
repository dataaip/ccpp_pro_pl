# SIGTERM, SIGSEGV, SIGINT, SIGILL, SIGABRT, SIGFPE

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | signal | | | | | | raise | | | | | | sig_atomic_t | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIG_DFLSIG_IGN | | | | | | SIG_ERR | | | | | |
| Signal types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****SIGABRTSIGFPESIGILL**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****SIGINTSIGSEGVSIGTERM**** | | | | | |
| Non-local jumps | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setjmp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | longjmp | | | | | |
| Types | | | | |
| jmp_buf | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<signal.h>` |  |  |
| #define SIGTERM /\*implementation defined\*/ |  |  |
| #define SIGSEGV /\*implementation defined\*/ |  |  |
| #define SIGINT /\*implementation defined\*/ |  |  |
| #define SIGILL /\*implementation defined\*/ |  |  |
| #define SIGABRT /\*implementation defined\*/ |  |  |
| #define SIGFPE /\*implementation defined\*/ |  |  |
|  |  |  |

Each of the above macro constants expands to an integer constant expression with distinct values, which represent different signals sent to the program.

|  |  |
| --- | --- |
| Constant | Explanation |
| `SIGTERM` | termination request, sent to the program |
| `SIGSEGV` | invalid memory access (segmentation fault) |
| `SIGINT` | external interrupt, usually initiated by the user |
| `SIGILL` | invalid program image, such as invalid instruction |
| `SIGABRT` | abnormal termination condition, as is e.g. initiated by abort() |
| `SIGFPE` | erroneous arithmetic operation such as divide by zero |

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.14/3 Signal handling <signal.h> (p: 193)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.14/3 Signal handling <signal.h> (p: 265)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.14/3 Signal handling <signal.h> (p: 246)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.7 SIGNAL HANDLING <signal.h>

### See also

|  |  |
| --- | --- |
| signal | sets a signal handler for particular signal   (function) |
| raise | runs the signal handler for particular signal   (function) |
| C++ documentation for signal types | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/program/SIG_types&oldid=140335>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 June 2022, at 08:14.