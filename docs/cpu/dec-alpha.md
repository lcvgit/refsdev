# DEC Alpha

- **Bits**: 64-bit
- **Endianness**: Bi

## Identification

`_ALPHA_`
`__ALPHA`
`__ALPHA__`

:   Identifies the target CPU as the DEC Alpha.

`__Alpha_AXP`
`__Alpha_AXP__`

:   Identifies the target CPU as the DEC Alpha.

`__alpha`
`__alpha__`

:   Identifies the target CPU as the DEC Alpha.

`__alpha_vxworks`
`__alpha_vxworks__`

:   Identifies the target CPU as the DEC Alpha.

`_M_ALPHA`
`__M_ALPHA__`

:   Identifies the target CPU as the DEC Alpha.

## Extension

`__alpha_bwx__`

:   Byte/Word Extension (BWX)

`__alpha_cix__`

:   Count Extension (CIX)

`__alpha_fix__`

:   Square-root and Floating-point Convert Extension (FIX)

`__alpha_max__`

:   Motion Video Instructions (MVI)

    !!!note
    
        The predefined macro `__alpha_max__` appears to be named after the similar RISC Multimedia Acceleration eXtensions (MAX-1, MAX-2), which shares many similarities with the DEC Alpha's Motion Video Instructions (MVI).

## Versioning

`__alpha_ev4__`

:   Defined if the CPU is a variant of the DEC Alpha EV4 (e.g., 21064, 21064A, etc.).

`__alpha_ev5__`

:   Defined if the CPU is a variant of the DEC Alpha EV5 (e.g., 21164, 21164A, etc.).

`__alpha_ev6__`

:   Defined if the CPU is a variant of the DEC Alpha EV6 (e.g., 21264, 21264A, etc.).

| Model   | Code Name | Status      | Extensions |
| ------- | --------- | ----------- | ---------- |
| ADU     | **EV3**   | *Prototype* |            |
| 21064   | **EV4**   | Released    |            |
| 21064   | EV4s      | Released    |            |
| 21064A  | EV45      | Released    |            |
| 21066   | LCA4      | Released    |            |
| 21066A  | LCA4s     | Released    |            |
| 21068   | LCA45     | Released    |            |
| 21068A  | LCA45     | Released    |            |
| 21164   | **EV5**   | Released    | `R`        |
| 21164A  | EV56      | Released    | `RB`       |
| 21164PC | PCA56     | Released    | `RBM`      |
| 21164PC | PCA57     | Released    | `RBM`      |
| 21264   | **EV6**   | Released    | `RBMF`     |
| 21264A  | EV67      | Released    | `RBMFC`    |
| 21264B  | EV68AL    | Released    | `RBMFCT`   |
| 21264C  | EV68CB    | Released    | `RBMFCT`   |
| 21264D  | EV68CX    | Released    | `RBMFCT`   |
| 21364   | **EV7**   | Released    | `RBMFCT`   |
| 21364   | EV7z      | Released    | `RBMFCT`   |
| 21364A  | EV78/EV79 | *Cancelled* | `RBMFCT`   |
| 21464   | *EV8*     | *Cancelled* | `RBMFCT`   |

- `R`, Hardware support for rounding to positive/negative infinity.
- `B`, Byte/Word Extension (BWX), instructions for 8-bit and 16-bit operations from memory and I/O.
- `M`, Motion Video Instructions (MVI), "*multimedia*" instructions (minimum/maximum operations).
- `F`, Square-root and Floating-point Conversion Extension (FIX), instructions for converting integer and floating-point data between registers; and for square root operations.
- `C`, Count Extension (CIX), instructions for counting and finding bits.
- `T`, Hardware support for prefetch with modify intent to improve the performance of the first attempt to acquire a lock.

## References

- [DEC Alpha - Wikipedia](https://en.wikipedia.org/wiki/DEC_Alpha){:target="_blank"}
- [gcc/config/alpha/alpha.h](https://github.com/gcc-mirror/gcc/blob/master/gcc/config/alpha/alpha.h){:target="_blank"}
- [GCC - DEC Alpha Options](https://gcc.gnu.org/onlinedocs/gcc-4.1.2/gcc/DEC-Alpha-Options.html#DEC-Alpha-Options){:target="_blank"}
- [CPU Database - DEC Alpha](http://cpudb.stanford.edu/manufacturers/3.html){:target="_blank"}
- [chessprogramming.org - DEC Alpha](https://www.chessprogramming.org/DEC_Alpha){:target="_blank"}
- [emuvm.com - DEC Alpha](https://emuvm.com/alpha-systems/){:target="_blank"}
- [NetBSD - DEC Alpha](https://man.bsd.lv/NetBSD-8.1/alpha/intro.4){:target="_blank"}
- [HP Digital Technical Journal - DEC Alpha](https://web.archive.org/web/20230123052748/https://www.hpl.hp.com/hpjournal/dtj/vol4num4/toc.htm){:target="_blank"}
- [HP Archived Technical Documentation - DEC Alpha](https://web.archive.org/web/20080404230535/http://h18002.www1.hp.com/alphaserver/technology/chip-docs.html){:target="_blank"}
- [FTP Archive - DEC Alpha](https://ftp.zx.net.nz/pub/archive/ftp.digital.com/pub/DEC/DECinfo/semiconductor/literature/){:target="_blank"}
- [bitsavers.org - DEC Alpha](https://bitsavers.org/pdf/dec/alpha/){:target="_blank"}

*[ADU]: Alpha Demonstration Unit
