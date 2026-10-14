# NanoMig vAmigaTS Test Report

- **NanoMig SHA:** [0f3d2fdac8dd7097127d07d78029c31f3758c32c](https://github.com/harbaum/NanoMig/commit/0f3d2fdac8dd7097127d07d78029c31f3758c32c)
- **vAmigaTS SHA:** [e807e3256d73135f1960e7f9aef2c16d8a6a56b4](https://github.com/dirkwhoffmann/vAmigaTS/commit/e807e3256d73135f1960e7f9aef2c16d8a6a56b4)
- **Regression repo commit SHA:** `5fcf22540fbd55c281ca1bed16f99df9ed135317`
- **Build profile:** Tang Nano 20k, fx68k
- **Date:** 2026-10-14T20:22:13.968794+02:00

## Summary

| Total | PASS | FAIL | DEVIATING_CONFIG | NOT_CALIBRATED | NO_REFERENCE | ERROR |
|---|---|---|---|---|---|---|
| 1225 | 402 | 806 | 2 | 13 | 2 | 0 |

## Groups and Agreement with Hand Verdicts (2024)

| Group | Variants | PASS | FAIL | NOT_CALIBRATED | Both identical | Both different | Hand ident / auto diff | Hand diff / auto ident | N/A |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| [Agnus/Blitter](Agnus_Blitter.md) | 233 | 48 | 185 | 0 | 48 | 154 | 31 | 0 | 0 |
| [Agnus/Copper](Agnus_Copper.md) | 223 | 86 | 137 | 0 | 43 | 28 | 43 | 0 | 0 |
| [Agnus/DDF](Agnus_DDF.md) | 124 | 35 | 89 | 0 | 14 | 28 | 20 | 0 | 0 |
| [Agnus/DIW](Agnus_DIW.md) | 62 | 46 | 16 | 0 | 20 | 5 | 6 | 0 | 0 |
| [Agnus/Misc](Agnus_Misc.md) | 12 | 1 | 0 | 11 | 0 | 0 | 0 | 0 | 6 |
| [Agnus/Registers](Agnus_Registers.md) | 249 | 42 | 205 | 2 | 6 | 87 | 11 | 0 | 22 |
| [Denise/DIW](Denise_DIW.md) | 25 | 24 | 1 | 0 | 0 | 0 | 0 | 0 | 12 |
| [Denise/ECS](Denise_ECS.md) | 6 | 2 | 4 | 0 | 0 | 0 | 0 | 0 | 2 |
| [Denise/Misc](Denise_Misc.md) | 9 | 4 | 3 | 0 | 0 | 0 | 0 | 0 | 4 |
| [Denise/Registers](Denise_Registers.md) | 68 | 8 | 60 | 0 | 0 | 0 | 0 | 0 | 68 |
| [Denise/Sprites](Denise_Sprites.md) | 214 | 106 | 106 | 0 | 0 | 0 | 0 | 0 | 114 |
| **Total** | **1225** | **402** | **806** | **13** | **131** | **302** | **111** | **0** | **228** |

## How to read

- **PASS:** The rendered frame is identical to the vAmigaTS reference at the Amiga's 4 bits per channel inside the cutout, which here also means the rebuilt vAmiga `.raw` is byte-identical.
- **FAIL:** Differences were detected inside the compared area (cutout).
- **NOT_CALIBRATED:** The raster geometry has not been calibrated yet; no image is produced.
- **NO_REFERENCE:** vAmigaTS ships no reference `.raw` for this variant; it is not simulated.
- **Hand verdicts (2024):** The hand verdicts of August 2024 are kept in tag `manual-2024-08`, whose `_ecs` screenshots came from a simulation without an ECS mode.
