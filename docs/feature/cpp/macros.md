---
hide:
    - toc
---
# C++ Feature Test Macros

## Language

| Macro | Values | Papers |
| ----- | ------ | ------ |
| `__cpp_deleted_function` | `#!c 202403` | [P2573R2] |
| `__cpp_aggregate_bases` | `#!c 201603` | [P0017R1] |
| `__cpp_aggregate_nsdmi` | `#!c 201304` | [N3653] |
| `__cpp_aggregate_paren_init` | `#!c 201902` | [P0960R3] |
| `__cpp_alias_templates` | `#!c 200704` | [N2258] |
| `__cpp_aligned_new` | `#!c 201606` | [P0035R4] |
| `__cpp_attributes` | `#!c 200809` | [N2761] |
| `__cpp_binary_literals` | `#!c 201304` | [N3472] |
| `__cpp_capture_star_this` | `#!c 201603` | [P0018R3] |
| `__cpp_char8_t` | `#!c 201811`<br>`#!c 202207` | [P0482R6]<br>[P2513R3] |
| `__cpp_concepts` | `#!c 201707`<br>`#!c 201811`<br>`#!c 201907`<br>`#!c 202002` | [P0734R0]<br>[P1084R2]<br>[P1452R2]<br>[P0848R3] |
| `__cpp_conditional_explicit` | `#!c 201806` | [P0892R2] |
| `__cpp_consteval` | `#!c 201811`<br>`#!c 202211` | [P1073R3]<br>[P2564R3] |
| `__cpp_constexpr` | `#!c 200704`<br>`#!c 201304`<br>`#!c 201603`<br>`#!c 201806`<br>`#!c 201811`<br>`#!c 201907`<br>`#!c 202002`<br>`#!c 202110`<br>`#!c 202207`<br>`#!c 202211`<br>`#!c 202306` | [N2235]<br>[N3652]<br>[P0170R1]<br>[P1064R0]<br>[P1002R1, P1327R1]<br>[P1331R2, P1668R1]<br>[P1330R0]<br>[P2242R3]<br>[P2448R2]<br>[P2647R1]<br>[P2738R1] |
| `__cpp_constexpr_dynamic_alloc` | `#!c 201907` | [P0784R7] |
| `__cpp_constexpr_in_decltype` | `#!c 201711` | [P0859R0] |
| `__cpp_constinit` | `#!c 201907` | [P1143R2] |
| `__cpp_decltype` | `#!c 200707` | [N2343] |
| `__cpp_decltype_auto` | `#!c 201304` | [N3638] |
| `__cpp_deduction_guides` | `#!c 201606`<br>`#!c 201611`<br>`#!c 201703`<br>`#!c 201907` | [P0091R3]<br>[P0512R0]<br>[P0620R0]<br>[P1814R0, P1816R0] |
| `__cpp_delegating_constructors` | `#!c 200604` | [N1986] |
| `__cpp_designated_initializers` | `#!c 201707` | [P0329R4] |
| `__cpp_enumerator_attributes` | `#!c 201411` | [N4266] |
| `__cpp_exceptions` | `#!c 199711` |  |
| `__cpp_explicit_this_parameter` | `#!c 202110` | [P0847R7] |
| `__cpp_fold_expressions` | `#!c 201411`<br>`#!c 201603` | [N4295]<br>[P0036R0] |
| `__cpp_generic_lambdas` | `#!c 201304`<br>`#!c 201707` | [N3649]<br>[P0428R2] |
| `__cpp_guaranteed_copy_elision` | `#!c 201606` | [P0135R1] |
| `__cpp_hex_float` | `#!c 201603` | [P0245R1] |
| `__cpp_if_consteval` | `#!c 202106` | [P1938R3] |
| `__cpp_if_constexpr` | `#!c 201606` | [P0292R2] |
| `__cpp_impl_coroutine` | `#!c 201902` | [P0912R5, LWG3393] |
| `__cpp_impl_destroying_delete` | `#!c 201806` | [P0722R3] |
| `__cpp_impl_three_way_comparison` | `#!c 201711`<br>`#!c 201902`<br>`#!c 201907` | [P0515R3, P0768R1]<br>[P1185R2]<br>[P1630R1] |
| `__cpp_implicit_move` | `#!c 202207` | [P2266R3] |
| `__cpp_inheriting_constructors` | `#!c 200802`<br>`#!c 201511` | [N2540]<br>[P0136R1] |
| `__cpp_init_captures` | `#!c 201304`<br>`#!c 201803` | [N3648]<br>[P0780R2] |
| `__cpp_initializer_lists` | `#!c 200806` | [N2672] |
| `__cpp_inline_variables` | `#!c 201606` | [P0386R2] |
| `__cpp_lambdas` | `#!c 200907` | [N2927] |
| `__cpp_modules` | `#!c 201907` | [P1103R3, P1811R0] |
| `__cpp_multidimensional_subscript` | `#!c 202110`<br>`#!c 202211` | [P2128R6]<br>[P2589R1] |
| `__cpp_named_character_escapes` | `#!c 202207` | [P2071R2] |
| `__cpp_namespace_attributes` | `#!c 201411` | [N4266] |
| `__cpp_noexcept_function_type` | `#!c 201510` | [P0012R1] |
| `__cpp_nontype_template_args` | `#!c 201411`<br>`#!c 201911` | [N4268]<br>[P1907R1] |
| `__cpp_nontype_template_parameter_auto` | `#!c 201606` | [P0127R2] |
| `__cpp_nontype_template_parameter_class` | `#!c 201806`<br>_deleted_ | [P0732R2]<br>[P1907R1] |
| `__cpp_nsdmi` | `#!c 200809` | [N2756] |
| `__cpp_pack_indexing` | `#!c 202311` | [P2662R3] |
| `__cpp_placeholder_variables` | `#!c 202306` | [P2169R4] |
| `__cpp_range_based_for` | `#!c 200907`<br>`#!c 201603`<br>`#!c 202211` | [N2930]<br>[P0184R0]<br>[P2644R1, P2718R0, CWG2659] |
| `__cpp_raw_strings` | `#!c 200710` | [N2442] |
| `__cpp_ref_qualifiers` | `#!c 200710` | [N2439] |
| `__cpp_return_type_deduction` | `#!c 201304` | [N3638] |
| `__cpp_rtti` | `#!c 199711` |  |
| `__cpp_rvalue_references` | `#!c 200610` | [N2118] |
| `__cpp_size_t_suffix` | `#!c 202011` | [P0330R8] |
| `__cpp_sized_deallocation` | `#!c 201309` | [N3778] |
| `__cpp_static_assert` | `#!c 200410`<br>`#!c 201411`<br>`#!c 202306` | [N1720]<br>[N3928]<br>[P2741R3] |
| `__cpp_static_call_operator` | `#!c 202207` | [P1169R4] |
| `__cpp_structured_bindings` | `#!c 201606`<br>`#!c 202403` | [P0217R3]<br>[P0609R3] |
| `__cpp_template_template_args` | `#!c 201611` | [P0522R0] |
| `__cpp_threadsafe_static_init` | `#!c 200806` | [N2660] |
| `__cpp_unicode_characters` | `#!c 200704` | [N2249] |
| `__cpp_unicode_literals` | `#!c 200710` | [N2442] |
| `__cpp_user_defined_literals` | `#!c 200809` | [N2765] |
| `__cpp_using_enum` | `#!c 201907` | [P1099R5] |
| `__cpp_variable_templates` | `#!c 201304` | [N3651] |
| `__cpp_variadic_friend` | `#!c 202403` | [P2893R3] |
| `__cpp_variadic_templates` | `#!c 200704` | [N2242] |
| `__cpp_variadic_using` | `#!c 201611` | [P0195R2] |

