# ISO/IEC 14882:2017

- [N3922] DR11: New `auto` rules for direct-list-initialization
- [N3928] `static_assert` with no message
- [N4051] `typename` in a template template parameter
- [N4086] Removing trigraphs
- [N4230] Nested `namespace` definition
- [N4266] Attributes for namespaces and enumerators
- [N4267] u8 character literals
- [N4268] Allow constant evaluation for all non-type template arguments
- [N4295] Fold Expressions
- [P0036R0] Unary fold expressions and empty parameter packs
- [P0001R1] Remove Deprecated Use of the `register` Keyword
- [P0002R1] Remove Deprecated `operator++(bool)`
- [P0012R1] Make exception specifications part of the type system
- [P0017R1] Aggregate classes with base classes
- [P0061R1] `__has_include` in preprocessor conditionals
- [P0136R1] DR11: New specification for inheriting constructors (DR1941 et al)
- [P0018R3] Lambda capture of `*this`
- [P0138R2] Direct-list-initialization of enumerations
- [P0170R1] `constexpr` `lambda` expressions
- [P0184R0] Differing begin and end types in range-based for
- [P0188R1] `[[fallthrough]]` attribute
- [P0189R1] `[[nodiscard]]` attribute
- [P0212R1] `[[maybe_unused]]` attribute
- [P0245R1] Hexadecimal floating-point literals
- [P0028R4] Using attribute namespaces without repetition
- [P0035R4] Dynamic memory allocation for over-aligned data
- [P0091R3] Class template argument deduction
- [P0127R2] Non-type template parameters with `auto` type
- [P0135R1] Guaranteed copy elision
- [P0137R1] Replacement of class objects containing reference members
- [P0145R3] Stricter expression evaluation order
- [P0217R3] Structured Bindings
- [P0283R2] Ignore unknown attributes
- [P0292R2] constexpr if statements
- [P0305R1] init-statements for if and switch
- [P0386R2] Inline variables
- [P0003R5] Removing dynamic exception specifications
- [P0195R2] Pack expansions in using-declarations
- [P0522R0] DR98: Matching of template template-arguments excludes compatible templates

## Library Features

- [N3911] `std::void_t`
- [N4259] `std::uncaught_exceptions()`
- [N4280] `std::size()`, `std::empty()` and `std::data()`
- [N4387] Improving `std::pair` and `std::tuple`
- [N4389] `std::bool_constant`
- [N4508] `std::shared_mutex` (untimed)
- [P0006R0] Type traits variable templates
- [P0013R1] Logical operator type traits
- [P0024R2] Parallel algorithms and execution policies
- [P0025R1] `std::clamp()`
- [P0154R1] Hardware interference size
- [P0185R1] (nothrow-)swappable traits
- [P0218R1] File system library (std::filesystem)
- [N3921, P0220R1] std::string_view
- [P0220R1] `std::any`
- [P0220R1] `std::optional`
- [P0220R1] Polymorphic memory resources
- [P0226R1] Mathematical special functions
- [P0063R3] Major portion of C11 standard library
- [P0083R3] Splicing Maps and Sets
- [P0084R2] return type of emplace* functions of some containers changed from void to reference
- [P0088R3] `std::variant`
- [P0209R2] `std::make_from_tuple()`
- [P0258R2] `std::has_unique_object_representations`
- [P0295R0] `std::gcd()` and `std::lcm()`
- [P0005R4, P0358R1] `std::not_fn`
- [P0067R5] Elementary string conversions: `std::to_chars`/`std::from_chars`
- [P0414R2] `std::shared_ptr` and `std::weak_ptr` with array support
- [P0156R2] `std::scoped_lock`
- [P0298R3] `std::byte`
- [LWG2911] `std::is_aggregate`
- [LWG3657] DR17: `std::hash<std::filesystem::path>`

<!---
GCC

- [N4086] Removing trigraphs
- [N4267] u8 character literals
    - `__cpp_unicode_characters >= 201411 `
- [N4295] Folding expressions
    - `__cpp_fold_expressions >= 201411`
- [N4266] Attributes for namespaces and enumerators
    - `__cpp_namespace_attributes >= 201411`
    - `__cpp_enumerator_attributes >= 201411`
- [N4230] Nested namespace definitions
    - `__cpp_nested_namespace_definitions >= 201411`
- [N4268] Allow constant evaluation for all non-type template arguments
    - `__cpp_nontype_template_args >= 201411`
- [N3928] Extending static_assert
    - `__cpp_static_assert >= 201411`
- [N3922] New Rules for auto deduction from braced-init-list
- [N4051] Allow typename in a template template parameter
- [P0188R1] `[[fallthrough]]` attribute
    - `__has_cpp_attribute(fallthrough)`
- [P0189R1]	[[nodiscard]] attribute
    - `__has_cpp_attribute(nodiscard)`
- [P0212R1] `[[maybe_unused]]` attribute
    - `__has_cpp_attribute(maybe_unused)`
- [P0017R1] Extension to aggregate initialization
    - `__cpp_aggregate_bases >= 201603`
- [P0170R1] Wording for constexpr lambda
    - `__cpp_constexpr >= 201603`
- [P0036R0] Unary Folds and Empty Parameter Packs
    - `__cpp_fold_expressions >= 201603`
- [P0184R0] Generalizing the Range-Based For Loop
    - `__cpp_range_based_for >= 201603`
- [P0018R3] Lambda capture of *this by Value
    - `__cpp_capture_star_this >= 201603`
- [P0138R2] Construction Rules for enum class variables
- [P0245R1] Hexadecimal floating literals for C++
    - `__cpp_hex_float >= 201603`
