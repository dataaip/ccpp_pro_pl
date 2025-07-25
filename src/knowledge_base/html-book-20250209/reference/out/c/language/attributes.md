# Attribute specifier sequence(since C23)

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
| typedef | | | | |
| Static assertions | | | | |
| ****Attributes**** (C23) | | | | |

 ****Attributes****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| deprecated(C23) | | | | |
| fallthrough(C23) | | | | |
| nodiscard(C23) | | | | |
| maybe_unused(C23) | | | | |
| noreturn_Noreturn(C23)(C23)(deprecated) | | | | |
| unsequenced(C23) | | | | |
| reproducible(C23) | | | | |

Introduces implementation-defined attributes for types, objects, expressions, etc.

### Syntax

:   `[[`attr ﻿`]]` `[[`attr1, attr2, attr3`(`args`)``]]` `[[`attribute-prefix`::`attr ﻿`(`args`)``]]`

Formally, the syntax is

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `[[` attribute-list `]]` |  | (since C23) |
|  | | | | | | | | | |

where attribute-list is a comma-separated sequence of zero or more attribute-token ﻿s

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| standard-attribute | (1) |  |
|  | | | | | | | | | |
| attribute-prefix `::` identifier | (2) |  |
|  | | | | | | | | | |
| standard-attribute `(` argument-list ﻿(optional) `)` | (3) |  |
|  | | | | | | | | | |
| attribute-prefix `::` identifier `(` argument-list ﻿(optional) `)` | (4) |  |
|  | | | | | | | | | |

where attribute-prefix is an identifier and argument-list is a sequence of tokens where parentheses, brackets and braces are balanced (balanced-token-sequence).

1) standard attribute, such as [[fallthrough]]2) attribute with a namespace, such as [[gnu::unused]]3) standard attribute with arguments, such as [[deprecated("reason")]]4) attribute with both a namespace and an argument list, such as [[gnu::nonnull(1)]]

### Explanation

Attributes provide the unified standard syntax for implementation-defined language extensions, such as the GNU and IBM language extensions `__attribute__((...))`, Microsoft extension `__declspec()`, etc.

An attribute can be used almost everywhere in the C program, and can be applied to almost everything: to types, to variables, to functions, to names, to code blocks, to entire translation units, although each particular attribute is only valid where it is permitted by the implementation: `[[expect_true]]` could be an attribute that can only be used with an if, and not with a class declaration. `[[omp::parallel()]]` could be an attribute that applies to a code block or to a for loop, but not to the type `int`, etc. (note these two attributes are fictional examples, see below for the standard and some non-standard attributes)

In declarations, attributes may appear both before the whole declaration and directly after the name of the entity that is declared, in which case they are combined. In most other situations, attributes apply to the directly preceding entity.

Two consecutive left square bracket tokens (`[[`) may only appear when introducing an attribute-specifier or inside an attribute argument.

Besides the standard attributes listed below, implementations may support arbitrary non-standard attributes with implementation-defined behavior. All attributes unknown to an implementation are ignored without causing an error.

Every standard-attribute is reserved for standardization. That is, every non-standard attribute is prefixed by a attribute-prefix provided by the implementation, e.g. `[[gnu::may_alias]]` and `[[clang::no_sanitize]]`.

### Standard attributes

Only the following attributes are defined by the C standard. Every standard attribute whose name is of form `attr` can be also spelled as `__attr__` and its meaning is not changed.

|  |  |
| --- | --- |
| `[[deprecated]]`(C23) `[[deprecated("reason")]]`(C23) | indicates that the use of the name or entity declared with this attribute is allowed, but discouraged for some reason (attribute specifier) |
| `[[fallthrough]]`(C23) | indicates that the fall through from the previous case label is intentional and should not be diagnosed by a compiler that warns on fall-through (attribute specifier) |
| `[[nodiscard]]`(C23) `[[nodiscard("reason")]]`(C23) | encourages the compiler to issue a warning if the return value is discarded (attribute specifier) |
| `[[maybe_unused]]`(C23) | suppresses compiler warnings on unused entities, if any (attribute specifier) |
| `[[noreturn]]`(C23) `[[_Noreturn]]`(C23)(deprecated) | indicates that the function does not return (attribute specifier) |
| `[[unsequenced]]`(C23) | indicates that a function is stateless, effectless, idempotent and independent (attribute specifier) |
| `[[reproducible]]`(C23) | indicates that a function is effectless and idempotent (attribute specifier) |

### Attribute testing

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `__has_c_attribute(` attribute-token `)` |  |  |
|  | | | | | | | | | |

Checks for the presence of an attribute token named by attribute-token.

For standard attributes, it will expand to the year and month in which the attribute was added to the working draft (see table below), the presence of vendor-specific attributes is determined by a non-zero integer constant.

`__has_c_attribute` can be expanded in the expression of #if and #elif.
It is treated as a defined macro by #ifdef, #ifndef and defined but cannot be used anywhere else.

| attribute-token | Attribute | Value | Standard |
| --- | --- | --- | --- |
| `deprecated` | `[[deprecated]]` | 201904L | (C23) |
| `fallthrough` | `[[fallthrough]]` | 201904L | (C23) |
| `maybe_unused` | `[[maybe_unused]]` | 201904L | (C23) |
| `nodiscard` | `[[nodiscard]]` | 202003L | (C23) |
| `noreturn` `_Noreturn` | `[[noreturn]]` `[[_Noreturn]]` | 202202L | (C23) |
| `unsequenced` | `[[unsequenced]]` | 202207L | (C23) |
| `reproducible` | `[[reproducible]]` | 202207L | (C23) |

### Example

Run this code

```
[[gnu::hot]] [[gnu::const]] [[nodiscard]]
int f(void); // declare f with three attributes
 
[[gnu::const, gnu::hot, nodiscard]]
int f(void); // the same as above, but uses a single attr
             // specifier that contains three attributes
 
int f(void) { return 0; }
 
int main(void)
{
}

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.7.12 Attributes (p: TBD)

### See also

|  |  |
| --- | --- |
| C++ documentation for Attribute specifier sequence | |

### External links

|  |  |
| --- | --- |
| 1. | Attributes in GCC |
| 2. | Attributes in Clang |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/attributes&oldid=178605>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 December 2024, at 14:21.