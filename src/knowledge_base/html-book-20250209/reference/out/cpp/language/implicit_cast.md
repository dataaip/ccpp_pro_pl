# Implicit conversions

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****Implicit conversions**** | | | | | | static_cast | | | | | | const_cast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Explicit conversions | | | | | | dynamic_cast | | | | | | reinterpret_cast | | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****Implicit conversions**** | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

Implicit conversions are performed whenever an expression of some type `T1` is used in context that does not accept that type, but accepts some other type `T2`; in particular:

- when the expression is used as the argument when calling a function that is declared with `T2` as parameter;
- when the expression is used as an operand with an operator that expects `T2`;
- when initializing a new object of type `T2`, including `return` statement in a function returning `T2`;
- when the expression is used in a switch statement (`T2` is integral type);
- when the expression is used in an if statement or a loop (`T2` is bool).

The program is well-formed (compiles) only if there exists one unambiguous **implicit conversion sequence** from `T1` to `T2`.

If there are multiple overloads of the function or operator being called, after the implicit conversion sequence is built from `T1` to each available `T2`, overload resolution rules decide which overload is compiled.

Note: in arithmetic expressions, the destination type for the implicit conversions on the operands to binary operators is determined by a separate set of rules: usual arithmetic conversions.

### Order of the conversions

Implicit conversion sequence consists of the following, in this order:

1) zero or one **standard conversion sequence**;2) zero or one **user-defined conversion**;3) zero or one **standard conversion sequence** (only if a user-defined conversion is used).

When considering the argument to a constructor or to a user-defined conversion function, only one standard conversion sequence is allowed (otherwise user-defined conversions could be effectively chained). When converting from one non-class type to another non-class type, only a standard conversion sequence is allowed.

A standard conversion sequence consists of the following, in this order:

1) zero or one conversion from the following set:

- **lvalue-to-rvalue conversion**,
- **array-to-pointer conversion**, and
- **function-to-pointer conversion**;
2) zero or one **numeric promotion** or **numeric conversion**;

|  |  |
| --- | --- |
| 3) zero or one **function pointer conversion**; | (since C++17) |

4) zero or one **qualification conversion**.

A user-defined conversion consists of zero or one non-explicit single-argument converting constructor or non-explicit conversion function call.

An expression e is said to be **implicitly convertible to `T2`** if and only if `T2` can be copy-initialized from e, that is the declaration T2 t = e; is well-formed (can be compiled), for some invented temporary `t`. Note that this is different from direct initialization (T2 t(e)), where explicit constructors and conversion functions would additionally be considered.

#### Contextual conversions

|  |  |  |  |
| --- | --- | --- | --- |
| In the following contexts, the type bool is expected and the implicit conversion is performed if the declaration bool t(e); is well-formed (that is, an explicit conversion function such as explicit T::operator bool() const; is considered). Such expression e is said to be **contextually converted to bool**.   - the controlling expression of if, while, for; - the operands of the built-in logical operators `!`, `&&` and `||`; - the first operand of the conditional operator `?:`; - the predicate in a `static_assert` declaration; - the expression in a `noexcept` specifier;  |  |  | | --- | --- | | - the expression in an `explicit` specifier; | (since C++20) | | (since C++11) |

In the following contexts, a context-specific type `T` is expected, and the expression e of class type `E` is only allowed if

|  |  |
| --- | --- |
| - `E` has a single non-explicit(since C++11) user-defined conversion function to an allowable type. | (until C++14) |
| - there is exactly one type `T` among the allowable types such that `E` has non-explicit conversion functions whose return types are (possibly cv-qualified) `T` or reference to (possibly cv-qualified) `T`, and - e is implicitly convertible to `T`. | (since C++14) |

Such expression e is said to be **contextually implicitly converted** to the specified type `T`. Note that explicit conversion functions are not considered, even though they are considered in contextual conversions to bool.(since C++11)

- the argument of the delete-expression (`T` is any object pointer type);
- integral constant expression, where a literal class is used (`T` is any integral or unscoped enumeration type, the selected user-defined conversion function must be constexpr);
- the controlling expression of the `switch` statement (`T` is any integral or enumeration type).

