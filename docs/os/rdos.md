# RDOS

## Identification

`__RDOS__`

:   Identifies the target operating system as RDOS.

## References

<!---
<gcc/config/i386/rdos.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()		\
    do						\
      {						\
        builtin_define ("__RDOS__");		\
        builtin_assert ("system=rdos");		\
      }						\
    while (0)
--->