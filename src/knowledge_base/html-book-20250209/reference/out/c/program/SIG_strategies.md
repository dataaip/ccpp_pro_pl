# SIG_DFL, SIG_IGN

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | signal | | | | | | raise | | | | | | sig_atomic_t | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****SIG_DFLSIG_IGN**** | | | | | | SIG_ERR | | | | | |
| Signal types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGABRTSIGFPESIGILL | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGINTSIGSEGVSIGTERM | | | | | |
| Non-local jumps | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setjmp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | longjmp | | | | | |
| Types | | | | |
| jmp_buf | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<signal.h>` |  |  |
| #define SIG_DFL /\*implementation defined\*/ |  |  |
| #define SIG_IGN /\*implementation defined\*/ |  |  |
|  |  |  |

The ****SIG_DFL**** and ****SIG_IGN**** macros expand into integral expressions that are not equal to an address of any function. The macros define signal handling strategies for signal() function.

|  |  |
| --- | --- |
| Constant | Explanation |
| `SIG_DFL` | default signal handling |
| `SIG_IGN` | signal is ignored |

### Example

Run this code

```
#include <signal.h>
#include <stdio.h>
 
int main(void)
{
    /* using the default signal handler */
    raise(SIGTERM);
    printf("Exit main()\n");   /* never reached */
}

```

Output:

```
(none)

```

### Example

Run this code

```
#include <signal.h>
#include <stdio.h>
 
int main(void)
{
    /* ignoring the signal */
    signal(SIGTERM, SIG_IGN);
    raise(SIGTERM);
    printf("Exit main()\n");
}

```

Output:

```
Exit main()

```

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
| C++ documentation for SIG_DFL, SIG_IGN | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/program/SIG_strategies&oldid=140329>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 June 2022, at 07:04.