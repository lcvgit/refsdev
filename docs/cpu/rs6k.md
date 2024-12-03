# RS/6000

## Identification

`_IBMR2`
`__IBMR2__`

`_POWER`
`__POWER__`

`__THW_RS6000`

## References

<!---
Type|Macro|Description
---|---|---
Identification|`__THW_RS6000`|Defined by XL C/C++
Identification|`_IBMR2`|
Identification|`_POWER`|
Identification|`_ARCH_PWR`<br/>`_ARCH_PWR2`<br/>`_ARCH_PWR3`<br/>`_ARCH_PWR4`|

#define CPP_CPU_SPEC \
"%{!mcpu*: \
  %{mpower: %{!mpower2: -D_ARCH_PWR}} \
  %{mpower2: -D_ARCH_PWR2} \
  %{mpowerpc*: -D_ARCH_PPC} \
  %{mno-power: %{!mpowerpc*: -D_ARCH_COM}} \
  %{!mno-power: %{!mpower2: %(cpp_default)}}} \
%{mcpu=common: -D_ARCH_COM} \
%{mcpu=power: -D_ARCH_PWR} \
%{mcpu=power2: -D_ARCH_PWR2} \
%{mcpu=powerpc: -D_ARCH_PPC} \
%{mcpu=rios: -D_ARCH_PWR} \
%{mcpu=rios1: -D_ARCH_PWR} \
%{mcpu=rios2: -D_ARCH_PWR2} \
%{mcpu=rsc: -D_ARCH_PWR} \
%{mcpu=rsc1: -D_ARCH_PWR} \
%{mcpu=401: -D_ARCH_PPC} \
%{mcpu=403: -D_ARCH_PPC} \
%{mcpu=405: -D_ARCH_PPC} \
%{mcpu=505: -D_ARCH_PPC} \
%{mcpu=601: -D_ARCH_PPC -D_ARCH_PWR} \
%{mcpu=602: -D_ARCH_PPC} \
%{mcpu=603: -D_ARCH_PPC} \
%{mcpu=603e: -D_ARCH_PPC} \
%{mcpu=ec603e: -D_ARCH_PPC} \
%{mcpu=604: -D_ARCH_PPC} \
%{mcpu=604e: -D_ARCH_PPC} \
%{mcpu=620: -D_ARCH_PPC} \
%{mcpu=740: -D_ARCH_PPC} \
%{mcpu=7400: -D_ARCH_PPC} \
%{mcpu=7450: -D_ARCH_PPC} \
%{mcpu=750: -D_ARCH_PPC} \
%{mcpu=801: -D_ARCH_PPC} \
%{mcpu=821: -D_ARCH_PPC} \
%{mcpu=823: -D_ARCH_PPC} \
%{mcpu=860: -D_ARCH_PPC} \
%{maltivec: -D__ALTIVEC__}"

/* Common ASM definitions used by ASM_SPEC among the various targets
   for handling -mcpu=xxx switches.  */
#define ASM_CPU_SPEC \
"%{!mcpu*: \
  %{mpower: %{!mpower2: -mpwr}} \
  %{mpower2: -mpwrx} \
  %{mpowerpc*: -mppc} \
  %{mno-power: %{!mpowerpc*: -mcom}} \
  %{!mno-power: %{!mpower2: %(asm_default)}}} \
%{mcpu=common: -mcom} \
%{mcpu=power: -mpwr} \
%{mcpu=power2: -mpwrx} \
%{mcpu=powerpc: -mppc} \
%{mcpu=rios: -mpwr} \
%{mcpu=rios1: -mpwr} \
%{mcpu=rios2: -mpwrx} \
%{mcpu=rsc: -mpwr} \
%{mcpu=rsc1: -mpwr} \
%{mcpu=401: -mppc} \
%{mcpu=403: -mppc} \
%{mcpu=405: -mppc} \
%{mcpu=505: -mppc} \
%{mcpu=601: -m601} \
%{mcpu=602: -mppc} \
%{mcpu=603: -mppc} \
%{mcpu=603e: -mppc} \
%{mcpu=ec603e: -mppc} \
%{mcpu=604: -mppc} \
%{mcpu=604e: -mppc} \
%{mcpu=620: -mppc} \
%{mcpu=740: -mppc} \
%{mcpu=7400: -mppc} \
%{mcpu=7450: -mppc} \
%{mcpu=750: -mppc} \
%{mcpu=801: -mppc} \
%{mcpu=821: -mppc} \
%{mcpu=823: -mppc} \
%{mcpu=860: -mppc} \
%{maltivec: -maltivec}"
////


////
AIX

#define CPP_PREDEFINES "-D_IBMR2 -D_POWER -D_AIX -D_AIX32 -D_LONG_LONG \
-Asystem=unix -Asystem=aix -Acpu=rs6000 -Amachine=rs6000"

/* Define appropriate architecture macros for preprocessor depending on
   target switches.  */

#define CPP_SPEC "%{posix: -D_POSIX_SOURCE}\
   %{ansi: -D_ANSI_C_SOURCE}\
   %(cpp_cpu)"
////

////
AIX31
  #define CPP_PREDEFINES "-D_IBMR2 -D_AIX -Asystem=unix -Asystem=aix -Acpu=rs6000 -Amachine=rs6000"

AIX41
  #define CPP_PREDEFINES "-D_IBMR2 -D_POWER -D_AIX -D_AIX32 -D_AIX41 \
  -D_LONG_LONG -Asystem=unix -Asystem=aix"

AIX43
  #define CPP_PREDEFINES "-D_IBMR2 -D_POWER -D_AIX -D_AIX32 -D_AIX41 -D_AIX43 \
  -D_LONG_LONG -Asystem=unix -Asystem=aix"

AIX51
  #define CPP_PREDEFINES "-D_IBMR2 -D_POWER -D_LONG_LONG \
  -D_AIX -D_AIX32 -D_AIX41 -D_AIX43 -D_AIX51 -Asystem=unix -Asystem=aix"

BEOS
  #define CPP_PREDEFINES "-D__BEOS__ -D__POWERPC__ -Asystem=beos -Acpu=powerpc -Amachine=powerpc"

Darwin
  #define CPP_PREDEFINES "-D__ppc__ -D__POWERPC__ -D__NATURAL_ALIGNMENT__ -D__MACH__ -D__BIG_ENDIAN__ -D__APPLE__"

eabi (embedded)
  #define CPP_PREDEFINES \
    "-DPPC -D__embedded__ -Asystem=embedded -Acpu=powerpc -Amachine=powerpc"

