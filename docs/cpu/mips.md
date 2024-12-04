# MIPS

## Identification

`_mips`
`__mips`
`__mips__`

: Identifies the target architecture as MIPS.

`__MIPS__`

: Identifies the target architecture as MIPS.

## Versioning

## References

<!---
Type|Macro|Description
---|---|---
Identification|`__mips__`<br/>`mips`|Defined by GNU C
Version|`_MIPS_ISA` = `_MIPS_ISA_MIPS'V'`|V = MIPS ISA level
Version|`_R3000`<br/>`_R4000`<br/>`_R5900`|
Identification|`__mips`|Defined by MIPSpro and GNU C
Version|`__mips`|The value indicates the MIPS ISA (Instruction Set Architecture) level
Version|`__MIPS_ISA'V'__`|V = MIPS ISA level
Identification|`__MIPS__`|Defined by Metrowerks

##### Example #####

CPU|`_MIPS_ISA`|GNU C Macro|`__mips`|MIPSpro Macro
---|---|---|---|---
R2000|`_MIPS_ISA_MIPS1`| |1|
R3000|`_MIPS_ISA_MIPS1`|`_R3000`|1|
R6000|`_MIPS_ISA_MIPS2`| |2|`__MIPS_ISA2__`
R4000| |`_R4000`| |
R4400|`_MIPS_ISA_MIPS3`| |3|`__MIPS_ISA3__`
R8000|`_MIPS_ISA_MIPS4`| |4|`__MIPS_ISA4__`
R10000|`_MIPS_ISA_MIPS4`| |4|`__MIPS_ISA4__`

<gcc/config/mips/mips.h> (3.1.0)

#ifndef CPP_PREDEFINES
#define CPP_PREDEFINES "-Dmips -Dunix -Dhost_mips -DMIPSEB -DR3000 -DSYSTYPE_BSD43 \
-D_mips -D_unix -D_host_mips -D_MIPSEB -D_R3000 -D_SYSTYPE_BSD43 \
-Asystem=unix -Asystem=bsd -Acpu=mips -Amachine=mips"
#endif

