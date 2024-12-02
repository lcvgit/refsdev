# VxWorks

## Identification

`__vxworks`

:   Identifies the target operating system as VxWorks.

`__VXWORKS__`

:   Identifies the target operating system as VxWorks.

## Versioning

`_WRS_VXWORKS_MAJOR`

:   An integer for the major version of VxWorks.

`_WRS_VXWORKS_MINOR`

:   An integer for the minor version of VxWorks.

`_WRS_VXWORKS_MAINT`

:   An integer for the patch version of VxWorks.

## References

- <http://en.wikipedia.org/wiki/VxWorks>{:target="_blank"}

<!---
<gcc/config/vxworks.h> (14.2.0)

  #define VXWORKS_OS_CPP_BUILTINS()					\
    do									\
      {									\
        builtin_define ("__vxworks");					\
        builtin_define ("__VXWORKS__");					\
        builtin_assert ("system=unix");					\
        if (TARGET_VXWORKS_RTP)						\
    builtin_define ("__RTP__");					\
        else								\
    builtin_define ("_WRS_KERNEL");					\
        builtin_define ("TOOL_FAMILY=" VXWORKS_PERSONALITY);		\
        builtin_define ("TOOL=" VXWORKS_PERSONALITY);			\
        if (TARGET_VXWORKS7)						\
          {								\
            builtin_define ("_VSB_CONFIG_FILE=<config/vsbConfig.h>");	\
                            \
      /* _ALLOW_KEYWORD_MACROS is needed on VxWorks 7 to		\
          prevent compilation failures triggered by our		\
          definition of "inline" in ansidecl when "inline"		\
          is not a keyword.  */					\
      if (!flag_isoc99 && !c_dialect_cxx())			\
              builtin_define ("_ALLOW_KEYWORD_MACROS");			\
          }								\
        /* C++ support relies on C99 features from C++11, even C++98	\
          for listdc++ in particular, with corresponding checks at	\
          configure time.  Make sure C99 features are exposed by the	\
          system headers.  */						\
        if (c_dialect_cxx())						\
          builtin_define("_C99");						\
      }									\
    while (0)

<gcc/config/vxworksae.h> (14.2.0)

  /* A VxWorks 653 implementation of TARGET_OS_CPP_BUILTINS.  */
  #define VXWORKS_OS_CPP_BUILTINS()                                       \
    do                                                                    \
      {                                                                   \
        builtin_define ("__vxworks");                                     \
        builtin_define ("__VXWORKS__");                                   \
      }                                                                   \
    while (0)

<gcc/config/mips/vxworks.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()                        \
    do                                                    \
      {                                                   \
        if (TARGET_64BIT)					\
    builtin_define ("CPU=MIPS64");			\
        else						\
    builtin_define ("CPU=MIPS32");			\
        if (TARGET_BIG_ENDIAN)				\
    builtin_define ("MIPSEB");			\
        else						\
    builtin_define ("MIPSEL");			\
        if (TARGET_SOFT_FLOAT)				\
    builtin_define ("SOFT_FLOAT");			\
        VXWORKS_OS_CPP_BUILTINS ();			\
      }                                                   \
    while (0)

<gcc/config/rs6000/vxworks.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()		\
    do						\
      {						\
        builtin_define ("__ELF__");		\
        if (!TARGET_VXWORKS7)			\
    builtin_define ("__EABI__");		\
              \
        /* CPU macros, based on what the system compilers do.  */	\
        if (!TARGET_VXWORKS7)			\
    {					\
      builtin_define ("__ppc");		\
      /* Namespace violation below, but the system headers \
        really depend heavily on this.  */	\
      builtin_define ("CPU_FAMILY=PPC");	\
              \
      /* __PPC__ isn't actually emitted by the system compiler \
        prior to vx7 but has been advertised by us for ages.  */	\
      builtin_define ("__PPC__");		\
    }					\
        else					\
    {					\
      builtin_define ("__PPC__");		\
      builtin_define ("__powerpc__");	\
      if (TARGET_64BIT)			\
        {					\
          builtin_define ("__PPC64__");	\
          builtin_define ("__powerpc64__");	\
        }					\
      else					\
        {					\
          builtin_define ("__PPC");		\
          builtin_define ("__powerpc");	\
        }					\
              \
      /* __ppc isn't emitted by the system compiler \
        any more but a few system headers still depend \
        on it, as well as on __ppc__.  */	\
      builtin_define ("__ppc");		\
      builtin_define ("__ppc__");		\
    }					\
              \
        /* Asserts for #cpu and #machine.  */	\
        if (TARGET_64BIT)				\
    {					\
      builtin_assert ("cpu=powerpc64");     \
      builtin_assert ("machine=powerpc64"); \
    }					\
        else 					\
    {					\
      builtin_assert ("cpu=powerpc");	\
      builtin_assert ("machine=powerpc");   \
    }					\
              \
        /* PowerPC VxWorks specificities.  */	\
        if (!TARGET_SOFT_FLOAT)			\
    {					\
      builtin_define ("__hardfp");		\
      builtin_define ("_WRS_HARDWARE_FP");  \
    }                                       \
              \
        /* Common VxWorks and port items.  */	\
        VXWORKS_OS_CPP_BUILTINS ();		\
        TARGET_OS_SYSV_CPP_BUILTINS ();		\
      }		\
    while (0)

<gcc/config/sh/vxworks.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()	\
    do					\
      {					\
        builtin_define ("CPU=SH7000");	\
        VXWORKS_OS_CPP_BUILTINS ();	\
      }					\
    while (0)
--->