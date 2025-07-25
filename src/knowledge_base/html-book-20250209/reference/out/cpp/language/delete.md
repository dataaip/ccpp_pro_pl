# delete expression

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `new` expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****`delete` expression**** | | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | ****`delete`-expression**** | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

Destroys object(s) previously allocated by the new-expression and releases obtained memory area.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `::`(optional) `delete` expression | (1) |  |
|  | | | | | | | | | |
| `::`(optional) `delete[]` expression | (2) |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| expression | - | one of the following:  - an expression of class type contextually implicitly convertible to a pointer to object type - a prvalue of pointer to object type |

1) Destroys one non-array object created by a new-expression.2) Destroys an array created by a [new[]-expression](new.html "cpp/language/new").

### Explanation

Given the pointer evaluated from expression (after possible conversions) as ptr.

1) ptr must be one of

- a null pointer,
- a pointer to a non-array object created by a new-expression, or
- a pointer to a base subobject of a non-array object created by a new-expression.
 The pointed-to type of ptr must be similar to the type of the object (or of a base subobject). If ptr is anything else, including if it is a pointer obtained by the array form of new-expression, the behavior is undefined.2) ptr must be a null pointer or a pointer whose value is previously obtained by an array form of new-expression whose allocation function was not a non-allocating form (i.e. overload (10)). The pointed-to type of ptr must be similar to the element type of the array object. If ptr is anything else, including if it is a pointer obtained by the non-array form of new-expression, the behavior is undefined.

The result of the delete-expression always has type void.

If the object being deleted has incomplete class type at the point of deletion, and the complete class has a non-trivial destructor or a deallocation function, the behavior is undefined(until C++26)the program is ill-formed(since C++26).

If ptr is not a null pointer and the deallocation function is not a destroying delete(since C++20), the delete-expression invokes the destructor (if any) for the object that is being destroyed, or for every element of the array being destroyed (proceeding from the last element to the first element of the array). The destructor must be accessible from the point where the delete-expression appears.

After that, whether or not an exception was thrown by any destructor, the delete-expression invokes the deallocation function: either operator delete (first version) or operator delete[] (second version), unless the matching new-expression was combined with another new-expression(since C++14).

The deallocation function's name is looked up in the scope of the dynamic type of the object pointed to by ptr, which means class-specific deallocation functions, if present, are found before the global ones. If `::` is present in the delete-expression, only the global namespace is examined by this lookup. In any case, any declarations other than of usual deallocation functions are discarded.

If any deallocation function is found, the function to be called is selected as follows (see deallocation function for a more detailed description of these functions and their effects):

|  |  |
| --- | --- |
| - If at least one of the deallocation functions is a destroying delete, all non-destroying deletes are ignored. | (since C++20) |
| - If the type's alignment requirement exceeds `__STDCPP_DEFAULT_NEW_ALIGNMENT__`, alignment-aware deallocation functions (with a parameter of type std::align_val_t) are preferred. For other types, the alignment-unaware deallocation functions (without a parameter of type std::align_val_t) are preferred.   - If more than one preferred functions are found, only preferred functions are considered in the next step. - If no preferred functions are found, the non-preferred ones are considered in the next step.   - If only one function is left, that function is selected. | (since C++17) |

- If the deallocation functions that were found are class-specific, size-unaware class-specific deallocation function (without a parameter of type std::size_t) is preferred over size-aware class-specific deallocation function (with a parameter of type std::size_t).

|  |  |
| --- | --- |
| - Otherwise, lookup reached global scope, and:   - If the type is complete and if, for the array form only, the operand is a pointer to a class type with a non-trivial destructor or a (possibly multi-dimensional) array thereof, the global size-aware global function (with a parameter of type std::size_t) is selected. - Otherwise, it is unspecified whether the global size-aware deallocation function (with a parameter of type std::size_t) or the global size-unaware deallocation function (without a parameter of type std::size_t) is selected. | (since C++14) |

The selected deallocation function must be accessible from the point where the delete-expression appears, unless the deallocation function is selected at the point of definition of the dynamic type’s virtual destructor.

The pointer to the block of storage to be reclaimed is passed to the deallocation function that was selected by the process above as the first argument. The size of the block is passed as the optional std::size_t argument. The alignment requirement is passed as the optional std::align_val_t argument.(since C++17)

If ptr is a null pointer value, no destructors are called, and
the deallocation function may or may not be called (it's unspecified), but the default deallocation functions are guaranteed to do nothing when passed a null pointer.

If ptr is a pointer to a base class subobject of the object that was allocated with new, the destructor of the base class must be virtual, otherwise the behavior is undefined.

### Notes

A pointer to void cannot be deleted because it is not a pointer to an object type.

|  |  |
| --- | --- |
| Because a pair of brackets following the keyword delete is always interpreted as the array form of a delete-expression, a lambda-expression with an empty capture list immediately after delete must be enclosed in parentheses.   ```text // delete []{ return new int; }(); // parse error delete ([]{ return new int; })();  // OK ``` | (since C++11) |

### Keywords

delete

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 288 | C++98 | for the first form, the static type of the operand was compared with its dynamic type | compare the static type of the object to be deleted with its dynamic type |
| CWG 353 | C++98 | whether the deallocation function will be invoked if the destructor throws an exception was unspecified | always invoked |
| CWG 599 | C++98 | the first form could take a null pointer of any type, including function pointers | except pointers to object types, all other pointer types are rejected |
| CWG 1642 | C++98 | expression could be a pointer lvalue | not allowed |
| CWG 2474 | C++98 | deleting a pointer to an object of a similar but different type resulted in undefined behavior | made well-defined |
| CWG 2624 | C++98 | pointers obtained from non-allocating operator new[] could be passed to delete[] | prohibited |
| CWG 2758 | C++98 | it was unclear how access control was done for the deallocation function and the destructor | made clear |

### See also

- new
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/delete&oldid=173711>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 July 2024, at 21:46.