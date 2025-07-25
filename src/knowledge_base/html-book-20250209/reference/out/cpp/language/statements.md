# Statements

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
| ****Flow control**** | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | static_cast | | | | | | const_cast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Explicit conversions | | | | | | dynamic_cast | | | | | | reinterpret_cast | | | | | |
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

 ****Statements****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Labels | | | | |
| label : statement | | | | |
| Expression statements | | | | |
| expression ; | | | | |
| Compound statements | | | | |
| `{` statement... `}` | | | | |
| Selection statements | | | | |
| if | | | | |
| switch | | | | |
| Iteration statements | | | | |
| while | | | | |
| do while | | | | |
| for | | | | |
| range for (C++11) | | | | |
| Jump statements | | | | |
| break | | | | |
| continue | | | | |
| return | | | | |
| goto | | | | |
| Declaration statements | | | | |
| declaration ; | | | | |
| Try blocks | | | | |
| try block | | | | |
| Transactional memory | | | | |
| `synchronized`, `atomic_commit`, etc (TM TS) | | | | |

**Statements** are fragments of the C++ program that are executed in sequence. The body of any function is a sequence of statements. For example:

```
int main()
{
    int n = 1;                        // declaration statement
    n = n + 1;                        // expression statement
    std::cout << "n = " << n << '\n'; // expression statement
    return 0;                         // return statement
}

```

C++ includes the following types of statements:

1) labeled statements;2) expression statements;3) compound statements;4) selection statements;5) iteration statements;6) jump statements;7) declaration statements;8) try blocks;9) atomic and synchronized blocks (TM TS).

### Labeled statements

A labeled statement labels a statement for control flow purposes.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| label statement |  |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| label | - | the label applied to the statement (defined below) |
| statement | - | the statement which the label applies to, it can be a labeled statement itself, allowing multiple labels |

#### Labels

label is defined as

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr ﻿(optional) identifier `:` | (1) |  |
|  | | | | | | | | | |
| attr ﻿(optional) `case` constexpr `:` | (2) |  |
|  | | | | | | | | | |
| attr ﻿(optional) `default:` | (3) |  |
|  | | | | | | | | | |

1) target for goto;2) case label in a switch statement;3) default label in a switch statement.

|  |  |
| --- | --- |
| An attribute sequence attr may appear just at the beginning of the label (in which case it applies to the label), or just before any statement itself, in which case it applies to the entire statement. | (since C++11) |

A label with an identifier declared inside a function matches all goto statements with the same identifier in that function, in all nested blocks, before and after its own declaration.

Two labels in a function must not have the same identifier.

|  |  |
| --- | --- |
| Besides being added to a statement, labels can also be used anywhere in compound statements. | (since C++23) |

Labels are not found by unqualified lookup: a label can have the same name as any other entity in the program.

```
void f()
{
    {
        goto label; // label in scope even though declared later
        label:      // label can appear at the end of a block standalone since C++23
    }
    goto label; // label ignores block scope
}
 
void g()
{
    goto label; // error: label not in scope in g()
}

```

#### Control-flow-limited statements

The following statements are **control-flow-limited statements** ﻿:

- The compound-statement of a try block.
- The compound-statement of a handler.

|  |  |
| --- | --- |
| - All substatements of a constexpr if statement. | (since C++17) |
| - All substatements of a consteval if statement. | (since C++23) |

For each control-flow-limited statement `S`:

- All goto target labels delcared in `S` can only be referred to by statements in `S`.
- Each case or default label appearing within `S` can only be associated with a switch statement within `S`.

### Expression statements

An expression statement is an expression followed by a semicolon.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr ﻿(optional) expression ﻿(optional) `;` |  |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| attr | - | (since C++11) optional sequence of any number of attributes |
| expression | - | an expression |

Most statements in a typical C++ program are expression statements, such as assignments or function calls.

An expression statement without an expression is called a **null statement**. It is often used to provide an empty body to a for or while loop. It can also be used to carry a label in the end of a compound statement.(until C++23)

### Compound statements

A compound statement or **block** groups a sequence of statements into a single statement.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr ﻿(optional) `{` statement... ﻿(optional) label... ﻿(optional)(since C++23) `}` |  |  |
|  | | | | | | | | | |

When one statement is expected, but multiple statements need to be executed in sequence (for example, in an if statement or a loop), a compound statement may be used:

```
if (x > 5)          // start of if statement
{                   // start of block
    int n = 1;      // declaration statement
    std::cout << n; // expression statement
}                   // end of block, end of if statement

```

Each compound statement introduces its own block scope; variables declared inside a block are destroyed at the closing brace in reverse order:

```
int main()
{ // start of outer block
    {                                // start of inner block
        std::ofstream f("test.txt"); // declaration statement
        f << "abc\n";                // expression statement
    }                                // end of inner block, f is flushed and closed
    std::ifstream f("test.txt"); // declaration statement
    std::string str;             // declaration statement
    f >> str;                    // expression statement
} // end of outer block, str is destroyed, f is closed

```

