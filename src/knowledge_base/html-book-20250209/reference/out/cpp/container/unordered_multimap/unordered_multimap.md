# std::unordered_multimap<Key,T,Hash,KeyEqual,Allocator>::unordered_multimap

From cppreference.com
< cpp‎ | container‎ | unordered multimap
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

`std::unordered_multimap`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****unordered_multimap::unordered_multimap**** | | | | | | unordered_multimap::~unordered_multimap | | | | | | unordered_multimap::operator= | | | | | | unordered_multimap::get_allocator | | | | | | Iterators | | | | | | unordered_multimap::beginunordered_multimap::cbegin | | | | | | unordered_multimap::endunordered_multimap::cend | | | | | | Capacity | | | | | | unordered_multimap::size | | | | | | unordered_multimap::max_size | | | | | | unordered_multimap::empty | | | | | | Modifiers | | | | | | unordered_multimap::clear | | | | | | unordered_multimap::insert | | | | | | unordered_multimap::insert_range(C++23) | | | | | | unordered_multimap::emplace | | | | | | unordered_multimap::emplace_hint | | | | | | unordered_multimap::erase | | | | | | unordered_multimap::swap | | | | | | unordered_multimap::extract(C++17) | | | | | | unordered_multimap::merge(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_multimap::count | | | | | | unordered_multimap::find | | | | | | unordered_multimap::contains(C++20) | | | | | | unordered_multimap::equal_range | | | | | | Bucket interface | | | | | | unordered_multimap::begin(size_type)unordered_multimap::cbegin(size_type) | | | | | | unordered_multimap::end(size_type)unordered_multimap::cend(size_type) | | | | | | unordered_multimap::bucket_count | | | | | | unordered_multimap::max_bucket_count | | | | | | unordered_multimap::bucket_size | | | | | | unordered_multimap::bucket | | | | | | Hash policy | | | | | | unordered_multimap::load_factor | | | | | | unordered_multimap::max_load_factor | | | | | | unordered_multimap::rehash | | | | | | unordered_multimap::reserve | | | | | | Observers | | | | | | unordered_multimap::hash_function | | | | | | unordered_multimap::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_multimap) | | | | | | erase_if(std::unordered_multimap)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| unordered_multimap()      : unordered_multimap(size_type(/\* unspecified \*/)) {} |  | (since C++11)  (until C++20) |
| unordered_multimap(); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
| explicit unordered_multimap( size_type bucket_count,  const Hash& hash = Hash(),                               const key_equal& equal = key_equal(), const Allocator& alloc = Allocator() ); | (2) | (since C++11) |
| unordered_multimap( size_type bucket_count,  const Allocator& alloc ) : unordered_multimap(bucket_count, Hash(), key_equal(), alloc) {} | (3) | (since C++14) |
| unordered_multimap( size_type bucket_count,  const Hash& hash,                      const Allocator& alloc ) : unordered_multimap(bucket_count, hash, key_equal(), alloc) {} | (4) | (since C++14) |
| explicit unordered_multimap( const Allocator& alloc ); | (5) | (since C++11) |
| template< class InputIt >  unordered_multimap( InputIt first, InputIt last,                      size_type bucket_count = /\* unspecified \*/,                      const Hash& hash = Hash(),                      const key_equal& equal = key_equal(), const Allocator& alloc = Allocator() ); | (6) | (since C++11) |
| template< class InputIt >  unordered_multimap( InputIt first, InputIt last,                      size_type bucket_count,                      const Allocator& alloc )      : unordered_multimap(first, last,                          bucket_count, Hash(), key_equal(), alloc) {} | (7) | (since C++14) |
| template< class InputIt >  unordered_multimap( InputIt first, InputIt last,                      size_type bucket_count,                      const Hash& hash,                      const Allocator& alloc )      : unordered_multimap(first, last,                          bucket_count, hash, key_equal(), alloc) {} | (8) | (since C++14) |
| unordered_multimap( const unordered_multimap& other ); | (9) | (since C++11) |
| unordered_multimap( const unordered_multimap& other, const Allocator& alloc ); | (10) | (since C++11) |
| unordered_multimap( unordered_multimap&& other ); | (11) | (since C++11) |
| unordered_multimap( unordered_multimap&& other, const Allocator& alloc ); | (12) | (since C++11) |
| unordered_multimap( std::initializer_list<value_type> init,                      size_type bucket_count = /\* unspecified \*/,                      const Hash& hash = Hash(),                      const key_equal& equal = key_equal(), const Allocator& alloc = Allocator() ); | (13) | (since C++11) |
| unordered_multimap( std::initializer_list<value_type> init,                      size_type bucket_count,                      const Allocator& alloc )      : unordered_multimap(init, bucket_count,                          Hash(), key_equal(), alloc) {} | (14) | (since C++14) |
| unordered_multimap( std::initializer_list<value_type> init,                      size_type bucket_count,                      const Hash& hash,                      const Allocator& alloc )      : unordered_multimap(init, bucket_count,                          hash, key_equal(), alloc) {} | (15) | (since C++14) |
| template< container-compatible-range<value_type> R >  unordered_multimap( std::from_range_t, R&& rg,                      size_type bucket_count = /\* see description \*/,                      const Hash& hash = Hash(),                      const key_equal& equal = key_equal(), const Allocator& alloc = Allocator() ); | (16) | (since C++23) |
| template< container-compatible-range<value_type> R >  unordered_multimap( std::from_range_t, R&& rg,                      size_type bucket_count,                      const Allocator& alloc )      : unordered_multimap(std::from_range, std::forward<R>(rg),                          bucket_count, Hash(), key_equal(), alloc) {} | (17) | (since C++23) |
| template< container-compatible-range<value_type> R >  unordered_multimap( std::from_range_t, R&& rg,                      size_type bucket_count,                      const Hash& hash,                      const Alloc& alloc )      : unordered_multimap(std::from_range, std::forward<R>(rg),                          bucket_count, hash, key_equal(), alloc) {} | (18) | (since C++23) |
|  |  |  |

