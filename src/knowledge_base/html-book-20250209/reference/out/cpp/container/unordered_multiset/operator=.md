# std::unordered_multiset<Key,Hash,KeyEqual,Allocator>::operator=

From cppreference.com
< cpp‎ | container‎ | unordered multiset
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

Containers library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Sequence | | | | |
| array(C++11) | | | | |
| vector | | | | |
| vector<bool> | | | | |
| inplace_vector(C++26) | | | | |
| deque | | | | |
| forward_list(C++11) | | | | |
| list | | | | |
| Associative | | | | |
| set | | | | |
| multiset | | | | |
| map | | | | |
| multimap | | | | |
| Unordered associative | | | | |
| unordered_set(C++11) | | | | |
| unordered_multiset(C++11) | | | | |
| unordered_map(C++11) | | | | |
| unordered_multimap(C++11) | | | | |
| Adaptors | | | | |
| stack | | | | |
| queue | | | | |
| priority_queue | | | | |
| flat_set(C++23) | | | | |
| flat_multiset(C++23) | | | | |
| flat_map(C++23) | | | | |
| flat_multimap(C++23) | | | | |
| Views | | | | |
| span(C++20) | | | | |
| mdspan(C++23) | | | | |
| Tables | | | | |
| Iterator invalidation | | | | |
| Member function table | | | | |
| Non-member function table | | | | |

`std::unordered_multiset`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_multiset::unordered_multiset | | | | | | unordered_multiset::~unordered_multiset | | | | | | ****unordered_multiset::operator=**** | | | | | | unordered_multiset::get_allocator | | | | | | Iterators | | | | | | unordered_multiset::beginunordered_multiset::cbegin | | | | | | unordered_multiset::endunordered_multiset::cend | | | | | | Capacity | | | | | | unordered_multiset::size | | | | | | unordered_multiset::max_size | | | | | | unordered_multiset::empty | | | | | | Modifiers | | | | | | unordered_multiset::clear | | | | | | unordered_multiset::insert | | | | | | unordered_multiset::insert_range(C++23) | | | | | | unordered_multiset::emplace | | | | | | unordered_multiset::emplace_hint | | | | | | unordered_multiset::erase | | | | | | unordered_multiset::swap | | | | | | unordered_multiset::extract(C++17) | | | | | | unordered_multiset::merge(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_multiset::count | | | | | | unordered_multiset::find | | | | | | unordered_multiset::contains(C++20) | | | | | | unordered_multiset::equal_range | | | | | | Bucket interface | | | | | | unordered_multiset::begin(size_type)unordered_multiset::cbegin(size_type) | | | | | | unordered_multiset::end(size_type)unordered_multiset::cend(size_type) | | | | | | unordered_multiset::bucket_count | | | | | | unordered_multiset::max_bucket_count | | | | | | unordered_multiset::bucket_size | | | | | | unordered_multiset::bucket | | | | | | Hash policy | | | | | | unordered_multiset::load_factor | | | | | | unordered_multiset::max_load_factor | | | | | | unordered_multiset::rehash | | | | | | unordered_multiset::reserve | | | | | | Observers | | | | | | unordered_multiset::hash_function | | | | | | unordered_multiset::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_multiset) | | | | | | erase_if(std::unordered_multiset)(C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| unordered_multiset& operator=( const unordered_multiset& other ); | (1) | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| unordered_multiset& operator=( unordered_multiset&& other ); |  | (since C++11)  (until C++17) |
| unordered_multiset& operator=( unordered_multiset&& other ) noexcept(/\* see below \*/); |  | (since C++17) |
|  |  |  |
| --- | --- | --- |
| unordered_multiset& operator=( std::initializer_list<value_type> ilist ); | (3) | (since C++11) |
|  |  |  |

Replaces the contents of the container.

1) Copy assignment operator. Replaces the contents with a copy of the contents of other. If std::allocator_traits<allocator_type>::propagate_on_container_copy_assignment::value is true, the allocator of \*this is replaced by a copy of other. If the allocator of \*this after assignment would compare unequal to its old value, the old allocator is used to deallocate the memory, then the new allocator is used to allocate it before copying the elements. Otherwise, the memory owned by \*this may be reused when possible. In any case, the elements originally belonging to \*this may be either destroyed or replaced by element-wise copy-assignment.2) Move assignment operator. Replaces the contents with those of other using move semantics (i.e. the data in other is moved from other into this container). other is in a valid but unspecified state afterwards. If std::allocator_traits<allocator_type>::propagate_on_container_move_assignment::value is true, the allocator of \*this is replaced by a copy of that of other. If it is false and the allocators of \*this and other do not compare equal, \*this cannot take ownership of the memory owned by other and must move-assign each element individually, allocating additional memory using its own allocator as needed. In any case, all elements originally belonging to \*this are either destroyed or replaced by element-wise move-assignment.3) Replaces the contents with those identified by initializer list ilist.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another container to use as data source |
| ilist | - | initializer list to use as data source |

### Return value

\*this

### Complexity

1) Linear in the size of \*this and other.2) Linear in the size of \*this unless the allocators do not compare equal and do not propagate, in which case linear in the size of \*this and other.3) Linear in the size of \*this and ilist.

### Exceptions

|  |  |
| --- | --- |
| 1-3) May throw implementation-defined exceptions. | (until C++17) |
| 1,3) May throw implementation-defined exceptions.2)noexcept specification:noexcept(std::allocator_traits<Allocator>::is_always_equal::value  && std::is_nothrow_move_assignable<Hash>::value && std::is_nothrow_move_assignable<Pred>::value) | (since C++17) |

### Notes

After container move assignment (overload (2)), unless element-wise move assignment is forced by incompatible allocators, references, pointers, and iterators (other than the end iterator) to `other` remain valid, but refer to elements that are now in \*this. The current standard makes this guarantee via the blanket statement in [[container.reqmts]/67](https://eel.is/c++draft/container.reqmts#67), and a more direct guarantee is under consideration via LWG issue 2321.

### Example

The following code uses operator= to assign one std::unordered_multiset to another:

Run this code

```
#include <initializer_list>
#include <iostream>
#include <iterator>
#include <unordered_set>
 
void print(auto const comment, auto const& container)
{
    auto size = std::size(container);
    std::cout << comment << "{ ";
    for (auto const& element : container)
        std::cout << element << (--size ? ", " : " ");
    std::cout << "}\n";
}
 
int main()
{
    std::unordered_multiset<int> x{1, 2, 3}, y, z;
    const auto w = {4, 5, 6, 7};
 
    std::cout << "Initially:\n";
    print("x = ", x);
    print("y = ", y);
    print("z = ", z);
 
    std::cout << "Copy assignment copies data from x to y:\n";
    y = x;
    print("x = ", x);
    print("y = ", y);
 
    std::cout << "Move assignment moves data from x to z, modifying both x and z:\n";
    z = std::move(x);
    print("x = ", x);
    print("z = ", z);
 
    std::cout << "Assignment of initializer_list w to z:\n";
    z = w;
    print("w = ", w);
    print("z = ", z);
}

```

Possible output:

```
Initially:
x = { 3, 2, 1 }
y = { }
z = { }
Copy assignment copies data from x to y:
x = { 3, 2, 1 }
y = { 3, 2, 1 }
Move assignment moves data from x to z, modifying both x and z:
x = { }
z = { 3, 2, 1 }
Assignment of initializer_list w to z:
w = { 4, 5, 6, 7 }
z = { 7, 6, 5, 4 }

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs the `unordered_multiset`   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_multiset/operator%3D&oldid=135867>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 November 2021, at 07:33.