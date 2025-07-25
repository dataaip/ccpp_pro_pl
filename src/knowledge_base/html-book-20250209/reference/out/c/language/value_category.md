# Value categories

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
| ****value category**** | | | | |
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
| cast operators | | | | |

Each expression in C (an operator with its arguments, a function call, a constant, a variable name, etc) is characterized by two independent properties: a type and a value category.

Every expression belongs to one of three value categories: lvalue, non-lvalue object (rvalue), and function designator.

### Lvalue expressions

Lvalue expression is any expression with object type other than the type `void`, which potentially designates an object (the behavior is undefined if an lvalue does not actually designate an object when it is evaluated). In other words, lvalue expression evaluates to the **object identity**. The name of this value category ("left value") is historic and reflects the use of lvalue expressions as the left-hand operand of the assignment operator in the CPL programming language.

Lvalue expressions can be used in the following **lvalue contexts**:

- as the operand of the address-of operator (except if the lvalue designates a bit-field or was declared register).
- as the operand of the pre/post increment and decrement operators.
- as the left-hand operand of the member access (dot) operator.
- as the left-hand operand of the assignment and compound assignment operators.

If an lvalue expression is used in any context other than `sizeof`, `_Alignof`, or the operators listed above, non-array lvalues of any complete type undergo lvalue conversion, which models the memory load of the value of the object from its location. Similarly, array lvalues undergo array-to-pointer conversion when used in any context other than `sizeof`, `_Alignof`, address-of operator, or array initialization from a string literal.

The semantics of `const`/`volatile`/`restrict`-qualifiers and atomic types apply to lvalues only (lvalue conversion strips the qualifiers and removes atomicity).

The following expressions are lvalues:

- identifiers, including function named parameters, provided they were declared as designating objects (not functions or enumeration constants)
- string literals
- (C99) compound literals
- parenthesized expression if the unparenthesized expression is an lvalue
- the result of a member access (dot) operator if its left-hand argument is lvalue
- the result of a member access through pointer `->` operator
- the result of the indirection (unary `*`) operator applied to a pointer to object
- the result of the subscription operator (`[]`)

#### Modifiable lvalue expressions

A **modifiable lvalue** is any lvalue expression of complete, non-array type which is not const-qualified, and, if it's a struct/union, has no members that are const-qualified, recursively.

Only modifiable lvalue expressions may be used as arguments to increment/decrement, and as left-hand arguments of assignment and compound assignment operators.

### Non-lvalue object expressions

Known as **rvalues**, non-lvalue object expressions are the expressions of object types that do not designate objects, but rather values that have no object identity or storage location. The address of a non-lvalue object expression cannot be taken.

The following expressions are non-lvalue object expressions:

- integer, character, and floating constants
- all operators not specified to return lvalues, including

:   - any function call expression
    - any cast expression (note that compound literals, which look similar, are lvalues)
    - member access operator (dot) applied to a non-lvalue structure/union, f().x, (x,s1).a, (s1=s2).m
    - results of all arithmetic, relational, logical, and bitwise operators
    - results of increment and decrement operators (note: pre-forms are lvalues in C++)
    - results of assignment operators (note: also lvalues in C++)
    - the conditional operator (note: is lvalue in C++ if both the second and third operands are lvalues of the same type)
    - the comma operator (note: is lvalue in C++ if the second operand is)
    - the address-of operator, even if neutralized by application to the result of unary `*` operator

As a special case, expressions of type `void` are assumed to be non-lvalue object expressions that yield a value which has no representation and requires no storage.

Note that a struct/union rvalue that has a member (possibly nested) of array type does in fact designate an object with temporary lifetime. This object can be accessed through lvalue expressions that form by indexing the array member or by indirection through the pointer obtained by array-to-pointer conversion of the array member.

### Function designator expression

A function designator (the identifier introduced by a function declaration) is an expression of function type. When used in any context other than the address-of operator, `sizeof`, and `_Alignof` (the last two generate compile errors when applied to functions), the function designator is always converted to a non-lvalue pointer to function. Note that the function-call operator is defined for pointers to functions and not for function designators themselves.

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.3.2.1 Lvalues, arrays, and function designators (p: 40)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.3.2.1 Lvalues, arrays, and function designators (p: 54-55)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.3.2.1 Lvalues, arrays, and function designators (p: 46)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.2.2.1 Lvalues and function designators

### See also

|  |  |
| --- | --- |
| C++ documentation for Value categories | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/value_category&oldid=152391>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 May 2023, at 22:19.