eabisim
  #define CPP_PREDEFINES \
    "-DPPC -D__embedded__ -D__simulator__ -Asystem=embedded -Asystem=simulator -Acpu=powerpc -Amachine=powerpc"

Linux
  #define CPP_PREDEFINES \
  "-DPPC -D__ELF__ -Dpowerpc -Acpu=powerpc -Amachine=powerpc"

Linux64
  #define CPP_PREDEFINES \
  "-D_PPC_ -D__PPC__ -D_PPC64_ -D__PPC64__ -D__powerpc__ -D__powerpc64__ \
    -D_PIC_ -D__PIC__ -D_BIG_ENDIAN -D__BIG_ENDIAN__ -D__ELF__ \
    -D__LONG_MAX__=9223372036854775807L \
    -Acpu=powerpc64 -Amachine=powerpc64"

Lynx
  #define CPP_PREDEFINES "-Acpu=rs6000 -Amachine=rs6000 -Asystem=lynx -Asystem=unix -DLynx -D_IBMR2 -Dunix -Drs6000 -Dlynx -DLYNX"

Mach
  #define CPP_PREDEFINES "-Drios -D_IBMR2 -Dunix -Asystem=unix -Asystem=mach -Acpu=rs6000 -Amachine=rs6000"

RTEMS
  #define CPP_PREDEFINES "-DPPC -D__rtems__ \
   -Asystem=rtems -Acpu=powerpc -Amachine=powerpc"

VxWorks
  #define CPP_PREDEFINES "\
  -D__vxworks -D__vxworks__ -Asystem=vxworks -Asystem=embedded \
  -Acpu=powerpc -Amachine=powerpc"
////


////
/* IBM RS/6000 CPU names..
   Copyright (C) 1991-2024 Free Software Foundation, Inc.
   Contributed by Richard Kenner (kenner@vlsi1.ultra.nyu.edu)

   This file is part of GCC.

   GCC is free software; you can redistribute it and/or modify it
   under the terms of the GNU General Public License as published
   by the Free Software Foundation; either version 3, or (at your
   option) any later version.

   GCC is distributed in the hope that it will be useful, but WITHOUT
   ANY WARRANTY; without even the implied warranty of MERCHANTABILITY
   or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public
   License for more details.

   You should have received a copy of the GNU General Public License
   along with GCC; see the file COPYING3.  If not see
   <http://www.gnu.org/licenses/>.  */

/* ISA masks.  */
#ifndef ISA_2_1_MASKS
#define ISA_2_1_MASKS		OPTION_MASK_MFCRF
#define ISA_2_2_MASKS		(ISA_2_1_MASKS | OPTION_MASK_POPCNTB)
#define ISA_2_4_MASKS		(ISA_2_2_MASKS | OPTION_MASK_FPRND)

  /* For ISA 2.05, don't add ALTIVEC, since in general it isn't a win on
     power6.  In ISA 2.04, fsel, fre, fsqrt, etc. were no longer documented
     as optional.  Group masks by server and embedded. */
#define ISA_2_5_MASKS_EMBEDDED	(ISA_2_4_MASKS				\
				 | OPTION_MASK_CMPB			\
				 | OPTION_MASK_RECIP_PRECISION		\
				 | OPTION_MASK_PPC_GFXOPT		\
				 | OPTION_MASK_PPC_GPOPT)

#define ISA_2_5_MASKS_SERVER	(ISA_2_5_MASKS_EMBEDDED | OPTION_MASK_DFP)

  /* For ISA 2.06, don't add ISEL, since in general it isn't a win, but
     altivec is a win so enable it.  */
#define ISA_2_6_MASKS_EMBEDDED	(ISA_2_5_MASKS_EMBEDDED | OPTION_MASK_POPCNTD)
#define ISA_2_6_MASKS_SERVER	(ISA_2_5_MASKS_SERVER			\
				 | OPTION_MASK_POPCNTD			\
				 | OPTION_MASK_ALTIVEC			\
				 | OPTION_MASK_VSX)

/* For now, don't provide an embedded version of ISA 2.07.  Do not set power8
   fusion here, instead set it in rs6000.cc if we are tuning for a power8
   system.  */
#define ISA_2_7_MASKS_SERVER	(ISA_2_6_MASKS_SERVER			\
				 | OPTION_MASK_POWER8			\
				 | OPTION_MASK_P8_VECTOR		\
				 | OPTION_MASK_CRYPTO			\
				 | OPTION_MASK_EFFICIENT_UNALIGNED_VSX	\
				 | OPTION_MASK_QUAD_MEMORY		\
				 | OPTION_MASK_QUAD_MEMORY_ATOMIC)

/* ISA masks setting fusion options.  */
#define OTHER_FUSION_MASKS	(OPTION_MASK_P8_FUSION			\
				 | OPTION_MASK_P8_FUSION_SIGN)

/* Add ISEL back into ISA 3.0, since it is supposed to be a win.  Do not add
   FLOAT128_HW here until we are ready to make -mfloat128 on by default.  */
#define ISA_3_0_MASKS_SERVER	((ISA_2_7_MASKS_SERVER			\
				  | OPTION_MASK_ISEL			\
				  | OPTION_MASK_MODULO			\
				  | OPTION_MASK_P9_MINMAX		\
				  | OPTION_MASK_P9_MISC			\
				  | OPTION_MASK_P9_VECTOR)		\
				 & ~OTHER_FUSION_MASKS)

/* Support for the IEEE 128-bit floating point hardware requires a lot of the
   VSX instructions that are part of ISA 3.0.  */
#define ISA_3_0_MASKS_IEEE	(OPTION_MASK_VSX			\
				 | OPTION_MASK_P8_VECTOR		\
				 | OPTION_MASK_P9_VECTOR)

/* Flags that need to be turned off if -mno-power10.  */
/* We comment out PCREL_OPT here to disable it by default because SPEC2017
   performance was degraded by it.  */
#define OTHER_POWER10_MASKS	(OPTION_MASK_MMA			\
				 | OPTION_MASK_PCREL			\
				 /* | OPTION_MASK_PCREL_OPT */		\
				 | OPTION_MASK_PREFIXED)

#define ISA_3_1_MASKS_SERVER	(ISA_3_0_MASKS_SERVER			\
				 | OPTION_MASK_POWER10			\
				 | OTHER_POWER10_MASKS)

