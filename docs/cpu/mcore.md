# MCore

<!---
<gcc/config/mcore/mcore.h> (3.1.0)
#define CPP_PREDEFINES \
  "-D__mcore__ -D__MCORE__=1 -D__declspec(x)=__attribute__((x))" SUBTARGET_CPP_PREDEFINES

/* If -m4align is ever re-enabled then uncomment this line as well:
   #define CPP_SPEC "%{!m4align:-D__MCORE_ALIGN_8__} %{m4align:-D__MCORE__ALIGN_4__}" */
  
#undef  CPP_SPEC
#define CPP_SPEC "							\
%{mbig-endian:								\
  %{mlittle-endian:%echoose either big or little endian, not both}	\
  -D__MCOREBE__}							\
%{m210:									\
  %{m340:%echoose either m340 or m210 not both}				\
  %{mlittle-endian:%ethe m210 does not have little endian support}	\
  -D__M210__}								\
%{!mbig-endian: -D__MCORELE__}						\
%{!m210: -D__M340__}							\
"
/* If -m4align is ever re-enabled then add this line to the definition of CPP_SPEC
   %{!m4align:-D__MCORE_ALIGN_8__} %{m4align:-D__MCORE__ALIGN_4__} */

////


////
<gcc/config/mcore/mcore.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()					  \
  do									  \
    {									  \
      builtin_define ("__mcore__");					  \
      builtin_define ("__MCORE__");					  \
      if (TARGET_LITTLE_END)						  \
        builtin_define ("__MCORELE__");					  \
      else								  \
        builtin_define ("__MCOREBE__");					  \
      if (TARGET_M340)							  \
        builtin_define ("__M340__");					  \
      else								  \
        builtin_define ("__M210__");					  \
    }									  \
  while (0)
--->