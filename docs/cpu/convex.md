# Convex

## Identification

`convex`
`__convex__`

:   Identifies the target machine/processor as Convex.

## Versioning

`__convex_c1__`

:   Indicates that the machine/processor belongs to the Convex C1 Family.

    GNU Compiler (3.1) -- Defined if the command line option `-mc1` is enabled.

    !!!bug
        
        A typo for the Convex C1 macro is found in GCC documentation however, the `<gcc/config/convex/convex.h>` header contains the correct spelling of `__convex_c1__`.

`__convex_c2__`

:   Indicates that the machine/processor belongs to the Convex C2 Family.

    GNU Compiler (3.1) -- Defined if the command line option `-mc2` is enabled.

`__convex_c32__`

:   Indicates that the machine/processor belongs to the Convex C32xx Family.

    GNU Compiler (3.1) -- Defined if the command line option `-mc32` is enabled.

`__convex_c34__`

:   Indicates that the machine/processor belongs to the Convex C34xx Family.

    GNU Compiler (3.1) -- Defined if the command line option `-mc34` is enabled.

`__convex_c38__`

:   Indicates that the machine/processor belongs to the Convex C38xx Family.

GNU Compiler (3.1) -- Defined if the command line option `-mc38` is enabled.

## References

- [Convex Computer - Wikipedia](https://en.wikipedia.org/wiki/Convex_Computer){:target="_blank"}
- [GCC 3.1 - Convex Options](https://gcc.gnu.org/onlinedocs/gcc-3.1/gcc/Convex-Options.html){:target="_blank"}

<!---
<gcc/config/convex/convex.h> (3.1)

#define CPP_PREDEFINES "-Dconvex -Dunix -Asystem=unix -Acpu=convex -Amachine=convex"

#if (TARGET_DEFAULT | TARGET_CPU_DEFAULT) & 1

/* C1 default */

#if _IEEE_FLOAT_

#define CPP_SPEC							\
"%{!mc2:%{!mc32:%{!mc34:%{!mc38:-D__convex_c1__}}}}			\
 %{mc2:-D__convex_c2__}							\
 %{mc32:-D__convex_c32__}						\
 %{mc34:-D__convex_c34__}						\
 %{mc38:-D__convex_c38__}						\
 %{fno-builtin:-D__NO_INLINE}						\
 -D__NO_INLINE_MATH -D__NO_INLINE_STDLIB				\
 -D_IEEE_FLOAT_								\
 %{.S:-P}								\
 %{!traditional:-D__stdc__}						\
 %{!traditional:-D_LONGLONG}						\
 %{!traditional:-Ds64_t=long\\ long -Du64_t=unsigned\\ long\\ long}	\
 %{!ansi:-D_POSIX_SOURCE}						\
 %{!ansi:-D_CONVEX_SOURCE}"

#else

#define CPP_SPEC							\
"%{!mc2:%{!mc32:%{!mc34:%{!mc38:-D__convex_c1__}}}}			\
 %{mc2:-D__convex_c2__}							\
 %{mc32:-D__convex_c32__}						\
 %{mc34:-D__convex_c34__}						\
 %{mc38:-D__convex_c38__}						\
 %{fno-builtin:-D__NO_INLINE}						\
 -D__NO_INLINE_MATH -D__NO_INLINE_STDLIB				\
 -D_CONVEX_FLOAT_							\
 %{.S:-P}								\
 %{!traditional:-D__stdc__}						\
 %{!traditional:-D_LONGLONG}						\
 %{!traditional:-Ds64_t=long\\ long -Du64_t=unsigned\\ long\\ long}	\
 %{!ansi:-D_POSIX_SOURCE}						\
 %{!ansi:-D_CONVEX_SOURCE}"

#endif

#define LIB_SPEC							\
"%{!mc2:%{!mc32:%{!mc34:%{!mc38:-lC1%{traditional:_old}%{p:_p}%{pg:_p}}}}} \
 %{mc2:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}				\
 %{mc32:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}				\
 %{mc34:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}				\
 %{mc38:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}				\
 -lc%{traditional:_old}%{p:_p}%{pg:_p}"

#endif

#if (TARGET_DEFAULT | TARGET_CPU_DEFAULT) & 2

/* C2 default */

#if _IEEE_FLOAT_

#define CPP_SPEC							\
"%{mc1:-D__convex_c1__}							\
 %{!mc1:%{!mc32:%{!mc34:%{!mc38:-D__convex_c2__}}}}			\
 %{mc32:-D__convex_c32__}						\
 %{mc34:-D__convex_c34__}						\
 %{mc38:-D__convex_c38__}						\
 %{fno-builtin:-D__NO_INLINE}						\
 -D__NO_INLINE_MATH -D__NO_INLINE_STDLIB				\
 -D_IEEE_FLOAT_								\
 %{.S:-P}								\
 %{!traditional:-D__stdc__}						\
 %{!traditional:-D_LONGLONG}						\
 %{!traditional:-Ds64_t=long\\ long -Du64_t=unsigned\\ long\\ long}	\
 %{!ansi:-D_POSIX_SOURCE}						\
 %{!ansi:-D_CONVEX_SOURCE}"

#else

#define CPP_SPEC							\
"%{mc1:-D__convex_c1__}							\
 %{!mc1:%{!mc32:%{!mc34:%{!mc38:-D__convex_c2__}}}}			\
 %{mc32:-D__convex_c32__}						\
 %{mc34:-D__convex_c34__}						\
 %{mc38:-D__convex_c38__}						\
 %{fno-builtin:-D__NO_INLINE}						\
 -D__NO_INLINE_MATH -D__NO_INLINE_STDLIB				\
 -D_CONVEX_FLOAT_							\
 %{.S:-P}								\
 %{!traditional:-D__stdc__}						\
 %{!traditional:-D_LONGLONG}						\
 %{!traditional:-Ds64_t=long\\ long -Du64_t=unsigned\\ long\\ long}	\
 %{!ansi:-D_POSIX_SOURCE}						\
 %{!ansi:-D_CONVEX_SOURCE}"

#endif

#define LIB_SPEC							\
"%{mc1:-lC1%{traditional:_old}%{p:_p}%{pg:_p}}				\
 %{!mc1:%{!mc32:%{!mc34:%{!mc38:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}}}} \
 %{mc32:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}				\
 %{mc34:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}				\
 %{mc38:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}				\
 -lc%{traditional:_old}%{p:_p}%{pg:_p}"

#endif

#if (TARGET_DEFAULT | TARGET_CPU_DEFAULT) & 4

/* C32 default */

#if _IEEE_FLOAT_

#define CPP_SPEC							\
"%{mc1:-D__convex_c1__}							\
 %{mc2:-D__convex_c2__}							\
 %{!mc1:%{!mc2:%{!mc34:%{!mc38:-D__convex_c32__}}}}			\
 %{mc34:-D__convex_c34__}						\
 %{mc38:-D__convex_c38__}						\
 %{fno-builtin:-D__NO_INLINE}						\
 -D__NO_INLINE_MATH -D__NO_INLINE_STDLIB				\
 -D_IEEE_FLOAT_								\
 %{.S:-P}								\
 %{!traditional:-D__stdc__}						\
 %{!traditional:-D_LONGLONG}						\
 %{!traditional:-Ds64_t=long\\ long -Du64_t=unsigned\\ long\\ long}	\
 %{!ansi:-D_POSIX_SOURCE}						\
 %{!ansi:-D_CONVEX_SOURCE}"

#else

#define CPP_SPEC							\
"%{mc1:-D__convex_c1__}							\
 %{mc2:-D__convex_c2__}							\
 %{!mc1:%{!mc2:%{!mc34:%{!mc38:-D__convex_c32__}}}}			\
 %{mc34:-D__convex_c34__}						\
 %{mc38:-D__convex_c38__}						\
 %{fno-builtin:-D__NO_INLINE}						\
 -D__NO_INLINE_MATH -D__NO_INLINE_STDLIB				\
 -D_CONVEX_FLOAT_							\
 %{.S:-P}								\
 %{!traditional:-D__stdc__}						\
 %{!traditional:-D_LONGLONG}						\
 %{!traditional:-Ds64_t=long\\ long -Du64_t=unsigned\\ long\\ long}	\
 %{!ansi:-D_POSIX_SOURCE}						\
 %{!ansi:-D_CONVEX_SOURCE}"

#endif

#define LIB_SPEC							\
"%{mc1:-lC1%{traditional:_old}%{p:_p}%{pg:_p}}				\
 %{mc2:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}				\
 %{!mc1:%{!mc2:%{!mc34:%{!mc38:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}}}} \
 %{mc34:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}				\
 %{mc38:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}				\
 -lc%{traditional:_old}%{p:_p}%{pg:_p}"

#endif

#if (TARGET_DEFAULT | TARGET_CPU_DEFAULT) & 010

/* C34 default */

#if _IEEE_FLOAT_

#define CPP_SPEC							\
"%{mc1:-D__convex_c1__}							\
 %{mc2:-D__convex_c2__}							\
 %{mc32:-D__convex_c32__}						\
 %{!mc1:%{!mc2:%{!mc32:%{!mc38:-D__convex_c34__}}}}			\
 %{mc38:-D__convex_c38__}						\
 %{fno-builtin:-D__NO_INLINE}						\
 -D__NO_INLINE_MATH -D__NO_INLINE_STDLIB				\
 -D_IEEE_FLOAT_								\
 %{.S:-P}								\
 %{!traditional:-D__stdc__}						\
 %{!traditional:-D_LONGLONG}						\
 %{!traditional:-Ds64_t=long\\ long -Du64_t=unsigned\\ long\\ long}	\
 %{!ansi:-D_POSIX_SOURCE}						\
 %{!ansi:-D_CONVEX_SOURCE}"

#else

#define CPP_SPEC							\
"%{mc1:-D__convex_c1__}							\
 %{mc2:-D__convex_c2__}							\
 %{mc32:-D__convex_c32__}						\
 %{!mc1:%{!mc2:%{!mc32:%{!mc38:-D__convex_c34__}}}}			\
 %{mc38:-D__convex_c38__}						\
 %{fno-builtin:-D__NO_INLINE}						\
 -D__NO_INLINE_MATH -D__NO_INLINE_STDLIB				\
 -D_CONVEX_FLOAT_							\
 %{.S:-P}								\
 %{!traditional:-D__stdc__}						\
 %{!traditional:-D_LONGLONG}						\
 %{!traditional:-Ds64_t=long\\ long -Du64_t=unsigned\\ long\\ long}	\
 %{!ansi:-D_POSIX_SOURCE}						\
 %{!ansi:-D_CONVEX_SOURCE}"

#endif

#define LIB_SPEC							\
"%{mc1:-lC1%{traditional:_old}%{p:_p}%{pg:_p}}				\
 %{mc2:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}				\
 %{mc32:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}				\
 %{!mc1:%{!mc2:%{!mc32:%{!mc38:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}}}} \
 %{mc38:-lC2%{traditional:_old}%{p:_p}%{pg:_p}}				\
 -lc%{traditional:_old}%{p:_p}%{pg:_p}"

#endif

#if (TARGET_DEFAULT | TARGET_CPU_DEFAULT) & 020

/* C38 default */

#if _IEEE_FLOAT_

#define CPP_SPEC							\
"%{mc1:-D__convex_c1__}							\
 %{mc2:-D__convex_c2__}							\
 %{mc32:-D__convex_c32__}						\
 %{mc34:-D__convex_c34__}						\
 %{fno-builtin:-D__NO_INLINE}						\
 -D__NO_INLINE_MATH -D__NO_INLINE_STDLIB				\
 -D_IEEE_FLOAT_								\
 %{!mc1:%{!mc2:%{!mc32:%{!mc34:-D__convex_c38__}}}}			\
 %{.S:-P}								\
 %{!traditional:-D__stdc__}						\
 %{!traditional:-D_LONGLONG}						\
 %{!traditional:-Ds64_t=long\\ long -Du64_t=unsigned\\ long\\ long}	\
 %{!ansi:-D_POSIX_SOURCE}						\
 %{!ansi:-D_CONVEX_SOURCE}"

#else

#define CPP_SPEC							\
"%{mc1:-D__convex_c1__}							\
 %{mc2:-D__convex_c2__}							\
 %{mc32:-D__convex_c32__}						\
 %{mc34:-D__convex_c34__}						\
 %{fno-builtin:-D__NO_INLINE}						\
 -D__NO_INLINE_MATH -D__NO_INLINE_STDLIB				\
 -D_CONVEX_FLOAT_							\
 %{!mc1:%{!mc2:%{!mc32:%{!mc34:-D__convex_c38__}}}}			\
 %{.S:-P}								\
 %{!traditional:-D__stdc__}						\
 %{!traditional:-D_LONGLONG}						\
 %{!traditional:-Ds64_t=long\\ long -Du64_t=unsigned\\ long\\ long}	\
 %{!ansi:-D_POSIX_SOURCE}						\
 %{!ansi:-D_CONVEX_SOURCE}"

#endif
--->