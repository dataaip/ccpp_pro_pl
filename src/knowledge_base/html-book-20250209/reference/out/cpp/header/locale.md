# Standard library header <locale>

From cppreference.com
< cpp‎ | header
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

Standard library headers

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | ****<locale>**** | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the text processing library.

|  |  |
| --- | --- |
| Classes | |
| locale | set of polymorphic facets that encapsulate cultural differences   (class) |
| String and stream conversions | |
| wstring_convert(C++11)(deprecated in C++17)(removed in C++26) | performs conversions between a wide string and a byte string   (class template) |
| wbuffer_convert(C++11)(deprecated in C++17)(removed in C++26) | performs conversion between a byte stream buffer and a wide stream buffer   (class template) |
| Facet category base classes | |
| ctype_base | defines character classification categories   (class) |
| codecvt_base | defines character conversion errors   (class) |
| messages_base | defines messages catalog type   (class) |
| time_base | defines date format constants   (class) |
| money_base | defines monetary formatting patterns   (class) |
| Facet categories | |
| ctype | defines character classification tables   (class template) |
| ctype<char> | specialization of std::ctype for type char   (class template specialization) |
| codecvt | converts between character encodings, including UTF-8, UTF-16, UTF-32   (class template) |
| collate | defines lexicographical comparison and hashing of strings   (class template) |
| messages | implements retrieval of strings from message catalogs   (class template) |
| time_get | parses time/date values from an input character sequence into std::tm   (class template) |
| time_put | formats contents of std::tm for output as character sequence   (class template) |
| num_get | parses numeric values from an input character sequence   (class template) |
| num_put | formats numeric values for output as character sequence   (class template) |
| numpunct | defines numeric punctuation rules   (class template) |
| money_get | parses and constructs a monetary value from an input character sequence   (class template) |
| money_put | formats a monetary value for output as a character sequence   (class template) |
| moneypunct | defines monetary formatting parameters used by std::money_get and std::money_put   (class template) |
| Locale-specific facet categories | |
| ctype_byname | represents the system-supplied std::ctype for the named locale   (class template) |
| codecvt_byname | represents the system-supplied std::codecvt for the named locale   (class template) |
| messages_byname | represents the system-supplied std::messages for the named locale   (class template) |
| collate_byname | represents the system-supplied std::collate for the named locale   (class template) |
| time_get_byname | represents the system-supplied std::time_get for the named locale   (class template) |
| time_put_byname | represents the system-supplied std::time_put for the named locale   (class template) |
| numpunct_byname | represents the system-supplied std::numpunct for the named locale   (class template) |
| moneypunct_byname | represents the system-supplied std::moneypunct for the named locale   (class template) |
| Functions | |
| Locales and facets | |
| use_facet | obtains a facet from a locale   (function template) |
| has_facet | checks if a locale implements a specific facet   (function template) |
| Character classification | |
| isspace(std::locale) | checks if a character is classified as whitespace by a locale   (function template) |
| isblank(std::locale)(C++11) | checks if a character is classified as a blank character by a locale   (function template) |
| iscntrl(std::locale) | checks if a character is classified as a control character by a locale   (function template) |
| isupper(std::locale) | checks if a character is classified as uppercase by a locale   (function template) |
| islower(std::locale) | checks if a character is classified as lowercase by a locale   (function template) |
| isalpha(std::locale) | checks if a character is classified as alphabetic by a locale   (function template) |
| isdigit(std::locale) | checks if a character is classified as a digit by a locale   (function template) |
| ispunct(std::locale) | checks if a character is classified as punctuation by a locale   (function template) |
| isxdigit(std::locale) | checks if a character is classified as a hexadecimal digit by a locale   (function template) |
| isalnum(std::locale) | checks if a character is classified as alphanumeric by a locale   (function template) |
| isprint(std::locale) | checks if a character is classified as printable by a locale   (function template) |
| isgraph(std::locale) | checks if a character is classified as graphical by a locale   (function template) |
| Character conversions | |
| toupper(std::locale) | converts a character to uppercase using the ctype facet of a locale   (function template) |
| tolower(std::locale) | converts a character to lowercase using the `ctype` facet of a locale   (function template) |

#### Synopsis

