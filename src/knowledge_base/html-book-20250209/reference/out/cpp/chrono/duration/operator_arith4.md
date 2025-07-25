# operator+,-,\*,/,%(std::chrono::duration)

From cppreference.com
< cpp‎ | chrono‎ | duration
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

Date and time library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Time point | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | time_point(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clock_time_conversion(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clock_cast(C++20) | | | | | |
| Duration | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration(C++11) | | | | | |
| Clocks | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | system_clock(C++11) | | | | | | steady_clock(C++11) | | | | | | is_clock(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | utc_clock(C++20) | | | | | | tai_clock(C++20) | | | | | | high_resolution_clock(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | gps_clock(C++20) | | | | | | file_clock(C++20) | | | | | | local_t(C++20) | | | | | |
| Time of day | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_amis_pm(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | make12make24(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hh_mm_ss(C++20) | | | | | |  | | | | | |
| Calendar | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

std::chrono::duration

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration::duration | | | | | | duration::operator= | | | | | | duration::count | | | | | | duration::zero | | | | | | duration::min | | | | | | duration::max | | | | | | duration::operator+duration::operator- | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration::operator++duration::operator-- | | | | | | duration::operator+=duration::operator-=duration::operator\*=duration::operator/=duration::operator%= | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****operator+operator-operator\*operator/operator%**** | | | | | | operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(C++20) | | | | | | operator<<(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration_cast | | | | | | floor(C++17) | | | | | | ceil(C++17) | | | | | | round(C++17) | | | | | | abs(C++17) | | | | | | operator""h(C++14) | | | | | | operator""min(C++14) | | | | | | operator""s(C++14) | | | | | | operator""ms(C++14) | | | | | | operator""us(C++14) | | | | | | operator""ns(C++14) | | | | | | from_stream(C++20) | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_type | | | | | | treat_as_floating_point | | | | | | duration_values | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | formatter<std::chrono::duration>(C++20) | | | | | | hash<std::chrono::duration>(C++26) | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| template< class Rep1, class Period1, class Rep2, class Period2 >  typename std::common_type<duration<Rep1,Period1>, duration<Rep2,Period2>>::type      constexpr operator+( const duration<Rep1,Period1>& lhs, const duration<Rep2,Period2>& rhs ); | (1) | (since C++11) |
| template< class Rep1, class Period1, class Rep2, class Period2 >  typename std::common_type<duration<Rep1,Period1>, duration<Rep2,Period2>>::type      constexpr operator-( const duration<Rep1,Period1>& lhs, const duration<Rep2,Period2>& rhs ); | (2) | (since C++11) |
| template< class Rep1, class Period, class Rep2 >  duration<typename std::common_type<Rep1,Rep2>::type, Period>      constexpr operator\*( const duration<Rep1,Period>& d, const Rep2& s ); | (3) | (since C++11) |
| template< class Rep1, class Rep2, class Period >  duration<typename std::common_type<Rep1,Rep2>::type, Period>      constexpr operator\*( const Rep1& s, const duration<Rep2,Period>& d ); | (4) | (since C++11) |
| template< class Rep1, class Period, class Rep2 >  duration<typename std::common_type<Rep1,Rep2>::type, Period>      constexpr operator/( const duration<Rep1,Period>& d, const Rep2& s ); | (5) | (since C++11) |
| template< class Rep1, class Period1, class Rep2, class Period2 >  typename std::common_type<Rep1,Rep2>::type      constexpr operator/( const duration<Rep1,Period1>& lhs, const duration<Rep2,Period2>& rhs ); | (6) | (since C++11) |
| template< class Rep1, class Period, class Rep2 >  duration<typename std::common_type<Rep1,Rep2>::type, Period>      constexpr operator%( const duration<Rep1, Period>& d, const Rep2& s ); | (7) | (since C++11) |
| template< class Rep1, class Period1, class Rep2, class Period2 >  typename std::common_type<duration<Rep1,Period1>, duration<Rep2,Period2>>::type      constexpr operator%( const duration<Rep1,Period1>& lhs, const duration<Rep2,Period2>& rhs ); | (8) | (since C++11) |
|  |  |  |

Performs basic arithmetic operations between two durations or between a duration and a tick count.

1) Converts the two durations to their common type and creates a duration whose tick count is the sum of the tick counts after conversion.2) Converts the two durations to their common type and creates a duration whose tick count is the rhs number of ticks subtracted from the lhs number of ticks after conversion.3,4) Converts the duration d to one whose `rep` is the common type between `Rep1` and `Rep2`, and multiples the number of ticks after conversion by s.
These overloads participate in overload resolution only if s is convertible to typename std::common_type<Rep1, Rep2>::type.5) Converts the duration d to one whose `rep` is the common type between `Rep1` and `Rep2`, and divides the number of ticks after conversion by s. This overload participates in overload resolution only if s is convertible to typename std::common_type<Rep1, Rep2>::type and `Rep2` is not a specialization of `duration`.6) Converts the two durations to their common type and divides the tick count of lhs after conversion by the tick count of rhs after conversion. Note that the return value of this operator is not a duration.7) Converts the duration d to one whose `rep` is the common type between `Rep1` and `Rep2`, and creates a duration whose tick count is the remainder of the division of the tick count, after conversion, by s. This overload participates in overload resolution only if s is convertible to typename std::common_type<Rep1, Rep2>::type and `Rep2` is not a specialization of `duration`.8) Converts the two durations to their common type and creates a duration whose tick count is the remainder of the tick counts after conversion.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs | - | duration on the left-hand side of the operator |
| rhs | - | duration on the right-hand side of the operator |
| d | - | the duration argument for mixed-argument operators |
| s | - | non-duration argument for mixed-argument operators |

