# NanoMig vAmigaTS Test Report

- **NanoMig SHA:** [0f3d2fdac8dd7097127d07d78029c31f3758c32c](https://github.com/harbaum/NanoMig/commit/0f3d2fdac8dd7097127d07d78029c31f3758c32c)
- **vAmigaTS SHA:** [e807e3256d73135f1960e7f9aef2c16d8a6a56b4](https://github.com/dirkwhoffmann/vAmigaTS/commit/e807e3256d73135f1960e7f9aef2c16d8a6a56b4)
- **Regression repo commit SHA:** `2ec3f74c3d00e0516daf25dbb1d98efa1139b03d`
- **Build profile:** Tang Nano 20k, fx68k
- **Date:** 2026-10-17T06:36:20.745895+02:00

## Summary

| Total | PASS | FAIL | DEVIATING_CONFIG | NOT_CALIBRATED | NO_REFERENCE | ERROR |
|---|---|---|---|---|---|---|
| 2610 | 458 | 1517 | 610 | 13 | 12 | 0 |

## Groups and Agreement with Hand Verdicts (2024)

| Group | Variants | PASS | FAIL | NOT_CALIBRATED | Both identical | Both different | Hand ident / auto diff | Hand diff / auto ident | N/A |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| [Agnus/Blitter](Agnus_Blitter.md) | 233 | 48 | 185 | 0 | 48 | 154 | 31 | 0 | 0 |
| [Agnus/Copper](Agnus_Copper.md) | 223 | 86 | 137 | 0 | 43 | 28 | 43 | 0 | 0 |
| [Agnus/DDF](Agnus_DDF.md) | 124 | 35 | 89 | 0 | 14 | 28 | 20 | 0 | 0 |
| [Agnus/DIW](Agnus_DIW.md) | 62 | 46 | 16 | 0 | 20 | 5 | 6 | 0 | 0 |
| [Agnus/Misc](Agnus_Misc.md) | 12 | 1 | 0 | 11 | 0 | 0 | 0 | 0 | 6 |
| [Agnus/Registers](Agnus_Registers.md) | 249 | 42 | 205 | 2 | 6 | 87 | 11 | 0 | 22 |
| [CIA/CIA](CIA_CIA.md) | 10 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 10 |
| [CPU/68010](CPU_68010.md) | 40 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 40 |
| [CPU/Exceptions](CPU_Exceptions.md) | 30 | 15 | 0 | 0 | 0 | 0 | 0 | 0 | 15 |
| [CPU/IPL](CPU_IPL.md) | 447 | 2 | 213 | 0 | 0 | 0 | 0 | 0 | 231 |
| [CPU/IPL2](CPU_IPL2.md) | 6 | 0 | 3 | 0 | 0 | 0 | 0 | 0 | 3 |
| [CPU/Misc](CPU_Misc.md) | 41 | 6 | 15 | 0 | 0 | 0 | 0 | 0 | 21 |
| [CPU/Timing](CPU_Timing.md) | 491 | 0 | 243 | 0 | 0 | 0 | 0 | 0 | 248 |
| [CPU/Timing2](CPU_Timing2.md) | 44 | 0 | 7 | 0 | 0 | 0 | 0 | 0 | 37 |
| [Denise/DIW](Denise_DIW.md) | 25 | 24 | 1 | 0 | 0 | 0 | 0 | 0 | 12 |
| [Denise/ECS](Denise_ECS.md) | 6 | 2 | 4 | 0 | 0 | 0 | 0 | 0 | 2 |
| [Denise/Misc](Denise_Misc.md) | 9 | 4 | 3 | 0 | 0 | 0 | 0 | 0 | 4 |
| [Denise/Registers](Denise_Registers.md) | 68 | 8 | 60 | 0 | 0 | 0 | 0 | 0 | 68 |
| [Denise/Sprites](Denise_Sprites.md) | 214 | 106 | 106 | 0 | 0 | 0 | 0 | 0 | 114 |
| [Mainboard/Ports](Mainboard_Ports.md) | 29 | 6 | 12 | 0 | 0 | 0 | 0 | 0 | 21 |
| [Mainboard/UART](Mainboard_UART.md) | 44 | 0 | 44 | 0 | 0 | 0 | 0 | 0 | 22 |
| [Memory/Ram](Memory_Ram.md) | 5 | 0 | 5 | 0 | 0 | 0 | 0 | 0 | 5 |
| [Memory/Rom](Memory_Rom.md) | 4 | 0 | 4 | 0 | 0 | 0 | 0 | 0 | 4 |
| [Misc/Init](Misc_Init.md) | 5 | 1 | 3 | 0 | 0 | 0 | 0 | 0 | 4 |
| [Paula/Audio](Paula_Audio.md) | 16 | 0 | 16 | 0 | 0 | 0 | 0 | 0 | 16 |
| [Paula/Drive](Paula_Drive.md) | 7 | 0 | 6 | 0 | 0 | 0 | 0 | 0 | 7 |
| [Paula/Interrupts](Paula_Interrupts.md) | 164 | 24 | 140 | 0 | 0 | 0 | 0 | 0 | 82 |
| [Paula/Registers](Paula_Registers.md) | 2 | 2 | 0 | 0 | 0 | 0 | 0 | 0 | 2 |
| **Total** | **2610** | **458** | **1517** | **13** | **131** | **302** | **111** | **0** | **996** |

## How far off the FAILs are

Differing pixels per FAIL, of the 716 x 285 = 204060 compared pixels. Most tests draw their result as Copper or DMA stripes, so a stripe one colour clock off already costs thousands of pixels: the size says more about the kind of difference than about how close NanoMig is.

| Group | PASS | FAIL <= 20 px | FAIL 21-200 px | FAIL 201-2000 px | FAIL 2001-20000 px | FAIL > 20000 px |
|---|---:|---:|---:|---:|---:|---:|
| Agnus/Blitter | 48 | 9 | 0 | 7 | 151 | 18 |
| Agnus/Copper | 86 | 10 | 18 | 14 | 87 | 8 |
| Agnus/DDF | 35 | 11 | 0 | 7 | 67 | 4 |
| Agnus/DIW | 46 | 0 | 1 | 7 | 1 | 7 |
| Agnus/Misc | 1 | 0 | 0 | 0 | 0 | 0 |
| Agnus/Registers | 42 | 14 | 6 | 14 | 113 | 58 |
| CPU/Exceptions | 15 | 0 | 0 | 0 | 0 | 0 |
| CPU/IPL | 2 | 0 | 0 | 0 | 172 | 41 |
| CPU/IPL2 | 0 | 0 | 0 | 0 | 3 | 0 |
| CPU/Misc | 6 | 1 | 0 | 3 | 10 | 1 |
| CPU/Timing | 0 | 0 | 0 | 0 | 243 | 0 |
| CPU/Timing2 | 0 | 0 | 0 | 0 | 6 | 1 |
| Denise/DIW | 24 | 0 | 0 | 1 | 0 | 0 |
| Denise/ECS | 2 | 0 | 0 | 0 | 0 | 4 |
| Denise/Misc | 4 | 0 | 0 | 0 | 3 | 0 |
| Denise/Registers | 8 | 2 | 8 | 11 | 20 | 19 |
| Denise/Sprites | 106 | 3 | 13 | 48 | 18 | 24 |
| Mainboard/Ports | 6 | 1 | 0 | 0 | 6 | 5 |
| Mainboard/UART | 0 | 0 | 0 | 0 | 44 | 0 |
| Memory/Ram | 0 | 1 | 0 | 0 | 1 | 3 |
| Memory/Rom | 0 | 0 | 0 | 0 | 4 | 0 |
| Misc/Init | 1 | 0 | 1 | 2 | 0 | 0 |
| Paula/Audio | 0 | 0 | 0 | 0 | 14 | 2 |
| Paula/Drive | 0 | 0 | 0 | 0 | 6 | 0 |
| Paula/Interrupts | 24 | 0 | 0 | 0 | 136 | 4 |
| Paula/Registers | 2 | 0 | 0 | 0 | 0 | 0 |
| **Total** | **458** | **52** | **47** | **114** | **1105** | **199** |

## How to read

- **PASS:** The rendered frame is identical to the vAmigaTS reference at the Amiga's 4 bits per channel inside the cutout, which here also means the rebuilt vAmiga `.raw` is byte-identical.
- **FAIL:** Differences were detected inside the compared area (cutout).
- **NOT_CALIBRATED:** The raster geometry has not been calibrated yet; no image is produced.
- **NO_REFERENCE:** vAmigaTS ships no reference `.raw` for this variant; it is not simulated.
- **The references are vAmiga screenshots**, not photos of real hardware: `PASS` means identical to vAmiga. See [REFERENCES.md](REFERENCES.md).
- **Labels** never change a result. `denise-ecs-sensitive`: an `_ecs` test that uses an ECS-only Denise feature; vAmiga's A500 ECS has an OCS Denise, NanoMig's ECS mode an ECS Denise. `reference-contradicts-photo`: the vAmigaTS hardware photo of this test shows something else than the reference.
- **Hand verdicts (2024):** The hand verdicts of August 2024 are kept in tag `manual-2024-08`, whose `_ecs` screenshots came from a simulation without an ECS mode.
