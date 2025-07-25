# std::source_location::source_location

From cppreference.com
< cpp‎ | utility‎ | source location
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

Utilities library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

std::source_location

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| Creation | | | | |
| ****source_location::source_location**** | | | | |
| source_location::current | | | | |
| Field access | | | | |
| source_location::line | | | | |
| source_location::column | | | | |
| source_location::file_name | | | | |
| source_location::function_name | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr source_location() noexcept; | (1) | (since C++20) |
| source_location( const source_location& other ); | (2) | (since C++20) |
| source_location( source_location&& other ) noexcept; | (3) | (since C++20) |
|  |  |  |

1) Constructs a `source_location` object of unspecified value.2,3) Copy and move constructors. It is unspecified whether they are trivial and/or constexpr.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another `source_location` to copy or move from |

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <ranges>
#include <source_location>
#include <string_view>
#include <vector>
 
// GCC specific type name printer
#if (__GNUG__ >= 11)
template<typename T>
auto type_name_helper(const std::source_location s = std::source_location::current())
{
    using std::operator""sv;
    const std::string_view fun_name{s.function_name()};
    constexpr auto prefix{"[with T = "sv};
    const auto type_name_begin{fun_name.find(prefix)};
    if (""sv.npos == type_name_begin)
        return ""sv;
    const std::size_t first{type_name_begin + prefix.length()};
    return std::string_view{fun_name.cbegin() + first, fun_name.cend() - 1};
}
 
template<typename T>
auto type_name() { return type_name_helper<T>(); }
#endif
 
void print(std::string_view const comment, std::source_location const l)
{
    std::cout << comment << ":\n"
              << "  file_name     : " << std::quoted(l.file_name()) << '\n'
              << "  function_name : " << std::quoted(l.function_name()) << '\n'
              << "  line          : " << l.line() << '\n'
              << "  column        : " << l.column() << '\n';
}
 
int main()
{
    constexpr std::source_location default_constructed;
    print("default constructed", default_constructed);
 
    constexpr std::source_location current = std::source_location::current();
    print("current", current);
 
#if (__GNUG__ >= 11)
    const std::vector<std::vector<int>> v{{1,2}, {3,4,5}, {6}};
    auto jv = std::ranges::join_view(v);
    std::cout << '\n'
              << '[' << type_name<int>() << "]\n"
              << '[' << type_name<double*>() << "]\n"
              << '[' << type_name<decltype([](){})>() << "]\n"
              << '[' << type_name<decltype(type_name<int>())>() << "]\n"
              << '[' << type_name<decltype(jv)>() << "]\n";
#endif
}

```

Possible output:

```
default constructed:
  file_name     : ""
  function_name : ""
  line          : 0
  column        : 0
current:
  file_name     : "main.cpp"
  function_name : "int main()"
  line          : 39
  column        : 75
 
[int]
[double*]
[main()::<lambda()>]
[std::basic_string_view<char>]
[std::ranges::join_view<std::ranges::ref_view<const std::vector<std::vector<int> > > >]

```

### See also

|  |  |
| --- | --- |
| current[static] | constructs a new `source_location` corresponding to the location of the call site   (public static member function) |
| (constructor) | constructs a new `stacktrace_entry`   (public member function of `std::stacktrace_entry`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/source_location/source_location&oldid=161410>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 October 2023, at 23:39.