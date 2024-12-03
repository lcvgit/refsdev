# PRU

## Identification

`__pru__`

: Identifies the target architecture as PRU.

`__PRU__`

: Identifies the target architecture as PRU.

`__PRU_V3__`

: Identifies the target architecture as PRU.

## References

<!---
<gcc/config/pru/pru.h>

#define TARGET_CPU_CPP_BUILTINS()		    \
  do						    \
    {						    \
      builtin_define_std ("__PRU__");		    \
      builtin_define_std ("__pru__");		    \
      builtin_define_std ("__PRU_V3__");	    \
      builtin_define_std ("__LITTLE_ENDIAN__");	    \
      builtin_define_std ("__little_endian__");	    \
      /* Trampolines are disabled for now.  */	    \
      builtin_define_std ("NO_TRAMPOLINES");	    \
    }						    \
  while (0)
--->