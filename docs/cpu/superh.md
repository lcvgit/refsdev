# SuperH

## Identification

`__sh__`

: Identifies the target architecture as SuperH.

## Versioning

<!--
`__sh1__`
`__SH1__`

:

`__sh2__`
`__SH2__`

:

`__SH2E__`

:

`__SH2A__`

:

`__sh3__`
`__SH3__`

:

`__SH4_NOFPU__`

:

`__SH4_SINGLE_ONLY__`

:

`__SH3E__`

:

`__SH4_SINGLE__`

:

`__SH4__`

:

`__SH4A__`

:
-->

## References

<!---
Type|Macro|Description
---|---|---
Identification|`__sh__`|Defined by GNU C
Version|`__sh1__`<br/>`__sh2__`<br/>`__sh3__`<br/>`__SH3__`<br/>`__SH4__`<br/>`__SH5__`|

#define CPP_SPEC " \
%{m5-64media|m5-64media-nofpu|m5-32media|m5-32media-nofpu:-D__SHMEDIA__=1} \
%{m5-compact|m5-compact-nofpu:-D__SHMEDIA__=0} \
%{m5-64media|m5-64media-nofpu:-D__SH5__=64 -D__LONG_MAX__=9223372036854775807L} \
%{m5-32media|m5-32media-nofpu|m5-compact|m5-compact-nofpu:-D__SH5__=32} \
%{m5-64media-nofpu|m5-32media-nofpu|m5-compact-nofpu:-D__SH4_NOFPU__} \
%{m1:-D__sh1__} \
%{m2:-D__sh2__} \
%{m3:-D__sh3__} \
%{m3e:-D__SH3E__} \
%{m4-single-only:-D__SH4_SINGLE_ONLY__} \
%{m4-single:-D__SH4_SINGLE__} \
%{m4-nofpu:-D__sh3__ -D__SH4_NOFPU__} \
%{m4:-D__SH4__} \
%{!m1:%{!m2:%{!m3*:%{!m4*:%{!m5*:%(cpp_default_cpu_spec)}}}}} \
%{mhitachi:-D__HITACHI__} \
%(subtarget_cpp_spec) \
%(subtarget_cpp_ptr_spec) \
%(subtarget_cpp_endian_spec) "

#ifndef SUBTARGET_CPP_ENDIAN_SPEC
#define SUBTARGET_CPP_ENDIAN_SPEC "%{ml:-D__LITTLE_ENDIAN__}"
#endif

#ifndef SUBTARGET_CPP_SPEC
#define SUBTARGET_CPP_SPEC ""
#endif

#ifndef CPP_DEFAULT_CPU_SPEC
#define CPP_DEFAULT_CPU_SPEC "-D__sh1__"
#endif

#ifndef SUBTARGET_CPP_PTR_SPEC
#define SUBTARGET_CPP_PTR_SPEC "\
%{m5-64media|m5-64media-nofpu|m5-32media|m5-32media-nofpu|m5-compact|m5-compact-nofpu:-D__SIZE_TYPE__=long\\ unsigned\\ int -D__PTRDIFF_TYPE__=long\\ int} \
%{!m5-64media:%{!m5-64media-nofpu:%{!m5-32media:%{!m5-32media-nofpu:%{!m5-compact:%{!m5-compact-nofpu:-D__SIZE_TYPE__=unsigned\\ int -D__PTRDIFF_TYPE__=int}}}}}} \
"
#endif

#define EXTRA_SPECS						\
  { "subtarget_cpp_spec", SUBTARGET_CPP_SPEC },			\
  { "subtarget_cpp_endian_spec", SUBTARGET_CPP_ENDIAN_SPEC },	\
  { "subtarget_cpp_ptr_spec", SUBTARGET_CPP_PTR_SPEC },		\
  { "cpp_default_cpu_spec", CPP_DEFAULT_CPU_SPEC },

#define CPP_PREDEFINES "-D__sh__ -Acpu=sh -Amachine=sh"

////


////
<gcc/config/sh/sh-c.cc> (14.2.0)

#define builtin_define(TXT) cpp_define (pfile, TXT)
#define builtin_assert(TXT) cpp_assert (pfile, TXT)

/* Implement the TARGET_CPU_CPP_BUILTINS macro  */
void
sh_cpu_cpp_builtins (cpp_reader* pfile)
{
  builtin_define ("__sh__");
  builtin_assert ("cpu=sh");
  builtin_assert ("machine=sh");
  switch ((int) sh_cpu)
    {
    case PROCESSOR_SH1:
      builtin_define ("__sh1__");
      builtin_define ("__SH1__");
      break;
    case PROCESSOR_SH2:
      builtin_define ("__sh2__");
      builtin_define ("__SH2__");
      break;
    case PROCESSOR_SH2E:
      builtin_define ("__SH2E__");
      break;
    case PROCESSOR_SH2A:
      builtin_define ("__SH2A__");
      if (TARGET_SH2A_DOUBLE)
	builtin_define (TARGET_FPU_SINGLE
			? "__SH2A_SINGLE__" : "__SH2A_DOUBLE__");
      else
	builtin_define (TARGET_FPU_ANY
			? "__SH2A_SINGLE_ONLY__" : "__SH2A_NOFPU__");
      break;
    case PROCESSOR_SH3:
      builtin_define ("__sh3__");
      builtin_define ("__SH3__");
      if (TARGET_HARD_SH4)
	builtin_define ("__SH4_NOFPU__");
      break;
    case PROCESSOR_SH3E:
      builtin_define (TARGET_HARD_SH4 ? "__SH4_SINGLE_ONLY__" : "__SH3E__");
      break;
    case PROCESSOR_SH4:
      builtin_define (TARGET_FPU_SINGLE ? "__SH4_SINGLE__" : "__SH4__");
      break;
    case PROCESSOR_SH4A: \
      builtin_define ("__SH4A__");
      builtin_define (TARGET_SH4
		      ? (TARGET_FPU_SINGLE ? "__SH4_SINGLE__" : "__SH4__")
		      : TARGET_FPU_ANY ? "__SH4_SINGLE_ONLY__"
		      : "__SH4_NOFPU__");
      break;
    }
  if (TARGET_FPU_ANY)
    builtin_define ("__SH_FPU_ANY__");
  if (TARGET_FPU_DOUBLE)
    builtin_define ("__SH_FPU_DOUBLE__");
  if (TARGET_HITACHI)
    builtin_define ("__HITACHI__");
  if (TARGET_FMOVD)
    builtin_define ("__FMOVD_ENABLED__");
  if (TARGET_FDPIC)
    {
      builtin_define ("__SH_FDPIC__");
      builtin_define ("__FDPIC__");
    }
  builtin_define (TARGET_LITTLE_ENDIAN
		  ? "__LITTLE_ENDIAN__" : "__BIG_ENDIAN__");

  cpp_define_formatted (pfile, "__SH_ATOMIC_MODEL_%s__",
			selected_atomic_model ().cdef_name);
}
--->