# RX

## Identification

`__RX__`

: Identifies the target architecture as RX.

## References

<!---
<gcc/config/rx/rx.h> (14.2.0)

  #define TARGET_CPU_CPP_BUILTINS()               \
    do                                            \
      {                                           \
        builtin_define ("__RX__"); 		\
        builtin_assert ("cpu=RX"); 		\
        if (rx_cpu_type == RX610)			\
    {					\
            builtin_define ("__RX610__");		\
            builtin_assert ("machine=RX610");	\
    }					\
        else if (rx_cpu_type == RX100)		\
    {					\
            builtin_define ("__RX100__");		\
            builtin_assert ("machine=RX100");	\
    }					\
        else if (rx_cpu_type == RX200)		\
    {					\
            builtin_define ("__RX200__");		\
            builtin_assert ("machine=RX200");	\
          }					\
        else if (rx_cpu_type == RX600)		\
          {					\
            builtin_define ("__RX600__");		\
            builtin_assert ("machine=RX600");	\
          }					\
              \
        if (TARGET_BIG_ENDIAN_DATA)		\
    builtin_define ("__RX_BIG_ENDIAN__");	\
        else					\
    builtin_define ("__RX_LITTLE_ENDIAN__");\
                    \
        if (TARGET_64BIT_DOUBLES)			\
    builtin_define ("__RX_64BIT_DOUBLES__");\
        else					\
    builtin_define ("__RX_32BIT_DOUBLES__");\
                    \
        if (ALLOW_RX_FPU_INSNS)			\
    builtin_define ("__RX_FPU_INSNS__");	\
              \
        if (TARGET_AS100_SYNTAX)			\
    builtin_define ("__RX_AS100_SYNTAX__"); \
        else					\
    builtin_define ("__RX_GAS_SYNTAX__");   \
              \
        if (TARGET_GCC_ABI)			\
    builtin_define ("__RX_GCC_ABI__");	\
        else					\
    builtin_define ("__RX_ABI__");		\
              \
        if (rx_allow_string_insns)		\
    builtin_define ("__RX_ALLOW_STRING_INSNS__"); \
        else					\
    builtin_define ("__RX_DISALLOW_STRING_INSNS__");\
      }                                           \
    while (0)


<gcc/config/rx/linux.h> (14.2.0)

  #define TARGET_CPU_CPP_BUILTINS()               \
    do                                            \
      {                                           \
        builtin_define ("__RX__"); 		\
        builtin_assert ("cpu=RX"); 		\
        if (rx_cpu_type == RX610)			\
          builtin_assert ("machine=RX610");	\
      else					\
          builtin_assert ("machine=RX600");	\
                    \
        if (TARGET_BIG_ENDIAN_DATA)		\
    builtin_define ("__RX_BIG_ENDIAN__");	\
        else					\
    builtin_define ("__RX_LITTLE_ENDIAN__");\
              \
        if (TARGET_64BIT_DOUBLES)			\
    builtin_define ("__RX_64BIT_DOUBLES__");\
        else					\
    builtin_define ("__RX_32BIT_DOUBLES__");\
                    \
        if (ALLOW_RX_FPU_INSNS)			\
    builtin_define ("__RX_FPU_INSNS__");	\
              \
      }                                           \
    while (0)
--->