/* Flags that need to be turned off if -mno-vsx.  */
#define OTHER_VSX_VECTOR_MASKS	(OPTION_MASK_EFFICIENT_UNALIGNED_VSX	\
				 | OPTION_MASK_FLOAT128_KEYWORD		\
				 | OPTION_MASK_P8_VECTOR		\
				 | OPTION_MASK_CRYPTO			\
				 | OPTION_MASK_P9_VECTOR		\
				 | OPTION_MASK_FLOAT128_HW		\
				 | OPTION_MASK_P9_MINMAX)

/* Flags that need to be turned off if -mno-altivec.  */
#define OTHER_ALTIVEC_MASKS	(OTHER_VSX_VECTOR_MASKS			\
				 | OPTION_MASK_VSX)

#define POWERPC_7400_MASK	(OPTION_MASK_PPC_GFXOPT | OPTION_MASK_ALTIVEC)

/* Deal with ports that do not have -mstrict-align.  */
#ifdef OPTION_MASK_STRICT_ALIGN
#define OPTION_MASK_STRICT_ALIGN_OPTIONAL OPTION_MASK_STRICT_ALIGN
#else
#define OPTION_MASK_STRICT_ALIGN 0
#define OPTION_MASK_STRICT_ALIGN_OPTIONAL 0
#ifndef MASK_STRICT_ALIGN
#define MASK_STRICT_ALIGN 0
#endif
#endif

/* Mask of all options to set the default isa flags based on -mcpu=<xxx>.  */
#define POWERPC_MASKS		(OPTION_MASK_ALTIVEC			\
				 | OPTION_MASK_CMPB			\
				 | OPTION_MASK_CRYPTO			\
				 | OPTION_MASK_DFP			\
				 | OPTION_MASK_DLMZB			\
				 | OPTION_MASK_EFFICIENT_UNALIGNED_VSX	\
				 | OPTION_MASK_FLOAT128_HW		\
				 | OPTION_MASK_FLOAT128_KEYWORD		\
				 | OPTION_MASK_FPRND			\
				 | OPTION_MASK_POWER10			\
				 | OPTION_MASK_P10_FUSION		\
				 | OPTION_MASK_HTM			\
				 | OPTION_MASK_ISEL			\
				 | OPTION_MASK_MFCRF			\
				 | OPTION_MASK_MMA			\
				 | OPTION_MASK_MODULO			\
				 | OPTION_MASK_MULHW			\
				 | OPTION_MASK_NO_UPDATE		\
				 | OPTION_MASK_POWER8			\
				 | OPTION_MASK_P8_FUSION		\
				 | OPTION_MASK_P8_VECTOR		\
				 | OPTION_MASK_P9_MINMAX		\
				 | OPTION_MASK_P9_MISC			\
				 | OPTION_MASK_P9_VECTOR		\
				 | OPTION_MASK_PCREL			\
				 | OPTION_MASK_PCREL_OPT		\
				 | OPTION_MASK_POPCNTB			\
				 | OPTION_MASK_POPCNTD			\
				 | OPTION_MASK_POWERPC64		\
				 | OPTION_MASK_PPC_GFXOPT		\
				 | OPTION_MASK_PPC_GPOPT		\
				 | OPTION_MASK_PREFIXED			\
				 | OPTION_MASK_QUAD_MEMORY		\
				 | OPTION_MASK_QUAD_MEMORY_ATOMIC	\
				 | OPTION_MASK_RECIP_PRECISION		\
				 | OPTION_MASK_SOFT_FLOAT		\
				 | OPTION_MASK_STRICT_ALIGN_OPTIONAL	\
				 | OPTION_MASK_VSX)

#endif

/* This table occasionally claims that a processor does not support a
   particular feature even though it does, but the feature is slower than the
   alternative.  Thus, it shouldn't be relied on as a complete description of
   the processor's support.

   Please keep this list in order, and don't forget to update the documentation
   in invoke.texi when adding a new processor or flag.

   Before including this file, define a macro:

   RS6000_CPU (NAME, CPU, FLAGS)

   where the arguments are the fields of struct rs6000_ptt.  */

RS6000_CPU ("401", PROCESSOR_PPC403, OPTION_MASK_SOFT_FLOAT)
RS6000_CPU ("403", PROCESSOR_PPC403, OPTION_MASK_SOFT_FLOAT | MASK_STRICT_ALIGN)
RS6000_CPU ("405", PROCESSOR_PPC405, OPTION_MASK_SOFT_FLOAT
	    | OPTION_MASK_MULHW | OPTION_MASK_DLMZB)
RS6000_CPU ("405fp", PROCESSOR_PPC405, OPTION_MASK_MULHW | OPTION_MASK_DLMZB)
RS6000_CPU ("440", PROCESSOR_PPC440, OPTION_MASK_SOFT_FLOAT
	    | OPTION_MASK_MULHW | OPTION_MASK_DLMZB)
RS6000_CPU ("440fp", PROCESSOR_PPC440, OPTION_MASK_MULHW | OPTION_MASK_DLMZB)
RS6000_CPU ("464", PROCESSOR_PPC440, OPTION_MASK_SOFT_FLOAT
	    | OPTION_MASK_MULHW | OPTION_MASK_DLMZB)
RS6000_CPU ("464fp", PROCESSOR_PPC440, OPTION_MASK_MULHW | OPTION_MASK_DLMZB)
RS6000_CPU ("476", PROCESSOR_PPC476, OPTION_MASK_SOFT_FLOAT
	    | OPTION_MASK_PPC_GFXOPT | OPTION_MASK_MFCRF | OPTION_MASK_POPCNTB
	    | OPTION_MASK_FPRND | OPTION_MASK_CMPB | OPTION_MASK_MULHW
	    | OPTION_MASK_DLMZB)
RS6000_CPU ("476fp", PROCESSOR_PPC476, OPTION_MASK_PPC_GFXOPT
	    | OPTION_MASK_MFCRF | OPTION_MASK_POPCNTB | OPTION_MASK_FPRND
	    | OPTION_MASK_CMPB | OPTION_MASK_MULHW | OPTION_MASK_DLMZB)
