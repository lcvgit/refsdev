# MCST eLbrus Compiler Collection

## Identification

`__LCC__`

:   Identifies the compiler as MCST LCC.

    !!!warning

        The predefined macro `__LCC__` is also defined by the Local C Compiler.

`__MCST__`

:   Identifies the compiler as MCST LCC.

    Added in 1.25.0.

## Versioning

`__LCC__`

:   An integer for the version of the MCST LCC compiler, which is encoded as a decimal integer with the general form of <**_ABB_**>~10~, where:

    - <**_A_**>~10~ is the major version; and
    - <**_BB_**>~10~ is the minor version.

`__LCC_MINOR__`

:   An integer for the major version of the MCST LCC compiler.

## References

- <http://mcst.ru/lcc>{:target="_blank"}

*[MCST]: Moscow Center of SPARC Technologies
*[LCC]: eLbrus Compiler Collection