```
#include <cassert>
 
template<typename T>
class zero_init
{
    T val;
public:
    zero_init() : val(static_cast<T>(0)) {}
    zero_init(T val) : val(val) {}
    operator T&() { return val; }
    operator T() const { return val; }
};
 
int main()
{
    zero_init<int> i;
    assert(i == 0);
 
    i = 7;
    assert(i == 7);
 
    switch (i) {}     // error until C++14 (more than one conversion function)
                      // OK since C++14 (both functions convert to the same type int)
    switch (i + 0) {} // always okay (implicit conversion)
}

```

### Value transformations

Value transformations are conversions that change the value category of an expression. They take place whenever an expression appears as an operand of an operator that expects an expression of a different value category:

- Whenever a glvalue appears as an operand of an operator that requires a prvalue for that operand, the **lvalue-to-rvalue**, **array-to-pointer**, or **function-to-pointer** standard conversions are applied to convert the expression to a prvalue.

|  |  |
| --- | --- |
| - Unless otherwise specified, whenever a prvalue appears as an operand of an operator that expects a glvalue for that operand, the **temporary materialization conversion** is applied to convert the expression to an xvalue. | (since C++17) |

#### Lvalue-to-rvalue conversion

An lvalue(until C++11)A glvalue(since C++11) of any non-function, non-array type `T` can be implicitly converted to an rvalue(until C++11)a prvalue(since C++11):

- If `T` is not a class type, the type of the rvalue(until C++11)prvalue(since C++11) is the cv-unqualified version of `T`.
- Otherwise, the type of the rvalue(until C++11)prvalue(since C++11) is `T`.

If an lvalue-to-rvalue conversion from an incomplete type is required by a program, that program is ill-formed.

Given the object to which the lvalue(until C++11)glvalue(since C++11) refers as obj:

|  |  |
| --- | --- |
| - When an lvalue-to-rvalue conversion occurs within the operand of `sizeof`, the value contained in obj is not accessed, since that operator does not evaluate its operand.  - The result of the conversion is the value contained in obj. If one of `T` and the type of obj is a signed integer type, and the other is the corresponding unsigned integer type, the result is the value of type `T` with the same value representation of obj. | (until C++11) |
| - When an lvalue-to-rvalue conversion is applied to an expression E, the value contained in obj is not accessed if:   - E is not potentially evaluated, or - the evaluation of E results in the evaluation of a member Ex of the set of potential results of E, and Ex names a variable x that is not odr-used by Ex.   - The result of the conversion is determined as follows:   - If `T` is (possibly cv-qualified) std::nullptr_t, the result is a null pointer constant. obj is not accessed by the conversion, so there is no side effect even if `T` is volatile-qualified, and the glvalue can refer to an inactive member of a union. - Otherwise, if `T` is a class type:   |  |  | | --- | --- | | - The conversion copy-initializes a temporary of type `T` from the glvalue, and the result of the conversion is a prvalue for the temporary. | (until C++17) | | - The conversion copy-initializes the result object from the glvalue. | (since C++17) |   - Otherwise, if obj contains an invalid pointer value, the behavior is implementation-defined. - Otherwise, if the bits in the value representation of obj are not valid for obj's type, the behavior is undefined. - Otherwise, obj is read, and(since C++20) the result is the value contained in obj. If one of `T` and the type of obj is a signed integer type, and the other is the corresponding unsigned integer type, the result is the value of type `T` with the same value representation of obj. | (since C++11) |

This conversion models the act of reading a value from a memory location into a CPU register.

#### Array-to-pointer conversion

An lvalue or rvalue of type “array of N `T`” or “array of unknown bound of `T`” can be implicitly converted to a prvalue of type “pointer to `T`”. If the array is a prvalue, temporary materialization occurs.(since C++17) The resulting pointer refers to the first element of the array (see Array-to-pointer decay for details).

#### Function-to-pointer conversion

An lvalue of function type can be implicitly converted to a prvalue pointer to that function. This does not apply to non-static member functions because lvalues that refer to non-static member functions do not exist.

