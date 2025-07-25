# Injected-class-name

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

 Classes

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| Overview | | | | |
| `class`/`struct` types | | | | |
| `union` types | | | | |
| ****Injected-class-name**** | | | | |
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
| Destructor | | | | |
| Inheritance | | | | |
| Base and derived classes | | | | |
| Empty base optimization (EBO) | | | | |
| Virtual member functions | | | | |
| Pure virtual functions and abstract classes | | | | |
| `override` specifier (C++11) | | | | |
| `final` specifier (C++11) | | | | |

The injected-class-name is the unqualified name of a class within the scope of said class.

In a class template, the injected-class-name can be used either as a template name that refers to the current template, or as a class name that refers to the current instantiation.

### Explanation

In a class scope, the class name of the current class or the template name of the current class template is treated as if it were a public member name; this is called **injected-class-name**. The point of declaration of the name is immediately following the opening brace of the class (template) definition.

```
int X;
 
struct X
{
    void f()
    {
        X* p;   // OK, X is an injected-class-name
        ::X* q; // Error: name lookup finds a variable name, which hides the struct name
    }
};
 
template<class T>
struct Y
{
    void g()
    {
        Y* p;    // OK, Y is an injected-class-name
        Y<T>* q; // OK, Y is an injected-class-name, but Y<T> is not
    }
};

```

Like other members, injected-class-names are inherited. In the presence of private or protected inheritance, the injected-class-name of an indirect base class might end up being inaccessible in a derived class.

```
struct A {};
struct B : private A {};
struct C : public B
{
    A* p;   // Error: injected-class-name A is inaccessible
    ::A* q; // OK, does not use the injected-class-name
};

```

### In class template

The injected-class-name of a class template can be used as a template-name or a type-name.

In the following cases, the injected-class-name is treated as a template-name of the class template itself:

- It is followed by `<`.
- It is used as a template template argument.
- It is the final identifier in the elaborated class specifier of a friend class template declaration.

Otherwise, it is treated as a type-name, and is equivalent to the template-name followed by the template-parameters of the class template enclosed in `<>`.

```
template<template<class, class> class>
struct A;
 
template<class T1, class T2>
struct X
{
    X<T1, T2>* p;   // OK, X is treated as a template-name
 
    using a = A<X>; // OK, X is treated as a template-name
 
    template<class U1, class U2>
    friend class X; // OK, X is treated as a template-name
 
    X* q;           // OK, X is treated as a type-name, equivalent to X<T1, T2>
};

```

Within the scope of a class template specialization or partial specialization, when the injected-class-name is used as a type-name, it is equivalent to the template-name followed by the template-arguments of the class template specialization or partial specialization enclosed in `<>`.

```
template<>
struct X<void, void>
{
    X* p; // OK, X is treated as a type-name, equivalent to X<void, void>
 
    template<class, class>
    friend class X; // OK, X is treated as a template-name (same as in primary template)
 
    X<void, void>* q; // OK, X is treated as a template-name
};
 
template<class T>
struct X<char, T>
{
    X* p, q; // OK, X is treated as a type-name, equivalent to X<char, T>
 
    using r = X<int, int>; // OK, can be used to name another specialization
};

```

The injected-class-name of a class template or class template specialization can be used either as a template-name or a type-name wherever it is in scope.

```
template<>
class X<int, char>
{
    class B
    {
        X a;            // meaning X<int, char>
 
        template<class, class>
        friend class X; // meaning ::X
    };
};
 
template<class T>
struct Base
{
    Base* p; // OK: Base means Base<T>
};
 
template<class T>
struct Derived : public Base<T*>
{
    typename Derived::Base* p; // OK: Derived::Base means Derived<T>::Base,
                               // which is Base<T*>
};
 
template<class T, template<class> class U = T::template Base>
struct Third {};
 
Third<Derived<int>> t; // OK: default argument uses injected-class-name as a template

```

A lookup that finds an injected-class-name can result in an ambiguity in certain cases (for example, if it is found in more than one base class). If all of the injected-class-names that are found refer to specializations of the same class template, and if the name is used as a template-name, the reference refers to the class template itself and not a specialization thereof, and is not ambiguous.

```
template<class T>
struct Base {};
 
template<class T>
struct Derived: Base<int>, Base<char>
{
    typename Derived::Base b;         // error: ambiguous
    typename Derived::Base<double> d; // OK
};

```

### injected-class-name and constructors

Constructors do not have names, but the injected-class-name of the enclosing class is considered to name a constructor in constructor declarations and definitions.

In a qualified name `C::D`, if

- name lookup does not ignore function names, and
- lookup of `D` in the scope of the class `C` finds its injected-class-name

the qualified name is always considered to name `C`'s constructor. Such a name can only be used in the declaration of a constructor (e.g. in a friend constructor declaration, a constructor template specialization, constructor template instantiation, or constructor definition) or be used to inherit constructors(since C++11).

```
struct A
{
    A();
    A(int);
 
    template<class T>
    A(T) {}
};
using A_alias = A;
 
A::A() {}
A_alias::A(int) {}
template A::A(double);
 
struct B : A
{
    using A_alias::A;
};
 
A::A a;         // Error: A::A is considered to name a constructor, not a type
struct A::A a2; // OK, same as 'A a2;'
B::A b;         // OK, same as 'A b;'

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 1004 | C++98 | an injected-class-name could not be a template template argument | allowed, it refers to the class template itself in this case |
| CWG 2637 | C++98 | the entire template-id could be an injected-class-name | only the template name can |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/injected-class-name&oldid=171881>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 May 2024, at 01:15.