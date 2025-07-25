# Lifetime

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

 Basic Concepts

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Comments | | | | |
| ASCII | | | | |
| Punctuation | | | | |
| Names and identifiers | | | | |
| Types | | | | |
| Fundamental types | | | | |
| Objects | | | | |
| Scope | | | | |
| ****Object lifetime**** | | | | |
| Storage duration and linkage | | | | |
| Definitions and ODR | | | | |
| Name lookup | | | | |
| Qualified name lookup | | | | |
| Unqualified name lookup | | | | |
| The as-if rule | | | | |
| Undefined behavior | | | | |
| Memory model | | | | |
| Multi-threaded executions and data races (C++11) | | | | |
| Character sets and encodings | | | | |
| Phases of translation | | | | |
| The `main` function | | | | |
| Modules (C++20) | | | | |

Every object and reference has a **lifetime**, which is a runtime property: for any object or reference, there is a point of execution of a program when its lifetime begins, and there is a moment when it ends.

The lifetime of an object begins when:

- storage with the proper alignment and size for its type is obtained, and
- its initialization (if any) is complete (including default initialization via no constructor or trivial default constructor), except that

:   - if the object is a union member or subobject thereof, its lifetime only begins if that union member is the initialized member in the union, or it is made active,
    - if the object is nested in a union object, its lifetime may begin if the containing union object is assigned or constructed by a trivial special member function,
    - an array object's lifetime may also begin if it is allocated by std::allocator::allocate.

Some operations implicitly create objects of implicit-lifetime types in given region of storage and start their lifetime. If a subobject of an implicitly created object is not of an implicit-lifetime type, its lifetime does not begin implicitly.

The lifetime of an object ends when:

- if it is of a non-class type, the object is destroyed (maybe via a pseudo-destructor call), or
- if it is of a class type, the destructor call starts, or
- the storage which the object occupies is released, or is reused by an object that is not nested within it.

Lifetime of an object is equal to or is nested within the lifetime of its storage, see storage duration.

The lifetime of a reference begins when its initialization is complete and ends as if it were a scalar object.

Note: the lifetime of the referred object may end before the end of the lifetime of the reference, which makes dangling references possible.

Lifetimes of non-static data members and base subobjects begin and end following class initialization order.

### Temporary object lifetime

Temporary objects are created when a prvalue is materialized so that it can be used as a glvalue, which occurs(since C++17) in the following situations:

- binding a reference to a prvalue

|  |  |
| --- | --- |
| - initializing an object of type std::initializer_list<T> from a brace-enclosed initializer list | (since C++11) |

|  |  |  |  |
| --- | --- | --- | --- |
| - returning a prvalue from a function - conversion that creates a prvalue (including T(a, b, c) and T{})  |  |  | | --- | --- | | - lambda expression | (since C++11) |  - copy-initialization that requires conversion of the initializer, - reference-initialization to a different but convertible type or to a bitfield. | (until C++17) |
| - when performing member access on a class prvalue - when performing an array-to-pointer conversion or subscripting on an array prvalue - for unevaluated operands in `sizeof` and `typeid` - when a prvalue appears as a discarded-value expression | (since C++17) |

|  |  |
| --- | --- |
| Also, temporary objects are created:   - if supported by the implementation, when passing or returning an object of trivially-copyable type in a function call expression (this allows passing structs in CPU registers)   The materialization of a temporary object is generally delayed as long as possible in order to avoid creating unnecessary temporary object: see copy elision. | (since C++17) |

All temporary objects are destroyed as the last step in evaluating the full-expression that (lexically) contains the point where they were created, and if multiple temporary objects were created, they are destroyed in the order opposite to the order of creation. This is true even if that evaluation ends in throwing an exception.

There are the following exceptions from that:

- The lifetime of a temporary object may be extended by binding to a reference, see reference initialization for details.
- The lifetime of a temporary object created when evaluating the default arguments of a default or copy constructor used to initialize or copy an element of an array ends before the next element of the array begins initialization.

