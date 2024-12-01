# Visium

<!---
<gcc/config/visium/visium.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()			\
  do							\
    {							\
      builtin_define ("__VISIUM__");			\
      if (TARGET_MCM)					\
	builtin_define ("__VISIUM_ARCH_MCM__");		\
      if (TARGET_BMI)					\
	builtin_define ("__VISIUM_ARCH_BMI__");		\
      if (TARGET_FPU_IEEE)				\
	builtin_define ("__VISIUM_ARCH_FPU_IEEE__");	\
    }							\
  while (0)
--->