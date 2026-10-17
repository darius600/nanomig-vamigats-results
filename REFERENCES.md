# What the vAmigaTS references are, and which machines are compared

## Reference images are vAmiga screenshots

Each vAmigaTS test folder holds two kinds of images:

- **Photos** of a real Amiga's screen, e.g. `diwv9_A500_OCS.JPG`, `diwv9_A500_ECS.jpg`,
  `shspot1_A500_plus.jpeg`. These are what the vAmigaTS README means by "reference images
  taken on real Amigas".
- **`.raw` files**, which the harness compares pixel by pixel. They are **vAmiga's own
  screenshots**: vAmigaTS [`Scripts/Makefile3`](https://github.com/dirkwhoffmann/vAmigaTS/blob/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Scripts/Makefile3#L80),
  rule `%.raw:` ("Creating missing raw image"), runs vAmiga with the test's `.retrosh` script
  and stores the screenshot as the reference.
  vAmigaTS uses them as regression baselines for vAmiga.

So `PASS` means: NanoMig's frame is identical to what vAmiga produced when the `.raw` file was
made. Agreement with real hardware can only be judged from the photo, at the resolution of a
photo.

## Which machines are compared

| vAmigaTS scheme (`regression setup …`) | vAmiga Agnus | vAmiga Denise | vAmiga memory | harness flags | NanoMig mode | scripts at vAmigaTS e807e32 |
|---|---|---|---|---|---|---|
| `A500_OCS_1MB` (`_ocs`) | OCS, MOS 8371 | OCS, MOS 8362R8 | 512 KB chip + 512 KB slow | `--chipset 0x00 --memory 0x04` | OCS Agnus + OCS Denise | 553 |
| `A500_ECS_1MB` (`_ecs`) | ECS 1 MB, MOS 8372 | **OCS**, MOS 8362R8 | 512 KB chip + 512 KB slow | `--chipset 0x08 --memory 0x04` | ECS Agnus + **ECS** Denise | 2054 |
| `A500_PLUS_1MB` (`_plus`) | ECS 2 MB, MOS 8375 | ECS, MOS 8373 | 512 KB chip + 512 KB slow | `--chipset 0x08 --memory 0x04` | ECS Agnus + ECS Denise | 3 |

Sources: vAmiga at 899da5dd,
[`Core/Components/Amiga.cpp`](https://github.com/dirkwhoffmann/vAmiga/blob/899da5ddd872dfb2e9e35e80247cbb2b36086524/Core/Components/Amiga.cpp#L601-L635)
(the config schemes),
[`AgnusTypes.h`](https://github.com/dirkwhoffmann/vAmiga/blob/899da5ddd872dfb2e9e35e80247cbb2b36086524/Core/Components/Agnus/AgnusTypes.h) and
[`DeniseTypes.h`](https://github.com/dirkwhoffmann/vAmiga/blob/899da5ddd872dfb2e9e35e80247cbb2b36086524/Core/Components/Denise/DeniseTypes.h);
NanoMig at the pinned commit,
[`src/minimig-aga/minimig.v`](https://github.com/harbaum/NanoMig/blob/0f3d2fdac8dd7097127d07d78029c31f3758c32c/src/minimig-aga/minimig.v)
(one `ecs` signal feeds Agnus, Denise and Gary).

The photos labelled `A500_ECS` show the same configuration as vAmiga's `A500_ECS_1MB`: on
`Denise/Misc/Id/deniseid/deniseid_A500_ECS_1.jpeg` all 16 bit bands are bright, i.e. DENISEID
reads `$FFFF`, which is an OCS Denise.

## What this means for the results

- **OCS (`_ocs`):** NanoMig, vAmiga and the photographed A500 have the same chip set.
- **ECS (`_ecs`):** the same Agnus. For Denise it compares NanoMig's ECS Denise with an OCS
  Denise, because NanoMig has no mode for an ECS Agnus with an OCS Denise (A500 rev. 6A). This
  matters only where a test uses an ECS-only Denise feature: DENISEID, SuperHires, DIWHIGH,
  KILLEHB, BRDRBLNK and the other BPLCON3 bits. Such tests carry the label
  **`denise-ecs-sensitive`**, found by scanning the test sources (register names, DENISEID read
  by address, BPLCON0 values with the SuperHires bit). Example: `Denise/Misc/Id/deniseid`
  (NanoMig reads `$FFFC`, the reference `$FFFF`).
- **A500+ (`_plus`):** NanoMig's ECS mode matches the chip set.
- About four out of five variants are `_ecs`.

## Known cases where the photo contradicts the reference

`Agnus/DIW/DIWV/diwv9`, `diwv12`, `diwv13`, `diwv14` (`_ecs`) carry the label
**`reference-contradicts-photo`**. These tests write DIWSTRT in the line where it should take
effect, near DDFSTRT or in mid-line.

| test | photo of a real A500 (ECS Agnus) | vAmiga reference | NanoMig |
|---|---|---|---|
| `diwv9_ecs` | one yellow column on the left | two columns in the middle | one yellow column on the left |
| `diwv12_ecs` | one column and garbage in bitplane 1 | two clean columns | two clean columns |
| `diwv13_ecs` | one column, garbage at the top | two clean columns | two clean columns |
| `diwv14_ecs` | no picture, only the dashed lines | two columns | two columns |
| `diwv15_ecs` | two columns | two columns | two columns |

Photo, source and ADF come from the same vAmigaTS commit (January 2022); the `.raw` files were
made on 31.12.2023. The OCS photos agree with the OCS references. For these variants a `FAIL`
says nothing about real hardware; in `diwv9_ecs` NanoMig looks like the photo and vAmiga does
not. Caveat: one photo per test from one machine, and the effect looks like a timing edge case
that may vary between chips.

## Age of the references

The `.raw` files at the pinned vAmigaTS commit were made by vAmiga versions from 2021 to 2024
(see `git log` per file), and vAmiga has changed since. Example: current vAmiga applies the
SuperHires colour encoding only with an ECS Denise
([`PixelEngine::shresModeEcs`](https://github.com/dirkwhoffmann/vAmiga/blob/899da5ddd872dfb2e9e35e80247cbb2b36086524/Core/Components/Denise/PixelEngine.cpp#L218)),
while `ddf1sh_ecs.raw` (an OCS Denise configuration, made 31.12.2023) shows the encoding.
