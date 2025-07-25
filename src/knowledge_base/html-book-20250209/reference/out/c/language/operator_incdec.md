# Increment/decrement operators

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
| logical operators | | | | |
| comparison operators | | | | |
| arithmetic operators | | | | |
| assignment operators | | | | |
| ****increment and decrement**** | | | | |
| function call, comma, conditional operator | | | | |
| sizeof | | | | |
| _Alignof(C11\*) | | | | |
| cast operators | | | | |

Increment/decrement operators are unary operators that increment/decrement the value of a variable by 1.

They can have postfix form:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| expr `++` |  |  |
|  | | | | | | | | | |
| expr `--` |  |  |
|  | | | | | | | | | |

As well as the prefix form:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `++` expr |  |  |
|  | | | | | | | | | |
| `--` expr |  |  |
|  | | | | | | | | | |

The operand expr of both prefix and postfix increment or decrement must be a modifiable lvalue of integer type (including `_Bool` and enums), real floating type, or a pointer type. It may be cvr-qualified, unqualified, or atomic.

The result of the postfix increment and decrement operators is the value of expr.

The result of the prefix increment operator is the result of adding the value `1` to the value of expr: the expression ++e is equivalent to e += 1. The result of the prefix decrement operator is the result of subtracting the value `1` from the value of expr: the expression --e is equivalent to e -= 1.

Increment operators initiate the side-effect of adding the value `1` of appropriate type to the operand. Decrement operators initiate the side-effect of subtracting the value `1` of appropriate type from the operand. As with any other side-effects, these operations complete at or before the next sequence point.

```
int a = 1;
int b = a++; // stores 1+a (which is 2) to a
             // returns the old value of a (which is 1)
             // After this line, b == 1 and a == 2
a = 1;
int c = ++a; // stores 1+a (which is 2) to a
             // returns 1+a (which is 2)
             // after this line, c == 2 and a == 2

```

|  |  |
| --- | --- |
| Post-increment or post-decrement on any atomic variable is an atomic read-modify-write operation with memory order memory_order_seq_cst. | (since C11) |

See arithmetic operators for limitations on pointer arithmetic, as well as for implicit conversions applied to the operands.

### Notes

Because of the side-effects involved, increment and decrement operators must be used with care to avoid undefined behavior due to violations of sequencing rules.

Increment/decrement operators are not defined for complex or imaginary types: the usual definition of adding/subtracting the real number 1 would have no effect on imaginary types, and making it add/subtract `i` for imaginaries but `1` for complex numbers would have made it handle `0+yi` different from `yi`.

Unlike C++ (and some implementations of C), the increment/decrement expressions are never themselves lvalues: &++a is invalid.

### Example

Run this code

```
#include <stdio.h>
#include <stdlib.h>
 
int main(void)
{
    int a = 1;
    int b = 1;
 
    printf("original values: a == %d, b == %d\n", a, b);
    printf("result of postfix operators: a++ == %d, b-- == %d\n", a++, b--);
    printf("after postfix operators applied: a == %d, b == %d\n", a, b);
    printf("\n");
 
    // Reset a and b.
    a = 1;
    b = 1;
 
    printf("original values: a == %d, b == %d\n", a, b);
    printf("result of prefix operators: ++a == %d, --b == %d\n", ++a, --b);
    printf("after prefix operators applied: a == %d, b == %d\n", a, b);
}

```

Output:

```
original values: a == 1, b == 1
result of postfix operators: a++ == 1, b-- == 1
after postfix operators applied: a == 2, b == 0
 
original values: a == 1, b == 1
result of prefix operators: ++a == 2, --b == 0
after prefix operators applied: a == 2, b == 0

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.5.2.4 Postfix increment and decrement operators (p: TBD)

:   - 6.5.3.1 Prefix increment and decrement operators (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 6.5.2.4 Postfix increment and decrement operators (p: TBD)

:   - 6.5.3.1 Prefix increment and decrement operators (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.5.2.4 Postfix increment and decrement operators (p: 85)

:   - 6.5.3.1 Prefix increment and decrement operators (p: 88)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.5.2.4 Postfix increment and decrement operators (p: 75)

:   - 6.5.3.1 Prefix increment and decrement operators (p: 78)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.3.2.4 Postfix increment and decrement operators

:   - 3.3.3.1 Prefix increment and decrement operators

### See also

Operator precedence

| Common operators | | | | | | |
| --- | --- | --- | --- | --- | --- | --- |
| assignment | ****increment decrement**** | arithmetic | logical | comparison | member access | other |
| a = b  a += b  a -= b  a \*= b  a /= b  a %= b  a &= b  a |= b  a ^= b  a <<= b  a >>= b | ++a  --a  a++  a-- | +a  -a  a + b  a - b  a \* b  a / b  a % b  ~a  a & b  a | b  a ^ b  a << b  a >> b | !a  a && b  a || b | a == b  a != b  a < b  a > b  a <= b  a >= b | a[b]  \*a  &a  a->b  a.b | a(...)  a, b  (type) a  a ? b : c  sizeof   _Alignof (since C11) (until C23)   alignof (since C23) |

|  |  |
| --- | --- |
| C++ documentation for Increment/decrement operators | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/operator_incdec&oldid=153216>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 June 2023, at 10:27.