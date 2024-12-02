# Phoenix RTOS

## Identification

`phoenix`
`__phoenix`
`__phoenix__`

:   Identifies the target operating system as Phoenix RTOS.

## References

<!---
<gcc/config/phoenix.h> (14.2.0)

#define TARGET_OS_CPP_BUILTINS()           \
    do {                                   \
      builtin_define_std ("phoenix");      \
      builtin_define_std ("unix");         \
      builtin_assert ("system=phoenix");   \
      builtin_assert ("system=unix");      \
    } while (0)
--->