```
namespace std {
 
    // locale:
    class locale;
    template <class Facet> const Facet& use_facet(const locale&);
    template <class Facet> bool has_facet(const locale&) noexcept;
 
    // convenience interfaces:
    template <class CharT> bool isspace (CharT c, const locale& loc);
    template <class CharT> bool isprint (CharT c, const locale& loc);
    template <class CharT> bool iscntrl (CharT c, const locale& loc);
    template <class CharT> bool isupper (CharT c, const locale& loc);
    template <class CharT> bool islower (CharT c, const locale& loc);
    template <class CharT> bool isalpha (CharT c, const locale& loc);
    template <class CharT> bool isdigit (CharT c, const locale& loc);
    template <class CharT> bool ispunct (CharT c, const locale& loc);
    template <class CharT> bool isxdigit(CharT c, const locale& loc);
    template <class CharT> bool isalnum (CharT c, const locale& loc);
    template <class CharT> bool isgraph (CharT c, const locale& loc);
    template <class CharT> CharT toupper(CharT c, const locale& loc);
    template <class CharT> CharT tolower(CharT c, const locale& loc);
    template <class Codecvt, class Elem = wchar_t,
              class Wide_alloc = std::allocator<Elem>,
        class Byte_alloc = std::allocator<char>> class wstring_convert;
    template <class Codecvt, class Elem = wchar_t,
              class Tr = char_traits<Elem>> class wbuffer_convert;
 
    // ctype:
    class ctype_base;
    template <class CharT> class ctype;
    template <>            class ctype<char>; // specialization
    template <class CharT> class ctype_byname;
    class codecvt_base;
    template <class internT, class externT, class stateT> class codecvt;
    template <class internT, class externT, class stateT> class codecvt_byname;
 
    // numeric:
    template <class CharT, class InputIter = istreambuf_iterator<CharT>> class num_get;
    template <class CharT, class OutputIter = osterambuf_iterator<CharT>> class num_put;
    template <class CharT> class numpunct;
    template <class CharT> class numpunct_byname;
 
    // collation:
    template <class CharT> class collate;
    template <class CharT> class collate_byname;
 
    // date and time:
    class time_base;
    template <class CharT, class InputIter = istreambuf_iterator<CharT>>
        class time_get;
    template <class CharT, class InputIter> = istreambuf_iterator<CharT>>
        class time_get_byname;
    template <class CharT, class OutputIter> = ostreambuf_iterator<CharT>>
        class time_put;
    template <class CharT, class OutputIter> = ostreambuf_iterator<CharT>>
        class time_put_byname;
 
    // money:
    class money_base;
    template <class CharT, class InputIter = istreambuf_iterator<CharT>> >
        class money_get;
    template <class CharT, class OutputIter = ostreambuf_iterator<CharT>> >
        class money_put;
    template <class CharT, bool Intl = false> class moneypunct;
    template <class CharT, bool Intl = false> class moneypunct_byname;
 
    // message retrieval:
    class messages_base;
    template <class CharT> class messages;
    template <class CharT> class messages_byname;
}

```

#### Class std::locale

```
class locale
{
public:
    // types:
    class facet;
    class id;
    typedef int category;
    static const category // values assigned here are for exposition only
        none     = 0,
        collate  = 0x010,
        ctype    = 0x020,
        monetary = 0x040,
        numeric  = 0x080,
        time     = 0x100,
        messages = 0x200,
        all = collate | ctype | monetary | numeric | time | messages;
 
    // construct/copy/destroy:
    locale() noexcept;
    locale(const locale& other) noexcept;
    explicit locale(const char* std_name);
    explicit locale(const string& std_name);
    locale(const locale& other, const char* std_name, category);
    locale(const locale& other, const string& std_name, category);
    template <class Facet> locale(const locale& other, Facet* f);
    locale(const locale& other, const locale& one, category);
    ~locale();
 
    // not virtual
    const locale& operator=(const locale& other) noexcept;
    template <class Facet> locale combine(const locale& other) const;
 
    // locale operations:
    basic_string<char>
    name() const;
    bool operator==(const locale& other) const;
    bool operator!=(const locale& other) const;
    template <class CharT, class Traits, class Allocator>
    bool operator()(const basic_string<CharT,Traits,Allocator>& s1,
                    const basic_string<CharT,Traits,Allocator>& s2) const;
 
    // global locale objects:
    static
    locale global(const locale&);
    static const locale& classic();
};

```

#### Class std::ctype_base