Constructs new container from a variety of data sources. Optionally uses user supplied bucket_count as a minimal number of buckets to create, hash as the hash function, equal as the function to compare keys and alloc as the allocator.

1-5) Constructs empty container. Sets max_load_factor() to 1.0. For the default constructor, the number of buckets is unspecified.6-8) Constructs the container with the contents of the range ``first`,`last`)`. Sets [max_load_factor() to 1.0.9,10) Copy constructor. Constructs the container with the copy of the contents of other, copies the load factor, the predicate, and the hash function as well. If alloc is not provided, allocator is obtained by calling std::allocator_traits<allocator_type>::select_on_container_copy_construction(other.get_allocator()).

|  |  |
| --- | --- |
| The template parameter `Allocator` is only deduced from the first argument while used in class template argument deduction. | (since C++23) |

11,12) Move constructor. Constructs the container with the contents of other using move semantics. If alloc is not provided, allocator is obtained by move-construction from the allocator belonging to other.

|  |  |
| --- | --- |
| The template parameter `Allocator` is only deduced from the first argument while used in class template argument deduction. | (since C++23) |

13-15) Initializer-list constructor. Constructs the container with the contents of the initializer list init, same as unordered_multimap(init.begin(), init.end()).16-18) Constructs the container with the contents of rg.

### Parameters

|  |  |  |
| --- | --- | --- |
| alloc | - | allocator to use for all memory allocations of this container |
| bucket_count | - | minimal number of buckets to use on initialization. If it is not specified, an unspecified default value is used |
| hash | - | hash function to use |
| equal | - | comparison function to use for all key comparisons of this container |
| first, last | - | the range ``first`,`last`)` to copy the elements from |
| rg | - | a [container compatible range, that is, an `input_range` whose elements are convertible to `value_type` |
| other | - | another container to be used as source to initialize the elements of the container with |
| init | - | initializer list to initialize the elements of the container with |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |

### Complexity

1-5) Constant.6-8) Average case linear (i.e. O(N), where N is std::distance(first, last)), worst case quadratic, i.e. O(N2).9,10) Linear in size of other.11,12) Constant. If alloc is given and alloc != other.get_allocator(), then linear.13-15) Average case O(N) (N is std::size(init)), worst case O(N2).16-18) Average case O(N) (N is ranges::distance(rg)), worst case O(N2).

### Exceptions

Calls to `Allocator::allocate` may throw.

### Notes

After container move construction (overload (4)), references, pointers, and iterators (other than the end iterator) to `other` remain valid, but refer to elements that are now in \*this. The current standard makes this guarantee via the blanket statement in [[container.reqmts]/67](https://eel.is/c++draft/container.reqmts#67), and a more direct guarantee is under consideration via LWG issue 2321.

Although not formally required until C++23, some implementations have already put the template parameter `Allocator` into non-deduced contexts in earlier modes.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges-aware construction and insertion; overloads (16-18) |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2193 | C++11 | the default constructor (1) was explicit | made non-explicit |
| LWG 2230 | C++11 | the semantics of overload (13) was not specified | specified |

### See also

|  |  |
| --- | --- |
| operator= | assigns values to the container   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_multimap/unordered_multimap&oldid=135912>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 November 2021, at 14:57.