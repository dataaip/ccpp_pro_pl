# break statement

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
| while | | | | |
| do-while | | | | |
| for | | | | |
| Jump statements | | | | |
| ****break**** | | | | |
| continue | | | | |
| return | | | | |
| goto | | | | |

Causes the enclosing for, while or do-while loop or switch statement to terminate.

Used when it is otherwise awkward to terminate the loop using the condition expression and conditional statements.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr-spec-seq ﻿(optional) `break` `;` |  |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| attr-spec-seq | - | (C23) optional list of attributes, applied to the `break` statement |

Appears only within the statement of a loop body (`while`, `do-while`, `for`) or within the statement of a `switch`.

### Explanation

After this statement the control is transferred to the statement or declaration immediately following the enclosing loop or switch, as if by `goto`.

### Keywords

break

### Notes

A break statement cannot be used to break out of multiple nested loops. The `goto` statement may be used for this purpose.

### Example

Run this code

```
#include <stdio.h>
 
int main(void)
{
    int i = 2;
    switch (i)
    {
        case 1: printf("1");
        case 2: printf("2");   // i==2, so execution starts at this case label
        case 3: printf("3");
        case 4:
        case 5: printf("45");
                break;         // execution of subsequent cases is terminated
        case 6: printf("6");
    }
    printf("\n");
 
    // Compare outputs from these two nested for loops.
    for (int j = 0; j < 2; j++)
        for (int k = 0; k < 5; k++)
            printf("%d%d ", j,k);
    printf("\n");
 
    for (int j = 0; j < 2; j++)
    {
        for (int k = 0; k < 5; k++) // only this loop is exited by break
        {
            if (k == 2)
                break;
            printf("%d%d ", j,k);
        }
    }
}

```

Possible output:

```
2345
00 01 02 03 04 10 11 12 13 14
00 01 10 11

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.8.6.3 The break statement (p: 111)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.8.6.3 The break statement (p: 153)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.8.6.3 The break statement (p: 138)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.6.6.3 The break statement

### See also

|  |  |
| --- | --- |
| `[[fallthrough]]`(C23) | indicates that the fall through from the previous case label is intentional and should not be diagnosed by a compiler that warns on fall-through (attribute specifier) |
| C++ documentation for `break` statement | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/break&oldid=155195>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 July 2023, at 07:57.