```
class ctype_base
{
public:
    typedef /*bitmask-type*/ mask;
 
    // numeric values are for exposition only.
    static const mask space = 1 << 0;
    static const mask print = 1 << 1;
    static const mask cntrl = 1 << 2;
    static const mask upper = 1 << 3;
    static const mask lower = 1 << 4;
    static const mask alpha = 1 << 5;
    static const mask digit = 1 << 6;
    static const mask punct = 1 << 7;
    static const mask xdigit= 1 << 8;
    static const mask blank = 1 << 9;
    static const mask alnum = alpha | digit;
    static const mask graph = alnum | punct;
};

```

#### Class std::ctype

```
template <class CharT>
class ctype : public locale::facet, public ctype_base
{
public:
    typedef CharT char_type;
 
    explicit ctype(size_t refs = 0);
 
    bool is(mask m, CharT c) const;
    const CharT* is(const CharT* low, const CharT* high, mask* vec) const;
    const CharT* scan_is(mask m,
                         const CharT* low, const CharT* high) const;
    const CharT* scan_not(mask m,
                          const CharT* low, const CharT* high) const;
 
    CharT        toupper(CharT c) const;
    const CharT* toupper(CharT* low, const CharT* high) const;
    CharT        tolower(CharT c) const;
    const CharT* tolower(CharT* low, const CharT* high) const;
 
    CharT        widen(char c) const;
    const char*  widen(const char* low, const char* high, CharT* to) const;
    char         narrow(CharT c, char dfault) const;
    const CharT* narrow(const CharT* low, const CharT*, char dfault,
                        char* to) const;
 
    static locale::id id;
 
protected:
    ~ctype();
    virtual bool do_is(mask m, CharT c) const;
    virtual const CharT* do_is(const CharT* low, const CharT* high,
                               mask* vec) const;
    virtual const CharT* do_scan_is(mask m,
                                    const CharT* low, const CharT* high) const;
    virtual const CharT* do_scan_not(mask m,
                                     const CharT* low, const CharT* high) const;
 
    virtual CharT do_toupper(CharT) const;
    virtual const CharT* do_toupper(CharT* low, const CharT* high) const;
    virtual CharT do_tolower(CharT) const;
    virtual const CharT* do_tolower(CharT* low, const CharT* high) const;
    virtual CharT do_widen(char) const;
    virtual const char*  do_widen(const char* low, const char* high,
                                  CharT* dest) const;
    virtual char do_narrow(CharT, char dfault) const;
    virtual const CharT* do_narrow(const CharT* low, const CharT* high,
                                   char dfault, char* dest) const;
};

```

#### Class std::ctype_byname

```
template <class CharT>
class ctype_byname : public ctype<CharT>
{
public:
    typedef typename ctype<CharT>::mask mask;
    explicit ctype_byname(const char*, size_t refs = 0);
    explicit ctype_byname(const string&, size_t refs = 0);
    protected:
    ~ctype_byname();
};

```

#### Class std::ctype<char>

```
template <> class ctype<char>
    : public locale::facet, public ctype_base
{
public:
    typedef char char_type;
    explicit ctype(const mask* tab = 0, bool del = false,
                   size_t refs = 0);
    bool is(mask m, char c) const;
    const char* is(const char* low, const char* high, mask* vec) const;
    const char* scan_is (mask m,
                         const char* low, const char* high) const;
    const char* scan_not(mask m,
                         const char* low, const char* high) const;
    char        toupper(char c) const;
    const char* toupper(char* low, const char* high) const;
    char        tolower(char c) const;
    const char* tolower(char* low, const char* high) const;
    char        widen(char c) const;
    const char* widen(const char* low, const char* high, char* to) const;
    char        narrow(char c, char dfault) const;
    const char* narrow(const char* low, const char* high, char dfault,
                       char* to) const;
 
    static locale::id id;
 
    static const size_t table_size = /* implementation-defined */;
    const mask* table() const noexcept;
    static const mask* classic_table() noexcept;
 
protected:
    ~ctype();
    virtual char        do_toupper(char c) const;
    virtual const char* do_toupper(char* low, const char* high) const;
    virtual char        do_tolower(char c) const;
    virtual const char* do_tolower(char* low, const char* high) const;
    virtual char        do_widen(char c) const;
    virtual const char* do_widen(const char* low,
                                 const char* high,
                                 char* to) const;
    virtual char        do_narrow(char c, char dfault) const;
    virtual const char* do_narrow(const char* low,
                                  const char* high,
                                  char dfault, char* to) const;
};

```