RS6000_CPU ("505", PROCESSOR_MPCCORE, 0)
RS6000_CPU ("601", PROCESSOR_PPC601, OPTION_MASK_MULTIPLE)
RS6000_CPU ("602", PROCESSOR_PPC603, OPTION_MASK_PPC_GFXOPT)
RS6000_CPU ("603", PROCESSOR_PPC603, OPTION_MASK_PPC_GFXOPT)
RS6000_CPU ("603e", PROCESSOR_PPC603, OPTION_MASK_PPC_GFXOPT)
RS6000_CPU ("604", PROCESSOR_PPC604, OPTION_MASK_PPC_GFXOPT)
RS6000_CPU ("604e", PROCESSOR_PPC604e, OPTION_MASK_PPC_GFXOPT)
RS6000_CPU ("620", PROCESSOR_PPC620, OPTION_MASK_PPC_GFXOPT | MASK_POWERPC64)
RS6000_CPU ("630", PROCESSOR_PPC630, OPTION_MASK_PPC_GFXOPT | MASK_POWERPC64)
RS6000_CPU ("740", PROCESSOR_PPC750, OPTION_MASK_PPC_GFXOPT)
RS6000_CPU ("7400", PROCESSOR_PPC7400, POWERPC_7400_MASK)
RS6000_CPU ("7450", PROCESSOR_PPC7450, POWERPC_7400_MASK)
RS6000_CPU ("750", PROCESSOR_PPC750, OPTION_MASK_PPC_GFXOPT)
RS6000_CPU ("801", PROCESSOR_MPCCORE, OPTION_MASK_SOFT_FLOAT)
RS6000_CPU ("821", PROCESSOR_MPCCORE, OPTION_MASK_SOFT_FLOAT)
RS6000_CPU ("823", PROCESSOR_MPCCORE, OPTION_MASK_SOFT_FLOAT)
RS6000_CPU ("8540", PROCESSOR_PPC8540, MASK_STRICT_ALIGN | OPTION_MASK_ISEL)
RS6000_CPU ("8548", PROCESSOR_PPC8548, MASK_STRICT_ALIGN | OPTION_MASK_ISEL)
RS6000_CPU ("a2", PROCESSOR_PPCA2, OPTION_MASK_PPC_GFXOPT | MASK_POWERPC64
	    | OPTION_MASK_POPCNTB | OPTION_MASK_CMPB
	    | OPTION_MASK_NO_UPDATE)
RS6000_CPU ("e300c2", PROCESSOR_PPCE300C2, OPTION_MASK_SOFT_FLOAT)
RS6000_CPU ("e300c3", PROCESSOR_PPCE300C3, 0)
RS6000_CPU ("e500mc", PROCESSOR_PPCE500MC, OPTION_MASK_PPC_GFXOPT
	    | OPTION_MASK_ISEL)
RS6000_CPU ("e500mc64", PROCESSOR_PPCE500MC64,
	    MASK_POWERPC64 | OPTION_MASK_PPC_GFXOPT | OPTION_MASK_ISEL)
RS6000_CPU ("e5500", PROCESSOR_PPCE5500,
	    MASK_POWERPC64 | OPTION_MASK_PPC_GFXOPT | OPTION_MASK_ISEL)
RS6000_CPU ("e6500", PROCESSOR_PPCE6500, POWERPC_7400_MASK | MASK_POWERPC64
	    | OPTION_MASK_MFCRF | OPTION_MASK_ISEL)
RS6000_CPU ("860", PROCESSOR_MPCCORE, OPTION_MASK_SOFT_FLOAT)
RS6000_CPU ("970", PROCESSOR_POWER4, POWERPC_7400_MASK | OPTION_MASK_PPC_GPOPT
	    | OPTION_MASK_MFCRF | MASK_POWERPC64)
RS6000_CPU ("cell", PROCESSOR_CELL, POWERPC_7400_MASK  | OPTION_MASK_PPC_GPOPT
	    | OPTION_MASK_MFCRF | MASK_POWERPC64)
RS6000_CPU ("ec603e", PROCESSOR_PPC603, OPTION_MASK_SOFT_FLOAT)
RS6000_CPU ("G3", PROCESSOR_PPC750, OPTION_MASK_PPC_GFXOPT)
RS6000_CPU ("G4",  PROCESSOR_PPC7450, POWERPC_7400_MASK)
RS6000_CPU ("G5", PROCESSOR_POWER4, POWERPC_7400_MASK | OPTION_MASK_PPC_GPOPT
	    | OPTION_MASK_MFCRF | MASK_POWERPC64)
RS6000_CPU ("titan", PROCESSOR_TITAN, OPTION_MASK_MULHW | OPTION_MASK_DLMZB)
RS6000_CPU ("power3", PROCESSOR_PPC630, OPTION_MASK_PPC_GFXOPT | MASK_POWERPC64)
RS6000_CPU ("power4", PROCESSOR_POWER4, MASK_POWERPC64 | OPTION_MASK_PPC_GPOPT
	    | OPTION_MASK_PPC_GFXOPT | OPTION_MASK_MFCRF)
RS6000_CPU ("power5", PROCESSOR_POWER5, MASK_POWERPC64 | OPTION_MASK_PPC_GPOPT
	    | OPTION_MASK_PPC_GFXOPT | OPTION_MASK_MFCRF | OPTION_MASK_POPCNTB)
RS6000_CPU ("power5+", PROCESSOR_POWER5, MASK_POWERPC64 | OPTION_MASK_PPC_GPOPT
	    | OPTION_MASK_PPC_GFXOPT | OPTION_MASK_MFCRF | OPTION_MASK_POPCNTB
	    | OPTION_MASK_FPRND)
RS6000_CPU ("power6", PROCESSOR_POWER6, MASK_POWERPC64 | OPTION_MASK_PPC_GPOPT
	    | OPTION_MASK_PPC_GFXOPT | OPTION_MASK_MFCRF | OPTION_MASK_POPCNTB
	    | OPTION_MASK_FPRND | OPTION_MASK_CMPB | OPTION_MASK_DFP
	    | OPTION_MASK_RECIP_PRECISION)
RS6000_CPU ("power6x", PROCESSOR_POWER6, MASK_POWERPC64 | OPTION_MASK_PPC_GPOPT
	    | OPTION_MASK_PPC_GFXOPT | OPTION_MASK_MFCRF | OPTION_MASK_POPCNTB
	    | OPTION_MASK_FPRND | OPTION_MASK_CMPB | OPTION_MASK_DFP
	    | OPTION_MASK_RECIP_PRECISION)
RS6000_CPU ("power7", PROCESSOR_POWER7, MASK_POWERPC64 | ISA_2_6_MASKS_SERVER)
RS6000_CPU ("power8", PROCESSOR_POWER8, MASK_POWERPC64 | ISA_2_7_MASKS_SERVER
	    | OPTION_MASK_HTM)
