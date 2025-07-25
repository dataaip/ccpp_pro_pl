# while loop

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

 Statements

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Labels | | | | |
| label : statement | | | | |
| Expression statements | | | | |
| expression ; | | | | |
| Compound statements | | | | |
| { statement... } | | | | |
| Selection statements | | | | |
| if | | | | |
| switch | | | | |
| Iteration statements | | | | |
| ****while**** | | | | |
| do-while | | | | |
| for | | | | |
| Jump statements | | | | |
| break | | | | |
| continue | | | | |
| return | | | | |
| goto | | | | |

Executes a statement repeatedly, until the value of expression becomes equal to zero. The test takes place before each iteration.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr-spec-seq(optional) `while (` expression `)` statement |  |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| expression | - | any expression of scalar type. This expression is evaluated before each iteration, and if it compares equal to zero, the loop is exited. |
| statement | - | any statement, typically a compound statement, which serves as the body of the loop |
| attr-spec-seq | - | (C23)optional list of attributes, applied to the loop statement |

### Explanation

A `while` statement causes the statement (also called **the loop body**) to be executed repeatedly until the expression (also called **controlling expression**) compares equal to zero. The repetition occurs regardless of whether the loop body is entered normally or by a goto into the middle of statement.

The evaluation of expression takes place before each execution of statement (unless entered by a goto). If the controlling expression needs to be evaluated after the loop body, the do-while loop may be used.

If the execution of the loop needs to be terminated at some point,  break statement can be used as a terminating statement.

If the execution of the loop needs to be continued at the end of the loop body,  continue statement can be used as a shortcut.

A program with an endless loop has undefined behavior if the loop has no observable behavior (I/O, volatile accesses, atomic or synchronization operation) in any part of its statement or expression. This allows the compilers to optimize out all unobservable loops without proving that they terminate. The only exceptions are the loops where
expression is a constant expression; `while(true)` is always an endless loop.

|  |  |
| --- | --- |
| As with all other selection and iteration statements, the while statement establishes block scope: any identifier introduced in the expression goes out of scope after the statement. | (since C99) |

### Notes

Boolean and pointer expressions are often used as loop controlling expressions. The boolean value `false` and the null pointer value of any pointer type compare equal to zero.

### Keywords

while

### Example

Run this code

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
enum { SIZE = 8 };
int main(void)
{
    // trivial example
    int array[SIZE], n = 0;
    while(n < SIZE) array[n++] = rand() % 2;
    puts("Array filled!");
    n = 0;
    while(n < SIZE) printf("%d ", array[n++]);
    printf("\n");
 
    // classic strcpy() implementation
    // (copies a null-terminated string from src to dst)
    char src[] = "Hello, world", dst[sizeof src], *p = dst, *q = src;
    while((*p++ = *q++)) // double parentheses (that are not strictly necessary)
                         // used to suppress warnings, ensuring that this is an
                         // assignment (as opposed to a comparison) by intention,
                         // whose result is used as a truth value
        ; // null statement
    puts(dst);
}

```

Output:

```
Array filled!
1 0 1 1 1 1 0 0 
Hello, world

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.8.5.1 The while statement (p: 109)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.8.5.1 The while statement (p: 151)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.8.5.1 The while statement (p: 136)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.6.5.1 The while statement

### See also

|  |  |
| --- | --- |
| C++ documentation for `while` loop | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/while&oldid=147751>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 February 2023, at 16:37.