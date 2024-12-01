# FR-V

<!---
<gcc/config/frv/frv.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()					\
  do									\
    {									\
      int issue_rate;							\
									\
      builtin_define ("__frv__");					\
      builtin_assert ("machine=frv");					\
									\
      issue_rate = frv_issue_rate ();					\
      if (issue_rate > 1)						\
	builtin_define_with_int_value ("__FRV_VLIW__", issue_rate);	\
      builtin_define_with_int_value ("__FRV_GPR__", NUM_GPRS);		\
      builtin_define_with_int_value ("__FRV_FPR__", NUM_FPRS);		\
      builtin_define_with_int_value ("__FRV_ACC__", NUM_ACCS);		\
									\
      switch (frv_cpu_type)						\
	{								\
	case FRV_CPU_GENERIC:						\
	  builtin_define ("__CPU_GENERIC__");				\
	  break;							\
	case FRV_CPU_FR550:						\
	  builtin_define ("__CPU_FR550__");				\
	  break;							\
	case FRV_CPU_FR500:						\
	case FRV_CPU_TOMCAT:						\
	  builtin_define ("__CPU_FR500__");				\
	  break;							\
	case FRV_CPU_FR450:						\
	  builtin_define ("__CPU_FR450__");				\
	  break;							\
	case FRV_CPU_FR405:						\
	  builtin_define ("__CPU_FR405__");				\
	  break;							\
	case FRV_CPU_FR400:						\
	  builtin_define ("__CPU_FR400__");				\
	  break;							\
	case FRV_CPU_FR300:						\
	case FRV_CPU_SIMPLE:						\
	  builtin_define ("__CPU_FR300__");				\
	  break;							\
	}								\
									\
      if (TARGET_HARD_FLOAT)						\
	builtin_define ("__FRV_HARD_FLOAT__");				\
      if (TARGET_DWORD)							\
	builtin_define ("__FRV_DWORD__");				\
      if (TARGET_FDPIC)							\
	builtin_define ("__FRV_FDPIC__");				\
      if (flag_leading_underscore > 0)					\
	builtin_define ("__FRV_UNDERSCORE__");				\
    }									\
  while (0)
--->