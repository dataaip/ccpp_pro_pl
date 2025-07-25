# Arithmetic operators

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
| ****arithmetic operators**** | | | | |
| assignment operators | | | | |
| increment and decrement | | | | |
| function call, comma, conditional operator | | | | |
| sizeof | | | | |
| _Alignof(C11\*) | | | | |
| cast operators | | | | |

Arithmetic operators apply standard mathematical operations to their operands.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: consider a more general-purpose ToC for this and other tables that cover multiple topics |

| Operator | Operator name | Example | Result |
| --- | --- | --- | --- |
| + | unary plus | +a | the value of ****a**** after promotions |
| - | unary minus | -a | the negative of ****a**** |
| + | addition | a + b | the addition of ****a**** and ****b**** |
| - | subtraction | a - b | the subtraction of ****b**** from ****a**** |
| \* | product | a \* b | the product of ****a**** and ****b**** |
| / | division | a / b | the division of ****a**** by ****b**** |
| % | remainder | a % b | the remainder of ****a**** divided by ****b**** |
| ~ | bitwise NOT | ~a | the bitwise NOT of ****a**** |
| & | bitwise AND | a & b | the bitwise AND of ****a**** and ****b**** |
| | | bitwise OR | a | b | the bitwise OR of ****a**** and ****b**** |
| ^ | bitwise XOR | a ^ b | the bitwise XOR of ****a**** and ****b**** |
| << | bitwise left shift | a << b | ****a**** left shifted by ****b**** |
| >> | bitwise right shift | a >> b | ****a**** right shifted by ****b**** |

### Overflows

Unsigned integer arithmetic is always performed modulo 2n  
 where n is the number of bits in that particular integer. E.g. for unsigned int, adding one to UINT_MAX gives ​0​, and subtracting one from ​0​ gives UINT_MAX.

When signed integer arithmetic operation overflows (the result does not fit in the result type), the behavior is undefined: it may wrap around according to the rules of the representation (typically 2's complement), it may trap on some platforms or due to compiler options (e.g. `-ftrapv` in GCC and Clang), or may be completely optimized out by the compiler.

#### Floating-point environment

If #pragma STDC FENV_ACCESS is set to `ON`, all floating-point arithmetic operators obey the current floating-point rounding direction and report floating-point arithmetic errors as specified in math_errhandling unless part of a static initializer (in which case floating-point exceptions are not raised and the rounding mode is to nearest)

#### Floating-point contraction

Unless #pragma STDC FP_CONTRACT is set to `OFF`, all floating-point arithmetic may be performed as if the intermediate results have infinite range and precision, that is optimizations that omit rounding errors and floating-point exceptions that would be observed if the expression was evaluated exactly as written. For example, allows the implementation of (x\*y) + z with a single fused multiply-add CPU instruction or optimization of a = x\*x\*x\*x; as tmp = x\*x; a = tmp\*tmp.

Unrelated to contracting, intermediate results of floating-point arithmetic may have range and precision that is different from the one indicated by its type, see FLT_EVAL_METHOD

### Unary arithmetic

The unary arithmetic operator expressions have the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `+` expression | (1) |  |
|  | | | | | | | | | |
| `-` expression | (2) |  |
|  | | | | | | | | | |

1) unary plus (promotion)2) unary minus (negation)

|  |  |  |
| --- | --- | --- |
| expression | - | expression of any arithmetic type |

Both unary plus and unary minus first apply integral promotions to their operand, and then

- unary plus returns the value after promotion
- unary minus returns the negative of the value after promotion (except that the negative of a NaN is another NaN)

The type of the expression is the type after promotion, and the value category is non-lvalue.

#### Notes

