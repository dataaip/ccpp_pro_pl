# std::unique_ptr<T,Deleter>::unique_ptr

From cppreference.com
< cpp‎ | memory‎ | unique ptr
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

Memory management library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **voidify**(exposition only\*) | | | | | | Uninitialized memory algorithms | | | | | | uninitialized_copy | | | | | | uninitialized_fill | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | destroy(C++17) | | | | | | destroy_at(C++17) | | | | | | uninitialized_copy_n(C++11) | | | | | | uninitialized_fill_n | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | destroy_n(C++17) | | | | | | construct_at(C++20) | | | | | | Constrained uninitialized memory algorithms | | | | | | ranges::uninitialized_copy(C++20) | | | | | | ranges::uninitialized_fill(C++20) | | | | | | ranges::uninitialized_move(C++20) | | | | | | ranges::construct_at(C++20) | | | | | | ranges::destroy(C++20) | | | | | | ranges::destroy_n(C++20) | | | | | | ranges::destroy_at(C++20) | | | | | | ranges::uninitialized_copy_n(C++20) | | | | | | ranges::uninitialized_fill_n(C++20) | | | | | | ranges::uninitialized_move_n(C++20) | | | | | | ranges::uninitialized_default_construct(C++20) | | | | | | ranges::uninitialized_value_construct(C++20) | | | | | | ranges::uninitialized_default_construct_n(C++20) | | | | | | ranges::uninitialized_value_construct_n(C++20) | | | | | | C Library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | malloc | | | | | | calloc | | | | | | realloc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | aligned_alloc(C++17) | | | | | | free | | | | | |  | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Allocators | | | | | | allocator | | | | | | allocator_traits(C++11) | | | | | | allocation_result(C++23) | | | | | | allocator_arg(C++11) | | | | | | uses_allocator(C++11) | | | | | | uses_allocator_construction_args(C++20) | | | | | | make_obj_using_allocator(C++20) | | | | | | uninitialized_construct_using_allocator(C++20) | | | | | | scoped_allocator_adaptor(C++11) | | | | | | pmr::polymorphic_allocator(C++17) | | | | | | Memory resources | | | | | | pmr::memory_resource(C++17) | | | | | | pmr::get_default_resource(C++17) | | | | | | pmr::set_default_resource(C++17) | | | | | | pmr::new_delete_resource(C++17) | | | | | | pmr::null_memory_resource(C++17) | | | | | | pmr::synchronized_pool_resource(C++17) | | | | | | pmr::unsynchronized_pool_resource(C++17) | | | | | | pmr::monotonic_buffer_resource(C++17) | | | | | | pmr::pool_options(C++17) | | | | | | Garbage collection support | | | | | | declare_reachable(C++11)(until C++23) | | | | | | undeclare_reachable(C++11)(until C++23) | | | | | | declare_no_pointers(C++11)(until C++23) | | | | | | undeclare_no_pointers(C++11)(until C++23) | | | | | | pointer_safety(C++11)(until C++23) | | | | | | get_pointer_safety(C++11)(until C++23) | | | | | | Uninitialized storage | | | | | | raw_storage_iterator(until C++20\*) | | | | | | get_temporary_buffer(until C++20\*) | | | | | | return_temporary_buffer(until C++20\*) | | | | | | Explicit lifetime management | | | | | | start_lifetime_asstart_lifetime_as_array(C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Smart pointers | | | | | | unique_ptr(C++11) | | | | | | shared_ptr(C++11) | | | | | | weak_ptr(C++11) | | | | | | auto_ptr(until C++17\*) | | | | | | owner_less(C++11) | | | | | | owner_less<void>(C++17) | | | | | | owner_hash(C++26) | | | | | | owner_equal(C++26) | | | | | | enable_shared_from_this(C++11) | | | | | | bad_weak_ptr(C++11) | | | | | | default_delete(C++11) | | | | | | out_ptr_t(C++23) | | | | | | inout_ptr_t(C++23) | | | | | | Low level memory management | | | | | | operator new | | | | | | [operator new[]](../new/operator_new.html "cpp/memory/new/operator new") | | | | | | operator delete | | | | | | [operator delete[]](../new/operator_delete.html "cpp/memory/new/operator delete") | | | | | | get_new_handler(C++11) | | | | | | set_new_handler | | | | | | launder(C++17) | | | | | | bad_alloc | | | | | | bad_array_new_length(C++11) | | | | | | nothrow_t | | | | | | align_val_t(C++17) | | | | | | destroying_delete_t(C++20) | | | | | | new_handler | | | | | | nothrow | | | | | | Miscellaneous | | | | | | pointer_traits(C++11) | | | | | | to_address(C++20) | | | | | | addressof(C++11) | | | | | | align(C++11) | | | | | | assume_aligned(C++20) | | | | | | is_sufficiently_aligned(C++26) | | | | | |

std::unique_ptr

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****unique_ptr::unique_ptr**** | | | | |
| unique_ptr::~unique_ptr | | | | |
| unique_ptr::operator= | | | | |
| Modifiers | | | | |
| unique_ptr::release | | | | |
| unique_ptr::reset | | | | |
| unique_ptr::swap | | | | |
| Observers | | | | |
| unique_ptr::get | | | | |
| unique_ptr::get_deleter | | | | |
| unique_ptr::operator bool | | | | |
| unique_ptr::operator\*unique_ptr::operator-> | | | | |
| [unique_ptr::operator[]](operator_at.html "cpp/memory/unique ptr/operator at") | | | | |
| Non-member functions | | | | |
| make_uniquemake_unique_for_overwrite(C++14)(C++20) | | | | |
| operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(C++20) | | | | |
| operator<<(C++20) | | | | |
| swap(std::unique_ptr) | | | | |
| Helper classes | | | | |
| hash<std::unique_ptr> | | | | |

|  |  |  |
| --- | --- | --- |
| members of the primary template, unique_ptr<T> |  |  |
| constexpr unique_ptr() noexcept;  constexpr unique_ptr( std::nullptr_t ) noexcept; | (1) |  |
| explicit unique_ptr( pointer p ) noexcept; | (2) | (constexpr since C++23) |
| unique_ptr( pointer p, /\* see below \*/ d1 ) noexcept; | (3) | (constexpr since C++23) |
| unique_ptr( pointer p, /\* see below \*/ d2 ) noexcept; | (4) | (constexpr since C++23) |
| unique_ptr( unique_ptr&& u ) noexcept; | (5) | (constexpr since C++23) |
| template< class U, class E >  unique_ptr( unique_ptr<U, E>&& u ) noexcept; | (6) | (constexpr since C++23) |
| unique_ptr( const unique_ptr& ) = delete; | (7) |  |
| template< class U >  unique_ptr( std::auto_ptr<U>&& u ) noexcept; | (8) | (removed in C++17) |
| members of the specialization for arrays, unique_ptr<T[]> |  |  |
| constexpr unique_ptr() noexcept;  constexpr unique_ptr( std::nullptr_t ) noexcept; | (1) |  |
| template< class U >  explicit unique_ptr( U p ) noexcept; | (2) | (constexpr since C++23) |
| template< class U >  unique_ptr( U p, /\* see below \*/ d1 ) noexcept; | (3) | (constexpr since C++23) |
| template< class U >  unique_ptr( U p, /\* see below \*/ d2 ) noexcept; | (4) | (constexpr since C++23) |
| unique_ptr( unique_ptr&& u ) noexcept; | (5) | (constexpr since C++23) |
| template< class U, class E >  unique_ptr( unique_ptr<U, E>&& u ) noexcept; | (6) | (constexpr since C++23) |
| unique_ptr( const unique_ptr& ) = delete; | (7) |  |
|  |  |  |

1) Constructs a `std::unique_ptr` that owns nothing. Value-initializes the stored pointer and the stored deleter. Requires that `Deleter` is DefaultConstructible and that construction does not throw an exception. These overloads participate in overload resolution only if std::is_default_constructible<Deleter>::value is true and Deleter is not a pointer type.2) Constructs a `std::unique_ptr` which owns p, initializing the stored pointer with p and value-initializing the stored deleter. Requires that `Deleter` is DefaultConstructible and that construction does not throw an exception. This overload participates in overload resolution only if std::is_default_constructible<Deleter>::value is true and Deleter is not a pointer type.

