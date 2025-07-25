# Exceptions

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

 ****Exceptions****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| try block | | | | |
| Throwing exceptions | | | | |
| Handling exceptions | | | | |
| Exception specification | | | | |
| noexcept specification (C++11) | | | | |
| dynamic specification (until C++17\*) | | | | |
| noexcept operator (C++11) | | | | |

Exception handling provides a way of transferring control and information from some point in the execution of a program to a handler associated with a point previously passed by the execution (in other words, exception handling transfers control up the call stack).

Evaluating a throw expression will throw an exception. Exceptions can also be thrown in other contexts.

In order for an exception to be caught, the throw expression has to be inside a try block, and the try block has to contain a handler that matches the type of the exception object.

When declaring a function, the following specification(s) may be provided to limit the types of the exceptions a function may throw:

|  |  |
| --- | --- |
| - dynamic exception specifications | (until C++17) |

|  |  |
| --- | --- |
| - noexcept specifications | (since C++11) |

Errors that arise during exception handling are handled by std::terminate and std::unexpected(until C++17).

### Usage

While throw expression can be used to transfer control to an arbitrary block of code up the execution stack, for arbitrary reasons (similar to std::longjmp), its intended usage is error handling.

#### Error handling

Throwing an exception is used to signal errors from functions, where "errors" are typically limited to only the following[[1]](exceptions.html#cite_note-1)[[2]](exceptions.html#cite_note-2)[[3]](exceptions.html#cite_note-3):

1. Failures to meet the postconditions, such as failing to produce a valid return value object.
2. Failures to meet the preconditions of another function that must be called.
3. (for non-private member functions) Failures to (re)establish a class invariant.

In particular, this implies that the failures of constructors (see also RAII) and most operators should be reported by throwing exceptions.

In addition, so-called **wide contract** functions use exceptions to indicate unacceptable inputs, for example, std::basic_string::at has no preconditions, but throws an exception to indicate index out of range.

#### Exception safety

After the error condition is reported by a function, additional guarantees may be provided with regards to the state of the program. The following four levels of exception guarantee are generally recognized[[4]](exceptions.html#cite_note-4)[[5]](exceptions.html#cite_note-5)[[6]](exceptions.html#cite_note-6), which are strict supersets of each other:

1. **Nothrow (or nofail) exception guarantee** — the function never throws exceptions. Nothrow (errors are reported by other means or concealed) is expected of destructors and other functions that may be called during stack unwinding. The destructors are `noexcept` by default.(since C++11) Nofail (the function always succeeds) is expected of swaps, move constructors, and other functions used by those that provide strong exception guarantee.
2. **Strong exception guarantee** — If the function throws an exception, the state of the program is rolled back to the state just before the function call (for example, std::vector::push_back).
3. **Basic exception guarantee** — If the function throws an exception, the program is in a valid state. No resources are leaked, and all objects' invariants are intact.
4. **No exception guarantee** — If the function throws an exception, the program may not be in a valid state: resource leaks, memory corruption, or other invariant-destroying errors may have occurred.

Generic components may, in addition, offer **exception-neutral guarantee**: if an exception is thrown from a template parameter (e.g. from the `Compare` function object of std::sort or from the constructor of `T` in std::make_shared), it is propagated, unchanged, to the caller.

### Exception objects

While objects of any complete type and cv pointers to void may be thrown as exception objects, all standard library functions throw unnamed objects by value, and the types of those objects are derived (directly or indirectly) from std::exception. User-defined exceptions usually follow this pattern.[[7]](exceptions.html#cite_note-7)[[8]](exceptions.html#cite_note-8)[[9]](exceptions.html#cite_note-9)

To avoid unnecessary copying of the exception object and object slicing, the best practice for handlers is to catch by reference.[[10]](exceptions.html#cite_note-10)[[11]](exceptions.html#cite_note-11)[[12]](exceptions.html#cite_note-12)[[13]](exceptions.html#cite_note-13)

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_constexpr_exceptions` | `202411L` | (C++26) | constexpr exceptions |

### External links

|  |
| --- |
| 1. ↑  H. Sutter (2004) "When and How to Use Exceptions" in Dr. Dobb's 2. ↑ H. Sutter, A. Alexandrescu (2004), "C++ Coding Standards", Item 70 3. ↑ C++ Core Guidelines I.10: Use exceptions to signal a failure to perform a required task 4. ↑ B. Stroustrup (2000), "The C++ Programming Language" Appendix E 5. ↑ H. Sutter (2000) "Exceptional C++" 6. ↑ D. Abrahams (2001) "Exception Safety in Generic Components" 7. ↑ D. Abrahams (2001) "Error and Exception Handling" 8. ↑ isocpp.org Super-FAQ "What should I throw?" 9. ↑ C++ Core Guidelines E.14: Use purpose-designed user-defined types as exceptions (not built-in types) 10. ↑ C++ Core Guidelines E.15: Throw by value, catch exceptions from a hierarchy by reference 11. ↑ S. Meyers (1996) "More Effective C++" Item 13 12. ↑ isocpp.org Super-FAQ "What should I catch?" 13. ↑ H. Sutter, A. Alexandrescu (2004) "C++ Coding Standards" Item 73 |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/exceptions&oldid=178582>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 December 2024, at 13:54.