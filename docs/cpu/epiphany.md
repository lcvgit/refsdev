# Epiphany

## Identification

`__epiphany__`

: Identifies the target architecture as Epiphany.

## References

- <https://en.wikipedia.org/wiki/Zero_ASIC#Epiphany_V>{:target="_blank"}


<!---
Type 	Macro
Identification 	__epiphany__

<gcc/config/epiphany/epiphany.h> (14.2.0)

#define TARGET_CPU_CPP_BUILTINS()		\
  do						\
    {						\
	builtin_define ("__epiphany__");	\
        builtin_define ("__little_endian__");	\
	builtin_define_with_int_value ("__EPIPHANY_STACK_OFFSET__", \
				       epiphany_stack_offset); \
	builtin_assert ("cpu=epiphany");	\
	builtin_assert ("machine=epiphany");	\
    } while (0)
--->