# va_copy

From cppreference.com
< c‎ | variadic
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

 Variadic functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| va_start | | | | |
| va_arg | | | | |
| ****va_copy****(C99) | | | | |
| va_end | | | | |
| va_list | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdarg.h>` |  |  |
| void va_copy( va_list dest, va_list src ); |  | (since C99) |
|  |  |  |

The `va_copy` macro copies `src` to `dest`.

va_end should be called on `dest` before the function returns or any subsequent re-initialization of `dest` (via calls to va_start or va_copy).

### Parameters

|  |  |  |
| --- | --- | --- |
| dest | - | an instance of the va_list type to initialize |
| src | - | the source va_list that will be used to initialize `dest` |

### Expanded value

(none)

### Example

Run this code

```
#include <stdio.h>
#include <stdarg.h>
#include <math.h>
 
double sample_stddev(int count, ...) 
{
    /* Compute the mean with args1. */
    double sum = 0;
    va_list args1;
    va_start(args1, count);
    va_list args2;
    va_copy(args2, args1);   /* copy va_list object */
    for (int i = 0; i < count; ++i) {
        double num = va_arg(args1, double);
        sum += num;
    }
    va_end(args1);
    double mean = sum / count;
 
    /* Compute standard deviation with args2 and mean. */
    double sum_sq_diff = 0;
    for (int i = 0; i < count; ++i) {
        double num = va_arg(args2, double);
        sum_sq_diff += (num-mean) * (num-mean);
    }
    va_end(args2);
    return sqrt(sum_sq_diff / count);
}
 
int main(void) 
{
    printf("%f\n", sample_stddev(4, 25.0, 27.3, 26.9, 25.7));
}

```

Possible output:

```
0.920258

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.16.1.2 The va_copy macro (p: 270)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.15.1.2 The va_copy macro (p: 250)

### See also

|  |  |
| --- | --- |
| va_arg | accesses the next variadic function argument   (function macro) |
| va_end | ends traversal of the variadic function arguments   (function macro) |
| va_list | holds the information needed by va_start, va_arg, va_end, and va_copy   (typedef) |
| va_start | enables access to variadic function arguments   (function macro) |
| C++ documentation for va_copy | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/variadic/va_copy&oldid=117388>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 March 2020, at 01:14.