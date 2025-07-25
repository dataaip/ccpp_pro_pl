# offsetof

From cppreference.com
< c‎ | types
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

 Type support

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| size_t | | | | |
| ptrdiff_t | | | | |
| nullptr_t(C23) | | | | |
| NULL | | | | |
| max_align_t(C11) | | | | |
| ****offsetof**** | | | | |
| Numeric limits | | | | |
| Fixed width integer types (C99) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stddef.h>` |  |  |
| #define offsetof(type, member) /\*implementation-defined\*/ |  |  |
|  |  |  |

The macro ****offsetof**** expands to an integer constant expression of type size_t, the value of which is the offset, in bytes, from the beginning of an object of specified type to its specified subobject, including padding if any.

Given an object `o` of type `type` with static storage duration, &(o.member) shall be an address constant expression and point to a subobject of `o`. Otherwise, the behavior is undefined.

|  |  |
| --- | --- |
| If the type name specified in `type` contains a comma not between matching parentheses, the behavior is undefined. | (since C23) |

### Notes

If `offsetof` is applied to a bit-field member, the behavior is undefined, because the address of a bit-field cannot be taken.

`member` is not restricted to a direct member. It can denote a subobject of a given member, such as an element of an array member.

Even though it is specified in C23 that specifying a new type containing an unparenthesized comma in `offsetof` is undefined behavior, such usage is generally not supported even in earlier modes: offsetof(struct Foo { int a, b; }, a) generally fails to compile.

|  |  |
| --- | --- |
| typeof can be used to avoid the bad effect of commas in the definition of a new type, e.g. offsetof(typeof(struct { int i, j; }), i) is well-defined. | (since C23) |

### Example

Run this code

```
#include <stdio.h>
#include <stddef.h>
 
struct S {
    char c;
    double d;
};
 
int main(void)
{
    printf("the first element is at offset %zu\n", offsetof(struct S, c));
    printf("the double is at offset %zu\n", offsetof(struct S, d));
}

```

Possible output:

```
the first element is at offset 0
the double is at offset 8

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| DR 496 | C89 | only structs and struct members were mentioned | unions and other subobjects are also supported |

### See also

|  |  |
| --- | --- |
| size_t | unsigned integer type returned by the sizeof operator   (typedef) |
| C++ documentation for offsetof | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/types/offsetof&oldid=170432>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 March 2024, at 15:33.