|  |  |
| --- | --- |
| This constructor is not selected by class template argument deduction. | (since C++17) |

3,4) Constructs a `std::unique_ptr` object which owns p, initializing the stored pointer with p and initializing a deleter `D` as below (depends upon whether `D` is a reference type).a) If `D` is non-reference type A, then the signatures are:

|  |  |  |
| --- | --- | --- |
| unique_ptr(pointer p, const A& d) noexcept; | (1) | (requires that `Deleter` is nothrow-CopyConstructible) |
| unique_ptr(pointer p, A&& d) noexcept; | (2) | (requires that `Deleter` is nothrow-MoveConstructible) |
|  |  |  |

b) If `D` is an lvalue-reference type A&, then the signatures are:

|  |  |  |
| --- | --- | --- |
| unique_ptr(pointer p, A& d) noexcept; | (1) |  |
| unique_ptr(pointer p, A&& d) = delete; | (2) |  |
|  |  |  |

c) If `D` is an lvalue-reference type const A&, then the signatures are:

|  |  |  |
| --- | --- | --- |
| unique_ptr(pointer p, const A& d) noexcept; | (1) |  |
| unique_ptr(pointer p, const A&& d) = delete; | (2) |  |
|  |  |  |

 In all cases the deleter is initialized from std::forward<decltype(d)>(d). These overloads participate in overload resolution only if std::is_constructible<D, decltype(d)>::value is true.

