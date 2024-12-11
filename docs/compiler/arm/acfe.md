# Arm Compiler for Embedded

## Identification

`__ARMCOMPILER_VERSION`

:   Identifies the compiler as Arm Compiler for Embedded.

`__ARMCC_VERSION`

:   Identifies the compiler as Arm Compiler for Embedded.

## Versioning

`__ARMCOMPILER_VERSION`

:   An integer for the version of Arm Compiler for Embedded, which is encoded as a decimal integer with the general form of <**_ABBCCDD_**>~10~, where:

    - <**_A_**>~10~ is the major version;
    - <**_BB_**>~10~ is the minor version;
    - <**_CC_**>~10~ is the patch version; and
    - <**_DD_**>~10~ is reserved.

`__ARMCC_VERSION`

:   An integer for the version of Arm Compiler for Embedded, which is encoded as a decimal integer with the general form of <**_ABCCCC_**>~10~, where:

    - <**_A_**>~10~ is the major version;
    - <**_B_**>~10~ is the minor version; and
    - <**_CCCC_**>~10~ is the patch version.

    !!!note

        If `__ARMCOMPILER_VERSION` is defined, then `__ARMCC_VERSION` is defined as `__ARMCOMPILER_VERSION`.

## References

- [Arm Compiler 6.23 Reference Guide (pdf)](https://documentation-service.arm.com/static/671fa191ad463325b23263ce){:target="_blank"}
- [Arm Compiler 5.06 User Guide (pdf)](https://documentation-service.arm.com/static/602cda95083323480d479712){:target="_blank"}
- [Arm Compiler 4.1 Reference Guide (pdf)](https://documentation-service.arm.com/static/5f915811f86e16515cdc3335){:target="_blank"}

*[ACfE]: Arm Compiler for Embedded
