# std::unordered_map<Key,T,Hash,KeyEqual,Allocator>::operator[]

From cppreference.com
< cpp‎ | container‎ | unordered map
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

std::unordered_map

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_map::unordered_map | | | | | | unordered_map::~unordered_map | | | | | | unordered_map::operator= | | | | | | unordered_map::get_allocator | | | | | | Iterators | | | | | | unordered_map::beginunordered_map::cbegin | | | | | | unordered_map::endunordered_map::cend | | | | | | Capacity | | | | | | unordered_map::size | | | | | | unordered_map::max_size | | | | | | unordered_map::empty | | | | | | Modifiers | | | | | | unordered_map::clear | | | | | | unordered_map::erase | | | | | | unordered_map::swap | | | | | | unordered_map::extract(C++17) | | | | | | unordered_map::merge(C++17) | | | | | | unordered_map::insert | | | | | | unordered_map::insert_range(C++23) | | | | | | unordered_map::insert_or_assign(C++17) | | | | | | unordered_map::emplace | | | | | | unordered_map::emplace_hint | | | | | | unordered_map::try_emplace(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_map::at | | | | | | ****unordered_map::operator[]**** | | | | | | unordered_map::count | | | | | | unordered_map::find | | | | | | unordered_map::contains(C++20) | | | | | | unordered_map::equal_range | | | | | | Bucket interface | | | | | | unordered_map::begin(size_type)unordered_map::cbegin(size_type) | | | | | | unordered_map::end(size_type)unordered_map::cend(size_type) | | | | | | unordered_map::bucket_count | | | | | | unordered_map::max_bucket_count | | | | | | unordered_map::bucket_size | | | | | | unordered_map::bucket | | | | | | Hash policy | | | | | | unordered_map::load_factor | | | | | | unordered_map::max_load_factor | | | | | | unordered_map::rehash | | | | | | unordered_map::reserve | | | | | | Observers | | | | | | unordered_map::hash_function | | | | | | unordered_map::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_map) | | | | | | erase_if(std::unordered_map)(C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| T& operator[]( const Key& key ); | (1) | (since C++11) |
| T& operator[]( Key&& key ); | (2) | (since C++11) |
| template< class K >  T& operator[]( K&& x ); | (3) | (since C++26) |
|  |  |  |

Returns a reference to the value that is mapped to a key equivalent to key or x respectively, performing an insertion if such key does not already exist.

1) Inserts a `value_type` object constructed in-place from std::piecewise_construct, std::forward_as_tuple(key), std::tuple<>() if the key does not exist. Equivalent to return this->try_emplace(key).first->second;.(since C++17)When the default allocator is used, this results in the key being copy constructed from `key` and the mapped value being value-initialized.

|  |  |  |
| --- | --- | --- |
| -`value_type` must be EmplaceConstructible from std::piecewise_construct, std::forward_as_tuple(key), std::tuple<>(). When the default allocator is used, this means that `key_type` must be CopyConstructible and `mapped_type` must be DefaultConstructible. | | |

2) Inserts a `value_type` object constructed in-place from std::piecewise_construct, std::forward_as_tuple(std::move(key)), std::tuple<>() if the key does not exist. Equivalent to return this->try_emplace(std::move(key)).first->second;.(since C++17)  
When the default allocator is used, this results in the key being move constructed from `key` and the mapped value being value-initialized.

|  |  |  |
| --- | --- | --- |
| -`value_type` must be EmplaceConstructible from std::piecewise_construct, std::forward_as_tuple(std::move(key)), std::tuple<>(). When the default allocator is used, this means that `key_type` must be MoveConstructible and `mapped_type` must be DefaultConstructible. | | |

3) Inserts a `value_type` object constructed in-place if there is no key that transparently compares **equivalent** to the value x. Equivalent to return this->try_emplace(std::forward<K>(x)).first->second;.
This overload participates in overload resolution only if Hash::is_transparent and KeyEqual::is_transparent are valid and each denotes a type. This assumes that such `Hash` is callable with both `K` and `Key` type, and that the `KeyEqual` is transparent, which, together, allows calling this function without constructing an instance of `Key`.

