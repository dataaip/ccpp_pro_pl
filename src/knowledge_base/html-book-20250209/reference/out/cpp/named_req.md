# Named Requirements

From cppreference.com
< cpp
C++

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Freestanding and hosted | | | | |
| Language | | | | |
| Standard library | | | | |
| Standard library headers | | | | |
| ****Named requirements**** | | | | |
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

****C++ named requirements****

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Basic | | | | | | DefaultConstructible | | | | | | MoveConstructible(C++11) | | | | | | CopyConstructible | | | | | | CopyAssignable | | | | | | MoveAssignable(C++11) | | | | | | Destructible | | | | | | Type properties | | | | | | ScalarType | | | | | | PODType | | | | | | TriviallyCopyable(C++11) | | | | | | TrivialType(C++11) | | | | | | StandardLayoutType(C++11) | | | | | | ImplicitLifetimeType | | | | | | Library-wide | | | | | | BooleanTestable | | | | | | EqualityComparable | | | | | | LessThanComparable | | | | | | Swappable | | | | | | ValueSwappable(C++11) | | | | | | NullablePointer(C++11) | | | | | | Hash(C++11) | | | | | | Allocator | | | | | | FunctionObject | | | | | | Callable | | | | | | Predicate | | | | | | BinaryPredicate | | | | | | Compare | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Container | | | | | | Container | | | | | | ReversibleContainer | | | | | | AllocatorAwareContainer | | | | | | SequenceContainer | | | | | | ContiguousContainer(C++17) | | | | | | AssociativeContainer | | | | | | UnorderedAssociativeContainer(C++11) | | | | | | Container element | | | | | | DefaultInsertable(C++11) | | | | | | CopyInsertable(C++11) | | | | | | MoveInsertable(C++11) | | | | | | EmplaceConstructible(C++11) | | | | | | Erasable(C++11) | | | | | | Iterator | | | | | | LegacyIterator | | | | | | LegacyInputIterator | | | | | | LegacyOutputIterator | | | | | | LegacyForwardIterator | | | | | | LegacyBidirectionalIterator | | | | | | LegacyRandomAccessIterator | | | | | | LegacyContiguousIterator(C++17) | | | | | | ConstexprIterator(C++20) | | | | | | Stream I/O | | | | | | FormattedInputFunction | | | | | | UnformattedInputFunction | | | | | | FormattedOutputFunction | | | | | | UnformattedOutputFunction | | | | | | Formatters | | | | | | BasicFormatter(C++20) | | | | | | Formatter(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random Numbers | | | | | | SeedSequence(C++11) | | | | | | RandomNumberEngine(C++11) | | | | | | RandomNumberDistribution(C++11) | | | | | | UniformRandomBitGenerator(C++11) | | | | | | RandomNumberEngineAdaptor(C++11) | | | | | | Concurrency | | | | | | BasicLockable(C++11) | | | | | | Lockable(C++11) | | | | | | TimedLockable(C++11) | | | | | | SharedLockable(C++14) | | | | | | SharedTimedLockable(C++14) | | | | | | Mutex(C++11) | | | | | | TimedMutex(C++11) | | | | | | SharedMutex(C++17) | | | | | | SharedTimedMutex(C++14) | | | | | | Ranges | | | | | | RangeAdaptorObject(C++20) | | | | | | RangeAdaptorClosureObject(C++20) | | | | | | Multidimensional View | | | | | | LayoutMapping(C++23) | | | | | | LayoutMappingPolicy(C++23) | | | | | | AccessorPolicy(C++23) | | | | | | Other | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | CharTraits | | | | | | RegexTraits(C++11) | | | | | | BitmaskType | | | | | | LiteralType(C++11) | | | | | | NumericType | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | UnaryTypeTrait(C++11) | | | | | | BinaryTypeTrait(C++11) | | | | | | TransformationTrait(C++11) | | | | | | Clock(C++11) | | | | | | TrivialClock(C++11) | | | | | | |  | | | | | |

The **named requirements** listed on this page are the named requirements used in the normative text of the C++ standard to define the expectations of the standard library.

The burden to ensure that library templates are instantiated with template arguments that satisfy these requirements is on the programmer. Failure to do so may result in very complex compiler diagnostics.

Some of these requirements are formalized in C++20 using the concepts language feature.

|  |  |
| --- | --- |
| Basic | |
| DefaultConstructible | specifies that an object of the type can be default constructed (named requirement) |
| MoveConstructible(C++11) | specifies that an object of the type can be constructed from rvalue (named requirement) |
| CopyConstructible | specifies that an object of the type can be constructed from lvalue (named requirement) |
| MoveAssignable(C++11) | specifies that an object of the type can be assigned from rvalue (named requirement) |
| CopyAssignable | specifies that an object of the type can be assigned from lvalue (named requirement) |
| Destructible | specifies that an object of the type can be destroyed (named requirement) |
| Type properties | |
| Note: the standard does not define named requirements with names specified in this subcategory.  These are type categories defined by the core language. They are included here as named requirements only for consistency. | |
| ScalarType | object types that are not array types or class types (named requirement) |
| PODType(deprecated in C++20) | POD (Plain Old Data) types, compatible with C struct (named requirement) |
| TriviallyCopyable(C++11) | objects of these types can maintain their values after copying their underlying bytes (named requirement) |
| TrivialType(C++11)(deprecated in C++26) | objects of these types can be trivially constructed and copied (named requirement) |
| StandardLayoutType(C++11) | these types are useful for communicating with code written in other programming languages (named requirement) |
| ImplicitLifetimeType | objects of these types can be implicitly created, and their lifetimes can be implicitly started (named requirement) |
| Library-wide | |
| BooleanTestable | boolean operations (operator&&, operator||, and operator!) have usual semantics (named requirement) |
| EqualityComparable | `operator==` is an equivalence relation (named requirement) |
| LessThanComparable | `operator<` is a strict weak ordering relation (named requirement) |
| Swappable | can be swapped with an unqualified non-member function call swap() (named requirement) |
| ValueSwappable(C++11) | a LegacyIterator that dereferences to a Swappable type (named requirement) |
| NullablePointer(C++11) | a pointer-like type supporting a null value (named requirement) |
| Hash(C++11) | a FunctionObject that for inputs with different values has a low probability of giving the same output (named requirement) |
| Allocator | a class type that contains allocation information (named requirement) |
| FunctionObject | an object that can be called with the function call syntax (named requirement) |
| Callable | a type for which the invoke operation is defined (named requirement) |
| Predicate | a FunctionObject that returns a value convertible to bool for one argument without modifying it (named requirement) |
| BinaryPredicate | a FunctionObject that returns a value convertible to bool for two arguments without modifying them (named requirement) |
| Compare | a BinaryPredicate that establishes an ordering relation (named requirement) |

|  |  |
| --- | --- |
| Container | |
| Container | data structure that allows element access using iterators (named requirement) |
| ReversibleContainer | container using bidirectional iterators (named requirement) |
| AllocatorAwareContainer(C++11) | container using an allocator (named requirement) |
| SequenceContainer | container with elements stored linearly (named requirement) |
| ContiguousContainer(C++17) | container with elements stored at adjacent memory addresses (named requirement) |
| AssociativeContainer | container that stores elements by associating them to keys (named requirement) |
| UnorderedAssociativeContainer(C++11) | container that stores elements stored in buckets by associating them to keys (named requirement) |
| Container element | |
| DefaultInsertable(C++11) | element can be default-constructed in uninitialized storage (named requirement) |
| CopyInsertable(C++11) | element can be copy-constructed in uninitialized storage (named requirement) |
| MoveInsertable(C++11) | element can be move-constructed in uninitialized storage (named requirement) |
| EmplaceConstructible(C++11) | element can be constructed in uninitialized storage (named requirement) |
| Erasable(C++11) | element can be destroyed using an allocator (named requirement) |
| Iterator | |
| LegacyIterator | general concept to access data within some data structure (named requirement) |
| LegacyInputIterator | iterator that can be used to read data (named requirement) |
| LegacyOutputIterator | iterator that can be used to write data (named requirement) |
| LegacyForwardIterator | iterator that can be used to read data multiple times (named requirement) |
| LegacyBidirectionalIterator | iterator that can be both incremented and decremented (named requirement) |
| LegacyRandomAccessIterator | iterator that can be advanced in constant time (named requirement) |
| LegacyContiguousIterator(C++17) | iterator to contiguously-allocated elements (named requirement) |
| ConstexprIterator(C++20) | iterator that can be used during constant expression evaluation (named requirement) |
| Stream I/O functions | |
| UnformattedInputFunction | a stream input function that does not skip leading whitespace and counts the processed characters (named requirement) |
| FormattedInputFunction | a stream input function that skips leading whitespace (named requirement) |
| UnformattedOutputFunction | a basic stream output function (named requirement) |
| FormattedOutputFunction | a stream output function that sets failbit on errors and returns a reference to the stream (named requirement) |
| Formatters | |
| BasicFormatter(C++20) | abstracts formatting operations for a given formatting argument type and character type (named requirement) |
| Formatter(C++20) | defines functions used by the formatting library (named requirement) |
| Random Number Generation | |
| SeedSequence(C++11) | consumes a sequence of integers and produces a sequence of 32-bit unsigned values (named requirement) |
| UniformRandomBitGenerator(C++11) | returns uniformly distributed random unsigned integers (named requirement) |
| RandomNumberEngine(C++11) | a deterministic UniformRandomBitGenerator, defined by the seed (named requirement) |
| RandomNumberEngineAdaptor(C++11) | a RandomNumberEngine that transforms the output of another RandomNumberEngine (named requirement) |
| RandomNumberDistribution(C++11) | returns random numbers distributed according to a given mathematical probability density function (named requirement) |
| Concurrency | |
| BasicLockable(C++11) | provides exclusive ownership semantics for execution agents (i.e. threads) (named requirement) |
| Lockable(C++11) | a BasicLockable that supports attempted lock acquisition (named requirement) |
| TimedLockable(C++11) | a Lockable that supports timed lock acquisition (named requirement) |
| SharedLockable(C++14) | provides shared ownership semantics for execution agents (i.e. threads) (named requirement) |
| SharedTimedLockable(C++14) | a SharedLockable that supports timed lock acquisition (named requirement) |
| Mutex(C++11) | a Lockable that protects against data races and sequentially consistent synchronization (named requirement) |
| TimedMutex(C++11) | a TimedLockable that protects against data races and sequentially consistent synchronization (named requirement) |
| SharedMutex(C++17) | a Mutex that supports shared ownership semantics (named requirement) |
| SharedTimedMutex(C++14) | a TimedMutex that supports shared ownership semantics (named requirement) |
| Ranges | |
| RangeAdaptorObject(C++20) | a FunctionObject that creates a range adaptor from a `viewable_range` and additional arguments (named requirement) |
| RangeAdaptorClosureObject(C++20) | a FunctionObject that supports the pipe operator (named requirement) |
| Multidimensional View Customization | |
| LayoutMapping(C++23) | controls the mapping of multidimensional index in mdspan (named requirement) |
| LayoutMappingPolicy(C++23) | a policy that holds LayoutMapping requirements (named requirement) |
| AccessorPolicy(C++23) | a policy that controls access to data handle in mdspan (named requirement) |
| Other | |
| UnaryTypeTrait(C++11) | describes a property of a type (named requirement) |
| BinaryTypeTrait(C++11) | describes a relationship between two types (named requirement) |
| TransformationTrait(C++11) | modifies a property of a type (named requirement) |
| Clock(C++11) | aggregates a duration, a time point, and a function to get the current time point (named requirement) |
| TrivialClock(C++11) | a Clock that does not throw exceptions (named requirement) |
| CharTraits | defines types and functions for a character type (named requirement) |
| BitmaskType | bitset, integer, or enumeration (named requirement) |
| NumericType | a type for which initialization is effectively equal to assignment (named requirement) |
| RegexTraits(C++11) | defines types and functions used by the regular expressions library (named requirement) |
| LiteralType(C++11) | a type with constexpr constructor (named requirement) |

|  |  |
| --- | --- |
|  | This section is incomplete Reason: Any other missing requirement? |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/named_req&oldid=178049>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 November 2024, at 21:46.