|  |  |
| --- | --- |
| These two constructors are not selected by class template argument deduction. | (since C++17) |

2-4) In the specialization for arrays behave the same as the constructors that take a pointer parameter in the primary template except that they additionally do not participate in overload resolution unless one of the following is true:

- `U` is the same type as `pointer`, or
- `U` is std::nullptr_t, or
- `pointer` is the same type as `element_type*` and `U` is some pointer type `V*` such that `V(*)[]` is implicitly convertible to `element_type(*)[]`.
5) Constructs a `unique_ptr` by transferring ownership from u to \*this and stores the null pointer in u. This constructor only participates in overload resolution if std::is_move_constructible<Deleter>::value is true. If `Deleter` is not a reference type, requires that it is nothrow-MoveConstructible (if `Deleter` is a reference, `get_deleter()` and `u.get_deleter()` after move construction reference the same value).6) Constructs a `unique_ptr` by transferring ownership from u to \*this, where u is constructed with a specified deleter (`E`). It depends upon whether `E` is a reference type, as following:a) if `E` is a reference type, this deleter is copy constructed from u's deleter (requires that this construction does not throw),b) if `E` is a non-reference type, this deleter is move constructed from u's deleter (requires that this construction does not throw). This constructor only participates in overload resolution if all of the following is true:a) unique_ptr<U, E>::pointer is implicitly convertible to `pointer`,b) U is not an array type,c) either `Deleter` is a reference type and `E` is the same type as `Deleter`, or `Deleter` is not a reference type and `E` is implicitly convertible to `Deleter`.6) In the specialization for arrays behaves the same as in the primary template, except that it will only participate in overload resolution if all of the following is true:

- `U` is an array type,
- `pointer` is the same type as `element_type*`,
- unique_ptr<U,E>::pointer is the same type as unique_ptr<U,E>::element_type\*,
- unique_ptr<U,E>::element_type(\*)[] is convertible to `element_type(*)[]`,
- either `Deleter` is a reference type and `E` is the same type as `Deleter`, or `Deleter` is not a reference type and `E` is implicitly convertible to `Deleter`.
7) Copy constructor is explicitly deleted.8) Constructs a `unique_ptr` where the stored pointer is initialized with u.release() and the stored deleter is value-initialized. This constructor only participates in overload resolution if `U*` is implicitly convertible to `T*` and `Deleter` is the same type as std::default_delete<T>.

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | a pointer to an object to manage |
| d1, d2 | - | a deleter to use to destroy the object |
| u | - | another smart pointer to acquire the ownership from |

### Notes

|  |  |
| --- | --- |
| Instead of using the overload (2) together with new, it is often a better idea to use std::make_unique<T>. | (since C++14) |

std::unique_ptr<Derived> is implicitly convertible to std::unique_ptr<Base> through the overload (6) (because both the managed pointer and std::default_delete are implicitly convertible).

Because the default constructor is constexpr, static unique_ptrs are initialized as part of static non-local initialization, before any dynamic non-local initialization begins. This makes it safe to use a unique_ptr in a constructor of any static object.

|  |  |
| --- | --- |
| There is no class template argument deduction from pointer type because it is impossible to distinguish a pointer obtained from array and non-array forms of new. | (since C++17) |

