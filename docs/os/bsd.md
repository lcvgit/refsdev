# BSD Environment

## Identification

`BSD`

:   Identifies the environment as BSD.

    Defined in `<sys/param.h>`.

`_SYSTYPE_BSD`

:   Identifies the environment as BSD.

For the sake of portability, predefined macros for identifying BSDi, DragonFly, FreeBSD, MidnightBSD, NetBSD, OpenBSD, and/or other variants of BSD can potentially be used prior to including `<sys/param.h>`.

## Versioning

`BSD`

:   An integer for the version of BSD, which is encoded as a decimal integer with the general form of <**_yyyymm_**>~10~, where:

    - <**_yyyy_**>~10~ is a year; and
    - <**_mm_**>~10~ is a month;

    corresponding to the release date for a given version of BSD.
