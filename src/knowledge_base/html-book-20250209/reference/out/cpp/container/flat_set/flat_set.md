# std::flat_set<Key,Compare,KeyContainer>::flat_set

From cppreference.com
< cpp‎ | container‎ | flat set
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

std::flat_set

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****flat_set::flat_set**** | | | | | | flat_set::operator= | | | | | | Iterators | | | | | | flat_set::beginflat_set::cbegin | | | | | | flat_set::endflat_set::cend | | | | | | flat_set::rbeginflat_set::crbegin | | | | | | flat_set::rendflat_set::crend | | | | | | Capacity | | | | | | flat_set::size | | | | | | flat_set::max_size | | | | | | flat_set::empty | | | | | | Observers | | | | | | flat_set::key_comp | | | | | | flat_set::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | flat_set::clear | | | | | | flat_set::insert | | | | | | flat_set::insert_range | | | | | | flat_set::emplace | | | | | | flat_set::emplace_hint | | | | | | flat_set::erase | | | | | | flat_set::swap | | | | | | flat_set::extract | | | | | | flat_set::replace | | | | | | Lookup | | | | | | flat_set::count | | | | | | flat_set::find | | | | | | flat_set::contains | | | | | | flat_set::equal_range | | | | | | flat_set::lower_bound | | | | | | flat_set::upper_bound | | | | | | | Non-member functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_set) | | | | | | erase_if(std::flat_set) | | | | | | |
| Helper classes | | | | |
| uses_allocator<std::flat_set> | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| flat_set()      : flat_set(key_compare()) { } | (1) | (since C++23) |
| template< class Allocator >  flat_set( const flat_set& other, const Allocator& alloc ); | (2) | (since C++23) |
| template< class Allocator >  flat_set( flat_set&& other, const Allocator& alloc ); | (3) | (since C++23) |
| explicit flat_set( container_type cont,                     const key_compare& comp = key_compare() ); | (4) | (since C++23) |
| template< class Allocator >  flat_set( const container_type& cont, const Allocator& alloc ); | (5) | (since C++23) |
| template< class Allocator >  flat_set( const container_type& cont, const key_compare& comp, const Allocator& alloc ); | (6) | (since C++23) |
| flat_set( std::sorted_unique_t s, container_type cont,  const key_compare& comp = key_compare() ) : c(std::move(cont)), compare(comp) { } | (7) | (since C++23) |
| template< class Allocator >  flat_set( std::sorted_unique_t s, const container_type& cont, const Allocator& alloc ); | (8) | (since C++23) |
| template< class Allocator >  flat_set( std::sorted_unique_t s, const container_type& cont, const key_compare& comp, const Allocator& alloc ); | (9) | (since C++23) |
| explicit flat_set( const key_compare& comp )      : c(), compare(comp) { } | (10) | (since C++23) |
| template< class Allocator >  flat_set( const key_compare& comp, const Allocator& alloc ); | (11) | (since C++23) |
| template< class Allocator >  explicit flat_set( const Allocator& alloc ); | (12) | (since C++23) |
| template< class InputIter >  flat_set( InputIter first, InputIter last,            const key_compare& comp = key_compare() ) : c(), compare(comp); | (13) | (since C++23) |
| template< class InputIter, class Allocator >  flat_set( InputIter first, InputIter last, const key_compare& comp, const Allocator& alloc ); | (14) | (since C++23) |
| template< class InputIter, class Allocator >  flat_set( InputIter first, InputIter last, const Allocator& alloc ); | (15) | (since C++23) |
| template< container-compatible-range<value_type> R >  flat_set( std::from_range_t, R&& rg, const key_compare& comp ) : flat_set(comp); | (16) | (since C++23) |
| template< container-compatible-range<value_type> R >  flat_set( std::from_range_t fr, R&& rg ) : flat_set( fr, std::forward<R>(rg), key_compare() ) { } | (17) | (since C++23) |
| template< container-compatible-range<value_type> R, class Allocator >  flat_set( std::from_range_t, R&& rg, const Allocator& alloc ); | (18) | (since C++23) |
| template< container-compatible-range<value_type> R, class Allocator >  flat_set( std::from_range_t, R&& rg, const key_compare& comp, const Allocator& alloc ); | (19) | (since C++23) |
| template< class InputIter >  flat_set( std::sorted_unique_t s, InputIter first, InputIter last,            const key_compare& comp = key_compare() ) : c(first, last), compare(comp) { } | (20) | (since C++23) |
| template< class InputIter, class Allocator >  flat_set( std::sorted_unique_t s, InputIter first, InputIter last, const key_compare& comp, const Allocator& alloc ); | (21) | (since C++23) |
| template< class InputIter, class Allocator >  flat_set( std::sorted_unique_t s, InputIter first, InputIter last, const Allocator& alloc ); | (22) | (since C++23) |
| flat_set( std::initializer_list<value_type> init,  const key_compare& comp = key_compare() ) : flat_set(init.begin(), init.end(), comp) { } | (23) | (since C++23) |
| template< class Allocator >  flat_set( std::initializer_list<value_type> init, const key_compare& comp, const Allocator& alloc ); | (24) | (since C++23) |
| template< class Allocator >  flat_set( std::initializer_list<value_type> init, const Allocator& alloc ); | (25) | (since C++23) |
| flat_set( std::sorted_unique_t s, std::initializer_list<value_type> init,  const key_compare& comp = key_compare() ) : flat_set(s, init.begin(), init.end(), comp) { } | (26) | (since C++23) |
| template< class Allocator >  flat_set( std::sorted_unique_t s, std::initializer_list<value_type> init, const key_compare& comp, const Allocator& alloc ); | (27) | (since C++23) |
| template< class Allocator >  flat_set( std::sorted_unique_t s, std::initializer_list<value_type> init, const Allocator& alloc ); | (28) | (since C++23) |
|  |  |  |

