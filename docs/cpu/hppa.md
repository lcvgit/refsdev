# HP/PA RISC

<!---
Type 	Macro 	Description
Identification 	__hppa__ 	Defined by GNU C
Identification 	__HPPA__ 	Defined by Stratus VOS C
Identification 	__hppa 	

Version 	_PA_RISC'V'_'R' 	V = Version
                            R = Revision

CPU 	Macro
PA RISC 1.0 	_PA_RISC1_0
PA RISC 1.1 	_PA_RISC1_1
              __HPPA11__
              __PA7100__
PA RISC 2.0 	_PA_RISC2_0
              __RISC2_0__
              __HPPA20__
              __PA8000__

#define CPP_PA10_SPEC ""
#define CPP_PA11_SPEC "-D_PA_RISC1_1 -D__hp9000s700"
#define CPP_PA20_SPEC "-D_PA_RISC2_0 -D__hp9000s800"
#define CPP_64BIT_SPEC "-D__LP64__ -D__LONG_MAX__=9223372036854775807L"

#define CPP_SPEC "\
%{mpa-risc-1-0:%(cpp_pa10)} \
%{mpa-risc-1-1:%(cpp_pa11)} \
%{msnake:%(cpp_pa11)} \
%{mpa-risc-2-0:%(cpp_pa20)} \
%{!mpa-risc-1-0:%{!mpa-risc-1-1:%{!mpa-risc-2-0:%{!msnake:%(cpp_cpu_default)}}}} \
%{m64bit:%(cpp_64bit)} \
%{!m64bit:%(cpp_64bit_default)} \
%{!ansi: -D_HPUX_SOURCE -D_HIUX_SOURCE -D__STDC_EXT__ -D_INCLUDE_LONGLONG} \
%{threads: -D_REENTRANT -D_DCE_THREADS}"

#define CPLUSPLUS_CPP_SPEC "\
-D_HPUX_SOURCE -D_HIUX_SOURCE -D__STDC_EXT__ -D_INCLUDE_LONGLONG \
%{mpa-risc-1-0:%(cpp_pa10)} \
%{mpa-risc-1-1:%(cpp_pa11)} \
%{msnake:%(cpp_pa11)} \
%{mpa-risc-2-0:%(cpp_pa20)} \
%{!mpa-risc-1-0:%{!mpa-risc-1-1:%{!mpa-risc-2-0:%{!msnake:%(cpp_cpu_default)}}}} \
%{m64bit:%(cpp_64bit)} \
%{!m64bit:%(cpp_64bit_default)} \
%{threads: -D_REENTRANT -D_DCE_THREADS}"

#define CPP_PREDEFINES "-Dhppa -Dhp9000s800 -D__hp9000s800 -Dhp9k8 -Dunix -Dhp9000 -Dhp800 -Dspectrum -DREVARGV -Asystem=unix -Asystem=bsd -Acpu=hppa -Amachine=hppa"

<gcc/config/pa/pa.h> (14.2.0)

  #define TARGET_CPU_CPP_BUILTINS()				\
  do {								\
      builtin_assert("cpu=hppa");				\
      builtin_assert("machine=hppa");				\
      builtin_define("__hppa");					\
      builtin_define("__hppa__");				\
      builtin_define("__BIG_ENDIAN__");				\
      if (TARGET_PA_20)						\
        builtin_define("_PA_RISC2_0");				\
      else if (TARGET_PA_11)					\
        builtin_define("_PA_RISC1_1");				\
      else							\
        builtin_define("_PA_RISC1_0");				\
      if (HPUX_LONG_DOUBLE_LIBRARY)				\
        builtin_define("__SIZEOF_FLOAT128__=16");		\
      if (TARGET_SOFT_FLOAT)					\
        builtin_define("__SOFTFP__");				\
  } while (0)

  ...

  #define TARGET_OS_CPP_BUILTINS()				\
    do								\
      {								\
    builtin_define_std ("REVARGV");				\
    builtin_define_std ("hp800");				\
    builtin_define_std ("hp9000");				\
    builtin_define_std ("hp9k8");				\
    if (!c_dialect_cxx () && !flag_iso)			\
      builtin_define ("hppa");				\
    builtin_define_std ("spectrum");			\
    builtin_define_std ("unix");				\
    builtin_assert ("system=bsd");				\
    builtin_assert ("system=unix");				\
      }								\
    while (0)
--->