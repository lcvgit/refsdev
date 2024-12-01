# AArch64

<!--
Type|Macro|Description
---|---|---
Identification|`__aarch64__`|Defined by GNU C [1](http://gcc.gnu.org/viewcvs/trunk/gcc/config/aarch64/aarch64.h?view=markup)
Identification|`_M_ARM64`|Defined by Visual C++

<gcc/config/aarch64/aarch64-c.cc> (14.2.0)

  static void
  aarch64_update_cpp_builtins (cpp_reader *pfile)
  {
    aarch64_def_or_undef (flag_unsafe_math_optimizations, "__ARM_FP_FAST", pfile);

    cpp_undef (pfile, "__ARM_ARCH");
    builtin_define_with_int_value ("__ARM_ARCH", AARCH64_ISA_V9A ? 9 : 8);

    builtin_define_with_int_value ("__ARM_SIZEOF_MINIMAL_ENUM",
          flag_short_enums ? 1 : 4);
    aarch64_def_or_undef (TARGET_BIG_END, "__AARCH64EB__", pfile);
    aarch64_def_or_undef (TARGET_BIG_END, "__ARM_BIG_ENDIAN", pfile);
    aarch64_def_or_undef (!TARGET_BIG_END, "__AARCH64EL__", pfile);

    aarch64_def_or_undef (TARGET_FLOAT, "__ARM_FEATURE_FMA", pfile);

    if (TARGET_FLOAT)
      {
        builtin_define_with_int_value ("__ARM_FP", 0x0E);
        builtin_define ("__ARM_FP16_FORMAT_IEEE");
        builtin_define ("__ARM_FP16_ARGS");
      }
    else
      cpp_undef (pfile, "__ARM_FP");

    aarch64_def_or_undef (TARGET_FP_F16INST,
        "__ARM_FEATURE_FP16_SCALAR_ARITHMETIC", pfile);
    aarch64_def_or_undef (TARGET_SIMD_F16INST,
        "__ARM_FEATURE_FP16_VECTOR_ARITHMETIC", pfile);

    aarch64_def_or_undef (TARGET_SIMD, "__ARM_FEATURE_NUMERIC_MAXMIN", pfile);
    aarch64_def_or_undef (TARGET_SIMD, "__ARM_NEON", pfile);

    aarch64_def_or_undef (TARGET_CRC32, "__ARM_FEATURE_CRC32", pfile);
    aarch64_def_or_undef (TARGET_DOTPROD, "__ARM_FEATURE_DOTPROD", pfile);
    aarch64_def_or_undef (TARGET_COMPLEX, "__ARM_FEATURE_COMPLEX", pfile);
    aarch64_def_or_undef (TARGET_JSCVT, "__ARM_FEATURE_JCVT", pfile);

    cpp_undef (pfile, "__AARCH64_CMODEL_TINY__");
    cpp_undef (pfile, "__AARCH64_CMODEL_SMALL__");
    cpp_undef (pfile, "__AARCH64_CMODEL_LARGE__");

    switch (aarch64_cmodel)
      {
        case AARCH64_CMODEL_TINY:
        case AARCH64_CMODEL_TINY_PIC:
    builtin_define ("__AARCH64_CMODEL_TINY__");
    break;
        case AARCH64_CMODEL_SMALL:
        case AARCH64_CMODEL_SMALL_PIC:
    builtin_define ("__AARCH64_CMODEL_SMALL__");
    break;
        case AARCH64_CMODEL_LARGE:
    builtin_define ("__AARCH64_CMODEL_LARGE__");
    break;
        default:
    break;
      }

    aarch64_def_or_undef (TARGET_ILP32, "_ILP32", pfile);
    aarch64_def_or_undef (TARGET_ILP32, "__ILP32__", pfile);

    aarch64_def_or_undef (TARGET_AES && TARGET_SHA2, "__ARM_FEATURE_CRYPTO", pfile);
    aarch64_def_or_undef (TARGET_SIMD_RDMA, "__ARM_FEATURE_QRDMX", pfile);
    aarch64_def_or_undef (TARGET_SVE, "__ARM_FEATURE_SVE", pfile);
    cpp_undef (pfile, "__ARM_FEATURE_SVE_BITS");
    if (TARGET_SVE)
      {
        int bits;
        if (!BITS_PER_SVE_VECTOR.is_constant (&bits))
    bits = 0;
        builtin_define_with_int_value ("__ARM_FEATURE_SVE_BITS", bits);
      }
    aarch64_def_or_undef (TARGET_SVE, "__ARM_FEATURE_SVE_VECTOR_OPERATORS",
        pfile);
    aarch64_def_or_undef (TARGET_SVE_I8MM,
        "__ARM_FEATURE_SVE_MATMUL_INT8", pfile);
    aarch64_def_or_undef (TARGET_SVE_F32MM,
        "__ARM_FEATURE_SVE_MATMUL_FP32", pfile);
    aarch64_def_or_undef (TARGET_SVE_F64MM,
        "__ARM_FEATURE_SVE_MATMUL_FP64", pfile);
    aarch64_def_or_undef (TARGET_SVE2, "__ARM_FEATURE_SVE2", pfile);
    aarch64_def_or_undef (TARGET_SVE2_AES, "__ARM_FEATURE_SVE2_AES", pfile);
    aarch64_def_or_undef (TARGET_SVE2_BITPERM,
        "__ARM_FEATURE_SVE2_BITPERM", pfile);
    aarch64_def_or_undef (TARGET_SVE2_SHA3, "__ARM_FEATURE_SVE2_SHA3", pfile);
    aarch64_def_or_undef (TARGET_SVE2_SM4, "__ARM_FEATURE_SVE2_SM4", pfile);

    aarch64_def_or_undef (TARGET_LSE, "__ARM_FEATURE_ATOMICS", pfile);
    aarch64_def_or_undef (TARGET_AES, "__ARM_FEATURE_AES", pfile);
    aarch64_def_or_undef (TARGET_SHA2, "__ARM_FEATURE_SHA2", pfile);
    aarch64_def_or_undef (TARGET_SHA3, "__ARM_FEATURE_SHA3", pfile);
    aarch64_def_or_undef (TARGET_SHA3, "__ARM_FEATURE_SHA512", pfile);
    aarch64_def_or_undef (TARGET_SM4, "__ARM_FEATURE_SM3", pfile);
    aarch64_def_or_undef (TARGET_SM4, "__ARM_FEATURE_SM4", pfile);
    aarch64_def_or_undef (TARGET_F16FML, "__ARM_FEATURE_FP16_FML", pfile);

    aarch64_def_or_undef (TARGET_FRINT, "__ARM_FEATURE_FRINT", pfile);
    aarch64_def_or_undef (TARGET_TME, "__ARM_FEATURE_TME", pfile);
    aarch64_def_or_undef (TARGET_RNG, "__ARM_FEATURE_RNG", pfile);
    aarch64_def_or_undef (TARGET_MEMTAG, "__ARM_FEATURE_MEMORY_TAGGING", pfile);

    aarch64_def_or_undef (aarch_bti_enabled (),
        "__ARM_FEATURE_BTI_DEFAULT", pfile);

    cpp_undef (pfile, "__ARM_FEATURE_PAC_DEFAULT");
    if (aarch_ra_sign_scope != AARCH_FUNCTION_NONE)
      {
        int v = 0;
        if (aarch64_ra_sign_key == AARCH64_KEY_A)
    v |= 1;
        if (aarch64_ra_sign_key == AARCH64_KEY_B)
    v |= 2;
        if (aarch_ra_sign_scope == AARCH_FUNCTION_ALL)
    v |= 4;
        builtin_define_with_int_value ("__ARM_FEATURE_PAC_DEFAULT", v);
      }

    aarch64_def_or_undef (TARGET_PAUTH, "__ARM_FEATURE_PAUTH", pfile);
    aarch64_def_or_undef (TARGET_BTI, "__ARM_FEATURE_BTI", pfile);
    aarch64_def_or_undef (TARGET_I8MM, "__ARM_FEATURE_MATMUL_INT8", pfile);
    aarch64_def_or_undef (TARGET_BF16_SIMD,
        "__ARM_FEATURE_BF16_VECTOR_ARITHMETIC", pfile);
    aarch64_def_or_undef (TARGET_BF16_FP,
        "__ARM_FEATURE_BF16_SCALAR_ARITHMETIC", pfile);
    aarch64_def_or_undef (TARGET_BF16_FP,
        "__ARM_FEATURE_BF16", pfile);
    aarch64_def_or_undef (TARGET_SVE_BF16,
        "__ARM_FEATURE_SVE_BF16", pfile);

    aarch64_def_or_undef (TARGET_LS64,
        "__ARM_FEATURE_LS64", pfile);
    aarch64_def_or_undef (AARCH64_ISA_RCPC, "__ARM_FEATURE_RCPC", pfile);
    aarch64_def_or_undef (TARGET_D128, "__ARM_FEATURE_SYSREG128", pfile);

    aarch64_def_or_undef (TARGET_SME, "__ARM_FEATURE_SME", pfile);
    aarch64_def_or_undef (TARGET_SME_I16I64, "__ARM_FEATURE_SME_I16I64", pfile);
    aarch64_def_or_undef (TARGET_SME_F64F64, "__ARM_FEATURE_SME_F64F64", pfile);
    aarch64_def_or_undef (TARGET_SME2, "__ARM_FEATURE_SME2", pfile);

    /* Not for ACLE, but required to keep "float.h" correct if we switch
      target between implementations that do or do not support ARMv8.2-A
      16-bit floating-point extensions.  */
    cpp_undef (pfile, "__FLT_EVAL_METHOD__");
    builtin_define_with_int_value ("__FLT_EVAL_METHOD__",
          c_flt_eval_method (true));
    cpp_undef (pfile, "__FLT_EVAL_METHOD_C99__");
    builtin_define_with_int_value ("__FLT_EVAL_METHOD_C99__",
          c_flt_eval_method (false));
  }
-->
