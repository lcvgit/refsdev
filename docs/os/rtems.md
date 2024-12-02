# RTEMS

## Identification

`__rtems__`

:   Identifies the target operating system as RTEMS.

## References

<!---
<gcc/config/aarch64/rtems.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()		\
      do {					\
    builtin_define ("__rtems__");		\
    builtin_define ("__USE_INIT_FINI__");	\
    builtin_assert ("system=rtems");	\
      } while (0)


<gcc/config/moxie/rtems.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()		\
    do						\
      {						\
        builtin_define_std ("moxie");		\
        builtin_define ("__rtems__");		\
        builtin_assert ("system=rtems");		\
      }						\
    while (0)


<gcc/config/nios2/rtems.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()        \
  do {                                    \
    builtin_define ("__rtems__");         \
    builtin_define ("__USE_INIT_FINI__"); \
    builtin_assert ("system=rtems");      \
  } while (0)


<gcc/config/or1k/rtems.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()		\
    do						\
      {						\
    builtin_define ("__rtems__");		\
    builtin_define ("__USE_INIT_FINI__");	\
    builtin_assert ("system=rtems");	\
      }						\
    while (0)


<gcc/config/riscv/rtems.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()		\
      do {					\
    builtin_define ("__rtems__");		\
    builtin_define ("__USE_INIT_FINI__");	\
    builtin_assert ("system=rtems");	\
      } while (0)

<gcc/config/rs6000/rtems.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()			\
    do							\
      {							\
        builtin_define ("__rtems__");			\
        builtin_define ("__USE_INIT_FINI__");		\
        builtin_assert ("system=rtems");			\
        if (TARGET_64BIT)					\
    {						\
      builtin_define ("__PPC__");			\
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


<gcc/config/sh/rtems.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS() do {		\
    builtin_define( "__rtems__" );		\
    builtin_assert( "system=rtems" );		\
  } while (0)


<gcc/config/sh/rtemself.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS() do {		\
    builtin_define( "__rtems__" );		\
    builtin_assert( "system=rtems" );		\
  } while (0)


<gcc/config/sparc/rtemself.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()		\
    do						\
      {						\
    builtin_define ("__rtems__");		\
    builtin_define ("__USE_INIT_FINI__");	\
    builtin_assert ("system=rtems");	\
    if (sparc_fix_b2bst)			\
      builtin_define ("__FIX_LEON3FT_B2BST"); \
    if (sparc_fix_gr712rc || sparc_fix_ut700 || sparc_fix_ut699) \
      builtin_define ("__FIX_LEON3FT_TN0018"); \
      }						\
    while (0)


<gcc/config/v850/rtems.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()		\
    do						\
      {						\
        builtin_define( "__rtems__" );		\
        builtin_assert( "system=rtems" );		\
      }						\
    while (0)
--->