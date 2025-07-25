# bsearch, bsearch_s

From cppreference.com
< c‎ | algorithm
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

 Algorithms

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| qsortqsort_s(C11) | | | | |
| ****bsearchbsearch_s****(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdlib.h>` |  |  |
| void\* bsearch( const void \*key, const void \*ptr, size_t count, size_t size,                 int (\*comp)(const void\*, const void\*) ); | (1) |  |
| void\* bsearch_s( const void \*key, const void \*ptr, rsize_t count, rsize_t size,  int (\*comp)(const void \*, const void \*, void \*), void \*context ); | (2) | (since C11) |
| /\*QVoid\*/\* bsearch( const void \*key, /\*QVoid\*/ \*ptr, size_t count, size_t size,                      int (\*comp)(const void\*, const void\*) ); | (3) | (since C23) |
| /\*QVoid\*/\* bsearch_s( const void \*key, /\*QVoid\*/ \*ptr, rsize_t count, rsize_t size,  int (\*comp)(const void \*, const void \*, void \*), void \*context ); | (4) | (since C23) |
|  |  |  |

1) Finds an element equal to element pointed to by `key` in an array pointed to by `ptr`. The array contains `count` elements of `size` bytes and must be partitioned with respect to `key`, that is, all the elements that compare less than must appear before all the elements that compare equal to, and those must appear before all the elements that compare greater than the key object. A fully sorted array satisfies these requirements. The elements are compared using function pointed to by `comp`. The behavior is undefined if the array is not already partitioned with respect to `*key` in ascending order according to the same criterion that `comp` uses.2) Same as (1), except that the additional state argument `context` is passed to `comp` and that the following errors are detected at runtime and call the currently installed constraint handler function:

:   - `count` or `size` is greater than RSIZE_MAX
    - `key`, `ptr` or `comp` is a null pointer (unless `count` is zero)
:   As with all bounds-checked functions, `bsearch_s`  (and the corresponding type-generic macro)(since C23) is only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including <stdlib.h>.

3,4) Type-generic macros equivalent to (1) and (2) respectively. Let `T` be a unqualified object type (including void).

:   - If `ptr` is of type const T\*, the return type is const void\*.
    - Otherwise, if `ptr` is of type T\*, the return type is void\*.
    - Otherwise, the behavior is undefined.

If a macro definition of each of these generic functions is suppressed to access an actual function (e.g. if (bsearch), (bsearch_s), or a function pointer is used), the actual function declaration (1) or (2) becomes visible.

If the array contains several elements that `comp` would indicate as equal to the element searched for, then it is unspecified which element the function will return as the result.

|  |  |
| --- | --- |
| Direct usages of actual functions (1) and (2) are deprecated. | (since C23) |

### Parameters

|  |  |  |
| --- | --- | --- |
| key | - | pointer to the element to search for |
| ptr | - | pointer to the array to examine |
| count | - | number of element in the array |
| size | - | size of each element in the array in bytes |
| comp | - | comparison function which returns ​a negative integer value if the first argument is **less** than the second, a positive integer value if the first argument is **greater** than the second and zero if the arguments are equivalent. `key` is passed as the first argument, an element from the array as the second.  The signature of the comparison function should be equivalent to the following:   int cmp(const void \*a, const void \*b);  The function must not modify the objects passed to it and must return consistent results when called for the same objects, regardless of their positions in the array.  ​ |
| context | - | state of the comparator (e.g., collating sequence), passed to `comp` as the third argument |

### Return value

1) Pointer to an element in the array that compares equal to \*key, or null pointer if such element has not been found.2) Same as (1), except that the null pointer is also returned on runtime constraints violations.3,4) Same as (1) and (2) respectively, except that cv-qualification is adjusted.

### Notes

Despite the name, neither C nor POSIX standards require this function to be implemented using binary search or make any complexity guarantees.

Unlike other bounds-checked functions, `bsearch_s` does not treat arrays of zero size as a runtime constraint violation and instead indicates element not found (the other function that accepts arrays of zero size is qsort_s).

Until `bsearch_s`, users of `bsearch` often used global variables to represent the state of the comparator.

### Example

Run this code

```
#include <stdlib.h>
#include <stdio.h>
 
struct data {
    int nr;
    char const *value;
} dat[] = {
    {1, "Foo"}, {2, "Bar"}, {3, "Hello"}, {4, "World"}
};
 
int data_cmp(void const *lhs, void const *rhs) 
{
    struct data const *const l = lhs;
    struct data const *const r = rhs;
 
    if (l->nr < r->nr) return -1;
    else if (l->nr > r->nr) return 1;
    else return 0;
 
    // return (l->nr > r->nr) - (l->nr < r->nr); // possible shortcut
    // return l->nr - r->nr; // erroneous shortcut (fails if INT_MIN is present)
}
 
int main(void) 
{
    struct data key = { .nr = 3 };
    struct data const *res = bsearch(&key, dat, sizeof dat / sizeof dat[0],
                                     sizeof dat[0], data_cmp);
    if (res) {
        printf("No %d: %s\n", res->nr, res->value);
    } else {
        printf("No %d not found\n", key.nr);
    }
}

```

Output:

```
No 3: Hello

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.22.5.1 The bsearch function (p: 258)

:   - K.3.6.3.1 The bsearch_s function (p: 441-442)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.22.5.1 The bsearch function (p: 355)

:   - K.3.6.3.1 The bsearch_s function (p: 608-609)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.20.5.1 The bsearch function (p: 318-319)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.10.5.1 The bsearch function

### See also

|  |  |
| --- | --- |
| qsortqsort_s(C11) | sorts a range of elements with unspecified type   (function) |
| C++ documentation for bsearch | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/algorithm/bsearch&oldid=144569>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 October 2022, at 19:13.