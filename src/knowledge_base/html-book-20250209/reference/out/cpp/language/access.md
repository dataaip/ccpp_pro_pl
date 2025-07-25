# Access specifiers

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class declaration | | | | | | Constructors | | | | | | `this` pointer | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****Access specifiers**** | | | | | | `friend` specifier | | | | | |  | | | | | |
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
| ****Member access specifiers**** | | | | |
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

In a member-specification of a class/struct or union, define the accessibility of subsequent members.

In a base-specifier of a derived class declaration, define the accessibility of inherited members of the subsequent base class.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `public` `:` member-declarations | (1) |  |
|  | | | | | | | | | |
| `protected` `:` member-declarations | (2) |  |
|  | | | | | | | | | |
| `private` `:` member-declarations | (3) |  |
|  | | | | | | | | | |
| public base-class | (4) |  |
|  | | | | | | | | | |
| protected base-class | (5) |  |
|  | | | | | | | | | |
| private base-class | (6) |  |
|  | | | | | | | | | |

1) The members declared after the access specifier have public member access.2) The members declared after the access specifier have protected member access.3) The members declared after the access specifier have private member access.4) Public inheritance: the public and protected members of the base class listed after the access specifier keep their member access in the derived class.5) Protected inheritance: the public and protected members of the base class listed after the access specifier are protected members of the derived class.6) Private inheritance: the public and protected members of the base class listed after the access specifier are private members of the derived class.

The private members of the base class are always inaccessible to the derived class regardless of public, protected, or private inheritance.

### Explanation

The name of every class member (static, non-static, function, type, etc) has an associated "member access". When a name of the member is used anywhere a program, its access is checked, and if it does not satisfy the access rules, the program does not compile:

Run this code

```
#include <iostream>
 
class Example
{
public:             // all declarations after this point are public
    void add(int x) // member "add" has public access
    {
        n += x;     // OK: private Example::n can be accessed from Example::add
    }
private:            // all declarations after this point are private
    int n = 0;      // member "n" has private access
};
 
int main()
{
    Example e;
    e.add(1); // OK: public Example::add can be accessed from main
//  e.n = 7;  // error: private Example::n cannot be accessed from main
}

```

Access specifiers give the author of the class the ability to decide which class members are accessible to the users of the class (that is, the **interface**) and which members are for internal use of the class (the **implementation**).

### In detail

All members of a class (bodies of member functions, initializers of member objects, and the entire nested class definitions) have access to all names the class can access. A local class within a member function has access to all names the member function can access.

A class defined with the keyword `class` has private access for its members and its base classes by default. A class defined with the keyword `struct` has public access for its members and its base classes by default. A union has public access for its members by default.

To grant access to additional functions or classes to protected or private members, a friendship declaration may be used.

Accessibility applies to all names with no regard to their origin, so a name introduced by a typedef or using declarations (except inheriting constructors) is checked, not the name it refers to:

```
class A : X
{
    class B {};   // B is private in A
public:
    typedef B BB; // BB is public
};
 
void f()
{
    A::B y;  // error: A::B is private
    A::BB x; // OK: A::BB is public
}

```

Member access does not affect visibility: names of private and privately-inherited members are visible and considered by overload resolution, implicit conversions to inaccessible base classes are still considered, etc. Member access check is the last step after any given language construct is interpreted. The intent of this rule is that replacing any `private` with `public` never alters the behavior of the program.

Access checking for the names used in default function arguments as well as in the default template parameters is performed at the point of declaration, not at the point of use.

Access rules for the names of virtual functions are checked at the call point using the type of the expression used to denote the object for which the member function is called. The access of the final overrider is ignored:

```
struct B
{
    virtual int f(); // f is public in B
};
 
class D : public B
{
private:
    int f(); // f is private in D
};
 
void f()
{
    D d;
    B& b = d;
 
    b.f(); // OK: B::f is public, D::f is invoked even though it's private
    d.f(); // error: D::f is private
}

```

A name that is private according to unqualified name lookup, may be accessible through qualified name lookup:

