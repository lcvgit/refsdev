# SPARC

## Identification

`sparc`
`__sparc`
`__sparc__`

: Identifies the target architecture as SPARC.

`SPARC`
`__SPARC__`

: Identifies the target architecture as SPARC.

`__sparc64__`

: Identifies the target architecture as SPARC.

`__sparcv9`

: Identifies the target architecture as SPARC.

`__sparc_v9__`

: Identifies the target architecture as SPARC.

## References

<!---
Type|Macro|Description
---|---|---
Identification|`__sparc__`|Defined by GNU C
Identification|`__sparc`|Defined by Sun Studio
Version|`__sparc_v8__`<br/>`__sparc_v9__`|Defined by GNU C
Version|`__sparcv8`<br/>`__sparcv9`|Defined by Sun Studio

##### Example #####

CPU|Sun Studio Macro|GNU C Macro
---|---|---
SPARC v8 (SuperSPARC)|`__sparcv8`|`__sparc_v8__`
SPARC v9 (UltraSPARC)|`__sparcv9`|`__sparc_v9__`


#if TARGET_CPU_DEFAULT == TARGET_CPU_v9
/* ??? What does Sun's CC pass?  */
#define CPP_CPU64_DEFAULT_SPEC "-D__sparc_v9__"
/* ??? It's not clear how other assemblers will handle this, so by default
   use GAS.  Sun's Solaris assembler recognizes -xarch=v8plus, but this case
   is handled in sol2.h.  */
#define ASM_CPU64_DEFAULT_SPEC "-Av9"
#endif
#if TARGET_CPU_DEFAULT == TARGET_CPU_ultrasparc
#define CPP_CPU64_DEFAULT_SPEC "-D__sparc_v9__"
#define ASM_CPU64_DEFAULT_SPEC "-Av9a"
#endif

#if TARGET_CPU_DEFAULT == TARGET_CPU_sparclet
#define CPP_CPU32_DEFAULT_SPEC "-D__sparclet__"
#define ASM_CPU32_DEFAULT_SPEC "-Asparclet"
#endif

#if TARGET_CPU_DEFAULT == TARGET_CPU_sparclite
#define CPP_CPU32_DEFAULT_SPEC "-D__sparclite__"
#define ASM_CPU32_DEFAULT_SPEC "-Asparclite"
#endif

#if TARGET_CPU_DEFAULT == TARGET_CPU_supersparc
#define CPP_CPU32_DEFAULT_SPEC "-D__supersparc__ -D__sparc_v8__"
#define ASM_CPU32_DEFAULT_SPEC ""
#endif

#if TARGET_CPU_DEFAULT == TARGET_CPU_hypersparc
#define CPP_CPU32_DEFAULT_SPEC "-D__hypersparc__ -D__sparc_v8__"
#define ASM_CPU32_DEFAULT_SPEC ""
#endif

#if TARGET_CPU_DEFAULT == TARGET_CPU_sparclite86x
#define CPP_CPU32_DEFAULT_SPEC "-D__sparclite86x__"
#define ASM_CPU32_DEFAULT_SPEC "-Asparclite"
#endif

#ifdef SPARC_BI_ARCH

#define CPP_ARCH32_SPEC "-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int \
-D__GCC_NEW_VARARGS__ -Acpu=sparc -Amachine=sparc"
#define CPP_ARCH64_SPEC "-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int \
-D__arch64__ -Acpu=sparc64 -Amachine=sparc64"

#else

#define CPP_ARCH32_SPEC "-D__GCC_NEW_VARARGS__ -Acpu=sparc -Amachine=sparc"
#define CPP_ARCH64_SPEC "-D__arch64__ -Acpu=sparc64 -Amachine=sparc64"

#endif

#define CPP_ARCH_DEFAULT_SPEC \
(DEFAULT_ARCH32_P ? CPP_ARCH32_SPEC : CPP_ARCH64_SPEC)