#### Class std::codecvt_base

```
class codecvt_base
{
public:
    enum result { ok, partial, error, noconv };
};

```

#### Class std::codecvt

```
template <class internT, class externT, class stateT>
class codecvt : public locale::facet, public codecvt_base
{
public:
    typedef internT intern_type;
    typedef externT extern_type;
    typedef stateT state_type;
    explicit codecvt(size_t refs = 0);
    result out(stateT& state,
               const internT* from, const internT* from_end,
               const internT*& from_next,
               externT* to, externT* to_end, externT*& to_next) const;
    result unshift(stateT& state, externT* to,
                   externT* to_end, externT*& to_next) const;
    result in(stateT& state,
              const externT* from, const externT* from_end,
              const externT*& from_next,
              internT* to,
              internT* to_end, internT*& to_next) const;
    int encoding() const noexcept;
    bool always_noconv() const noexcept;
    int length(stateT&, const externT* from, const externT* end,
               size_t max) const;
    int max_length() const noexcept;
    static locale::id id;
protected:
    ~codecvt();
    virtual result do_out(stateT& state,
                          const internT* from, const internT* from_end,
                          const internT*& from_next,
                          externT* to,
                          externT* to_end, externT*& to_next) const;
    virtual result do_in(stateT& state,
                         const externT* from, const externT* from_end,
                         const externT*& from_next,
                         internT* to,
                         internT* to_end, internT*& to_next) const;
    virtual result do_unshift(stateT& state,
                              externT* to,
                              externT* to_end, externT*& to_next) const;
    virtual int do_encoding() const noexcept;
    virtual bool do_always_noconv() const noexcept;
    virtual int do_length(stateT&, const externT* from,
                          const externT* end, size_t max) const;
    virtual int do_max_length() const noexcept;
};

```

#### Class std::codecvt_byname

```
template <class internT, class externT, class stateT>
class codecvt_byname : public codecvt<internT, externT, stateT>
{
public:
    explicit codecvt_byname(const char*, size_t refs = 0);
    explicit codecvt_byname(const string&, size_t refs = 0);
protected:
    ~codecvt_byname();
};

```

#### Class std::num_get

```
template <class CharT, class InputIter = istreambuf_iterator<CharT>>
class num_get : public locale::facet
{
public:
    typedef CharT           char_type;
    typedef InputIter   iter_type;
    explicit num_get(size_t refs = 0);
    iter_type get(iter_type in, iter_type end, ios_base&,
                  ios_base::iostate& err, bool& v) const;
    iter_type get(iter_type in, iter_type end, ios_base&,
                  ios_base::iostate& err, long& v) const;
    iter_type get(iter_type in, iter_type end, ios_base&,
                  ios_base::iostate& err, long long& v) const;
    iter_type get(iter_type in, iter_type end, ios_base&,
                  ios_base::iostate& err, unsigned short& v) const;
    iter_type get(iter_type in, iter_type end, ios_base&,
                  ios_base::iostate& err, unsigned int& v) const;
    iter_type get(iter_type in, iter_type end, ios_base&,
                  ios_base::iostate& err, unsigned long& v) const;
    iter_type get(iter_type in, iter_type end, ios_base&,
                  ios_base::iostate& err, unsigned long long& v) const;
    iter_type get(iter_type in, iter_type end, ios_base&,
                  ios_base::iostate& err, float& v) const;
    iter_type get(iter_type in, iter_type end, ios_base&,
                  ios_base::iostate& err, double& v) const;
    iter_type get(iter_type in, iter_type end, ios_base&,
                  ios_base::iostate& err, long double& v) const;
    iter_type get(iter_type in, iter_type end, ios_base&,
                  ios_base::iostate& err, void*& v) const;
 
    static locale::id id;
 
protected:
    ~num_get();
 
    virtual iter_type do_get(iter_type, iter_type, ios_base&,
                             ios_base::iostate& err, bool& v) const;
    virtual iter_type do_get(iter_type, iter_type, ios_base&,
                             ios_base::iostate& err, long& v) const;
    virtual iter_type do_get(iter_type, iter_type, ios_base&,
                             ios_base::iostate& err, long long& v) const;
    virtual iter_type do_get(iter_type, iter_type, ios_base&,
                             ios_base::iostate& err, unsigned short& v) const;
    virtual iter_type do_get(iter_type, iter_type, ios_base&,
                             ios_base::iostate& err, unsigned int& v) const;
    virtual iter_type do_get(iter_type, iter_type, ios_base&,
                             ios_base::iostate& err, unsigned long& v) const;
    virtual iter_type do_get(iter_type, iter_type, ios_base&,
                             ios_base::iostate& err, unsigned long long& v) const;
    virtual iter_type do_get(iter_type, iter_type, ios_base&,
                             ios_base::iostate& err, float& v) const;
    virtual iter_type do_get(iter_type, iter_type, ios_base&,
                             ios_base::iostate& err, double& v) const;
    virtual iter_type do_get(iter_type, iter_type, ios_base&,
                             ios_base::iostate& err, long double& v) const;
    virtual iter_type do_get(iter_type, iter_type, ios_base&,
                             ios_base::iostate& err, void*& v) const;
};

```

