# `reinterpret_cast` conversion

From cppreference.com
< cpp‎ | language
C++

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Freestanding and hosted | | | | |
| Language | | | | |
| Standard library | | | | |
| Standard library headers | | | | |
| Named requirements | | | | |
| Feature test macros (C++20) | | | | |
| Language support library | | | | |
| Concepts library (C++20) | | | | |
| Diagnostics library | | | | |
| Memory management library | | | | |
| Metaprogramming library (C++11) | | | | |
| General utilities library | | | | |
| Containers library | | | | |
| Iterators library | | | | |
| Ranges library (C++20) | | | | |
| Algorithms library | | | | |
| Strings library | | | | |
| Text processing library | | | | |
| Numerics library | | | | |
| Date and time library | | | | |
| Input/output library | | | | |
| Filesystem library (C++17) | | | | |
| Concurrency support library (C++11) | | | | |
| Execution support library (C++26) | | | | |
| Technical specifications | | | | |
| Symbols index | | | | |
| External libraries | | | | |

C++ language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General topics | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Preprocessor | | | | | | Comments | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Keywords | | | | | | Escape sequences | | | | | |
| Flow control | | | | |
| Conditional execution statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | switch | | | | | |
| Iteration statements (loops) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | for | | | | | | range-`for` (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | while | | | | | | `do-while` | | | | | |
| Jump statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | continue - break | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | goto - return | | | | | |
| Functions | | | | |
| Function declaration | | | | |
| Lambda function expression | | | | |
| `inline` specifier | | | | |
| Dynamic exception specifications (until C++17\*) | | | | |
| `noexcept` specifier (C++11) | | | | |
| Exceptions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `throw`-expression | | | | | | `try` block | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | `catch` handler | | | | | |
| Namespaces | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace declaration | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace aliases | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Fundamental types | | | | | | Enumeration types | | | | | | Function types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class/struct types | | | | | | Union types | | | | | |  | | | | | |
| Specifiers | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const`/`volatile` | | | | | | decltype (C++11) | | | | | | auto (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | constexpr (C++11) | | | | | | consteval (C++20) | | | | | | constinit (C++20) | | | | | |
| Storage duration specifiers | | | | |
| Initialization | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default-initialization | | | | | | Value-initialization | | | | | | Zero-initialization | | | | | | Copy-initialization | | | | | | Direct-initialization | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Aggregate initialization | | | | | | List-initialization (C++11) | | | | | | Constant initialization | | | | | | Reference initialization | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Expressions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Operators | | | | | | Operator precedence | | | | | |
| Alternative representations | | | | |
| Literals | | | | |
| Boolean - Integer - Floating-point | | | | |
| Character - String - nullptr (C++11) | | | | |
| User-defined (C++11) | | | | |
| Utilities | | | | |
| Attributes (C++11) | | | | |
| Types | | | | |
| `typedef` declaration | | | | |
| Type alias declaration (C++11) | | | | |
| Casts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | static_cast | | | | | | const_cast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Explicit conversions | | | | | | dynamic_cast | | | | | | ****reinterpret_cast**** | | | | | |
| Memory allocation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `new` expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `delete` expression | | | | | |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class declaration | | | | | | Constructors | | | | | | `this` pointer | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Access specifiers | | | | | | `friend` specifier | | | | | |  | | | | | |
| Class-specific function properties | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Virtual function | | | | | | `override` specifier (C++11) | | | | | | `final` specifier (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | explicit (C++11) | | | | | | static | | | | | |  | | | | | |
| Special member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default constructor | | | | | | Copy constructor | | | | | | Move constructor (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Copy assignment | | | | | | Move assignment (C++11) | | | | | | Destructor | | | | | |
| Templates | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

 Expressions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | Constant expressions | | | | | | Primary expressions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lambda expressions (C++11) | | | | | | Requires expressions (C++20) | | | | | | Pack indexing expression (C++26) | | | | | | Potentially-evaluated expressions | | | | | |
| Literals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Integer literals | | | | | | Floating-point literals | | | | | | Boolean literals | | | | | | Character literals | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Escape sequences | | | | | | String literals | | | | | | Null pointer literal (C++11) | | | | | | User-defined literal (C++11) | | | | | |
| Operators | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | ****`reinterpret_cast`**** | | | | | |

Converts between types by reinterpreting the underlying bit pattern.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `reinterpret_cast<` target-type `>(` expression `)` |  |  |
|  | | | | | | | | | |

Returns a value of type target-type.

### Explanation

Unlike static_cast, but like const_cast, the reinterpret_cast expression does not compile to any CPU instructions (except when converting between integers and pointers, or between pointers on obscure architectures where pointer representation depends on its type). It is primarily a compile-time directive which instructs the compiler to treat expression as if it had the type target-type.

Only the following conversions can be done with reinterpret_cast, except when such conversions would cast away constness (or volatility).

1) An expression of integral, enumeration, pointer, or pointer-to-member type can be converted to its own type. The resulting value is the same as the value of expression.2) A pointer can be converted to any integral type large enough to hold all values of its type (e.g. to std::uintptr_t).3) A value of any integral or enumeration type can be converted to a pointer type. A pointer converted to an integer of sufficient size and back to the same pointer type is guaranteed to have its original value, otherwise the resulting pointer cannot be dereferenced safely (the round-trip conversion in the opposite direction is not guaranteed; the same pointer may have multiple integer representations) The null pointer constant NULL or integer zero is not guaranteed to yield the null pointer value of the target type; `static_cast` or implicit conversion should be used for this purpose.

|  |  |
| --- | --- |
| 4) Any value of type std::nullptr_t, including nullptr can be converted to any integral type as if it were (void\*)0, but no value, not even nullptr can be converted to std::nullptr_t: static_cast should be used for that purpose. | (since C++11) |

5) Any object pointer type `T1*` can be converted to another object pointer type `cv T2*`. This is exactly equivalent to static_cast<**cv** T2\*>(static_cast<**cv** void\*>(expression)) (which implies that if `T2`'s alignment requirement is not stricter than `T1`'s, the value of the pointer does not change and conversion of the resulting pointer back to its original type yields the original value). In any case, the resulting pointer may only be dereferenced safely if the dereferenced value is type-accessible.6) An lvalue(until C++11)glvalue(since C++11) expression of type `T1` can be converted to reference to another type `T2`. The result is that of \*reinterpret_cast<T2\*>(p), where p is a pointer of type “pointer to `T1`” to the object or function designated by expression. No temporary is materialized or(since C++17) created, no copy is made, no constructors or conversion functions are called. The resulting reference can only be accessed safely if it is type-accessible.7) Any pointer to function can be converted to a pointer to a different function type. The result is unspecified, but converting such pointer back to pointer to the original function type yields the pointer to the original function. The resulting pointer can only be called safely if it function type is call-compatible with the original function type.8) On some implementations (in particular, on any POSIX compatible system as required by `dlsym`), a function pointer can be converted to void\* or any other object pointer, or vice versa. If the implementation supports conversion in both directions, conversion to the original type yields the original value, otherwise the resulting pointer cannot be dereferenced or called safely.9) The null pointer value of any pointer type can be converted to any other pointer type, resulting in the null pointer value of that type. Note that the null pointer constant nullptr or any other value of type std::nullptr_t cannot be converted to a pointer with reinterpret_cast: implicit conversion or static_cast should be used for this purpose.10) A pointer to member function can be converted to pointer to a different member function of a different type. Conversion back to the original type yields the original value, otherwise the resulting pointer cannot be used safely.11) A pointer to member object of some class `T1` can be converted to a pointer to another member object of another class `T2`. If `T2`'s alignment is not stricter than `T1`'s, conversion back to the original type `T1` yields the original value, otherwise the resulting pointer cannot be used safely.

As with all cast expressions, the result is:

- an lvalue if target-type is an lvalue reference type or an rvalue reference to function type(since C++11);

|  |  |
| --- | --- |
| - an xvalue if target-type is an rvalue reference to object type; | (since C++11) |

- a prvalue otherwise.

### Type aliasing

#### Type accessibility

If a type `T_ref` is similar to any of the following types, an object of dynamic type `T_obj` is **type-accessible** through a lvalue(until C++11)glvalue(since C++11) of type `T_ref`:

- char
- unsigned char

|  |  |
| --- | --- |
| - std::byte | (since C++17) |

- `T_obj`
- the signed or unsigned type corresponding to `T_obj`

If a program attempts to read or modify the stored value of an object through a lvalue(until C++11)glvalue(since C++11) through which it is not type-accessible, the behavior is undefined.

This rule enables type-based alias analysis, in which a compiler assumes that the value read through a glvalue of one type is not modified by a write to a glvalue of a different type (subject to the exceptions noted above).

Note that many C++ compilers relax this rule, as a non-standard language extension, to allow wrong-type access through the inactive member of a union (such access is not undefined in C).

#### Call compatibility

If any of the following conditions is satisfied, a type `T_call` is **call-compatible** with a function type `T_func`:

- `T_call` is the same type as `T_func`.

|  |  |
| --- | --- |
| - `T_func*` can be converted to `T_call*` via a function pointer conversion. | (since C++17) |

If a function is called through an expression whose function type is not call-compatible with the type of the called function’s definition, the behavior is undefined.

### Notes

Assuming that alignment requirements are met, a reinterpret_cast does not change the value of a pointer outside of a few limited cases dealing with **pointer-interconvertible** objects:

```
struct S1 { int a; } s1;
struct S2 { int a; private: int b; } s2; // not standard-layout
union U { int a; double b; } u = {0};
int arr[2];
 
int* p1 = reinterpret_cast<int*>(&s1); // value of p1 is "pointer to s1.a" because
                                       // s1.a and s1 are pointer-interconvertible
 
int* p2 = reinterpret_cast<int*>(&s2); // value of p2 is unchanged by reinterpret_cast
                                       // and is "pointer to s2". 
 
int* p3 = reinterpret_cast<int*>(&u);  // value of p3 is "pointer to u.a":
                                       // u.a and u are pointer-interconvertible
 
double* p4 = reinterpret_cast<double*>(p3); // value of p4 is "pointer to u.b": u.a and
                                            // u.b are pointer-interconvertible because
                                            // both are pointer-interconvertible with u
 
int* p5 = reinterpret_cast<int*>(&arr); // value of p5 is unchanged by reinterpret_cast
                                        // and is "pointer to arr"

```

Performing a class member access that designates a non-static data member or a non-static member function on a glvalue that does not actually designate an object of the appropriate type - such as one obtained through a reinterpret_cast - results in undefined behavior:

```
struct S { int x; };
struct T { int x; int f(); };
struct S1 : S {};    // standard-layout
struct ST : S, T {}; // not standard-layout
 
S s = {};
auto p = reinterpret_cast<T*>(&s); // value of p is "pointer to s"
auto i = p->x; // class member access expression is undefined behavior;
               // s is not a T object
p->x = 1; // undefined behavior
p->f();   // undefined behavior
 
S1 s1 = {};
auto p1 = reinterpret_cast<S*>(&s1); // value of p1 is "pointer to the S subobject of s1"
auto i = p1->x; // OK
p1->x = 1;      // OK
 
ST st = {};
auto p2 = reinterpret_cast<S*>(&st); // value of p2 is "pointer to st"
auto i = p2->x; // undefined behavior
p2->x = 1;      // undefined behavior

```

Many compilers issue "strict aliasing" warnings in such cases, even though technically such constructs run afoul of something other than the paragraph commonly known as the "strict aliasing rule".

The purpose of strict aliasing and related rules is to enable type-based alias analysis, which would be decimated if a program can validly create a situation where two pointers to unrelated types (e.g., an int\* and a float\*) could simultaneously exist and both can be used to load or store the same memory (see this email on SG12 reflector). Thus, any technique that is seemingly capable of creating such a situation necessarily invokes undefined behavior.

When it is needed to interpret the bytes of an object as a value of a different type, std::memcpy or std::bit_cast(since C++20) can be used:

```
double d = 0.1;
std::int64_t n;
static_assert(sizeof n == sizeof d);
// n = *reinterpret_cast<std::int64_t*>(&d); // Undefined behavior
std::memcpy(&n, &d, sizeof d);               // OK
n = std::bit_cast<std::int64_t>(d);          // also OK

```

|  |  |
| --- | --- |
| If the implementation provides std::intptr_t and/or std::uintptr_t, then a cast from a pointer to an object type or **cv** void to these types is always well-defined. However, this is not guaranteed for a function pointer. | (since C++11) |

In C, aggregate copy and assignment access the aggregate object as a whole. But in C++ such actions are always performed through a member function call, which accesses the individual subobjects rather than the entire object (or, in the case of unions, copies the object representation, i.e., via unsigned char).

### Keywords

reinterpret_cast

### Example

Demonstrates some uses of reinterpret_cast:

Run this code

```
#include <cassert>
#include <cstdint>
#include <iostream>
 
int f() { return 42; }
 
int main()
{
    int i = 7;
 
    // pointer to integer and back
    std::uintptr_t v1 = reinterpret_cast<std::uintptr_t>(&i); // static_cast is an error
    std::cout << "The value of &i is " << std::showbase << std::hex << v1 << '\n';
    int* p1 = reinterpret_cast<int*>(v1);
    assert(p1 == &i);
 
    // pointer to function to another and back
    void(*fp1)() = reinterpret_cast<void(*)()>(f);
    // fp1(); undefined behavior
    int(*fp2)() = reinterpret_cast<int(*)()>(fp1);
    std::cout << std::dec << fp2() << '\n'; // safe
 
    // type aliasing through pointer
    char* p2 = reinterpret_cast<char*>(&i);
    std::cout << (p2[0] == '\x7' ? "This system is little-endian\n"
                                 : "This system is big-endian\n");
 
    // type aliasing through reference
    reinterpret_cast<unsigned int&>(i) = 42;
    std::cout << i << '\n';
 
    [[maybe_unused]] const int &const_iref = i;
    // int &iref = reinterpret_cast<int&>(
    //     const_iref); // compiler error - can't get rid of const
    // Must use const_cast instead: int &iref = const_cast<int&>(const_iref);
}

```

Possible output:

```
The value of &i is 0x7fff352c3580
42
This system is little-endian
42

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 195 | C++98 | conversion between function pointers and object pointers not allowed | made conditionally-supported |
| CWG 658 | C++98 | the result of pointer conversions was unspecified (except for conversions back to the original type) | specification provided for pointers whose pointed-to types satisfy the alignment requirements |
| CWG 799 | C++98 | it was unclear which identity conversion can be done by reinterpret_cast | made clear |
| CWG 1268 | C++11 | reinterpret_cast could only cast lvalues to reference types | xvalues also allowed |
| CWG 2780 | C++98 | reinterpret_cast could not cast function lvalues to other reference types | allowed |
| CWG 2939 | C++17 | reinterpret_cast could cast prvalues to rvalue reference types | not allowed |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 7.6.1.10 Reinterpret cast [expr.reinterpret.cast]

- C++20 standard (ISO/IEC 14882:2020):

:   - 7.6.1.9 Reinterpret cast [expr.reinterpret.cast]

- C++17 standard (ISO/IEC 14882:2017):

:   - 8.2.10 Reinterpret cast [expr.reinterpret.cast]

- C++14 standard (ISO/IEC 14882:2014):

:   - 5.2.10 Reinterpret cast [expr.reinterpret.cast]

- C++11 standard (ISO/IEC 14882:2011):

:   - 5.2.10 Reinterpret cast [expr.reinterpret.cast]

- C++98 standard (ISO/IEC 14882:1998):

:   - 5.2.10 Reinterpret cast [expr.reinterpret.cast]

- C++03 standard (ISO/IEC 14882:2003):

:   - 5.2.10 Reinterpret cast [expr.reinterpret.cast]

### See also

|  |  |
| --- | --- |
| `const_cast` conversion | adds or removes const |
| `static_cast` conversion | performs basic conversions |
| `dynamic_cast` conversion | performs checked polymorphic conversions |
| explicit casts | permissive conversions between types |
| standard conversions | implicit conversions from one type to another |
| bit_cast(C++20) | reinterpret the object representation of one type as that of another   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/reinterpret_cast&oldid=178886>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 31 December 2024, at 03:49.