The unary minus invokes undefined behavior due to signed integer overflow when applied to INT_MIN, LONG_MIN, or LLONG_MIN, on typical (2's complement) platforms.

In C++, unary operator `+` can also be used with other built-in types such as arrays and functions, not so in C.

Run this code

```
#include <stdio.h>
#include <complex.h>
#include <limits.h>
 
int main(void)
{
    char c = 'a';
    printf("sizeof char: %zu sizeof int: %zu\n", sizeof c, sizeof +c);
 
    printf("-1, where 1 is signed: %d\n", -1);
 
    // Defined behavior since arithmetic is performed for unsigned integer.
    // Hence, the calculation is (-1) modulo (2 raised to n) = UINT_MAX, where n is
    // the number of bits of unsigned int. If unsigned int is 32-bit long, then this
    // gives (-1) modulo (2 raised to 32) = 4294967295
    printf("-1, where 1 is unsigned: %u\n", -1u); 
 
    // Undefined behavior because the mathematical value of -INT_MIN = INT_MAX + 1
    // (i.e. 1 more than the maximum possible value for signed int)
    //
    // printf("%d\n", -INT_MIN);
 
    // Undefined behavior because the mathematical value of -LONG_MIN = LONG_MAX + 1
    // (i.e. 1 more than the maximum possible value for signed long)
    //
    // printf("%ld\n", -LONG_MIN);
 
    // Undefined behavior because the mathematical value of -LLONG_MIN = LLONG_MAX + 1
    // (i.e. 1 more than the maximum possible value for signed long long)
    //
    // printf("%lld\n", -LLONG_MIN);
 
    double complex z = 1 + 2*I;
    printf("-(1+2i) = %.1f%+.1f\n", creal(-z), cimag(-z));
}

```

Possible output:

```
sizeof char: 1 sizeof int: 4
-1, where 1 is signed: -1
-1, where 1 is unsigned: 4294967295
-(1+2i) = -1.0-2.0

```

### Additive operators

The binary additive arithmetic operator expressions have the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| lhs `+` rhs | (1) |  |
|  | | | | | | | | | |
| lhs `-` rhs | (2) |  |
|  | | | | | | | | | |

1) addition: lhs and rhs must be one of the following

:   - both have arithmetic types, including complex and imaginary
    - one is a pointer to complete object type, the other has integer type

2) subtraction: lhs and rhs must be one of the following

:   - both have arithmetic types, including complex and imaginary
    - lhs has pointer to complete object type, rhs has integer type
    - both are pointers to complete objects of compatible types, ignoring qualifiers

#### Arithmetic addition and subtraction

If both operands have arithmetic types, then

- first, usual arithmetic conversions are performed
- then, the values of the operands after conversions are added or subtracted following the usual rules of mathematics (for subtraction, rhs is subtracted from lhs), except that

:   - if one operand is NaN, the result is NaN
    - infinity minus infinity is NaN and FE_INVALID is raised
    - infinity plus the negative infinity is NaN and FE_INVALID is raised

Complex and imaginary addition and subtraction are defined as follows (note the result type is imaginary if both operands are imaginary and complex if one operand is real and the other imaginary, as specified by the usual arithmetic conversions):

| + or - | u | iv | u + iv |
| --- | --- | --- | --- |
| x | x ± u | x ± iv | (x ± u) ± iv |
| iy | ±u + iy | i(y ± v) | ±u + i(y ± v) |
| x + iy | (x ± u) + iy | x + i(y ± v) | (x ± u) + i(y ± v) |

Run this code

```
// work in progress
// note: take part of the c/language/conversion example

```

#### Pointer arithmetic

- If the pointer `P` points at an element of an array with index `I`, then

:   - P+N and N+P are pointers that point at an element of the same array with index `I+N`
    - P-N is a pointer that points at an element of the same array with index `I-N`

The behavior is defined only if both the original pointer and the result pointer are pointing at elements of the same array or one past the end of that array. Note that executing p-1 when p points at the first element of an array is undefined behavior and may fail on some platforms.

- If the pointer `P1` points at an element of an array with index `I` (or one past the end) and `P2` points at an element of the same array with index `J` (or one past the end), then

:   - P1-P2 has the value equal to I-J and the type ptrdiff_t (which is a signed integer type, typically half as large as the size of the largest object that can be declared)

The behavior is defined only if the result fits in ptrdiff_t.

For the purpose of pointer arithmetic, a pointer to an object that is not an element of any array is treated as a pointer to the first element of an array of size 1.

