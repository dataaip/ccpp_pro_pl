# Scalar initialization

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

 Initialization

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Explicit initialization | | | | |
| Implicit initialization | | | | |
| Empty initialization | | | | |
| ****Scalar initialization**** | | | | |
| Array initialization | | | | |
| Struct and union initialization | | | | |

When initializing an object of scalar type, the initializer must be a single expression

The initializer for a scalar (an object of integer type including booleans and enumerated types, floating type including complex and imaginary, and pointer type including pointer to function) must be a single expression, optionally enclosed in braces, or an empty initializer(since C23):

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `=` expression | (1) |  |
|  | | | | | | | | | |
| `=` `{` expression `}` | (2) |  |
|  | | | | | | | | | |
| `=` `{` `}` | (3) | (since C23) |
|  | | | | | | | | | |

1,2) The expression is evaluated, and its value, after conversion as if by assignment to the type of the object, becomes the initial value of the object being initialized.3) The object is empty-initialized, i.e. initialized to numeric zero for an object of an arithmetic or enumeration type, or null pointer value for an object of a pointer type.

### Notes

Because of the rules that apply to conversions as if by assignment, `const` and `volatile` qualifiers on the declared type are ignored when determining which type to convert the expression to.

See initialization for the rules that apply when no initializer is used.

As with all other initializations, expression must be a constant expression when initializing objects of static or thread-local storage duration.

The expression cannot be a comma operator (unless parenthesized) because the comma at the top level would be interpreted as the beginning of the next declarator.

When initializing objects of floating-point type, all computations for the objects with automatic storage duration are done as-if at execution time and are affected by the current rounding; floating-point errors are reported as specified in math_errhandling. For objects of static and thread-local storage duration, computations are done as-if at compile time, and no exceptions are raised:

```
void f(void)
{
#pragma STDC FENV_ACCESS ON
    static float v = 1.1e75; // does not raise exceptions: static init
 
    float u[] = { 1.1e75 }; // raises FE_INEXACT
    float w = 1.1e75;       // raises FE_INEXACT
 
    double x = 1.1e75; // may raise FE_INEXACT (depends on FLT_EVAL_METHOD)
    float y = 1.1e75f; // may raise FE_INEXACT (depends on FLT_EVAL_METHOD)
 
    long double z = 1.1e75; // does not raise exceptions (conversion is exact)
}

```

### Example

Run this code

```
#include <stdbool.h>
int main(void)
{
    bool b = true;
    const double d = 3.14;
    int k = 3.15; // conversion from double to int
    int n = {12}, // optional braces
       *p = &n,   // non-constant expression OK for automatic variable
       (*fp)(void) = main;
    enum {RED, BLUE} e = RED; // enumerations are scalar types as well
}

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.7.9/11 Initialization (p: 101)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.7.9/11 Initialization (p: 140)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.7.8/11 Initialization (p: 126)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 6.5.7 Initialization

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/scalar_initialization&oldid=139692>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 May 2022, at 08:06.