#define CPP_ARCH_SPEC "\
%{m32:%(cpp_arch32)} \
%{m64:%(cpp_arch64)} \
%{!m32:%{!m64:%(cpp_arch_default)}} \
"

/* Macros to distinguish endianness.  */
#define CPP_ENDIAN_SPEC "\
%{mlittle-endian:-D__LITTLE_ENDIAN__} \
%{mlittle-endian-data:-D__LITTLE_ENDIAN_DATA__}"
////


////
aout
  #define CPP_PREDEFINES "-Dsparc -Acpu=sparc -Amachine=sparc"

elf
  #define CPP_PREDEFINES "-Dsparc -D__elf__"

freebsd
  #undef  CPP_CPU64_DEFAULT_SPEC
  #define CPP_CPU64_DEFAULT_SPEC "-D__sparc64__ -D__sparc_v9__"

  #undef  CPP_PREDEFINES
  #define CPP_PREDEFINES FBSD_CPP_PREDEFINES

linux-aout
  #define CPP_PREDEFINES "-Dunix -Dsparc -D__gnu_linux__ -Dlinux -Asystem=unix -Asystem=posix"

linux
  #define CPP_PREDEFINES "-D__ELF__ -Dunix -D__sparc__ -D__gnu_linux__ -Dlinux -Asystem=unix -Asystem=posix"

linux64
  #define CPP_PREDEFINES "-D__ELF__ -Dunix -D_LONGLONG -D__sparc__ -D__gnu_linux__ -Dlinux -Asystem=unix -Asystem=posix"

lite
  #define CPP_PREDEFINES "-Dsparc -Dsparclite -Acpu=sparc -Amachine=sparc"

litecoff
  #define CPP_PREDEFINES "-Dsparc -Dsparclite -Acpu=sparc -Amachine=sparc"

liteelf
  #define CPP_PREDEFINES "-D__sparc__ -D__sparclite__ -Acpu=sparc -Amachine=sparc"

lynx-ng
  #define CPP_PREDEFINES "-Dunix -Dsparc -DLynx -DIBITS32 -Asystem=unix -Asystem=lynx -Acpu=sparc -Amachine=sparc"

lynx
  #define CPP_PREDEFINES "-Dunix -Dsparc -DSPARC -DLynx -DLYNX -DIBITS32 -Asystem=unix -Asystem=lynx -Acpu=sparc -Amachine=sparc"

netbsd-elf
  #define CPP_PREDEFINES "-D__sparc__ -D__NetBSD__ -D__ELF__ \
  -Asystem=unix -Asystem=NetBSD"

netbsd
  #define CPP_PREDEFINES "-Dunix -Dsparc -D__NetBSD__ -Asystem=unix -Asystem=NetBSD -Acpu=sparc -Amachine=sparc"

openbsd
  #define CPP_PREDEFINES "-D__unix__ -D__sparc__ -D__OpenBSD__ -Asystem=unix -Asystem=OpenBSD -Acpu=sparc -Amachine=sparc"

pbd
  #define CPP_PREDEFINES "-Dsparc -DUnicomPBD -Dunix -D__GCC_NEW_VARARGS__ -Asystem=unix -Acpu=sparc -Amachine=sparc"

rtems
  #define CPP_PREDEFINES "-Dsparc -D__GCC_NEW_VARARGS__ -D__rtems__ \
  -Asystem=rtems"

rtemself
  #define CPP_PREDEFINES "-Dsparc -D__GCC_NEW_VARARGS__ -D__rtems__ \
  -D__USE_INIT_FINI__ -Asystem=rtems"

