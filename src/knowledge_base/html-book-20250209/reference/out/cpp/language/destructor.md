# Destructors

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default constructor | | | | | | Copy constructor | | | | | | Move constructor (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Copy assignment | | | | | | Move assignment (C++11) | | | | | | ****Destructor**** | | | | | |
| Templates | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

 Classes

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| Overview | | | | |
| `class`/`struct` types | | | | |
| `union` types | | | | |
| Injected-class-name | | | | |
| Members | | | | |
| Data members | | | | |
| Static members | | | | |
| The `this` pointer | | | | |
| Nested classes | | | | |
| Member templates | | | | |
| Bit-fields | | | | |
| `using`-declarations | | | | |
| Member functions | | | | |
| Member access specifiers | | | | |
| Constructors and member initializer lists | | | | |
| Default member initializer (C++11) | | | | |
| `friend` specifier | | | | |
| `explicit` specifier | | | | |
| Converting constructor | | | | |
| Special member functions | | | | |
| Default constructor | | | | |
| Copy constructor | | | | |
| Move constructor (C++11) | | | | |
| Copy assignment operator | | | | |
| Move assignment operator (C++11) | | | | |
| ****Destructor**** | | | | |
| Inheritance | | | | |
| Base and derived classes | | | | |
| Empty base optimization (EBO) | | | | |
| Virtual member functions | | | | |
| Pure virtual functions and abstract classes | | | | |
| `override` specifier (C++11) | | | | |
| `final` specifier (C++11) | | | | |

A destructor is a special member function that is called when the lifetime of an object ends. The purpose of the destructor is to free the resources that the object may have acquired during its lifetime.

|  |  |
| --- | --- |
| A destructor cannot be a coroutine. | (since C++20) |

### Syntax

Destructors(until C++20)Prospective destructors(since C++20) are declared using member function declarators of the following form:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| class-name-with-tilde `(` parameter-list ﻿(optional) `)` except ﻿(optional) attr ﻿(optional) |  |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| class-name-with-tilde | - | an identifier expression, possibly followed by a list of attributes, and(since C++11) possibly enclosed by a pair parentheses |
| parameter-list | - | parameter list |
| except | - | |  |  | | --- | --- | | dynamic exception specification | (until C++11) | | either dynamic exception specification or noexcept specification | (since C++11) (until C++17) | | noexcept specification | (since C++17) | |
| attr | - | (since C++11) a list of attributes |

The only specifiers allowed in the declaration specifiers of a prospective(since C++20) destructor declaration are`constexpr`,(since C++11) `friend`, `inline` and `virtual` (in particular, no return type is allowed).

The identifier expression of class-name-with-tilde must have one of the following forms:

- In a member declaration that belongs to the member specification of a class or class template, but is not a friend declaration:

:   - For classes, the identifier expression is ~ followed by the injected-class-name of the immediately-enclosing class.
    - For class templates, the identifier expression is ~ followed by a class name that names the current instantiation(until C++20)the injected-class-name(since C++20) of the immediately-enclosing class template.

- Otherwise, the identifier expression is a qualified identifier whose terminal unqualified identifier is ~ followed by the injected-class name of the class nominated by the non-terminal parts of the qualified identifier.

### Explanation

The destructor is implicitly invoked whenever an object's lifetime ends, which includes

- program termination, for objects with static storage duration

|  |  |
| --- | --- |
| - thread exit, for objects with thread-local storage duration | (since C++11) |

- end of scope, for objects with automatic storage duration and for temporaries whose life was extended by binding to a reference
- delete-expression, for objects with dynamic storage duration
- end of the full expression, for nameless temporaries
- stack unwinding, for objects with automatic storage duration when an exception escapes their block, uncaught.

The destructor can also be invoked explicitly.

### Potentially-invoked destructor

A destructor of a class `C` is **potentially invoked** in the following situations:

- It is invoked explicitly or implicitly.
- A new expression creates an array of objects of type `C`.
- The result object of a return statement is of type `C`.
- An array is under aggregate initialization, and its element type is `C`.
- A class object is under aggregate initialization, and it has a member of type `C` where `C` is not an anonymous union type.
- A potentially constructed subobject is of type `C` in a non-delegating(since C++11) constructor.
- An exception object of type `C` is constructed.

If a potentially-invoked destructor is deleted or(since C++11) not accessible from the context of the invocation, the program is ill-formed.

|  |  |
| --- | --- |
| Prospective destructor A class may have one or more prospective destructors, one of which is selected as the destructor for the class.  In order to determine which prospective destructor is the destructor, at the end of the definition of the class, overload resolution is performed among prospective destructors declared in the class with an empty argument list. If the overload resolution fails, the program is ill-formed. Destructor selection does not odr-use the selected destructor, and the selected destructor may be deleted.  All prospective destructors are special member functions. If no user-declared prospective destructor is provided for class `T`, the compiler will always declare one (see below), and the implicitly declared prospective destructor is also the destructor for `T`. | (since C++20) |

### Implicitly-declared destructor

If no user-declared prospective(since C++20) destructor is provided for a class type, the compiler will always declare a destructor as an inline public member of its class.

As with any implicitly-declared special member function, the exception specification of the implicitly-declared destructor is non-throwing unless the destructor of any potentially-constructed base or member is potentially-throwing(since C++17)implicit definition would directly invoke a function with a different exception specification(until C++17). In practice, implicit destructors are noexcept unless the class is "poisoned" by a base or member whose destructor is noexcept(false).

### Implicitly-defined destructor

If an implicitly-declared destructor is not deleted, it is implicitly defined (that is, a function body is generated and compiled) by the compiler when it is odr-used. This implicitly-defined destructor has an empty body.

|  |  |
| --- | --- |
| If this satisfies the requirements of a constexpr destructor(until C++23)constexpr function(since C++23), the generated destructor is constexpr. | (since C++20) |

### Deleted destructor

The implicitly-declared or explicitly-defaulted destructor for class `T` is  undefined(until C++11)defined as deleted(since C++11) if any of the following conditions is satisfied:

- `T` has a potentially constructed subobject of class type `M` (or possibly multi-dimensional array thereof) such that `M` has a destructor that

:   - is deleted or inaccessible from the destructor of `T`, or
    - in the case of the subobject being a variant member, is non-trivial.

- The destructor is virtual and the lookup for the deallocation function results in

:   - an ambiguity, or
    - a function that is deleted or inaccessible from the destructor.

|  |  |
| --- | --- |
| An explicitly-defaulted prospective destructor for `T` is defined as deleted if it is not the destructor for `T`. | (since C++20) |

### Trivial destructor

The destructor for class `T` is trivial if all of the following is true:

- The destructor is not user-provided (meaning, it is either implicitly declared, or explicitly defined as defaulted on its first declaration).
- The destructor is not virtual (that is, the base class destructor is not virtual).
- All direct base classes have trivial destructors.
- All non-static data members of class type (or array of class type) have trivial destructors.

A trivial destructor is a destructor that performs no action. Objects with trivial destructors don't require a delete-expression and may be disposed of by simply deallocating their storage. All data types compatible with the C language (POD types) are trivially destructible.

### Destruction sequence

For both user-defined or implicitly-defined destructors, after executing the body of the destructor and destroying any automatic objects allocated within the body, the compiler calls the destructors for all non-static non-variant data members of the class, in reverse order of declaration, then it calls the destructors of all direct non-virtual base classes in reverse order of construction (which in turn call the destructors of their members and their base classes, etc), and then, if this object is of most-derived class, it calls the destructors of all virtual bases.

Even when the destructor is called directly (e.g. obj.~Foo();), the return statement in ~Foo() does not return control to the caller immediately: it calls all those member and base destructors first.

### Virtual destructors

Deleting an object through pointer to base invokes undefined behavior unless the destructor in the base class is virtual:

```
class Base
{
public:
    virtual ~Base() {}
};
 
class Derived : public Base {};
 
Base* b = new Derived;
delete b; // safe

```

A common guideline is that a destructor for a base class must be either public and virtual or protected and nonvirtual.

### Pure virtual destructors

A prospective(since C++20) destructor may be declared pure virtual, for example in a base class which needs to be made abstract, but has no other suitable functions that could be declared pure virtual. A pure virtual destructor must have a definition, since all base class destructors are always called when the derived class is destroyed:

```
class AbstractBase
{
public:
    virtual ~AbstractBase() = 0;
};
AbstractBase::~AbstractBase() {}
 
class Derived : public AbstractBase {};
 
// AbstractBase obj; // compiler error
Derived obj;         // OK

```

### Exceptions

As any other function, a destructor may terminate by throwing an exception (this usually requires it to be explicitly declared noexcept(false))(since C++11), however if this destructor happens to be called during stack unwinding, std::terminate is called instead.

Although std::uncaught_exceptions may sometimes be used to detect stack unwinding in progress, it is generally considered bad practice to allow any destructor to terminate by throwing an exception. This functionality is nevertheless used by some libraries, such as SOCI and Galera 3, which rely on the ability of the destructors of nameless temporaries to throw exceptions at the end of the full expression that constructs the temporary.

std::experimental::scope_success in Library fundamental TS v3 may have a potentially-throwing destructor, which throws an exception when the scope is exited normally and the exit function throws an exception.

### Notes

Calling a destructor directly for an ordinary object, such as a local variable, invokes undefined behavior when the destructor is called again, at the end of scope.

In generic contexts, the destructor call syntax can be used with an object of non-class type; this is known as pseudo-destructor call: see member access operator.

### Example

Run this code

```
#include <iostream>
 
struct A
{
    int i;
 
    A(int num) : i(num)
    {
        std::cout << "ctor a" << i << '\n';
    }
 
    ~A()
    {
        std::cout << "dtor a" << i << '\n';
    }
};
 
A a0(0);
 
int main()
{
    A a1(1);
    A* p;
 
    { // nested scope
        A a2(2);
        p = new A(3);
    } // a2 out of scope
 
    delete p; // calls the destructor of a3
}

```

Output:

```
ctor a0
ctor a1
ctor a2
ctor a3
dtor a2
dtor a3
dtor a1
dtor a0

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 193 | C++98 | whether automatic objects in a destructor are destroyed before or after the destruction of the class's base and member subobjects was unspecified | they are destroyed before destroying those subobjects |
| CWG 344 | C++98 | the declarator syntax of destructor was defective (had the same problem as CWG issue 194 and CWG issue 263 | changed the syntax to a specialized function declarator syntax |
| CWG 1241 | C++98 | static members might be destroyed right after destructor execution | only destroy non- static members |
| CWG 1353 | C++98 | the conditions where implicitly-declared destructors are undefined did not consider multi-dimensional array types | consider these types |
| CWG 1435 | C++98 | the meaning of “class name” in the declarator syntax of destructor was unclear | changed the syntax to a specialized function declarator syntax |
| CWG 2180 | C++98 | the destructor of class `X` called the destructors for `X`'s virtual direct base classes | those destructors are not called |
| CWG 2807 | C++20 | the declaration specifiers could contain consteval | prohibited |

### See also

- copy elision
- `new`
- `delete`
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/destructor&oldid=172275>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 June 2024, at 14:13.