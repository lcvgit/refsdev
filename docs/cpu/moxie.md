# Moxie

## Identification

`moxie`
`__moxie`
`__moxie__`

: Identifies the target architecture as Moxie.

`MOXIE`
`__MOXIE`
`__MOXIE__`

: Identifies the target architecture as Moxie.

## References

<!---
<gcc/config/moxie/moxie.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS() \
  { \
    builtin_define_std ("moxie");			\
    builtin_define_std ("MOXIE");			\
    if (TARGET_LITTLE_ENDIAN)				\
      builtin_define ("__MOXIE_LITTLE_ENDIAN__");	\
    else						\
      builtin_define ("__MOXIE_BIG_ENDIAN__");		\
  }
--->