---
tags:
  - picoJava
  - PJ
---
# picoJava

## Identification

`__pj__`

: Identifies the target architecture as PJ.

## References

- <https://en.wikipedia.org/wiki/PicoJava>{:target="_blank"}

<!---
#ifdef TARGET_LITTLE_ENDIAN_DEFAULT
#define CPP_SPEC        "%{mb:-D__BIG_ENDIAN__ }%{!mb:-D__LITTLE_ENDIAN__ }" 
#define ASM_SPEC        "%{mb:-EB }%{!mb:-EL }"
#else
#define CPP_SPEC        "%{ml:-D__LITTLE_ENDIAN__ }%{!ml:-D__BIG_ENDIAN__}"
#define ASM_SPEC        "%{ml:-EL } %{!ml:-EB }"
#endif

#ifndef CPP_PREDEFINES
#define CPP_PREDEFINES "-D__ELF__ -D__pj__ -Asystem=posix"
#endif
--->