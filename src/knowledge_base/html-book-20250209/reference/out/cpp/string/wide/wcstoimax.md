# std::wcstoimax, std::wcstoumax

From cppreference.com
< cpp‎ | string‎ | wide
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

Text processing library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Localization library | | | | |
| Regular expressions library (C++11) | | | | |
| Formatting library (C++20) | | | | |
| Null-terminated sequence utilities | | | | |
| Byte strings | | | | |
| Multibyte strings | | | | |
| Wide strings | | | | |
| Primitive numeric conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | to_chars(C++17) | | | | | | to_chars_result(C++17) | | | | | | from_chars(C++17) | | | | | | from_chars_result(C++17) | | | | | | chars_format(C++17) | | | | | |
| Text encoding identifications | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | text_encoding(C++26) | | | | | |

Null-terminated wide strings

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Character classification | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iswalnum | | | | | | iswalpha | | | | | | iswlower | | | | | | iswupper | | | | | | iswdigit | | | | | | iswxdigit | | | | | | wctype | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iswblank(C++11) | | | | | | iswctype | | | | | | iswcntrl | | | | | | iswgraph | | | | | | iswspace | | | | | | iswprint | | | | | | iswpunct | | | | | |
| Character manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | towlower | | | | | | towupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | towctrans | | | | | | wctrans | | | | | |
| Conversions to numeric formats | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcstolwcstoll(C++11) | | | | | | wcstofwcstodwcstold(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcstoulwcstoull(C++11) | | | | | | ****wcstoimaxwcstouimax****(C++11)(C++11) | | | | | |  | | | | | |
| String manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcslen | | | | | | wcscmp | | | | | | wcscoll | | | | | | wcsncmp | | | | | | wcschr | | | | | | wcsrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcspbrk | | | | | | wcsspn | | | | | | wcscspn | | | | | | wcsstr | | | | | | wcstok | | | | | |  | | | | | |
| String examination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcscpy | | | | | | wcsncpy | | | | | | wcsxfrm | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcscat | | | | | | wcsncat | | | | | |  | | | | | |
| Array manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | wmemcpy | | | | | | wmemmove | | | | | | wmemcmp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wmemchr | | | | | | wmemset | | | | | |  | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Types | | | | | | wctrans_t | | | | | | wctype_t | | | | | | wint_t | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Macros | | | | | | WCHAR_MIN WCHAR_MAX WEOF | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cinttypes>` |  |  |
| std::intmax_t wcstoimax( const wchar_t\* nptr, wchar_t\*\* endptr, int base ); |  | (since C++11) |
| std::uintmax_t wcstoumax( const wchar_t\* nptr, wchar_t\*\* endptr, int base ); |  | (since C++11) |
|  |  |  |

Interprets an unsigned integer value in a wide string pointed to by nptr.

Discards any whitespace characters (as identified by calling std::iswspace) until the first non-whitespace character is found, then takes as many characters as possible to form a valid **base-n** (where n=`base`) unsigned integer number representation and converts them to an integer value. The valid unsigned integer value consists of the following parts:

- (optional) plus or minus sign
- (optional) prefix (`0`) indicating octal base (applies only when the base is 8 or ​0​)
- (optional) prefix (`0x` or `0X`) indicating hexadecimal base (applies only when the base is 16 or ​0​)
- a sequence of digits

The set of valid values for base is `{0, 2, 3, ..., 36}`. The set of valid digits for base-`2` integers is `{0, 1}`, for base-`3` integers is `{0, 1, 2}`, and so on. For bases larger than `10`, valid digits include alphabetic characters, starting from `Aa` for base-`11` integer, to `Zz` for base-`36` integer. The case of the characters is ignored.

Additional numeric formats may be accepted by the currently installed C locale.

If the value of `base` is ​0​, the numeric base is auto-detected: if the prefix is `0`, the base is octal, if the prefix is `0x` or `0X`, the base is hexadecimal, otherwise the base is decimal.

If the minus sign was part of the input sequence, the numeric value calculated from the sequence of digits is negated as if by unary minus in the result type, which applies unsigned integer wraparound rules.

The functions sets the pointer pointed to by endptr to point to the wide character past the last character interpreted. If endptr is a null pointer, it is ignored.

### Parameters

|  |  |  |
| --- | --- | --- |
| nptr | - | pointer to the null-terminated wide string to be interpreted |
| endptr | - | pointer to a pointer to a wide character |
| base | - | **base** of the interpreted integer value |

### Return value

Integer value corresponding to the contents of str on success. If the converted value falls out of range of corresponding return type, range error occurs and INTMAX_MAX, INTMAX_MIN, UINTMAX_MAX, or ​0​ is returned, as appropriate. If no conversion can be performed, ​0​ is returned.

### Example

Run this code

```
#include <cinttypes>
#include <iostream>
#include <string>
 
int main()
{
    std::wstring str = L"helloworld";
    std::intmax_t val = std::wcstoimax(str.c_str(), nullptr, 36);
    std::wcout << str << " in base 36 is " << val << " in base 10\n";
 
    wchar_t* nptr;
    val = std::wcstoimax(str.c_str(), &nptr, 30);
    if (nptr != &str[0] + str.size())
        std::wcout << str << " in base 30 is invalid."
                   << " The first invalid digit is " << *nptr << '\n';
}

```

Output:

```
helloworld in base 36 is 1767707668033969 in base 10
helloworld in base 30 is invalid. The first invalid digit is w

```

### See also

|  |  |
| --- | --- |
| strtoimaxstrtoumax(C++11)(C++11) | converts a byte string to std::intmax_t or std::uintmax_t   (function) |
| wcstolwcstoll | converts a wide string to an integer value   (function) |
| wcstoulwcstoull | converts a wide string to an unsigned integer value   (function) |
| C documentation for wcstoimax, wcstoumax | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/wide/wcstoimax&oldid=153120>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 June 2023, at 10:30.