Run this code

```
// work in progress
int n = 4, m = 3;
int a[n][m];     // VLA of 4 VLAs of 3 ints each
int (*p)[m] = a; // p == &a[0] 
p = p + 1;       // p == &a[1] (pointer arithmetic works with VLAs just the same)
(*p)[2] = 99;    // changes a[1][2]

```

### Multiplicative operators

The binary multiplicative arithmetic operator expressions have the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| lhs `*` rhs | (1) |  |
|  | | | | | | | | | |
| lhs `/` rhs | (2) |  |
|  | | | | | | | | | |
| lhs `%` rhs | (3) |  |
|  | | | | | | | | | |

1) multiplication. lhs and rhs must have arithmetic types2) division. lhs and rhs must have arithmetic types3) remainder. lhs and rhs must have integer types

- first, usual arithmetic conversions are performed. Then...

#### Multiplication

The binary operator \* performs multiplication of its operands (after usual arithmetic conversions) following the usual arithmetic definitions, except that

- if one operand is a NaN, the result is a NaN
- multiplication of infinity by zero gives NaN and FE_INVALID is raised
- multiplication of infinity by a nonzero gives infinity (even for complex arguments)

Because in C, any complex value with at least one infinite part is an infinity even if its other part is a NaN, the usual arithmetic rules do not apply to complex-complex multiplication. Other combinations of floating operands follow the following table:

| \* | u | iv | u + iv |
| --- | --- | --- | --- |
| x | xu | i(xv) | (xu) + i(xv) |
| iy | i(yu) | −yv | (−yv) + i(yu) |
| x + iy | (xu) + i(yu) | (−yv) + i(xv) | **special rules** |

Besides infinity handling, complex multiplication is not allowed to overflow intermediate results, except when #pragma STDC CX_LIMITED_RANGE is set to `ON`, in which case the value may be calculated as if by (x+iy)×(u+iv) = (xu-yv)+i(yu+xv), as the programmer assumes the responsibility of limiting the range of the operands and dealing with the infinities.

Despite disallowing undue overflow, complex multiplication may raise spurious floating-point exceptions (otherwise it is prohibitively difficult to implement non-overflowing versions)

Run this code

```
#include <stdio.h>
#include <stdio.h>
#include <complex.h>
#include <math.h>
int main(void)
{
 
 
// TODO simpler cases, take some from C++
 
 
   double complex z = (1 + 0*I) * (INFINITY + I*INFINITY);
// textbook formula would give
// (1+i0)(∞+i∞) ⇒ (1×∞ – 0×∞) + i(0×∞+1×∞) ⇒ NaN + I*NaN
// but C gives a complex infinity
   printf("%f + i*%f\n", creal(z), cimag(z));
 
// textbook formula would give
// cexp(∞+iNaN) ⇒ exp(∞)×(cis(NaN)) ⇒ NaN + I*NaN
// but C gives  ±∞+i*nan
   double complex y = cexp(INFINITY + I*NAN);
   printf("%f + i*%f\n", creal(y), cimag(y));
 
}

```

Possible output:

```
inf + i*inf 
inf + i*nan

```

#### Division

The binary operator `/` divides the first operand by the second (after usual arithmetic conversions) following the usual arithmetic definitions, except that

- when the type after usual arithmetic conversions is an integer type, the result is the algebraic quotient (not a fraction), rounded in implementation-defined direction(until C99)truncated towards zero(since C99)
- if one operand is a NaN, the result is a NaN
- if the first operand is a complex infinity and the second operand is finite, then the result of the `/` operator is a complex infinity
- if the first operand is finite and the second operand is a complex infinity, then the result of the `/` operator is a zero.

Because in C, any complex value with at least one infinite part as an infinity even if its other part is a NaN, the usual arithmetic rules do not apply to complex-complex division. Other combinations of floating operands follow the following table:

| / | u | iv |
| --- | --- | --- |
| x | x/u | i(−x/v) |
| iy | i(y/u) | y/v |
| x + iy | (x/u) + i(y/u) | (y/v) + i(−x/v) |

