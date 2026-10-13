# NanoMig vAmigaTS Test Report

- **NanoMig SHA:** [0f3d2fdac8dd7097127d07d78029c31f3758c32c](https://github.com/harbaum/NanoMig/commit/0f3d2fdac8dd7097127d07d78029c31f3758c32c)
- **vAmigaTS SHA:** [e807e3256d73135f1960e7f9aef2c16d8a6a56b4](https://github.com/dirkwhoffmann/vAmigaTS/commit/e807e3256d73135f1960e7f9aef2c16d8a6a56b4)
- **Regression repo commit SHA:** `6c3f2bd7ee5b73e2cfa65c2b0d4bcbf984df279e`
- **Build profile:** Tang Nano 20k, fx68k
- **Date:** 2026-10-11T23:50:20.014307+02:00

## Summary

| Total | PASS | FAIL | DEVIATING_CONFIG | NOT_CALIBRATED | ERROR |
|---|---|---|---|---|---|
| 903 | 258 | 632 | 0 | 13 | 0 |

## Groups and Agreement with Hand Verdicts (2024)

| Group | Variants | PASS | FAIL | NOT_CALIBRATED | Both identical | Both different | Hand ident / auto diff | Hand diff / auto ident | N/A |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| [Agnus/Blitter](Agnus_Blitter.md) | 233 | 48 | 185 | 0 | 48 | 154 | 31 | 0 | 0 |
| [Agnus/Copper](Agnus_Copper.md) | 223 | 86 | 137 | 0 | 43 | 28 | 43 | 0 | 0 |
| [Agnus/DDF](Agnus_DDF.md) | 124 | 35 | 89 | 0 | 14 | 28 | 20 | 0 | 0 |
| [Agnus/DIW](Agnus_DIW.md) | 62 | 46 | 16 | 0 | 20 | 5 | 6 | 0 | 0 |
| [Agnus/Misc](Agnus_Misc.md) | 12 | 1 | 0 | 11 | 0 | 0 | 0 | 0 | 6 |
| [Agnus/Registers](Agnus_Registers.md) | 249 | 42 | 205 | 2 | 6 | 87 | 11 | 0 | 22 |
| **Total** | **903** | **258** | **632** | **13** | **131** | **302** | **111** | **0** | **28** |

## How to read

- **PASS:** The rendered frame is identical to the vAmigaTS reference at the Amiga's 4 bits per channel inside the cutout, which here also means the rebuilt vAmiga `.raw` is byte-identical.
- **FAIL:** Differences were detected inside the compared area (cutout).
- **NOT_CALIBRATED:** The raster geometry has not been calibrated yet; no image is produced.
- **Hand verdicts (2024):** The hand verdicts of August 2024 are kept in tag `manual-2024-08`, whose `_ecs` screenshots came from a simulation without an ECS mode.
