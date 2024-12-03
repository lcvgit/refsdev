# Xtensa

## Identification

`__XTENSA__`

: Identifies the target architecture as Xtensa.

## References

<!---
elf
  #define CPP_PREDEFINES "-D__XTENSA__ -D__ELF__ -Acpu=xtensa -Amachine=xtensa"
linux
  #define CPP_PREDEFINES \
  "-D__XTENSA__ -D__ELF__ -Acpu=xtensa -Amachine=xtensa \
    -Dunix -D__gnu_linux__ -Dlinux -Asystem=posix"
////

////
#if XCHAL_HAVE_BE
#define CPP_ENDIAN_SPEC "\
  %{mlittle-endian:-D__XTENSA_EL__} \
  %{!mlittle-endian:-D__XTENSA_EB__} "
#else /* !XCHAL_HAVE_BE */
#define CPP_ENDIAN_SPEC "\
  %{mbig-endian:-D__XTENSA_EB__} \
  %{!mbig-endian:-D__XTENSA_EL__} "
#endif /* !XCHAL_HAVE_BE */

#if XCHAL_HAVE_FP
#define CPP_FLOAT_SPEC "%{msoft-float:-D__XTENSA_SOFT_FLOAT__}"
#else
#define CPP_FLOAT_SPEC "%{!mhard-float:-D__XTENSA_SOFT_FLOAT__}"
#endif
////

////
<gcc/config/xtensa/xtensa.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()					\
  do {									\
    const char **builtin;						\
    builtin_assert ("cpu=xtensa");					\
    builtin_assert ("machine=xtensa");					\
    builtin_define ("__xtensa__");					\
    builtin_define ("__XTENSA__");					\
    builtin_define (TARGET_WINDOWED_ABI ?				\
		    "__XTENSA_WINDOWED_ABI__" : "__XTENSA_CALL0_ABI__");\
    builtin_define (TARGET_BIG_ENDIAN ? "__XTENSA_EB__" : "__XTENSA_EL__"); \
    if (!TARGET_HARD_FLOAT)						\
      builtin_define ("__XTENSA_SOFT_FLOAT__");				\
    for (builtin = xtensa_get_config_strings (); *builtin; ++builtin)	\
      builtin_define (*builtin);					\
  } while (0)
--->