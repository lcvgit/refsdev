# C-SKY

## Identification

`__csky__`

:   Identifies the target CPU as C-SKY.

`__CSKY__`

:   Identifies the target CPU as C-SKY.

## References

<!---
<gcc/config/csky/csky.c> (14.2.0)

void
csky_cpu_cpp_builtins (cpp_reader *pfile)
{
  const char *arch_name = csky_active_target.arch_pp_name;
  char *pp_name = (char *) alloca (1 + strlen (arch_name) + 4);
  sprintf (pp_name, "__%s__", arch_name);
  builtin_define (pp_name);

  builtin_define ("__csky__=2");
  builtin_define ("__CSKY__=2");
  builtin_define ("__ckcore__=2");
  builtin_define ("__CKCORE__=2");

  builtin_define ("__CSKYABIV2__");
  builtin_define ("__cskyabiv2__");
  builtin_define ("__CSKYABI__=2");
  builtin_define ("__cskyabi__=2");

  if (TARGET_BIG_ENDIAN)
    {
      builtin_define ("__ckcoreBE__");
      builtin_define ("__cskyBE__");
      builtin_define ("__cskybe__");
      builtin_define ("__CSKYBE__");
    }
  else
    {
      builtin_define ("__ckcoreLE__");
      builtin_define ("__cskyLE__");
      builtin_define ("__cskyle__");
      builtin_define ("__CSKYLE__");
    }

  if (TARGET_HARD_FLOAT)
    {
      builtin_define ("__csky_hard_float__");
      builtin_define ("__CSKY_HARD_FLOAT__");
      if (TARGET_HARD_FLOAT_ABI)
	{
	  builtin_define ("__csky_hard_float_abi__");
	  builtin_define ("__CSKY_HARD_FLOAT_ABI__");
	}
      else
	{
	  builtin_define ("__csky_soft_float_abi__");
	  builtin_define ("__CSKY_SOFT_FLOAT_ABI__");
	}
      if (TARGET_SINGLE_FPU)
	{
	  builtin_define ("__csky_hard_float_fpu_sf__");
	  builtin_define ("__CSKY_HARD_FLOAT_FPU_SF__");
	}
    }
  else
    {
      builtin_define ("__csky_soft_float__");
      builtin_define ("__CSKY_SOFT_FLOAT__");
    }

  if (CSKY_ISA_FEATURE (fpv2_sf))
    {
      builtin_define ("__csky_fpuv2__");
      builtin_define ("__CSKY_FPUV2__");
    }

  if (TARGET_SUPPORT_FPV3)
    {
      builtin_define ("__csky_fpuv3__");
      builtin_define ("__CSKY_FPUV3__");
    }

  if (TARGET_ELRW)
    {
      builtin_define ("__csky_elrw__");
      builtin_define ("__CSKY_ELRW__");
    }
  if (TARGET_ISTACK)
    {
      builtin_define ("__csky_istack__");
      builtin_define ("__CSKY_ISTACK__");
    }
  if (TARGET_MP)
    {
      builtin_define ("__csky_mp__");
      builtin_define ("__CSKY_MP__");
    }
  if (TARGET_CP)
    {
      builtin_define ("__csky_cp__");
      builtin_define ("__CSKY_CP__");
    }
  if (TARGET_CACHE)
    {
      builtin_define ("__csky_cache__");
      builtin_define ("__CSKY_CACHE__");
    }
  if (TARGET_SECURITY)
    {
      builtin_define ("__csky_security__");
      builtin_define ("__CSKY_SECURITY__");
    }
  if (TARGET_TRUST)
    {
      builtin_define ("__csky_trust__");
      builtin_define ("__CSKY_TRUST__");
    }
  if (TARGET_DSP)
    {
      builtin_define ("__csky_dsp__");
      builtin_define ("__CSKY_DSP__");
    }
  if (TARGET_EDSP)
    {
      builtin_define ("__csky_edsp__");
      builtin_define ("__CSKY_EDSP__");
    }
  if (TARGET_VDSP)
    {
      builtin_define ("__csky_vdsp__");
      builtin_define ("__CSKY_VDSP__");
    }
}
--->