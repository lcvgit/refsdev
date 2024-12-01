# FreeBSD

## Identification

`__FreeBSD__`

:   Identifies the target operating system as FreeBSD.

## Versioning

`__FreeBSD__`

:   An integer for the major version of FreeBSD.

`__FreeBSD_version`

:   An integer for the version of FreeBSD, which is encoded as a decimal integer with the general form of <**_AABBCDD_**>~10~, where:

    - <**_AA_**>~10~ is the major version;
    - <**_BB_**>~10~ is the minor version;
    - <**_C_**>~10~ indicates the release type; and
    - <**_DD_**>~10~ is a build version.

    The value of <**_C_**>~10~ is between 0 and 4, inclusive, for releases; otherwise, the value of <**_C_**>~10~ is between 5 and 9, inclusive.

    Defined in `<sys/param.h>`.

## References

- <https://cgit.freebsd.org/src/tree/sys/sys/param.h#n47>{:target="_blank"}
- <https://docs.freebsd.org/en/books/porters-handbook/versions/>{:target="_blank"}
- <https://github.com/gcc-mirror/gcc/blob/bca515ff1893fe4ca1a9042364af3c43f93a397c/gcc/config/freebsd-spec.h#L36>{:target="_blank"}