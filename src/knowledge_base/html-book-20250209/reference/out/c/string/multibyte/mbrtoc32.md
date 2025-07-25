# mbrtoc32

From cppreference.com
< c‎ | string‎ | multibyte
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

 Strings library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Null-terminated byte strings | | | | |
| Null-terminated multibyte strings | | | | |
| Null-terminated wide strings | | | | |

 Null-terminated multibyte strings

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Wide/multibyte conversions | | | | |
| mbsinit(C95) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstowcsmbstowcs_s(C11) | | | | | | btowc(C95) | | | | | | mbrtowc(C95) | | | | | | mbsrtowcsmbsrtowcs_s(C95)(C11) | | | | | | mbrtoc8(C23) | | | | | | c8rtomb(C23) | | | | | | mbrtoc16(C11) | | | | | | c16rtomb(C11) | | | | | | c32rtomb(C11) | | | | | | ****mbrtoc32****(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbtowc | | | | | | wctombwctomb_s(C11) | | | | | | wcstombswcstombs_s(C11) | | | | | | wctob(C95) | | | | | | wcrtombwcrtomb_s(C95)(C11) | | | | | | wcsrtombswcsrtombs_s(C95)(C11) | | | | | | mbrlen(C95) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstate_t(C95) | | | | | | char8_t(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | char16_t(C11) | | | | | | char32_t(C11) | | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_CUR_MAX | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<uchar.h>` |  |  |
| size_t mbrtoc32( char32_t restrict \* pc32, const char \* restrict s,                   size_t n, mbstate_t \* restrict ps ); |  | (since C11) |
|  |  |  |

Converts a single code point from its narrow multibyte character representation to its variable-length 32-bit wide character representation (but typically, UTF-32).

If `s` is not a null pointer, inspects at most `n` bytes of the multibyte character string, beginning with the byte pointed to by `s` to determine the number of bytes necessary to complete the next multibyte character (including any shift sequences, and taking into account the current multibyte conversion state \*ps). If the function determines that the next multibyte character in `s` is complete and valid, converts it to the corresponding 32-bit wide character and stores it in \*pc32 (if `pc32` is not null).

If the multibyte character in `*s` corresponds to a multi-char32_t sequence (not possible with UTF-32), then after the first call to this function, `*ps` is updated in such a way that the next calls to `mbrtoc32` will write out the additional char32_t, without considering `*s`.

If `s` is a null pointer, the values of `n` and `pc32` are ignored and the call is equivalent to mbrtoc32(NULL, "", 1, ps).

If the wide character produced is the null character, the conversion state \*ps represents the initial shift state.

If the macro __STDC_UTF_32__ is defined, the 32-bit encoding used by this function is UTF-32; otherwise, it is implementation-defined. The macro is always defined and the encoding is always UTF-32.(since C23) In any case, the multibyte character encoding used by this function is specified by the currently active C locale.

### Parameters

|  |  |  |
| --- | --- | --- |
| pc32 | - | pointer to the location where the resulting 32-bit wide character will be written |
| s | - | pointer to the multibyte character string used as input |
| n | - | limit on the number of bytes in s that can be examined |
| ps | - | pointer to the conversion state object used when interpreting the multibyte string |

### Return value

The first of the following that applies:

- ​0​ if the character converted from `s` (and stored in \*pc32 if non-null) was the null character
- the number of bytes [1...n] of the multibyte character successfully converted from `s`
- (size_t)-3 if the next char32_t from a multi-char32_t character has now been written to \*pc32. No bytes are processed from the input in this case.
- (size_t)-2 if the next `n` bytes constitute an incomplete, but so far valid, multibyte character. Nothing is written to \*pc32.
- (size_t)-1 if encoding error occurs. Nothing is written to `*pc32`, the value EILSEQ is stored in errno and the value of \*ps is unspecified.

### Example

Run this code

```
#include <stdio.h>
#include <locale.h>
#include <string.h>
#include <uchar.h>
#include <assert.h>
 
int main(void)
{
    setlocale(LC_ALL, "en_US.utf8");
    char in[] = u8"zß水🍌"; // or "z\u00df\u6c34\U0001F34C"
    const size_t in_size = sizeof in / sizeof *in;
 
    printf("Processing %zu UTF-8 code units: [ ", in_size);
    for (size_t i = 0; i < in_size; ++i)
        printf("0x%02x ", (unsigned char)in[i]);
 
    puts("]");
 
    char32_t out[in_size];
    char32_t *p_out = out;
    char *p_in = in, *end = in + in_size;
    mbstate_t state;
    memset(&state, 0, sizeof(state));
    size_t rc;
    while ((rc = mbrtoc32(p_out, p_in, end - p_in, &state)))
    {
        assert(rc != (size_t)-3); // no surrogate pairs in UTF-32
        if (rc == (size_t)-1) break; // invalid input
        if (rc == (size_t)-2) break; // truncated input
        p_in += rc;
        ++p_out;
    }
 
    size_t out_size = p_out+1 - out;
    printf("into %zu UTF-32 code units: [ ", out_size);
    for (size_t i = 0; i < out_size; ++i)
        printf("0x%08X ", out[i]);
 
    puts("]");
}

```

Output:

```
Processing 11 UTF-8 code units: [ 0x7a 0xc3 0x9f 0xe6 0xb0 0xb4 0xf0 0x9f 0x8d 0x8c 0x00 ]
into 5 UTF-32 code units: [ 0x0000007A 0x000000DF 0x00006C34 0x0001F34C 0x00000000 ]

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.30.1.5 The mbrtoc32 function (p: 410)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.28.1.3 The mbrtoc32 function (p: 293-294)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.28.1.3 The mbrtoc32 function (p: 400-401)

### See also

|  |  |
| --- | --- |
| c32rtomb(C11) | converts a UTF-32 character to narrow multibyte encoding   (function) |
| C++ documentation for mbrtoc32 | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/multibyte/mbrtoc32&oldid=153898>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 June 2023, at 06:59.