#### Class std::num_put

```
template <class CharT, class OutputIter = ostreambuf_iterator<CharT>>
class num_put : public locale::facet
{
public:
    typedef CharT char_type;
    typedef OutputIter iter_type;
 
    explicit num_put(size_t refs = 0);
 
    iter_type put(iter_type s, ios_base& f, char_type fill,
                  bool v) const;
    iter_type put(iter_type s, ios_base& f, char_type fill,
                  long v) const;
    iter_type put(iter_type s, ios_base& f, char_type fill,
                  long long v) const;
    iter_type put(iter_type s, ios_base& f, char_type fill,
                  unsigned long v) const;
    iter_type put(iter_type s, ios_base& f, char_type fill,
                  unsigned long long v) const;
    iter_type put(iter_type s, ios_base& f, char_type fill,
                  double v) const;
    iter_type put(iter_type s, ios_base& f, char_type fill,
                  long double v) const;
    iter_type put(iter_type s, ios_base& f, char_type fill,
                  const void* v) const;
 
    static locale::id id;
 
protected:
    ~num_put();
 
    virtual iter_type do_put(iter_type, ios_base&, char_type fill,
                             bool v) const;
    virtual iter_type do_put(iter_type, ios_base&, char_type fill,
                             long v) const;
    virtual iter_type do_put(iter_type, ios_base&, char_type fill,
                             long long v) const;
    virtual iter_type do_put(iter_type, ios_base&, char_type fill,
                             unsigned long) const;
    virtual iter_type do_put(iter_type, ios_base&, char_type fill,
                             unsigned long long) const;
    virtual iter_type do_put(iter_type, ios_base&, char_type fill,
                             double v) const;
    virtual iter_type do_put(iter_type, ios_base&, char_type fill,
                             long double v) const;
    virtual iter_type do_put(iter_type, ios_base&, char_type fill,
                             const void* v) const;
};

```

#### Class std::numpunct

```
template <class CharT>
class numpunct : public locale::facet
{
public:
    typedef CharT char_type;
    typedef basic_string<CharT> string_type;
 
    explicit numpunct(size_t refs = 0);
 
    char_type   decimal_point() const;
    char_type   thousands_sep() const;
    string      grouping()      const;
    string_type truename()      const;
    string_type falsename()     const;
 
    static locale::id id;
 
protected:
    ~numpunct(); // virtual
 
    virtual char_type   do_decimal_point() const;
    virtual char_type   do_thousands_sep() const;
    virtual string      do_grouping()      const;
    virtual string_type do_truename()      const; // for bool
    virtual string_type do_falsename()     const; // for bool
};

```

#### Class std::numpunct_byname

```
template <class CharT>
class numpunct_byname : public numpunct<CharT>
{
public:
    typedef CharT char_type;
    typedef basic_string<CharT> string_type;
 
    explicit numpunct_byname(const char*, size_t refs = 0);
    explicit numpunct_byname(const string&, size_t refs = 0);
 
protected:
    ~numpunct_byname();
};

```

#### Class std::collate

