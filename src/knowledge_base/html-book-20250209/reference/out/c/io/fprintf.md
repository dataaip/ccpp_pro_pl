# printf, fprintf, sprintf, snprintf, printf_s, fprintf_s, sprintf_s, snprintf_s

From cppreference.com
< c‎ | io
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 File input/output

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Types and objects | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stdinstdoutstderr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FILE | | | | | | fpos_t | | | | | |  | | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | File access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fopenfopen_s(C11) | | | | | | freopenfreopen_s(C11) | | | | | | fwide(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setbuf | | | | | | setvbuf | | | | | | fclose | | | | | | fflush | | | | | |  | | | | | | | Unformatted input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetc | | | | | | fgets | | | | | | fputc | | | | | | fputs | | | | | | getchar | | | | | | getsgets_s(until C11)(C11) | | | | | | putchar | | | | | | puts | | | | | | ungetc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetwcgetwc(C95)(C95) | | | | | | fgetws(C95) | | | | | | fputwcputwc(C95)(C95) | | | | | | fputws(C95) | | | | | | getwchar(C95) | | | | | | putwchar(C95) | | | | | | ungetwc(C95) | | | | | |  | | | | | | | Formatted input | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scanffscanfsscanfscanf_sfscanf_ssscanf_s(C11)(C11)(C11) | | | | | | wscanffwscanfswscanfwscanf_sfwscanf_sswscanf_s(C95)(C95)(C95)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vscanfvfscanfvsscanfvscanf_svfscanf_svsscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | vwscanfvfwscanfvswscanfvwscanf_svfwscanf_svswscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Direct input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fread | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwrite | | | | | | | Formatted output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****printffprintfsprintfsnprintfprintf_sfprintf_ssprintf_ssnprintf_s****(C99)(C11)(C11)(C11)(C11) | | | | | | wprintffwprintfswprintfwprintf_sfwprintf_sswprintf_ssnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vprintfvfprintfvsprintfvsnprintfvprintf_svfprintf_svsprintf_svsnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | vwprintfvfwprintfvswprintfvwprintf_svfwprintf_svswprintf_svsnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | | File positioning | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ftell | | | | | | fgetpos | | | | | | fseek | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fsetpos | | | | | | rewind | | | | | |  | | | | | | | Error handling | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clearerr | | | | | | feof | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ferror | | | | | | perror | | | | | | | Operations on files | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove | | | | | | tmpfiletmpfile_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rename | | | | | | tmpnamtmpnam_s(C11) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdio.h>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| int printf( const char\*          format, ... ); |  | (until C99) |
| int printf( const char\* restrict format, ... ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| int fprintf( FILE\*          stream, const char\*          format, ... ); |  | (until C99) |
| int fprintf( FILE\* restrict stream, const char\* restrict format, ... ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| int sprintf( char\*          buffer, const char\*          format, ... ); |  | (until C99) |
| int sprintf( char\* restrict buffer, const char\* restrict format, ... ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
| int snprintf( char\* restrict buffer, size_t bufsz,                const char\* restrict format, ... ); | (4) | (since C99) |
| int printf_s( const char\* restrict format, ... ); | (5) | (since C11) |
| int fprintf_s( FILE\* restrict stream, const char\* restrict format, ... ); | (6) | (since C11) |
| int sprintf_s( char\* restrict buffer, rsize_t bufsz,                 const char\* restrict format, ... ); | (7) | (since C11) |
| int snprintf_s( char\* restrict buffer, rsize_t bufsz,                  const char\* restrict format, ... ); | (8) | (since C11) |
|  |  |  |

Loads the data from the given locations, converts them to character string equivalents and writes the results to a variety of sinks/streams:

1) Writes the results to the output stream stdout.2) Writes the results to the output stream stream.3) Writes the results to a character string buffer. The behavior is undefined if the string to be written (plus the terminating null character) exceeds the size of the array pointed to by buffer.4) Writes the results to a character string buffer. At most bufsz - 1 characters are written. The resulting character string will be terminated with a null character, unless bufsz is zero. If bufsz is zero, nothing is written and buffer may be a null pointer, however the return value (number of bytes that would be written not including the null terminator) is still calculated and returned.5-8) Same as (1-4), except that the following errors are detected at runtime and call the currently installed constraint handler function:

:   - the conversion specifier `%n` is present in format
    - any of the arguments corresponding to `%s` is a null pointer
    - stream or format or buffer is a null pointer
    - bufsz is zero or greater than RSIZE_MAX
    - encoding errors occur in any of string and character conversion specifiers
    - (for `sprintf_s` only), the string to be stored in buffer (including the trailing null) would exceed bufsz.
:   As with all bounds-checked functions, `printf_s`, `fprintf_s`, `sprintf_s`, and `snprintf_s` are only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including <stdio.h>.

### Parameters