Besides infinity handling, complex division is not allowed to overflow intermediate results, except when #pragma STDC CX_LIMITED_RANGE is set to `ON`, in which case the value may be calculated as if by (x+iy)/(u+iv) = [(xu+yv)+i(yu-xv)]/(u2  
+v2  
), as the programmer assumes the responsibility of limiting the range of the operands and dealing with the infinities.

Despite disallowing undue overflow, complex division may raise spurious floating-point exceptions (otherwise it is prohibitively difficult to implement non-overflowing versions)

If the second operand is zero, the behavior is undefined, except that if the IEEE floating-point arithmetic is supported, and the floating-point division is taking place, then

- Dividing a non-zero number by ±0.0 gives the correctly-signed infinity and FE_DIVBYZERO is raised
- Dividing 0.0 by 0.0 gives NaN and FE_INVALID is raised

#### Remainder

The binary operator % yields the remainder of the division of the first operand by the second (after usual arithmetic conversions).

The sign of the remainder is defined in such a way that if the quotient `a/b` is representable in the result type, then (a/b)\*b + a%b == a.

If the second operand is zero, the behavior is undefined.

If the quotient `a/b` is not representable in the result type, the behavior of both `a/b` and `a%b` is undefined (that means INT_MIN%-1 is undefined on 2's complement systems)

Note: the remainder operator does not work on floating-point types, the library function fmod provides that functionality.

### Bitwise logic

The bitwise arithmetic operator expressions have the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `~` rhs | (1) |  |
|  | | | | | | | | | |
| lhs `&` rhs | (2) |  |
|  | | | | | | | | | |
| lhs `|` rhs | (3) |  |
|  | | | | | | | | | |
| lhs `^` rhs | (4) |  |
|  | | | | | | | | | |

1) bitwise NOT2) bitwise AND3) bitwise OR4) bitwise XOR

where

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | expressions of integer type |

First, operators &, ^, and | perform usual arithmetic conversions on both operands and the operator ~ performs integer promotions on its only operand.

Then, the corresponding binary logic operators are applied bitwise; that is, each bit of the result is set or cleared according to the logic operation (NOT, AND, OR, or XOR), applied to the corresponding bits of the operands.

Note: bitwise operators are commonly used to manipulate bit sets and bit masks.

Note: for unsigned types (after promotion), the expression ~E is equivalent to the maximum value representable by the result type minus the original value of E.

Run this code

```
#include <stdio.h>
#include <stdint.h>
 
int main(void)
{
    uint32_t a = 0x12345678;
    uint16_t mask = 0x00f0;
 
    printf("Promoted mask:\t%#010x\n"
           "Value:\t\t%#x\n"
           "Setting bits:\t%#x\n"
           "Clearing bits:\t%#x\n"
           "Selecting bits:\t%#010x\n"
           , mask
           , a
           , a | mask
           , a & ~mask
           , a & mask
    );
}

```

Possible output:

```
Promoted mask:  0x000000f0
Value:          0x12345678
Setting bits:   0x123456f8
Clearing bits:  0x12345608
Selecting bits: 0x00000070

```

### Shift operators

The bitwise shift operator expressions have the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| lhs `<<` rhs | (1) |  |
|  | | | | | | | | | |
| lhs `>>` rhs | (2) |  |
|  | | | | | | | | | |

1) left shift of lhs by rhs bits2) right shift of lhs by rhs bits

where

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | expressions of integer type |

First, integer promotions are performed, individually, on each operand (Note: this is unlike other binary arithmetic operators, which all perform usual arithmetic conversions). The type of the result is the type of lhs after promotion.

The behavior is undefined if rhs is negative or is greater or equal the number of bits in the promoted lhs.

For unsigned lhs, the value of `LHS << RHS` is the value of LHS \* 2RHS  
, reduced modulo maximum value of the return type plus 1 (that is, bitwise left shift is performed and the bits that get shifted out of the destination type are discarded). For signed lhs with nonnegative values, the value of `LHS << RHS` is LHS \* 2RHS  
 if it is representable in the promoted type of lhs, otherwise the behavior is undefined.