sol2
  #define CPP_PREDEFINES \
  "-Dsparc -Dsun -Dunix -D__svr4__ -D__SVR4 -D__PRAGMA_REDEFINE_EXTNAME \
  -Asystem=unix -Asystem=svr4"

  #undef CPP_SUBTARGET_SPEC
  #define CPP_SUBTARGET_SPEC "\
  %{pthreads:-D_REENTRANT -D_PTHREADS} \
  %{!pthreads:%{threads:-D_REENTRANT -D_SOLARIS_THREADS}} \
  %{compat-bsd:-iwithprefixbefore ucbinclude -I/usr/ucbinclude} \
  "

  /* For C++ we need to add some additional macro definitions required
    by the C++ standard library.  */
  #define CPLUSPLUS_CPP_SPEC "\
  -D_XOPEN_SOURCE=500 -D_LARGEFILE_SOURCE=1 -D_LARGEFILE64_SOURCE=1 \
  -D__EXTENSIONS__ \
  %(cpp) \

sp64-elf
  #define CPP_PREDEFINES "-Dsparc -D__ELF__ -Acpu=sparc -Amachine=sparc"

sp86x-aout
  #define CPP_PREDEFINES "-D__sparc__ -D__sparclite86x__ -Acpu=sparc -Amachine=sparc"

sp86x-elf
  #define CPP_PREDEFINES "-D__sparc__ -D__sparclite86x__ -Acpu=sparc -Amachine=sparc"

splet
  #define CPP_PREDEFINES "-Dsparc -Acpu=sparc -Amachine=sparc" 

sun4o3
  #define CPP_PREDEFINES "-Dsparc -Dsun -Dunix -Asystem=unix -Asystem=bsd"

sunos4
  #define CPP_PREDEFINES "-Dsparc -Dsun -Dunix -Asystem=unix -Asystem=bsd"

sysv4
  #define CPP_PREDEFINES \
  "-Dsparc -Dunix -D__svr4__ -Asystem=unix -Asystem=svr4"

vxsim
  #define CPP_PREDEFINES \
  "-DCPU=SIMSPARCSOLARIS -D__vxworks -D__vxworks__ -Dsparc -D__svr4__ -D__SVR4 \
    -Asystem=embedded -Asystem=svr4 -Acpu=sparc -Amachine=sparc\
    -D__GCC_NEW_VARARGS__"

vxsparc
  #define CPP_PREDEFINES "-Dsparc -Acpu=sparc -Amachine=sparc"

vxsparc64
  #define CPP_PREDEFINES "-D__vxworks -D__sparc__ -Dsparc -D__GCC_NEW_VARARGS__"

////



////
<gcc/config/sparc/freebsd.h> (14.2.0)

  #define FBSD_TARGET_CPU_CPP_BUILTINS()		\
    do						\
      {						\
        builtin_define ("__sparc64__");		\
        builtin_define ("__sparc__");		\
        builtin_define ("__sparc_v9__");		\
        builtin_define ("__sparcv9");		\
      }						\
    while (0)

<gcc/config/sparc/sparc-c.cc> (14.2.0)

  void
  sparc_target_macros (void)
  {
    builtin_define_std ("sparc");

    if (TARGET_ARCH64)
      {
        cpp_assert (parse_in, "cpu=sparc64");
        cpp_assert (parse_in, "machine=sparc64");
      }
    else
      {
        cpp_assert (parse_in, "cpu=sparc");
        cpp_assert (parse_in, "machine=sparc");
      }

    if (TARGET_VIS4B)
      {
        cpp_define (parse_in, "__VIS__=0x410");
        cpp_define (parse_in, "__VIS=0x410");
      }
    else if (TARGET_VIS4)
      {
        cpp_define (parse_in, "__VIS__=0x400");
        cpp_define (parse_in, "__VIS=0x400");
      }
    else if (TARGET_VIS3)
      {
        cpp_define (parse_in, "__VIS__=0x300");
        cpp_define (parse_in, "__VIS=0x300");
      }
    else if (TARGET_VIS2)
      {
        cpp_define (parse_in, "__VIS__=0x200");
        cpp_define (parse_in, "__VIS=0x200");
      }
    else if (TARGET_VIS)
      {
        cpp_define (parse_in, "__VIS__=0x100");
        cpp_define (parse_in, "__VIS=0x100");
      }
  }
--->