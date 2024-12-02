# SDE MTK

<!----
<gcc/config/mips/sdemtk.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()			\
    do							\
      {							\
        builtin_assert ("system=sde");			\
        builtin_assert ("system=posix");			\
        builtin_define ("__SDE_MIPS__");			\
                \
        /* Deprecated: use __mips_isa_rev >= 2.  */	\
        if (ISA_MIPS32R2)					\
          builtin_define ("__mipsr2");			\
                \
        /* Deprecated: use __mips_fpr == 64.  */		\
        if (TARGET_FLOAT64)				\
    builtin_define ("__mipsfp64");			\
                \
        if (TARGET_NO_FLOAT) 				\
    builtin_define ("__NO_FLOAT");			\
        else if (TARGET_SOFT_FLOAT_ABI)			\
    builtin_define ("__SOFT_FLOAT");		\
        else if (TARGET_SINGLE_FLOAT)			\
    builtin_define ("__SINGLE_FLOAT");		\
                \
        if (TARGET_BIG_ENDIAN)				\
          {						\
      builtin_assert ("endian=big");		\
      builtin_assert ("cpu=mipseb");		\
    }						\
        else						\
          {						\
      builtin_assert ("endian=little");		\
      builtin_assert ("cpu=mipsel");		\
    }						\
      }							\
    while (0)
--->