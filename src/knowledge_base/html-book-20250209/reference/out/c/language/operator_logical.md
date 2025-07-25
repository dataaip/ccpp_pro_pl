# Logical operators

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

 Expressions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| value category | | | | |
| evaluation order and sequence points | | | | |
| constant expressions | | | | |
| implicit conversions | | | | |
| generic selection (C11) | | | | |
| constants and literals | | | | |
| integer constant | | | | |
| floating constant | | | | |
| character constant | | | | |
| true/false(C23) | | | | |
| nullptr(C23) | | | | |
| string literal | | | | |
| compound literal (C99) | | | | |
| operators | | | | |
| operator precedence | | | | |
| member access and indirection | | | | |
| ****logical operators**** | | | | |
| comparison operators | | | | |
| arithmetic operators | | | | |
| assignment operators | | | | |
| increment and decrement | | | | |
| function call, comma, conditional operator | | | | |
| sizeof | | | | |
| _Alignof(C11\*) | | | | |
| cast operators | | | | |

Logical operators apply standard boolean algebra operations to their operands.

| Operator | Operator name | Example | Result |
| --- | --- | --- | --- |
| ! | logical NOT | !a | the logical negation of ****a**** |
| && | logical AND | a && b | the logical AND of ****a**** and ****b**** |
| || | logical OR | a || b | the logical OR of ****a**** and ****b**** |

### Logical NOT

The logical NOT expression has the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `!` expression |  |  |
|  | | | | | | | | | |

where

|  |  |  |
| --- | --- | --- |
| expression | - | an expression of any scalar type |

The logical NOT operator has type int. Its value is ​0​ if expression evaluates to a value that compares unequal to zero. Its value is 1 if expression evaluates to a value that compares equal to zero. (so !E is the same as (0==E))

Run this code

```
#include <stdbool.h>
#include <stdio.h>
#include <ctype.h>
int main(void)
{
    bool b = !(2+2 == 4); // not true
    printf("!(2+2==4) = %s\n", b ? "true" : "false");
 
    int n = isspace('a'); // non-zero if 'a' is a space, zero otherwise
    int x = !!n; // "bang-bang", common C idiom for mapping integers to [0,1]
                 // (all non-zero values become 1)
    char *a[2] = {"non-space", "space"};
    puts(a[x]); // now x can be safely used as an index to array of 2 strings
}

```

Output:

```
!(2+2==4) = false
non-space

```

### Logical AND

The logical AND expression has the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| lhs `&&` rhs |  |  |
|  | | | | | | | | | |

where

|  |  |  |
| --- | --- | --- |
| lhs | - | an expression of any scalar type |
| rhs | - | an expression of any scalar type, which is only evaluated if lhs does not compare equal to ​0​ |

The logical-AND operator has type int and the value 1 if both lhs and rhs compare unequal to zero. It has the value ​0​ otherwise (if either lhs or rhs or both compare equal to zero).

There is a sequence point after the evaluation of lhs. If the result of lhs compares equal to zero, then rhs is not evaluated at all (so-called **short-circuit evaluation**)

Run this code

```
#include <stdbool.h>
#include <stdio.h>
int main(void)
{
    bool b = 2+2==4 && 2*2==4; // b == true
 
    1 > 2 && puts("this won't print");
 
    char *p = "abc";
    if(p && *p) // common C idiom: if p is not null
                // AND if p does not point at the end of the string
    {           // (note that thanks to short-circuit evaluation, this
                //  will not attempt to dereference a null pointer)
    // ...      // ... then do some string processing
    }
}

```

### Logical OR

The logical OR expression has the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| lhs `||` rhs |  |  |
|  | | | | | | | | | |

where

|  |  |  |
| --- | --- | --- |
| lhs | - | an expression of any scalar type |
| rhs | - | an expression of any scalar type, which is only evaluated if lhs compares equal to ​0​ |

The logical-OR operator has type int and the value 1 if either lhs or rhs compare unequal to zero. It has value ​0​ otherwise (if both lhs and rhs compare equal to zero).

There is a sequence point after the evaluation of lhs. If the result of lhs compares unequal to zero, then rhs is not evaluated at all (so-called **short-circuit evaluation**)

Run this code

```
#include <stdbool.h>
#include <stdio.h>
#include <string.h>
#include <errno.h>
int main(void)
{
    bool b = 2+2 == 4 || 2+2 == 5; // true
    printf("true or false = %s\n", b ? "true" : "false");
 
    // logical OR can be used simialar to perl's "or die", as long as rhs has scalar type
    fopen("test.txt", "r") || printf("could not open test.txt: %s\n", strerror(errno));
}

```

Possible output:

```
true or false = true
could not open test.txt: No such file or directory

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 6.5.3.3 Unary arithmetic operators (p: 89)

:   - 6.5.13 Logical AND operator (p: 99)

:   - 6.5.14 Logical OR operator (p: 99)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.5.3.3 Unary arithmetic operators (p: 79)

:   - 6.5.13 Logical AND operator (p: 89)

:   - 6.5.14 Logical OR operator (p: 89)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.3.3.3 Unary arithmetic operators

:   - 3.3.13 Logical AND operator

:   - 3.3.14 Logical OR operator

### See Also

Operator precedence

| Common operators | | | | | | |
| --- | --- | --- | --- | --- | --- | --- |
| assignment | increment decrement | arithmetic | ****logical**** | comparison | member access | other |
| a = b  a += b  a -= b  a \*= b  a /= b  a %= b  a &= b  a |= b  a ^= b  a <<= b  a >>= b | ++a  --a  a++  a-- | +a  -a  a + b  a - b  a \* b  a / b  a % b  ~a  a & b  a | b  a ^ b  a << b  a >> b | !a  a && b  a || b | a == b  a != b  a < b  a > b  a <= b  a >= b | a[b]  \*a  &a  a->b  a.b | a(...)  a, b  (type) a  a ? b : c  sizeof   _Alignof (since C11) (until C23)   alignof (since C23) |

### See also

|  |  |
| --- | --- |
| C++ documentation for Logical operators | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/operator_logical&oldid=171168>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 April 2024, at 04:33.