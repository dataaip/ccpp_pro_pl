# Typedef declaration

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
| constexpr(C23) | | | | |
| volatile | | | | |
| restrict(C99) | | | | |
| Alignment specifiers | | | | |
| Storage duration and linkage | | | | |
| External and tentative definitions | | | | |
| ****typedef**** | | | | |
| Static assertions | | | | |
| Attributes (C23) | | | | |

The **typedef declaration** provides a way to declare an identifier as a type alias, to be used to replace a possibly complex type name

The keyword typedef is used in a declaration, in the grammatical position of a storage-class specifier, except that it does not affect storage or linkage:

```
typedef int int_t; // declares int_t to be an alias for the type int
typedef char char_t, *char_p, (*fp)(void); // declares char_t to be an alias for char
                                           // char_p to be an alias for char*
                                           // fp to be an alias for char(*)(void)

```

### Explanation

If a declaration uses typedef as storage-class specifier, every declarator in it defines an identifier as an alias to the type specified. Since only one storage-class specifier is permitted in a declaration, typedef declaration cannot be static or extern.

typedef declaration does not introduce a distinct type, it only establishes a synonym for an existing type, thus typedef names are compatible with the types they alias. Typedef names share the name space with ordinary identifiers such as enumerators, variables and function.

|  |  |
| --- | --- |
| A typedef for a VLA can only appear at block scope. The length of the array is evaluated each time the flow of control passes over the typedef declaration, as opposed to the declaration of the array itself:   ```text void copyt(int n) {     typedef int B[n]; // B is a VLA, its size is n, evaluated now     n += 1;     B a; // size of a is n from before +=1     int b[n]; // a and b are different sizes     for (int i = 1; i < n; i++)         a[i-1] = b[i]; } ``` | (since C99) |

### Notes

typedef name may be an incomplete type, which may be completed as usual:

```
typedef int A[]; // A is int[]
A a = {1, 2}, b = {3,4,5}; // type of a is int[2], type of b is int[3]

```

typedef declarations are often used to inject names from the tag name space into the ordinary name space:

```
typedef struct tnode tnode; // tnode in ordinary name space
                            // is an alias to tnode in tag name space
struct tnode {
    int count;
    tnode *left, *right; // same as struct tnode *left, *right;
}; // now tnode is also a complete type
tnode s, *sp; // same as struct tnode s, *sp;

```

They can even avoid using the tag name space at all:

```
typedef struct { double hi, lo; } range;
range z, *zp;

```

Typedef names are also commonly used to simplify the syntax of complex declarations:

```
// array of 5 pointers to functions returning pointers to arrays of 3 ints
int (*(*callbacks[5])(void))[3];
 
// same with typedefs
typedef int arr_t[3]; // arr_t is array of 3 int
typedef arr_t* (*fp)(void); // pointer to function returning arr_t*
fp callbacks[5];

```

Libraries often expose system-dependent or configuration-dependent types as typedef names, to present a consistent interface to the users or to other library components:

```
#if defined(_LP64)
typedef int     wchar_t;
#else
typedef long    wchar_t;
#endif

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.7.8 Type definitions (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 6.7.8 Type definitions (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.7.8 Type definitions (p: 137-138)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.7.7 Type definitions (p: 123-124)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.5.6 Type definitions

### Keywords

typedef

### See also

|  |  |
| --- | --- |
| C++ documentation for `typedef` declaration | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/typedef&oldid=169928>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 February 2024, at 02:58.