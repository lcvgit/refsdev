# ISO/IEC 14882:2011

## Language Features

- [N1653] C99 preprocessor
- [N1720] `static_assert`
- [N1757] Right angle brackets
- [N1791] Extended friend declarations
- [N1811] `long long`
- [N1984] `auto`
- [N1986] Delegating constructors
- [N1987] `extern template`
- [N2235] `constexpr`
- [N2249] `char16_t` and `char32_t`
- [N2255, N2518, N2984, N3142] Compiler support for type traits
- [N2258] Template aliases
- [N2341] `alignas`
- [N2341] `alignof`
- [N2346] Defaulted and deleted functions
- [N2347] Strongly-typed `enum`
- [N2427] Atomic operations
- [N2431] `nullptr`
- [N2437] Explicit conversion operators
- [N2439] ref-qualifiers
- [N2442] Unicode string literals
- [N2442] Raw string literals
- [N2535] Inline namespaces
- [N2540] Inheriting constructors
- [N2541] Trailing function return types
- [N2544] Unrestricted unions
- [N2242, N2555] Variadic templates
- [N2634] Expression SFINAE
- [N2657] Local and unnamed types as template parameters
- [N2659] Thread-local storage
- [N2660] Dynamic initialization and destruction with concurrency (magic statics)
- [N2670] Garbage Collection and Reachability-Based Leak Detection
- [N2672] Initializer lists
- [N2756] Non-static data member initializers
- [N2761] Attributes
- [N2764] Forward (opaque) `enum` declarations
- [N2765] User-defined literals
- [N2118, N2844, CWG1138] Rvalue references
- [N2550, N2658, N2927] Lambda expressions
- [N2930, N3271] Range-for loop
- [N3050] `noexcept`
- [N3053] Defaulted move special member functions
- [N2928, N3206 N3272] override and final
- [N2343, N3276] `decltype`

## Library Features

- [N1429] Regular expressions library
- [N1836, N2240, N2244, N2255, N2342, N2984, N3142] Type traits
- [N1913, LWG1192] Member functions `cbegin`, `cend`, `crbegin`, and `crend` of containers
- [N2670] Garbage Collection and Reachability-Based Leak Detection (library support)
- [N2071, N2072] Money, Time, and hexfloat I/O manipulators
- [N2668] Disallowing COW (copy-on-write) `std::basic_string`

## References

- <https://en.cppreference.com/w/cpp/11>{:target="_blank"}
- <https://gcc.gnu.org/projects/cxx-status.html#cxx11>{:target="_blank"}
- <https://gcc.gnu.org/onlinedocs/libstdc++/manual/status.html>{:target="_blank}
- <https://clang.llvm.org/cxx_status.html>{:target="_blank"}
- <https://www.edg.com/features.html>{:target="_blank"}

<!---
GCC

- [N2118]	Rvalue references
  - [N2439]	Rvalue references for `*this`
- [N1610]	Initialization of class objects by rvalues
- [N2756]	Non-static data member initializers
- [N2242]	Variadic templates
  - [N2555]	Extending variadic template template parameters
- [N2672]	Initializer lists
- [N1720]	Static assertions
- [N1984]	auto-typed variables
  - [N1737]	Multi-declarator auto
  - [N2546]	Removal of auto as a storage-class specifier
  - [N2541]	New function declarator syntax
- [N2927]	New wording for C++0x lambdas
- [N2343]	Declared type of an expression
  - [N3276]	decltype and call expressions
- [N1757]	Right angle brackets
- [DR226]	Default template arguments for function templates
- [DR339]	Solving the SFINAE problem for expressions
- [N2258]	Template aliases
- [N1987]	Extern templates
- [N2431]	Null pointer constant
- [N2347]	Strongly-typed enums
  - [N2764] Forward declarations for enums
- [N2761]	Generalized attributes
- [N2235]	Generalized constant expressions
- [N2341]	Alignment support
- [N1986]	Delegating constructors
- [N2540]	Inheriting constructors
- [N2437]	Explicit conversion operators
- [N2249]	New character types
- [N2442]	Unicode string literals
- [N2442]	Raw string literals
- [N2170]	Universal character name literals
- [N2765]	User-defined literals
- [N2342]	Standard Layout Types
- [N2346]	Defaulted and deleted functions
- [N1791]	Extended friend declarations
- [N2253]	Extending sizeof
- [N2535]	Inline namespaces
- [N2544]	Unrestricted unions
- [N2657]	Local and unnamed types as template arguments
- [N2930]	Range-based for
- [N2928, N3206, N3272]	Explicit virtual overrides
- [N2670]	Minimal support for garbage collection and reachability-based leak detection
- [N3050]	Allowing move constructors to throw [noexcept]
- [N3053]	Defining move special member functions
- [N2239]	Sequence points
- [N2427]	Atomic operations
- [N2748]	Strong Compare and Exchange
- [N2752]	Bidirectional Fences
- [N2429]	Memory model
- [N2664]	Data-dependency ordering: atomics and memory model
- [N2179]	Propagating exceptions
- [N2440]	Abandoning a process and at_quick_exit
- [N2547]	Allow atomics use in signal handlers
- [N2659]	Thread-local storage
- [N2660]	Dynamic initialization and destruction with concurrency
- [N2340]	__func__ predefined identifier
- [N1653]	C99 preprocessor
- [N1811]	long long
- [N1988]	Extended integral types

