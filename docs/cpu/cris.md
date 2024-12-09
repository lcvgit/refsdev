# CRIS

## Identification

`cris`
`__cris`
`__cris__`

:   Identifies the target CPU as CRIS.

`CRIS`
`__CRIS`
`__CRIS__`

:   Identifies the target CPU as CRIS.

`GNU_CRIS`
`__GNU_CRIS`
`__GNU_CRIS__`

:   Identifies the target CPU as CRIS.

## Versioning

`__CRIS_ABI_version`

:   An integer for the CRIS ABI version.

`__CRIS_arch_version`

:   An integer for the CRIS version.

## References

- <https://en.wikipedia.org/wiki/ETRAX_CRIS>{:target="_blank"}

<!---
<gcc/config/cris/cris.h> (3.1.0)

#define CPP_PREDEFINES	"-Dcris -DCRIS -DGNU_CRIS"

#define CPP_SPEC \
 "-$ -D__CRIS_ABI_version=2\
  %{mtune=*:-D__tune_%* %{mtune=v*:-D__CRIS_arch_tune=%*}}\
   %{mtune=etrax4:-D__tune_v3 -D__CRIS_arch_tune=3}\
   %{mtune=etrax100:-D__tune_v8 -D__CRIS_arch_tune=8}\
   %{mtune=svinto:-D__tune_v8 -D__CRIS_arch_tune=8}\
   %{mtune=etrax100lx:-D__tune_v10 -D__CRIS_arch_tune=10}\
   %{mtune=ng:-D__tune_v10 -D__CRIS_arch_tune=10}\
  %{mcpu=*:-D__arch_%* %{mcpu=v*:-D__CRIS_arch_version=%*}}\
   %{mcpu=etrax4:-D__arch_v3 -D__CRIS_arch_version=3}\
   %{mcpu=etrax100:-D__arch_v8 -D__CRIS_arch_version=8}\
   %{mcpu=svinto:-D__arch_v8 -D__CRIS_arch_version=8}\
   %{mcpu=etrax100lx:-D__arch_v10 -D__CRIS_arch_version=10}\
   %{mcpu=ng:-D__arch_v10 -D__CRIS_arch_version=10}\
  %{march=*:-D__arch_%* %{march=v*:-D__CRIS_arch_version=%*}}\
   %{march=etrax4:-D__arch_v3 -D__CRIS_arch_version=3}\
   %{march=etrax100:-D__arch_v8 -D__CRIS_arch_version=8}\
   %{march=svinto:-D__arch_v8 -D__CRIS_arch_version=8}\
   %{march=etrax100lx:-D__arch_v10 -D__CRIS_arch_version=10}\
   %{march=ng:-D__arch_v10 -D__CRIS_arch_version=10}\
  %{metrax100:-D__arch__v8 -D__CRIS_arch_version=8}\
  %{metrax4:-D__arch__v3 -D__CRIS_arch_version=3}\
  %(cpp_subtarget)"

/* For the cris-*-elf subtarget.  */
#define CRIS_CPP_SUBTARGET_SPEC \
 "-D__ELF__\
  %{mbest-lib-options:\
   %{!moverride-best-lib-options:\
    %{!march=*:%{!metrax*:%{!mcpu=*:-D__tune_v10 -D__CRIS_arch_tune=10}}}}}"

#define CRIS_CC1_SUBTARGET_SPEC \
 "-melf\
  %{mbest-lib-options:\
   %{!moverride-best-lib-options:\
    %{!march=*:%{!mcpu=*:-mtune=v10 -D__CRIS_arch_tune=10}}\
    %{!finhibit-size-directive:\
      %{!fno-function-sections: -ffunction-sections}\
      %{!fno-data-sections: -fdata-sections}}}}"
////


////
<gcc/config/cris/cris.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()		\
  do						\
    {						\
      builtin_define_std ("cris");		\
      builtin_define_std ("CRIS");		\
      builtin_define_std ("GNU_CRIS");		\
      builtin_define ("__CRIS_ABI_version=2");	\
      builtin_assert ("cpu=cris");		\
      builtin_assert ("machine=cris");		\
    }						\
  while (0)
--->