# std::printf, std::fprintf, std::sprintf, std::snprintf

From cppreference.com
< cpp‎ | io‎ | c
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

Input/output library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| I/O manipulators | | | | |
| Print functions (C++23) | | | | |
| C-style I/O | | | | |
| Buffers | | | | |
| basic_streambuf | | | | |
| basic_filebuf | | | | |
| basic_stringbuf | | | | |
| basic_spanbuf(C++23) | | | | |
| strstreambuf(C++98/26\*) | | | | |
| basic_syncbuf(C++20) | | | | |
| Streams | | | | |
| Abstractions | | | | |
| ios_base | | | | |
| basic_ios | | | | |
| basic_istream | | | | |
| basic_ostream | | | | |
| basic_iostream | | | | |
| File I/O | | | | |
| basic_ifstream | | | | |
| basic_ofstream | | | | |
| basic_fstream | | | | |
| String I/O | | | | |
| basic_istringstream | | | | |
| basic_ostringstream | | | | |
| basic_stringstream | | | | |
| Array I/O | | | | |
| basic_ispanstream(C++23) | | | | |
| basic_ospanstream(C++23) | | | | |
| basic_spanstream(C++23) | | | | |
| istrstream(C++98/26\*) | | | | |
| ostrstream(C++98/26\*) | | | | |
| strstream(C++98/26\*) | | | | |
| Synchronized Output | | | | |
| basic_osyncstream(C++20) | | | | |
| Types | | | | |
| streamoff | | | | |
| streamsize | | | | |
| fpos | | | | |
| Error category interface | | | | |
| iostream_category(C++11) | | | | |
| io_errc(C++11) | | | | |

