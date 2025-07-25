# Assignment operators

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
| ****assignment operators**** | | | | |
| increment and decrement | | | | |
| function call, comma, conditional operator | | | | |
| sizeof | | | | |
| _Alignof(C11\*) | | | | |
| cast operators | | | | |

Assignment and compound assignment operators are binary operators that modify the variable to their left using the value to their right.

| Operator | Operator name | Example | Description | Equivalent of |
| --- | --- | --- | --- | --- |
| = | basic assignment | a = b | ****a**** becomes equal to ****b**** | N/A |
| += | addition assignment | a += b | ****a**** becomes equal to the addition of ****a**** and ****b**** | a = a + b |
| -= | subtraction assignment | a -= b | ****a**** becomes equal to the subtraction of ****b**** from ****a**** | a = a - b |
| \*= | multiplication assignment | a \*= b | ****a**** becomes equal to the product of ****a**** and ****b**** | a = a \* b |
| /= | division assignment | a /= b | ****a**** becomes equal to the division of ****a**** by ****b**** | a = a / b |
| %= | modulo assignment | a %= b | ****a**** becomes equal to the remainder of ****a**** divided by ****b**** | a = a % b |
| &= | bitwise AND assignment | a &= b | ****a**** becomes equal to the bitwise AND of ****a**** and ****b**** | a = a & b |
| |= | bitwise OR assignment | a |= b | ****a**** becomes equal to the bitwise OR of ****a**** and ****b**** | a = a | b |
| ^= | bitwise XOR assignment | a ^= b | ****a**** becomes equal to the bitwise XOR of ****a**** and ****b**** | a = a ^ b |
| <<= | bitwise left shift assignment | a <<= b | ****a**** becomes equal to ****a**** left shifted by ****b**** | a = a << b |
| >>= | bitwise right shift assignment | a >>= b | ****a**** becomes equal to ****a**** right shifted by ****b**** | a = a >> b |

### Simple assignment

The simple assignment operator expressions have the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| lhs `=` rhs |  |  |
|  | | | | | | | | | |

where

|  |  |  |
| --- | --- | --- |
| lhs | - | modifiable lvalue expression of any complete object type |
| rhs | - | expression of any type implicitly convertible to lhs or compatible with lhs |

Assignment performs implicit conversion from the value of rhs to the type of lhs and then replaces the value in the object designated by lhs with the converted value of rhs.

Assignment also returns the same value as what was stored in `lhs` (so that expressions such as a = b = c are possible). The value category of the assignment operator is non-lvalue (so that expressions such as (a=b)=c are invalid).

rhs and lhs must satisfy one of the following:

- both lhs and rhs have compatible struct or union type, or..
- rhs must be implicitly convertible to lhs, which implies

:   - both lhs and rhs have arithmetic types, in which case lhs may be volatile-qualified or atomic(since C11)
    - both lhs and rhs have pointer to compatible (ignoring qualifiers) types, or one of the pointers is a pointer to void, and the conversion would not add qualifiers to the pointed-to type. lhs may be volatile or restrict(since C99)-qualified or atomic(since C11).
    - lhs is a (possibly qualified or atomic(since C11)) pointer and rhs is a null pointer constant such as NULL or a nullptr_t value(since C23)

|  |  |
| --- | --- |
| - lhs has type (possibly qualified or atomic(since C11)) _Bool and rhs is a pointer or a nullptr_t value(since C23) | (since C99) |

|  |  |
| --- | --- |
| - lhs has type (possibly qualified or atomic) nullptr_t and rhs has type nullptr_t | (since C23) |

#### Notes

If rhs and lhs overlap in memory (e.g. they are members of the same union), the behavior is undefined unless the overlap is exact and the types are compatible.

Although arrays are not assignable, an array wrapped in a struct is assignable to another object of the same (or compatible) struct type.

The side effect of updating lhs is sequenced after the value computations, but not the side effects of lhs and rhs themselves and the evaluations of the operands are, as usual, unsequenced relative to each other (so the expressions such as i=++i; are undefined)

Assignment strips extra range and precision from floating-point expressions (see FLT_EVAL_METHOD).

