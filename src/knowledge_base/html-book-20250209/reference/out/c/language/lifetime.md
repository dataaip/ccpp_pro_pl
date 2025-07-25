# Lifetime

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
| ****Lifetime**** | | | | |
| Lookup and name spaces | | | | |
| Type | | | | |
| Arithmetic types | | | | |
| Objects and alignment | | | | |
| The main() function | | | | |
| The as-if rule | | | | |
| Undefined behavior | | | | |
| Memory model and data races | | | | |

Every object in C exists, has a constant address, retains its last-stored value (except when the value is indeterminate), and, for VLA, retains its size(since C99) over a portion of program execution known as this object's **lifetime**.

For the objects that are declared with automatic, static, and thread storage duration, lifetime equals their storage duration (note the difference between non-VLA and VLA automatic storage duration).

For the objects with allocated storage duration, the lifetime begins when the allocation function returns (including the return from realloc) and ends when the realloc or deallocation function is called. Note that since allocated objects have no declared type, the type of the lvalue expression first used to access this object becomes its effective type.

Accessing an object outside of its lifetime is undefined behavior.

```
int* foo(void) {
    int a = 17; // a has automatic storage duration
    return &a;
}  // lifetime of a ends
int main(void) {
    int* p = foo(); // p points to an object past lifetime ("dangling pointer")
    int n = *p; // undefined behavior
}

```

A pointer to an object (or one past the object) whose lifetime ended has indeterminate value.

### Temporary lifetime

Struct and union objects with array members (either direct or members of nested struct/union members) that are designated by non-lvalue expressions, have **temporary lifetime**. Temporary lifetime begins when the expression that refers to such object is evaluated and ends at the next sequence point(until C11)when the containing full expression or full declarator ends(since C11).

Any attempt to modify an object with temporary lifetime results in undefined behavior.

```
struct T { double a[4]; };
struct T f(void) { return (struct T){3.15}; }
double g1(double* x) { return *x; }
void g2(double* x) { *x = 1.0; }
int main(void)
{
    double d = g1(f().a); // C99: UB access to a[0] in g1 whose lifetime ended
                          //      at the sequence point at the start of g1
                          // C11: OK, d is 3.15
    g2(f().a); // C99: UB modification of a[0] whose lifetime ended at the sequence point
               // C11: UB attempt to modify a temporary object
}

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.2.4 Storage durations of objects (p: 30)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.2.4 Storage durations of objects (p: 38-39)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.2.4 Storage durations of objects (p: 32)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.1.2.4 Storage durations of objects

### See also

|  |  |
| --- | --- |
| C++ documentation for Object lifetime | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/lifetime&oldid=138081>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 February 2022, at 04:01.