- [P0035R4] Dynamic memory allocation for over-aligned data
    - `__cpp_aligned_new >= 201606`
- [P0135R1] Guaranteed copy elision
    - `__cpp_guaranteed_copy_elision >= 201606`
- [P0145R3] Refining Expression Evaluation Order for Idiomatic C++
- [P0292R2] constexpr if
    - `__cpp_if_constexpr >= 201606`
- [P0305R1] Selection statements with initializer
- [P0091R3] P0512R0	Template argument deduction for class templates
    - `__cpp_deduction_guides >= 201606`
    - `__cpp_deduction_guides >= 201611`
- [P0127R2] Declaring non-type template parameters with auto
    - `__cpp_template_auto >= 201606`
    - `__cpp_nontype_template_parameter_auto >= 201606`
- [P0028R4] Using attribute namespaces without repetition
- [P0283R2] Ignoring unsupported non-standard attributes
- [P0217R3] Structured bindings
    - `__cpp_structured_bindings >= 201606`
- [P0001R1] Remove Deprecated Use of the register Keyword
- [P0002R1] Remove Deprecated operator++(bool)
- [P0012R1] Make exception specifications be part of the type system
    - `__cpp_noexcept_function_type >= 201510`
- [P0061R1] `__has_include` for C++17
- [P0136R1] Rewording inheriting constructors (core issue 1941 et al)
    - `__cpp_inheriting_constructors >= 201511`
- [P0386R2] Inline variables
    - `__cpp_inline_variables >= 201606`
- [P0522R0] DR 150, Matching of template template arguments
    - `__cpp_template_template_args >= 201611`
- [P0003R5] Removing dynamic exception specifications
- [P0195R2] Pack expansions in using-declarations
    - `__cpp_variadic_using >= 201611`
- [P0298R0] A byte type definition

Clang

N3928	static_assert with no message
N4086	Disabling trigraph expansion by default
N4051	typename in a template template parameter
N3922	New auto rules for direct-list-initialization 
N4295	Fold expressions
P0036R0	
N4267	u8 character literals
N4230	Nested namespace definition
N4266	Attributes for namespaces and enumerators
N4268	Allow constant evaluation for all non-type template arguments
P0001R1	Remove deprecated register storage class
P0002R1	Remove deprecated bool increment
P0012R1	Make exception specifications part of the type system
P0061R1	__has_include in preprocessor conditionals
P0188R1	[[fallthrough]] attribute
P0189R1	[[nodiscard]] attribute
P1771R1 (DR)	
P0212R1	[[maybe_unused]] attribute
P0017R1	Aggregate initialization of classes with base classes
P0170R1	constexpr lambda expressions
P0184R0	Differing begin and end types in range-based for
P0018R3	Lambda capture of *this
P0138R2	Direct-list-initialization of enums
P0245R1	Hexadecimal floating-point literals
P0028R4	Using attribute namespaces without repetition
P0035R4	Dynamic memory allocation for over-aligned data
P0091R3	Template argument deduction for class templates
P0512R0	
P0620R0 (DR)	
P0702R1 (DR)	
P0127R2	Non-type template parameters with auto type
P0135R1	Guaranteed copy elision
P0145R3	Stricter expression evaluation order
P0400R0	
P0283R2	Requirement to ignore unknown attributes
P0292R2	constexpr if-statements
P0386R2	Inline variables
P0217R3	Structured bindings
P0961R1 (DR)	
P0969R0 (DR)	
P0305R1	Separate variable and condition for if and switch
P0522R0 (DR)	Matching template template parameters to compatible arguments
P0003R5	Removing deprecated dynamic exception specifications
P0195R2	Pack expansions in using-declarations

EDG
N4266	Attributes for namespaces and enumerators
N4267	u8 character literals
N4268	Constant evaluation for all non-type template arguments
N4230	Nested namespace definitions
N4295	Fold expressions
N3928	Extended static_assert
N3922	New rules for auto deduction from braced-init-list
N4051	Allow typename in template template parameter list
N4086	Removing trigraphs
N4261	Qualification conversions and pointers to arrays of pointers
P0001R1	Remove deprecated register keyword
P0002R1	Remove deprecated operator++(bool)
P0012R1	Exception specification part of type
P0061R1	__has_include
P0136R1	Rewording inheriting constructors
P0188R1	[[fallthrough]]
P0189R1	[[nodiscard]]
P0212R1	[[maybe_unused]]
P0017R1	Extension to aggregate initialization
P0170R1	Constexpr lambda
P0036R0	Unary folds and empty parameter packs
P0184R0	Generalized range-based for
P0018R3	Lambda capture of *this by value
P0138R2	Construction rules for enum class values
P0245R1	Hexadecimal floating literals
P0028R4	Using attribute namespaces without repetition
P0035R4	Dynamic memory allocation for over-aligned data
P0091R3	Template argument deduction for class templates
P0127R2	Declaring non-type template parameters with auto
P0135R1	Guaranteed copy elision through simplified value categories
P0137R1	Replacement of class objects containing reference members
P0145R3/P0400R0	Refining Expression Evaluation Order for Idiomatic C++
P0283R2	Standard and non-standard attributes
P0292R2	constexpr if
P0386R2	Inline Variables
P0217R3	Structured Bindings
P0305R1	Selection statements with initializer
P0003R5	Removing deprecated exception specificatoins
P0195R2	Pack expansions in using-declarations
P0522R0	Matching of template template-arguments excludes compatible templates
P0298R3	A byte type definition

--->