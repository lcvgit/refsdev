# BPF

<!---
<gcc/config/bpf/bpf-c.cc> (14.2.0)

  void
  bpf_target_macros (cpp_reader *pfile)
  {
    builtin_define ("__BPF__");
    builtin_define ("__bpf__");

    if (TARGET_BIG_ENDIAN)
      builtin_define ("__BPF_BIG_ENDIAN__");
    else
      builtin_define ("__BPF_LITTLE_ENDIAN__");

    switch (bpf_isa)
      {
      case ISA_V1:
        builtin_define_with_int_value ("__BPF_CPU_VERSION__", 1);
        break;
      case ISA_V2:
        builtin_define_with_int_value ("__BPF_CPU_VERSION__", 2);
        break;
      case ISA_V3:
        builtin_define_with_int_value ("__BPF_CPU_VERSION__", 3);
        break;
      case ISA_V4:
        builtin_define_with_int_value ("__BPF_CPU_VERSION__", 4);
        break;
      default:
        gcc_unreachable ();
        break;
      }

    /* Different BPF CPU versions support different features.  Some of
      them can be enabled/disabled explicitly.  */
    if (bpf_has_alu32)
      builtin_define ("__BPF_FEATURE_ALU32");
    if (bpf_has_jmp32)
      builtin_define ("__BPF_FEATURE_JMP32");
    if (bpf_has_jmpext)
      builtin_define ("__BPF_FEATURE_JMP_EXT");
    if (bpf_has_bswap)
      builtin_define ("__BPF_FEATURE_BSWAP");
    if (bpf_has_sdiv)
      builtin_define ("__BPF_FEATURE_SDIV_SMOD");
    if (bpf_has_smov)
      builtin_define ("__BPF_FEATURE_MOVSX");

    /* Other CPU features can only be enabled/disabled generically by
      selecting the corresponding CPU version.  */
    if (bpf_isa >= ISA_V4)
      {
        builtin_define ("__BPF_FEATURE_LDSX");
        builtin_define ("__BPF_FEATURE_GOTOL");
        builtin_define ("__BPF_FEATURE_ST");
      }
  }
--->