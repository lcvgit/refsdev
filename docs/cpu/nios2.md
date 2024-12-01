# NIOS II

<!---
<gcc/config/nios2/nios2.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()                   \
  do                                                \
    {                                               \
      builtin_define_std ("NIOS2");                 \
      builtin_define_std ("nios2");                 \
      if (TARGET_BIG_ENDIAN)                        \
        builtin_define_std ("nios2_big_endian");    \
      else                                          \
        builtin_define_std ("nios2_little_endian"); \
      builtin_define_with_int_value (		    \
        "__nios2_arch__", (int) nios2_arch_option); \
    }						    \
  while (0)
--->