C-style I/O

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Types and objects | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | FILE | | | | | | fpos_t | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stdinstdoutstderr | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | File access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fopen | | | | | | freopen | | | | | | fclose | | | | | | fflush | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwide | | | | | | setbuf | | | | | | setvbuf | | | | | |  | | | | | | | Direct input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fread | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwrite | | | | | | | Unformatted input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetcgetc | | | | | | fgets | | | | | | fputcputc | | | | | | fputs | | | | | | getchar | | | | | | gets(until C++14) | | | | | | putchar | | | | | | puts | | | | | | ungetc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetwcgetwc | | | | | | fgetws | | | | | | fputwcputwc | | | | | | fputws | | | | | | getwchar | | | | | | putwchar | | | | | | ungetwc | | | | | |  | | | | | |  | | | | | | | Formatted input | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scanffscanfsscanf | | | | | | vscanfvfscanfvsscanf(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wscanffwscanfswscanf | | | | | | vwscanfvfwscanfvswscanf(C++11)(C++11)(C++11) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Formatted output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****printffprintfsprintfsnprintf****(C++11) | | | | | | vprintfvfprintfvsprintfvsnprintf(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wprintffwprintfswprintf | | | | | | vwprintfvfwprintfvswprintf | | | | | | | File positioning | | | | | | ftell | | | | | | fgetpos | | | | | | fseek | | | | | | fsetpos | | | | | | rewind | | | | | | Error handling | | | | | | clearerr | | | | | | feof | | | | | | ferror | | | | | | perror | | | | | | Operations on files | | | | | | remove | | | | | | rename | | | | | | tmpfile | | | | | | tmpnam | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstdio>` |  |  |
| int printf( const char\* format, ... ); | (1) |  |
| int fprintf( std::FILE\* stream, const char\* format, ... ); | (2) |  |
| int sprintf( char\* buffer, const char\* format, ... ); | (3) |  |
| int snprintf( char\* buffer, std::size_t buf_size, const char\* format, ... ); | (4) | (since C++11) |
|  |  |  |

Loads the data from the given locations, converts them to character string equivalents and writes the results to a variety of sinks.

1) Writes the results to stdout.2) Writes the results to a file stream stream.3) Writes the results to a character string buffer.4) Writes the results to a character string buffer. At most buf_size - 1 characters are written. The resulting character string will be terminated with a null character, unless buf_size is zero. If buf_size is zero, nothing is written and buffer may be a null pointer, however the return value (number of bytes that would be written not including the null terminator) is still calculated and returned.

If a call to `sprintf` or `snprintf` causes copying to take place between objects that overlap, the behavior is undefined (e.g. sprintf(buf, "%s text", buf);).

### Parameters

|  |  |  |
| --- | --- | --- |
| stream | - | output file stream to write to |
| buffer | - | pointer to a character string to write to |
| buf_size | - | up to buf_size - 1 characters may be written, plus the null terminator |
| format | - | pointer to a null-terminated multibyte string specifying how to interpret the data |
| ... | - | arguments specifying data to print. If any argument after default argument promotions is not the type expected by the corresponding conversion specification (the expected type is the promoted type or a compatible type of the promoted type), or if there are fewer arguments than required by format, the behavior is undefined. If there are more arguments than required by format, the extraneous arguments are evaluated and ignored |

The ****format**** string consists of ordinary byte characters (except `%`), which are copied unchanged into the output stream, and conversion specifications. Each conversion specification has the following format:

:   - introductory `%` character.

:   - (optional) one or more flags that modify the behavior of the conversion:

    :   - `-`: the result of the conversion is left-justified within the field (by default it is right-justified).
        - `+`: the sign of signed conversions is always prepended to the result of the conversion (by default the result is preceded by minus only when it is negative).
        - **space**: if the result of a signed conversion does not start with a sign character, or is empty, space is prepended to the result. It is ignored if `+` flag is present.
        - `#`: **alternative form** of the conversion is performed. See the table below for exact effects otherwise the behavior is undefined.
        - `0`: for integer and floating-point number conversions, leading zeros are used to pad the field instead of **space** characters. For integer numbers it is ignored if the precision is explicitly specified. For other conversions using this flag results in undefined behavior. It is ignored if `-` flag is present.

:   - (optional) integer value or `*` that specifies minimum field width. The result is padded with **space** characters (by default), if required, on the left when right-justified, or on the right if left-justified. In the case when `*` is used, the width is specified by an additional argument of type int, which appears before the argument to be converted and the argument supplying precision if one is supplied. If the value of the argument is negative, it results with the `-` flag specified and positive field width (Note: This is the minimum width: The value is never truncated.).

:   - (optional) `.` followed by integer number or `*`, or neither that specifies **precision** of the conversion. In the case when `*` is used, the **precision** is specified by an additional argument of type int, which appears before the argument to be converted, but after the argument supplying minimum field width if one is supplied. If the value of this argument is negative, it is ignored. If neither a number nor `*` is used, the precision is taken as zero. See the table below for exact effects of **precision**.

:   - (optional) **length modifier** that specifies the size of the argument (in combination with the conversion format specifier, it specifies the type of the corresponding argument).

:   - conversion format specifier.

The following format specifiers are available:

| Conversion Specifier | Explanation | Expected Argument Type | | | | | | | | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ****Length Modifier********→**** | | `hh` (C++11) | `h` | (none) | `l` | `ll` (C++11) | `j` (C++11) | `z` (C++11) | `t` (C++11) | `L` |
| `%` | Writes literal `%`. The full conversion specification must be `%%`. | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A |
| `c` | Writes a ****single character****.  The argument is first converted to unsigned char. If the ****l**** modifier is used, the argument is first converted to a character string as if by ****%ls**** with a wchar_t[2] argument. | N/A | N/A | int | wint_t | N/A | N/A | N/A | N/A | N/A |
| `s` | Writes a ****character string****  The argument must be a pointer to the initial element of an array of characters. **Precision** specifies the maximum number of bytes to be written. If **Precision** is not specified, writes every byte up to and not including the first null terminator. If the ****l**** specifier is used, the argument must be a pointer to the initial element of an array of wchar_t, which is converted to char array as if by a call to wcrtomb with zero-initialized conversion state. | N/A | N/A | char\* | wchar_t\* | N/A | N/A | N/A | N/A | N/A |
| `d` `i` | Converts a ****signed integer**** into decimal representation **[-]dddd**.  **Precision** specifies the minimum number of digits to appear. The default precision is 1.  If both the converted value and the precision are ​0​ the conversion results in no characters. | signed char | short | int | long | long long | intmax_t | signed size_t | ptrdiff_t | N/A |
| `o` | Converts an ****unsigned integer**** into octal representation **oooo**.  **Precision** specifies the minimum number of digits to appear. The default precision is 1. If both the converted value and the precision are ​0​ the conversion results in no characters. In the **alternative implementation** precision is increased if necessary, to write one leading zero. In that case if both the converted value and the precision are ​0​, single ​0​ is written. | unsigned char | unsigned short | unsigned int | unsigned long | unsigned long long | uintmax_t | size_t | unsigned version of ptrdiff_t | N/A |
| `x` `X` | Converts an ****unsigned integer**** into hexadecimal representation **hhhh**.  For the `x` conversion letters `abcdef` are used.  For the `X` conversion letters `ABCDEF` are used.  **Precision** specifies the minimum number of digits to appear. The default precision is 1. If both the converted value and the precision are ​0​ the conversion results in no characters. In the **alternative implementation** `0x` or `0X` is prefixed to results if the converted value is nonzero. | N/A |
| `u` | Converts an ****unsigned integer**** into decimal representation **dddd**.  **Precision** specifies the minimum number of digits to appear. The default precision is 1. If both the converted value and the precision are ​0​ the conversion results in no characters. | N/A |
| `f` `F` | Converts ****floating-point number**** to the decimal notation in the style **[-]ddd.ddd**.  **Precision** specifies the exact number of digits to appear after the decimal point character. The default precision is 6. In the **alternative implementation** decimal point character is written even if no digits follow it. For infinity and not-a-number conversion style see notes. | N/A | N/A | double | double(C++11) | N/A | N/A | N/A | N/A | long double |
| `e` `E` | Converts ****floating-point number**** to the decimal exponent notation.  For the `e` conversion style **[-]d.ddd** ﻿`e`**±dd** is used.  For the `E` conversion style **[-]d.ddd** ﻿`E`**±dd** is used.  The exponent contains at least two digits, more digits are used only if necessary. If the value is ​0​, the exponent is also ​0​. **Precision** specifies the exact number of digits to appear after the decimal point character. The default precision is 6. In the **alternative implementation** decimal point character is written even if no digits follow it. For infinity and not-a-number conversion style see notes. | N/A | N/A | N/A | N/A | N/A | N/A |
| `a` `A` (C++11) | Converts ****floating-point number**** to the hexadecimal exponent notation.  For the `a` conversion style **[-]** ﻿`0x`**h.hhh** ﻿`p`**±d** is used.  For the `A` conversion style **[-]** ﻿`0X`**h.hhh** ﻿`P`**±d** is used.  The first hexadecimal digit is not `0` if the argument is a normalized floating-point value. If the value is ​0​, the exponent is also ​0​. **Precision** specifies the exact number of digits to appear after the hexadecimal point character. The default precision is sufficient for exact representation of the value. In the **alternative implementation** decimal point character is written even if no digits follow it. For infinity and not-a-number conversion style see notes. | N/A | N/A | N/A | N/A | N/A | N/A |
| `g` `G` | Converts ****floating-point number**** to decimal or decimal exponent notation depending on the value and the **precision**.  For the `g` conversion style conversion with style `e` or `f` will be performed.  For the `G` conversion style conversion with style `E` or `F` will be performed.  Let `P` equal the precision if nonzero, 6 if the precision is not specified, or 1 if the precision is ​0​. Then, if a conversion with style `E` would have an exponent of `X`:   - if **P > X ≥ −4**, the conversion is with style `f` or `F` and precision **P − 1 − X**. - otherwise, the conversion is with style `e` or `E` and precision **P − 1**.   Unless **alternative representation** is requested the trailing zeros are removed, also the decimal point character is removed if no fractional part is left. For infinity and not-a-number conversion style see notes. | N/A | N/A | N/A | N/A | N/A | N/A |
| `n` | Returns the ****number of characters written**** so far by this call to the function.  The result is **written** to the value pointed to by the argument. The specification may not contain any **flag**, **field width**, or **precision**. | signed char\* | short\* | int\* | long\* | long long\* | intmax_t\* | signed size_t\* | ptrdiff_t\* | N/A |
| `p` | Writes an implementation defined character sequence defining a ****pointer****. | N/A | N/A | void\* | N/A | N/A | N/A | N/A | N/A | N/A |

The floating-point conversion functions convert infinity to `inf` or `infinity`. Which one is used is implementation defined.

Not-a-number is converted to `nan` or `nan(char_sequence)`. Which one is used is implementation defined.

The conversions `F`, `E`, `G`, `A` output `INF`, `INFINITY`, `NAN` instead.

The conversion specifier used to print char, unsigned char, signed char, short, and unsigned short expects promoted types of default argument promotions, but before printing its value will be converted to char, unsigned char, signed char, short, and unsigned short. It is safe to pass values of these types because of the promotion that takes place when a variadic function is called.

The correct conversion specifications for the fixed-width character types (int8_t, etc) are defined in the header <cinttypes> (although PRIdMAX, PRIuMAX, etc is synonymous with `%jd`, `%ju`, etc).

The memory-writing conversion specifier `%n` is a common target of security exploits where format strings depend on user input and is not supported by the bounds-checked `printf_s` family of functions.

There is a sequence point after the action of each conversion specifier; this permits storing multiple `%n` results in the same variable or, as an edge case, printing a string modified by an earlier `%n` within the same call.

If a conversion specification is invalid, the behavior is undefined.

### Return value

1,2) Number of characters written if successful or a negative value if an error occurred.3) Number of characters written if successful (not including the terminating null character) or a negative value if an error occurred.4) Number of characters that would have been written for a sufficiently large buffer if successful (not including the terminating null character), or a negative value if an error occurred. Thus, the (null-terminated) output has been completely written if and only if the returned value is nonnegative and less than buf_size.

