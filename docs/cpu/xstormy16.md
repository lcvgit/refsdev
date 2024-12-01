# Xstormy16

<!---
<gcc/config/stormy16/stormy16.h> (3.1.0)

#define CPP_PREDEFINES "-Dxstormy16 -Amachine=xstormy16 -D__INT_MAX__=32767"
////

////
<gcc/config/stormy16/stormy16.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()		\
  do						\
    {						\
      builtin_define_std ("xstormy16");		\
      builtin_assert ("machine=xstormy16");	\
      builtin_assert ("cpu=xstormy16");		\
    }						\
  while (0)
--->