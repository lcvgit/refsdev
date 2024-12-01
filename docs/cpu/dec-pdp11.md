# DEC PDP-11

<!---
#define CPP_PREDEFINES "-Dpdp11"
////

////
<gcc/config/pdp11/pdp11.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()		\
  do						\
    {						\
      builtin_define_std ("pdp11");		\
      if (TARGET_INT16) 					\
	builtin_define_with_int_value ("__pdp11_int", 16);	\
      else							\
	builtin_define_with_int_value ("__pdp11_int", 32);	\
      if (TARGET_40)						\
	builtin_define_with_int_value ("__pdp11_model", 40);	\
      else if (TARGET_45)					\
	builtin_define_with_int_value ("__pdp11_model", 45);	\
      else							\
	builtin_define_with_int_value ("__pdp11_model", 10);	\
      if (TARGET_FPU)						\
	builtin_define ("__pdp11_fpu");				\
      if (TARGET_AC0)						\
	builtin_define ("__pdp11_ac0");				\
    }						\
  while (0)
--->