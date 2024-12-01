# Android

## Identification

`ANDROID`
`__ANDROID__`

:   Identifies the target operating system as Android.

## Versioning

`__ANDROID_API__`

:   An integer for the Android API level.

    Defined in `<android/api-level.h>`, which is included by `<features.h>`.

### API Level

| Platform Version                              | API Level            | `VERSION_CODE`           |
| --------------------------------------------- | -------------------- | ------------------------ |
| Android 15                                    | `#!c 35`             | `VANILLA_ICE_CREAM`      |
| Android 14                                    | `#!c 34`             | `UPSIDE_DOWN_CAKE`       |
| Android 13                                    | `#!c 33`             | `TIRAMISU`               |
| Android 12                                    | `#!c 32`<br>`#!c 31` | `S_V2`<br>`S`            |
| Android 11                                    | `#!c 30`             | `R`                      |
| Android 10                                    | `#!c 29`             | `Q`                      |
| Android 9                                     | `#!c 28`             | `P`                      |
| Android 8.1                                   | `#!c 27`             | `O_MR1`                  |
| Android 8.0                                   | `#!c 26`             | `O`                      |
| Android 7.1.1<br>Android 7.1                  | `#!c 25`             | `N_MR1`                  |
| Android 7.0                                   | `#!c 24`             | `N`                      |
| Android 6.0                                   | `#!c 23`             | `M`                      |
| Android 5.1                                   | `#!c 22`             | `LOLLIPOP_MR1`           |
| Android 5.0                                   | `#!c 21`             | `LOLLIPOP`               |
| Android 4.4W                                  | `#!c 20`             | `KITKAT_WATCH`           |
| Android 4.4                                   | `#!c 19`             | `KITKAT`                 |
| Android 4.3                                   | `#!c 18`             | `JELLY_BEAN_MR2`         |
| Android 4.2<br>Android 4.2.2                  | `#!c 17`             | `JELLY_BEAN_MR1`         |
| Android 4.1.1<br>Android 4.1                  | `#!c 16`             | `JELLY_BEAN`             |
| Android 4.0.4<br>Android 4.0.3                | `#!c 15`             | `ICE_CREAM_SANDWICH_MR1` |
| Android 4.0.2<br>Android 4.0.1<br>Android 4.0 | `#!c 14`             | `ICE_CREAM_SANDWICH`     |
| Android 3.2                                   | `#!c 13`             | `HONEYCOMB_MR2`          |
| Android 3.1.x                                 | `#!c 12`             | `HONEYCOMB_MR1`          |
| Android 3.0.x                                 | `#!c 11`             | `HONEYCOMB`              |
| Android 2.3.4<br>Android 2.3.3                | `#!c 10`             | `GINGERBREAD_MR1`        |
| Android 2.3.2<br>Android 2.3.1<br>Android 2.3 | `#!c 9`              | `GINGERBREAD`            |
| Android 2.2.x                                 | `#!c 8`              | `FROYO`                  |
| Android 2.1.x                                 | `#!c 7`              | `ECLAIR_MR1`             |
| Android 2.0.1                                 | `#!c 6`              | `ECLAIR_0_1`             |
| Android 2.0                                   | `#!c 5`              | `ECLAIR`                 |
| Android 1.6                                   | `#!c 4`              | `DONUT`                  |
| Android 1.5                                   | `#!c 3`              | `CUPCAKE`                |
| Android 1.1                                   | `#!c 2`              | `BASE_1_1`               |
| Android 1.0                                   | `#!c 1`              | `BASE`                   |

<!---
#### Normalized Versions

| `__ANDROID_API__` | Version |
| ----------------- | ------- |
| `#!c 35`          | 15.0.0  |
| `#!c 34`          | 14.0.0  |
| `#!c 33`          | 13.0.0  |
| `#!c 32`          | 12.0.1  |
| `#!c 31`          | 12.0.0  |
| `#!c 30`          | 11.0.0  |
| `#!c 29`          | 10.0.0  |
| `#!c 28`          | 9.0.0   |
| `#!c 27`          | 8.1.0   |
| `#!c 26`          | 8.0.0   |
| `#!c 25`          | 7.1.0   |
| `#!c 24`          | 7.0.0   |
| `#!c 23`          | 6.0.0   |
| `#!c 22`          | 5.1.0   |
| `#!c 21`          | 5.0.0   |
| `#!c 20`          | 4.4.1   |
| `#!c 19`          | 4.4.0   |
| `#!c 18`          | 4.3.0   |
| `#!c 17`          | 4.2.0   |
| `#!c 16`          | 4.1.0   |
| `#!c 15`          | 4.0.3   |
| `#!c 14`          | 4.0.0   |
| `#!c 13`          | 3.2.0   |
| `#!c 12`          | 3.1.0   |
| `#!c 11`          | 3.0.0   |
| `#!c 10`          | 2.3.3   |
| `#!c 9`           | 2.3.0   |
| `#!c 8`           | 2.2.0   |
| `#!c 7`           | 2.1.0   |
| `#!c 6`           | 2.0.1   |
| `#!c 5`           | 2.0.0   |
| `#!c 4`           | 1.6.0   |
| `#!c 3`           | 1.5.0   |
| `#!c 2`           | 1.1.0   |
| `#!c 1`           | 1.0.0   |
--->

### Comparison Macros

| Code Name        | Comparison Macro        | Value    |
| ---------------- | ----------------------- | -------- |
| Gingerbread      | `__ANDROID_API_G__`     | `#!c 9`  |
| IceCreamSandwich | `__ANDROID_API_I__`     | `#!c 14` |
| Jellybean        | `__ANDROID_API_J__`     | `#!c 16` |
| Jellybean MR1    | `__ANDROID_API_J_MR1__` | `#!c 17` |
| Jellybean MR2    | `__ANDROID_API_J_MR2__` | `#!c 18` |
| KitKat           | `__ANDROID_API_K__`     | `#!c 19` |
| Lollipop         | `__ANDROID_API_L__`     | `#!c 21` |
| Lollipop MR1     | `__ANDROID_API_L_MR1__` | `#!c 22` |
| Marshmallow      | `__ANDROID_API_M__`     | `#!c 23` |
| Nougat           | `__ANDROID_API_N__`     | `#!c 24` |
| Nougat MR1       | `__ANDROID_API_N_MR1__` | `#!c 25` |
| Oreo             | `__ANDROID_API_O__`     | `#!c 26` |
| Oreo MR1         | `__ANDROID_API_O_MR1__` | `#!c 27` |
| Pie              | `__ANDROID_API_P__`     | `#!c 28` |
| QuinceTart       | `__ANDROID_API_Q__`     | `#!c 29` |
| RedVelvetCake    | `__ANDROID_API_R__`     | `#!c 30` |
| Snowcone         | `__ANDROID_API_S__`     | `#!c 31` |
| Tiramisu         | `__ANDROID_API_T__`     | `#!c 33` |
| UpsideDownCake   | `__ANDROID_API_U__`     | `#!c 34` |
| VanillaIceCream  | `__ANDROID_API_V__`     | `#!c 35` |

!!!info

    The comparison macros are defined in `<android/api-level.h>`.

## References

- [Android - Wikipedia](https://en.wikipedia.org/wiki/Android_(operating_system)){:target="_blank"}
- [Android Version History - Wikipedia](https://en.wikipedia.org/wiki/Android_version_history){:target="_blank"}
- [android/api-level.h](https://android.googlesource.com/platform/bionic/+/master/libc/include/android/api-level.h#96){:target="_blank"}
- [Android API Levels](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels){:target="_blank"}
