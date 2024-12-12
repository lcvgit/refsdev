# AMD Optimizing C/C++ Compiler

<!-- Based on Clang and DragonEgg/Flang -->

The AOCC compiler is based on LLVM and has enhanced support for AMD Zen processors (e.g., Epyc, Ryzen).  For dialects of C/C++, AOCC is based on LLVM Clang.  AOCC also supports Fortran and is now based on LLVM Flang (since AOCC 1.2.0); while, earlier versions were based on DragonEgg with GCC 4.8.2.

## Identification

`__aocc__`

:   Identifies the compiler as AOCC.

    Added in 4.1.0.

## Versioning

`__aocc_major__`

:   An integer for the major version of AOCC.

    Added in 4.1.0.

`__aocc_minor__`

:   An integer for the major version of AOCC.

    Added in 4.1.0.

`__aocc_patchlevel__`

:   An integer for the major version of AOCC.

    Added in 4.1.0.

| AOCC                  | LLVM                         |
| --------------------- | ---------------------------- |
| 1.0.0<br>(2017-05-01) | 4.0.0                        |
| 1.1.0<br>(2017-12-15) | 6.0.0-trunk<br>(2017-11-30)  |
| 1.2.0<br>(2018-04-11) | 6.0.0<br>(2018-03-08)        |
| 1.2.1<br>(2018-06-12) | 6.0.0<br>(2018-03-08)        |
| 2.0.0<br>(2019-08-07) | 8.0.0<br>(2019-03-20)        |
| 2.1.0<br>(2019-11-22) | 9.0.0<br>(2019-09-19)        |
| 2.2.0<br>(2020-06-30) | 10.0.0<br>(2020-03-24)       |
| 2.3.0<br>(2020-12-03) | 11.0.0<br>(2020-10-12)       |
| 3.0.0<br>(2021-03-15) | 12.0.0-trunk<br>(2020-10-22) |
| 3.1.0<br>(2021-07-19) | 12.0.0<br>(2021-04-14)       |
| 3.2.0<br>(2021-12-10) | 13.0.0<br>(2021-10-04)       |
| 4.0.0<br>(2022-11-10) | 14.0.6<br>(2022-06-24)       |
| 4.1.0<br>(2023-08-04) | 16.0.3<br>(2023-05-03)       |
| 4.2.0<br>(2024-02-27) | 16.0.3<br>(2023-05-03)       |
| 5.0.0<br>(2024-10-10) | 17.0.6<br>(2023-11-28)       |

## References

- <https://en.wikipedia.org/wiki/AMD_Optimizing_C/C%2B%2B_Compiler>{:target="_blank"}
- <https://www.amd.com/en/developer/aocc.html>{:target="_blank"}
- [AOCC Archives](https://www.amd.com/en/developer/aocc/aocc-archives.html){:target="_blank"}
- [AOCC Archives - 3.1.0](https://web.archive.org/web/20210730070951/https://developer.amd.com/aocc-archive-section/){:target="_blank"}
- [AOCC Archives - 3.3.0](https://web.archive.org/web/20230207144235/https://developer.amd.com/aocc-archive-section/){:target="_blank"}
- [AOCC Archives - 4.0.0](https://web.archive.org/web/20230118185243/https://developer.amd.com/aocc-archive-section/){:target="_blank"}
- [AOCC 1.0.0](https://web.archive.org/web/20171021164032/https://developer.amd.com/amd-aocc/){:target="_blank"}
- [AOCC 1.2.0](https://web.archive.org/web/20180501015511/https://developer.amd.com/amd-aocc/){:target="_blank"}
- [AOCC 1.2.1](https://web.archive.org/web/20180709194500/https://developer.amd.com/amd-aocc/){:target="_blank"}
- [AOCC 1.2.1 Patched](https://web.archive.org/web/20180729013056/https://developer.amd.com/amd-aocc/){:target="_blank"}
- [AOCC 2.1.0](https://web.archive.org/web/20191207071606/https://developer.amd.com/amd-aocc/){:target="_blank"}
- [AOCC 2.2.0](https://web.archive.org/web/20200909115713/https://developer.amd.com/amd-aocc/){:target="_blank"}
- [AOCC 2.3.0](https://web.archive.org/web/20201225035200/https://developer.amd.com/amd-aocc/){:target="_blank"}
- [AOCC 3.0.0](https://web.archive.org/web/20210413095423/https://developer.amd.com/amd-aocc/){:target="_blank"}
- [AOCC 3.1.0](https://web.archive.org/web/20210730062401/https://developer.amd.com/amd-aocc/){:target="_blank"}
- [AOCC 3.2.0](https://web.archive.org/web/20220324053932/https://developer.amd.com/amd-aocc/){:target="_blank"}
- [AOCC 4.0.0](https://web.archive.org/web/20221218005225/https://developer.amd.com/amd-aocc/){:target="_blank"}
- [AOCC 4.0.0](https://web.archive.org/web/20230106032132/https://developer.amd.com/amd-aocc/){:target="_blank"}