### Return value

Assuming that CD is the function return type and CD<A, B> = std::common_type<A, B>::type, then:

1) CD(CD(lhs).count() + CD(rhs).count())2) CD(CD(lhs).count() - CD(rhs).count())3,4) CD(CD(d).count() \* s)5) CD(CD(d).count() / s)6) CD(lhs).count() / CD(rhs).count() (the return type of this operator is not a duration)7) CD(CD(d).count() % s)8) CD(CD(lhs).count() % CD(rhs).count())

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
int main()
{
    // Simple arithmetic:
    std::chrono::seconds s = std::chrono::hours(1)
                           + 2 * std::chrono::minutes(10)
                           + std::chrono::seconds(70) / 10;
    std::cout << "1 hour + 2*10 min + 70/10 sec = " << s << " (seconds)\n";
 
    using namespace std::chrono_literals;
 
    // Difference between dividing a duration by a number
    // and dividing a duration by another duration:
    std::cout << "Dividing that by 2 minutes gives "
              << s / 2min << '\n'
              << "Dividing that by 2 gives "
              << (s / 2).count() << " seconds\n";
 
    // The remainder operator is useful in determining where
    // in a time frame is this particular duration, e.g. to
    // break it down into hours, minutes, and seconds:
    std::cout << s << " (seconds) = "
              << std::chrono::duration_cast<std::chrono::hours>(
                 s) << " (hour) + "
              << std::chrono::duration_cast<std::chrono::minutes>(
                 s % 1h) << " (minutes) + "
              << std::chrono::duration_cast<std::chrono::seconds>(
                 s % 1min) << " (seconds)\n";
 
    constexpr auto sun_earth_distance{150'000'000ULL}; // km
    constexpr auto speed_of_light{300000ULL}; // km/sec
    std::chrono::seconds t(sun_earth_distance / speed_of_light); // sec
    std::cout << "A photon flies from the Sun to the Earth in "
              << t / 1min << " minutes " << t % 1min << " (seconds)\n";
}

```

Output:

```
1 hour + 2*10 min + 70/10 sec = 4807s (seconds)
Dividing that by 2 minutes gives 40
Dividing that by 2 gives 2403 seconds
4807s (seconds) = 1h (hour) + 20min (minutes) + 7s (seconds)
A photon flies from the Sun to the Earth in 8 minutes 20s (seconds)

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3050 | C++11 | convertibility constraint used non-const xvalue | use const lvalues instead |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/duration/operator_arith4&oldid=161874>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 November 2023, at 16:30.