### Notes

POSIX specifies that errno is set on error. It also specifies additional conversion specifications, most notably support for argument reordering (n$ immediately after % indicates `n`th argument).

Calling `std::snprintf` with zero buf_size and null pointer for buffer is useful (when the overhead of double-call is acceptable) to determine the necessary buffer size to contain the output:

```
auto fmt = "sqrt(2) = %f";
int sz = std::snprintf(nullptr, 0, fmt, std::sqrt(2));
std::vector<char> buf(sz + 1); // note +1 for null terminator
std::sprintf(buf.data(), fmt, std::sqrt(2)); // certain to fit

```

### Example

Run this code

```
#include <cinttypes>
#include <cstdint>
#include <cstdio>
#include <limits>
 
int main()
{
    const char* s = "Hello";
    std::printf("Strings:\n"); // same as std::puts("Strings:");
    std::printf("\t[%10s]\n", s);
    std::printf("\t[%-10s]\n", s);
    std::printf("\t[%*s]\n", 10, s);
    std::printf("\t[%-10.*s]\n", 4, s);
    std::printf("\t[%-*.*s]\n", 10, 4, s);
 
    std::printf("Characters:\t%c %%\n", 'A');
 
    std::printf("Integers:\n");
    std::printf("\tDecimal:    \t%i %d %.6i %i %.0i %+i %i\n",
                                  1, 2,   3, 0,   0,  4,-4);
    std::printf("\tHexadecimal:\t%x %x %X %#x\n",
                                  5,10,10,  6);
    std::printf("\tOctal:      \t%o %#o %#o\n",
                                 10, 10,  4);
 
    std::printf("Floating point:\n");
    std::printf("\tRounding:\t%f %.0f %.32f\n", 1.5, 1.5, 1.3);
    std::printf("\tPadding:\t%05.2f %.2f %5.2f\n", 1.5, 1.5, 1.5);
    std::printf("\tScientific:\t%E %e\n", 1.5, 1.5);
    std::printf("\tHexadecimal:\t%a %A\n", 1.5, 1.5);
    std::printf("\tSpecial values:\t0/0=%g 1/0=%g\n", 0.0/0.0, 1.0/0.0);
 
    std::printf("Variable width control:\n");
    std::printf("\tright-justified variable width: '%*c'\n", 5, 'x');
    int r = std::printf("\tleft-justified variable width : '%*c'\n", -5, 'x');
    std::printf("(the last printf printed %d characters)\n", r);
 
    std::printf("Fixed-width types:\n");
    std::uint32_t val = std::numeric_limits<std::uint32_t>::max();
    std::printf("\tLargest 32-bit value is %" PRIu32 " or %#" PRIx32 "\n",
                                                 val,            val);
}

```

