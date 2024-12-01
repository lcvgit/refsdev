# MinGW Environment

## Identification

`__MINGW32__`

:   Identifies the environment as MinGW.

## References

<!---
<gcc/config/i386/mingw.h>

  #define EXTRA_OS_CPP_BUILTINS()					\
    do								\
      {								\
        builtin_define ("__MSVCRT__");				\
        builtin_define ("__MINGW32__");			   	\
        builtin_define ("_WIN32");				\
        builtin_define_std ("WIN32");				\
        builtin_define_std ("WINNT");				\
        builtin_define_with_int_value ("_INTEGRAL_MAX_BITS",	\
              TYPE_PRECISION (intmax_type_node));\
        if (TARGET_64BIT && ix86_abi == MS_ABI)			\
    {							\
      builtin_define ("__MINGW64__");			\
      builtin_define_std ("WIN64");				\
      builtin_define ("_WIN64");				\
    }							\
        if (TARGET_USING_MCFGTHREAD)				\
    builtin_define ("__USING_MCFGTHREAD__");		\
      }								\
    while (0)
--->