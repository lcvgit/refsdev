---
tags:
  - Nvidia PTX
  - PTX
  - Parallel Thread Execution
---
# Nvidia PTX

## Identification

`__nvptx__`

: Identifies the target architecture as Nvidia PTX.

## Versioning

`__PTX_ISA_VERSION_MAJOR__`

: An integer for the Nvidia PTX major version.

`__PTX_ISA_VERSION_MINOR__`

: An integer for the Nvidia PTX minor version.

## References

<!---
<gcc/config/nvptx/nvptx-c.cc>
void
nvptx_cpu_cpp_builtins (void)
{
  cpp_assert (parse_in, "machine=nvptx");
  cpp_assert (parse_in, "cpu=nvptx");
  cpp_define (parse_in, "__nvptx__");
  if (TARGET_SOFT_STACK)
    cpp_define (parse_in, "__nvptx_softstack__");
  if (TARGET_UNIFORM_SIMT)
    cpp_define (parse_in,"__nvptx_unisimt__");

  const char *ptx_sm = NULL;
#define NVPTX_SM(XX, SEP) \
  {						\
    if (TARGET_SM ## XX)			\
      ptx_sm = "__PTX_SM__=" #XX "0"; \
  }
#include "nvptx-sm.def"
#undef NVPTX_SM
  cpp_define (parse_in, ptx_sm);

  {
    unsigned major
      = ptx_version_to_number ((ptx_version)ptx_version_option, true);
    unsigned minor
      = ptx_version_to_number ((ptx_version)ptx_version_option, false);
    cpp_define_formatted (parse_in, "__PTX_ISA_VERSION_MAJOR__=%u", major);
    cpp_define_formatted (parse_in, "__PTX_ISA_VERSION_MINOR__=%u", minor);
  }
}
--->