|  |  |
| --- | --- |
| A label at the end of a compound statement is treated as if it were followed by a null statement. | (since C++23) |

### Selection statements

A selection statement chooses between one of several control flows.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr ﻿(optional) `if constexpr`(optional) `(` init-statement ﻿(optional) condition `)` statement | (1) |  |
|  | | | | | | | | | |
| attr ﻿(optional) `if constexpr`(optional) `(` init-statement ﻿(optional) condition `)` statement `else` statement | (2) |  |
|  | | | | | | | | | |
| attr ﻿(optional) `switch (` init-statement ﻿(optional) condition `)` statement | (3) |  |
|  | | | | | | | | | |
| attr ﻿(optional) `if !`(optional) `consteval` compound-statement | (4) | (since C++23) |
|  | | | | | | | | | |
| attr ﻿(optional) `if !`(optional) `consteval` compound-statement `else` statement | (5) | (since C++23) |
|  | | | | | | | | | |

1) if statement;2) if statement with an else clause;3) switch statement;4) consteval if statement;5) consteval if statement with an else clause.

### Iteration statements

An iteration statement repeatedly executes some code.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr ﻿(optional) `while (` condition `)` statement | (1) |  |
|  | | | | | | | | | |
| attr ﻿(optional) `do` statement `while (` expression `)` `;` | (2) |  |
|  | | | | | | | | | |
| attr ﻿(optional) `for (` init-statement condition ﻿(optional) `;` expression ﻿(optional) `)` statement | (3) |  |
|  | | | | | | | | | |
| attr ﻿(optional) `for` `(` init-statement ﻿(optional)(since C++20) for-range-decl `:` for-range-init `)` statement | (4) | (since C++11) |
|  | | | | | | | | | |

1) while loop;2) do-while loop;3) for loop;4) range for loop.

### Jump statements

A jump statement unconditionally transfers control flow.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr ﻿(optional) `break;` | (1) |  |
|  | | | | | | | | | |
| attr ﻿(optional) `continue;` | (2) |  |
|  | | | | | | | | | |
| attr ﻿(optional) `return` expression ﻿(optional) `;` | (3) |  |
|  | | | | | | | | | |
| attr ﻿(optional) `return` braced-init-list `;` | (4) | (since C++11) |
|  | | | | | | | | | |
| attr ﻿(optional) `goto` identifier `;` | (5) |  |
|  | | | | | | | | | |

1) break statement;2) continue statement;3) return statement with an optional expression;4) return statement using list initialization;5) goto statement.

Note: for all jump statements, transfer out of a loop, out of a block, or back past an initialized variable with automatic storage duration involves the destruction of objects with automatic storage duration that are in scope at the point transferred from but not at the point transferred to. If multiple objects were initialized, the order of destruction is the opposite of the order of initialization.

### Declaration statements

A declaration statement introduces one or more identifiers into a block.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| block-declaration | (1) |  |
|  | | | | | | | | | |

1) See Declarations and Initialization for details.

### try blocks

A try block catches exceptions thrown when executing other statements.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr ﻿(optional) `try` compound-statement handler-sequence | (1) |  |
|  | | | | | | | | | |

1) See try block for details.

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Atomic and synchronized blocks An atomic and synchronized block provides transactional memory.   |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | |  | | | | | | | | | | | `synchronized` compound-statement | (1) | (TM TS) | |  | | | | | | | | | | | `atomic_noexcept` compound-statement | (2) | (TM TS) | |  | | | | | | | | | | | `atomic_cancel` compound-statement | (3) | (TM TS) | |  | | | | | | | | | | | `atomic_commit` compound-statement | (4) | (TM TS) | |  | | | | | | | | | |  1) synchronized block, executed in single total order with all synchronized blocks;2) atomic block that aborts on exceptions;3) atomic block that rolls back on exceptions;4) atomic block that commits on exceptions. | (TM TS) |

### Substatements

A **substatement** of a statement is one of the following:

- For a labeled statement, its statement ﻿.
- For a compound statement, any statement of its statement... ﻿.
- For a selection statement, any of its statement ﻿ or compound-statement ﻿(since C++23).
- For an iteration statement, its statement ﻿.

A statement S1 **encloses** a statement S2 if any of the following conditions is satisfied:

- S2 is a substatement of S1
- S1 is a selection statement or iteration statement, and S2 is the init-statement of S1.
- S1 is a try block, and S2 is either its compound-statement or the compound-statement of any handler in its handler-seq ﻿.
- S1 encloses a statement S3 and S3 encloses S2.

A statement S1 is **enclosed by** a statement S2 if S2 encloses S1.

### See also

|  |  |
| --- | --- |
| C documentation for Statements | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/statements&oldid=179323>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 January 2025, at 23:57.