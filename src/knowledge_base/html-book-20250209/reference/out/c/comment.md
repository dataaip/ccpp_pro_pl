# Comments

From cppreference.com
< c
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

 Basic Concepts

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****Comments**** | | | | |
| ASCII | | | | |
| Character sets | | | | |
| Translation phases | | | | |
| Punctuation | | | | |
| Identifier | | | | |
| Scope | | | | |
| Lifetime | | | | |
| Lookup and name spaces | | | | |
| Type | | | | |
| Arithmetic types | | | | |
| Objects and alignment | | | | |
| The main() function | | | | |
| The as-if rule | | | | |
| Undefined behavior | | | | |
| Memory model and data races | | | | |

Comments serve as a sort of in-code documentation. When inserted into a program, they are effectively ignored by the compiler; they are solely intended to be used as notes by the humans that read source code.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `/*` comment `*/` | (1) |  |
|  | | | | | | | | | |
| `//` comment | (2) | (since C99) |
|  | | | | | | | | | |

1) Often known as "C-style" or "multi-line" comments.2) Often known as "C++-style" or "single-line" comments.

All comments are removed from the program at translation phase 3 by replacing each comment with a single whitespace character.

### C-style

C-style comments are usually used to comment large blocks of text or small fragments of code; however, they can be used to comment single lines. To insert text as a C-style comment, simply surround the text with `/*` and `*/`. C-style comments tell the compiler to ignore all content between `/*` and `*/`. Although it is not part of the C standard, `/**` and `**/` are often used to indicate documentation blocks; this is legal because the second asterisk is simply treated as part of the comment.

Except within a character constant, a string literal, or a comment, the characters `/*` introduce a comment. The contents of such a comment are examined only to identify multibyte characters and to find the characters `*/` that terminate the comment. C-style comments cannot be nested.

|  |  |
| --- | --- |
| C++-style C++-style comments are usually used to comment single lines of text or code; however, they can be placed together to form multi-line comments. To insert text as a C++-style comment, simply precede the text with `//` and follow the text with the new line character. C++-style comments tell the compiler to ignore all content between `//` and a new line.  Except within a character constant, a string literal, or a comment, the characters `//` introduce a comment that includes all multibyte characters up to, but not including, the next new-line character. The contents of such a comment are examined only to identify multibyte characters and to find the new-line character that terminates the comment. C++-style comments can be nested:   ```text //  y = f(x);   // invoke algorithm ```   A C-style comment may appear within a C++-style comment:   ```text //  y = f(x);   /* invoke algorithm */ ```   A C++-style comment may appear within a C-style comment; this is a mechanism for excluding a small block of source code:   ```text /*     y = f(x);   // invoke algorithms     z = g(x); */ ``` | (since C99) |

### Notes

Because comments are removed before the preprocessor stage, a macro cannot be used to form a comment and an unterminated C-style comment doesn't spill over from an #include'd file.

```
/* An attempt to use a macro to form a comment. */
/* But, a space replaces characters "//".       */
#ifndef DEBUG
    #define PRINTF //
#else
    #define PRINTF printf
#endif
...  
PRINTF("Error in file %s at line %i\n", __FILE__, __LINE__);

```

Besides commenting out, other mechanisms used for source code exclusion are:

```
#if 0
    puts("this will not be compiled");
    /* no conflict with C-style comments */
    // no conflict with C++-style comments
#endif

```

and

```
if(0) {
    puts("this will be compiled but not be executed");
    /* no conflict with C-style comments */
    // no conflict with C++-style comments
}

```

The introduction of // comments in C99 was a breaking change in some rare circumstances:

```
a = b //*divisor:*/ c
+ d; /* C89 compiles a = b / c + d;
        C99 compiles a = b + d; */

```

### Example

Run this code

```
#include <stdio.h>
/*
C-style comments can contain
multiple lines.
*/
 
/* Or, just one line. */
 
// C++-style comments can comment one line.
 
// Or, they can
// be strung together.
 
int main(void)
{
  // The below code won't be run
  // puts("Hello");
 
  // The below code will be run
  puts("World");
 
  // A note regarding backslash + newline.
  // Despite belonging to translation phase 2 (vs phase 3 for comments),
  // '\' still determines which portion of the source code is considered
  // as 'comments':
  // This comment will be promoted to the next line \
  puts("Won't be run"); // may issue a warning "multi-line comment"
  puts("Hello, again");
}

```

Output:

```
World
Hello, again

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.4.9 Comments (p: 54)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.4.9 Comments (p: 75)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.4.9 Comments (p: 66)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.1.9 Comments

### See also

|  |  |
| --- | --- |
| C++ documentation for Comments | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/comment&oldid=146308>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 January 2023, at 00:14.