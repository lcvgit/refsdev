# ISO/IEC 14882:2011

## Language Features

- [N3323] Tweaked wording for contextual conversions
- [N3472] Binary literals
- [N3638] `decltype(auto)`, Return type deduction for normal functions
- [N3648] Initialized/Generalized lambda captures (init-capture)
- [N3649] Generic `lambda` expressions
- [N3651] Variable templates
- [N3652] Extended `constexpr`
- [N3653] Aggregates with default member initializers
- [N3664] Omitting/extending memory allocations
- [N3760] `[[deprecated]]` attribute
- [N3778] Sized deallocation
- [N3781] Single quote as digit separator

## Library Features

- [N3302] `constexpr` for `<complex>`
- [N3421] Transparent operator functors
- [N3462] `std::result_of` and SFINAE
- [N3469] `constexpr` for `<chrono>`
- [N3470] `constexpr` for `<array>`
- [N3471] `constexpr` for `<initializer_list>`, `<utility>` and `<tuple>`
- [N3545] Improved std::integral_constant
- [N3642] User-defined literals for `<chrono>` and `<string>`
- [N3644] Null forward iterators
- [N3654] `std::quoted`
- [N3656] `std::make_unique`
- [N3657] Heterogeneous associative lookup
- [N3658] `std::integer_sequence`
- [N3659] `std::shared_timed_mutex`
- [N3668] `std::exchange`
- [N3669] fixing `constexpr` member functions without `const`
- [N3670] `std::get<T>()`
- [N3671] Dual-Range std::equal, std::is_permutation, std::mismatch

<!--
GCC

-[N3323] Tweak to certain C++ contextual conversions	
-[N3472] Binary literals
    - `__cpp_binary_literals >= 201304`
-[N3638] Return type deduction for normal functions
    - `__cpp_decltype_auto >= 201304`
-[N3648] Generalized lambda capture (init-capture)
    - `__cpp_init_captures >= 201304`
-[N3649] Generic (polymorphic) lambda expressions
    - `__cpp_generic_lambdas >= 201304`
-[N3651] Variable templates
    - `__cpp_variable_templates >= 201304`
-[N3652] Relaxing requirements on constexpr functions
    - `__cpp_constexpr >= 201304`
-[N3653] Member initializers and aggregates
    - `__cpp_aggregate_nsdmi >= 201304`
-[N3664] Clarifying memory allocation
-[N3778] Sized deallocation
    - `__cpp_sized_deallocation >= 201309`
-[N3760] [[deprecated]] attribute
    - `__has_cpp_attribute(deprecated) >= 201309`
-[N3781] Single-quotation-mark as a digit separator
    - `__cpp_digit_separator >= 201309`

- [N3639] Runtime-sized arrays with automatic storage duration  (Removed from the standard)
    - `__cpp_runtime_arrays >= 198712`

Clang

- [N3323] Tweak to certain C++ contextual conversions
- [N3472] Binary literals
- [N3638] decltype(auto)
- [N3638] Return type deduction for normal functions
- [N3648] Initialized lambda captures
- [N3649] Generic lambdas
- [N3651] Variable templates
- [N3652] Relaxing requirements on constexpr functions
- [N3653] Member initializers and aggregates
- [N3664] Clarifying memory allocation
- [N3760] [[deprecated]] attribute
- [N3781] Single quotation mark as digit separator
- [N3778] C++ Sized Deallocation

EDG

- [N3323] Revision to contextual conversions
- [N3472] Binary literals
- [N3638] Return type deduction (and decltype(auto))
- [N3648] Generalized lambda capture
- [N3653] Member initializers and aggregates
- [N3652] Generalized constexpr and constexpr member functions and implicit const
- [N3664] Clarifying Memory Allocation (merged allocation)
- [N3651] Variable templates
- [N3649] Generic Lambdas
- [N3760] Deprecated attribute
- [N3778] Sized deallocation
- [N3781] Accept single quote as digit separator

-->