```
template <class CharT>
class collate : public locale::facet
{
public:
    typedef CharT char_type;
    typedef basic_string<CharT> string_type;
 
    explicit collate(size_t refs = 0);
 
    int compare(const CharT* low1, const CharT* high1,
                const CharT* low2, const CharT* high2) const;
    string_type transform(const CharT* low, const CharT* high) const;
    long hash(const CharT* low, const CharT* high) const;
 
    static locale::id id;
 
protected:
    ~collate();
 
    virtual int do_compare(const CharT* low1, const CharT* high1,
                           const CharT* low2, const CharT* high2) const;
    virtual string_type do_transform(const CharT* low,
                                     const CharT* high) const;
    virtual long do_hash (const CharT* low, const CharT* high) const;
};

```

#### Class std::collate_byname

```
template <class CharT>
class collate_byname : public collate<CharT>
{
public:
    typedef basic_string<CharT> string_type;
 
    explicit collate_byname(const char*, size_t refs = 0);
    explicit collate_byname(const string&, size_t refs = 0);
 
protected:
    ~collate_byname();
};

```

#### Class std::time_base

```
class time_base
{
public:
    enum dateorder { no_order, dmy, mdy, ymd, ydm };
};

```

#### Class std::time_get

```
template <class CharT, class InputIter = istreambuf_iterator<CharT>>
class time_get : public locale::facet, public time_base
{
public:
    typedef CharT char_type;
    typedef InputIter iter_type;
 
    explicit time_get(size_t refs = 0);
 
    dateorder date_order() const;
    iter_type get_time(iter_type s, iter_type end, ios_base& f,
                       ios_base::iostate& err, tm* t) const;
    iter_type get_date(iter_type s, iter_type end, ios_base& f,
                       ios_base::iostate& err, tm* t) const;
    iter_type get_weekday(iter_type s, iter_type end, ios_base& f,
                          ios_base::iostate& err, tm* t) const;
    iter_type get_monthname(iter_type s, iter_type end, ios_base& f,
                            ios_base::iostate& err, tm* t) const;
    iter_type get_year(iter_type s, iter_type end, ios_base& f,
                       ios_base::iostate& err, tm* t) const;
    iter_type get(iter_type s, iter_type end, ios_base& f,
                  ios_base::iostate& err, tm* t, char format,
                  char modifier = 0) const;
    iter_type get(iter_type s, iter_type end, ios_base& f,
                  ios_base::iostate& err, tm* t,
                  const char_type* fmt, const char_type* fmtend) const;
 
    static locale::id id;
 
protected:
    ~time_get();
 
    virtual dateorder do_date_order() const;
    virtual iter_type do_get_time(iter_type s, iter_type end, ios_base&,
                                  ios_base::iostate& err, tm* t) const;
    virtual iter_type do_get_date(iter_type s, iter_type end, ios_base&,
                                  ios_base::iostate& err, tm* t) const;
    virtual iter_type do_get_weekday(iter_type s, iter_type end, ios_base&,
                                     ios_base::iostate& err, tm* t) const;
    virtual iter_type do_get_monthname(iter_type s, iter_type end, ios_base&,
                                       ios_base::iostate& err, tm* t) const;
    virtual iter_type do_get_year(iter_type s, iter_type end, ios_base&,
                                  ios_base::iostate& err, tm* t) const;
    virtual iter_type do_get(iter_type s, iter_type end, ios_base& f,
                             ios_base::iostate& err, tm* t,
                             char format, char modifier) const;
};

```

#### Class std::time_get_byname

```
template <class CharT, class InputIter = istreambuf_iterator<CharT>>
class time_get_byname : public time_get<CharT, InputIter>
{
public:
    typedef time_base::dateorder dateorder;
    typedef InputIter iter_type;
 
    explicit time_get_byname(const char*, size_t refs = 0);
    explicit time_get_byname(const string&, size_t refs = 0);
 
protected:
    ~time_get_byname();
};

```

#### Class std::time_put

```
template <class CharT, class OutputIter = ostreambuf_iterator<CharT>>
class time_put : public locale::facet
{
public:
    typedef CharT char_type;
    typedef OutputIter iter_type;
 
    explicit time_put(size_t refs = 0);
 
    // the following is implemented in terms of other member functions.
    iter_type put(iter_type s, ios_base& f, char_type fill, const tm* tmb,
                  const CharT* pattern, const CharT* pat_end) const;
    iter_type put(iter_type s, ios_base& f, char_type fill,
                  const tm* tmb, char format, char modifier = 0) const;
 
    static locale::id id;
 
protected:
    ~time_put();
 
    virtual iter_type do_put(iter_type s, ios_base&, char_type, const tm* t,
                             char format, char modifier) const;
};

```