Possible output:

```
Strings:
	[     Hello]
	[Hello     ]
	[     Hello]
	[Hell      ]
	[Hell      ]
Characters:	A %
Integers:
	Decimal:    	1 2 000003 0  +4 -4
	Hexadecimal:	5 a A 0x6
	Octal:      	12 012 04
Floating point:
	Rounding:	1.500000 2 1.30000000000000004440892098500626
	Padding:	01.50 1.50  1.50
	Scientific:	1.500000E+00 1.500000e+00
	Hexadecimal:	0x1.8p+0 0X1.8P+0
	Special values:	0/0=-nan 1/0=inf
Variable width control:
	right-justified variable width: '    x'
	left-justified variable width : 'x    '
(the last printf printed 41 characters)
Fixed-width types:
	Largest 32-bit value is 4294967295 or 0xffffffff

```

### See also

|  |  |
| --- | --- |
| wprintffwprintfswprintf | prints formatted wide character output to stdout, a file stream or a buffer   (function) |
| vprintfvfprintfvsprintfvsnprintf(C++11) | prints formatted output to stdout, a file stream or a buffer using variable argument list   (function) |
| fputs | writes a character string to a file stream   (function) |
| scanffscanfsscanf | reads formatted input from stdin, a file stream or a buffer   (function) |
| to_chars(C++17) | converts an integer or floating-point value to a character sequence   (function) |
| print(C++23) | prints to stdout or a file stream using formatted representation of the arguments   (function template) |
| println(C++23) | same as std::print except that each print is terminated by additional new line   (function template) |
| C documentation for printf, fprintf, sprintf, snprintf | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/c/fprintf&oldid=179644>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 January 2025, at 04:19.