## Attribute

| Macro | Values | Papers |
| ----- | ------ | ------ |
| `__has_cpp_attribute(assume)` | `#!c 202207` | [P1774R8, CWG2615] |
| `__has_cpp_attribute(carries_dependency)` | `#!c 200809` | [N2782] |
| `__has_cpp_attribute(deprecated)` | `#!c 201309` | [N3760] |
| `__has_cpp_attribute(fallthrough)` | `#!c 201603` | [P0188R1] |
| `__has_cpp_attribute(likely)` | `#!c 201803` | [P0479R5] |
| `__has_cpp_attribute(maybe_unused)` | `#!c 201603` | [P0212R1] |
| `__has_cpp_attribute(no_unique_address)` | `#!c 201803` | [P0840R2] |
| `__has_cpp_attribute(nodiscard)` | `#!c 201603`<br>`#!c 201907` | [P0189R1]<br>[P1301R4, P1771R1] |
| `__has_cpp_attribute(noreturn)` | `#!c 200809` | [N2761] |
| `__has_cpp_attribute(unlikely)` | `#!c 201803` | [P0479R5] |

## Library

| Macro | Headers | Values | Papers |
| ----- | ------- | ------ | ------ |
| `__cpp_lib_adaptor_iterator_pair_constructor` | `<queue>`<br>`<stack>` | `#!c 202106` | [P1425R4] |
| `__cpp_lib_addressof_constexpr` | `<memory>` | `#!c 201603` | [LWG2296] |
| `__cpp_lib_algorithm_iterator_requirements` | `<algorithm>`<br>`<memory>`<br>`<numeric>` | `#!c 202207` | [P2408R5] |
| `__cpp_lib_allocate_at_least` | `<memory>` | `#!c 202106`<br>`#!c 202306` | [P0401R6]<br>[LWG3887] |
| `__cpp_lib_allocator_traits_is_always_equal` | `<deque>`<br>`<forward_list>`<br>`<list>`<br>`<map>`<br>`<memory>`<br>`<scoped_allocator>`<br>`<set>`<br>`<string>`<br>`<unordered_map>`<br>`<unordered_set>`<br>`<vector>` | `#!c 201411` | [N4258] |
| `__cpp_lib_any` | `<any>` | `#!c 201603`<br>`#!c 201606` | [P0220R1]<br>[P0032R3] |
| `__cpp_lib_apply` | `<tuple>` | `#!c 201603` | [P0220R1] |
| `__cpp_lib_array_constexpr` | `<array>`<br>`<iterator>` | `#!c 201603`<br>`#!c 201803`<br>`#!c 201806`<br>`#!c 201811` | [P0031R0]<br>[P0858R0, LWG3257]<br>[P1023R0]<br>[P1032R1] |
| `__cpp_lib_as_const` | `<utility>` | `#!c 201510` | [P0007R1] |
| `__cpp_lib_associative_heterogeneous_erasure` | `<map>`<br>`<set>`<br>`<unordered_map>`<br>`<unordered_set>` | `#!c 202110` | [P2077R3] |
| `__cpp_lib_associative_heterogeneous_insertion` | `<map>`<br>`<set>`<br>`<unordered_map>`<br>`<unordered_set>` | `#!c 202306` | [P2363R5] |
| `__cpp_lib_assume_aligned` | `<memory>` | `#!c 201811` | [P1007R3] |
| `__cpp_lib_atomic_flag_test` | `<atomic>` | `#!c 201907` | [P1135R6] |
| `__cpp_lib_atomic_float` | `<atomic>` | `#!c 201711` | [P0020R6] |
| `__cpp_lib_atomic_is_always_lock_free` | `<atomic>` | `#!c 201603` | [P0152R1] |
| `__cpp_lib_atomic_lock_free_type_aliases` | `<atomic>` | `#!c 201907` | [P1135R6] |
| `__cpp_lib_atomic_min_max` | `<atomic>` | `#!c 202403` | [P0493R5] |
| `__cpp_lib_atomic_ref` | `<atomic>` | `#!c 201806` | [P0019R8] |
| `__cpp_lib_atomic_shared_ptr` | `<memory>` | `#!c 201711` | [P0718R2] |
| `__cpp_lib_atomic_value_initialization` | `<atomic>`<br>`<memory>` | `#!c 201911` | [P0883R2] |
| `__cpp_lib_atomic_wait` | `<atomic>` | `#!c 201907` | [P1135R6] |
| `__cpp_lib_barrier` | `<barrier>` | `#!c 201907`<br>`#!c 202302` | [P1135R6]<br>[P2588R3] |
| `__cpp_lib_bind_back` | `<functional>` | `#!c 202202`<br>`#!c 202306` | [P2387R3]<br>[P2714R1] |
| `__cpp_lib_bind_front` | `<functional>` | `#!c 201811`<br>`#!c 201907`<br>`#!c 202306` | [P0356R5]<br>[P1651R0]<br>[P2714R1] |
| `__cpp_lib_bit_cast` | `<bit>` | `#!c 201806` | [P0476R2] |
| `__cpp_lib_bitops` | `<bit>` | `#!c 201907` | [P0553R4] |
| `__cpp_lib_bitset` | `<bitset>` | `#!c 202306` | [P2697R1] |
| `__cpp_lib_bool_constant` | `<type_traits>` | `#!c 201505` | [N4389] |
| `__cpp_lib_bounded_array_traits` | `<type_traits>` | `#!c 201902` | [P1357R1] |
| `__cpp_lib_boyer_moore_searcher` | `<functional>` | `#!c 201603` | [P0220R1] |
| `__cpp_lib_byte` | `<cstddef>` | `#!c 201603` | [P0298R3] |
| `__cpp_lib_byteswap` | `<bit>` | `#!c 202110` | [P1272R4] |
| `__cpp_lib_char8_t` | `<atomic>`<br>`<filesystem>`<br>`<istream>`<br>`<limits>`<br>`<locale>`<br>`<ostream>`<br>`<string>`<br>`<string_view>` | `#!c 201811`<br>`#!c 201907` | [P0482R6]<br>[P1423R3] |
| `__cpp_lib_chrono` | `<chrono>` | `#!c 201510`<br>`#!c 201611`<br>`#!c 201803`<br>`#!c 201907`<br>`#!c 202306` | [P0092R1]<br>[P0505R0]<br>[P0355R7]<br>[P1466R3]<br>[P2592R3] |
| `__cpp_lib_chrono_udls` | `<chrono>` | `#!c 201304` | [N3642] |
| `__cpp_lib_clamp` | `<algorithm>` | `#!c 201603` | [P0025R0] |
| `__cpp_lib_common_reference` | `<type_traits>` | `#!c 202302` | [P2655R3] |
| `__cpp_lib_common_reference_wrapper` | `<functional>` | `#!c 202302` | [P2655R3] |
| `__cpp_lib_complex_udls` | `<complex>` | `#!c 201309` | [N3779] |
| `__cpp_lib_concepts` | `<compare>`<br>`<concepts>` | `#!c 201806`<br>`#!c 201907`<br>`#!c 202002`<br>`#!c 202207` | [P0898R3]<br>[P1754R1]<br>[P1964R2]<br>[P2404R3] |
| `__cpp_lib_constexpr_algorithms` | `<algorithm>`<br>`<utility>` | `#!c 201703`<br>`#!c 201806`<br>`#!c 202306` | [P0202R3]<br>[P0879R0, LWG3256, LWG3792]<br>[P2562R1] |
| `__cpp_lib_constexpr_bitset` | `<bitset>` | `#!c 202207` | [P2417R2] |
| `__cpp_lib_constexpr_charconv` | `<charconv>` | `#!c 202207` | [P2291R3] |
| `__cpp_lib_constexpr_cmath` | `<cmath>`<br>`<cstdlib>` | `#!c 202202`<br>`#!c 202306` | [P0533R9]<br>[P1383R2] |
| `__cpp_lib_constexpr_complex` | `<complex>` | `#!c 201711`<br>`#!c 202306` | [P0415R1]<br>[P1383R2] |
| `__cpp_lib_constexpr_dynamic_alloc` | `<memory>` | `#!c 201907` | [P0784R7] |
| `__cpp_lib_constexpr_functional` | `<functional>` | `#!c 201811`<br>`#!c 201907` | [P1032R1]<br>[P1065R2] |
| `__cpp_lib_constexpr_iterator` | `<iterator>` | `#!c 201811` | [P1032R1] |
| `__cpp_lib_constexpr_memory` | `<memory>` | `#!c 201811`<br>`#!c 202202` | [P1006R1]<br>[P2273R3] |
| `__cpp_lib_constexpr_numeric` | `<numeric>` | `#!c 201911` | [P1645R1] |
| `__cpp_lib_constexpr_string` | `<string>` | `#!c 201611`<br>`#!c 201811`<br>`#!c 201907` | [P0426R1]<br>[P1032R1]<br>[P0980R1] |
| `__cpp_lib_constexpr_string_view` | `<string_view>` | `#!c 201611`<br>`#!c 201811` | [P0426R1]<br>[P1032R1] |
| `__cpp_lib_constexpr_tuple` | `<tuple>` | `#!c 201811` | [P1032R1] |
| `__cpp_lib_constexpr_typeinfo` | `<typeinfo>` | `#!c 202106` | [P1328R1] |
| `__cpp_lib_constexpr_utility` | `<utility>` | `#!c 201811` | [P1032R1] |
| `__cpp_lib_constexpr_vector` | `<vector>` | `#!c 201907` | [P1004R2] |
| `__cpp_lib_constrained_equality` | `<optional>`<br>`<tuple>`<br>`<utility>`<br>`<variant>` | `#!c 202403` | [P2944R3] |
| `__cpp_lib_containers_ranges` | `<deque>`<br>`<forward_list>`<br>`<list>`<br>`<map>`<br>`<queue>`<br>`<set>`<br>`<stack>`<br>`<string>`<br>`<unordered_map>`<br>`<unordered_set>`<br>`<vector>` | `#!c 202202` | [P1206R7] |
| `__cpp_lib_copyable_function` | `<functional>` | `#!c 202306` | [P2548R6] |
| `__cpp_lib_coroutine` | `<coroutine>` | `#!c 201902` | [P0912R5, LWG3393] |
| `__cpp_lib_debugging` | `<debugging>` | `#!c 202311`<br>`#!c 202403` | [P2546R5]<br>[P2810R4] |
| `__cpp_lib_deduction_guides` | | `#!c 201703` | [P0433R2] |
| `__cpp_lib_default_template_type_for_algorithm_values` | `<algorithm>`<br>`<deque>`<br>`<forward_list>`<br>`<list>`<br>`<ranges>`<br>`<string>`<br>`<vector>` | `#!c 202403` | [P2248R8] |
| `__cpp_lib_destroying_delete` | `<new>` | `#!c 201806` | [P0722R3] |
| `__cpp_lib_enable_shared_from_this` | `<memory>` | `#!c 201603` | [P0033R1] |
| `__cpp_lib_endian` | `<bit>` | `#!c 201907` | [P0463R1, P1612R1] |
| `__cpp_lib_erase_if` | `<deque>`<br>`<forward_list>`<br>`<list>`<br>`<map>`<br>`<set>`<br>`<string>`<br>`<unordered_map>`<br>`<unordered_set>`<br>`<vector>` | `#!c 201811`<br>`#!c 202002` | [P1209R0]<br>[P1115R3] |
| `__cpp_lib_exchange_function` | `<utility>` | `#!c 201304` | [N3668] |
| `__cpp_lib_execution` | `<execution>` | `#!c 201603`<br>`#!c 201902` | [P0024R2]<br>[P1001R2] |
| `__cpp_lib_expected` | `<expected>` | `#!c 202202`<br>`#!c 202211` | [P0323R12]<br>[P2505R5] |
| `__cpp_lib_filesystem` | `<filesystem>` | `#!c 201603`<br>`#!c 201606`<br>`#!c 201703` | [P0218R1]<br>[P0219R1, P0392R0]<br>[P0317R1] |
| `__cpp_lib_flat_map` | `<flat_map>` | `#!c 202207` | [P0429R9] |
| `__cpp_lib_flat_set` | `<flat_set>` | `#!c 202207` | [P1222R4, LWG3751] |
| `__cpp_lib_format` | `<format>` | `#!c 201907`<br>`#!c 202106`<br>`#!c 202110`<br>`#!c 202207`<br>`#!c 202304`<br>`#!c 202305`<br>`#!c 202306`<br>`#!c 202311` | [P0645R10, P1361R2, P1652R1]<br>[P2216R3]<br>[P2372R3, P2418R2]<br>[P2419R2, P2508R1]<br>[P2510R3]<br>[P2757R3]<br>[P2637R3]<br>[P2918R2] |
| `__cpp_lib_format_path` | `<filesystem>` | `#!c 202403` | [P2845R8] |
| `__cpp_lib_format_ranges` | `<format>` | `#!c 202207` | [P2286R8, P2585R1, LWG3750] |
| `__cpp_lib_format_uchar` | `<format>` | `#!c 202311` | [P2909R4] |
| `__cpp_lib_forward_like` | `<utility>` | `#!c 202207` | [P2445R1] |
| `__cpp_lib_freestanding_algorithm` | `<algorithm>` | `#!c 202311` | [P2407R5] |
| `__cpp_lib_freestanding_array` | `<array>` | `#!c 202311` | [P2407R5] |
| `__cpp_lib_freestanding_char_traits` | `<string>` | `#!c 202306` | [P2338R4] |
| `__cpp_lib_freestanding_charconv` | `<charconv>` | `#!c 202306` | [P2338R4] |
| `__cpp_lib_freestanding_cstdlib` | `<cmath>`<br>`<cstdlib>` | `#!c 202306` | [P2338R4] |
| `__cpp_lib_freestanding_cstring` | `<cstring>` | `#!c 202306`<br>`#!c 202311` | [P2338R4]<br>[P2937R0] |
| `__cpp_lib_freestanding_cwchar` | `<cwchar>` | `#!c 202306` | [P2338R4] |
| `__cpp_lib_freestanding_errc` | `<cerrno>`<br>`<system_error>` | `#!c 202306` | [P2338R4] |
| `__cpp_lib_freestanding_expected` | `<expected>` | `#!c 202311` | [P2833R2] |
| `__cpp_lib_freestanding_feature_test_macros` | | `#!c 202306` | [P2198R7] |
| `__cpp_lib_freestanding_functional` | `<functional>` | `#!c 202306` | [P2198R7] |
| `__cpp_lib_freestanding_iterator` | `<iterator>` | `#!c 202306` | [P2198R7] |
| `__cpp_lib_freestanding_mdspan` | `<mdspan>` | `#!c 202311` | [P2833R2] |
| `__cpp_lib_freestanding_memory` | `<memory>` | `#!c 202306` | [P2198R7] |
| `__cpp_lib_freestanding_operator_new` | `<operator_new>` | `#!c 202306` | [P2198R7] |
| `__cpp_lib_freestanding_optional` | `<optional>` | `#!c 202311` | [P2407R5] |
| `__cpp_lib_freestanding_ranges` | `<ranges>` | `#!c 202306` | [P2198R7] |
| `__cpp_lib_freestanding_ratio` | `<ratio>` | `#!c 202306` | [P2198R7] |
| `__cpp_lib_freestanding_string_view` | `<string_view>` | `#!c 202311` | [P2407R5] |
| `__cpp_lib_freestanding_tuple` | `<tuple>` | `#!c 202306` | [P2198R7] |
| `__cpp_lib_freestanding_utility` | `<utility>` | `#!c 202306` | [P2198R7] |
| `__cpp_lib_freestanding_variant` | `<variant>` | `#!c 202311` | [P2407R5] |
| `__cpp_lib_fstream_native_handle` | `<fstream>` | `#!c 202306` | [P1759R6] |
| `__cpp_lib_function_ref` | `<functional>` | `#!c 202306` | [P0792R14] |
| `__cpp_lib_gcd_lcm` | `<numeric>` | `#!c 201606` | [P0295R0] |
| `__cpp_lib_generate_random` | `<random>` | `#!c 202403` | [P1068R11] |
| `__cpp_lib_generator` | `<generator>` | `#!c 202207` | [P2502R2] |
| `__cpp_lib_generic_associative_lookup` | `<map>`<br>`<set>` | `#!c 201304` | [N3657] |
| `__cpp_lib_generic_unordered_hash_lookup` | `<unordered_map>`<br>`<unordered_set>` | `#!c 201902`<br>_deleted_ | [P0920R2]<br>[P1661R1] |
| `__cpp_lib_generic_unordered_lookup` | `<unordered_map>`<br>`<unordered_set>` | `#!c 201811` | [P0919R3] |
| `__cpp_lib_hardware_interference_size` | `<new>` | `#!c 201703` | [P0154R1] |
| `__cpp_lib_has_unique_object_representations` | `<type_traits>` | `#!c 201606` | [P0258R2] |
| `__cpp_lib_hazard_pointer` | `<hazard_pointer>` | `#!c 202306` | [P2545R4] |
| `__cpp_lib_hypot` | `<cmath>` | `#!c 201603` | [P0030R1] |
| `__cpp_lib_incomplete_container_elements` | `<forward_list>`<br>`<list>`<br>`<vector>` | `#!c 201505` | [N4510] |
| `__cpp_lib_int_pow2` | `<bit>` | `#!c 201806`<br>`#!c 202002` | [P0556R3]<br>[P1956R1] |
| `__cpp_lib_integer_comparison_functions` | `<utility>` | `#!c 202002` | [P0586R2] |
| `__cpp_lib_integer_sequence` | `<utility>` | `#!c 201304` | [N3658] |
| `__cpp_lib_integral_constant_callable` | `<type_traits>` | `#!c 201304` | [N3545] |
| `__cpp_lib_interpolate` | `<cmath>`<br>`<numeric>` | `#!c 201902` | [P0811R3] |
| `__cpp_lib_invoke` | `<functional>` | `#!c 201411` | [N4169] |
| `__cpp_lib_invoke_r` | `<functional>` | `#!c 202106` | [P2136R3] |
| `__cpp_lib_ios_noreplace` | `<ios>` | `#!c 202207` | [P2467R1] |
| `__cpp_lib_is_aggregate` | `<type_traits>` | `#!c 201703` | [LWG2911] |
| `__cpp_lib_is_constant_evaluated` | `<type_traits>` | `#!c 201811` | [P0595R2] |
| `__cpp_lib_is_final` | `<type_traits>` | `#!c 201402` | [LWG2112] |
| `__cpp_lib_is_implicit_lifetime` | `<type_traits>` | `#!c 202302` | [P2674R1] |
| `__cpp_lib_is_invocable` | `<type_traits>` | `#!c 201703` | [P0604R0] |
| `__cpp_lib_is_layout_compatible` | `<type_traits>` | `#!c 201907` | [P0466R5] |
| `__cpp_lib_is_nothrow_convertible` | `<type_traits>` | `#!c 201806` | [P0758R1, LWG3356] |
| `__cpp_lib_is_null_pointer` | `<type_traits>` | `#!c 201309` | [LWG2247] |
| `__cpp_lib_is_pointer_interconvertible` | `<type_traits>` | `#!c 201907` | [P0466R5] |
| `__cpp_lib_is_scoped_enum` | `<type_traits>` | `#!c 202011` | [P1048R1] |
| `__cpp_lib_is_swappable` | `<type_traits>` | `#!c 201603` | [P0185R1] |
| `__cpp_lib_is_within_lifetime` | `<type_traits>` | `#!c 202306` | [P2641R4] |
| `__cpp_lib_jthread` | `<stop_token>`<br>`<thread>` | `#!c 201907`<br>`#!c 201911` | [P0660R10]<br>[P1869R1] |
| `__cpp_lib_latch` | `<latch>` | `#!c 201907` | [P1135R6] |
| `__cpp_lib_launder` | `<new>` | `#!c 201606` | [P0137R1] |
| `__cpp_lib_linalg` | `<linalg>` | `#!c 202311` | [P1673R13] |
| `__cpp_lib_list_remove_return_type` | `<forward_list>`<br>`<list>` | `#!c 201806` | [P0646R1] |
| `__cpp_lib_logical_traits` | `<type_traits>` | `#!c 201510` | [P0013R1] |
| `__cpp_lib_make_from_tuple` | `<tuple>` | `#!c 201606` | [P0209R2] |
| `__cpp_lib_make_reverse_iterator` | `<iterator>` | `#!c 201402` | [LWG2285] |
| `__cpp_lib_make_unique` | `<memory>` | `#!c 201304` | [N3656] |
| `__cpp_lib_map_try_emplace` | `<map>` | `#!c 201411` | [N4279] |
| `__cpp_lib_math_constants` | `<numbers>` | `#!c 201907` | [P0631R8] |
| `__cpp_lib_math_special_functions` | `<cmath>` | `#!c 201603` | [P0226R1] |
| `__cpp_lib_mdspan` | `<mdspan>` | `#!c 202207` | [P0009R18, P2599R2, P2604R0, P2613R1] |
| `__cpp_lib_memory_resource` | `<memory_resource>` | `#!c 201603` | [P0220R1] |
| `__cpp_lib_modules` | | `#!c 202207` | [P2465R3] |
| `__cpp_lib_monadic_optional` | `<optional>` | `#!c 202110`<br>_deleted_ | [P0798R8]<br>[LWG3621] |
| `__cpp_lib_move_iterator_concept` | `<iterator>` | `#!c 202207` | [P2520R0] |
| `__cpp_lib_move_only_function` | `<functional>` | `#!c 202110` | [P0288R9] |
| `__cpp_lib_node_extract` | `<map>`<br>`<set>`<br>`<unordered_map>`<br>`<unordered_set>` | `#!c 201606` | [P0083R3] |
| `__cpp_lib_nonmember_container_access` | `<array>`<br>`<deque>`<br>`<forward_list>`<br>`<iterator>`<br>`<list>`<br>`<map>`<br>`<regex>`<br>`<set>`<br>`<string>`<br>`<unordered_map>`<br>`<unordered_set>`<br>`<vector>` | `#!c 201411` | [N4280] |
| `__cpp_lib_not_fn` | `<functional>` | `#!c 201603`<br>`#!c 202306` | [P0005R4]<br>[P2714R1] |
| `__cpp_lib_null_iterators` | `<iterator>` | `#!c 201304` | [N3644] |
| `__cpp_lib_optional` | `<optional>` | `#!c 201603`<br>`#!c 201606`<br>`#!c 202106`<br>`#!c 202110` | [P0220R1]<br>[P0032R3, P0307R2]<br>[P2231R1]<br>[P0798R8, LWG3621] |
| `__cpp_lib_out_ptr` | `<memory>` | `#!c 202106`<br>`#!c 202311` | [P1132R7]<br>[P2833R2] |
| `__cpp_lib_parallel_algorithm` | `<algorithm>`<br>`<numeric>` | `#!c 201603` | [P0024R2] |
| `__cpp_lib_polymorphic_allocator` | `<memory_resource>` | `#!c 201902` | [P0339R6, LWG3437] |
| `__cpp_lib_print` | `<ostream>`<br>`<print>` | `#!c 202207`<br>`#!c 202403` | [P2093R14]<br>[P3107R5] |
| `__cpp_lib_quoted_string_io` | `<iomanip>` | `#!c 201304` | [N3654] |
| `__cpp_lib_ranges` | `<algorithm>`<br>`<functional>`<br>`<iterator>`<br>`<memory>`<br>`<ranges>` | `#!c 201811`<br>`#!c 201907`<br>`#!c 201911`<br>`#!c 202106`<br>`#!c 202110`<br>`#!c 202202`<br>`#!c 202207`<br>`#!c 202211`<br>`#!c 202302` | [P0896R4]<br>[P1035R7]<br>[P1716R3]<br>[P2325R3]<br>[P2415R2]<br>[P2387R3]<br>[P2494R2]<br>[P2602R2]<br>[P2609R3] |
| `__cpp_lib_ranges_as_const` | `<ranges>` | `#!c 202207`<br>`#!c 202311` | [P2278R4]<br>[P2836R1] |
| `__cpp_lib_ranges_as_rvalue` | `<ranges>` | `#!c 202207` | [P2446R2] |
| `__cpp_lib_ranges_cartesian_product` | `<ranges>` | `#!c 202207` | [P2374R4, P2540R1] |
| `__cpp_lib_ranges_chunk` | `<ranges>` | `#!c 202202` | [P2442R1] |
| `__cpp_lib_ranges_chunk_by` | `<ranges>` | `#!c 202202` | [P2443R1] |
| `__cpp_lib_ranges_concat` | `<ranges>` | `#!c 202403` | [P2542R8] |
| `__cpp_lib_ranges_contains` | `<algorithm>` | `#!c 202207` | [P2302R4] |
| `__cpp_lib_ranges_enumerate` | `<ranges>` | `#!c 202302` | [P2164R9] |
| `__cpp_lib_ranges_find_last` | `<algorithm>` | `#!c 202207` | [P1223R5, LWG3807] |
| `__cpp_lib_ranges_fold` | `<algorithm>` | `#!c 202207` | [P2322R6] |
| `__cpp_lib_ranges_iota` | `<numeric>` | `#!c 202202` | [P2440R1] |
| `__cpp_lib_ranges_join_with` | `<ranges>` | `#!c 202202` | [P2441R2] |
| `__cpp_lib_ranges_repeat` | `<ranges>` | `#!c 202207` | [P2474R2] |
| `__cpp_lib_ranges_slide` | `<ranges>` | `#!c 202202` | [P2442R1] |
| `__cpp_lib_ranges_starts_ends_with` | `<algorithm>` | `#!c 202106` | [P1659R3] |
| `__cpp_lib_ranges_stride` | `<ranges>` | `#!c 202207` | [P1899R3] |
| `__cpp_lib_ranges_to_container` | `<ranges>` | `#!c 202202` | [P1206R7] |
| `__cpp_lib_ranges_zip` | `<ranges>`<br>`<tuple>`<br>`<utility>` | `#!c 202110` | [P2321R2] |
| `__cpp_lib_ratio` | `<ratio>` | `#!c 202306` | [P2734R0] |
| `__cpp_lib_raw_memory_algorithms` | `<memory>` | `#!c 201606` | [P0040R3] |
| `__cpp_lib_rcu` | `<rcu>` | `#!c 202306` | [P2545R4] |
| `__cpp_lib_reference_from_temporary` | `<type_traits>` | `#!c 202202` | [P2255R2] |
| `__cpp_lib_reference_wrapper` | `<functional>` | `#!c 202403` | [P2944R3] |
| `__cpp_lib_remove_cvref` | `<type_traits>` | `#!c 201711` | [P0550R2] |
| `__cpp_lib_result_of_sfinae` | `<functional>`<br>`<type_traits>` | `#!c 201210` | [N3462] |
| `__cpp_lib_robust_nonmodifying_seq_ops` | `<algorithm>` | `#!c 201304` | [N3671] |
| `__cpp_lib_sample` | `<algorithm>` | `#!c 201603` | [P0220R1] |
| `__cpp_lib_saturation_arithmetic` | `<numeric>` | `#!c 202311` | [P0543R3] |
| `__cpp_lib_scoped_lock` | `<mutex>` | `#!c 201703` | [P0156R2] |
| `__cpp_lib_semaphore` | `<semaphore>` | `#!c 201907` | [P1135R6] |
| `__cpp_lib_shared_mutex` | `<shared_mutex>` | `#!c 201505` | [N4508] |
| `__cpp_lib_shared_ptr_arrays` | `<memory>` | `#!c 201611`<br>`#!c 201707` | [P0497R0]<br>[P0674R1] |
| `__cpp_lib_shared_ptr_weak_type` | `<memory>` | `#!c 201606` | [P0163R0] |
| `__cpp_lib_shared_timed_mutex` | `<shared_mutex>` | `#!c 201402` | [N3891] |
| `__cpp_lib_shift` | `<algorithm>` | `#!c 201806`<br>`#!c 202202` | [P0769R2]<br>[P2440R1] |
| `__cpp_lib_smart_pointer_owner_equality` | `<memory>` | `#!c 202306` | [P1901R2] |
| `__cpp_lib_smart_ptr_for_overwrite` | `<memory>` | `#!c 202002` | [P1020R1, P1973R1] |
| `__cpp_lib_source_location` | `<source_location>` | `#!c 201907` | [P1208R6] |
| `__cpp_lib_span` | `<span>` | `#!c 201803`<br>`#!c 201902`<br>`#!c 202002`<br>`#!c 202311` | [P0122R7, LWG3274]<br>[P1024R3]<br>[P1976R2]<br>[P2821R5, P2833R2] |
| `__cpp_lib_span_initializer_list` | `<span>` | `#!c 202311` | [P2447R6] |
| `__cpp_lib_spanstream` | `<spanstream>` | `#!c 202106` | [P0448R4] |
| `__cpp_lib_ssize` | `<iterator>` | `#!c 201902` | [P1227R2] |
| `__cpp_lib_sstream_from_string_view` | `<sstream>` | `#!c 202306` | [P2495R3] |
| `__cpp_lib_stacktrace` | `<stacktrace>` | `#!c 202011` | [P0881R7] |
| `__cpp_lib_start_lifetime_as` | `<memory>` | `#!c 202207` | [P2590R2] |
| `__cpp_lib_starts_ends_with` | `<string>`<br>`<string_view>` | `#!c 201711` | [P0457R2] |
| `__cpp_lib_stdatomic_h` | `<stdatomic.h>` | `#!c 202011` | [P0943R6] |
| `__cpp_lib_string_contains` | `<string>`<br>`<string_view>` | `#!c 202011` | [P1679R3] |
| `__cpp_lib_string_resize_and_overwrite` | `<string>` | `#!c 202110` | [P1072R10] |
| `__cpp_lib_string_udls` | `<string>` | `#!c 201304` | [N3642] |
| `__cpp_lib_string_view` | `<string>`<br>`<string_view>` | `#!c 201603`<br>`#!c 201606`<br>`#!c 201803`<br>`#!c 202403` | [P0220R1]<br>[P0254R2]<br>[P0858R0, LWG3257]<br>[P2591R5] |
| `__cpp_lib_submdspan` | `<mdspan>` | `#!c 202306`<br>`#!c 202403` | [P2630R4]<br>[P2642R6] |
| `__cpp_lib_syncbuf` | `<syncstream>` | `#!c 201711`<br>`#!c 201803` | [P0053R7]<br>[P0753R2] |
| `__cpp_lib_text_encoding` | `<text_encoding>` | `#!c 202306` | [P1885R12] |
| `__cpp_lib_three_way_comparison` | `<compare>` | `#!c 201711`<br>`#!c 201907` | [P0768R1]<br>[P1614R2] |
| `__cpp_lib_to_address` | `<memory>` | `#!c 201711` | [P0653R2] |
| `__cpp_lib_to_array` | `<array>` | `#!c 201907` | [P0325R4] |
| `__cpp_lib_to_chars` | `<charconv>` | `#!c 201611`<br>`#!c 202306` | [P0067R5, P0682R1, LWG3137]<br>[P2497R0] |
| `__cpp_lib_to_string` | `<string>` | `#!c 202306` | [P2587R3] |
| `__cpp_lib_to_underlying` | `<utility>` | `#!c 202102` | [P1682R2] |
| `__cpp_lib_transformation_trait_aliases` | `<type_traits>` | `#!c 201304` | [N3655] |
| `__cpp_lib_transparent_operators` | `<functional>`<br>`<memory>` | `#!c 201210`<br>`#!c 201510` | [N3421]<br>[P0074R0] |
| `__cpp_lib_tuple_element_t` | `<tuple>` | `#!c 201402` | [N3887] |
| `__cpp_lib_tuple_like` | `<map>`<br>`<tuple>`<br>`<unordered_map>`<br>`<utility>` | `#!c 202207`<br>`#!c 202311` | [P2165R4]<br>[P2819R2] |
| `__cpp_lib_tuples_by_type` | `<tuple>`<br>`<utility>` | `#!c 201304` | [N3670] |
| `__cpp_lib_type_identity` | `<type_traits>` | `#!c 201806` | [P0887R1] |
| `__cpp_lib_type_trait_variable_templates` | `<type_traits>` | `#!c 201510` | [P0006R0] |
| `__cpp_lib_uncaught_exceptions` | `<exception>` | `#!c 201411` | [N4259] |
| `__cpp_lib_unordered_map_try_emplace` | `<unordered_map>` | `#!c 201411` | [N4279] |
| `__cpp_lib_unreachable` | `<utility>` | `#!c 202202` | [P0627R6] |
| `__cpp_lib_unwrap_ref` | `<type_traits>` | `#!c 201811` | [P0318R1, LWG3348] |
| `__cpp_lib_variant` | `<variant>` | `#!c 201606`<br>`#!c 202102`<br>`#!c 202106`<br>`#!c 202306` | [P0088R3, P0393R3, P0032R3]<br>[P2162R2]<br>[P2231R1]<br>[P2637R3] |
| `__cpp_lib_void_t` | `<type_traits>` | `#!c 201411` | [N3911] |
