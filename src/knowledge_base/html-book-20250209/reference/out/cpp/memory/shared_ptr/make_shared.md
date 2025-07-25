# std::make_shared, std::make_shared_for_overwrite

From cppreference.com
< cpp‎ | memory‎ | shared ptr
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

std::shared_ptr

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| shared_ptr::shared_ptr | | | | |
| shared_ptr::~shared_ptr | | | | |
| shared_ptr::operator= | | | | |
| Modifiers | | | | |
| shared_ptr::reset | | | | |
| shared_ptr::swap | | | | |
| Observers | | | | |
| shared_ptr::get | | | | |
| shared_ptr::operator\*shared_ptr::operator-> | | | | |
| [shared_ptr::operator[]](operator_at.html "cpp/memory/shared ptr/operator at")(C++17) | | | | |
| shared_ptr::use_count | | | | |
| shared_ptr::unique(until C++20\*) | | | | |
| shared_ptr::operator bool | | | | |
| shared_ptr::owner_before | | | | |
| shared_ptr::owner_hash(C++26) | | | | |
| shared_ptr::owner_equal(C++26) | | | | |
| Non-member functions | | | | |
| swap(std::shared_ptr) | | | | |
| ****make_sharedmake_shared_for_overwrite****(C++20) | | | | |
| allocate_sharedallocate_shared_for_overwrite(C++20) | | | | |
| static_pointer_castdynamic_pointer_castconst_pointer_castreinterpret_pointer_cast(C++17) | | | | |
| get_deleter | | | | |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | |
| operator<< | | | | |
| atomic_xxxfunctions (until C++26\*) | | | | |
| Helper classes | | | | |
| atomic<std::shared_ptr>(C++20) | | | | |
| hash<std::shared_ptr> | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<memory>` |  |  |
| template< class T, class... Args >  shared_ptr<T> make_shared( Args&&... args ); | (1) | (since C++11)  (T is not array) |
| template< class T >  shared_ptr<T> make_shared( std::size_t N ); | (2) | (since C++20)  (T is U[]) |
| template< class T >  shared_ptr<T> make_shared(); | (3) | (since C++20)  (T is U[N]) |
| template< class T >  shared_ptr<T> make_shared( std::size_t N, const std::remove_extent_t<T>& u ); | (4) | (since C++20)  (T is U[]) |
| template< class T >  shared_ptr<T> make_shared( const std::remove_extent_t<T>& u ); | (5) | (since C++20)  (T is U[N]) |
| template< class T >  shared_ptr<T> make_shared_for_overwrite(); | (6) | (since C++20)  (T is not U[]) |
| template< class T >  shared_ptr<T> make_shared_for_overwrite( std::size_t N ); | (7) | (since C++20)  (T is U[]) |
|  |  |  |

1) Constructs an object of type `T` and wraps it in a std::shared_ptr using args as the parameter list for the constructor of `T`. The object is constructed as if by the expression ::new (pv) T(std::forward<Args>(args)...), where `pv` is an internal void\* pointer to storage suitable to hold an object of type `T`. The storage is typically larger than sizeof(T) in order to use one allocation for both the control block of the shared pointer and the `T` object. The `std::shared_ptr` constructor called by this function enables `shared_from_this` with a pointer to the newly constructed object of type `T`.

|  |  |
| --- | --- |
| This overload participates in overload resolution only if T is not an array type. | (since C++20) |

2,3) Same as (1), but the object constructed is a possibly-multidimensional array whose non-array elements of type std::remove_all_extents_t<T> are value-initialized as if by placement-new expression ::new(pv) std::remove_all_extents_t<T>(). The overload (2) creates an array of size N along the first dimension. The array elements are initialized in ascending order of their addresses, and when their lifetime ends are destroyed in the reverse order of their original construction.4,5) Same as (2,3), but every element is initialized from the default value u. If `U` is not an array type, then this is performed as if by the same placement-new expression as in (1); otherwise, this is performed as if by initializing every non-array element of the (possibly multidimensional) array with the corresponding element from u with the same placement-new expression as in (1). The overload (4) creates an array of size N along the first dimension. The array elements are initialized in ascending order of their addresses, and when their lifetime ends are destroyed in the reverse order of their original construction.6) Same as (1) if `T` is not an array type and (3) if `T` is U[N], except that the created object is default-initialized.7) Same as (2), except that the individual array elements are default-initialized.

In each case, the object (or individual elements if `T` is an array type)(since C++20) will be destroyed by p->~X(), where `p` is a pointer to the object and `X` is its type.

### Parameters

|  |  |  |
| --- | --- | --- |
| args | - | list of arguments with which an instance of `T` will be constructed |
| N | - | array size to use |
| u | - | the initial value to initialize every element of the array |

### Return value

std::shared_ptr of an instance of type `T`.

### Exceptions

May throw std::bad_alloc or any exception thrown by the constructor of `T`. If an exception is thrown, the functions have no effect. If an exception is thrown during the construction of the array, already-initialized elements are destroyed in reverse order.(since C++20)

### Notes

This function may be used as an alternative to std::shared_ptr<T>(new T(args...)). The trade-offs are:

- std::shared_ptr<T>(new T(args...)) performs at least two allocations (one for the object `T` and one for the control block of the shared pointer), while std::make_shared<T> typically performs only one allocation (the standard recommends, but does not require this; all known implementations do this).
- If any std::weak_ptr references the control block created by `std::make_shared` after the lifetime of all shared owners ended, the memory occupied by `T` persists until all weak owners get destroyed as well, which may be undesirable if sizeof(T) is large.
- std::shared_ptr<T>(new T(args...)) may call a non-public constructor of `T` if executed in context where it is accessible, while `std::make_shared` requires public access to the selected constructor.
- Unlike the std::shared_ptr constructors, `std::make_shared` does not allow a custom deleter.
- `std::make_shared` uses ::new, so if any special behavior has been set up using a class-specific operator new, it will differ from std::shared_ptr<T>(new T(args...)).

|  |  |
| --- | --- |
| - std::shared_ptr supports array types (as of C++17), but `std::make_shared` does not. This functionality is supported by `boost::make_shared`. | (until C++20) |

|  |  |
| --- | --- |
| - code such as f(std::shared_ptr<int>(new int(42)), g()) can cause a memory leak if `g` gets called after new int(42) and throws an exception, while f(std::make_shared<int>(42), g()) is safe, since two function calls are never interleaved. | (until C++17) |

A constructor **enables `shared_from_this`** with a pointer ptr of type `U*` means that it determines if `U` has an unambiguous and accessible(since C++17) base class that is a specialization of std::enable_shared_from_this, and if so, the constructor evaluates 
if (ptr != nullptr && ptr->`weak_this` ﻿.expired())  
ptr->`weak_this`= std::shared_ptr<std::remove_cv_t<U>>  
(\*this, const_cast<std::remove_cv_t<U>\*>(ptr));
.

The assignment to the `weak_this` is not atomic and conflicts with any potentially concurrent access to the same object. This ensures that future calls to shared_from_this() would share ownership with the std::shared_ptr created by this raw pointer constructor.

The test ptr->`weak_this` ﻿.expired() in the code above makes sure that `weak_this` is not reassigned if it already indicates an owner. This test is required as of C++17.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_shared_ptr_arrays` | `201707L` | (C++20) | Array support of `std::make_shared`; overloads (2-5) |
| `__cpp_lib_smart_ptr_for_overwrite` | `202002L` | (C++20) | Smart pointer creation with default initialization (std::allocate_shared_for_overwrite, `std::make_shared_for_overwrite`, std::make_unique_for_overwrite); overloads (6,7) |

