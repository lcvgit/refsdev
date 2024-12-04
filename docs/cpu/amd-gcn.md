---
tags:
  - AMD GCN
  - AMD Graphics Core Next
  - AMDGCN
---
# AMD GCN

`__AMDGCN__`

: Identifies the target architecture as AMD GCN.

<!---
<gcc/config/gcn/gcn.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()                                              \
  do                                                                           \
    {                                                                          \
      builtin_define ("__AMDGCN__");                                           \
      if (TARGET_GCN3)                                                         \
	builtin_define ("__GCN3__");                                           \
      else if (TARGET_GCN5)                                                    \
	builtin_define ("__GCN5__");                                           \
      else if (TARGET_CDNA1)                                                   \
	builtin_define ("__CDNA1__");                                          \
      else if (TARGET_CDNA2)                                                   \
	builtin_define ("__CDNA2__");                                          \
      else if (TARGET_RDNA2)                                                   \
	builtin_define ("__RDNA2__");                                          \
      else if (TARGET_RDNA3)                                                   \
	builtin_define ("__RDNA3__");                                          \
      else                                                                     \
	gcc_unreachable ();                                                    \
      if (TARGET_FIJI)                                                         \
	{                                                                      \
	  builtin_define ("__fiji__");                                         \
	  builtin_define ("__gfx803__");                                       \
	}                                                                      \
      else if (TARGET_VEGA10)                                                  \
	builtin_define ("__gfx900__");                                         \
      else if (TARGET_VEGA20)                                                  \
	builtin_define ("__gfx906__");                                         \
      else if (TARGET_GFX908)                                                  \
	builtin_define ("__gfx908__");                                         \
      else if (TARGET_GFX90a)                                                  \
	builtin_define ("__gfx90a__");                                         \
      else if (TARGET_GFX90c)                                                  \
	builtin_define ("__gfx90c__");                                         \
      else if (TARGET_GFX1030)                                                 \
	builtin_define ("__gfx1030__");                                        \
      else if (TARGET_GFX1036)                                                 \
	builtin_define ("__gfx1036__");                                        \
      else if (TARGET_GFX1100)                                                 \
	builtin_define ("__gfx1100__");                                        \
      else if (TARGET_GFX1103)                                                 \
	builtin_define ("__gfx1103__");                                        \
      else                                                                     \
	gcc_unreachable ();                                                    \
  } while (0)
--->