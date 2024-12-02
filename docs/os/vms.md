# VMS

## Identification

`vms`
`__vms`
`__vms__`

:   Identifies the target operating system as VMS.

`VMS`
`__VMS`
`__VMS__`

:   Identifies the target operating system as VMS.

## Versioning

`__VMS_VER`

:   An integer for the version of VMS, which is encoded as a decimal integer with the general form of <**_AABBCDDEE_**>~10~, where:

    - <**_AA_**>~10~ is the major version;
    - <**_BB_**>~10~ is the minor version;
    - <**_C_**>~10~ is the edit number;
    - <**_DD_**>~10~ is the patch version; and
    - <**_EE_**>~10~ indicates the release type.

## References

- <http://en.wikipedia.org/wiki/Vms>{:target="_blank"}

<!---
<gcc/config/alpha/vms.h> (14.2.0)

  #define SUBTARGET_OS_CPP_BUILTINS()		\
      do {					\
        builtin_define ("__ALPHA");		\
        if (TARGET_FLOAT_VAX)			\
          builtin_define ("__G_FLOAT");		\
        else					\
          builtin_define ("__IEEE_FLOAT");	\
      } while (0)

<gcc/config/vms/vms.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()					 \
    do {									 \
      builtin_define_std ("vms");						 \
      builtin_define_std ("VMS");						 \
      builtin_assert ("system=vms");					 \
      SUBTARGET_OS_CPP_BUILTINS();					 \
      builtin_define ("__int64=long long");				 \
      if (flag_vms_pointer_size == VMS_POINTER_SIZE_32)			 \
        builtin_define ("__INITIAL_POINTER_SIZE=32");			 \
      else if (flag_vms_pointer_size == VMS_POINTER_SIZE_64)		 \
        builtin_define ("__INITIAL_POINTER_SIZE=64");			 \
      if (POINTER_SIZE == 64)						 \
        builtin_define ("__LONG_POINTERS=1");				 \
      builtin_define_with_int_value ("__CRTL_VER", vms_c_get_crtl_ver ()); \
      builtin_define_with_int_value ("__VMS_VER", vms_c_get_vms_ver ());   \
    } while (0)
////

////
VMS 	__VMS_VER
6.1 	60100022
6.2 	60200022
6.2-1I 	60210922
--->