Clang
N2118	Rvalue references
P1825R0 (DR)	
N2439	    Rvalue references for *this
N1610	Initialization of class objects by rvalues
N2756	Non-static data member initializers
N2242	Variadic templates
N2555	    Extending variadic template template parameters
N2672	Initializer lists
P1009R2 (DR)	
P1957R2 (DR)	
N1720	Static assertions
N1984	auto-typed variables
N1737	    Multi-declarator auto
N2546	    Removal of auto as a storage-class specifier
N2541	    New function declarator syntax
N2927	Lambda expressions
P0588R1 (DR)	
N2343	Declared type of an expression
N3276	    Incomplete return types
N1757	Right angle brackets
DR226	Default template arguments for function templates
DR339	Solving the SFINAE problem for expressions
N2258	Alias templates
N1987	Extern templates
N2431	Null pointer constant
N2347	Strongly-typed enums
N2764  DR1206	Forward declarations for enums
N2761	Standardized attribute syntax
N2235	Generalized constant expressions
P0859R0 (DR)	
N2341	Alignment support
N1627	Conditionally-support behavior
N1727	Changing undefined behavior into diagnosable errors
N1986	Delegating constructors
N2540	Inheriting constructors
P0136R1 (DR)	
N2437	Explicit conversion operators
N2249	New character types
N2442	Unicode string literals
N2442	Raw string literals
N2170	Universal character names in literals
N2765	User-defined literals
N2342	Standard Layout Types
N2346	Defaulted functions
P1286R2 (DR)	
N2346	Deleted functions
N1791	Extended friend declarations
N2253  DR850	Extending sizeof
N2535	Inline namespaces
N2544	Unrestricted unions
N2657	Local and unnamed types as template arguments
N2930	Range-based for
P0962R1 (DR)	
N2928  N3206  N3272	Explicit virtual overrides
N2670	Minimal support for garbage collection and reachability-based leak detection
N3050	Allowing move constructors to throw [noexcept]
N3053	Defining move special member functions
N2239	Sequence points
N2427	Atomic operations
N2748	Strong Compare and Exchange
N2752	Bidirectional Fences
N2429	Memory model
N2664	Data-dependency ordering: atomics and memory model
N2179	Propagating exceptions
N2547	Allow atomics use in signal handlers
N2659	Thread-local storage
N2660	Dynamic initialization and destruction with concurrency
N2340	__func__ predefined identifier
N1653	C99 preprocessor
N1811	long long
N1988	Extended integral types

EDG

- [N1988] Extended integral types
- [N2239] Sequence points
- [N2547] Atomics use in signal handlers
- [N2664] Data dependency ordering
- [N2670] Support for garbage collection
- [N2660] Dynamic initialization and destruction
- [N2752] Bidirectional fences
- [N2340] __func__
- [N2343] decltype
- [N1791] Extended friend
- [N1811] long long
- [N1653] C99 preprocessing vararg macros
- [N1653] C99 preprocessing empty macro arguments
- [N1653] C99 preprocessing concatenation of narrow/wide strings
- [N1757] >>
- [N1720] static_assert
- [N1987] extern template
- [N1984] auto
- [N2347] Strong enums
- [N2170] UCN changes
- [N1653] C99 preprocessing __STDC_HOSTED__
- [N1653] C99 preprocessing _Pragma in C++
- [N2118] Rvalue references
- [N2253] sizeof on nonstatic data members
- [N2346] Defaulted/deleted functions
- [N2546] Removal of auto as a storage-class specifier
- [N2550] Lambda expressions
- [N2658] Constness of lambda functions
- [N2258] Template aliases
- [N2431] nullptr
- [N2541] Trailing return types (with "auto")
- [N2656] Conversions to/from nullptr_t
- [N2657] Local/unnamed types as template parameters
- [N2634] SFINAE for expressions
- [N2761] Standard attributes
- [N2782] [[carries_dependency]] attribute
- [N2928] Attributes for checking hiding and overriding
- [N3065] Removal of export
- [N2242] Variadic templates
- [N2555] Extending variadic template template parameters
- [N2933] Parameter pack expansion in attributes
- [N2342] POD's Revisited; Resolving Core Issue 568
- [N2249] New char types
- [N2437] explicit conversion functions; boolean-conversion
- [N3282] Use of "this" in trailing-return-types
- [N2535] Namespace association ("inline namespace")
- [N2672] Initializer lists
- [N2778] Range-based for loops
- [N2930] Non-concept range-based for loops
- [N3052] Converting lambdas to function pointers
- [N3053] Implicit move constructors and assignment operators
- [N3050] "noexcept" specifier and operator
- [N3217] Brace-initializers as default arguments
- [N2764] Opaque enumeration definitions
- [N2544] Unrestricted unions
- [N3051] Deprecation of exception specifications
- [N2235] Generalized constant expressions
- [N2756] Non-static data member initializers
- [N3078] Constexpr functions with reference parameters
- [N3268] Declarations and braced-init-list returns in constexpr functions
- [N3277] Constexpr references
- [N1986] Delegating constructors
- [N2442] UTF-8 and raw string literals
- [N2439] Reference qualifier on member functions
- [N2984] Support for additional type traits
- [N3077] Alternative approach to raw string issues
- [N2341] Alignment (alignof/alignas)
- [N2765] User-defined literals
- [core issue 693] Deprecated conversion of string to pointer to non-const becomes error
- [N3055] Value categories
- [N3190] C-compatible alignment specifications
- [N3206] Context-sensitive keywords for overriding/hiding
- [N3272] Removal of hiding and "explicit" features in override control
- [N3276] Incomplete types in decltype function calls
- [N2540] Inheriting constructors
- [N2659] Thread-local storage
- [N3049] Additional decltype(...) uses
--->