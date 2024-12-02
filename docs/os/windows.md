# Windows Environment

## Identification

`__TOS_WIN__`

:   Identifies the target environment as Windows.

`_WIN16`

:   Identifies the target environment as Windows 16-bit.

`WIN32`
`_WIN32`
`__WIN32`
`__WIN32__`

:   Identifies the target environment as Windows.

`_WIN64`

:   Identifies the target environment as Windows 64-bit.

`WINNT`
`__WINNT`
`__WINNT__`

:   Identifies the target environment as Windows.

`_WINDOWS`
`__WINDOWS__`

:   Identifies the target environment as Windows.

`_WIN32_WCE`

:   Identifies the target environment as Windows CE.

## References

- <http://msdn.microsoft.com/en-us/library/ff540443.aspx>{:target="_blank"}
- <http://en.wikipedia.org/wiki/Category:Microsoft_Windows>{:target="_blank"}
- <https://github.com/open-watcom/open-watcom-v2/blob/e71622efc810f8cdfd538a85a97eccee8c4feece/bld/cc/c/coptions.c#L357-L360>{:target="_blank"}

<!---
## [Windows](http://en.wikipedia.org/wiki/Category:Microsoft_Windows) ##

Type|Macro|Description
---|---|---
Identification|`_WIN16`|Defined for 16-bit environments [1](http://msdn.microsoft.com/en-us/library/ff540443.aspx)
Identification|`_WIN32`|Defined for both 32-bit and 64-bit environments [1](http://msdn.microsoft.com/en-us/library/ff540443.aspx)
Identification|`_WIN64`|Defined for 64-bit environments [1](http://msdn.microsoft.com/en-us/library/ff540443.aspx)
Identification|`__WIN32__`|Defined by Borland C++
Identification|`__TOS_WIN__`|Defined by xlC
Identification|`__WINDOWS__`|Defined for 16-bit-environments by Watcom C/C++ [1](https://github.com/open-watcom/open-watcom-v2/blob/e71622efc810f8cdfd538a85a97eccee8c4feece/bld/cc/c/coptions.c#L357-L360)

## [Windows CE](http://en.wikipedia.org/wiki/Windows_CE) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`_WIN32_WCE`| |Defined by Embedded Visual C++
Version|`_WIN32_WCE`|VRR|V = VersionR = Revision
Identification|`WIN32_PLATFORM_'P'`| |P = Platform
Version|`WIN32_PLATFORM_'P'`|V|P = PlatformV = Version

##### Example #####

Version|`_WIN32_WCE`
---|---
2.01|201
2.11|211
3.0|300
4.0|400
4.1|410
4.2|420
5.0|501

Platform|Macro|Value
---|---|---
H/PC 2000|`WIN32_PLATFORM_HPC2000`|
H/PC Pro 2.11|`WIN32_PLATFORM_HPCPRO`|211
H/PC Pro 3.0|`WIN32_PLATFORM_HPCPRO`|300
Pocket PC|`WIN32_PLATFORM_PSPC`|1
Pocket PC 2002|`WIN32_PLATFORM_PSPC`|310
Windows Mobile 2003|`WIN32_PLATFORM_PSPC`|400
Smartphone 2002|`WIN32_PLATFORM_WFSP`|100

<gcc/config/i386/crtdll.h>

  #define EXTRA_OS_CPP_BUILTINS()					\
    do								\
      {								\
        builtin_define ("__CRTDLL__");				\
        builtin_define ("__MINGW32__");			   	\
        builtin_define ("_WIN32");				\
        builtin_define_std ("WIN32");				\
        builtin_define_std ("WINNT");				\
      }								\
    while (0)

<gcc/config/i386/djgpp.h>

  #define TARGET_OS_CPP_BUILTINS()		\
    do						\
      {						\
          if (!flag_iso)                          \
      builtin_define_with_int_value ("DJGPP",2);  \
    builtin_define_with_int_value ("__DJGPP",2);   \
    builtin_define_with_int_value ("__DJGPP__",2); \
    builtin_define_std ("MSDOS");		\
    builtin_define_std ("GO32");		\
    builtin_define_std ("unix");		\
    builtin_assert ("system=msdos");	\
      }						\
    while (0)
--->