|  |  |
| --- | --- |
| Temporary materialization A prvalue of any complete type `T` can be converted to an xvalue of the same type `T`. This conversion initializes a temporary object of type T from the prvalue by evaluating the prvalue with the temporary object as its result object, and produces an xvalue denoting the temporary object.  If `T` is a class or array of class type, it must have an accessible and non-deleted destructor.   ```text struct S { int m; }; int i = S().m; // member access expects glvalue as of C++17;                // S() prvalue is converted to xvalue ```   Temporary materialization occurs in the following situations:   - when binding a reference to a prvalue; - when accessing a non-static data member of a class prvalue; - when invoking an implicit object member function of a class prvalue; - when performing an array-to-pointer conversion (see above) or subscripting on an array prvalue; - when initializing an object of type std::initializer_list<T> from a braced-enclosed initializer list; - when a prvalue appears as a discarded-value expression.   Note that temporary materialization does ****not**** occur when initializing an object from a prvalue of the same type (by direct-initialization or copy-initialization): such object is initialized directly from the initializer. This ensures “guaranteed copy elision”. | (since C++17) |

### Integral promotion

prvalues of small integral types (such as char) and unscoped enumeration types may be converted to prvalues of larger integral types (such as int). In particular, arithmetic operators do not accept types smaller than int as arguments, and integral promotions are automatically applied after lvalue-to-rvalue conversion, if applicable. This conversion always preserves the value.

The following implicit conversions in this section are classified as **integral promotions**.

Note that for a given source type, the destination type of integral promotion is unique, And all other conversions are not promotions. For example, overload resolution chooses char -> int (promotion) over char -> short (conversion).

#### Promotion from integral types

A prvalue of type bool can be converted to a prvalue of type int, with false becoming ​0​ and true becoming 1.

For a prvalue val of an integral type `T` except bool:

1) If val is the result of an lvalue-to-rvalue conversion applied to a bit-field,

- val can be converted to a prvalue of type int if int can represent all the values of the bit-field;
- otherwise, val can be converted to unsigned int if unsigned int can represent all the values of the bit-field;
- otherwise, val can be converted according to the rules specified in item (3).
2) Otherwise (val is not converted from a bit-field),

- if `T` is char8_t, (since C++20)char16_t, char32_t or (since C++11)wchar_t, val can be converted according to the rules specified in item (3);
- otherwise, if the integer conversion rank of `T` is lower than the rank of int:

:   - val can be converted to a prvalue of type int if int can represent all the values of `T`;
    - otherwise, val can be converted to a prvalue of type unsigned int.

3) In the cases specified by item (1) (a converted bit-field not fitting unsigned int) or item (2) (`T` is one of the given character types), val can be converted to a prvalue of the first of the following types that can represent all the values of its underlying type:

:   - int
    - unsigned int
    - long
    - unsigned long

|  |  |
| --- | --- |
| - long long - unsigned long long - the underlying type of `T` | (since C++11) |

#### Promotion from enumeration types

A prvalue of an unscoped enumeration type whose underlying type is not fixed can be converted to a prvalue of the first type from the following list able to hold their entire value range:

- int
- unsigned int
- long
- unsigned long

|  |  |
| --- | --- |
| - long long - unsigned long long - the extended integer type such that   - its integer conversion rank is greater than the rank of long long, - its integer conversion rank is the lowest among all extended integer types, and - it is signed if there are two types with the lowest integer conversion rank among all extended integer types. | (since C++11) |

|  |  |
| --- | --- |
| A prvalue of an unscoped enumeration type whose underlying type is fixed can be converted to its underlying type. Moreover, if the underlying type is also subject to integral promotion, to the promoted underlying type. Conversion to the unpromoted underlying type is better for the purposes of overload resolution. | (since C++11) |

### Floating-point promotion

A prvalue of type float can be converted to a prvalue of type double. The value does not change.

This conversion is called **floating-point promotion**.

### Numeric conversions

Unlike the promotions, numeric conversions may change the values, with potential loss of precision.

#### Integral conversions

A prvalue of an integer type or of an unscoped enumeration type can be converted to any other integer type. If the conversion is listed under integral promotions, it is a promotion and not a conversion.

