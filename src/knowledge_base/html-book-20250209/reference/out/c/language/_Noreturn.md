# _Noreturn function specifier (since C11)(deprecated in C23)

From cppreference.com
< c‎ | language
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

 C language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Basic concepts | | | | |
| Keywords | | | | |
| Preprocessor | | | | |
| Statements | | | | |
| Expressions | | | | |
| Initialization | | | | |
| Declarations | | | | |
| Functions | | | | |
| Miscellaneous | | | | |
| History of C | | | | |
| Technical Specifications | | | | |

 Functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| function declaration | | | | |
| function definition | | | | |
| variadic arguments | | | | |
| inline(C99) | | | | |
| ****_Noreturn****(C11) | | | | |

Specifies that the function does not return to its point of invocation.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| _Noreturn function_declaration |  | (since C11)(deprecated in C23) |
|  | | | | | | | | | |

### Explanation

The `_Noreturn` keyword appears in a function declaration and specifies that the function does not return by executing the return statement or by reaching the end of the function body (it may return by executing longjmp). If the function declared `_Noreturn` returns, the behavior is undefined. A compiler diagnostic is recommended if this can be detected.

The `_Noreturn` specifier may appear more than once in the same function declaration, the behavior is the same as if it appeared once.

This specifier is typically used through the convenience macro noreturn, which is provided in the header `<stdnoreturn.h>`.

|  |  |
| --- | --- |
| `_Noreturn` function specifier is deprecated. `[[noreturn]]` attribute should be used instead.  The macro `noreturn` is also deprecated. | (since C23) |

### Keywords

_Noreturn

### Standard library

The following functions are `noreturn` in the standard library:

- abort()
- exit()
- _Exit()
- quick_exit()
- thrd_exit()
- longjmp()

### Example

Run this code

```
#include <stdio.h>
#include <stdlib.h>
#include <stdnoreturn.h>
 
// causes undefined behavior if i <= 0
// exits if i > 0
noreturn void exit_now(int i) // or _Noreturn void exit_now(int i)
{
    if (i > 0)
        exit(i);
}
 
int main(void)
{
    puts("Preparing to exit...");
    exit_now(2);
    puts("This code is never executed.");
}

```

Output:

```
Preparing to exit...

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.7.4 Function specifiers (p: TBD)

:   - 7.23 _Noreturn <stdnoreturn.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 6.7.4 Function specifiers (p: 90-91)

:   - 7.23 _Noreturn <stdnoreturn.h> (p: 263)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.7.4 Function specifiers (p: 125-127)

:   - 7.23 _Noreturn <stdnoreturn.h> (p: 361)

### See also

|  |  |
| --- | --- |
| `[[noreturn]]`(C23) `[[_Noreturn]]`(C23)(deprecated) | indicates that the function does not return (attribute specifier) |
| C++ documentation for `[[noreturn]]` | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/_Noreturn&oldid=180091>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 February 2025, at 12:34.