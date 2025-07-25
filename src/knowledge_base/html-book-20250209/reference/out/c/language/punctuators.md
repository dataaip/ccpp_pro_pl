# Punctuation

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
| ****Punctuation**** | | | | |
| Identifier | | | | |
| Scope | | | | |
| Lifetime | | | | |
| Lookup and name spaces | | | | |
| Type | | | | |
| Arithmetic types | | | | |
| Objects and alignment | | | | |
| The main() function | | | | |
| The as-if rule | | | | |
| Undefined behavior | | | | |
| Memory model and data races | | | | |

These are the punctuation symbols in C. The meaning of each symbol is detailed in the linked pages.

### `{` `}`

- In a struct or union definition, delimit the struct-declaration-list.
- In an enum definition, delimit the enumerator list.
- Delimit a compound statement. The compound statement may be part of a function definition.
- In initialization, delimit the initializers.

### `[` `]`

- Subscript operator.
- Part of array declarator in a declaration or a type-id.
- In initialization, introduce a designator for an array element. (since C99)
- In an attribute specifier, delimit the attributes. (since C23)

### `#`

- Introduce a preprocessing directive.
- The preprocessing operator for stringification.

### `##`

- The preprocessing operator for token pasting.

### `(` `)`

- In an expression, indicate grouping.
- Function call operator.
- In a `sizeof`, `_Alignof`(since C11) , `typeof` or `typeof_unqual`(since C23) expression, delimit the operand.
- In an explicit cast, delimit the type-id.
- In a compound literal, delimit the type-id. (since C99)
- In a declaration or a type-id, indicate grouping.
- In a function declarator (in a declaration or a type-id), delimit the parameter list.
- In an `if`, `switch`, `while`, `do-while`, or `for` statement, delimit the controlling clause.
- In a function-like macro definition, delimit the macro parameters.
- In a function-like macro invocation, delimit the macro arguments or prevent commas from being interpreted as argument separators.
- Part of a `defined`, `__has_include`, `__has_embed` or `__has_c_attribute`(since C23) preprocessing operator.
- Part of a generic selection expression. (since C11)
- In an `_Atomic` type specifier, delimit the type-id. (since C11)
- In a static assertion declaration, delimit the operands. (since C11)
- In an `_Alignas` specifier, delimit the operand. (since C11)
- In an attribute, delimit the attribute arguments. (since C23)
- In a bit-precise integer type name (_BitInt(N)), delimit the size. (since C23)
- Part of __VA_OPT__ replacement in a variadic macro definition. (since C23)
- In a preprocessor parameter used in #embed directives and __has_embed preprocessing expressions, delimit the preprocessor parameter clause. (since C23)

### `;`

- Indicate the end of

:   - a statement (including the init-statement of a for statement)
    - a declaration or struct-declaration-list

- Separate the second and third clauses of a for statement.

### `:`

- Part of conditional operator.
- Part of label declaration.
- In a bit-field member declaration, introduce the width.
- Introduce an enum base, which specifies the underlying type of the enum. (since C23)
- In a generic association, delimit the type-id or default and the selected expression. (since C11)

### `...`

- In the parameter list of a function declarator, signify a variadic function.
- In a macro definition, signify a variadic macro. (since C99)

### `?`

- Part of conditional operator.

### `::`

- In an attribute, indicate attribute scope. (since C23)
- In a preprocessor prefixed parameter (used by #embed and __has_embed), indicate scope. (since C23)

### `.`

- Member access operator.
- In initialization, introduce a designator for a struct/union member. (since C99)

### `->`

- Member access operator.

### `~`

- Unary complement operator (a.k.a. bitwise not operator).

### `!`

- Logical not operator.

### `+`

- Unary plus operator.
- Binary plus operator.

### `-`

- Unary minus operator.
- Binary minus operator.

### `*`

- Indirection operator.
- Multiplication operator.
- Pointer operator operator in a declarator or in a type-id.
- Placeholder for the length of a variable-length array declarator in a function declaration. (since C99)

### `/`

- Division operator.

### `%`

- Modulo operator.

### `^`

- Bitwise xor operator.

### `&`

- Address-of operator.
- Bitwise and operator.

### `|`

- Bitwise or operator.

### `=`

- Simple assignment operator.
- In initialization, delimit the object and the initializer list.
- In an enum definition, introduce the value of enumeration constant.

### `+=`

- Compound assignment operator.

### `-=`

- Compound assignment operator.

### `*=`

- Compound assignment operator.

### `/=`

- Compound assignment operator.

### `%=`

- Compound assignment operator.

### `^=`

- Compound assignment operator.

### `&=`

- Compound assignment operator.

### `|=`

- Compound assignment operator.

### `==`

- Equality operator.

### `!=`

- Inequality operator.

### `<`

- Less-than operator.
- Introduce a header name in

:   - a #include directive
    - a __has_include preprocessing expression (since C23)
    - a #embed directive (since C23)
    - a __has_embed preprocessing expression (since C23)
    - implementation-defined locations within a `#pragma` directive

### `>`

- Greater-than operator.
- Indicate the end of a header name in

:   - a #include directive
    - a __has_include preprocessing expression (since C23)
    - a #embed directive (since C23)
    - a __has_embed preprocessing expression (since C23)
    - implementation-defined locations within a `#pragma` directive

### `<=`

- Less-than-or-equal-to operator.

### `>=`

- Greater-than-or-equal-to operator.

### `&&`

- Logical and operator.

### `||`

- Logical or operator.

### `<<`

- Bitwise shift operator.

### `>>`

- Bitwise shift operator.

### `<<=`

- Compound assignment operator.

### `>>=`

- Compound assignment operator.

### `++`

- Increment operator.

### `--`

- Decrement operator.

### `,`

- Comma operator.
- List separator in

:   - the declarator list in a declaration
    - initializer list in initialization, including compound literals(since C99)
    - the argument list in a function call expression
    - the enumerator list in an enum declaration
    - a function parameter list
    - the macro parameter list in a function-like macro definition
    - the macro argument list in a function-like macro invocation, unless found between an inner set of parentheses
    - the generic association list in a generic selection expression (since C11)
    - an attribute list (since C23)

- In a static assertion declaration, separate the arguments. (since C11)
- In a generic selection expression, separate the controlling expression and the generic association list. (since C11)

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.4.6 Punctuators (p: 68-69)

- C17 standard (ISO/IEC 9899:2018):

:   - 6.4.6 Punctuators (p: 52-53)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.4.6 Punctuators (p: 72-73)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.4.6 Punctuators (p: 63-64)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.1.6 Punctuators

### See also

|  |  |
| --- | --- |
| Alternative representations (C95) | alternative spellings for certain operators |
| C++ documentation for Punctuation | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/punctuators&oldid=159676>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 September 2023, at 17:36.