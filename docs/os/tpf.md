# TPF

## Identification

`tpf`
`__tpf`
`__tpf__`

:   Identifies the target operating system as TPF.

## References

- <https://en.wikipedia.org/wiki/Transaction_Processing_Facility>{:target="_blank"}

<!---
<gcc/config/s390/tpf.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()                \
    do                                            \
      {                                           \
        builtin_define_std ("tpf");               \
        builtin_assert ("system=tpf");            \
        builtin_define ("__ELF__");               \
      }                                           \
    while (0)
--->