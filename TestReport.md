# NanoMig vAmigaTS Test Report

- **NanoMig:** [0f3d2fdac8dd7097127d07d78029c31f3758c32c](https://github.com/harbaum/NanoMig/commit/0f3d2fdac8dd7097127d07d78029c31f3758c32c) · **vAmigaTS:** [e807e3256d73135f1960e7f9aef2c16d8a6a56b4](https://github.com/dirkwhoffmann/vAmigaTS/commit/e807e3256d73135f1960e7f9aef2c16d8a6a56b4) · **Build profile:** Tang Nano 20k, fx68k
- **Simulated:** 2026-10-10 to 2026-10-17 · **Published:** 2026-10-17
- **Published with:** [nanomig-vamigats-regression `b0e43cb`](https://github.com/darius600/nanomig-vamigats-regression/commit/b0e43cbeaa5f30697058f4db6372e8aaec9d78ce)

## Where to start

**1975 variants compared: 458 identical to the reference (PASS), 1517 different (FAIL).** The other 635 were not compared (DEVIATING_CONFIG 610, NOT_CALIBRATED 13, NO_REFERENCE 12; see [How to read](#how-to-read)). ERROR: 0.

The 10 FAILs closest to the reference. Each is one test that reruns in about 15 minutes:

| Test | Variant | Machine | Differing px | Image |
|---|---|---|---:|---|
| Mainboard/Ports/POT/stop1 | stop1 | A500 ECS | 2 | [stop1.png](Mainboard/Ports/POT/stop1/stop1.png) |
| Agnus/Copper/Wait/waitblt1 | waitblt1_ecs | A500 ECS | 4 | [waitblt1_ecs.png](Agnus/Copper/Wait/waitblt1/waitblt1_ecs.png) |
| Agnus/Copper/Wait/waitblt1 | waitblt1_ocs | A500 OCS | 4 | [waitblt1_ocs.png](Agnus/Copper/Wait/waitblt1/waitblt1_ocs.png) |
| Agnus/Copper/Wait/waitblt4 | waitblt4_ecs | A500 ECS | 4 | [waitblt4_ecs.png](Agnus/Copper/Wait/waitblt4/waitblt4_ecs.png) |
| Agnus/Copper/Wait/waitblt4 | waitblt4_ocs | A500 OCS | 4 | [waitblt4_ocs.png](Agnus/Copper/Wait/waitblt4/waitblt4_ocs.png) |
| Denise/Registers/BPLCON1/overscan6 | overscan6 | A500 ECS | 4 | [overscan6.png](Denise/Registers/BPLCON1/overscan6/overscan6.png) |
| Memory/Ram/byteacc/byteacc1 | byteacc1 | A500 ECS | 4 | [byteacc1.png](Memory/Ram/byteacc/byteacc1/byteacc1.png) |
| Agnus/DDF/DDF/farright1 | farright1_ecs | A500 ECS | 6 | [farright1_ecs.png](Agnus/DDF/DDF/farright1/farright1_ecs.png) |
| Agnus/DDF/DDF/farright1 | farright1_ocs | A500 OCS | 6 | [farright1_ocs.png](Agnus/DDF/DDF/farright1/farright1_ocs.png) |
| Agnus/DDF/DDF/farright3 | farright3_ocs | A500 OCS | 6 | [farright3_ocs.png](Agnus/DDF/DDF/farright3/farright3_ocs.png) |

All 52 FAILs with 20 differing pixels or fewer: [Near misses](#near-misses).

**One routine behind many FAILs:** 632 of the 1517 FAILs come from tests whose source calls vAmigaTS's `synccpu` routine (`include/util.i`). It synchronises the CPU with the beam and draws the magenta bar at the top of the image. Where that bar differs, everything the CPU draws after it is shifted as well, so these FAILs may share one cause. That has not been established yet.

## Summary

| Variants | PASS | FAIL | DEVIATING_CONFIG | NOT_CALIBRATED | NO_REFERENCE | ERROR |
|---:|---:|---:|---:|---:|---:|---:|
| 2610 | 458 | 1517 | 610 | 13 | 12 | 0 |

## Results per group

| Group | Variants | PASS | FAIL | DEVIATING_CONFIG | NOT_CALIBRATED | NO_REFERENCE | ERROR |
|---|---:|---:|---:|---:|---:|---:|---:|
| [Agnus/Blitter](Agnus_Blitter.md) | 233 | 48 | 185 | 0 | 0 | 0 | 0 |
| [Agnus/Copper](Agnus_Copper.md) | 223 | 86 | 137 | 0 | 0 | 0 | 0 |
| [Agnus/DDF](Agnus_DDF.md) | 124 | 35 | 89 | 0 | 0 | 0 | 0 |
| [Agnus/DIW](Agnus_DIW.md) | 62 | 46 | 16 | 0 | 0 | 0 | 0 |
| [Agnus/Misc](Agnus_Misc.md) | 12 | 1 | 0 | 0 | 11 | 0 | 0 |
| [Agnus/Registers](Agnus_Registers.md) | 249 | 42 | 205 | 0 | 2 | 0 | 0 |
| [CIA/CIA](CIA_CIA.md) | 10 | 0 | 0 | 0 | 0 | 10 | 0 |
| [CPU/68010](CPU_68010.md) | 40 | 0 | 0 | 40 | 0 | 0 | 0 |
| [CPU/Exceptions](CPU_Exceptions.md) | 30 | 15 | 0 | 15 | 0 | 0 | 0 |
| [CPU/IPL](CPU_IPL.md) | 447 | 2 | 213 | 232 | 0 | 0 | 0 |
| [CPU/IPL2](CPU_IPL2.md) | 6 | 0 | 3 | 3 | 0 | 0 | 0 |
| [CPU/Misc](CPU_Misc.md) | 41 | 6 | 15 | 20 | 0 | 0 | 0 |
| [CPU/Timing](CPU_Timing.md) | 491 | 0 | 243 | 248 | 0 | 0 | 0 |
| [CPU/Timing2](CPU_Timing2.md) | 44 | 0 | 7 | 37 | 0 | 0 | 0 |
| [Denise/DIW](Denise_DIW.md) | 25 | 24 | 1 | 0 | 0 | 0 | 0 |
| [Denise/ECS](Denise_ECS.md) | 6 | 2 | 4 | 0 | 0 | 0 | 0 |
| [Denise/Misc](Denise_Misc.md) | 9 | 4 | 3 | 2 | 0 | 0 | 0 |
| [Denise/Registers](Denise_Registers.md) | 68 | 8 | 60 | 0 | 0 | 0 | 0 |
| [Denise/Sprites](Denise_Sprites.md) | 214 | 106 | 106 | 0 | 0 | 2 | 0 |
| [Mainboard/Ports](Mainboard_Ports.md) | 29 | 6 | 12 | 11 | 0 | 0 | 0 |
| [Mainboard/UART](Mainboard_UART.md) | 44 | 0 | 44 | 0 | 0 | 0 | 0 |
| [Memory/Ram](Memory_Ram.md) | 5 | 0 | 5 | 0 | 0 | 0 | 0 |
| [Memory/Rom](Memory_Rom.md) | 4 | 0 | 4 | 0 | 0 | 0 | 0 |
| [Misc/Init](Misc_Init.md) | 5 | 1 | 3 | 1 | 0 | 0 | 0 |
| [Paula/Audio](Paula_Audio.md) | 16 | 0 | 16 | 0 | 0 | 0 | 0 |
| [Paula/Drive](Paula_Drive.md) | 7 | 0 | 6 | 1 | 0 | 0 | 0 |
| [Paula/Interrupts](Paula_Interrupts.md) | 164 | 24 | 140 | 0 | 0 | 0 | 0 |
| [Paula/Registers](Paula_Registers.md) | 2 | 2 | 0 | 0 | 0 | 0 | 0 |
| **Total** | **2610** | **458** | **1517** | **610** | **13** | **12** | **0** |

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

## Agreement with the 2024 hand verdicts

Counted per **test directory**, not per variant: one directory holds the variants of one test (`_ocs`, `_ecs`, ...). A directory counts as identical when all its compared variants PASS, and as different when one of them FAILs. Groups without any hand verdict are left out. Where the two disagree, the class counts: it comes from the exact comparison, while the hand verdict was made by eye on older screenshots.

| Group | Both identical | Both different | Hand identical, now different | Hand different, now identical |
|---|---:|---:|---:|---:|
| [Agnus/Blitter](Agnus_Blitter.md) | 48 | 154 | 31 | 0 |
| [Agnus/Copper](Agnus_Copper.md) | 43 | 28 | 43 | 0 |
| [Agnus/DDF](Agnus_DDF.md) | 14 | 28 | 20 | 0 |
| [Agnus/DIW](Agnus_DIW.md) | 20 | 5 | 6 | 0 |
| [Agnus/Registers](Agnus_Registers.md) | 6 | 87 | 11 | 0 |
| **Total** | **131** | **302** | **111** | **0** |

## How to read

- **PASS:** The frame is identical to the vAmigaTS reference at the Amiga's 4 bits per channel inside the cutout. In all 458 PASS the `.raw` rebuilt from the capture is also byte-identical to the reference (`raw_status`).
- **FAIL:** Differences were found inside the compared area (cutout). The group pages give the number of differing pixels and link the image.
- **DEVIATING_CONFIG:** The script asks for something NanoMig on a Tang Nano 20k cannot be configured to: a 68010, joystick, mouse or keyboard input, further floppy drives. Not simulated; the reason is on the group page.
- **NOT_CALIBRATED:** Simulated, but the raster (NTSC, interlace) has no verified crop yet, so it is not compared.
- **NO_REFERENCE:** vAmigaTS ships no reference `.raw` for this variant; not simulated.
- **ERROR:** The simulation itself failed or exceeded its time limit. Rerun it.
- **`raw_status` "missing colours"** (in `.result.json`): NanoMig produced a colour that no reference uses, so no `.raw` can be rebuilt. The frame is still compared at 4 bits per channel.
- **The references are vAmiga screenshots**, not photos of real hardware: `PASS` means identical to vAmiga. See [REFERENCES.md](REFERENCES.md).
- **Labels** never change a result. `denise-ecs-sensitive`: an `_ecs` test that uses an ECS-only Denise feature; vAmiga's A500 ECS has an OCS Denise, NanoMig's ECS mode an ECS Denise. `reference-contradicts-photo`: the vAmigaTS hardware photo of this test shows something else than the reference.
- **Image titles** give positions in vAmiga's coordinates (x 196–911, y 26–310); in the 716 × 285 panels, subtract 196 from x and 26 from y.
- **Hand verdicts (2024):** The hand verdicts of August 2024 are kept in tag `manual-2024-08`, whose `_ecs` screenshots came from a simulation without an ECS mode.

## Near misses

All FAILs with 20 differing pixels or fewer, fewest first.

| Test | Variant | Machine | Differing px | Image |
|---|---|---|---:|---|
| Mainboard/Ports/POT/stop1 | stop1 | A500 ECS | 2 | [stop1.png](Mainboard/Ports/POT/stop1/stop1.png) |
| Agnus/Copper/Wait/waitblt1 | waitblt1_ecs | A500 ECS | 4 | [waitblt1_ecs.png](Agnus/Copper/Wait/waitblt1/waitblt1_ecs.png) |
| Agnus/Copper/Wait/waitblt1 | waitblt1_ocs | A500 OCS | 4 | [waitblt1_ocs.png](Agnus/Copper/Wait/waitblt1/waitblt1_ocs.png) |
| Agnus/Copper/Wait/waitblt4 | waitblt4_ecs | A500 ECS | 4 | [waitblt4_ecs.png](Agnus/Copper/Wait/waitblt4/waitblt4_ecs.png) |
| Agnus/Copper/Wait/waitblt4 | waitblt4_ocs | A500 OCS | 4 | [waitblt4_ocs.png](Agnus/Copper/Wait/waitblt4/waitblt4_ocs.png) |
| Denise/Registers/BPLCON1/overscan6 | overscan6 | A500 ECS | 4 | [overscan6.png](Denise/Registers/BPLCON1/overscan6/overscan6.png) |
| Memory/Ram/byteacc/byteacc1 | byteacc1 | A500 ECS | 4 | [byteacc1.png](Memory/Ram/byteacc/byteacc1/byteacc1.png) |
| Agnus/DDF/DDF/farright1 | farright1_ecs | A500 ECS | 6 | [farright1_ecs.png](Agnus/DDF/DDF/farright1/farright1_ecs.png) |
| Agnus/DDF/DDF/farright1 | farright1_ocs | A500 OCS | 6 | [farright1_ocs.png](Agnus/DDF/DDF/farright1/farright1_ocs.png) |
| Agnus/DDF/DDF/farright3 | farright3_ocs | A500 OCS | 6 | [farright3_ocs.png](Agnus/DDF/DDF/farright3/farright3_ocs.png) |
| Agnus/DDF/DDF/single1 | single1_ocs | A500 OCS | 6 | [single1_ocs.png](Agnus/DDF/DDF/single1/single1_ocs.png) |
| Agnus/DDF/DDF/single4 | single4_ocs | A500 OCS | 6 | [single4_ocs.png](Agnus/DDF/DDF/single4/single4_ocs.png) |
| Agnus/DDF/DDF/single5 | single5_ecs | A500 ECS | 6 | [single5_ecs.png](Agnus/DDF/DDF/single5/single5_ecs.png) |
| Agnus/Registers/DMACON/bpumod4 | bpumod4_ecs | A500 ECS | 6 | [bpumod4_ecs.png](Agnus/Registers/DMACON/bpumod4/bpumod4_ecs.png) |
| Agnus/Registers/DMACON/bpumod4 | bpumod4_ocs | A500 OCS | 6 | [bpumod4_ocs.png](Agnus/Registers/DMACON/bpumod4/bpumod4_ocs.png) |
| Denise/Registers/BPLCON1/overscan6b | overscan6b | A500 ECS | 6 | [overscan6b.png](Denise/Registers/BPLCON1/overscan6b/overscan6b.png) |
| Denise/Sprites/clip/clip2h | clip2h | A500 ECS | 6 | [clip2h.png](Denise/Sprites/clip/clip2h/clip2h.png) |
| Agnus/Blitter/dmacon/dmacon1 | dmacon1 | A500 ECS | 8 | [dmacon1.png](Agnus/Blitter/dmacon/dmacon1/dmacon1.png) |
| Agnus/Blitter/dmacon/dmacon2 | dmacon2 | A500 ECS | 8 | [dmacon2.png](Agnus/Blitter/dmacon/dmacon2/dmacon2.png) |
| Agnus/Blitter/dmacon/dmacon3 | dmacon3 | A500 ECS | 8 | [dmacon3.png](Agnus/Blitter/dmacon/dmacon3/dmacon3.png) |
| Agnus/Blitter/dmacon/dmacon4 | dmacon4 | A500 ECS | 8 | [dmacon4.png](Agnus/Blitter/dmacon/dmacon4/dmacon4.png) |
| Agnus/Blitter/dmacon/dmacon5 | dmacon5 | A500 ECS | 8 | [dmacon5.png](Agnus/Blitter/dmacon/dmacon5/dmacon5.png) |
| Agnus/Blitter/dmacon/dmacon6 | dmacon6 | A500 ECS | 8 | [dmacon6.png](Agnus/Blitter/dmacon/dmacon6/dmacon6.png) |
| Agnus/Blitter/dmacon/dmacon7 | dmacon7 | A500 ECS | 8 | [dmacon7.png](Agnus/Blitter/dmacon/dmacon7/dmacon7.png) |
| Agnus/Blitter/dmacon/dmacon8 | dmacon8 | A500 ECS | 8 | [dmacon8.png](Agnus/Blitter/dmacon/dmacon8/dmacon8.png) |
| Agnus/Blitter/dmacon/dmacon9 | dmacon9 | A500 ECS | 8 | [dmacon9.png](Agnus/Blitter/dmacon/dmacon9/dmacon9.png) |
| Agnus/Registers/oldDMACON/bplen1 | bplen1_OCS | A500 OCS | 8 | [bplen1_OCS.png](Agnus/Registers/oldDMACON/bplen1/bplen1_OCS.png) |
| Agnus/Registers/oldDMACON/bplen2 | bplen2_ECS | A500 ECS | 8 | [bplen2_ECS.png](Agnus/Registers/oldDMACON/bplen2/bplen2_ECS.png) |
| Agnus/Registers/oldDMACON/oldbplen1 | oldbplen1_OCS | A500 OCS | 8 | [oldbplen1_OCS.png](Agnus/Registers/oldDMACON/oldbplen1/oldbplen1_OCS.png) |
| Agnus/Registers/oldDMACON/oldbplen2 | oldbplen2_ECS | A500 ECS | 8 | [oldbplen2_ECS.png](Agnus/Registers/oldDMACON/oldbplen2/oldbplen2_ECS.png) |
| Agnus/Registers/DMACON/bpumod1 | bpumod1_ecs | A500 ECS | 12 | [bpumod1_ecs.png](Agnus/Registers/DMACON/bpumod1/bpumod1_ecs.png) |
| Agnus/Registers/DMACON/bpumod1 | bpumod1_ocs | A500 OCS | 12 | [bpumod1_ocs.png](Agnus/Registers/DMACON/bpumod1/bpumod1_ocs.png) |
| Agnus/Registers/DMACON/resmod3 | resmod3_ecs | A500 ECS | 15 | [resmod3_ecs.png](Agnus/Registers/DMACON/resmod3/resmod3_ecs.png) |
| Agnus/Registers/DMACON/resmod3 | resmod3_ocs | A500 OCS | 15 | [resmod3_ocs.png](Agnus/Registers/DMACON/resmod3/resmod3_ocs.png) |
| Agnus/Copper/Skip/copskip1 | copskip1_ecs | A500 ECS | 16 | [copskip1_ecs.png](Agnus/Copper/Skip/copskip1/copskip1_ecs.png) |
| Agnus/Copper/Skip/copskip1 | copskip1_ocs | A500 OCS | 16 | [copskip1_ocs.png](Agnus/Copper/Skip/copskip1/copskip1_ocs.png) |
| CPU/Misc/Order/moveorder1 | moveorder1_68000 | A500 ECS | 16 | [moveorder1_68000.png](CPU/Misc/Order/moveorder1/moveorder1_68000.png) |
| Denise/Sprites/general/sprbpu1 | sprbpu1_ECS | A500 ECS | 16 | [sprbpu1_ECS.png](Denise/Sprites/general/sprbpu1/sprbpu1_ECS.png) |
| Denise/Sprites/general/sprbpu1 | sprbpu1_OCS | A500 OCS | 16 | [sprbpu1_OCS.png](Denise/Sprites/general/sprbpu1/sprbpu1_OCS.png) |
| Agnus/DDF/DDF/ddf10 | ddf10_ecs | A500 ECS | 18 | [ddf10_ecs.png](Agnus/DDF/DDF/ddf10/ddf10_ecs.png) |
| Agnus/DDF/DDF/ddf2 | ddf2_ecs | A500 ECS | 18 | [ddf2_ecs.png](Agnus/DDF/DDF/ddf2/ddf2_ecs.png) |
| Agnus/DDF/DDF/ddf3 | ddf3_ecs | A500 ECS | 18 | [ddf3_ecs.png](Agnus/DDF/DDF/ddf3/ddf3_ecs.png) |
| Agnus/DDF/DDF/ddf6 | ddf6_ecs | A500 ECS | 18 | [ddf6_ecs.png](Agnus/DDF/DDF/ddf6/ddf6_ecs.png) |
| Agnus/DDF/DDF/ddf7 | ddf7_ecs | A500 ECS | 18 | [ddf7_ecs.png](Agnus/DDF/DDF/ddf7/ddf7_ecs.png) |
| Agnus/Registers/DMACON/bpumod2 | bpumod2_ecs | A500 ECS | 18 | [bpumod2_ecs.png](Agnus/Registers/DMACON/bpumod2/bpumod2_ecs.png) |
| Agnus/Registers/DMACON/bpumod2 | bpumod2_ocs | A500 OCS | 18 | [bpumod2_ocs.png](Agnus/Registers/DMACON/bpumod2/bpumod2_ocs.png) |
| Agnus/Registers/DMACON/bpumod3 | bpumod3_ecs | A500 ECS | 18 | [bpumod3_ecs.png](Agnus/Registers/DMACON/bpumod3/bpumod3_ecs.png) |
| Agnus/Registers/DMACON/bpumod3 | bpumod3_ocs | A500 OCS | 18 | [bpumod3_ocs.png](Agnus/Registers/DMACON/bpumod3/bpumod3_ocs.png) |
| Agnus/Copper/Wait/waitblt5 | waitblt5_ecs | A500 ECS | 20 | [waitblt5_ecs.png](Agnus/Copper/Wait/waitblt5/waitblt5_ecs.png) |
| Agnus/Copper/Wait/waitblt5 | waitblt5_ocs | A500 OCS | 20 | [waitblt5_ocs.png](Agnus/Copper/Wait/waitblt5/waitblt5_ocs.png) |
| Agnus/Copper/oldJump/jump3a | jump3a_ecs | A500 ECS | 20 | [jump3a_ecs.png](Agnus/Copper/oldJump/jump3a/jump3a_ecs.png) |
| Agnus/Copper/oldJump/jump3a | jump3a_ocs | A500 OCS | 20 | [jump3a_ocs.png](Agnus/Copper/oldJump/jump3a/jump3a_ocs.png) |