RS6000_CPU ("power9", PROCESSOR_POWER9, MASK_POWERPC64 | ISA_3_0_MASKS_SERVER
	    | OPTION_MASK_HTM)
RS6000_CPU ("power10", PROCESSOR_POWER10, MASK_POWERPC64 | ISA_3_1_MASKS_SERVER)
RS6000_CPU ("powerpc", PROCESSOR_POWERPC, 0)
RS6000_CPU ("powerpc64", PROCESSOR_POWERPC64, OPTION_MASK_PPC_GFXOPT
	    | MASK_POWERPC64)
RS6000_CPU ("powerpc64le", PROCESSOR_POWER8, MASK_POWERPC64
	    | ISA_2_7_MASKS_SERVER | OPTION_MASK_HTM)
RS6000_CPU ("rs64", PROCESSOR_RS64A, OPTION_MASK_PPC_GFXOPT | MASK_POWERPC64)
////



////
<gcc/config/rs6000/rs6000-c.cc> (14.2.0)

/* Define or undefine macros based on the current target.  If the user does
   #pragma GCC target, we need to adjust the macros dynamically.  */

void
rs6000_target_modify_macros (bool define_p, HOST_WIDE_INT flags)
{
  if (TARGET_DEBUG_BUILTIN || TARGET_DEBUG_TARGET)
    fprintf (stderr,
	     "rs6000_target_modify_macros (%s, " HOST_WIDE_INT_PRINT_HEX ")\n",
	     (define_p) ? "define" : "undef",
	     flags);

  /* Each of the flags mentioned below controls whether certain
     preprocessor macros will be automatically defined when
     preprocessing source files for compilation by this compiler.
     While most of these flags can be enabled or disabled
     explicitly by specifying certain command-line options when
     invoking the compiler, there are also many ways in which these
     flags are enabled or disabled implicitly, based on compiler
     defaults, configuration choices, and on the presence of certain
     related command-line options.  Many, but not all, of these
     implicit behaviors can be found in file "rs6000.cc", the
     rs6000_option_override_internal() function.

     In general, each of the flags may be automatically enabled in
     any of the following conditions:

     1. If no -mcpu target is specified on the command line and no
	--with-cpu target is specified to the configure command line
	and the TARGET_DEFAULT macro for this default cpu host
	includes the flag, and the flag has not been explicitly disabled
	by command-line options.

     2. If the target specified with -mcpu=target on the command line, or
	in the absence of a -mcpu=target command-line option, if the
	target specified using --with-cpu=target on the configure
	command line, is disqualified because the associated binary
	tools (e.g. the assembler) lack support for the requested cpu,
	and the TARGET_DEFAULT macro for this default cpu host
	includes the flag, and the flag has not been explicitly disabled
	by command-line options.

     3. If either of the above two conditions apply except that the
	TARGET_DEFAULT macro is defined to equal zero, and
	TARGET_POWERPC64 and
	a) BYTES_BIG_ENDIAN and the flag to be enabled is either
	   OPTION_MASK_PPC_GFXOPT or MASK_POWERPC64 (flags for "powerpc64"
	   target), or
	b) !BYTES_BIG_ENDIAN and the flag to be enabled is either
	   MASK_POWERPC64 or it is one of the flags included in
	   ISA_2_7_MASKS_SERVER (flags for "powerpc64le" target).

     4. If a cpu has been requested with a -mcpu=target command-line option
	and this cpu has not been disqualified due to shortcomings of the
	binary tools, and the set of flags associated with the requested cpu
	include the flag to be enabled.  See rs6000-cpus.def for macro
	definitions that represent various ABI standards
	(e.g. ISA_2_1_MASKS, ISA_3_0_MASKS_SERVER) and for a list of
	the specific flags that are associated with each of the cpu
	choices that can be specified as the target of a -mcpu=target
	compile option, or as the target of a --with-cpu=target
	configure option.  Target flags that are specified in either
	of these two ways are considered "implicit" since the flags
	are not mentioned specifically by name.

	Additional documentation describing behavior specific to
	particular flags is provided below, immediately preceding the
	use of each relevant flag.

     5. If there is no -mcpu=target command-line option, and the cpu
	requested by a --with-cpu=target command-line option has not
	been disqualified due to shortcomings of the binary tools, and
	the set of flags associated with the specified target include
	the flag to be enabled.  See the notes immediately above for a
	summary of the flags associated with particular cpu
	definitions.  */

  /* rs6000_isa_flags based options.  */
  rs6000_define_or_undefine_macro (define_p, "_ARCH_PPC");
  if ((flags & OPTION_MASK_PPC_GPOPT) != 0)
    rs6000_define_or_undefine_macro (define_p, "_ARCH_PPCSQ");
  if ((flags & OPTION_MASK_PPC_GFXOPT) != 0)
    rs6000_define_or_undefine_macro (define_p, "_ARCH_PPCGR");
  if ((flags & OPTION_MASK_POWERPC64) != 0)
    rs6000_define_or_undefine_macro (define_p, "_ARCH_PPC64");
  if ((flags & OPTION_MASK_MFCRF) != 0)
    rs6000_define_or_undefine_macro (define_p, "_ARCH_PWR4");
  if ((flags & OPTION_MASK_POPCNTB) != 0)
    rs6000_define_or_undefine_macro (define_p, "_ARCH_PWR5");
  if ((flags & OPTION_MASK_FPRND) != 0)
    rs6000_define_or_undefine_macro (define_p, "_ARCH_PWR5X");
  if ((flags & OPTION_MASK_CMPB) != 0)
    rs6000_define_or_undefine_macro (define_p, "_ARCH_PWR6");
  if ((flags & OPTION_MASK_POPCNTD) != 0)
    rs6000_define_or_undefine_macro (define_p, "_ARCH_PWR7");
  if ((flags & OPTION_MASK_POWER8) != 0)
    rs6000_define_or_undefine_macro (define_p, "_ARCH_PWR8");
  if ((flags & OPTION_MASK_MODULO) != 0)
    rs6000_define_or_undefine_macro (define_p, "_ARCH_PWR9");
  if ((flags & OPTION_MASK_POWER10) != 0)
    rs6000_define_or_undefine_macro (define_p, "_ARCH_PWR10");
  if ((flags & OPTION_MASK_SOFT_FLOAT) != 0)
    rs6000_define_or_undefine_macro (define_p, "_SOFT_FLOAT");
  if ((flags & OPTION_MASK_RECIP_PRECISION) != 0)
    rs6000_define_or_undefine_macro (define_p, "__RECIP_PRECISION__");
  /* Note that the OPTION_MASK_ALTIVEC flag is automatically turned on
     in any of the following conditions:
     1. The operating system is Darwin and it is configured for 64
	bit.  (See darwin_rs6000_override_options.)
     2. The operating system is Darwin and the operating system
	version is 10.5 or higher and the user has not explicitly
	disabled ALTIVEC by specifying -mcpu=G3 or -mno-altivec and
	the compiler is not producing code for integration within the
	kernel.  (See darwin_rs6000_override_options.)
     Note that the OPTION_MASK_ALTIVEC flag is automatically turned
     off in any of the following conditions:
     1. The operating system does not support saving of AltiVec
	registers (OS_MISSING_ALTIVEC).
     2. If an inner context (as introduced by
	__attribute__((__target__())) or #pragma GCC target()
	requests a target that normally enables the
	OPTION_MASK_ALTIVEC flag but the outer-most "main target"
	does not support the rs6000_altivec_abi, this flag is
	turned off for the inner context unless OPTION_MASK_ALTIVEC
	was explicitly enabled for the inner context.  */
  if ((flags & OPTION_MASK_ALTIVEC) != 0)
    {
      const char *vec_str = (define_p) ? "__VEC__=10206" : "__VEC__";
      rs6000_define_or_undefine_macro (define_p, "__ALTIVEC__");
      rs6000_define_or_undefine_macro (define_p, vec_str);

	  /* Define this when supporting context-sensitive keywords.  */
      if (!flag_iso)
	rs6000_define_or_undefine_macro (define_p, "__APPLE_ALTIVEC__");
      if (rs6000_aix_extabi)
	rs6000_define_or_undefine_macro (define_p, "__EXTABI__");
    }
  /* Note that the OPTION_MASK_VSX flag is automatically turned on in
     the following conditions:
     1. TARGET_P8_VECTOR is explicitly turned on and the OPTION_MASK_VSX
        was not explicitly turned off.  Hereafter, the OPTION_MASK_VSX
        flag is considered to have been explicitly turned on.
     Note that the OPTION_MASK_VSX flag is automatically turned off in
     the following conditions:
     1. The operating system does not support saving of AltiVec
	registers (OS_MISSING_ALTIVEC).
     2. If the option TARGET_HARD_FLOAT is turned off.  Hereafter, the
	OPTION_MASK_VSX flag is considered to have been turned off
	explicitly.
     3. If TARGET_AVOID_XFORM is turned on explicitly at the outermost
	compilation context, or if it is turned on by any means in an
	inner compilation context.  Hereafter, the OPTION_MASK_VSX
	flag is considered to have been turned off explicitly.
     4. If TARGET_ALTIVEC was explicitly disabled.  Hereafter, the
	OPTION_MASK_VSX flag is considered to have been turned off
	explicitly.
     5. If an inner context (as introduced by
	__attribute__((__target__())) or #pragma GCC target()
	requests a target that normally enables the
	OPTION_MASK_VSX flag but the outer-most "main target"
	does not support the rs6000_altivec_abi, this flag is
	turned off for the inner context unless OPTION_MASK_VSX
	was explicitly enabled for the inner context.  */
  if ((flags & OPTION_MASK_VSX) != 0)
    rs6000_define_or_undefine_macro (define_p, "__VSX__");
  if ((flags & OPTION_MASK_HTM) != 0)
    {
      rs6000_define_or_undefine_macro (define_p, "__HTM__");
      /* Tell the user that our HTM insn patterns act as memory barriers.  */
      rs6000_define_or_undefine_macro (define_p, "__TM_FENCE__");
    }
  /* Note that the OPTION_MASK_P8_VECTOR flag is automatically turned
     on in the following conditions:
     1. TARGET_P9_VECTOR is explicitly turned on and
        OPTION_MASK_P8_VECTOR is not explicitly turned off.
        Hereafter, the OPTION_MASK_P8_VECTOR flag is considered to
        have been turned off explicitly.
     Note that the OPTION_MASK_P8_VECTOR flag is automatically turned
     off in the following conditions:
     1. If any of TARGET_HARD_FLOAT, TARGET_ALTIVEC, or TARGET_VSX
	were turned off explicitly and OPTION_MASK_P8_VECTOR flag was
	not turned on explicitly.
     2. If TARGET_ALTIVEC is turned off.  Hereafter, the
	OPTION_MASK_P8_VECTOR flag is considered to have been turned off
	explicitly.
     3. If TARGET_VSX is turned off and OPTION_MASK_P8_VECTOR was not
        explicitly enabled.  If TARGET_VSX is explicitly enabled, the
        OPTION_MASK_P8_VECTOR flag is hereafter also considered to
	have been turned off explicitly.  */
  if ((flags & OPTION_MASK_P8_VECTOR) != 0)
    rs6000_define_or_undefine_macro (define_p, "__POWER8_VECTOR__");
  /* Note that the OPTION_MASK_P9_VECTOR flag is automatically turned
     off in the following conditions:
     1. If TARGET_P8_VECTOR is turned off and OPTION_MASK_P9_VECTOR is
        not turned on explicitly. Hereafter, if OPTION_MASK_P8_VECTOR
        was turned on explicitly, the OPTION_MASK_P9_VECTOR flag is
        also considered to have been turned off explicitly.
     Note that the OPTION_MASK_P9_VECTOR is automatically turned on
     in the following conditions:
     1. If TARGET_P9_MINMAX was turned on explicitly.
        Hereafter, THE OPTION_MASK_P9_VECTOR flag is considered to
        have been turned on explicitly.  */
  if ((flags & OPTION_MASK_P9_VECTOR) != 0)
    rs6000_define_or_undefine_macro (define_p, "__POWER9_VECTOR__");
  /* Note that the OPTION_MASK_QUAD_MEMORY flag is automatically
     turned off in the following conditions:
     1. If TARGET_POWERPC64 is turned off.
     2. If WORDS_BIG_ENDIAN is false (non-atomic quad memory
	load/store are disabled on little endian).  */
  if ((flags & OPTION_MASK_QUAD_MEMORY) != 0)
    rs6000_define_or_undefine_macro (define_p, "__QUAD_MEMORY__");
  /* Note that the OPTION_MASK_QUAD_MEMORY_ATOMIC flag is automatically
     turned off in the following conditions:
     1. If TARGET_POWERPC64 is turned off.
     Note that the OPTION_MASK_QUAD_MEMORY_ATOMIC flag is
     automatically turned on in the following conditions:
     1. If TARGET_QUAD_MEMORY and this flag was not explicitly
	disabled.  */
  if ((flags & OPTION_MASK_QUAD_MEMORY_ATOMIC) != 0)
    rs6000_define_or_undefine_macro (define_p, "__QUAD_MEMORY_ATOMIC__");
  /* Note that the OPTION_MASK_CRYPTO flag is automatically turned off
     in the following conditions:
     1. If any of TARGET_HARD_FLOAT or TARGET_ALTIVEC or TARGET_VSX
	are turned off explicitly and OPTION_MASK_CRYPTO is not turned
	on explicitly.
     2. If TARGET_ALTIVEC is turned off.  */
  if ((flags & OPTION_MASK_CRYPTO) != 0)
    rs6000_define_or_undefine_macro (define_p, "__CRYPTO__");
  if ((flags & OPTION_MASK_FLOAT128_KEYWORD) != 0)
    {
      rs6000_define_or_undefine_macro (define_p, "__FLOAT128__");
      if (define_p)
	rs6000_define_or_undefine_macro (true, "__float128=__ieee128");
      else
	rs6000_define_or_undefine_macro (false, "__float128");
      if (ieee128_float_type_node && define_p)
	rs6000_define_or_undefine_macro (true, "__SIZEOF_FLOAT128__=16");
      else
	rs6000_define_or_undefine_macro (false, "__SIZEOF_FLOAT128__");
    }
  /* OPTION_MASK_FLOAT128_HARDWARE can be turned on if -mcpu=power9 is used or
     via the target attribute/pragma.  */
  if ((flags & OPTION_MASK_FLOAT128_HW) != 0)
    rs6000_define_or_undefine_macro (define_p, "__FLOAT128_HARDWARE__");

  /* Tell the user if we are targeting CELL.  */
  if (rs6000_cpu == PROCESSOR_CELL)
    rs6000_define_or_undefine_macro (define_p, "__PPU__");

  /* Tell the user if we support the MMA instructions.  */
  if ((flags & OPTION_MASK_MMA) != 0)
    rs6000_define_or_undefine_macro (define_p, "__MMA__");
  /* Whether pc-relative code is being generated.  */
  if ((flags & OPTION_MASK_PCREL) != 0)
    rs6000_define_or_undefine_macro (define_p, "__PCREL__");
  /* Tell the user -mrop-protect is in play.  */
  if (rs6000_rop_protect)
    rs6000_define_or_undefine_macro (define_p, "__ROP_PROTECT__");
  /* Tell the user __builtin_set_fpscr_rn now returns the FPSCR fields
     in a double.  Originally the built-in returned void.  */
  if ((flags & OPTION_MASK_SOFT_FLOAT) == 0)
    rs6000_define_or_undefine_macro (define_p,
				     "__SET_FPSCR_RN_RETURNS_FPSCR__");
}

