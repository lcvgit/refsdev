# NDS32

## Identification

`__nds32__`

: Identifies the target architecture as NDS32.

`__NDS32__`

: Identifies the target architecture as NDS32.

## References

<!---
<gcc/config/nds32/nds32.h> (14.2.0)

void
nds32_cpu_cpp_builtins(struct cpp_reader *pfile)
{
#define builtin_define(TXT) cpp_define (pfile, TXT)
#define builtin_assert(TXT) cpp_assert (pfile, TXT)
  builtin_define ("__nds32__");
  builtin_define ("__NDS32__");

  /* We need to provide builtin macro to describe the size of
     each vector for interrupt handler under elf toolchain.  */
  if (!TARGET_LINUX_ABI)
    {
      if (TARGET_ISR_VECTOR_SIZE_4_BYTE)
	builtin_define ("__NDS32_ISR_VECTOR_SIZE_4__");
      else
	builtin_define ("__NDS32_ISR_VECTOR_SIZE_16__");
    }

  if (TARGET_HARD_FLOAT)
    builtin_define ("__NDS32_ABI_2FP_PLUS__");
  else
    builtin_define ("__NDS32_ABI_2__");

  if (TARGET_ISA_V2)
    builtin_define ("__NDS32_ISA_V2__");
  if (TARGET_ISA_V3)
    builtin_define ("__NDS32_ISA_V3__");
  if (TARGET_ISA_V3M)
    builtin_define ("__NDS32_ISA_V3M__");

  if (TARGET_FPU_SINGLE)
    builtin_define ("__NDS32_EXT_FPU_SP__");
  if (TARGET_FPU_DOUBLE)
    builtin_define ("__NDS32_EXT_FPU_DP__");

  if (TARGET_EXT_FPU_FMA)
    builtin_define ("__NDS32_EXT_FPU_FMA__");
  if (NDS32_EXT_FPU_DOT_E)
    builtin_define ("__NDS32_EXT_FPU_DOT_E__");
  if (TARGET_FPU_SINGLE || TARGET_FPU_DOUBLE)
    {
      switch (nds32_fp_regnum)
	{
	case 0:
	case 4:
	  builtin_define ("__NDS32_EXT_FPU_CONFIG_0__");
	  break;
	case 1:
	case 5:
	  builtin_define ("__NDS32_EXT_FPU_CONFIG_1__");
	  break;
	case 2:
	case 6:
	  builtin_define ("__NDS32_EXT_FPU_CONFIG_2__");
	  break;
	case 3:
	case 7:
	  builtin_define ("__NDS32_EXT_FPU_CONFIG_3__");
	  break;
	default:
	  abort ();
	}
    }

  if (TARGET_BIG_ENDIAN)
    builtin_define ("__NDS32_EB__");
  else
    builtin_define ("__NDS32_EL__");

  if (TARGET_REDUCED_REGS)
    builtin_define ("__NDS32_REDUCED_REGS__");
  if (TARGET_CMOV)
    builtin_define ("__NDS32_CMOV__");
  if (TARGET_EXT_PERF)
    builtin_define ("__NDS32_EXT_PERF__");
  if (TARGET_EXT_PERF2)
    builtin_define ("__NDS32_EXT_PERF2__");
  if (TARGET_EXT_STRING)
    builtin_define ("__NDS32_EXT_STRING__");
  if (TARGET_16_BIT)
    builtin_define ("__NDS32_16_BIT__");
  if (TARGET_GP_DIRECT)
    builtin_define ("__NDS32_GP_DIRECT__");
  if (TARGET_VH)
    builtin_define ("__NDS32_VH__");
  if (NDS32_EXT_DSP_P ())
    builtin_define ("__NDS32_EXT_DSP__");

  if (TARGET_BIG_ENDIAN)
    builtin_define ("__big_endian__");

  builtin_assert ("cpu=nds32");
  builtin_assert ("machine=nds32");

  if (TARGET_HARD_FLOAT)
    builtin_define ("__NDS32_ABI_2FP_PLUS");
  else
    builtin_define ("__NDS32_ABI_2");

#undef builtin_define
#undef builtin_assert
}
--->