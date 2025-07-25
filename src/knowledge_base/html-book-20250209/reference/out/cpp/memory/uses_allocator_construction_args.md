# std::uses_allocator_construction_args

From cppreference.com
< cpp‎ | memory
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **voidify**(exposition only\*) | | | | | | Uninitialized memory algorithms | | | | | | uninitialized_copy | | | | | | uninitialized_fill | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | destroy(C++17) | | | | | | destroy_at(C++17) | | | | | | uninitialized_copy_n(C++11) | | | | | | uninitialized_fill_n | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | destroy_n(C++17) | | | | | | construct_at(C++20) | | | | | | Constrained uninitialized memory algorithms | | | | | | ranges::uninitialized_copy(C++20) | | | | | | ranges::uninitialized_fill(C++20) | | | | | | ranges::uninitialized_move(C++20) | | | | | | ranges::construct_at(C++20) | | | | | | ranges::destroy(C++20) | | | | | | ranges::destroy_n(C++20) | | | | | | ranges::destroy_at(C++20) | | | | | | ranges::uninitialized_copy_n(C++20) | | | | | | ranges::uninitialized_fill_n(C++20) | | | | | | ranges::uninitialized_move_n(C++20) | | | | | | ranges::uninitialized_default_construct(C++20) | | | | | | ranges::uninitialized_value_construct(C++20) | | | | | | ranges::uninitialized_default_construct_n(C++20) | | | | | | ranges::uninitialized_value_construct_n(C++20) | | | | | | C Library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | malloc | | | | | | calloc | | | | | | realloc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | aligned_alloc(C++17) | | | | | | free | | | | | |  | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Allocators | | | | | | allocator | | | | | | allocator_traits(C++11) | | | | | | allocation_result(C++23) | | | | | | allocator_arg(C++11) | | | | | | uses_allocator(C++11) | | | | | | ****uses_allocator_construction_args****(C++20) | | | | | | make_obj_using_allocator(C++20) | | | | | | uninitialized_construct_using_allocator(C++20) | | | | | | scoped_allocator_adaptor(C++11) | | | | | | pmr::polymorphic_allocator(C++17) | | | | | | Memory resources | | | | | | pmr::memory_resource(C++17) | | | | | | pmr::get_default_resource(C++17) | | | | | | pmr::set_default_resource(C++17) | | | | | | pmr::new_delete_resource(C++17) | | | | | | pmr::null_memory_resource(C++17) | | | | | | pmr::synchronized_pool_resource(C++17) | | | | | | pmr::unsynchronized_pool_resource(C++17) | | | | | | pmr::monotonic_buffer_resource(C++17) | | | | | | pmr::pool_options(C++17) | | | | | | Garbage collection support | | | | | | declare_reachable(C++11)(until C++23) | | | | | | undeclare_reachable(C++11)(until C++23) | | | | | | declare_no_pointers(C++11)(until C++23) | | | | | | undeclare_no_pointers(C++11)(until C++23) | | | | | | pointer_safety(C++11)(until C++23) | | | | | | get_pointer_safety(C++11)(until C++23) | | | | | | Uninitialized storage | | | | | | raw_storage_iterator(until C++20\*) | | | | | | get_temporary_buffer(until C++20\*) | | | | | | return_temporary_buffer(until C++20\*) | | | | | | Explicit lifetime management | | | | | | start_lifetime_asstart_lifetime_as_array(C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Smart pointers | | | | | | unique_ptr(C++11) | | | | | | shared_ptr(C++11) | | | | | | weak_ptr(C++11) | | | | | | auto_ptr(until C++17\*) | | | | | | owner_less(C++11) | | | | | | owner_less<void>(C++17) | | | | | | owner_hash(C++26) | | | | | | owner_equal(C++26) | | | | | | enable_shared_from_this(C++11) | | | | | | bad_weak_ptr(C++11) | | | | | | default_delete(C++11) | | | | | | out_ptr_t(C++23) | | | | | | inout_ptr_t(C++23) | | | | | | Low level memory management | | | | | | operator new | | | | | | [operator new[]](new/operator_new.html "cpp/memory/new/operator new") | | | | | | operator delete | | | | | | [operator delete[]](new/operator_delete.html "cpp/memory/new/operator delete") | | | | | | get_new_handler(C++11) | | | | | | set_new_handler | | | | | | launder(C++17) | | | | | | bad_alloc | | | | | | bad_array_new_length(C++11) | | | | | | nothrow_t | | | | | | align_val_t(C++17) | | | | | | destroying_delete_t(C++20) | | | | | | new_handler | | | | | | nothrow | | | | | | Miscellaneous | | | | | | pointer_traits(C++11) | | | | | | to_address(C++20) | | | | | | addressof(C++11) | | | | | | align(C++11) | | | | | | assume_aligned(C++20) | | | | | | is_sufficiently_aligned(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<memory>` |  |  |
| `T` is not a specialization of std::pair |  |  |
| template< class T, class Alloc, class... Args >  constexpr auto uses_allocator_construction_args( const Alloc& alloc,     Args&&... args ) noexcept; | (1) | (since C++20) |
| `T` is a specialization of std::pair |  |  |
| template< class T, class Alloc, class Tuple1, class Tuple2 >  constexpr auto uses_allocator_construction_args( const Alloc& alloc, std::piecewise_construct_t, Tuple1&& x, Tuple2&& y ) noexcept; | (2) | (since C++20) |
| template< class T, class Alloc >  constexpr auto uses_allocator_construction_args( const Alloc& alloc ) noexcept; | (3) | (since C++20) |
| template< class T, class Alloc, class U, class V >  constexpr auto uses_allocator_construction_args( const Alloc& alloc,     U&& u, V&& v ) noexcept; | (4) | (since C++20) |
| template< class T, class Alloc, class U, class V >  constexpr auto uses_allocator_construction_args( const Alloc& alloc, std::pair<U, V>& pr ) noexcept; | (5) | (since C++23) |
| template< class T, class Alloc, class U, class V >  constexpr auto uses_allocator_construction_args( const Alloc& alloc, const std::pair<U, V>& pr ) noexcept; | (6) | (since C++20) |
| template< class T, class Alloc, class U, class V >  constexpr auto uses_allocator_construction_args( const Alloc& alloc, std::pair<U, V>&& pr ) noexcept; | (7) | (since C++20) |
| template< class T, class Alloc, class U, class V >  constexpr auto uses_allocator_construction_args( const Alloc& alloc, const std::pair<U, V>&& pr ) noexcept; | (8) | (since C++23) |
| template< class T, class Alloc, class NonPair >  constexpr auto uses_allocator_construction_args( const Alloc& alloc,     NonPair&& non_pair ) noexcept; | (9) | (since C++20) |
|  |  |  |

Prepares the argument list needed to create an object of the given type `T` by means of uses-allocator construction.

1) This overload participates in overload resolution only if `T` is not a specialization of std::pair. Returns std::tuple determined as follows:

- If std::uses_allocator_v<T, Alloc> is false and std::is_constructible_v<T, Args...> is true, returns std::forward_as_tuple(std::forward<Args>(args)...).
- Otherwise, if std::uses_allocator_v<T, Alloc> is true and std::is_constructible_v<T, std::allocator_arg_t, const Alloc&, Args...> is true, returns  
  std::tuple<std::allocator_arg_t, const Alloc&, Args&&...>(std::allocator_arg, alloc,  
                                                            std::forward<Args>(args)...).
- Otherwise, if std::uses_allocator_v<T, Alloc> is true and std::is_constructible_v<T, Args..., const Alloc&> is true, returns std::forward_as_tuple(std::forward<Args>(args)..., alloc).
- Otherwise, the program is ill-formed.
2) This overload participates in overload resolution only if `T` is a specialization of std::pair. For `T` that is std::pair<T1, T2>, equivalent to

```
return std::make_tuple(std::piecewise_construct,
    std::apply(&alloc
        {
            return std::uses_allocator_construction_args<T1>(alloc,
                       std::forward<decltype(args1)>(args1)...);
        }, std::forward<Tuple1>(x)
    ),
    std::apply(&alloc
        {
            return std::uses_allocator_construction_args<T2>(alloc,
                       std::forward<decltype(args2)>(args2)...);
        }, std::forward<Tuple2>(y)
    )
);

```

3) This overload participates in overload resolution only if `T` is a specialization of std::pair. Equivalent to

```
return std::uses_allocator_construction_args<T>(alloc,
    std::piecewise_construct, std::tuple<>{}, std::tuple<>{}
);

```

4) This overload participates in overload resolution only if `T` is a specialization of std::pair. Equivalent to

```
return std::uses_allocator_construction_args<T>(alloc,
    std::piecewise_construct,
    std::forward_as_tuple(std::forward<U>(u)),
    std::forward_as_tuple(std::forward<V>(v))
);

```

5,6) This overload participates in overload resolution only if `T` is a specialization of std::pair. Equivalent to

```
return std::uses_allocator_construction_args<T>(alloc,
    std::piecewise_construct,
    std::forward_as_tuple(pr.first),
    std::forward_as_tuple(pr.second)
);

```

7,8) This overload participates in overload resolution only if `T` is a specialization of std::pair. Equivalent to

```
return std::uses_allocator_construction_args<T>(alloc,
    std::piecewise_construct,
    std::forward_as_tuple(std::get<0>(std::move(pr))),
    std::forward_as_tuple(std::get<1>(std::move(pr)))
);

```

9) This overload participates in overload resolution only if `T` is a specialization of std::pair, and given the exposition-only function template

```
template<class A, class B>
void /*deduce-as-pair*/(const std::pair<A, B>&);

```

, /\*deduce-as-pair\*/(non_pair) is ill-formed when considered as an unevaluated operand.  
Let the exposition-only class `pair-constructor` be defined as

```
class /*pair-constructor*/
{
    const Alloc& alloc_; // exposition only
    NonPair&     u_;     // exposition only
 
    constexpr reconstruct(const std::remove_cv<T>& p) const // exposition only
    {
        return std::make_obj_using_allocator<std::remove_cv<T>>(alloc_, p);
    }
 
    constexpr reconstruct(std::remove_cv<T>&& p) const // exposition only
    {
        return std::make_obj_using_allocator<std::remove_cv<T>>(alloc_, std::move(p));
    }
 
public:
    constexpr operator std::remove_cv<T>() const
    {
        return reconstruct(std::forward<NonPair>(u_));
    }
};

```

This overload is equivalent to return std::make_tuple(pair_construction);, where `pair_construction` is a value of type `pair-constructor` whose `alloc_` and `u_` members are `alloc` and `non_pair` respectively.

### Parameters

|  |  |  |
| --- | --- | --- |
| alloc | - | the allocator to use |
| args | - | the arguments to pass to `T`'s constructor |
| x | - | tuple of arguments to pass to the constructors of `T`'s `first` data member |
| y | - | tuple of arguments to pass to the constructors of `T`'s `second` data member |
| u | - | single argument to pass to the constructor of `T`'s `first` data member |
| v | - | single argument to pass to the constructor of `T`'s `second` data member |
| pr | - | a pair whose `first` data member will be passed to the constructor of `T`'s `first` data member and `second` data member will be passed to the constructor of `T`'s `second` data member |
| non_pair | - | single argument to convert to a std::pair for further construction |

### Return value

std::tuple of arguments suitable for passing to the constructor of `T`.

### Notes

The overloads (2-9) provide allocator propagation into std::pair, which supports neither leading-allocator nor trailing-allocator calling conventions (unlike, e.g. std::tuple, which uses leading-allocator convention).

When used in uses-allocator construction, the conversion function of `pair-constructor` converts the provided argument to std::pair at first, and then constructs the result from that std::pair by uses-allocator construction.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3525 | C++20 | no overload could handle non-`pair` types convertible to `pair` | reconstructing overload added |

### See also

|  |  |
| --- | --- |
| uses_allocator(C++11) | checks if the specified type supports uses-allocator construction   (class template) |
| make_obj_using_allocator(C++20) | creates an object of the given type by means of uses-allocator construction   (function template) |
| uninitialized_construct_using_allocator(C++20) | creates an object of the given type at specified memory location by means of uses-allocator construction   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/memory/uses_allocator_construction_args&oldid=160321>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 October 2023, at 06:52.