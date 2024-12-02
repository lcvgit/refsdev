# SVR4 Environment

## Identification

`__sysv__`
`__svr4__`
`__SVR4`
`_SYSTYPE_SVR4`

## References

- <http://en.wikipedia.org/wiki/UNIX_System_V>{:target="_blank"}

<!----
<gcc/config/rs6000/sysv4.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()		\
    do						\
      {						\
        builtin_define_std ("PPC");		\
        builtin_define_std ("unix");		\
        builtin_define ("__svr4__");		\
        builtin_assert ("system=unix");		\
        builtin_assert ("system=svr4");		\
        builtin_assert ("cpu=powerpc");		\
        builtin_assert ("machine=powerpc");	\
        TARGET_OS_SYSV_CPP_BUILTINS ();		\
      }						\
    while (0)
--->