```
class A {};
 
class B : private A {};
 
class C : public B
{
    A* p;   // error: unqualified name lookup finds A as the private base of B
    ::A* q; // OK: qualified name lookup finds the namespace-level declaration
};

```

A name that is accessible through multiple paths in the inheritance graph has the access of the path with the most access:

```
class W
{
public:
    void f();
};
 
class A : private virtual W {};
 
class B : public virtual W {};
 
class C : public A, public B
{
    void f()
    {
        W::f(); // OK: W is accessible to C through B
    }
};

```

Any number of access specifiers may appear within a class, in any order.

|  |  |
| --- | --- |
| Member access specifiers may affect class layout: the addresses of non-static data members are only guaranteed to increase in order of declaration for the members not separated by an access specifier(until C++11)with the same access(since C++11). | (until C++23) |

|  |  |
| --- | --- |
| For standard-layout types, all non-static data members must have the same access. | (since C++11) |

When a member is redeclared within the same class, it must do so under the same member access:

```
struct S
{
    class A;    // S::A is public
private:
    class A {}; // error: cannot change access
};

```

### Public member access

Public members form a part of the public interface of a class (other parts of the public interface are the non-member functions found by ADL).

A public member of a class is accessible anywhere:

```
class S
{
public:
    // n, E, A, B, C, U, f are public members
    int n;
    enum E {A, B, C};
    struct U {};
    static void f() {}
};
 
int main()
{
    S::f();     // S::f is accessible in main
 
    S s;
    s.n = S::B; // S::n and S::B are accessible in main
 
    S::U x;     // S::U is accessible in main
}

```

### Protected member access

Protected members form the interface of a class to its derived classes (which is distinct from the public interface of the class).

A protected member of a class is only accessible

1) to the members and friends of that class;2) to the members and friends of any derived class of that class, but only when the class of the object through which the protected member is accessed is that derived class or a derived class of that derived class:

```
struct Base
{
protected:
    int i;
private:
    void g(Base& b, struct Derived& d);
};
 
struct Derived : Base
{
    friend void h(Base& b, Derived& d);
    void f(Base& b, Derived& d) // member function of a derived class
    {
        ++d.i;                  // OK: the type of d is Derived
        ++i;                    // OK: the type of the implied '*this' is Derived
//      ++b.i;                  // error: can't access a protected member through
                                // Base (otherwise it would be possible to change
                                // other derived classes, like a hypothetical
                                // Derived2, base implementation)
    }
};
 
void Base::g(Base& b, Derived& d) // member function of Base
{
    ++i;                          // OK
    ++b.i;                        // OK
    ++d.i;                        // OK
}
 
void h(Base& b, Derived& d) // Friend of Derived
{
    ++d.i;                  // OK: friend of Derived can access a protected 
                            // member through an object of Derived
//  ++b.i;                  // error: friend of Derived is not a friend of Base
}
 
void x(Base& b, Derived& d) // non-member non-friend
{
//  ++b.i;                  // error: no access from non-member
//  ++d.i;                  // error: no access from non-member
}

```

When a pointer to a protected member is formed, it must use a derived class in its declaration:

```
struct Base
{
protected:
    int i;
};
 
struct Derived : Base
{
    void f()
    {
//      int Base::* ptr = &Base::i;    // error: must name using Derived
        int Base::* ptr = &Derived::i; // OK
    }
};

```

### Private member access

Private members form the implementation of a class, as well as the private interface for the other members of the class.

A private member of a class is only accessible to the members and friends of that class, regardless of whether the members are on the same or different instances:

```
class S
{
private:
    int n; // S::n is private
public:
    S() : n(10) {}                    // this->n is accessible in S::S
    S(const S& other) : n(other.n) {} // other.n is accessible in S::S
};

```

The explicit cast (C-style and function-style) allows casting from a derived lvalue to reference to its private base, or from a pointer to derived to a pointer to its private base.

### Inheritance

See derived classes for the meaning of public, protected, and private inheritance.

### Keywords

public,
protected,
private

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 1873 | C++98 | protected members were accessible to friends of derived classes | made inaccessible |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/access&oldid=179970>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 January 2025, at 00:48.