For unsigned lhs and for signed lhs with nonnegative values, the value of `LHS >> RHS` is the integer part of LHS / 2RHS  
. For negative `LHS`, the value of `LHS >> RHS` is implementation-defined where in most implementations, this performs arithmetic right shift (so that the result remains negative). Thus in most implementations, right shifting a signed `LHS` fills the new higher-order bits with the original sign bit (i.e. with 0 if it was non-negative and 1 if it was negative).

Run this code

```
#include <stdio.h>
enum {ONE=1, TWO=2};
int main(void)
{
    char c = 0x10;
    unsigned long long ulong_num = 0x123;
    printf("0x123 << 1  = %#llx\n"
           "0x123 << 63 = %#llx\n"   // overflow truncates high bits for unsigned numbers
           "0x10  << 10 = %#x\n",    // char is promoted to int
           ulong_num << 1, ulong_num << 63, c << 10);
    long long long_num = -1000;
    printf("-1000 >> 1 = %lld\n", long_num >> ONE);  // implementation defined
}

```

Possible output:

```
0x123 << 1  = 0x246
0x123 << 63 = 0x8000000000000000
0x10  << 10 = 0x4000
-1000 >> 1 = -500

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.5.3.3 Unary arithmetic operators (p: 64)

:   - 6.5.5 Multiplicative operators (p: 66)

:   - 6.5.6 Additive operators (p: 66-68)

:   - 6.5.7 Bitwise shift operators (p: 68)

:   - 6.5.10 Bitwise AND operator (p: 70)

:   - 6.5.11 Bitwise exclusive OR operator (p: 70)

:   - 6.5.12 Bitwise inclusive OR operator (p: 70-71)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.5.3.3 Unary arithmetic operators (p: 89)

:   - 6.5.5 Multiplicative operators (p: 92)

:   - 6.5.6 Additive operators (p: 92-94)

:   - 6.5.7 Bitwise shift operators (p: 94-95)

:   - 6.5.10 Bitwise AND operator (p: 97)

:   - 6.5.11 Bitwise exclusive OR operator (p: 98)

:   - 6.5.12 Bitwise inclusive OR operator (p: 98)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.5.3.3 Unary arithmetic operators (p: 79)

:   - 6.5.5 Multiplicative operators (p: 82)

:   - 6.5.6 Additive operators (p: 82-84)

:   - 6.5.7 Bitwise shift operators (p: 84-85)

:   - 6.5.10 Bitwise AND operator (p: 87)

:   - 6.5.11 Bitwise exclusive OR operator (p: 88)

:   - 6.5.12 Bitwise inclusive OR operator (p: 88)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.3.3.3 Unary arithmetic operators

:   - 3.3.5 Multiplicative operators

:   - 3.3.6 Additive operators

:   - 3.3.7 Bitwise shift operators

:   - 3.3.10 Bitwise AND operator

:   - 3.3.11 Bitwise exclusive OR operator

:   - 3.3.12 Bitwise inclusive OR operator

### See also

Operator precedence

| Common operators | | | | | | |
| --- | --- | --- | --- | --- | --- | --- |
| assignment | increment decrement | ****arithmetic**** | logical | comparison | member access | other |
| a = b  a += b  a -= b  a \*= b  a /= b  a %= b  a &= b  a |= b  a ^= b  a <<= b  a >>= b | ++a  --a  a++  a-- | +a  -a  a + b  a - b  a \* b  a / b  a % b  ~a  a & b  a | b  a ^ b  a << b  a >> b | !a  a && b  a || b | a == b  a != b  a < b  a > b  a <= b  a >= b | a[b]  \*a  &a  a->b  a.b | a(...)  a, b  (type) a  a ? b : c  sizeof   _Alignof (since C11) (until C23)   alignof (since C23) |

|  |  |
| --- | --- |
| C++ documentation for Arithmetic operators | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/operator_arithmetic&oldid=176253>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 September 2024, at 09:31.