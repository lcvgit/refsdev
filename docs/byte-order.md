# Byte Order

`__STDC_ENDIAN_NATIVE__`
`__STDC_ENDIAN_BIG__`
`__STDC_ENDIAN_LITTLE__`

Defined in `<stdbit.h>` (since C23).

`__BYTE_ORDER__`
`__ORDER_BIG_ENDIAN__`
`__ORDER_LITTLE_ENDIAN__`
`__ORDER_PDP_ENDIAN__`

Defined by GCC/Clang.

`__BYTE_ORDER`
`__BIG_ENDIAN`
`__LITTLE_ENDIAN`
`__PDP_ENDIAN`

Defined in `<endian.h>`.

<!--
`_BYTE_ORDER`
`_BIG_ENDIAN`
`_LITTLE_ENDIAN`
`_PDP_ENDIAN`
-->

`BYTE_ORDER`
`BIG_ENDIAN`
`LITTLE_ENDIAN`
`PDP_ENDIAN`

Defined in `<machine/endian.h>`.

`__FLOAT_WORD_ORDER__`
`__ORDER_BIG_ENDIAN__`
`__ORDER_LITTLE_ENDIAN__`
`__ORDER_PDP_ENDIAN__`

Defined by GCC/Clang.

`__FLOAT_WORD_ORDER`
`__BIG_ENDIAN`
`__LITTLE_ENDIAN`
`__PDP_ENDIAN`

Defined in `<ieee754.h>`.

`BIG_ENDIAN`
`_BIG_ENDIAN`
`__BIG_ENDIAN`
`__BIGENDIAN__`
`__BIG_ENDIAN__`
`__big_endian__`
`__THW_BIG_ENDIAN__`

`__ARMEB__`
`__ARM_BIG_ENDIAN`
`__THUMBEB__`
`__AARCH64EB__`
`__MICROBLAZEEB__`
`MIPSEB`
`_MIPSEB`
`__MIPSEB`
`__MIPSEB__`
`__BPF_BIG_ENDIAN__`
`__ckcoreBE__`
`__cskyBE__`
`__cskybe__`
`__CSKYBE__`
`__MCOREBE__`
`__MOXIE_BIG_ENDIAN__`
`__NDS32_EB__`
`nios2_big_endian`
`__nios2_big_endian`
`__nios2_big_endian__`
`__RX_BIG_ENDIAN__`
`__XTENSA_EB__`

- HP/PA RISC
- M68000
- S/370
- S/3790
- SPARC
- System/Z

`LITTLE_ENDIAN`
`_LITTLE_ENDIAN`
`__LITTLE_ENDIAN`
`__LITTLEENDIAN__`
`__LITTLE_ENDIAN__`
`__little_endian__`

`__ARMEL__`
`__THUMBEL__`
`__AARCH64EL__`
`__MICROBLAZEEL__`
`MIPSEL`
`_MIPSEL`
`__MIPSEL`
`__MIPSEL__`
`__BPF_LITTLE_ENDIAN__`
`__ckcoreLE__`
`__cskyLE__`
`__cskyle__`
`__CSKYLE__`
`__MCORELE__`
`__MOXIE_LITTLE_ENDIAN__`
`__NDS32_EL__`
`nios2_little_endian`
`__nios2_little_endian`
`__nios2_little_endian__`
`__RX_LITTLE_ENDIAN__`
`__XTENSA_EL__`

<!-- SPARC __LITTLE_ENDIAN_DATA__ -->

- AMD64
- Arm (Windows)
- Blackfin
- IA-64 (if `__BIG_ENDIAN__` is not defined)
- Elbrus 2000
- LoongArch
- MSP430
- RISC-V
- VAX
- x86

`__PDP_ENDIAN`
`_PDP_ENDIAN`
`PDP_ENDIAN`
`__PDP_ENDIAN__`

- PDP-11

<!-- RS/6000 __VEC_ELEMENT_REG_ORDER__ -->