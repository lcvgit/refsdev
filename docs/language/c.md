# C

## Identification

`__GNUC__`

:   Identifies the language as a dialect of C.

`LANGUAGE_C`
`_LANGUAGE_C`
`__LANGUAGE_C`
`__LANGUAGE_C__`

:   Identifies the language as C.

`__STDC__`

:   Identifies the language as C.

## Features

`__STDC_HOSTED__`

:   Defined as `1` if the implementation is a hosted implementation or defined as `0` if it is not.

## Versioning

`__STDC_VERSION__`

:   An integer for the version of the C language (ISO/IEC 9899), which is encoded as a decimal integer with the general form of `<yyyymm>`, where `<yyyy>` and `<mm>` are the year and month specified by the standard.

    | Standard | `__STDC_VERSION__` |
    | -------- | ------------------ |
    | C95      | `#!c 199409L`      |
    | C99      | `#!c 199901L`      |
    | C11      | `#!c 201112L`      |
    | C17      | `#!c 201710L`      |
    | C23      | `#!c 202311L`      |

    !!!note

        The `__STDC_VERSION__` macro was not introduced until ISO/IEC 9899:1990/Amd 1:1994 (C95) however, it is an amendment to ISO/IEC 9899:1990 (C90).