|  |  |
| --- | --- |
| - The lifetime of a temporary object created in a structured binding declaration (introduced by the initializer for a variable with unique name) is extended to the end of the structured binding declaration. | (since C++17) |
| - The lifetime of a temporary object created in the range-initializer of a range-for statement that would otherwise be destroyed at the end of the range-initializer is extended to the end of the loop body. | (since C++23) |

### Storage reuse

A program is not required to call the destructor of an object to end its lifetime if the object is trivially-destructible (be careful that the correct behavior of the program may depend on the destructor). However, if a program ends the lifetime of a non-trivially destructible object that is a variable explicitly, it must ensure that a new object of the same type is constructed in-place (e.g. via placement new) before the destructor may be called implicitly, i.e. due to scope exit or exception for automatic objects, due to thread exit for thread-local objects,(since C++11) or due to program exit for static objects; otherwise the behavior is undefined.

```
class T {}; // trivial
 
struct B
{
    ~B() {} // non-trivial
};
 
void x()
{
    long long n; // automatic, trivial
    new (&n) double(3.14); // reuse with a different type okay
} // okay
 
void h()
{
    B b; // automatic non-trivially destructible
    b.~B(); // end lifetime (not required, since no side-effects)
    new (&b) T; // wrong type: okay until the destructor is called
} // destructor is called: undefined behavior

```

It is undefined behavior to reuse storage that is or was occupied by a const complete object of static, thread-local,(since C++11) or automatic storage duration because such objects may be stored in read-only memory:

```
struct B
{
    B(); // non-trivial
    ~B(); // non-trivial
};
const B b; // const static
 
void h()
{
    b.~B(); // end the lifetime of b
    new (const_cast<B*>(&b)) const B; // undefined behavior: attempted reuse of a const
}

```

When evaluating a new expression, storage is considered reused after it is returned from the allocation function, but before the evaluation of the initializer of the new expression:

```
struct S
{
    int m;
};
 
void f()
{
    S x{1};
    new(&x) S(x.m); // undefined behavior: the storage is reused
}

```

If a new object is created at the address that was occupied by another object, then all pointers, references, and the name of the original object will automatically refer to the new object and, once the lifetime of the new object begins, can be used to manipulate the new object, but only if the original object is transparently replaceable by the new object.

If all following conditions are satisfied, object x is **transparently replaceable** by object y:

- The storage for y exactly overlays the storage location which x occupied.
- y is of the same type as x (ignoring the top-level cv-qualifiers).
- x is not a complete const object.
- Neither x nor y is a base class subobject, or a member subobject declared with `[[no_unique_address]]`(since C++20).
- One of the following conditions is satisfied:

:   - x and y are both complete objects.
    - x and y are direct subobjects of objects ox and oy respectively, and ox is transparently replaceable by oy.

```
struct C
{
    int i;
    void f();
    const C& operator=(const C&);
};
 
const C& C::operator=(const C& other)
{
    if (this != &other)
    {
        this->~C();          // lifetime of *this ends
        new (this) C(other); // new object of type C created
        f();                 // well-defined
    }
    return *this;
}
 
C c1;
C c2;
c1 = c2; // well-defined
c1.f();  // well-defined; c1 refers to a new object of type C

```

|  |  |
| --- | --- |
| If the conditions listed above are not met, a valid pointer to the new object may still be obtained by applying the pointer optimization barrier std::launder:   ```text struct A {      virtual int transmogrify(); };   struct B : A {     int transmogrify() override { ::new(this) A; return 2; } };   inline int A::transmogrify() { ::new(this) B; return 1; }   void test() {     A i;     int n = i.transmogrify();     // int m = i.transmogrify(); // undefined behavior:     // the new A object is a base subobject, while the old one is a complete object     int m = std::launder(&i)->transmogrify(); // OK     assert(m + n == 3); } ``` | (since C++17) |

