# Alternative operators and tokens

From cppreference.com
< c‎ | language
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

 C language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Basic concepts | | | | |
| Keywords | | | | |
| Preprocessor | | | | |
| Statements | | | | |
| Expressions | | | | |
| Initialization | | | | |
| Declarations | | | | |
| Functions | | | | |
| Miscellaneous | | | | |
| History of C | | | | |
| Technical Specifications | | | | |

C source code may be written in any 8-bit character set that includes the ISO 646:1983 invariant character set, even non-ASCII ones. However, several C operators and punctuators require characters that are outside of the ISO 646 codeset: `{, }, [, ], #, \, ^, |, ~`. To be able to use character encodings where some or all of these symbols do not exist (such as the German DIN 66003), there are two possibilities: alternative spellings of operators that use these characters or special combinations of two or three ISO 646 compatible characters that are interpreted as if they were a single non-ISO 646 character.

## Operator macros (C95)

There are alternative spellings for the operators that use non-ISO646 characters, defined in ****<iso646.h>**** as macros:

|  |  |
| --- | --- |
| Defined in header `<iso646.h>` | |
| Primary | Alternative |
| `&&` | `and`   (operator macro) |
| `&=` | `and_eq`   (operator macro) |
| `&` | `bitand`   (operator macro) |
| `|` | `bitor`   (operator macro) |
| `~` | `compl`   (operator macro) |
| `!` | `not`   (operator macro) |
| `!=` | `not_eq`   (operator macro) |
| `||` | `or`   (operator macro) |
| `|=` | `or_eq`   (operator macro) |
| `^` | `xor`   (operator macro) |
| `^=` | `xor_eq`   (operator macro) |

The characters & and ! are invariant under ISO-646, but alternatives are provided for the operators that use these characters anyway to accommodate even more restrictive historical charsets.

There is no alternative spelling (such as eq) for the equality operator == because the character = was present in all supported charsets.

## Alternative tokens (C95)

The following alternative tokens are part of the core language, and, in all respects of the language, each alternative token behaves exactly the same as its primary token, except for its spelling (the stringification operator can make the spelling visible). The two-letter alternative tokens are sometimes called "digraphs" (even though it is four letters long %:%: is also considered a digraph).

| Primary | Alternative |
| --- | --- |
| `{` | `<%` |
| } | `%>` |
| `[` | `<:` |
| `]` | `:>` |
| `#` | `%:` |
| `##` | `%:%:` |

## Trigraphs (removed in C23)

The following three-character groups (trigraphs) are parsed before comments and string literals are recognized, and each appearance of a trigraph is replaced by the corresponding primary character:

| Primary | Trigraph |
| --- | --- |
| `{` | `??<` |
| } | `??>` |
| `[` | `??(` |
| `]` | `??)` |
| `#` | `??=` |
| `\` | `??/` |
| `^` | `??'` |
| `|` | `??!` |
| `~` | `??-` |

Because trigraphs are processed early, a comment such as // Will the next line be executed?????/ will effectively comment out the following line, and the string literal such as "What's going on??!" is parsed as "What's going on|".

### Example

Demonstrates alternative operator spellings from the ****<iso646.h>**** as well as use of digraphs and trigraphs.
If command line arguments contain spaces they should be wrapped in the quotation marks, e.g., "Third World!".

Run this code

```
%:include <stdio.h>
%:include <stdlib.h>
??=include <iso646.h>
 
int main(int argc, char** argv)
??<
    if (argc > 1 and argv<:1:> not_eq NULL)
    <%
       printf("Hello %s??/n", argv<:1:>);
    %>
    else
    <%
       printf("Hello %s??/n", argc? argv??(42??'42??) : __FILE__);
    %>
 
    return EXIT_SUCCESS;
??>

```

Possible output:

```
Hello ./a.out

```

### See also

|  |  |
| --- | --- |
| C++ documentation for Alternative operator representations | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/operator_alternative&oldid=180061>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 February 2025, at 16:04.