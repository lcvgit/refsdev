# C++

## Identification

`c_plusplus`

:   Identifies the language as C++.

`__cplusplus`

:   Identifies the language as C++.

`__cplusplus_cli`

:   Identifies the language as C++/CLI.

`__embedded_cplusplus`

:   Identifies the language as Embedded C++.

`__GNUG__`

:   Identifies the language as C++.

    Equivalent to `(__GNUC__ && __cplusplus)`.

`LANGUAGE_C_PLUS_PLUS`
`_LANGUAGE_C_PLUS_PLUS`
`__LANGUAGE_C_PLUS_PLUS`
`__LANGUAGE_C_PLUS_PLUS__`

:   Identifies the language as C++.

`__STDCPP__`

:   Identifies the language as C++.

## Features

`__STDC_HOSTED__`

:   Defined as `#!c 1` if the implementation is a hosted implementation or defined as `#!c 0` if it is not.

## Library

## Versioning

`__cplusplus`

:   An integer for the version of the C++ standard (ISO/IEC 14882), encoded as a decimal integer with the general form of `<yyyymm>L`, where `<yyyy>` and `<mm>` are a year and month specified by the standard.

    | Standard | `__cplusplus` |
    | -------- | ------------- |
    | C++98    | `#!c 199711L` |
    | C++03    | `#!c 199711L` |
    | C++11    | `#!c 201103L` |
    | C++14    | `#!c 201402L` |
    | C++17    | `#!c 201703L` |
    | C++20    | `#!c 202002L` |
    | C++23    | `#!c 202302L` |

    !!!info

        Early drafts of C++98 defined `__cplusplus` as `#!c 199707L` which certain compilers retained (e.g., HP aC++).

`__cplusplus_cli`

:   An integer for the version of the C++/CLI standard, encoded as a decimal integer with the general form of `<yyyymm>L`.