Similarly, if an object is created in the storage of a class member or array element, the created object is only a subobject (member or element) of the original object's containing object if:

- the lifetime of the containing object has begun and not ended
- the storage for the new object exactly overlays the storage of the original object
- the new object is of the same type as the original object (ignoring cv-qualification).

|  |  |  |  |
| --- | --- | --- | --- |
| Otherwise, the name of the original subobject cannot be used to access the new object without std::launder:   |  |  | | --- | --- | |  | This section is incomplete Reason: an appropriate example | | (since C++17) |

#### Providing storage

As a special case, objects can be created in arrays of unsigned char or std::byte(since C++17) (in which case it is said that the array **provides storage** for the object) if

- the lifetime of the array has begun and not ended
- the storage for the new object fits entirely within the array
- there is no array object that satisfies these constraints nested within the array.

If that portion of the array previously provided storage for another object, the lifetime of that object ends because its storage was reused, however the lifetime of the array itself does not end (its storage is not considered to have been reused).

```
template<typename... T>
struct AlignedUnion
{
    alignas(T...) unsigned char data[max(sizeof(T)...)];
};
 
int f()
{
    AlignedUnion<int, char> au;
    int *p = new (au.data) int;     // OK, au.data provides storage
    char *c = new (au.data) char(); // OK, ends lifetime of *p
    char *d = new (au.data + 1) char();
    return *c + *d; // OK
}

```

### Access outside of lifetime

Before the lifetime of an object has started but after the storage which the object will occupy has been allocated or, after the lifetime of an object has ended and before the storage which the object occupied is reused or released, the behaviors of the following uses of the glvalue expression that identifies that object are undefined, unless the object is being constructed or destructed (separate set of rules applies):

1. Lvalue to rvalue conversion (e.g. function call to a function that takes a value).
2. Access to a non-static data member or a call to a non-static member function.
3. Binding a reference to a virtual base class subobject.
4. `dynamic_cast` or `typeid` expressions.

The above rules apply to pointers as well (binding a reference to virtual base is replaced by implicit conversion to a pointer to virtual base), with two additional rules:

1. `static_cast` of a pointer to storage without an object is only allowed when casting to (possibly cv-qualified) void\*.
2. Pointers to storage without an object that were cast to possibly cv-qualified void\* can only be `static_cast` to pointers to possibly cv-qualified char, or possibly cv-qualified unsigned char, or possibly cv-qualified std::byte(since C++17).

During construction and destruction it is generally allowed to call non-static member functions, access non-static data members, and use `typeid` and `dynamic_cast`. However, because the lifetime either has not begun yet (during construction) or has already ended (during destruction), only specific operations are allowed. For one restriction, see virtual function calls during construction and destruction.

### Notes

Until the resolution of CWG issue 2256, the end of lifetime rules are different between non-class objects (end of storage duration) and class objects (reverse order of construction):

```
struct A
{
    int* p;
    ~A() { std::cout << *p; } // undefined behavior since CWG2256: n does not outlive a
                              // well-defined until CWG2256: prints 123
};
 
void f()
{
    A a;
    int n = 123; // if n did not outlive a, this could have been optimized out (dead store)
    a.p = &n;
}

```

Until the resolution of RU007, a non-static member of a const-qualified type or a reference type prevents its containing object from being transparently replaceable, which makes std::vector and std::deque hard to implement:

```
struct X { const int n; };
union U { X x; float f; };
 
void tong()
{
    U u = { {1} };
    u.f = 5.f;                          // OK: creates new subobject of 'u'
    X *p = new (&u.x) X {2};            // OK: creates new subobject of 'u'
    assert(p->n == 2);                  // OK
    assert(u.x.n == 2);                 // undefined until RU007:
                                        // 'u.x' does not name the new subobject
    assert(*std::launder(&u.x.n) == 2); // OK even until RU007
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 119 | C++98 | an object of a class type with a non-trivial constructor can only start its lifetime when the constructor call has completed | lifetime also started for other initializations |
| CWG 201 | C++98 | lifetime of a temporary object in a default argument of a default constructor was required to end when the initialization of the array completes | lifetime ends before initializing the next element (also resolves CWG issue 124) |
| CWG 274 | C++98 | an lvalue designating an out-of-lifetime object could be used as the operand of static_cast only if the conversion was ultimately to cv-unqualified char& or unsigned char& | cv-qualified char& and unsigned char& also allowed |
| CWG 597 | C++98 | the following behaviors were undefined: 1. a pointer to an out-of-lifetime object is implicitly converted to a pointer to a non-virtual base class 2. an lvalue referring to an out-of-lifetime object is bound to a reference to a non-virtual base class 3. an lvalue referring to an out-of-lifetime object is used as the operand of a static_cast (with a few exceptions) | made well-defined |
| CWG 2012 | C++98 | lifetime of references was specified to match storage duration, requiring that extern references are alive before their initializers run | lifetime begins at initialization |
| CWG 2107 | C++98 | the resolution of CWG issue 124 was not applied to copy constructors | applied |
| CWG 2256 | C++98 | lifetime of trivially destructible objects were inconsistent with other objects | made consistent |
| CWG 2470 | C++98 | more than one arrays could provide storage for the same object | only one provides |
| CWG 2489 | C++98 | char[] cannot provide storage, but objects could be implicitly created within its storage | objects cannot be implicitly created within  the storage of char[] |
| CWG 2527 | C++98 | if a destructor is not invoked because of reusing storage and the program depends on its side effects, the behavior was undefined | the behavior is well- defined in this case |
| CWG 2721 | C++98 | the exact time point of storage reuse was unclear for placement new | made clear |
| CWG 2849 | C++23 | function parameter objects were considered as temporary objects for range-for loop temporary object lifetime extension | not considered as temporary objects |
| CWG 2854 | C++98 | exception objects were temporary objects | they are not temporary objects |
| CWG 2867 | C++17 | the lifetime of temporary objects created in structured binding declarations were not extended | extended to the end of the declaration |
| P0137R1 | C++98 | creating an object in an array of unsigned char reused its storage | its storage is not reused |
| P0593R6 | C++98 | a pseudo-destructor call had no effects | it destroys the object |
| P1971R0 | C++98 | a non-static data member of a const-qualified type or a reference type prevented its containing object from being transparently replaceable | restriction removed |
| P2103R0 | C++98 | transparently replaceability did not require keeping the original structure | requires |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 6.7.3 Object lifetime [basic.life]

:   - 11.9.5 Construction and destruction [class.cdtor]

- C++20 standard (ISO/IEC 14882:2020):

:   - 6.7.3 Object lifetime [basic.life]

:   - 11.10.4 Construction and destruction [class.cdtor]

- C++17 standard (ISO/IEC 14882:2017):

:   - 6.8 Object lifetime [basic.life]

:   - 15.7 Construction and destruction [class.cdtor]

- C++14 standard (ISO/IEC 14882:2014):

:   - 3 Object lifetime [basic.life]

:   - 12.7 Construction and destruction [class.cdtor]

- C++11 standard (ISO/IEC 14882:2011):

:   - 3.8 Object lifetime [basic.life]

:   - 12.7 Construction and destruction [class.cdtor]

- C++03 standard (ISO/IEC 14882:2003):

:   - 3.8 Object lifetime [basic.life]

:   - 12.7 Construction and destruction [class.cdtor]

- C++98 standard (ISO/IEC 14882:1998):

:   - 3.8 Object lifetime [basic.life]

:   - 12.7 Construction and destruction [class.cdtor]

### See also

|  |  |
| --- | --- |
| C documentation for Lifetime | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/lifetime&oldid=180270>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 February 2025, at 00:41.