# Arm

## Identification

`_ARM`

: Identifies the target architecture as Arm.

`__arm`
`__arm__`

: Identifies the target architecture as Arm.

`_M_ARM`

: Identifies the target architecture as Arm.

`_M_ARMT`

: Identifies the target architecture as Arm in Thumb mode.

`__thumb__`

: Identifies the target architecture as Arm in Thumb mode.

`__TARGET_ARCH_ARM`

: Identifies the target architecture as Arm.

## Versioning

## References

<!---
Type|Macro|Description
---|---|---
Identification|`__arm__`|Defined by GNU C and RealView
Identification|`__thumb__`|Defined by GNU C and RealView in Thumb mode
Version|`__ARM_ARCH_'V'__`|V = Version<br/><br/>Defined by GNU C [1](http://wiki.ubuntu.com/ARM/Thumb2PortingHowto)
Identification|`__TARGET_ARCH_ARM`<br/>`__TARGET_ARCH_THUMB`|Defined by RealView
Version|`__TARGET_ARCH_ARM` = V<br/>`__TARGET_ARCH_THUMB` = V|V = Version
Version|`__TARGET_ARCH_'VR'`|VR = Version and Revision
Identification|`_ARM`|Defined by ImageCraft C
Identification|`_M_ARM`|Defined by Visual C++
Identification|`_M_ARMT`|Defined by Visual C++ in Thumb mode
Version|`_M_ARM` = V|V = Version
Identification|`__arm`|Defined by Diab

CPU|Macro|`_M_ARM`
---|---|---
ARM 2|`__ARM_ARCH_2__`|
ARM 3|`__ARM_ARCH_3__`<br/>`__ARM_ARCH_3M__`|
ARM 4T|`__ARM_ARCH_4T__`<br/>`__TARGET_ARM_4T`|
ARM 5|`__ARM_ARCH_5__`<br/>`__ARM_ARCH_5E__`|5
ARM 5T|`__ARM_ARCH_5T__`<br/>`__ARM_ARCH_5TE__`<br/>`__ARM_ARCH_5TEJ__`|
ARM 6|`__ARM_ARCH_6__`<br/>`__ARM_ARCH_6J__`<br/>`__ARM_ARCH_6K__`<br/>`__ARM_ARCH_6Z__`<br/>`__ARM_ARCH_6ZK__`|6
ARM 6T2|`__ARM_ARCH_6T2__`|
ARM 7|`__ARM_ARCH_7__`<br/>`__ARM_ARCH_7A__`<br/>`__ARM_ARCH_7R__`<br/>`__ARM_ARCH_7M__`<br/>`__ARM_ARCH_7S__`|7


<gcc/config/arm/arm-c.cc> (14.2.0)

  static void
  arm_cpu_builtins (struct cpp_reader* pfile)
  {
    def_or_undef_macro (pfile, "__ARM_FEATURE_DSP", TARGET_DSP_MULTIPLY);
    def_or_undef_macro (pfile, "__ARM_FEATURE_QBIT", TARGET_ARM_QBIT);
    def_or_undef_macro (pfile, "__ARM_FEATURE_SAT", TARGET_ARM_SAT);
    def_or_undef_macro (pfile, "__ARM_FEATURE_CRYPTO", TARGET_CRYPTO);
    def_or_undef_macro (pfile, "__ARM_FEATURE_AES", TARGET_CRYPTO);
    def_or_undef_macro (pfile, "__ARM_FEATURE_SHA2", TARGET_CRYPTO);

    def_or_undef_macro (pfile, "__ARM_FEATURE_UNALIGNED", unaligned_access);

    def_or_undef_macro (pfile, "__ARM_FEATURE_QRDMX", TARGET_NEON_RDMA);

    def_or_undef_macro (pfile, "__ARM_FEATURE_CRC32", TARGET_CRC32);
    def_or_undef_macro (pfile, "__ARM_FEATURE_DOTPROD", TARGET_DOTPROD);
    def_or_undef_macro (pfile, "__ARM_FEATURE_COMPLEX", TARGET_COMPLEX);
    def_or_undef_macro (pfile, "__ARM_32BIT_STATE", TARGET_32BIT);

    def_or_undef_macro (pfile, "__ARM_FEATURE_PAUTH", TARGET_HAVE_PACBTI);
    def_or_undef_macro (pfile, "__ARM_FEATURE_BTI", TARGET_HAVE_PACBTI);
    def_or_undef_macro (pfile, "__ARM_FEATURE_BTI_DEFAULT",
            aarch_enable_bti == 1);

    cpp_undef (pfile, "__ARM_FEATURE_PAC_DEFAULT");
    if (aarch_ra_sign_scope != AARCH_FUNCTION_NONE)
    {
      unsigned int pac = 1;

      if (aarch_ra_sign_scope == AARCH_FUNCTION_ALL)
        pac |= 0x4;

      builtin_define_with_int_value ("__ARM_FEATURE_PAC_DEFAULT", pac);
    }

    cpp_undef (pfile, "__ARM_FEATURE_MVE");
    if (TARGET_HAVE_MVE && TARGET_HAVE_MVE_FLOAT)
      {
        builtin_define_with_int_value ("__ARM_FEATURE_MVE", 3);
      }
    else if (TARGET_HAVE_MVE)
      {
        builtin_define_with_int_value ("__ARM_FEATURE_MVE", 1);
      }

    cpp_undef (pfile, "__ARM_FEATURE_CMSE");
    if (arm_arch8 && !arm_arch_notm)
      {
        if (arm_arch_cmse && use_cmse)
    builtin_define_with_int_value ("__ARM_FEATURE_CMSE", 3);
        else
    builtin_define ("__ARM_FEATURE_CMSE");
      }

    cpp_undef (pfile, "__ARM_FEATURE_LDREX");
    if (TARGET_ARM_FEATURE_LDREX)
      builtin_define_with_int_value ("__ARM_FEATURE_LDREX",
            TARGET_ARM_FEATURE_LDREX);

    /* ACLE says that __ARM_FEATURE_CLZ is defined if the hardware
      supports it; it's also clear that this doesn't mean the current
      ISA, so we define this even when compiling for Thumb1 if the
      target supports CLZ in A32.  */
    def_or_undef_macro (pfile, "__ARM_FEATURE_CLZ",
            ((TARGET_ARM_ARCH >= 5 && arm_arch_notm)
            || TARGET_ARM_ARCH_ISA_THUMB >=2));

    def_or_undef_macro (pfile, "__ARM_FEATURE_NUMERIC_MAXMIN",
            TARGET_ARM_ARCH >= 8 && TARGET_NEON && TARGET_VFP5);

    def_or_undef_macro (pfile, "__ARM_FEATURE_SIMD32", TARGET_INT_SIMD);

    builtin_define_with_int_value ("__ARM_SIZEOF_MINIMAL_ENUM",
          flag_short_enums ? 1 : 4);
    builtin_define_type_sizeof ("__ARM_SIZEOF_WCHAR_T", wchar_type_node);

    cpp_undef (pfile, "__ARM_ARCH_PROFILE");
    if (TARGET_ARM_ARCH_PROFILE)
      builtin_define_with_int_value ("__ARM_ARCH_PROFILE",
            TARGET_ARM_ARCH_PROFILE);

    /* Define __arm__ even when in thumb mode, for
      consistency with armcc.  */
    builtin_define ("__arm__");
    if (TARGET_ARM_ARCH)
      {
        cpp_undef (pfile, "__ARM_ARCH");
        builtin_define_with_int_value ("__ARM_ARCH", TARGET_ARM_ARCH);
      }
    if (arm_arch_notm)
      builtin_define ("__ARM_ARCH_ISA_ARM");
    builtin_define ("__APCS_32__");

    def_or_undef_macro (pfile, "__GCC_ASM_FLAG_OUTPUTS__", !TARGET_THUMB1);

    def_or_undef_macro (pfile, "__thumb__", TARGET_THUMB);
    def_or_undef_macro (pfile, "__thumb2__", TARGET_THUMB2);
    if (TARGET_BIG_END)
      def_or_undef_macro (pfile, "__THUMBEB__", TARGET_THUMB);
    else
      def_or_undef_macro (pfile, "__THUMBEL__", TARGET_THUMB);

    cpp_undef (pfile, "__ARM_ARCH_ISA_THUMB");
    if (TARGET_ARM_ARCH_ISA_THUMB)
      builtin_define_with_int_value ("__ARM_ARCH_ISA_THUMB",
            TARGET_ARM_ARCH_ISA_THUMB);

    if (TARGET_BIG_END)
      {
        builtin_define ("__ARMEB__");
        builtin_define ("__ARM_BIG_ENDIAN");
      }
    else
      {
        builtin_define ("__ARMEL__");
      }

    if (TARGET_SOFT_FLOAT)
      builtin_define ("__SOFTFP__");

    builtin_define ("__VFP_FP__");

    cpp_undef (pfile, "__ARM_FP");
    if (TARGET_ARM_FP)
      builtin_define_with_int_value ("__ARM_FP", TARGET_ARM_FP);

    def_or_undef_macro (pfile, "__ARM_FP16_FORMAT_IEEE",
            arm_fp16_format == ARM_FP16_FORMAT_IEEE);
    def_or_undef_macro (pfile, "__ARM_FP16_FORMAT_ALTERNATIVE",
            arm_fp16_format == ARM_FP16_FORMAT_ALTERNATIVE);
    def_or_undef_macro (pfile, "__ARM_FP16_ARGS",
            arm_fp16_format != ARM_FP16_FORMAT_NONE);

    def_or_undef_macro (pfile, "__ARM_FEATURE_FP16_SCALAR_ARITHMETIC",
            TARGET_VFP_FP16INST);
    def_or_undef_macro (pfile, "__ARM_FEATURE_FP16_VECTOR_ARITHMETIC",
            TARGET_NEON_FP16INST);
    def_or_undef_macro (pfile, "__ARM_FEATURE_FP16_FML", TARGET_FP16FML);

    def_or_undef_macro (pfile, "__ARM_FEATURE_FMA", TARGET_FMA);
    def_or_undef_macro (pfile, "__ARM_NEON__", TARGET_NEON);
    def_or_undef_macro (pfile, "__ARM_NEON", TARGET_NEON);

    cpp_undef (pfile, "__ARM_NEON_FP");
    if (TARGET_NEON_FP)
      builtin_define_with_int_value ("__ARM_NEON_FP", TARGET_NEON_FP);

    /* Add a define for interworking. Needed when building libgcc.a.  */
    if (arm_cpp_interwork)
      builtin_define ("__THUMB_INTERWORK__");

    builtin_define (arm_arch_name);
    if (arm_arch_xscale)
      builtin_define ("__XSCALE__");
    if (arm_arch_iwmmxt)
      {
        builtin_define ("__IWMMXT__");
        builtin_define ("__ARM_WMMX");
      }
    if (arm_arch_iwmmxt2)
      builtin_define ("__IWMMXT2__");
    /* ARMv6KZ was originally identified as the misspelled __ARM_ARCH_6ZK__.  To
      preserve the existing behavior, the misspelled feature macro must still be
      defined.  */
    if (arm_arch6kz)
      builtin_define ("__ARM_ARCH_6ZK__");
    if (TARGET_AAPCS_BASED)
      {
        if (arm_pcs_default == ARM_PCS_AAPCS_VFP)
    builtin_define ("__ARM_PCS_VFP");
        else if (arm_pcs_default == ARM_PCS_AAPCS)
    builtin_define ("__ARM_PCS");
        builtin_define ("__ARM_EABI__");
      }

    def_or_undef_macro (pfile, "__FDPIC__", TARGET_FDPIC);

    def_or_undef_macro (pfile, "__ARM_ARCH_EXT_IDIV__", TARGET_IDIV);
    def_or_undef_macro (pfile, "__ARM_FEATURE_IDIV", TARGET_IDIV);

    def_or_undef_macro (pfile, "__ARM_ASM_SYNTAX_UNIFIED__", inline_asm_unified);

    cpp_undef (pfile, "__ARM_FEATURE_COPROC");
    if (TARGET_32BIT && arm_arch4 && !(arm_arch8 && arm_arch_notm))
      {
        int coproc_level = 0x1;

        if (arm_arch5t)
    coproc_level |= 0x2;
        if (arm_arch5te)
    coproc_level |= 0x4;
        if (arm_arch6)
    coproc_level |= 0x8;

        builtin_define_with_int_value ("__ARM_FEATURE_COPROC", coproc_level);
      }

    def_or_undef_macro (pfile, "__ARM_FEATURE_CDE", TARGET_CDE);
    cpp_undef (pfile, "__ARM_FEATURE_CDE_COPROC");
    if (TARGET_CDE)
      builtin_define_with_int_value ("__ARM_FEATURE_CDE_COPROC",
            arm_arch_cde_coproc);

    def_or_undef_macro (pfile, "__ARM_FEATURE_MATMUL_INT8", TARGET_I8MM);
    def_or_undef_macro (pfile, "__ARM_FEATURE_BF16_SCALAR_ARITHMETIC",
            TARGET_BF16_FP);
    def_or_undef_macro (pfile, "__ARM_FEATURE_BF16_VECTOR_ARITHMETIC",
            TARGET_BF16_SIMD);
    def_or_undef_macro (pfile, "__ARM_BF16_FORMAT_ALTERNATIVE",
            TARGET_BF16_FP || TARGET_BF16_SIMD);
  }

  void
  arm_cpu_cpp_builtins (struct cpp_reader * pfile)
  {
    builtin_assert ("cpu=arm");
    builtin_assert ("machine=arm");

    arm_cpu_builtins (pfile);
  }
--->