void
rs6000_cpu_cpp_builtins (cpp_reader *pfile)
{
  /* Define all of the common macros.  */
  rs6000_target_modify_macros (true, rs6000_isa_flags);

  if (TARGET_FRE)
    builtin_define ("__RECIP__");
  if (TARGET_FRES)
    builtin_define ("__RECIPF__");
  if (TARGET_FRSQRTE)
    builtin_define ("__RSQRTE__");
  if (TARGET_FRSQRTES)
    builtin_define ("__RSQRTEF__");
  if (TARGET_FLOAT128_TYPE)
    builtin_define ("__FLOAT128_TYPE__");
  if (ibm128_float_type_node)
    builtin_define ("__SIZEOF_IBM128__=16");
  if (ieee128_float_type_node)
    builtin_define ("__SIZEOF_IEEE128__=16");
#ifdef TARGET_LIBC_PROVIDES_HWCAP_IN_TCB
  builtin_define ("__BUILTIN_CPU_SUPPORTS__");
#endif

  if (TARGET_EXTRA_BUILTINS && cpp_get_options (pfile)->lang != CLK_ASM)
    {
      /* Define the AltiVec syntactic elements.  */
      builtin_define ("__vector=__attribute__((altivec(vector__)))");
      builtin_define ("__pixel=__attribute__((altivec(pixel__))) unsigned short");
      builtin_define ("__bool=__attribute__((altivec(bool__))) unsigned");

      if (!flag_iso)
	{
	  builtin_define ("vector=vector");
	  builtin_define ("pixel=pixel");
	  builtin_define ("bool=bool");
	  builtin_define ("_Bool=_Bool");
	  init_vector_keywords ();

	  /* Enable context-sensitive macros.  */
	  cpp_get_callbacks (pfile)->macro_to_expand = rs6000_macro_to_expand;
	}
    }
  if (!TARGET_HARD_FLOAT)
    builtin_define ("_SOFT_DOUBLE");
  /* Used by lwarx/stwcx. errata work-around.  */
  if (rs6000_cpu == PROCESSOR_PPC405)
    builtin_define ("__PPC405__");
  /* Used by libstdc++.  */
  if (TARGET_NO_LWSYNC)
    builtin_define ("__NO_LWSYNC__");

  if (TARGET_EXTRA_BUILTINS)
    {
      /* For the VSX builtin functions identical to Altivec functions, just map
	 the altivec builtin into the vsx version (the altivec functions
	 generate VSX code if -mvsx).  */
      builtin_define ("__builtin_vsx_xxland=__builtin_vec_and");
      builtin_define ("__builtin_vsx_xxlandc=__builtin_vec_andc");
      builtin_define ("__builtin_vsx_xxlnor=__builtin_vec_nor");
      builtin_define ("__builtin_vsx_xxlor=__builtin_vec_or");
      builtin_define ("__builtin_vsx_xxlxor=__builtin_vec_xor");
      builtin_define ("__builtin_vsx_xxsel=__builtin_vec_sel");
      builtin_define ("__builtin_vsx_vperm=__builtin_vec_perm");

      /* Also map the a and m versions of the multiply/add instructions to the
	 builtin for people blindly going off the instruction manual.  */
      builtin_define ("__builtin_vsx_xvmaddadp=__builtin_vsx_xvmadddp");
      builtin_define ("__builtin_vsx_xvmaddmdp=__builtin_vsx_xvmadddp");
      builtin_define ("__builtin_vsx_xvmaddasp=__builtin_vsx_xvmaddsp");
      builtin_define ("__builtin_vsx_xvmaddmsp=__builtin_vsx_xvmaddsp");
      builtin_define ("__builtin_vsx_xvmsubadp=__builtin_vsx_xvmsubdp");
      builtin_define ("__builtin_vsx_xvmsubmdp=__builtin_vsx_xvmsubdp");
      builtin_define ("__builtin_vsx_xvmsubasp=__builtin_vsx_xvmsubsp");
      builtin_define ("__builtin_vsx_xvmsubmsp=__builtin_vsx_xvmsubsp");
      builtin_define ("__builtin_vsx_xvnmaddadp=__builtin_vsx_xvnmadddp");
      builtin_define ("__builtin_vsx_xvnmaddmdp=__builtin_vsx_xvnmadddp");
      builtin_define ("__builtin_vsx_xvnmaddasp=__builtin_vsx_xvnmaddsp");
      builtin_define ("__builtin_vsx_xvnmaddmsp=__builtin_vsx_xvnmaddsp");
      builtin_define ("__builtin_vsx_xvnmsubadp=__builtin_vsx_xvnmsubdp");
      builtin_define ("__builtin_vsx_xvnmsubmdp=__builtin_vsx_xvnmsubdp");
      builtin_define ("__builtin_vsx_xvnmsubasp=__builtin_vsx_xvnmsubsp");
      builtin_define ("__builtin_vsx_xvnmsubmsp=__builtin_vsx_xvnmsubsp");
    }

  /* Map the old _Float128 'q' builtins into the new 'f128' builtins.  */
  if (TARGET_FLOAT128_TYPE)
    {
      builtin_define ("__builtin_fabsq=__builtin_fabsf128");
      builtin_define ("__builtin_copysignq=__builtin_copysignf128");
      builtin_define ("__builtin_nanq=__builtin_nanf128");
      builtin_define ("__builtin_nansq=__builtin_nansf128");
      builtin_define ("__builtin_infq=__builtin_inff128");
      builtin_define ("__builtin_huge_valq=__builtin_huge_valf128");
    }

  /* Tell users they can use __builtin_bswap{16,64}.  */
  builtin_define ("__HAVE_BSWAP__");

  /* May be overridden by target configuration.  */
  RS6000_CPU_CPP_ENDIAN_BUILTINS();

  if (TARGET_LONG_DOUBLE_128)
    {
      builtin_define ("__LONG_DOUBLE_128__");
      builtin_define ("__LONGDOUBLE128");

      if (TARGET_IEEEQUAD)
	{
	  /* Older versions of GLIBC used __attribute__((__KC__)) to create the
	     IEEE 128-bit floating point complex type for C++ (which does not
	     support _Float128 _Complex).  If the default for long double is
	     IEEE 128-bit mode, the library would need to use
	     __attribute__((__TC__)) instead.  Defining __KF__ and __KC__
	     is a stop-gap to build with the older libraries, until we
	     get an updated library.  */
	  builtin_define ("__LONG_DOUBLE_IEEE128__");
	  builtin_define ("__KF__=__TF__");
	  builtin_define ("__KC__=__TC__");
	}
      else
	builtin_define ("__LONG_DOUBLE_IBM128__");
    }

  switch (TARGET_CMODEL)
    {
      /* Deliberately omit __CMODEL_SMALL__ since that was the default
	 before --mcmodel support was added.  */
    case CMODEL_MEDIUM:
      builtin_define ("__CMODEL_MEDIUM__");
      break;
    case CMODEL_LARGE:
      builtin_define ("__CMODEL_LARGE__");
      break;
    default:
      break;
    }

  switch (rs6000_current_abi)
    {
    case ABI_V4:
      builtin_define ("_CALL_SYSV");
      break;
    case ABI_AIX:
      builtin_define ("_CALL_AIXDESC");
      builtin_define ("_CALL_AIX");
      builtin_define ("_CALL_ELF=1");
      break;
    case ABI_ELFv2:
      builtin_define ("_CALL_ELF=2");
      break;
    case ABI_DARWIN:
      builtin_define ("_CALL_DARWIN");
      break;
    default:
      break;
    }

  /* Vector element order.  */
  if (BYTES_BIG_ENDIAN)
    builtin_define ("__VEC_ELEMENT_REG_ORDER__=__ORDER_BIG_ENDIAN__");
  else
    builtin_define ("__VEC_ELEMENT_REG_ORDER__=__ORDER_LITTLE_ENDIAN__");

  /* Let the compiled code know if 'f' class registers will not be available.  */
  if (TARGET_SOFT_FLOAT)
    builtin_define ("__NO_FPRS__");

  /* Whether aggregates passed by value are aligned to a 16 byte boundary
     if their alignment is 16 bytes or larger.  */
  if ((TARGET_MACHO && rs6000_darwin64_abi)
      || DEFAULT_ABI == ABI_ELFv2
      || (DEFAULT_ABI == ABI_AIX && !rs6000_compat_align_parm))
    builtin_define ("__STRUCT_PARM_ALIGN__=16");
}
////

