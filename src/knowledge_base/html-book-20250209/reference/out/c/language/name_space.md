# Lookup and name spaces

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

 Basic Concepts

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Comments | | | | |
| ASCII | | | | |
| Character sets | | | | |
| Translation phases | | | | |
| Punctuation | | | | |
| Identifier | | | | |
| Scope | | | | |
| Lifetime | | | | |
| ****Lookup and name spaces**** | | | | |
| Type | | | | |
| Arithmetic types | | | | |
| Objects and alignment | | | | |
| The main() function | | | | |
| The as-if rule | | | | |
| Undefined behavior | | | | |
| Memory model and data races | | | | |

When an identifier is encountered in a C program, a lookup is performed to locate the declaration that introduced that identifier and that is currently in scope. C allows more than one declaration for the same identifier to be in scope simultaneously if these identifiers belong to different categories, called **name spaces**:

1) Label name space: all identifiers declared as labels.2) Tag names: all identifiers declared as names of structs, unions and enumerated types. Note that all three kinds of tags share one name space.3) Member names: all identifiers declared as members of any one struct or union. Every struct and union introduces its own name space of this kind.

|  |  |
| --- | --- |
| 4) Global attribute name space: attribute tokens defined by the standard or implementation-defined attribute prefixes.5) Non-standard attribute names: attribute names following attribute prefixes. Each attribute prefix has a separate name space for the implementation-defined attributes it introduces. | (since C23) |

6) All other identifiers, called **ordinary identifiers** to distinguish from (1-5) (function names, object names, typedef names, enumeration constants).

At the point of lookup, the name space of an identifier is determined by the manner in which it is used:

1) identifier appearing as the operand of a goto statement is looked up in the label name space.2) identifier that follows the keyword struct, union, or enum is looked up in the tag name space.3) identifier that follows the member access or member access through pointer operator is looked up in the name space of members of the type determined by the left-hand operand of the member access operator.

|  |  |
| --- | --- |
| 4) identifier that directly appears in an attribute specifier ([[...]]) is looked up in the global attribute name space.5) identifier that follows the :: token following an attribute prefix is looked in the name space introduced by the attribute prefix. | (since C23) |

6) all other identifiers are looked up in the name space of ordinary identifiers.

### Notes

The names of macros are not part of any name space because they are replaced by the preprocessor prior to semantic analysis.

It is common practice to inject struct/union/enum names into the name space of the ordinary identifiers using a typedef declaration:

```
struct A { };       // introduces the name A in tag name space
typedef struct A A; // first, lookup for A after "struct" finds one in tag name space
                    // then introduces the name A in the ordinary name space
struct A* p;        // OK, this A is looked up in the tag name space
A* q;               // OK, this A is looked up in the ordinary name space

```

A well-known example of the same identifier being used across two name spaces is the identifier stat from the POSIX header `sys/stat.h`. It names a function when used as an ordinary identifier and indicates a struct when used as a tag.

Unlike in C++, enumeration constants are not struct members, and their name space is the name space of ordinary identifiers, and since there is no struct scope in C, their scope is the scope in which the struct declaration appears:

```
struct tagged_union {
   enum {INT, FLOAT, STRING} type;
   union {
      int integer;
      float floating_point;
      char *string;
   };
} tu;
 
tu.type = INT; // OK in C, error in C++

```

|  |  |
| --- | --- |
| If a standard attribute, an attribute prefix, or a non-standard attribute name is not supported, the invalid attribute itself is ignored without causing an error. | (since C23) |

### Example

Run this code

```
void foo (void) { return; } // ordinary name space, file scope
struct foo {      // tag name space, file scope
    int foo;      // member name space for this struct foo, file scope
    enum bar {    // tag name space, file scope
        RED       // ordinary name space, file scope
    } bar;        // member name space for this struct foo, file scope
    struct foo* p; // OK: uses tag/file scope name "foo"
};
enum bar x; // OK: uses tag/file-scope bar
// int foo; // Error: ordinary name space foo already in scope 
//union foo { int a, b; }; // Error: tag name space foo in scope
 
int main(void)
{
    goto foo; // OK uses "foo" from label name space/function scope
 
    struct foo { // tag name space, block scope (hides file scope)
       enum bar x; // OK, uses "bar" from tag name space/file scope
    };
    typedef struct foo foo; // OK: uses foo from tag name space/block scope
                            // defines block-scope ordinary foo (hides file scope)
    (foo){.x=RED}; // uses ordinary/block-scope foo and ordinary/file-scope RED
 
foo:; // label name space, function scope
}

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.2.3 Name spaces of identifiers (p: 29-30)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.2.3 Name spaces of identifiers (p: 37)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.2.3 Name spaces of identifiers (p: 31)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.1.2.3 Name spaces of identifiers

### See also

|  |  |
| --- | --- |
| C++ documentation for Name lookup | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/name_space&oldid=136120>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 December 2021, at 03:53.