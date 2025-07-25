# C attribute: unsequenced, reproducible (since C23)

From cppreference.com
< c‎ | language‎ | attributes
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
| Attributes (C23) | | | | |

 Attributes

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| deprecated(C23) | | | | |
| fallthrough(C23) | | | | |
| nodiscard(C23) | | | | |
| maybe_unused(C23) | | | | |
| noreturn_Noreturn(C23)(C23)(deprecated) | | | | |
| ****unsequenced****(C23) | | | | |
| reproducible(C23) | | | | |

Provides the compiler with information about the access of objects by a function such that certain properties of function calls can be deduced.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `[[` `unsequenced` `]]` `[[` `__unsequenced__` `]]` | (1) |  |
|  | | | | | | | | | |
| `[[` `reproducible` `]]` `[[` `__reproducible__` `]]` | (2) |  |
|  | | | | | | | | | |

1) Indicates that a function is effectless, idempotent, stateless, and independent.2) Indicates that a function is effectless and idempotent.

### Explanation

These attributes apply to a function declarator or to a type specifier that has a function type. The corresponding attribute is a property of the function type.

#### Effectless

An evaluation of a function call is effectless if any store operation
that is sequenced during the call is the modification of an object that synchronizes with the call; if additionally the operation is observable, all access to the object must be based on a unique pointer parameter of the function.

#### Idempotent

An evaluation E is idempotent if a second evaluation of E can be sequenced immediately after the original one without changing the resulting value, if any, or the observable state of the execution.

#### Stateless

A function F is stateless if any definition of an object of static or thread storage duration in F or in a function that is called by F is const but not volatile qualified.

#### Independent

A function F is independent if for any object X that is observed by a call to F
through an lvalue that is not based on a parameter of the call, all accesses to X in all calls to F during the same program execution observe the same value;
otherwise if the access is based on a pointer parameter, there shall be a unique such pointer parameter P such that any access to X shall be to an lvalue that is based on P.

An object X is observed by a function call if both synchronize, if X is not local to the call, if X has a lifetime that starts before the function call, and if an access of X is sequenced during the call; the last value of X, if any, that is stored before the call is said to be the value of X that is observed by the call.

### Notes

These attributes exist for the purpose of compiler optimization.

If a function is reproducible, multiple subsequent calls can be treated as a single call.

If a function is unsequenced, multiple subsequent calls can be treated as a single call, and the calls can be parallelized and reordered arbitrarily.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/attributes/unsequenced&oldid=168505>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 January 2024, at 21:54.