#if MIPS_ABI_DEFAULT == ABI_EABI
#define SUBTARGET_CPP_SIZE_SPEC "\
%{mabi=eabi|!mabi=*:\
  %{mips1|mips2|mips32|mlong32|mgp32:%{!mips3:%{!mips4:%{!mips5:%{!mips64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}}}}} \
  %{mlong64:\
    %{mgp64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
    %{!mgp64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}}\
  %{mips3|mips4|mips5|mips64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}} \
  %{!mips1:%{!mips2:%{!mips3:%{!mips4:%{!mips5:%{!mips32:%{!mips64:%{!mlong32:%{!mlong64:%{!mgp32:%{!mgp64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}}}}}}}}}}}\
%{mabi=o64:\
 %{mlong64:\
   %{!mgp32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
   %{mgp32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
 %{!mlong64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
%{mabi=32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
"
#endif

#if MIPS_ABI_DEFAULT == ABI_O64
#define SUBTARGET_CPP_SIZE_SPEC "\
%{mabi=eabi:\
  %{mips1|mips2|mips32|mlong32|mgp32:%{!mips3:%{!mips4:%{!mips5:%{!mips64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}}}}} \
  %{mlong64:\
    %{mgp64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
    %{!mgp64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}}\
  %{mips3|mips4|mips5|mips64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}} \
  %{!mips1:%{!mips2:%{!mips3:%{!mips4:%{!mips5:%{!mips32:%{!mips64:%{!mlong32:%{!mlong64:%{!mgp32:%{!mgp64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}}}}}}}}}}}\
%{mabi=o64|!mabi=*:\
 %{mlong64:\
   %{!mgp32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
   %{mgp32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
 %{!mlong64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
%{mabi=32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}\
"
#endif

#if MIPS_ABI_DEFAULT == ABI_32
#define SUBTARGET_CPP_SIZE_SPEC "\
%{mabi=eabi:\
  %{mips1|mips2|mips32|mlong32|mgp32:%{!mips3:%{!mips4:%{!mips5:%{!mips64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}}}}} \
  %{mlong64:\
    %{mgp64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
    %{!mgp64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}}\
  %{mips3|mips4|mips5|mips64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}} \
  %{!mips1:%{!mips2:%{!mips3:%{!mips4:%{!mips5:%{!mips32:%{!mips64:%{!mlong32:%{!mlong64:%{!mgp32:%{!mgp64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}}}}}}}}}}}\
%{mabi=o64:\
 %{mlong64:\
   %{!mgp32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
   %{mgp32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
 %{!mlong64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
%{mabi=32|!mabi=*:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}\
"
#endif

#if MIPS_ABI_DEFAULT == ABI_MEABI
#define SUBTARGET_CPP_SIZE_SPEC "\
%{mabi=eabi:\
  %{mips1|mips2|mips32|mlong32|mgp32:%{!mips3:%{!mips4:%{!mips5:%{!mips64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}}}}} \
  %{mlong64:\
    %{mgp64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
    %{!mgp64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}}\
  %{mips3|mips4|mips5|mips64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}} \
  %{!mips1:%{!mips2:%{!mips3:%{!mips4:%{!mips5:%{!mips32:%{!mips64:%{!mlong32:%{!mlong64:%{!mgp32:%{!mgp64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}}}}}}}}}}}\
%{mabi=o64:\
 %{mlong64:\
   %{!mgp32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
   %{mgp32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
 %{!mlong64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
%{mabi=32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}\
%{mabi=meabi|!mabi=*:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
"
#endif

#else

/* 64-bit default ISA.  */

#if MIPS_ABI_DEFAULT == ABI_EABI
#define SUBTARGET_CPP_SIZE_SPEC "\
%{mabi=eabi|!mabi=*: \
  %{mips1|mips2|mips32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
  %{mlong32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
  %{mlong64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
  %{mgp32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
  %{mips3|mips4|mips5|mips64:%{!mips1:%{!mips2:%{!mips32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}}}}\
  %{!mips1:%{!mips2:%{!mips3:%{!mips4:%{!mips5:%{!mips32:%{!mips64:%{!mlong32:%{!mlong64:%{!mgp32:%{!mgp64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}}}}}}}}}}}\
  %{mgp64:%{!mlong32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}}}\
%{mabi=o64:\
 %{mlong64:\
   %{!mgp32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
   %{mgp32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
 %{!mlong64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
%{mabi=32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
"
#endif

#if MIPS_ABI_DEFAULT == ABI_O64
#define SUBTARGET_CPP_SIZE_SPEC "\
%{mabi=eabi: \
  %{mips1|mips2|mips32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
  %{mlong32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
  %{mlong64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
  %{mgp32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
  %{mips3|mips4|mips5|mips64:%{!mips1:%{!mips2:%{!mips32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}}}}\
  %{!mips1:%{!mips2:%{!mips3:%{!mips4:%{!mips5:%{!mips32:%{!mips64:%{!mlong32:%{!mlong64:%{!mgp32:%{!mgp64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}}}}}}}}}}}\
  %{mgp64:%{!mlong32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}}}\
%{mabi=o64|!mabi=*:\
 %{mlong64:\
   %{!mgp32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
   %{mgp32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
 %{!mlong64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
%{mabi=32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}\
"
#endif

#if MIPS_ABI_DEFAULT == ABI_32
#define SUBTARGET_CPP_SIZE_SPEC "\
%{mabi=eabi:\
  %{mips1|mips2|mips32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
  %{mlong32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
  %{mlong64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
  %{mgp32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
  %{mips3|mips4|mips5|mips64:%{!mips1:%{!mips2:%{!mips32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}}}}\
  %{!mips1:%{!mips2:%{!mips3:%{!mips4:%{!mips5:%{!mips32:%{!mips64:%{!mlong32:%{!mlong64:%{!mgp32:%{!mgp64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}}}}}}}}}}}\
  %{mgp64:%{!mlong32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}}}\
%{mabi=o64:\
 %{mlong64:\
   %{!mgp32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
   %{mgp32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
 %{!mlong64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
%{mabi=32|!mabi=*:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}\
"
#endif

#if MIPS_ABI_DEFAULT == ABI_MEABI
#define SUBTARGET_CPP_SIZE_SPEC "\
%{mabi=eabi:\
  %{mips1|mips2|mips32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
  %{mlong32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
  %{mlong64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
  %{mgp32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int} \
  %{mips3|mips4|mips5|mips64:%{!mips1:%{!mips2:%{!mips32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}}}}\
  %{!mips1:%{!mips2:%{!mips3:%{!mips4:%{!mips5:%{!mips32:%{!mips64:%{!mlong32:%{!mlong64:%{!mgp32:%{!mgp64:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}}}}}}}}}}}\
  %{mgp64:%{!mlong32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int}}}\
%{mabi=o64:\
 %{mlong64:\
   %{!mgp32:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
   %{mgp32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
 %{!mlong64:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}} \
%{mabi=32:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}\
%{mabi=meabi|!mabi=*:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
"
#endif

#endif

#endif

/* SUBTARGET_CPP_SPEC is passed to the preprocessor.  It may be
   overridden by subtargets.  */
#ifndef SUBTARGET_CPP_SPEC
#define SUBTARGET_CPP_SPEC ""
#endif

/* If we're using 64bit longs, then we have to define __LONG_MAX__
   correctly.  Similarly for 64bit ints and __INT_MAX__.  */
#ifndef LONG_MAX_SPEC
#if ((TARGET_DEFAULT | TARGET_CPU_DEFAULT) & MASK_LONG64)
#define LONG_MAX_SPEC "%{!mlong32:-D__LONG_MAX__=9223372036854775807L}"
#else
#define LONG_MAX_SPEC "%{mlong64:-D__LONG_MAX__=9223372036854775807L}"
#endif
#endif

/* Define appropriate macros for fpr register size.  */
#ifndef CPP_FPR_SPEC
#if ((TARGET_DEFAULT | TARGET_CPU_DEFAULT) & MASK_FLOAT64)
#define CPP_FPR_SPEC "-D__mips_fpr=64"
#else
#define CPP_FPR_SPEC "-D__mips_fpr=32"
#endif
#endif

/* For C++ we need to ensure that _LANGUAGE_C_PLUS_PLUS is defined independent
   of the source file extension.  */
#undef CPLUSPLUS_CPP_SPEC
#define CPLUSPLUS_CPP_SPEC "\
-D__LANGUAGE_C_PLUS_PLUS -D_LANGUAGE_C_PLUS_PLUS \
%(cpp) \
"
/* CPP_SPEC is the set of arguments to pass to the preprocessor.  */

#ifndef CPP_SPEC
#define CPP_SPEC "\
%{.m:	-D__LANGUAGE_OBJECTIVE_C -D_LANGUAGE_OBJECTIVE_C -D__LANGUAGE_C -D_LANGUAGE_C} \
%{.S|.s: -D__LANGUAGE_ASSEMBLY -D_LANGUAGE_ASSEMBLY %{!ansi:-DLANGUAGE_ASSEMBLY}} \
%{!.S: %{!.s: %{!.cc: %{!.cxx: %{!.cpp: %{!.cp: %{!.c++: %{!.C: %{!.m: -D__LANGUAGE_C -D_LANGUAGE_C %{!ansi:-DLANGUAGE_C}}}}}}}}}} \
%(subtarget_cpp_size_spec) \
%{mips3:-U__mips -D__mips=3 -D__mips64} \
%{mips4:-U__mips -D__mips=4 -D__mips64} \
%{mips32:-U__mips -D__mips=32} \
%{mips64:-U__mips -D__mips=64 -D__mips64} \
%{mgp32:-U__mips64} %{mgp64:-D__mips64} \
%{mfp32:-D__mips_fpr=32} %{mfp64:-D__mips_fpr=64} %{!mfp32: %{!mfp64: %{mgp32:-D__mips_fpr=32} %{!mgp32: %(cpp_fpr_spec)}}} \
%{msingle-float:%{!msoft-float:-D__mips_single_float}} \
%{m4650:%{!msoft-float:-D__mips_single_float}} \
%{msoft-float:-D__mips_soft_float} \
%{mabi=eabi:-D__mips_eabi} \
%{mips16:%{!mno-mips16:-D__mips16}} \
%{EB:-UMIPSEL -U_MIPSEL -U__MIPSEL -U__MIPSEL__ -D_MIPSEB -D__MIPSEB -D__MIPSEB__ %{!ansi:-DMIPSEB}} \
%{EL:-UMIPSEB -U_MIPSEB -U__MIPSEB -U__MIPSEB__ -D_MIPSEL -D__MIPSEL -D__MIPSEL__ %{!ansi:-DMIPSEL}} \
%(long_max_spec) \
%(subtarget_cpp_spec) "
#endif

<gcc/config/mips/mips.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()					\
  do									\
    {									\
      builtin_assert ("machine=mips");                        		\
      builtin_assert ("cpu=mips");					\
      builtin_define ("__mips__");     					\
      builtin_define ("_mips");						\
									\
      /* We do this here because __mips is defined below and so we	\
	 can't use builtin_define_std.  We don't ever want to define	\
	 "mips" for VxWorks because some of the VxWorks headers		\
	 construct include filenames from a root directory macro,	\
	 an architecture macro and a filename, where the architecture	\
	 macro expands to 'mips'.  If we define 'mips' to 1, the	\
	 architecture macro expands to 1 as well.  */			\
      if (!flag_iso && !TARGET_VXWORKS)					\
	builtin_define ("mips");					\
									\
      if (TARGET_64BIT)							\
	builtin_define ("__mips64");					\
									\
      /* Treat _R3000 and _R4000 like register-size			\
	 defines, which is how they've historically			\
	 been used.  */							\
      if (TARGET_64BIT)							\
	{								\
	  builtin_define_std ("R4000");					\
	  builtin_define ("_R4000");					\
	}								\
      else								\
	{								\
	  builtin_define_std ("R3000");					\
	  builtin_define ("_R3000");					\
	}								\
									\
      if (TARGET_FLOAT64)						\
	builtin_define ("__mips_fpr=64");				\
      else if (TARGET_FLOATXX)						\
	builtin_define ("__mips_fpr=0");				\
      else								\
	builtin_define ("__mips_fpr=32");				\
									\
      if (mips_base_compression_flags & MASK_MIPS16)			\
	builtin_define ("__mips16");					\
									\
      if (TARGET_MIPS16E2)						\
	builtin_define ("__mips_mips16e2");				\
									\
      if (TARGET_MIPS3D)						\
	builtin_define ("__mips3d");					\
									\
      if (TARGET_SMARTMIPS)						\
	builtin_define ("__mips_smartmips");				\
									\
      if (mips_base_compression_flags & MASK_MICROMIPS)			\
	builtin_define ("__mips_micromips");				\
									\
      if (TARGET_MCU)							\
	builtin_define ("__mips_mcu");					\
									\
      if (TARGET_EVA)							\
	builtin_define ("__mips_eva");					\
									\
      if (TARGET_DSP)							\
	{								\
	  builtin_define ("__mips_dsp");				\
	  if (TARGET_DSPR2)						\
	    {								\
	      builtin_define ("__mips_dspr2");				\
	      builtin_define ("__mips_dsp_rev=2");			\
	    }								\
	  else								\
	    builtin_define ("__mips_dsp_rev=1");			\
	}								\
									\
      if (ISA_HAS_MSA)							\
	{								\
	  builtin_define ("__mips_msa");				\
	  builtin_define ("__mips_msa_width=128");			\
	}								\
									\
      MIPS_CPP_SET_PROCESSOR ("_MIPS_ARCH", mips_arch_info);		\
      MIPS_CPP_SET_PROCESSOR ("_MIPS_TUNE", mips_tune_info);		\
									\
      if (ISA_MIPS1)							\
	{								\
	  builtin_define ("__mips=1");					\
	  builtin_define ("_MIPS_ISA=_MIPS_ISA_MIPS1");			\
	}								\
      else if (ISA_MIPS2)						\
	{								\
	  builtin_define ("__mips=2");					\
	  builtin_define ("_MIPS_ISA=_MIPS_ISA_MIPS2");			\
	}								\
      else if (ISA_MIPS3)						\
	{								\
	  builtin_define ("__mips=3");					\
	  builtin_define ("_MIPS_ISA=_MIPS_ISA_MIPS3");			\
	}								\
      else if (ISA_MIPS4)						\
	{								\
	  builtin_define ("__mips=4");					\
	  builtin_define ("_MIPS_ISA=_MIPS_ISA_MIPS4");			\
	}								\
      else if (mips_isa >= MIPS_ISA_MIPS32				\
	       && mips_isa < MIPS_ISA_MIPS64)				\
	{								\
	  builtin_define ("__mips=32");					\
	  builtin_define ("_MIPS_ISA=_MIPS_ISA_MIPS32");		\
	}								\
      else if (mips_isa >= MIPS_ISA_MIPS64)				\
	{								\
	  builtin_define ("__mips=64");					\
	  builtin_define ("_MIPS_ISA=_MIPS_ISA_MIPS64");		\
	}								\
      if (mips_isa_rev > 0)						\
	builtin_define_with_int_value ("__mips_isa_rev",		\
				       mips_isa_rev);			\
									\
      switch (mips_abi)							\
	{								\
	case ABI_32:							\
	  builtin_define ("_ABIO32=1");					\
	  builtin_define ("_MIPS_SIM=_ABIO32");				\
	  break;							\
									\
	case ABI_N32:							\
	  builtin_define ("_ABIN32=2");					\
	  builtin_define ("_MIPS_SIM=_ABIN32");				\
	  break;							\
									\
	case ABI_64:							\
	  builtin_define ("_ABI64=3");					\
	  builtin_define ("_MIPS_SIM=_ABI64");				\
	  break;							\
									\
	case ABI_O64:							\
	  builtin_define ("_ABIO64=4");					\
	  builtin_define ("_MIPS_SIM=_ABIO64");				\
	  break;							\
	}								\
									\
      builtin_define_with_int_value ("_MIPS_SZINT", INT_TYPE_SIZE);	\
      builtin_define_with_int_value ("_MIPS_SZLONG", LONG_TYPE_SIZE);	\
      builtin_define_with_int_value ("_MIPS_SZPTR", POINTER_SIZE);	\
      builtin_define_with_int_value ("_MIPS_FPSET",			\
				     32 / MAX_FPRS_PER_FMT);		\
      builtin_define_with_int_value ("_MIPS_SPFPSET",			\
				     TARGET_ODD_SPREG ? 32 : 16);	\
									\
      /* These defines reflect the ABI in use, not whether the  	\
	 FPU is directly accessible.  */				\
      if (TARGET_NO_FLOAT)						\
	builtin_define ("__mips_no_float");				\
      else if (TARGET_HARD_FLOAT_ABI)					\
	builtin_define ("__mips_hard_float");				\
      else								\
	builtin_define ("__mips_soft_float");				\
									\
      if (TARGET_SINGLE_FLOAT)						\
	builtin_define ("__mips_single_float");				\
									\
      if (TARGET_PAIRED_SINGLE_FLOAT)					\
	builtin_define ("__mips_paired_single_float");			\
									\
      if (mips_abs == MIPS_IEEE_754_2008)				\
	builtin_define ("__mips_abs2008");				\
									\
      if (mips_nan == MIPS_IEEE_754_2008)				\
	builtin_define ("__mips_nan2008");				\
									\
      if (TARGET_BIG_ENDIAN)						\
	{								\
	  builtin_define_std ("MIPSEB");				\
	  builtin_define ("_MIPSEB");					\
	}								\
      else								\
	{								\
	  builtin_define_std ("MIPSEL");				\
	  builtin_define ("_MIPSEL");					\
	}								\
                                                                        \
      /* Whether calls should go through $25.  The separate __PIC__	\
	 macro indicates whether abicalls code might use a GOT.  */	\
      if (TARGET_ABICALLS)						\
	builtin_define ("__mips_abicalls");				\
									\
      /* Whether Loongson vector modes are enabled.  */			\
      if (TARGET_LOONGSON_MMI)						\
	{								\
	  builtin_define ("__mips_loongson_vector_rev");		\
	  builtin_define ("__mips_loongson_mmi");			\
	}								\
									\
      /* Whether Loongson EXT modes are enabled.  */			\
      if (TARGET_LOONGSON_EXT)						\
	{								\
	  builtin_define ("__mips_loongson_ext");			\
	  if (TARGET_LOONGSON_EXT2)					\
	    {								\
	      builtin_define ("__mips_loongson_ext2");			\
	      builtin_define ("__mips_loongson_ext_rev=2");		\
	    }								\
	  else								\
	      builtin_define ("__mips_loongson_ext_rev=1");		\
	}								\
									\
      /* Historical Octeon macro.  */					\
      if (TARGET_OCTEON)						\
	builtin_define ("__OCTEON__");					\
									\
      if (TARGET_SYNCI)							\
	builtin_define ("__mips_synci");				\
									\
      /* Macros dependent on the C dialect.  */				\
      if (preprocessing_asm_p ())					\
	{								\
	  builtin_define_std ("LANGUAGE_ASSEMBLY");			\
	  builtin_define ("_LANGUAGE_ASSEMBLY");			\
	}								\
      else if (c_dialect_cxx ())					\
	{								\
	  builtin_define ("_LANGUAGE_C_PLUS_PLUS");			\
	  builtin_define ("__LANGUAGE_C_PLUS_PLUS");			\
	  builtin_define ("__LANGUAGE_C_PLUS_PLUS__");			\
	}								\
      else								\
	{								\
	  builtin_define_std ("LANGUAGE_C");				\
	  builtin_define ("_LANGUAGE_C");				\
	}								\
      if (c_dialect_objc ())						\
	{								\
	  builtin_define ("_LANGUAGE_OBJECTIVE_C");			\
	  builtin_define ("__LANGUAGE_OBJECTIVE_C");			\
	  /* Bizarre, but retained for backwards compatibility.  */	\
	  builtin_define_std ("LANGUAGE_C");				\
	  builtin_define ("_LANGUAGE_C");				\
	}								\
									\
      if (mips_abi == ABI_EABI)						\
	builtin_define ("__mips_eabi");					\
									\
      if (TARGET_CACHE_BUILTIN)						\
	builtin_define ("__GCC_HAVE_BUILTIN_MIPS_CACHE");		\
      if (!ISA_HAS_LXC1_SXC1)						\
	builtin_define ("__mips_no_lxc1_sxc1");				\
      if (!ISA_HAS_UNFUSED_MADD4 && !ISA_HAS_FUSED_MADD4)		\
	builtin_define ("__mips_no_madd4");				\
									\
      if (TARGET_CB_NEVER)						\
	builtin_define ("__mips_compact_branches_never");		\
      else if (TARGET_CB_ALWAYS)					\
	builtin_define ("__mips_compact_branches_always");		\
      else 								\
	builtin_define ("__mips_compact_branches_optimal");		\
									\
      if (STRICT_ALIGNMENT)						\
	builtin_define ("__mips_strict_alignment");			\
    }									\
  while (0)

<gcc/config/mips/netbsd.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()				\
  do								\
    {								\
      builtin_assert ("cpu=mips");				\
      builtin_define ("__mips__");				\
      builtin_define ("_mips");					\
								\
      /* No _R3000 or _R4000.  */				\
      if (TARGET_64BIT)						\
	builtin_define ("__mips64");				\
								\
      if (TARGET_FLOAT64)					\
	builtin_define ("__mips_fpr=64");			\
      else							\
	builtin_define ("__mips_fpr=32");			\
								\
      if (TARGET_MIPS16)					\
	builtin_define ("__mips16");				\
								\
      MIPS_CPP_SET_PROCESSOR ("_MIPS_ARCH", mips_arch_info);	\
      MIPS_CPP_SET_PROCESSOR ("_MIPS_TUNE", mips_tune_info);	\
								\
      if (ISA_MIPS1)						\
	builtin_define ("__mips=1");				\
      else if (ISA_MIPS2)					\
	builtin_define ("__mips=2");				\
      else if (ISA_MIPS3)					\
	builtin_define ("__mips=3");				\
      else if (ISA_MIPS4)					\
	builtin_define ("__mips=4");				\
      else if (mips_isa >= MIPS_ISA_MIPS32			\
	       && mips_isa < MIPS_ISA_MIPS64)			\
	builtin_define ("__mips=32");				\
      else if (mips_isa >= MIPS_ISA_MIPS64)			\
	builtin_define ("__mips=64");				\
      if (mips_isa_rev > 0)					\
        builtin_define_with_int_value ("__mips_isa_rev",	\
                                       mips_isa_rev);		\
								\
      if (TARGET_HARD_FLOAT)					\
	builtin_define ("__mips_hard_float");			\
      else if (TARGET_SOFT_FLOAT)				\
	builtin_define ("__mips_soft_float");			\
								\
      if (TARGET_SINGLE_FLOAT)					\
	builtin_define ("__mips_single_float");			\
								\
      if (TARGET_BIG_ENDIAN)					\
	builtin_define ("__MIPSEB__");				\
      else							\
	builtin_define ("__MIPSEL__");				\
								\
      /* No language dialect defines.  */			\
								\
      /* ABIs handled in TARGET_OS_CPP_BUILTINS.  */		\
    }								\
  while (0)
--->