- If the destination type is unsigned, the resulting value is the smallest unsigned value equal to the source value modulo 2n  
   where n is the number of bits used to represent the destination type.

:   - That is, depending on whether the destination type is wider or narrower, signed integers are sign-extended[[1]](implicit_cast.html#cite_note-1) or truncated and unsigned integers are zero-extended or truncated respectively.

- If the destination type is signed, the value does not change if the source integer can be represented in the destination type. Otherwise the result is implementation-defined(until C++20)the unique value of the destination type equal to the source value modulo 2n  
   where n is the number of bits used to represent the destination type(since C++20) (note that this is different from signed integer arithmetic overflow, which is undefined).
- If the source type is bool, the value false is converted to zero and the value true is converted to the value one of the destination type (note that if the destination type is int, this is an integer promotion, not an integer conversion).
- If the destination type is bool, this is a boolean conversion (see below).

1. ↑ This only applies if the arithmetic is two's complement which is only required for the exact-width integer types. Note, however, that at the moment all platforms with a C++ compiler use two's complement arithmetic.

#### Floating-point conversions

|  |  |
| --- | --- |
| A prvalue of a floating-point type can be converted to a prvalue of any other floating-point type. | (until C++23) |
| A prvalue of a floating-point type can be converted to a prvalue of any other floating-point type with a greater or equal floating-point conversion rank.  A prvalue of a standard floating-point type can be converted to a prvalue of any other standard floating-point type.  `static_cast` can be used to explicitly convert a prvalue of floating-point type to any other floating-point type. | (since C++23) |

If the conversion is listed under floating-point promotions, it is a promotion and not a conversion.

- If the source value can be represented exactly in the destination type, it does not change.
- If the source value is between two representable values of the destination type, the result is one of those two values (it is implementation-defined which one, although if IEEE arithmetic is supported, rounding defaults to nearest).
- Otherwise, the behavior is undefined.

#### Floating–integral conversions

A prvalue of floating-point type can be converted to a prvalue of any integer type. The fractional part is truncated, that is, the fractional part is discarded.

- If the truncated value cannot fit into the destination type, the behavior is undefined (even when the destination type is unsigned, modulo arithmetic does not apply).
- If the destination type is bool, this is a boolean conversion (see below).

A prvalue of integer or unscoped enumeration type can be converted to a prvalue of any floating-point type. The result is exact if possible.

- If the value can fit into the destination type but cannot be represented exactly, it is implementation defined whether the closest higher or the closest lower representable value will be selected, although if IEEE arithmetic is supported, rounding defaults to nearest.
- If the value cannot fit into the destination type, the behavior is undefined.
- If the source type is bool, the value false is converted to zero, and the value true is converted to one.

#### Pointer conversions

A null pointer constant can be converted to any pointer type, and the result is the null pointer value of that type. Such conversion (known as **null pointer conversion**) is allowed to convert to a cv-qualified type as a single conversion, that is, it is not considered a combination of numeric and qualifying conversions.

A prvalue pointer to any (optionally cv-qualified) object type `T` can be converted to a prvalue pointer to (identically cv-qualified) void. The resulting pointer represents the same location in memory as the original pointer value.

- If the original pointer is a null pointer value, the result is a null pointer value of the destination type.

A prvalue ptr of type “pointer to (possibly cv-qualified) `Derived`” can be converted to a prvalue of type “pointer to (possibly cv-qualified) `Base`”, where `Base` is a base class of `Derived`, and `Derived` is a complete class type. If the `Base` is inaccessible or ambiguous, the program is ill-formed.

- If ptr is a null pointer value, the result is also a null pointer value.
- Otherwise, if `Base` is a virtual base class of `Derived` and ptr does not point to an object whose type is similar to `Derived` and that is within its lifetime or within its period of construction or destruction, the behavior is undefined.
- Otherwise, the result is a pointer to the base class subobject of the derived class object.

#### Pointer-to-member conversions

A null pointer constant can be converted to any pointer-to-member type, and the result is the null member pointer value of that type. Such conversion (known as **null member pointer conversion**) is allowed to convert to a cv-qualified type as a single conversion, that is, it is not considered a combination of numeric and qualifying conversions.

A prvalue of type “pointer to member of `Base` of type (possibly cv-qualified) `T`” can be converted to a prvalue of type “pointer to member of `Derived` of type (identically cv-qualified) `T`”, where `Base` is a base class of `Derived`, and `Derived` is a complete class type. If `Base` is inaccessible, ambiguous, or virtual base of `Derived` or is a base of some intermediate virtual base of `Derived`, the program is ill-formed.

- If `Derived` does not contain the original member and is not a base class of the class containing the original member, the behavior is undefined.
- Otherwise, the resulting pointer can be dereferenced with a `Derived` object, and it will access the member within the `Base` base subobject of that `Derived` object.

#### Boolean conversions

A prvalue of integral, floating-point, unscoped enumeration, pointer, and pointer-to-member types can be converted to a prvalue of type bool.

The value zero (for integral, floating-point, and unscoped enumeration) and the null pointer and the null pointer-to-member values become false. All other values become true.

|  |  |
| --- | --- |
| In the context of a direct-initialization, a bool object may be initialized from a prvalue of type std::nullptr_t, including nullptr. The resulting value is false. However, this is not considered to be an implicit conversion. | (since C++11) |

### Qualification conversions

Generally speaking:

- A prvalue of type pointer to cv-qualified type `T` can be converted to a prvalue pointer to a more cv-qualified same type `T` (in other words, constness and volatility can be added).
- A prvalue of type pointer to member of cv-qualified type `T` in class `X` can be converted to a prvalue pointer to member of more cv-qualified type `T` in class `X`.

The formal definition of “qualification conversion” is given below.

#### Similar types

Informally, two types are **similar** if, ignoring top-level cv-qualification:

- they are the same type; or
- they are both pointers, and the pointed-to types are similar; or
- they are both pointers to member of the same class, and the types of the pointed-to members are similar; or
- they are both arrays and the array element types are similar.

For example:

- const int\* const \* and int\*\* are similar;
- int (\*)(int\*) and int (\*)(const int\*) are not similar;
- const int (\*)(int\*) and int (\*)(int\*) are not similar;
- int (\*)(int\* const) and int (\*)(int\*) are similar (they are the same type);
- std::pair<int, int> and std::pair<const int, int> are not similar.

Formally, type similarity is defined in terms of qualification-decomposition.

A **qualification-decomposition** of a type `T` is a sequence of components `cv_i` and `P_i` such that `T` is “`cv_0 P_0 cv_1 P_1 ... cv_n−1 P_n−1 cv_n U`” for non-negative n, where

- each `cv_i` is a set of const and volatile, and
- each `P_i` is

:   - “pointer to”,
    - “pointer to member of class `C_i` of type”,
    - “array of N_i”, or
    - “array of unknown bound of”.

If `P_i` designates an array, the cv-qualifiers `cv_i+1` on the element type are also taken as the cv-qualifiers `cv_i` of the array.

```
// T is “pointer to pointer to const int”, it has 3 qualification-decompositions:
// n = 0 -> cv_0 is empty, U is “pointer to pointer to const int”
// n = 1 -> cv_0 is empty, P_0 is “pointer to”,
//          cv_1 is empty, U is “pointer to const int”
// n = 2 -> cv_0 is empty, P_0 is “pointer to”,
//          cv_1 is empty, P_1 is “pointer to”,
//          cv_2 is “const", U is “int”
using T = const int**;
 
// substitute any of the following type to U gives one of the decompositions:
// U = U0 -> the decomposition with n = 0: U0
// U = U1 -> the decomposition with n = 1: pointer to [U1]
// U = U2 -> the decomposition with n = 2: pointer to [pointer to [const U2]]
using U2 = int;
using U1 = const U2*;
using U0 = U1*;

```

Two types `T1` and `T2` are **similar** if there exists a qualification-decomposition for each of them, where all following conditions are satisfied for the two qualification-decompositions:

- They have the same n.
- The types denoted by `U` are the same.
- The corresponding `P_i` components are the same or one is “array of N_i” and the other is “array of unknown bound of”(since C++20) for all i.

```
// the qualification-decomposition with n = 2:
// pointer to [volatile pointer to [const int]]
using T1 = const int* volatile *;
 
// the qualification-decomposition with n = 2:
// const pointer to [pointer to [int]]
using T2 = int** const;
 
// For the two qualification-decompositions above
// although cv_0, cv_1 and cv_2 are all different,
// they have the same n, U, P_0 and P_1,
// therefore types T1 and T2 are similar.

```

#### Combining cv-qualifications

In the description below, the longest qualification-decomposition of type `Tn` is denoted as `Dn`, and its components are denoted as `cvn_i` and `Pn_i`.

|  |  |
| --- | --- |
| A prvalue expression of type `T1` can be converted to type `T2` if all following conditions are satisfied:   - `T1` and `T2` are similar. - For every non-zero i, if const is in `cv1_i`, then const is also in `cv2_i`, and similarly for volatile. - For every non-zero i, if `cv1_i` and `cv2_i` are different, then const is in `cv2_k` for every k in `[`1`,`i`)`.   The **qualification-combined type** of two types `T1` and `T2` is a type `T3` similar to `T1` such that   - `cv3_0` is empty, - for every non-zero i, `cv3_i` is the union of `cv1_i` and `cv2_i`, and - if `cv3_i` is different from `cv1_i` or `c2_i`, then const is added to `cv3_k` for every k in `[`1`,`i`)`. | (until C++20) |
| The **qualification-combined type** of two types `T1` and `T2` is a type `T3` similar to `T1`, where `D3` satisfies all following conditions:   - `cv3_0` is empty. - For every non-zero i, `cv3_i` is the union of `cv1_i` and `cv2_i`. - If `P1_i` or `P2_i` is “array of unknown bound of”, `P3_i` is “array of unknown bound of”, otherwise it is `P1_i`. - If `cv3_i` is different from `cv1_i` or `cv2_i`, or `P3_i` is different from `P1_i` or `P2_i`, then const is added to `cv3_k` for every k in `[`1`,`i`)`.   A prvalue of type `T1` can be converted to type `T2` if the qualification-combined type of `T1` and `T2` is cv-unqualified `T2`. | (since C++20) |

```
// longest qualification-decomposition of T1 (n = 2):
// pointer to [pointer to [char]]
using T1 = char**;
 
// longest qualification-decomposition of T2 (n = 2):
// pointer to [pointer to [const char]]
using T2 = const char**;
 
// Determining the cv3_i and T_i components of D3 (n = 2):
// cv3_1 = empty (union of empty cv1_1 and empty cv2_1)
// cv3_2 = “const” (union of empty cv1_2 and “const” cv2_2)
// P3_0 = “pointer to” (no array of unknown bound, use P1_0)
// P3_1 = “pointer to” (no array of unknown bound, use P1_1)
// All components except cv_2 are the same, cv3_2 is different from cv1_2,
// therefore add “const” to cv3_k for each k in 1, 2): cv3_1 becomes “const”.
// T3 is “pointer to const pointer to const char”, i.e., const char* const *.
using T3 = /* the qualification-combined type of T1 and T2 */;
 
int main()
{
    const char c = 'c';
    char* pc;
    T1 ppc = &pc;
    T2 pcc = ppc; // Error: T3 is not the same as cv-unqualified T2,
                  //        no implicit conversion.
 
    *pcc = &c;
    *pc = 'C';    // If the erroneous assignment above is allowed,
                  // the const object “c” may be modified.
}

```

Note that in the C programming language, const/volatile can be added to the first level only:

```
char** p = 0;
char * const* p1 = p;       // OK in C and C++
const char* const * p2 = p; // error in C, OK in C++

```

|  |  |
| --- | --- |
| Function pointer conversions  - A [prvalue of type pointer to non-throwing function can be converted to a prvalue pointer to potentially-throwing function. - A prvalue of type pointer to non-throwing member function can be converted to a prvalue pointer to potentially-throwing member function.  ```text void (*p)(); void (**pp)() noexcept = &p; // error: cannot convert to pointer to noexcept function   struct S {     typedef void (*p)();     operator p(); }; void (*q)() noexcept = S(); // error: cannot convert to pointer to noexcept function ``` | (since C++17) |

### The safe bool problem

Until C++11, designing a class that should be usable in boolean contexts (e.g. if (obj) { ... }) presented a problem: given a user-defined conversion function, such as T::operator bool() const;, the implicit conversion sequence allowed one additional standard conversion sequence after that function call, which means the resultant bool could be converted to int, allowing such code as obj << 1; or int i = obj;.

One early solution for this can be seen in std::basic_ios, which initially defines operator void\*, so that the code such as if (std::cin) {...} compiles because void\* is convertible to bool, but int n = std::cout; does not compile because void\* is not convertible to int. This still allows nonsense code such as delete std::cout; to compile.

Many pre-C++11 third party libraries were designed with a more elaborate solution, known as the Safe Bool idiom. std::basic_ios also allowed this idiom via LWG issue 468, and operator void\* was replaced (see notes).

Since C++11, explicit bool conversion can also be used to resolve the safe bool problem.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 170 | C++98 | the behavior of pointer-to-member conversions was unclear if the derived class does not have the original member | made clear |
| CWG 172 | C++98 | enumeration type was promoted based on its underlying type | based on its value range instead |
| CWG 330 (N4261) | C++98 | the conversion from double\* const (\*p)[3] to double const \* const (\*p)[3] was invalid | made valid |
| CWG 519 | C++98 | null pointer values were not guaranteed to be preserved when converting to another pointer type | always preserved |
| CWG 616 | C++98 | the behavior of lvalue to rvalue conversion of any uninitialized object and pointer objects of invalid values was always undefined | indeterminate unsigned char is allowed; use of invalid pointers is implementation-defined |
| CWG 685 | C++98 | the underlying type of an enumeration type was not prioritized in integral promotion if it is fixed | prioritized |
| CWG 707 | C++98 | integer to floating point conversion had defined behavior in all cases | the behavior is undefined if the value being converted is out of the destination range |
| CWG 1423 | C++11 | std::nullptr_t was convertible to bool in both direct- and copy-initialization | direct-initialization only |
| CWG 1773 | C++11 | a name expression that appears in a potentially-evaluated expression such that the object named is not odr-used might still be evaluated during an lvalue-to-rvalue conversion | not evaluated |
| CWG 1781 | C++11 | std::nullptr_t to bool was considered an implicit conversion even though it is only valid for direct-initialization | no longer considered an implicit conversion |
| CWG 1787 | C++98 | the behavior of reading from an indeterminate unsigned char cached in a register was undefined | made well-defined |
| CWG 1981 | C++11 | contextual conversions considered explicit conversion functions | not considered |
| CWG 2140 | C++11 | it was unclear whether lvalue-to-rvalue conversions from std::nullptr_t lvalues fetch these lvalues from memory | not fetched |
| CWG 2310 | C++98 | for derived-to-base pointer conversions and base-to-derived pointer-to-member conversions, the derived class type could be incomplete | must be complete |
| CWG 2484 | C++20 | char8_t and char16_t had different integral promotion strategies, but they can fit both of them | char8_t should be promoted in the same way as char16_t |
| CWG 2485 | C++98 | integral promotions involving bit-fields were not specified well | improved the specification |
| CWG 2813 | C++23 | temporary materialization would occur when an explicit object member function of a class prvalue is invoked | will not occur in this case |
| CWG 2861 | C++98 | a pointer to a type-inaccessible object could be converted a pointer to a base class subobject | the behavior is undefined in this case |
| CWG 2879 | C++17 | temporary materialization conversion was applied on prvalue as an operand of an operator that expects glvalue | not applied in some cases |
| CWG 2899 | C++98 | lvalue-to-rvalue conversions could be applied to lvalues designating objects with invalid value representations | the behavior is undefined in this case |
| CWG 2901 | C++98 | the result of lvalue-to-rvalue conversion from an unsigned int lvalue referring to an int object with value -1 was unclear | made clear |

### See also

- `const_cast`
- `static_cast`
- `dynamic_cast`
- `reinterpret_cast`
- explicit cast
- user-defined conversion

|  |  |
| --- | --- |
| C documentation for Implicit conversions | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/implicit_conversion&oldid=179768>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 January 2025, at 23:08.