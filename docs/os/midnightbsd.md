# MidnightBSD

## Identification

`__MidnightBSD__`

:   Identifies the target operating system as MidnightBSD.

## Versioning

`__MidnightBSD_version`

:   An integer for the version of MidnightBSD, which is encoded as a decimal integer with the general form of <**_AABBCDD_**>~10~, where:

    - <**_AA_**>~10~ is the major version;
    - <**_BB_**>~10~ is the minor version;
    - <**_C_**>~10~ indicates the release type; and
    - <**_DD_**>~10~ is the build version.

    The value of <**_C_**>~10~ is between 0 and 4 for releases; otherwise, the value of <**_C_**>~10~ is between 5 and 9, inclusive.

## References

- <https://en.wikipedia.org/wiki/MidnightBSD>{:target="_blank"}
- <https://github.com/MidnightBSD/src>{:target="_blank"}
- <https://github.com/MidnightBSD/src/blob/43e574daadc5011ff1f5f258bbcb82c68e9e1cae/sys/sys/param.h#L55>{:target="_blank"}