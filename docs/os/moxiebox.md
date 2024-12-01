# moxiebox Environment

## Identification

`__moxiebox__`

:   Identifies the target environment as moxiebox.

## References

<!---
<gcc/config/moxie/moxiebox.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()		\
    do						\
      {						\
        builtin_define_std ("moxie");		\
        builtin_define ("__moxiebox__");		\
        builtin_assert ("system=moxiebox");	\
      }						\
    while (0)
--->