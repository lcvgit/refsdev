# QNX

## Identification

`__QNX__`

:   Identifies the operating system as QNX.

`__QNXNTO__`

:   Identifies the operating system as QNX NTO.

## Versioning

`_NTO_VERSION`

:   An integer for the version of QNX NTO, which is encoded as a decimal integer with the general form of <**_ABB_**>~10~, where:

    - <**_A_**>~10~ is the major version; and
    - <**_BB_**>~10~ is the minor version.

    Only available if `__QNXNTO__` is defined.

    Defined in `<sys/neutrino.h>`.

`BBNDK_VERSION_CURRENT`

:   An integer for the version of the Blackberry NDK, which is encoded as a decimal integer with the general form of <**_AABBBBCCCC_**>~10~, where:

    - <**_AA_**>~10~ is the major version;
    - <**_BBBB_**>~10~ is the minor version; and
    - <**_CCCC_**>~10~ is the patch version.

    Defined in `<bbndk.h>`.

## References

- <http://en.wikipedia.org/wiki/QNX>{:target="_blank"}
