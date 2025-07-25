# Initialization

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
| ****Initialization**** | | | | |
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

 ****Initialization****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****Initializer**** | | | | |
| Default initialization | | | | |
| Value initialization | | | | |
| Direct initialization | | | | |
| Copy-initialization | | | | |
| List initialization (C++11) | | | | |
| Aggregate initialization | | | | |
| Reference initialization | | | | |
| Copy elision | | | | |
| Static initialization | | | | |
| Zero initialization | | | | |
| Constant initialization | | | | |
| Dynamic non-local initialization | | | | |
| Ordered dynamic initialization | | | | |
| Unordered dynamic initialization | | | | |
| Class member initialization | | | | |
| Member initializer list | | | | |
| Default member initializer (C++11) | | | | |

**Initialization** of a variable provides its initial value at the time of construction.

The initial value may be provided in the initializer section of a declarator or a new expression. It also takes place during function calls: function parameters and the function return values are also initialized.

### Initializers

For each declarator, the **initializer** (if exists) may be one of the following:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `=` expression | (1) |  |
|  | | | | | | | | | |
| `= {}` `= {` initializer-list `}` `= {` designated-initializer-list `}` | (2) | (since C++20) |
|  | | | | | | | | | |
| `(` expression-list `)` `(` initializer-list `)` | (3) | (until C++11) (since C++11) |
|  | | | | | | | | | |
| `{}` `{` initializer-list `}` `{` designated-initializer-list `}` | (4) | (since C++11) (since C++11) (since C++20) |
|  | | | | | | | | | |

1) Copy-initialization syntax.2) Aggregate initialization syntax.(until C++11)List-initialization syntax.(since C++11)3) Direct-initialization syntax.4) List-initialization syntax.

|  |  |  |
| --- | --- | --- |
| expression | - | any expression (except unparenthesized comma expressions) |
| expression-list | - | a comma-separated list of expressions (except unparenthesized comma expressions) |
| initializer-list | - | a comma-separated list of initializer clauses (see below) |
| designated-initializer-list | - | a comma-separated list of designated initializer clauses |

An **initializer clause** may be one of the following:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| expression | (1) |  |
|  | | | | | | | | | |
| `{}` | (2) |  |
|  | | | | | | | | | |
| `{` initializer-list `}` | (3) |  |
|  | | | | | | | | | |
| `{` designated-initializer-list `}` | (4) | (since C++20) |
|  | | | | | | | | | |

Syntaxes (2-4) are collectively called **brace-enclosed initializer list**.

#### Initializer semantics

If no initializer is specified for an object, the object is default-initialized. If no initializer is specified for a reference, the program is ill-formed.

If the initializer specified for an object is () (cannot appear in declarators due to the syntax restriction), the object is value-initialized. If the initializer specified for a reference is (), the program is ill-formed.

The semantics of initializers are as follows:

- If the entity being initialized is a reference, see reference initialization.
- Otherwise, the entity being initialized is an object. Given the type of the object as `T`:

:   - If the initializer is of syntax (1), the object is copy-initialized.

|  |  |
| --- | --- |
| - If the initializer is of syntax (2):   - If `T` is an aggregate, aggregate initialization applies. - If `T` is a scalar type, T x = { a }; is equivalent to T x = a;. - Otherwise, the program is ill-formed. | (until C++11) |
| - If the initializer is of syntax (2) or (4), the object is list-initialized. | (since C++11) |

:   - If the initializer is of syntax (3), the object is direct-initialized.

```
#include <string>
 
std::string s1;           // default-initialization
std::string s2();         // NOT an initialization!
                          // actually declares a function “s2”
                          // with no parameter and returns std::string
std::string s3 = "hello"; // copy-initialization
std::string s4("hello");  // direct-initialization
std::string s5{'a'};      // list-initialization (since C++11)
 
char a[3] = {'a', 'b'}; // aggregate initialization
                        // (part of list initialization since C++11)
char& c = a[0];         // reference initialization

```

### Non-local variables

All non-local variables with static storage duration are initialized as part of program startup, before the execution of the main function begins (unless deferred, see below). All non-local variables with thread-local storage duration are initialized as part of thread launch, sequenced-before the execution of the thread function begins. For both of these classes of variables, initialization occurs in two distinct stages:

#### Static initialization

There are two forms of static initialization:

1) If possible, constant initialization is applied.2) Otherwise, non-local static and thread-local variables are zero-initialized.

In practice:

- Constant initialization is usually applied at compile time. Pre-calculated object representations are stored as part of the program image. If the compiler doesn't do that, it must still guarantee that the initialization happens before any dynamic initialization.
- Variables to be zero-initialized are placed in the `.bss` segment of the program image, which occupies no space on disk and is zeroed out by the OS when loading the program.

#### Dynamic initialization

After all static initialization is completed, dynamic initialization of non-local variables occurs in the following situations:

1) **Unordered dynamic initialization**, which applies only to (static/thread-local) class template static data members and variable templates(since C++14) that aren't explicitly specialized. Initialization of such static variables is indeterminately sequenced with respect to all other dynamic initialization except if the program starts a thread before a variable is initialized, in which case its initialization is unsequenced(since C++17). Initialization of such thread-local variables is unsequenced with respect to all other dynamic initialization.

|  |  |
| --- | --- |
| 2) **Partially-ordered dynamic initialization**, which applies to all inline variables that are not an implicitly or explicitly instantiated specialization. If a partially-ordered V is defined before ordered or partially-ordered W in every translation unit, the initialization of V is sequenced before the initialization of W (or happens-before, if the program starts a thread). | (since C++17) |

3) **Ordered dynamic initialization**, which applies to all other non-local variables: within a single translation unit, initialization of these variables is always sequenced in exact order their definitions appear in the source code. Initialization of static variables in different translation units is indeterminately sequenced. Initialization of thread-local variables in different translation units is unsequenced.

If the initialization of a non-local variable with static or thread storage duration exits via an exception, std::terminate is called.

#### Early dynamic initialization

The compilers are allowed to initialize dynamically-initialized variables as part of static initialization (essentially, at compile time), if the following conditions are both true:

1) the dynamic version of the initialization does not change the value of any other object of namespace scope prior to its initialization2) the static version of the initialization produces the same value in the initialized variable as would be produced by the dynamic initialization if all variables not required to be initialized statically were initialized dynamically.

Because of the rule above, if initialization of some object `o1` refers to a namespace-scope object `o2`, which potentially requires dynamic initialization, but is defined later in the same translation unit, it is unspecified whether the value of `o2` used will be the value of the fully initialized `o2` (because the compiler promoted initialization of `o2` to compile time) or will be the value of `o2` merely zero-initialized.

```
inline double fd() { return 1.0; }
 
extern double d1;
 
double d2 = d1;   // unspecified:
                  // dynamically initialized to 0.0 if d1 is dynamically initialized, or
                  // dynamically initialized to 1.0 if d1 is statically initialized, or
                  // statically initialized to 0.0 (because that would be its value
                  // if both variables were dynamically initialized)
 
double d1 = fd(); // may be initialized statically or dynamically to 1.0

```

#### Deferred dynamic initialization

It is implementation-defined whether dynamic initialization happens-before the first statement of the main function (for statics) or the initial function of the thread (for thread-locals), or deferred to happen after.

If the initialization of a non-inline variable(since C++17) is deferred to happen after the first statement of main/thread function, it happens before the first ODR-use of any variable with static/thread storage duration defined in the same translation unit as the variable to be initialized. If no variable or function is ODR-used from a given translation unit, the non-local variables defined in that translation unit may never be initialized (this models the behavior of an on-demand dynamic library). However, as long as anything from a translation unit is ODR-used, all non-local variables whose initialization or destruction has side effects will be initialized even if they are not used in the program.

|  |  |
| --- | --- |
| If the initialization of an inline variable is deferred, it happens before the first ODR-use of that specific variable. | (since C++17) |

```
// ============
// == File 1 ==
 
#include "a.h"
#include "b.h"
 
B b;
A::A() { b.Use(); }
 
// ============
// == File 2 ==
 
#include "a.h"
 
A a;
 
// ============
// == File 3 ==
 
#include "a.h"
#include "b.h"
 
extern A a;
extern B b;
 
int main()
{
    a.Use();
    b.Use();
}
 
// If a is initialized before main is entered, b may still be uninitialized
// at the point where A::A() uses it (because dynamic initialization is
// indeterminately sequenced across translation units)
 
// If a is initialized at some point after the first statement of main (which odr-uses
// a function defined in File 1, forcing its dynamic initialization to run),
// then b will be initialized prior to its use in A::A

```

### Static local variables

For initialization of local (that is, block scope) static and thread-local variables, see static block variables.

Initializer is not allowed in a block-scope declaration of a variable with external or internal linkage. Such a declaration must appear with extern and cannot be a definition.

### Class members

Non-static data members can be initialized with member initializer list or with a default member initializer.

### Notes

The order of destruction of non-local variables is described in std::exit.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 270 | C++98 | the order of initializing static data members of class templates was unspecified | specified as unordered except for explicit specializations and definitions |
| CWG 441 | C++98 | non-local references with static storage duration were not always initialized before dynamic initializations | considered as static initialization, always initialized before dynamic initializations |
| CWG 1415 | C++98 | a block-scope extern variable declaration could be a definition | prohibited (no initializer allowed in such declarations) |
| CWG 2599 | C++98 | it was unclear whether evaluating function arguments in the initializer is part of initialization | it is part of initialization |

### See also

- copy elision
- converting constructor
- copy constructor
- default constructor
- `explicit`
- move constructor
- `new`

|  |  |
| --- | --- |
| C documentation for Initialization | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/initialization&oldid=178911>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 31 December 2024, at 22:07.