Constructs new container adaptor from a variety of data sources and optionally provided comparison function object comp and/or allocator alloc.

1) A default constructor. Constructs an empty container adaptor.2) A copy constructor. Constructs `c` with the copy of the contents of other.c and `compare` with other.compare.
See allocator usage note below.3) A move constructor. Constructs the container adaptor with the contents of other using move semantics.
See allocator usage note below.4) Constructs the underlying container with the contents of the container cont. First, initializes `c` with std::move(cont) and `compare` with comp. Then sorts the `c` with respect to `comp`. Finally, makes elements unique, i.e. erases all but the first element from each group of consecutive equivalent elements.5) Same as (4), equivalent to flat_set(cont);.
See allocator usage note below.6) Same as (4), equivalent to flat_set(cont, comp);.
See allocator usage note below.7) Constructs the underlying container with the contents of the other container cont. Initializes `c` with std::move(cont) and `compare` with comp.8) Same as (7), equivalent to flat_set(s, cont);.
See allocator usage note below.9) Same as (7), equivalent to flat_set(s, cont, comp);.
See allocator usage note below.10) Constructs an empty container adaptor.11,12) Constructs an empty container adaptor.
See allocator usage note below.13) Constructs the container adaptor with the contents of the range ``first`,`last`)`, equivalent to insert(first, last);.14,15) Same as (13).
See [allocator usage note below.16) Constructs the container adaptor with the contents of the range rg. First, uses (10) as delegating constructor. Then initializes `c` with the contents of rg as if by insert_range(std::forward<R>(rg));.17) Same as (16) using it as delegating constructor.18,19) Same as (16).
See allocator usage note below.20) Constructs the underlying container with the contents of the range ``first`,`last`)`. Initializes [`c` with c(first, last) and `compare` with compare(comp).21,22) Same as (20).
See allocator usage note below.23) An initializer-list constructor. Constructs the underlying container with the contents of the initializer list init, using (13) as delegating constructor.24,25) Same as (23).
See allocator usage note below.26) An initializer-list constructor. Constructs the underlying container with the contents of the initializer list init, using (20) as delegating constructor.27,28) Save as (26).
See allocator usage note below.

Note for overloads (13-15,20-22): If ``first`,`last`)` is not a [valid range, the behavior is undefined.

Note for overloads (4-6,13-19,23-25): If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending LWG2844).

##### Allocator usage note

The constructors (2,3,5,6,8,9,11,12,14,15,17,19,21,22,24,25,27,28) are equivalent to the corresponding non-allocator constructors except that `c` is constructed with uses-allocator construction.
These overloads participate in overload resolution only if std::uses_allocator_v<container_type, Allocator> is true.

### Parameters

|  |  |  |
| --- | --- | --- |
| cont | - | a container to be used as source to initialize the underlying container |
| other | - | another `flat_set` to be used as source to initialize the elements of the underlying container with |
| alloc | - | an allocator to use for all memory allocations of the underlying container |
| comp | - | a function object to be used for all comparisons of keys |
| first, last | - | a range to copy the elements from |
| init | - | an initializer list to initialize the elements of the underlying container with |
| rg | - | a container compatible range (that is, an `input_range` whose elements are convertible to `value_type`) to be used as source to initialize the underlying container |
| fr | - | a disambiguation tag that indicates that the contained member should be range constructed |
| s | - | a disambiguation tag that indicates that the input sequence is sorted with respect to `compare` and all its elements are unique |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |
| -`Compare` must meet the requirements of Compare. | | |
| -`Allocator` must meet the requirements of Allocator. | | |

### Complexity

1) Constant.2) Linear in size of other.3) Same as the corresponding move-constructor of the wrapped container, i.e. constant or linear in size of cont.4-6) Linear in \(\scriptsize N\)N if cont is sorted with respect to compare, otherwise \(\scriptsize \mathcal{O}(N\cdot\log{(N)})\)𝓞(N·log(N)), where \(\scriptsize N\)N is the value of cont.size() before this call.7-9) Same as the corresponding move-constructor of the wrapped container, i.e. constant or linear in size of cont.10-12) Constant.13-15) Linear in \(\scriptsize N\)N if the input range `[`first`,`last`)` is sorted with respect to compare, otherwise \(\scriptsize \mathcal{O}(N\cdot\log{(N)})\)𝓞(N·log(N)), where \(\scriptsize N\)N is the value of cont.size() before this call.16-19) Linear in \(\scriptsize N\)N if the input range rg is sorted with respect to compare, otherwise \(\scriptsize \mathcal{O}(N\cdot\log{(N)})\)𝓞(N·log(N)), where \(\scriptsize N\)N is the value of cont.size() before this call.20-22) Linear in size of `[`first`,`last`)`.23-25) Linear in \(\scriptsize N\)N if the elements of init are sorted with respect to compare, otherwise \(\scriptsize \mathcal{O}(N\cdot\log{(N)})\)𝓞(N·log(N)), where \(\scriptsize N\)N is the value of cont.size() before this call.26-28) Linear in size of init.

### Exceptions

Calls to `Allocator::allocate` may throw.

### Notes

After container move construction (overload (3,16-19)), references, pointers, and iterators (other than the end iterator) to `other` remain valid, but refer to elements that are now in \*this. The current standard makes this guarantee via the blanket statement in [[container.reqmts]/67](https://eel.is/c++draft/container.reqmts#67), and a more direct guarantee is under consideration via LWG issue 2321.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| operator= | assigns values to the container adaptor   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_set/flat_set&oldid=171782>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 May 2024, at 15:10.