### Example

Run this code

```
#include <iostream>
#include <memory>
#include <type_traits>
#include <vector>
 
struct C
{
    // constructors needed (until C++20)
    C(int i) : i(i) {}
    C(int i, float f) : i(i), f(f) {}
    int i;
    float f{};
};
 
int main()
{
    // using `auto` for the type of `sp1`
    auto sp1 = std::make_shared<C>(1); // overload (1)
    static_assert(std::is_same_v<decltype(sp1), std::shared_ptr<C>>);
    std::cout << "sp1->{ i:" << sp1->i << ", f:" << sp1->f << " }\n";
 
    // being explicit with the type of `sp2`
    std::shared_ptr<C> sp2 = std::make_shared<C>(2, 3.0f); // overload (1)
    static_assert(std::is_same_v<decltype(sp2), std::shared_ptr<C>>);
    static_assert(std::is_same_v<decltype(sp1), decltype(sp2)>);
    std::cout << "sp2->{ i:" << sp2->i << ", f:" << sp2->f << " }\n";
 
    // shared_ptr to a value-initialized float[64]; overload (2):
    std::shared_ptr<float[]> sp3 = std::make_shared<float[]>(64);
 
    // shared_ptr to a value-initialized long[5][3][4]; overload (2):
    std::shared_ptr<long[][3][4]> sp4 = std::make_shared<long[][3][4]>(5);
 
    // shared_ptr to a value-initialized short[128]; overload (3):
    std::shared_ptr<short[128]> sp5 = std::make_shared<short[128]>();
 
    // shared_ptr to a value-initialized int[7][6][5]; overload (3):
    std::shared_ptr<int[7][6][5]> sp6 = std::make_shared<int[7][6][5]>();
 
    // shared_ptr to a double[256], where each element is 2.0; overload (4):
    std::shared_ptr<double[]> sp7 = std::make_shared<double[]>(256, 2.0);
 
    // shared_ptr to a double[7][2], where each double[2]
    // element is {3.0, 4.0}; overload (4):
    std::shared_ptr<double[][2]> sp8 = std::make_shared<double[][2]>(7, {3.0, 4.0});
 
    // shared_ptr to a vector<int>[4], where each vector
    // has contents {5, 6}; overload (4):
    std::shared_ptr<std::vector<int>[]> sp9 =
        std::make_shared<std::vector<int>[]>(4, {5, 6});
 
    // shared_ptr to a float[512], where each element is 1.0; overload (5):
    std::shared_ptr<float[512]> spA = std::make_shared<float[512]>(1.0);
 
    // shared_ptr to a double[6][2], where each double[2] element
    // is {1.0, 2.0}; overload (5):
    std::shared_ptr<double[6][2]> spB = std::make_shared<double[6][2]>({1.0, 2.0});
 
    // shared_ptr to a vector<int>[4], where each vector
    // has contents {5, 6}; overload (5):
    std::shared_ptr<std::vector<int>[4]> spC =
        std::make_shared<std::vector<int>[4]>({5, 6});
}

```

Output:

```
sp1->{ i:1, f:0 }
sp2->{ i:2, f:3 }

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs new `shared_ptr`   (public member function) |
| allocate_sharedallocate_shared_for_overwrite(C++20) | creates a shared pointer that manages a new object allocated using an allocator   (function template) |
| enable_shared_from_this(C++11) | allows an object to create a `shared_ptr` referring to itself   (class template) |
| make_uniquemake_unique_for_overwrite(C++14)(C++20) | creates a unique pointer that manages a new object   (function template) |
| [operator newoperator new[]](../new/operator_new.html "cpp/memory/new/operator new") | allocation functions   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/memory/shared_ptr/make_shared&oldid=153803>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 June 2023, at 10:13.