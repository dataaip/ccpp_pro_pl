# Standard library header <cmath>

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | ****<cmath>**** | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header was originally in the C standard library as <math.h>.

This header is part of the numeric library.

|  |  |
| --- | --- |
| Types | |
| float_t(C++11) | most efficient floating-point type at least as wide as float   (typedef) |
| double_t(C++11) | most efficient floating-point type at least as wide as double   (typedef) |
| Macros | |
| HUGE_VALFHUGE_VALHUGE_VALL(C++11)(C++11) | indicates the overflow value for float, double and long double respectively   (macro constant) |
| INFINITY(C++11) | evaluates to positive infinity or the value guaranteed to overflow a float   (macro constant) |
| NAN(C++11) | evaluates to a quiet NaN of type float   (macro constant) |
| math_errhandlingMATH_ERRNOMATH_ERREXCEPT(C++11)(C++11)(C++11) | defines the error handling mechanism used by the common mathematical functions   (macro constant) |
| Classification | |
| FP_NORMALFP_SUBNORMALFP_ZEROFP_INFINITEFP_NAN(C++11)(C++11)(C++11)(C++11)(C++11) | indicates a floating-point category   (macro constant) |
| Functions | |
| Basic operations | |
| abs(float)fabsfabsffabsl(C++11)(C++11) | absolute value of a floating point value (\(\small{|x|}\)|x|)   (function) |
| fmodfmodffmodl(C++11)(C++11) | remainder of the floating point division operation   (function) |
| remainderremainderfremainderl(C++11)(C++11)(C++11) | signed remainder of the division operation   (function) |
| remquoremquofremquol(C++11)(C++11)(C++11) | signed remainder as well as the three last bits of the division operation   (function) |
| fmafmaffmal(C++11)(C++11)(C++11) | fused multiply-add operation   (function) |
| fmaxfmaxffmaxl(C++11)(C++11)(C++11) | larger of two floating-point values   (function) |
| fminfminffminl(C++11)(C++11)(C++11) | smaller of two floating point values   (function) |
| fdimfdimffdiml(C++11)(C++11)(C++11) | positive difference of two floating point values (\({\small\max{(0, x-y)}}\)max(0, x-y))   (function) |
| nannanfnanl(C++11)(C++11)(C++11) | not-a-number (NaN)   (function) |
| Linear interpolation | |
| lerp(C++20) | linear interpolation function   (function) |
| Exponential functions | |
| expexpfexpl(C++11)(C++11) | returns e raised to the given power (\({\small e^x}\)ex)   (function) |
| exp2exp2fexp2l(C++11)(C++11)(C++11) | returns 2 raised to the given power (\({\small 2^x}\)2x)   (function) |
| expm1expm1fexpm1l(C++11)(C++11)(C++11) | returns e raised to the given power, minus 1 (\({\small e^x-1}\)ex-1)   (function) |
| loglogflogl(C++11)(C++11) | computes natural (base e) logarithm (\({\small\ln{x}}\)ln(x))   (function) |
| log10log10flog10l(C++11)(C++11) | computes common (base 10) logarithm (\({\small\log_{10}{x}}\)log10(x))   (function) |
| log2log2flog2l(C++11)(C++11)(C++11) | base 2 logarithm of the given number (\({\small\log_{2}{x}}\)log2(x))   (function) |
| log1plog1pflog1pl(C++11)(C++11)(C++11) | natural logarithm (to base e) of 1 plus the given number (\({\small\ln{(1+x)}}\)ln(1+x))   (function) |
| Power functions | |
| powpowfpowl(C++11)(C++11) | raises a number to the given power (\(\small{x^y}\)xy)   (function) |
| sqrtsqrtfsqrtl(C++11)(C++11) | computes square root (\(\small{\sqrt{x}}\)√x)   (function) |
| cbrtcbrtfcbrtl(C++11)(C++11)(C++11) | computes cube root (\(\small{\sqrt[3]{x}}\)3√x)   (function) |
| hypothypotfhypotl(C++11)(C++11)(C++11) | computes hypotenuse \(\scriptsize{\sqrt{x^2+y^2}}\)√x2 +y2  and \(\scriptsize{\sqrt{x^2+y^2+z^2}}\)√x2 +y2 +z2 (since C++17)   (function) |
| Trigonometric functions | |
| sinsinfsinl(C++11)(C++11) | computes sine (\({\small\sin{x}}\)sin(x))   (function) |
| coscosfcosl(C++11)(C++11) | computes cosine (\({\small\cos{x}}\)cos(x))   (function) |
| tantanftanl(C++11)(C++11) | computes tangent (\({\small\tan{x}}\)tan(x))   (function) |
| asinasinfasinl(C++11)(C++11) | computes arc sine (\({\small\arcsin{x}}\)arcsin(x))   (function) |
| acosacosfacosl(C++11)(C++11) | computes arc cosine (\({\small\arccos{x}}\)arccos(x))   (function) |
| atanatanfatanl(C++11)(C++11) | computes arc tangent (\({\small\arctan{x}}\)arctan(x))   (function) |
| atan2atan2fatan2l(C++11)(C++11) | arc tangent, using signs to determine quadrants   (function) |
| Hyperbolic functions | |
| sinhsinhfsinhl(C++11)(C++11) | computes hyperbolic sine (\({\small\sinh{x}}\)sinh(x))   (function) |
| coshcoshfcoshl(C++11)(C++11) | computes hyperbolic cosine (\({\small\cosh{x}}\)cosh(x))   (function) |
| tanhtanhftanhl(C++11)(C++11) | computes hyperbolic tangent (\({\small\tanh{x}}\)tanh(x))   (function) |
| asinhasinhfasinhl(C++11)(C++11)(C++11) | computes the inverse hyperbolic sine (\({\small\operatorname{arsinh}{x}}\)arsinh(x))   (function) |
| acoshacoshfacoshl(C++11)(C++11)(C++11) | computes the inverse hyperbolic cosine (\({\small\operatorname{arcosh}{x}}\)arcosh(x))   (function) |
| atanhatanhfatanhl(C++11)(C++11)(C++11) | computes the inverse hyperbolic tangent (\({\small\operatorname{artanh}{x}}\)artanh(x))   (function) |
| Error and gamma functions | |
| erferfferfl(C++11)(C++11)(C++11) | error function   (function) |
| erfcerfcferfcl(C++11)(C++11)(C++11) | complementary error function   (function) |
| tgammatgammaftgammal(C++11)(C++11)(C++11) | gamma function   (function) |
| lgammalgammaflgammal(C++11)(C++11)(C++11) | natural logarithm of the gamma function   (function) |
| Nearest integer floating-point operations | |
| ceilceilfceill(C++11)(C++11) | nearest integer not less than the given value   (function) |
| floorfloorffloorl(C++11)(C++11) | nearest integer not greater than the given value   (function) |
| trunctruncftruncl(C++11)(C++11)(C++11) | nearest integer not greater in magnitude than the given value   (function) |
| roundroundfroundllroundlroundflroundlllroundllroundfllroundl(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | nearest integer, rounding away from zero in halfway cases   (function) |
| nearbyintnearbyintfnearbyintl(C++11)(C++11)(C++11) | nearest integer using current rounding mode   (function) |
| rintrintfrintllrintlrintflrintlllrintllrintfllrintl(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | nearest integer using current rounding mode with exception if the result differs   (function) |
| Floating-point manipulation functions | |
| frexpfrexpffrexpl(C++11)(C++11) | decomposes a number into significand and base-2 exponent   (function) |
| ldexpldexpfldexpl(C++11)(C++11) | multiplies a number by 2 raised to an integral power   (function) |
| modfmodffmodfl(C++11)(C++11) | decomposes a number into integer and fractional parts   (function) |
| scalbnscalbnfscalbnlscalblnscalblnfscalblnl(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | multiplies a number by FLT_RADIX raised to a power   (function) |
| ilogbilogbfilogbl(C++11)(C++11)(C++11) | extracts exponent of the number   (function) |
| logblogbflogbl(C++11)(C++11)(C++11) | extracts exponent of the number   (function) |
| nextafternextafterfnextafterlnexttowardnexttowardfnexttowardl(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | next representable floating-point value towards the given value   (function) |
| copysigncopysignfcopysignl(C++11)(C++11)(C++11) | copies the sign of a floating point value   (function) |
| Classification and comparison | |
| fpclassify(C++11) | categorizes the given floating-point value   (function) |
| isfinite(C++11) | checks if the given number has finite value   (function) |
| isinf(C++11) | checks if the given number is infinite   (function) |
| isnan(C++11) | checks if the given number is NaN   (function) |
| isnormal(C++11) | checks if the given number is normal   (function) |
| signbit(C++11) | checks if the given number is negative   (function) |
| isgreater(C++11) | checks if the first floating-point argument is greater than the second   (function) |
| isgreaterequal(C++11) | checks if the first floating-point argument is greater or equal than the second   (function) |
| isless(C++11) | checks if the first floating-point argument is less than the second   (function) |
| islessequal(C++11) | checks if the first floating-point argument is less or equal than the second   (function) |
| islessgreater(C++11) | checks if the first floating-point argument is less or greater than the second   (function) |
| isunordered(C++11) | checks if two floating-point values are unordered   (function) |
| Mathematical special functions | |
| assoc_laguerreassoc_laguerrefassoc_laguerrel(C++17)(C++17)(C++17) | associated Laguerre polynomials   (function) |
| assoc_legendreassoc_legendrefassoc_legendrel(C++17)(C++17)(C++17) | associated Legendre polynomials   (function) |
| betabetafbetal(C++17)(C++17)(C++17) | beta function   (function) |
| comp_ellint_1comp_ellint_1fcomp_ellint_1l(C++17)(C++17)(C++17) | (complete) elliptic integral of the first kind   (function) |
| comp_ellint_2comp_ellint_2fcomp_ellint_2l(C++17)(C++17)(C++17) | (complete) elliptic integral of the second kind   (function) |
| comp_ellint_3comp_ellint_3fcomp_ellint_3l(C++17)(C++17)(C++17) | (complete) elliptic integral of the third kind   (function) |
| cyl_bessel_icyl_bessel_ifcyl_bessel_il(C++17)(C++17)(C++17) | regular modified cylindrical Bessel functions   (function) |
| cyl_bessel_jcyl_bessel_jfcyl_bessel_jl(C++17)(C++17)(C++17) | cylindrical Bessel functions (of the first kind)   (function) |
| cyl_bessel_kcyl_bessel_kfcyl_bessel_kl(C++17)(C++17)(C++17) | irregular modified cylindrical Bessel functions   (function) |
| cyl_neumanncyl_neumannfcyl_neumannl(C++17)(C++17)(C++17) | cylindrical Neumann functions   (function) |
| ellint_1ellint_1fellint_1l(C++17)(C++17)(C++17) | (incomplete) elliptic integral of the first kind   (function) |
| ellint_2ellint_2fellint_2l(C++17)(C++17)(C++17) | (incomplete) elliptic integral of the second kind   (function) |
| ellint_3ellint_3fellint_3l(C++17)(C++17)(C++17) | (incomplete) elliptic integral of the third kind   (function) |
| expintexpintfexpintl(C++17)(C++17)(C++17) | exponential integral   (function) |
| hermitehermitefhermitel(C++17)(C++17)(C++17) | Hermite polynomials   (function) |
| legendrelegendreflegendrel(C++17)(C++17)(C++17) | Legendre polynomials   (function) |
| laguerrelaguerreflaguerrel(C++17)(C++17)(C++17) | Laguerre polynomials   (function) |
| riemann_zetariemann_zetafriemann_zetal(C++17)(C++17)(C++17) | Riemann zeta function   (function) |
| sph_besselsph_besselfsph_bessell(C++17)(C++17)(C++17) | spherical Bessel functions (of the first kind)   (function) |
| sph_legendresph_legendrefsph_legendrel(C++17)(C++17)(C++17) | spherical associated Legendre functions   (function) |
| sph_neumannsph_neumannfsph_neumannl(C++17)(C++17)(C++17) | spherical Neumann functions   (function) |

### Synopsis

For each function with at least one parameter of type /\* floating-point-type \*/, an overload for each cv-unqualified floating-point type is provided where all uses of /\* floating-point-type \*/ in the function signature are replaced with that floating-point type.

For each function with at least one parameter of type /\* floating-point-type \*/ other than `std::abs`, additional overloads are provided to ensure that, if every argument corresponding to a /\* floating-point-type \*/ parameter has arithmetic type, then every such argument is effectively cast to the floating-point type with the greatest floating-point conversion rank and greatest floating-point conversion subrank among the types of all such arguments, where arguments of integer type are considered to have the same floating-point conversion rank as double. If no such floating-point type with the greatest rank and subrank exists, then overload resolution does not result in a usable candidate from the provided overloads.

```
namespace std {
  using float_t = /* see description */;
  using double_t = /* see description */;
}
 
#define HUGE_VAL /* see description */
#define HUGE_VALF /* see description */
#define HUGE_VALL /* see description */
#define INFINITY /* see description */
#define NAN /* see description */
#define FP_INFINITE /* see description */
#define FP_NAN /* see description */
#define FP_NORMAL /* see description */
#define FP_SUBNORMAL /* see description */
#define FP_ZERO /* see description */
#define FP_FAST_FMA /* see description */
#define FP_FAST_FMAF /* see description */
#define FP_FAST_FMAL /* see description */
#define FP_ILOGB0 /* see description */
#define FP_ILOGBNAN /* see description */
#define MATH_ERRNO /* see description */
#define MATH_ERREXCEPT /* see description */
 
#define math_errhandling /* see description */
 
namespace std {
  /* floating-point-type */ acos(/* floating-point-type */ x);
  float acosf(float x);
  long double acosl(long double x);
 
  /* floating-point-type */ asin(/* floating-point-type */ x);
  float asinf(float x);
  long double asinl(long double x);
 
  /* floating-point-type */ atan(/* floating-point-type */ x);
  float atanf(float x);
  long double atanl(long double x);
 
  /* floating-point-type */ atan2(/* floating-point-type */ y,
                                  /* floating-point-type */ x);
  float atan2f(float y, float x);
  long double atan2l(long double y, long double x);
 
  /* floating-point-type */ cos(/* floating-point-type */e x);
  float cosf(float x);
  long double cosl(long double x);
 
  /* floating-point-type */ sin(/* floating-point-type */ x);
  float sinf(float x);
  long double sinl(long double x);
 
  /* floating-point-type */ tan(/* floating-point-type */ x);
  float tanf(float x);
  long double tanl(long double x);
 
  /* floating-point-type */ acosh(/* floating-point-type */ x);
  float acoshf(float x);
  long double acoshl(long double x);
 
  /* floating-point-type */ asinh(/* floating-point-type */ x);
  float asinhf(float x);
  long double asinhl(long double x);
 
  /* floating-point-type */ atanh(/* floating-point-type */ x);
  float atanhf(float x);
  long double atanhl(long double x);
 
  /* floating-point-type */ cosh(/* floating-point-type */ x);
  float coshf(float x);
  long double coshl(long double x);
 
  /* floating-point-type */ sinh(/* floating-point-type */ x);
  float sinhf(float x);
  long double sinhl(long double x);
 
  /* floating-point-type */ tanh(/* floating-point-type */ x);
  float tanhf(float x);
  long double tanhl(long double x);
 
  /* floating-point-type */ exp(/* floating-point-type */ x);
  float expf(float x);
  long double expl(long double x);
 
  /* floating-point-type */ exp2(/* floating-point-type */ x);
  float exp2f(float x);
  long double exp2l(long double x);
 
  /* floating-point-type */ expm1(/* floating-point-type */ x);
  float expm1f(float x);
  long double expm1l(long double x);
 
  constexpr /* floating-point-type */ frexp(/* floating-point-type */ value, int* exp);
  constexpr float frexpf(float value, int* exp);
  constexpr long double frexpl(long double value, int* exp);
 
  constexpr int ilogb(/* floating-point-type */ x);
  constexpr int ilogbf(float x);
  constexpr int ilogbl(long double x);
 
  constexpr /* floating-point-type */ ldexp(/* floating-point-type */ x, int exp);
  constexpr float ldexpf(float x, int exp);
  constexpr long double ldexpl(long double x, int exp);
 
  /* floating-point-type */ log(/* floating-point-type */ x);
  float logf(float x);
  long double logl(long double x);
 
  /* floating-point-type */ log10(/* floating-point-type */ x);
  float log10f(float x);
  long double log10l(long double x);
 
  /* floating-point-type */ log1p(/* floating-point-type */ x);
  float log1pf(float x);
  long double log1pl(long double x);
 
  /* floating-point-type */ log2(/* floating-point-type */ x);
  float log2f(float x);
  long double log2l(long double x);
 
  constexpr /* floating-point-type */ logb(/* floating-point-type */ x);
  constexpr float logbf(float x);
  constexpr long double logbl(long double x);
 
  constexpr /* floating-point-type */ modf(/* floating-point-type */ value,
                                           /* floating-point-type */* iptr);
  constexpr float modff(float value, float* iptr);
  constexpr long double modfl(long double value, long double* iptr);
 
  constexpr /* floating-point-type */ scalbn(/* floating-point-type */ x, int n);
  constexpr float scalbnf(float x, int n);
  constexpr long double scalbnl(long double x, int n);
 
  constexpr /* floating-point-type */ scalbln(/* floating-point-type */ x, long int n);
  constexpr float scalblnf(float x, long int n);
  constexpr long double scalblnl(long double x, long int n);
 
  /* floating-point-type */ cbrt(/* floating-point-type */ x);
  float cbrtf(float x);
  long double cbrtl(long double x);
 
  // absolute values
  constexpr int abs(int j);                     // freestanding
  constexpr long int abs(long int j);           // freestanding
  constexpr long long int abs(long long int j); // freestanding
  constexpr /* floating-point-type */
    abs(/* floating-point-type */ j);           // freestanding-deleted
 
  constexpr /* floating-point-type */ fabs(/* floating-point-type */ x);
  constexpr float fabsf(float x);
  constexpr long double fabsl(long double x);
 
  /* floating-point-type */ hypot(/* floating-point-type */ x,
                                  /* floating-point-type */ y);
  float hypotf(float x, float y);
  long double hypotl(long double x, long double y);
 
  // three-dimensional hypotenuse
  float hypot(/* floating-point-type */ x,
              /* floating-point-type */ y,
              /* floating-point-type */ z);
 
  /* floating-point-type */ pow(/* floating-point-type */ x,
                                /* floating-point-type */ y);
  float powf(float x, float y);
  long double powl(long double x, long double y);
 
  /* floating-point-type */ sqrt(/* floating-point-type */ x);
  float sqrtf(float x);
  long double sqrtl(long double x);
 
  /* floating-point-type */ erf(/* floating-point-type */ x);
  float erff(float x);
  long double erfl(long double x);
 
  /* floating-point-type */ erfc(/* floating-point-type */ x);
  float erfcf(float x);
  long double erfcl(long double x);
 
  /* floating-point-type */ lgamma(/* floating-point-type */ x);
  float lgammaf(float x);
  long double lgammal(long double x);
 
  /* floating-point-type */ tgamma(/* floating-point-type */ x);
  float tgammaf(float x);
  long double tgammal(long double x);
 
  constexpr /* floating-point-type */ ceil(/* floating-point-type */ x);
  constexpr float ceilf(float x);
  constexpr long double ceill(long double x);
 
  constexpr /* floating-point-type */ floor(/* floating-point-type */ x);
  constexpr float floorf(float x);
  constexpr long double floorl(long double x);
 
  /* floating-point-type */ nearbyint(/* floating-point-type */ x);
  float nearbyintf(float x);
  long double nearbyintl(long double x);
 
  /* floating-point-type */ rint(/* floating-point-type */ x);
  float rintf(float x);
  long double rintl(long double x);
 
  long int lrint(/* floating-point-type */ x);
  long int lrintf(float x);
  long int lrintl(long double x);
 
  long long int llrint(/* floating-point-type */ x);
  long long int llrintf(float x);
  long long int llrintl(long double x);
 
  constexpr /* floating-point-type */ round(/* floating-point-type */ x);
  constexpr float roundf(float x);
  constexpr long double roundl(long double x);
 
  constexpr long int lround(/* floating-point-type */ x);
  constexpr long int lroundf(float x);
  constexpr long int lroundl(long double x);
 
  constexpr long long int llround(/* floating-point-type */ x);
  constexpr long long int llroundf(float x);
  constexpr long long int llroundl(long double x);
 
  constexpr /* floating-point-type */ trunc(/* floating-point-type */ x);
  constexpr float truncf(float x);
  constexpr long double truncl(long double x);
 
  constexpr /* floating-point-type */ fmod(/* floating-point-type */ x,
                                           /* floating-point-type */ y);
  constexpr float fmodf(float x, float y);
  constexpr long double fmodl(long double x, long double y);
 
  constexpr /* floating-point-type */ remainder(/* floating-point-type */ x,
                                                /* floating-point-type */ y);
  constexpr float remainderf(float x, float y);
  constexpr long double remainderl(long double x, long double y);
 
  constexpr /* floating-point-type */ remquo(/* floating-point-type */ x,
                                             /* floating-point-type */ y, int* quo);
  constexpr float remquof(float x, float y, int* quo);
  constexpr long double remquol(long double x, long double y, int* quo);
 
  constexpr /* floating-point-type */ copysign(/* floating-point-type */ x,
                                               /* floating-point-type */ y);
  constexpr float copysignf(float x, float y);
  constexpr long double copysignl(long double x, long double y);
 
  double nan(const char* tagp);
  float nanf(const char* tagp);
  long double nanl(const char* tagp);
 
  constexpr /* floating-point-type */ nextafter(/* floating-point-type */ x,
                                                /* floating-point-type */ y);
  constexpr float nextafterf(float x, float y);
  constexpr long double nextafterl(long double x, long double y);
 
  constexpr /* floating-point-type */ nexttoward(/* floating-point-type */ x,
                                                 long double y);
  constexpr float nexttowardf(float x, long double y);
  constexpr long double nexttowardl(long double x, long double y);
 
  constexpr /* floating-point-type */ fdim(/* floating-point-type */ x,
                                           /* floating-point-type */ y);
  constexpr float fdimf(float x, float y);
  constexpr long double fdiml(long double x, long double y);
 
  constexpr /* floating-point-type */ fmax(/* floating-point-type */ x,
                                           /* floating-point-type */ y);
  constexpr float fmaxf(float x, float y);
  constexpr long double fmaxl(long double x, long double y);
 
  constexpr /* floating-point-type */ fmin(/* floating-point-type */ x,
                                           /* floating-point-type */ y);
  constexpr float fminf(float x, float y);
  constexpr long double fminl(long double x, long double y);
 
  constexpr /* floating-point-type */ fma(/* floating-point-type */ x,
                                          /* floating-point-type */ y,
                                          /* floating-point-type */ z);
  constexpr float fmaf(float x, float y, float z);
  constexpr long double fmal(long double x, long double y, long double z);
 
  // linear interpolation
  constexpr /* floating-point-type */ lerp(/* floating-point-type */ a,
                                           /* floating-point-type */ b,
                                           /* floating-point-type */ t) noexcept;
 
  // classification / comparison functions
  constexpr int fpclassify(/* floating-point-type */ x);
 
  constexpr bool isfinite(/* floating-point-type */ x);
 
  constexpr bool isinf(/* floating-point-type */ x);
 
  constexpr bool isnan(/* floating-point-type */ x);
 
  constexpr bool isnormal(/* floating-point-type */ x);
 
  constexpr bool signbit(/* floating-point-type */ x);
 
  constexpr bool isgreater(/* floating-point-type */ x,
                           /* floating-point-type */ y);
 
  constexpr bool isgreaterequal(/* floating-point-type */ x,
                                /* floating-point-type */ y);
 
  constexpr bool isless(/* floating-point-type */ x,
                        /* floating-point-type */ y);
 
  constexpr bool islessequal(/* floating-point-type */ x,
                             /* floating-point-type */ y);
 
  constexpr bool islessgreater(/* floating-point-type */ x,
                               /* floating-point-type */ y);
 
  constexpr bool isunordered(/* floating-point-type */ x,
                             /* floating-point-type */ y);
 
  // mathematical special functions
 
  // associated Laguerre polynomials
  /* floating-point-type */ assoc_laguerre(unsigned n, unsigned m,
                                           /* floating-point-type */ x);
  float assoc_laguerref(unsigned n, unsigned m, float x);
  long double assoc_laguerrel(unsigned n, unsigned m, long double x);
 
  // associated Legendre functions
  /* floating-point-type */ assoc_legendre(unsigned l, unsigned m,
                                           /* floating-point-type */ x);
  float assoc_legendref(unsigned l, unsigned m, float x);
  long double assoc_legendrel(unsigned l, unsigned m, long double x);
 
  // beta function
  /* floating-point-type */ beta(/* floating-point-type */ x,
                                 /* floating-point-type */ y);
  float betaf(float x, float y);
  long double betal(long double x, long double y);
 
  // complete elliptic integral of the first kind
  /* floating-point-type */ comp_ellint_1(/* floating-point-type */ k);
  float comp_ellint_1f(float k);
  long double comp_ellint_1l(long double k);
 
  // complete elliptic integral of the second kind
  /* floating-point-type */ comp_ellint_2(/* floating-point-type */ k);
  float comp_ellint_2f(float k);
  long double comp_ellint_2l(long double k);
 
  // complete elliptic integral of the third kind
  /* floating-point-type */ comp_ellint_3(/* floating-point-type */ k,
                                          /* floating-point-type */ nu);
  float comp_ellint_3f(float k, float nu);
  long double comp_ellint_3l(long double k, long double nu);
 
  // regular modified cylindrical Bessel functions
  /* floating-point-type */ cyl_bessel_i(/* floating-point-type */ nu,
                                         /* floating-point-type */ x);
  float cyl_bessel_if(float nu, float x);
  long double cyl_bessel_il(long double nu, long double x);
 
  // cylindrical Bessel functions of the first kind
  /* floating-point-type */ cyl_bessel_j(/* floating-point-type */ nu,
                                         /* floating-point-type */ x);
  float cyl_bessel_jf(float nu, float x);
  long double cyl_bessel_jl(long double nu, long double x);
 
  // irregular modified cylindrical Bessel functions
  /* floating-point-type */ cyl_bessel_k(/* floating-point-type */ nu,
                                         /* floating-point-type */ x);
  float cyl_bessel_kf(float nu, float x);
  long double cyl_bessel_kl(long double nu, long double x);
 
  // cylindrical Neumann functions;
  // cylindrical Bessel functions of the second kind
  /* floating-point-type */ cyl_neumann(/* floating-point-type */ nu,
                                        /* floating-point-type */ x);
  float cyl_neumannf(float nu, float x);
  long double cyl_neumannl(long double nu, long double x);
 
  // incomplete elliptic integral of the first kind
  /* floating-point-type */ ellint_1(/* floating-point-type */ k,
                                     /* floating-point-type */ phi);
  float ellint_1f(float k, float phi);
  long double ellint_1l(long double k, long double phi);
 
  // incomplete elliptic integral of the second kind
  /* floating-point-type */ ellint_2(/* floating-point-type */ k,
                                     /* floating-point-type */ phi);
  float ellint_2f(float k, float phi);
  long double ellint_2l(long double k, long double phi);
 
  // incomplete elliptic integral of the third kind
  /* floating-point-type */ ellint_3(/* floating-point-type */ k,
                                     /* floating-point-type */ nu,
                                     /* floating-point-type */ phi);
  float ellint_3f(float k, float nu, float phi);
  long double ellint_3l(long double k, long double nu, long double phi);
 
  // exponential integral
  /* floating-point-type */ expint(/* floating-point-type */ x);
  float expintf(float x);
  long double expintl(long double x);
 
  // Hermite polynomials
  /* floating-point-type */ hermite(unsigned n, /* floating-point-type */ x);
  float hermitef(unsigned n, float x);
  long double hermitel(unsigned n, long double x);
 
  // Laguerre polynomials
  /* floating-point-type */ laguerre(unsigned n, /* floating-point-type */ x);
  float laguerref(unsigned n, float x);
  long double laguerrel(unsigned n, long double x);
 
  // Legendre polynomials
  /* floating-point-type */ legendre(unsigned l, /* floating-point-type */ x);
  float legendref(unsigned l, float x);
  long double legendrel(unsigned l, long double x);
 
  // Riemann zeta function
  /* floating-point-type */ riemann_zeta(/* floating-point-type */ x);
  float riemann_zetaf(float x);
  long double riemann_zetal(long double x);
 
  // spherical Bessel functions of the first kind
  /* floating-point-type */ sph_bessel(unsigned n, /* floating-point-type */ x);
  float sph_besself(unsigned n, float x);
  long double sph_bessell(unsigned n, long double x);
 
  // spherical associated Legendre functions
  /* floating-point-type */ sph_legendre(unsigned l, unsigned m,
                                         /* floating-point-type */ theta);
  float sph_legendref(unsigned l, unsigned m, float theta);
  long double  sph_legendrel(unsigned l, unsigned m, long double theta);
 
  // spherical Neumann functions;
  // spherical Bessel functions of the second kind
  /* floating-point-type */ sph_neumann(unsigned n, /* floating-point-type */ x);
  float sph_neumannf(unsigned n, float x);
  long double sph_neumannl(unsigned n, long double x);
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/cmath&oldid=166000>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 December 2023, at 06:52.