#### Class std::time_put_byname

```
template <class CharT, class OutputIter = ostreambuf_iterator<CharT>>
class time_put_byname : public time_put<CharT, OutputIter>
{
public:
    typedef CharT char_type;
    typedef OutputIter iter_type;
 
    explicit time_put_byname(const char*, size_t refs = 0);
    explicit time_put_byname(const string&, size_t refs = 0);
 
protected:
    ~time_put_byname();
};

```

#### Class std::money_get

```
template <class CharT, class InputIter = istreambuf_iterator<CharT>>
class money_get : public locale::facet
{
public:
    typedef CharT char_type;
    typedef InputIter iter_type;
    typedef basic_string<CharT> string_type;
 
    explicit money_get(size_t refs = 0);
 
    iter_type get(iter_type s, iter_type end, bool intl, ios_base& f,
                  ios_base::iostate& err, long double& units) const;
    iter_type get(iter_type s, iter_type end, bool intl, ios_base& f,
                  ios_base::iostate& err, string_type& digits) const;
 
    static locale::id id;
 
protected:
    ~money_get();
 
    virtual iter_type do_get(iter_type, iter_type, bool, ios_base&,
                             ios_base::iostate& err,
                             long double& units) const;
    virtual iter_type do_get(iter_type, iter_type, bool, ios_base&,
                             ios_base::iostate& err,
                             string_type& digits) const;
};

```

#### Class std::money_put

```
template <class CharT, class OutputIter = ostreambuf_iterator<CharT>>
class money_put : public locale::facet
{
public:
    typedef CharT char_type;
    typedef OutputIter iter_type;
    typedef basic_string<CharT> string_type;
 
    explicit money_put(size_t refs = 0);
 
    iter_type put(iter_type s, bool intl, ios_base& f,
                  char_type fill, long double units) const;
    iter_type put(iter_type s, bool intl, ios_base& f,
                  char_type fill, const string_type& digits) const;
 
    static locale::id id;
 
protected:
    ~money_put();
 
    virtual iter_type do_put(iter_type, bool, ios_base&, char_type fill,
                             long double units) const;
    virtual iter_type do_put(iter_type, bool, ios_base&, char_type fill,
                             const string_type& digits) const;
};

```

#### Class std::money_base

```
class money_base
{
public:
    enum part { none, space, symbol, sign, value };
    struct pattern { char field[4]; };
};

```

#### Class std::moneypunct

```
template <class CharT, bool International = false>
class moneypunct : public locale::facet, public money_base
{
public:
    typedef CharT char_type;
    typedef basic_string<CharT> string_type;
 
    explicit moneypunct(size_t refs = 0);
 
    CharT       decimal_point() const;
    CharT       thousands_sep() const;
    string      grouping()      const;
    string_type curr_symbol()   const;
    string_type positive_sign() const;
    string_type negative_sign() const;
    int         frac_digits()   const;
    pattern     pos_format()    const;
    pattern     neg_format()    const;
 
    static locale::id id;
    static const bool intl = International;
 
protected:
    ~moneypunct();
 
    virtual CharT       do_decimal_point() const;
    virtual CharT       do_thousands_sep() const;
    virtual string      do_grouping()      const;
    virtual string_type do_curr_symbol()   const;
    virtual string_type do_positive_sign() const;
    virtual string_type do_negative_sign() const;
    virtual int         do_frac_digits()   const;
    virtual pattern     do_pos_format()    const;
    virtual pattern     do_neg_format()    const;
};

```

#### Class std::moneypunct_byname

```
template <class CharT, bool Intl = false>
class moneypunct_byname : public moneypunct<CharT, Intl>
{
public:
    typedef money_base::pattern pattern;
    typedef basic_string<CharT> string_type;
 
    explicit moneypunct_byname(const char*, size_t refs = 0);
    explicit moneypunct_byname(const string&, size_t refs = 0);
 
protected:
    ~moneypunct_byname();
};

```

#### Class std::messages_base

```
class messages_base
{
public:
    typedef /* unspecified signed integer type */ catalog;
};

```

#### Class std::messages

