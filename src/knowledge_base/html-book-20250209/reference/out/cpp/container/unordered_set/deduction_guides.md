# deduction guides for `std::unordered_set`

From cppreference.com
< cpp‎ | container‎ | unordered set
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

`std::unordered_set`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_set::unordered_set | | | | | | unordered_set::~unordered_set | | | | | | unordered_set::operator= | | | | | | unordered_set::get_allocator | | | | | | Iterators | | | | | | unordered_set::beginunordered_set::cbegin | | | | | | unordered_set::endunordered_set::cend | | | | | | Capacity | | | | | | unordered_set::size | | | | | | unordered_set::max_size | | | | | | unordered_set::empty | | | | | | Modifiers | | | | | | unordered_set::clear | | | | | | unordered_set::erase | | | | | | unordered_set::swap | | | | | | unordered_set::extract(C++17) | | | | | | unordered_set::merge(C++17) | | | | | | unordered_set::insert | | | | | | unordered_set::insert_range(C++23) | | | | | | unordered_set::emplace | | | | | | unordered_set::emplace_hint | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_set::count | | | | | | unordered_set::find | | | | | | unordered_set::contains(C++20) | | | | | | unordered_set::equal_range | | | | | | Bucket interface | | | | | | unordered_set::begin(size_type)unordered_set::cbegin(size_type) | | | | | | unordered_set::end(size_type)unordered_set::cend(size_type) | | | | | | unordered_set::bucket_count | | | | | | unordered_set::max_bucket_count | | | | | | unordered_set::bucket_size | | | | | | unordered_set::bucket | | | | | | Hash policy | | | | | | unordered_set::load_factor | | | | | | unordered_set::max_load_factor | | | | | | unordered_set::rehash | | | | | | unordered_set::reserve | | | | | | Observers | | | | | | unordered_set::hash_function | | | | | | unordered_set::key_eq | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_set) | | | | | | erase_if(std::unordered_set)(C++20) | | | | | |
| ****Deduction guides**** (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<unordered_set>` |  |  |
| template<  class InputIt,      class Hash = std::hash<typename std::iterator_traits<InputIt>::value_type>,      class Pred = std::equal_to<typename std::iterator_traits<InputIt>::value_type>,      class Alloc = std::allocator<typename std::iterator_traits<InputIt>::value_type> >  unordered_set( InputIt, InputIt,                 typename /\* see below \*/::size_type = /\* see below \*/,                 Hash = Hash(), Pred = Pred(), Alloc = Alloc() )      -> unordered_set<typename std::iterator_traits<InputIt>::value_type,                      Hash, Pred, Alloc>; | (1) | (since C++17) |
| template< class T,  class Hash = std::hash<T>,            class Pred = std::equal_to<T>,            class Alloc = std::allocator<T> >  unordered_set( std::initializer_list<T>,                 typename /\* see below \*/::size_type = /\* see below \*/,                 Hash = Hash(), Pred = Pred(), Alloc = Alloc() ) -> unordered_set<T, Hash, Pred, Alloc>; | (2) | (since C++17) |
| template< class InputIt, class Alloc >  unordered_set( InputIt, InputIt, typename /\* see below \*/::size_type, Alloc )      -> unordered_set<typename std::iterator_traits<InputIt>::value_type,                       std::hash<typename std::iterator_traits<InputIt>::value_type>,                       std::equal_to<typename std::iterator_traits<InputIt>::value_type>,                      Alloc>; | (3) | (since C++17) |
| template< class InputIt, class Hash, class Alloc >  unordered_set( InputIt, InputIt, typename /\* see below \*/::size_type, Hash, Alloc )      -> unordered_set<typename std::iterator_traits<InputIt>::value_type, Hash,                       std::equal_to<typename std::iterator_traits<InputIt>::value_type>,                      Alloc>; | (4) | (since C++17) |
| template< class T, class Alloc >  unordered_set( std::initializer_list<T>, typename /\* see below \*/::size_type, Alloc ) -> unordered_set<T, std::hash<T>, std::equal_to<T>, Alloc>; | (5) | (since C++17) |
| template< class T, class Hash, class Alloc >  unordered_set( std::initializer_list<T>, typename /\* see below \*/::size_type,                 Hash, Alloc ) -> unordered_set<T, Hash, std::equal_to<T>, Alloc>; | (6) | (since C++17) |
| template< ranges::input_range R,  class Hash = std::hash<ranges::range_value_t<R>>,            class Pred = std::equal_to<ranges::range_value_t<R>>,            class Alloc = std::allocator<ranges::range_value_t<R>> >  unordered_set( std::from_range_t, R&&,                 typename /\* see below \*/::size_type = /\* see below \*/,                 Hash = Hash(), Pred = Pred(), Alloc = Alloc() ) -> unordered_set<ranges::range_value_t<R>, Hash, Pred, Alloc>; | (7) | (since C++23) |
| template< ranges::input_range R, class Alloc >  unordered_set( std::from_range_t, R&&,                 typename /\* see below \*/::size_type, Alloc )      -> unordered_set<ranges::range_value_t<R>, hash<ranges::range_value_t<R>>, std::equal_to<ranges::range_value_t<R>>, Alloc>; | (8) | (since C++23) |
| template< ranges::input_range R, class Alloc >  unordered_set( std::from_range_t, R&&, Alloc )      -> unordered_set<ranges::range_value_t<R>, hash<ranges::range_value_t<R>>, std::equal_to<ranges::range_value_t<R>>, Alloc>; | (9) | (since C++23) |
| template< ranges::input_range R, class Hash, class Alloc >  unordered_set( std::from_range_t, R&&,                 typename /\* see below \*/::size_type, Hash, Alloc )      -> unordered_set<ranges::range_value_t<R>, Hash, std::equal_to<ranges::range_value_t<R>>, Alloc>; | (10) | (since C++23) |
|  |  |  |

1-6) These deduction guides are provided for `unordered_set` to allow deduction from an iterator range (overloads (1,3,4)) and std::initializer_list (overloads (2,5,6)). This overload participates in overload resolution only if `InputIt` satisfies LegacyInputIterator, `Alloc` satisfies Allocator, neither `Hash` nor `Pred` satisfy Allocator, `Hash` is not an integral type.7-10) These deduction guides are provided for `unordered_set` to allow deduction from a std::from_range_t tag and an `input_range`.

Note: the extent to which the library determines that a type does not satisfy LegacyInputIterator is unspecified, except that as a minimum integral types do not qualify as input iterators. Likewise, the extent to which it determines that a type does not satisfy Allocator is unspecified, except that as a minimum the member type `Alloc::value_type` must exist and the expression std::declval<Alloc&>().allocate(std::size_t{}) must be well-formed when treated as an unevaluated operand.

The size_type parameter type in these guides refers to the size_type member type of the type deduced by the deduction guide.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges-aware construction and insertion; overloads (7-10) |

### Example

Run this code

```
#include <unordered_set>
 
int main()
{
    // guide #2 deduces std::unordered_set<int>
    std::unordered_set s = {1, 2, 3, 4};
 
    // guide #1 deduces std::unordered_set<int>
    std::unordered_set s2(s.begin(), s.end());
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_set/deduction_guides&oldid=135884>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 November 2021, at 08:05.