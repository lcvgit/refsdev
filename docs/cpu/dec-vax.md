# DEC VAX

## Identification

`vax`
`__vax__`

: Identifies the target architecture as the DEC VAX.

## References

<!---
<gcc/config/vax/vax.h> (3.1.0)

  #define CPP_PREDEFINES "-Dvax -D__vax__ -Dunix -Asystem=unix -Asystem=bsd -Acpu=vax -Amachine=vax"

  #define	CPP_SPEC "%{mg:%{!ansi:-DGFLOAT} -D__GFLOAT}"


<gcc/config/vax/vax.h> (14.2.0)

  #define TARGET_CPU_CPP_BUILTINS()		\
    do						\
      {						\
        builtin_define ("__vax__");		\
        builtin_assert ("cpu=vax");		\
        builtin_assert ("machine=vax");		\
        if (TARGET_G_FLOAT)			\
    {					\
      builtin_define ("__GFLOAT");		\
      builtin_define ("__GFLOAT__");	\
    }					\
      }						\
    while (0)
--->