|  |  |  |
| --- | --- | --- |
| stream | - | output file stream to write to |
| buffer | - | pointer to a character string to write to |
| bufsz | - | up to bufsz - 1 characters may be written, plus the null terminator |
| format | - | pointer to a null-terminated byte string specifying how to interpret the data |
| ... | - | arguments specifying data to print. If any argument after default argument promotions is not the type expected by the corresponding conversion specification (the expected type is the promoted type or a compatible type of the promoted type), or if there are fewer arguments than required by format, the behavior is undefined. If there are more arguments than required by format, the extraneous arguments are evaluated and ignored. |

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
| ****Length Modifier********→**** | | `hh` (C99) | `h` | (none) | `l` | `ll` (C99) | `j` (C99) | `z` (C99) | `t` (C99) | `L` |
| `%` | Writes literal `%`. The full conversion specification must be `%%`. | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A |
| `c` | Writes a ****single character****.  The argument is first converted to unsigned char. If the ****l**** modifier is used, the argument is first converted to a character string as if by ****%ls**** with a wchar_t[2] argument. | N/A | N/A | int | wint_t | N/A | N/A | N/A | N/A | N/A |
| `s` | Writes a ****character string****  The argument must be a pointer to the initial element of an array of characters. **Precision** specifies the maximum number of bytes to be written. If **Precision** is not specified, writes every byte up to and not including the first null terminator. If the ****l**** specifier is used, the argument must be a pointer to the initial element of an array of wchar_t, which is converted to char array as if by a call to wcrtomb with zero-initialized conversion state. | N/A | N/A | char\* | wchar_t\* | N/A | N/A | N/A | N/A | N/A |
| `d` `i` | Converts a ****signed integer**** into decimal representation **[-]dddd**.  **Precision** specifies the minimum number of digits to appear. The default precision is 1.  If both the converted value and the precision are ​0​ the conversion results in no characters. | signed char | short | int | long | long long | intmax_t | signed size_t | ptrdiff_t | N/A |
| `o` | Converts an ****unsigned integer**** into octal representation **oooo**.  **Precision** specifies the minimum number of digits to appear. The default precision is 1. If both the converted value and the precision are ​0​ the conversion results in no characters. In the **alternative implementation** precision is increased if necessary, to write one leading zero. In that case if both the converted value and the precision are ​0​, single ​0​ is written. | unsigned char | unsigned short | unsigned int | unsigned long | unsigned long long | uintmax_t | size_t | unsigned version of ptrdiff_t | N/A |
| `x` `X` | Converts an ****unsigned integer**** into hexadecimal representation **hhhh**.  For the `x` conversion letters `abcdef` are used.  For the `X` conversion letters `ABCDEF` are used.  **Precision** specifies the minimum number of digits to appear. The default precision is 1. If both the converted value and the precision are ​0​ the conversion results in no characters. In the **alternative implementation** `0x` or `0X` is prefixed to results if the converted value is nonzero. | N/A |
| `u` | Converts an ****unsigned integer**** into decimal representation **dddd**.  **Precision** specifies the minimum number of digits to appear. The default precision is 1. If both the converted value and the precision are ​0​ the conversion results in no characters. | N/A |
| `f` `F` | Converts ****floating-point number**** to the decimal notation in the style **[-]ddd.ddd**.  **Precision** specifies the exact number of digits to appear after the decimal point character. The default precision is 6. In the **alternative implementation** decimal point character is written even if no digits follow it. For infinity and not-a-number conversion style see notes. | N/A | N/A | double | double(C99) | N/A | N/A | N/A | N/A | long double |
| `e` `E` | Converts ****floating-point number**** to the decimal exponent notation.  For the `e` conversion style **[-]d.ddd** ﻿`e`**±dd** is used.  For the `E` conversion style **[-]d.ddd** ﻿`E`**±dd** is used.  The exponent contains at least two digits, more digits are used only if necessary. If the value is ​0​, the exponent is also ​0​. **Precision** specifies the exact number of digits to appear after the decimal point character. The default precision is 6. In the **alternative implementation** decimal point character is written even if no digits follow it. For infinity and not-a-number conversion style see notes. | N/A | N/A | N/A | N/A | N/A | N/A |
| `a` `A` (C99) | Converts ****floating-point number**** to the hexadecimal exponent notation.  For the `a` conversion style **[-]** ﻿`0x`**h.hhh** ﻿`p`**±d** is used.  For the `A` conversion style **[-]** ﻿`0X`**h.hhh** ﻿`P`**±d** is used.  The first hexadecimal digit is not `0` if the argument is a normalized floating-point value. If the value is ​0​, the exponent is also ​0​. **Precision** specifies the exact number of digits to appear after the hexadecimal point character. The default precision is sufficient for exact representation of the value. In the **alternative implementation** decimal point character is written even if no digits follow it. For infinity and not-a-number conversion style see notes. | N/A | N/A | N/A | N/A | N/A | N/A |
| `g` `G` | Converts ****floating-point number**** to decimal or decimal exponent notation depending on the value and the **precision**.  For the `g` conversion style conversion with style `e` or `f` will be performed.  For the `G` conversion style conversion with style `E` or `F` will be performed.  Let `P` equal the precision if nonzero, 6 if the precision is not specified, or 1 if the precision is ​0​. Then, if a conversion with style `E` would have an exponent of `X`:   - if **P > X ≥ −4**, the conversion is with style `f` or `F` and precision **P − 1 − X**. - otherwise, the conversion is with style `e` or `E` and precision **P − 1**.   Unless **alternative representation** is requested the trailing zeros are removed, also the decimal point character is removed if no fractional part is left. For infinity and not-a-number conversion style see notes. | N/A | N/A | N/A | N/A | N/A | N/A |
| `n` | Returns the ****number of characters written**** so far by this call to the function.  The result is **written** to the value pointed to by the argument. The specification may not contain any **flag**, **field width**, or **precision**. | signed char\* | short\* | int\* | long\* | long long\* | intmax_t\* | signed size_t\* | ptrdiff_t\* | N/A |
| `p` | Writes an implementation defined character sequence defining a ****pointer****. | N/A | N/A | void\* | N/A | N/A | N/A | N/A | N/A | N/A |