```
template <class CharT>
class messages : public locale::facet, public messages_base {
public:
    typedef CharT char_type;
    typedef basic_string<CharT> string_type;
 
    explicit messages(size_t refs = 0);
 
    catalog open(const basic_string<char>& fn, const locale&) const;
    string_type get(catalog c, int set, int msgid,
                    const string_type& dfault) const;
    void close(catalog c) const;
 
    static locale::id id;
 
protected:
    ~messages();
 
    virtual catalog do_open(const basic_string<char>&, const locale&) const;
    virtual string_type do_get(catalog, int set, int msgid,
                               const string_type& dfault) const;
    virtual void do_close(catalog) const;
};

```

#### Class std::messages_byname

```
template <class CharT>
class messages_byname : public messages<CharT>
{
public:
    typedef messages_base::catalog catalog;
    typedef basic_string<CharT> string_type;
 
    explicit messages_byname(const char*, size_t refs = 0);
    explicit messages_byname(const string&, size_t refs = 0);
 
protected:
    ~messages_byname();
};

```

#### Class std::wstring_convert

```
template<class Codecvt, class Elem = wchar_t,
    class Wide_alloc = std::allocator<Elem>,
    class Byte_alloc = std::allocator<char>>
class wstring_convert
{
public:
    typedef std::basic_string<char, char_traits<char>, Byte_alloc> byte_string;
    typedef std::basic_string<Elem, char_traits<Elem>, Wide_alloc> wide_string;
    typedef typename Codecvt::state_type state_type;
    typedef typename wide_string::traits_type::int_type int_type;
 
    explicit wstring_convert(Codecvt* pcvt = new Codecvt);
    wstring_convert(Codecvt* pcvt, state_type state);
    explicit wstring_convert(const byte_string& byte_err,
                             const wide_string& wide_err = wide_string());
    ~wstring_convert();
 
    wstring_convert(const wstring_convert&) = delete;
    wstring_convert& operator=(const wstring_convert&) = delete;
 
    wide_string from_bytes(char byte);
    wide_string from_bytes(const char* ptr);
    wide_string from_bytes(const byte_string& str);
    wide_string from_bytes(const char* first, const char* last);
    byte_string to_bytes(Elem wchar);
    byte_string to_bytes(const Elem* wptr);
    byte_string to_bytes(const wide_string& wstr);
    byte_string to_bytes(const Elem* first, const Elem* last);
    size_t converted() const noexcept;
    state_type state() const;
 
private:
    byte_string byte_err_string; // exposition only
    wide_string wide_err_string; // exposition only
    Codecvt* cvtptr;             // exposition only
    state_type cvtstate;         // exposition only
    size_t cvtcount;             // exposition only
};

```

#### Class std::wbuffer_convert

```
template<class Codecvt,
    class Elem = wchar_t,
    class Tr = std::char_traits<Elem>>
class wbuffer_convert : public std::basic_streambuf<Elem, Tr>
{
public:
    typedef typename Codecvt::state_type state_type;
 
    explicit wbuffer_convert(std::streambuf* bytebuf = 0,
                             Codecvt* pcvt = new Codecvt,
                             state_type state = state_type());
    ~wbuffer_convert();
 
    wbuffer_convert(const wbuffer_convert&) = delete;
    wbuffer_convert& operator=(const wbuffer_convert&) = delete;
 
    std::streambuf* rdbuf() const;
    std::streambuf* rdbuf(std::streambuf* bytebuf);
    state_type state() const;
private:
    std::streambuf* bufptr; // exposition only
    Codecvt* cvtptr;        // exposition only
    state_type cvtstate;    // exposition only
};

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 71 | C++98 | the parameter end of time_get::do_get_monthname was missing in the synopsis | added |
| LWG 75 | C++98 | the type of the parameter state of members length and `do_length` of codecvt and codecvt_byname was const stateT& in the synopsis | corrected to stateT& |
| LWG 124 | C++98 | the return types of members `do_scan_is` and `do_scan_not` of codecvt_byname were const char\* in the synopsis | corrected to const charT\* |
| LWG 228 | C++98 | all virtual member functions of `XXX_byname` facets were listed in the synopses | only lists the destructor (removed all other virtual member functions) |
| LWG 268 | C++98 | the semicolons following the declarations of the default constructor and copy constructor of std::locale were missing in the synopsis | added |
| LWG 1298 | C++98 | there was an explicit specialization ctype_byname<char> in the synopsis | removed |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/locale&oldid=179688>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 January 2025, at 11:17.