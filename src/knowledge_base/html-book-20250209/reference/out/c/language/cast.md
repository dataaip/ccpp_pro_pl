# cast operator

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
| increment and decrement | | | | |
| function call, comma, conditional operator | | | | |
| sizeof | | | | |
| _Alignof(C11\*) | | | | |
| ****cast operators**** | | | | |

Performs explicit type conversion

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `(` type-name `)` expression |  |  |
|  | | | | | | | | | |

where

|  |  |  |
| --- | --- | --- |
| type-name | - | either the type void or any scalar type |
| expression | - | any expression of scalar type (unless type-name is void, in which case it can be anything) |

### Explanation

If type-name is void, then expression is evaluated for its side-effects and its returned value is discarded, same as when expression is used on its own, as an expression statement.

Otherwise, if type-name is exactly the type of expression, nothing is done (except that if expression has floating type and is represented with greater range and precision than its type indicates -- see below)

Otherwise, the value of expression is converted to the type named by type-name, as follows:

Every implicit conversion as if by assignment is allowed.

In addition to the implicit conversions, the following conversions are allowed:

- Any integer can be cast to any pointer type. Except for the null pointer constants such as NULL (which doesn't need a cast), the result is implementation-defined, may not be correctly aligned, may not point to an object of the referenced type, and may be a trap representation.
- Any pointer type can be cast to any integer type. The result is implementation-defined, even for null pointer values (they do not necessarily result in the value zero). If the result cannot be represented in the target type, the behavior is undefined (unsigned integers do not implement modulo arithmetic on a cast from pointer)
- Any pointer to object can be cast to any other pointer to object. If the value is not correctly aligned for the target type, the behavior is undefined. Otherwise, if the value is converted back to the original type, it compares equal to the original value. If a pointer to object is cast to pointer to any character type, the result points at the lowest byte of the object and may be incremented up to sizeof the target type (in other words, can be used to examine object representation or to make a copy via memcpy or memmove).
- Any pointer to function can be cast to a pointer to any other function type. If the resulting pointer is converted back to the original type, it compares equal to the original value. If the converted pointer is used to make a function call, the behavior is undefined (unless the function types are compatible)
- When casting between pointers (either object or function), if the original value is a null pointer value of its type, the result is the correct null pointer value for the target type.

In any case (both when executing an implicit conversion and in the same-type cast), if expression and type-name are floating types and expression is represented with greater range and precision than its type indicates (see FLT_EVAL_METHOD), the range and precision are stripped off to match the target type.

The value category of the cast expression is always non-lvalue.

### Notes

Because `const`, `volatile`, `restrict`, and `_Atomic` qualifiers have effect on lvalues only, a cast to a cvr-qualified or atomic type is exactly equivalent to the cast to the corresponding unqualified type.

The cast to void is sometimes useful to silence compiler warnings about unused results.

The conversions not listed here are not allowed. In particular,

- there are no conversions between pointers and floating types
- there are no conversions between pointers to functions and pointers to objects (including void\*)

|  |  |
| --- | --- |
| If the implementation provides intptr_t and/or uintptr_t, then a cast from a pointer to an object type (including **cv** void) to these types is always well-defined. However, this is not guaranteed for a function pointer. | (since C99) |

Note that conversions between function pointers and object pointers are accepted as extensions by many compilers, and expected by some usages of POSIX `dlsym()` function.

### Example

Run this code

```
#include <stdio.h>
 
int main(void)
{
    // examining object representation is a legitimate use of cast
    double d = 3.14;
    printf("The double %.2f (%a) is: ", d, d);
    for (size_t n = 0; n < sizeof d; ++n)
        printf("0x%02x ", ((unsigned char*)&d)[n]);
 
    // edge cases
    struct S { int x; } s;
//    (struct S)s; // error; not a scalar type
                   // even though casting to the same type does nothing
    (void)s; // okay to cast any type to void
}

```

Possible output:

```
The double 3.14 (0x1.91eb851eb851fp+1) is: 0x1f 0x85 0xeb 0x51 0xb8 0x1e 0x09 0x40

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.5.4 Cast operators (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 6.5.4 Cast operators (p: 65-66)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.5.4 Cast operators (p: 91)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.5.4 Cast operators (p: 81)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.3.4 Cast operators

### See also

|  |  |
| --- | --- |
| C++ documentation for explicit type conversion | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/cast&oldid=150151>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 April 2023, at 05:07.