////
<gcc/config/rs6000/freebsd.h> (14.2.0)
#define FBSD_TARGET_CPU_CPP_BUILTINS()			\
  do							\
    {							\
      builtin_define ("__PPC__");			\
      builtin_define ("__ppc__");			\
      builtin_define ("__powerpc__");			\
      if (TARGET_64BIT)					\
	{						\
	  builtin_define ("__arch64__");		\
	  builtin_define ("__LP64__");			\
	  builtin_define ("__PPC64__");			\
	  builtin_define ("__powerpc64__");		\
	  builtin_assert ("cpu=powerpc64");		\
	  builtin_assert ("machine=powerpc64");		\
	}						\
      else						\
	{						\
	  builtin_define_std ("PPC");			\
	  builtin_define_std ("powerpc");		\
	  builtin_assert ("cpu=powerpc");		\
	  builtin_assert ("machine=powerpc");		\
	  TARGET_OS_SYSV_CPP_BUILTINS ();		\
	}						\
    }							\
  while (0)

#define RS6000_CPU_CPP_ENDIAN_BUILTINS()	\
  do						\
    {						\
      if (BYTES_BIG_ENDIAN)			\
	{					\
	  builtin_define ("__BIG_ENDIAN__");	\
	  builtin_define ("_BIG_ENDIAN");	\
	  builtin_assert ("machine=bigendian");	\
	}					\
      else					\
	{					\
	  builtin_define ("__LITTLE_ENDIAN__");	\
	  builtin_define ("_LITTLE_ENDIAN");	\
	  builtin_assert ("machine=littleendian"); \
	}					\
    }						\
  while (0)
--->