If after the operation the new number of elements is greater than old `max_load_factor()` `*``bucket_count()` a rehashing takes place.  
If rehashing occurs (due to the insertion), all iterators are invalidated. Otherwise (no rehashing), iterators are not invalidated.

### Parameters

|  |  |  |
| --- | --- | --- |
| key | - | the key of the element to find |
| x | - | a value of any type that can be transparently compared with a key |

### Return value

1,2) A reference to the mapped value of the new element if no element with key key existed. Otherwise, a reference to the mapped value of the existing element whose key is equivalent to key.3) A reference to the mapped value of the new element if no element with key that compares equivalent to the value x existed. Otherwise, a reference to the mapped value of the existing element whose key compares equivalent to x.

### Exceptions

If an exception is thrown by any operation, the insertion has no effect.

### Complexity

Average case: constant, worst case: linear in size.

### Notes

In the published C++11 and C++14 standards, this function was specified to require `mapped_type` to be DefaultInsertable and `key_type` to be CopyInsertable or MoveInsertable into \*this. This specification was defective and was fixed by LWG issue 2469, and the description above incorporates the resolution of that issue.

However, one implementation (libc++) is known to construct the `key_type` and `mapped_type` objects via two separate allocator `construct()` calls, as arguably required by the standards as published, rather than emplacing a `value_type` object.

operator[] is non-const because it inserts the key if it doesn't exist. If this behavior is undesirable or if the container is const, `at` may be used.

|  |  |
| --- | --- |
| `insert_or_assign` returns more information than operator[] and does not require default-constructibility of the mapped type. | (since C++17) |

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_associative_heterogeneous_insertion` | `202311L` | (C++26) | Heterogeneous overloads for the remaining member functions in ordered and unordered associative containers. (3) |

### Example

Run this code

```
#include <iostream>
#include <string>
#include <unordered_map>
 
void println(auto const comment, auto const& map)
{
    std::cout << comment << '{';
    for (const auto& pair : map)
        std::cout << '{' << pair.first << ": " << pair.second << '}';
    std::cout << "}\n";
}
 
int main()
{
    std::unordered_map<char, int> letter_counts{{'a', 27}, {'b', 3}, {'c', 1}};
 
    println("letter_counts initially contains: ", letter_counts);
 
    letter_counts['b'] = 42; // updates an existing value
    letter_counts['x'] = 9;  // inserts a new value
 
    println("after modifications it contains: ", letter_counts);
 
    // count the number of occurrences of each word
    // (the first call to operator[] initialized the counter with zero)
    std::unordered_map<std::string, int>  word_map;
    for (const auto& w : {"this", "sentence", "is", "not", "a", "sentence",
                          "this", "sentence", "is", "a", "hoax"})
        ++word_map[w];
    word_map["that"]; // just inserts the pair {"that", 0}
 
    for (const auto& [word, count] : word_map)
        std::cout << count << " occurrence(s) of word '" << word << "'\n";
}

```

Possible output:

```
letter_counts initially contains: {{a: 27}{b: 3}{c: 1}}
after modifications it contains: {{a: 27}{b: 42}{c: 1}{x: 9}}
2 occurrence(s) of word 'a'
1 occurrence(s) of word 'hoax'
2 occurrence(s) of word 'is'
1 occurrence(s) of word 'not'
3 occurrence(s) of word 'sentence'
0 occurrence(s) of word 'that'
2 occurrence(s) of word 'this'

```

### See also

|  |  |
| --- | --- |
| at | access specified element with bounds checking   (public member function) |
| insert_or_assign(C++17) | inserts an element or assigns to the current element if the key already exists   (public member function) |
| try_emplace(C++17) | inserts in-place if the key does not exist, does nothing if the key exists   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_map/operator_at&oldid=136038>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 December 2021, at 08:11.