---
tags:
  - OR1K
  - OpenRISC 1000
  - OpenRISC 1K
---
# OpenRISC 1000

## Identification

`__or1k__`

: Identifies the target architecture as the OpenRISC 1000.

`__OR1K__`

: Identifies the target architecture as the OpenRISC 1000.

## References

<!---
<gcc/config/or1k/or1k.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()		\
  do						\
    {						\
      builtin_define ("__OR1K__");		\
      builtin_define ("__OR1K_DELAY__");	\
      builtin_define ("__or1k__");		\
      if (TARGET_CMOV)				\
	builtin_define ("__or1k_cmov__");	\
      if (TARGET_HARD_FLOAT)			\
	builtin_define ("__or1k_hard_float__");	\
      builtin_assert ("cpu=or1k");		\
      builtin_assert ("machine=or1k");		\
    }						\
  while (0)
--->