The floating-point conversion functions convert infinity to `inf` or `infinity`. Which one is used is implementation defined.

Not-a-number is converted to `nan` or `nan(char_sequence)`. Which one is used is implementation defined.

The conversions `F`, `E`, `G`, `A` output `INF`, `INFINITY`, `NAN` instead.

The conversion specifier used to print char, unsigned char, signed char, short, and unsigned short expects promoted types of default argument promotions, but before printing its value will be converted to char, unsigned char, signed char, short, and unsigned short. It is safe to pass values of these types because of the promotion that takes place when a variadic function is called.

The correct conversion specifications for the fixed-width character types (int8_t, etc) are defined in the header <inttypes.h> (although PRIdMAX, PRIuMAX, etc is synonymous with `%jd`, `%ju`, etc).

The memory-writing conversion specifier `%n` is a common target of security exploits where format strings depend on user input and is not supported by the bounds-checked `printf_s` family of functions.

There is a sequence point after the action of each conversion specifier; this permits storing multiple `%n` results in the same variable or, as an edge case, printing a string modified by an earlier `%n` within the same call.

If a conversion specification is invalid, the behavior is undefined.

### Return value

1,2) number of characters transmitted to the output stream or negative value if an output error or an encoding error (for string and character conversion specifiers) occurred.3) number of characters written to buffer (not counting the terminating null character), or a negative value if an encoding error (for string and character conversion specifiers) occurred.4) number of characters (not including the terminating null character) which would have been written to buffer if bufsz was ignored, or a negative value if an encoding error (for string and character conversion specifiers) occurred.5,6) number of characters transmitted to the output stream or negative value if an output error, a runtime constraints violation error, or an encoding error occurred.7) number of characters written to buffer, not counting the null character (which is always written as long as buffer is not a null pointer and bufsz is not zero and not greater than RSIZE_MAX), or zero on runtime constraint violations, and negative value on encoding errors.8) number of characters not including the terminating null character (which is always written as long as buffer is not a null pointer and bufsz is not zero and not greater than RSIZE_MAX), which would have been written to buffer if bufsz was ignored, or a negative value if a runtime constraints violation or an encoding error occurred.

### Notes

The C standard and POSIX specify that the behavior of `sprintf` and its variants is undefined when an argument overlaps with the destination buffer. Example:

```
sprintf(dst, "%s and %s", dst, t); // <- broken: undefined behavior

```

POSIX specifies that errno is set on error. It also specifies additional conversion specifications, most notably support for argument reordering (n$ immediately after % indicates `n`th argument).

Calling `snprintf` with zero bufsz and null pointer for buffer is useful to determine the necessary buffer size to contain the output:

```
const char fmt[] = "sqrt(2) = %f";
int sz = snprintf(NULL, 0, fmt, sqrt(2));
char buf[sz + 1]; // note +1 for terminating null byte
snprintf(buf, sizeof buf, fmt, sqrt(2));

```

`snprintf_s`, just like `snprintf`, but unlike `sprintf_s`, will truncate the output to fit in bufsz - 1.

### Example

Run this code

