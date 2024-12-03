# MMIX

`__mmix__`

: Identifies the target architecture as MMIX.

`__MMIX__`

: Identifies the target architecture as MMIX.

## References

<!---
#define CPP_SPEC \
 "%{mabi=gnu:-D__MMIX_ABI_GNU__\
    %{mabi=mmixware:\
      %eoptions -mabi=mmixware and -mabi=gnu are mutually exclusive}}\
  %{!mabi=gnu:-D__MMIX_ABI_MMIXWARE__}"

/* Define __LONG_MAX__, since we're advised not to change glimits.h.  */
#define CPP_PREDEFINES "-D__mmix__ -D__MMIX__ -D__LONG_MAX__=9223372036854775807L"
////


////
<gcc/config/mmix/mmix.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()				\
  do								\
    {								\
      builtin_define ("__mmix__");				\
      builtin_define ("__MMIX__");				\
      if (TARGET_ABI_GNU)					\
	builtin_define ("__MMIX_ABI_GNU__");			\
      else							\
	builtin_define ("__MMIX_ABI_MMIXWARE__");		\
    }								\
  while (0)
--->