In C++, assignment operators are lvalue expressions, not so in C.

Run this code

```
#include <stdio.h>
 
int main(void)
{
    // integers
    int i = 1, j = 2, k = 3; // initialization, not assignment
 
    i = j = k;   // values of i and j are now 3
//  (i = j) = k; // Error: lvalue required
    printf("%d %d %d\n", i, j, k);
 
    // pointers
    const char c = 'A'; // initialization; not assignment
    const char *p = &c;  // initialization; not assignment
    const char **cpp = &p; // initialization; not assignment
 
//  cpp = &p;   // Error: char** is not convertible to const char**
    *cpp = &c;  // OK, char* is convertible to const char*
    printf("%c \n", **cpp);
    cpp = 0;    // OK, null pointer constant is convertible to any pointer
 
    // arrays
    int arr1[2] = {1,2}, arr2[2] = {3, 4};
//  arr1 = arr2; // Error: cannot assign to an array
    printf("arr1[0]=%d arr1[1]=%d arr2[0]=%d arr2[1]=%d\n",
            arr1[0],   arr1[1],   arr2[0],   arr2[1]);
 
    struct { int arr[2]; } sam1 = { {5, 6} }, sam2 = { {7, 8} };
    sam1 = sam2; // OK: can assign arrays wrapped in structs
 
    printf("%d %d \n", sam1.arr[0], sam1.arr[1]);
}

```

Output:

```
3 3 3
A
arr1[0]=1 arr1[1]=2 arr2[0]=3 arr2[1]=4
7 8

```

### Compound assignment

The compound assignment operator expressions have the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| lhs op rhs |  |  |
|  | | | | | | | | | |

where

|  |  |  |
| --- | --- | --- |
| op | - | one of \*=, /= %=, += -=, <<=, >>=, &=, ^=, |= |
| lhs, rhs | - | expressions with arithmetic types (where lhs may be qualified or atomic), except when op is += or -=, which also accept pointer types with the same restrictions as + and - |

The expression lhs @= rhs is exactly the same as lhs `=` lhs @ `(` rhs `)`, except that lhs is evaluated only once.

|  |  |
| --- | --- |
| If lhs has atomic type, the operation behaves as a single atomic read-modify-write operation with memory order memory_order_seq_cst.  For integer atomic types, the compound assignment @= is equivalent to:   ```text T1* addr = &lhs; T2 val = rhs; T1 old = *addr; T1 new; do { new = old @ val } while (!atomic_compare_exchange_strong(addr, &old, new); ``` | (since C11) |

Run this code

```
#include <stdio.h>
 
int main(void)
{
    int x = 10; 
    int hundred = 100; 
    int ten = 10; 
    int fifty = 50; 
 
    printf("%d %d %d %d\n", x, hundred, ten, fifty);
 
    hundred *= x; 
    ten     /= x; 
    fifty   %= x; 
 
    printf("%d %d %d %d\n", x, hundred, ten, fifty);
 
    return 0;
}

```

Output:

```
10 100 10 50
10 1000 1 0

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.5.16 Assignment operators (p: 72-73)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.5.16 Assignment operators (p: 101-104)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.5.16 Assignment operators (p: 91-93)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.3.16 Assignment operators

### See Also

Operator precedence

| Common operators | | | | | | |
| --- | --- | --- | --- | --- | --- | --- |
| ****assignment**** | increment decrement | arithmetic | logical | comparison | member access | other |
| a = b  a += b  a -= b  a \*= b  a /= b  a %= b  a &= b  a |= b  a ^= b  a <<= b  a >>= b | ++a  --a  a++  a-- | +a  -a  a + b  a - b  a \* b  a / b  a % b  ~a  a & b  a | b  a ^ b  a << b  a >> b | !a  a && b  a || b | a == b  a != b  a < b  a > b  a <= b  a >= b | a[b]  \*a  &a  a->b  a.b | a(...)  a, b  (type) a  a ? b : c  sizeof   _Alignof (since C11) (until C23)   alignof (since C23) |

### See also

|  |  |
| --- | --- |
| C++ documentation for Assignment operators | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/operator_assignment&oldid=142209>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 August 2022, at 08:36.