```
#include <inttypes.h>
#include <stdint.h>
#include <stdio.h>
 
int main(void)
{
    const char* s = "Hello";
    printf("Strings:\n"); // same as puts("Strings");
    printf(" padding:\n");
    printf("\t[%10s]\n", s);
    printf("\t[%-10s]\n", s);
    printf("\t[%*s]\n", 10, s);
    printf(" truncating:\n");
    printf("\t%.4s\n", s);
    printf("\t%.*s\n", 3, s);
 
    printf("Characters:\t%c %%\n", 'A');
 
    printf("Integers:\n");
    printf("\tDecimal:\t%i %d %.6i %i %.0i %+i %i\n",
                         1, 2,   3, 0,   0,  4,-4);
    printf("\tHexadecimal:\t%x %x %X %#x\n", 5, 10, 10, 6);
    printf("\tOctal:\t\t%o %#o %#o\n", 10, 10, 4);
 
    printf("Floating-point:\n");
    printf("\tRounding:\t%f %.0f %.32f\n", 1.5, 1.5, 1.3);
    printf("\tPadding:\t%05.2f %.2f %5.2f\n", 1.5, 1.5, 1.5);
    printf("\tScientific:\t%E %e\n", 1.5, 1.5);
    printf("\tHexadecimal:\t%a %A\n", 1.5, 1.5);
    printf("\tSpecial values:\t0/0=%g 1/0=%g\n", 0.0 / 0.0, 1.0 / 0.0);
 
    printf("Fixed-width types:\n");
    printf("\tLargest 32-bit value is %" PRIu32 " or %#" PRIx32 "\n",
                                     UINT32_MAX,     UINT32_MAX );
}

```

Possible output:

```
Strings:
 padding:
        [     Hello]
        [Hello     ]
        [     Hello]
 truncating:
        Hell
        Hel
Characters:     A %
Integers:
        Decimal:        1 2 000003 0  +4 -4
        Hexadecimal:    5 a A 0x6
        Octal:          12 012 04
Floating-point:
        Rounding:       1.500000 2 1.30000000000000004440892098500626
        Padding:        01.50 1.50  1.50
        Scientific:     1.500000E+00 1.500000e+00
        Hexadecimal:    0x1.8p+0 0X1.8P+0
        Special values: 0/0=-nan 1/0=inf
Fixed-width types:
        Largest 32-bit value is 4294967295 or 0xffffffff

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.21.6.1 The fprintf function (p: TBD)

:   - 7.21.6.3 The printf function (p: TBD)

:   - 7.21.6.5 The snprintf function (p: TBD)

:   - 7.21.6.6 The sprintf function (p: TBD)

:   - K.3.5.3.1 The fprintf_s function (p: TBD)

:   - K.3.5.3.3 The printf_s function (p: TBD)

:   - K.3.5.3.5 The snprintf_s function (p: TBD)

:   - K.3.5.3.6 The sprintf_s function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.21.6.1 The fprintf function (p: 225-230)

:   - 7.21.6.3 The printf function (p: 236)

:   - 7.21.6.5 The snprintf function (p: 237)

:   - 7.21.6.6 The sprintf function (p: 237)

:   - K.3.5.3.1 The fprintf_s function (p: 430)

:   - K.3.5.3.3 The printf_s function (p: 432)

:   - K.3.5.3.5 The snprintf_s function (p: 432-433)

:   - K.3.5.3.6 The sprintf_s function (p: 433)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.21.6.1 The fprintf function (p: 309-316)

:   - 7.21.6.3 The printf function (p: 324)

:   - 7.21.6.5 The snprintf function (p: 325)

:   - 7.21.6.6 The sprintf function (p: 325-326)

:   - K.3.5.3.1 The fprintf_s function (p: 591)

:   - K.3.5.3.3 The printf_s function (p: 593-594)

:   - K.3.5.3.5 The snprintf_s function (p: 594-595)

:   - K.3.5.3.6 The sprintf_s function (p: 595-596)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.19.6.1 The fprintf function (p: 274-282)

:   - 7.19.6.3 The printf function (p: 290)

:   - 7.19.6.5 The snprintf function (p: 290-291)

:   - 7.19.6.6 The sprintf function (p: 291)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.9.6.1 The fprintf function

:   - 4.9.6.3 The printf function

:   - 4.9.6.5 The sprintf function

### See also

|  |  |
| --- | --- |
| wprintffwprintfswprintfwprintf_sfwprintf_sswprintf_ssnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | prints formatted wide character output to stdout, a file stream or a buffer   (function) |
| vprintfvfprintfvsprintfvsnprintfvprintf_svfprintf_svsprintf_svsnprintf_s(C99)(C11)(C11)(C11)(C11) | prints formatted output to stdout, a file stream or a buffer  using variable argument list   (function) |
| fputs | writes a character string to a file stream   (function) |
| scanffscanfsscanfscanf_sfscanf_ssscanf_s(C11)(C11)(C11) | reads formatted input from stdin, a file stream or a buffer   (function) |
| C++ documentation for printf, fprintf, sprintf, snprintf | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/io/fprintf&oldid=179645>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 January 2025, at 04:19.