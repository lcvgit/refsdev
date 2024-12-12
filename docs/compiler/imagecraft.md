# Imagecraft

## Identification

`__IMAGECRAFT__`

:   Identifies the compiler as Imagecraft.

<!--
`_AVR`
`_Cortex`
`_MSP430`
`_HC08`
`_HC11`
`_HC12`
`_ARM`
`_M8C`
`_PROP` (Propeller)
-->

## Versioning

`__ICC_VERSION`

:   An integer for the version of the Imagecraft compiler, which is encoded as a decimal integer with the general form of <**_ABBCC_**>~10~, where:

    - <**_A_**>~10~ is the major version;
    - <**_BB_**>~10~ is the minor version; and
    - <**_CC_**>~10~ is the patch version.

    !!!note

        Earlier versions encode `__ICC_VERSION` as <**_ABB_**>~10~.

`__ICC_VERSION__`

:   A string for the version of the Imagecraft compiler.

`__BUILD`

:   An integer for the build of the Imagecraft compiler.

## References

- <https://imagecraft.com/>{:target="_blank"}
- <https://elmicro.com/files/icc/iccv8cortex_manual.pdf>{:target="_blank"}
- <https://www.pumpkininc.com/content/doc/manual/rm-iccavr.pdf>{:target="_blank"}