### Example

Run this code

```
#include <iostream>
#include <memory>
 
struct Foo // object to manage
{
    Foo() { std::cout << "Foo ctor\n"; }
    Foo(const Foo&) { std::cout << "Foo copy ctor\n"; }
    Foo(Foo&&) { std::cout << "Foo move ctor\n"; }
    ~Foo() { std::cout << "~Foo dtor\n"; }
};
 
struct D // deleter
{
    D() {};
    D(const D&) { std::cout << "D copy ctor\n"; }
    D(D&) { std::cout << "D non-const copy ctor\n"; }
    D(D&&) { std::cout << "D move ctor \n"; }
    void operator()(Foo* p) const
    {
        std::cout << "D is deleting a Foo\n";
        delete p;
    };
};
 
int main()
{
    std::cout << "Example constructor(1)...\n";
    std::unique_ptr<Foo> up1; // up1 is empty
    std::unique_ptr<Foo> up1b(nullptr); // up1b is empty
 
    std::cout << "Example constructor(2)...\n";
    {
        std::unique_ptr<Foo> up2(new Foo); //up2 now owns a Foo
    } // Foo deleted
 
    std::cout << "Example constructor(3)...\n";
    D d;
    {   // deleter type is not a reference
        std::unique_ptr<Foo, D> up3(new Foo, d); // deleter copied
    }
    {   // deleter type is a reference
        std::unique_ptr<Foo, D&> up3b(new Foo, d); // up3b holds a reference to d
    }
 
    std::cout << "Example constructor(4)...\n";
    {   // deleter is not a reference
        std::unique_ptr<Foo, D> up4(new Foo, D()); // deleter moved
    }
 
    std::cout << "Example constructor(5)...\n";
    {
        std::unique_ptr<Foo> up5a(new Foo);
        std::unique_ptr<Foo> up5b(std::move(up5a)); // ownership transfer
    }
 
    std::cout << "Example constructor(6)...\n";
    {
        std::unique_ptr<Foo, D> up6a(new Foo, d); // D is copied
        std::unique_ptr<Foo, D> up6b(std::move(up6a)); // D is moved
 
        std::unique_ptr<Foo, D&> up6c(new Foo, d); // D is a reference
        std::unique_ptr<Foo, D> up6d(std::move(up6c)); // D is copied
    }
 
#if (__cplusplus < 201703L)
    std::cout << "Example constructor(7)...\n";
    {
        std::auto_ptr<Foo> up7a(new Foo);
        std::unique_ptr<Foo> up7b(std::move(up7a)); // ownership transfer
    }
#endif
 
    std::cout << "Example array constructor...\n";
    {
        std::unique_ptr<Foo[]> up(new Foo[3]);
    } // three Foo objects deleted
}

```

Output:

```
Example constructor(1)...
Example constructor(2)...
Foo ctor
~Foo dtor
Example constructor(3)...
Foo ctor
D copy ctor
D is deleting a Foo
~Foo dtor
Foo ctor
D is deleting a Foo
~Foo dtor
Example constructor(4)...
Foo ctor
D move ctor
D is deleting a Foo
~Foo dtor
Example constructor(5)...
Foo ctor
~Foo dtor
Example constructor(6)...
Foo ctor
D copy ctor
D move ctor
Foo ctor
D non-const copy ctor
D is deleting a Foo
~Foo dtor
D is deleting a Foo
~Foo dtor
Example constructor(7)...
Foo ctor
~Foo dtor
Example array constructor...
Foo ctor
Foo ctor
Foo ctor
~Foo dtor
~Foo dtor
~Foo dtor

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2118 | C++11 | Constructors of `unique_ptr<T[]>` rejected qualification conversions. | Accept. |
| LWG 2520 | C++11 | `unique_ptr<T[]>` was accidentally made non-constructible from `nullptr_t`. | Made constructible. |
| LWG 2801 | C++11 | The default constructor was not constrained. | Constrained. |
| LWG 2899 | C++11 | The move constructor was not constrained. | Constrained. |
| LWG 2905 | C++11 | Constraint on the constructor from a pointer and a deleter was wrong. | Corrected. |
| LWG 2944 | C++11 | Some preconditions were accidentally dropped by LWG 2905 | Restored. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/memory/unique_ptr/unique_ptr&oldid=179837>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 January 2025, at 08:22.