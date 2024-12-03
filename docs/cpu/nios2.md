---
tags:
  - Nios 2
  - Nios II
---
# NIOS II

## Identification

`nios2`
`__nios2`
`__nios2__`

: Identifies the target architecture as the Nios II.

`NIOS2`
`__NIOS2`
`__NIOS2__`

: Identifies the target architecture as the Nios II.

## References

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