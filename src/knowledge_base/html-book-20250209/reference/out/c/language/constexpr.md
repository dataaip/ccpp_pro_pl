# constexpr specifier (since C23)

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

 Declarations

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Pointer | | | | |
| Array | | | | |
| enum | | | | |
| struct | | | | |
| union | | | | |
| Bit-field | | | | |
| Atomic types (C11) | | | | |
| const | | | | |
| ****constexpr****(C23) | | | | |
| volatile | | | | |
| restrict(C99) | | | | |
| Alignment specifiers | | | | |
| Storage duration and linkage | | | | |
| External and tentative definitions | | | | |
| typedef | | | | |
| Static assertions | | | | |
| Attributes (C23) | | | | |

A scalar object declared with the `constexpr` storage-class specifier is a constant. It must be fully and explicitly initialized according to the static initialization rules. It still has linkage appropriate to its declaration and it exist at runtime to have its address taken; it simply cannot be modified at runtime in any way, i.e. the compiler can use its knowledge of the object’s fixed value in any other constant expression.

Additionally, the constant expression that is used for the initializer of such a constant is checked at compile time.

An initializer of floating-point type must be evaluated with the translation-time floating-point environment.

There are some restrictions on the type of an object that can be declared with `constexpr`. Namely, the following constructs are not allowed to be `constexpr`:

- Pointers (except that null pointers can be `constexpr`),
- Variably modified types,
- Atomic types,
- `volatile` types,
- `restrict` pointers.

### Keywords

constexpr

### Notes

### Example

Run this code

```
#include <fenv.h>
#include <stdio.h>
 
int main(void)
{
    constexpr float f = 23.0f;
    constexpr float g = 33.0f;
    fesetround(FE_TOWARDZERO);
    constexpr float h = f / g; // is not affected by fesetround() above
    printf("%f\n", h);
}

```

Output:

```
0.696969

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - TBD TBD (p: TBD)

### See also

|  |  |
| --- | --- |
| C++ documentation for `constexpr` type specifier | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/constexpr&oldid=164881>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 December 2023, at 10:20.