# Solaris

## Identification

`sun`
`__sun`
`__sun__`

`__svr4__`
`__SVR4`

## References

- <http://en.wikipedia.org/wiki/Solaris_Operating_Environment>{:target="_blank"}

<!---
<gcc/config/sol2.h> (14.2.0)

#define TARGET_OS_CPP_BUILTINS()			\
  do {							\
    builtin_define_std ("unix");			\
    builtin_define_std ("sun");				\
    builtin_define ("__svr4__");			\
    builtin_define ("__SVR4");				\
    builtin_assert ("system=unix");			\
    builtin_assert ("system=svr4");			\
    /* For C++ we need to add some additional macro	\
       definitions required by the C++ standard		\
       library.  */					\
    if (c_dialect_cxx ())				\
      {							\
	switch (cxx_dialect)				\
	  {						\
	  case cxx98:					\
	  case cxx11:					\
	  case cxx14:					\
	    /* C++11 and C++14 are based on C99.	\
	       libstdc++ makes use of C99 features	\
	       even for C++98.  */			\
	    builtin_define ("__STDC_VERSION__=199901L");\
	    break;					\
							\
	  default:					\
	    /* C++17 is based on C11.  */		\
	    builtin_define ("__STDC_VERSION__=201112L");\
	    break;					\
	  }						\
	builtin_define ("_XOPEN_SOURCE=600");		\
	builtin_define ("_LARGEFILE_SOURCE=1");		\
	builtin_define ("_LARGEFILE64_SOURCE=1");	\
	builtin_define ("_FILE_OFFSET_BITS=64");	\
	builtin_define ("__EXTENSIONS__");		\
      }							\
    TARGET_SUB_OS_CPP_BUILTINS();			\
  } while (0)
////


////

Type|Macro|Description
---|---|---
Identification|`sun`|
Identification|`__sun`|
Version|`__'System'_'Version'`|System = `uname -s`<br/>Version = `uname -r`<br/>Any illegal character is replaced by an underscore.<br/><br/>Defined by Sun Studio

Use the SVR4 macros to distinguish between Solaris and SunOS.

```c
#if defined(sun) || defined(__sun)
	#if defined(__SVR4) || defined(__svr4__)
		/* Solaris */
	#else
		/* SunOS */
	#endif
#endif
```

##### Example #####

Solaris|Macro
---|---
2.7|`__SunOS_5_7`
8 |`__SunOS_5_8`
--->