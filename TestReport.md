# NanoMig vAmigaTS Test Report

- **NanoMig:** [4315acba5e9f1e15103037627aa78b3460cae8af](https://github.com/MiSTle-Dev/NanoMig/commit/4315acba5e9f1e15103037627aa78b3460cae8af) · **vAmigaTS:** [e807e3256d73135f1960e7f9aef2c16d8a6a56b4](https://github.com/dirkwhoffmann/vAmigaTS/commit/e807e3256d73135f1960e7f9aef2c16d8a6a56b4) · **Build profile:** Tang Nano 20k, fx68k
- **Simulated:** 2026-10-18 to 2026-10-20 · **Published:** 2026-10-21
- **Simulated on:** AMD Ryzen 7 5800H with Radeon Graphics, 8 cores (1223 variants); Intel(R) Core(TM) Ultra 7 165H, 11 cores (778 variants)
- **nanomig-vamigats-regression:** results made with [`52cfceb`](https://github.com/darius600/nanomig-vamigats-regression/commit/52cfcebe6b459281c51c43870da6b78f6d67417d) (2405 variants), [`f2ae07b`](https://github.com/darius600/nanomig-vamigats-regression/commit/f2ae07b41bbc746ee39016d1935592f2520a7ed3) (205 variants); published with [`8ca6474`](https://github.com/darius600/nanomig-vamigats-regression/commit/8ca64742c9a85f2827b0c806ee69ea3fdca67047)

## Summary

**1999 variants compared: 474 identical to the reference (PASS), 1525 different (FAIL).** The other 611 were not compared (DEVIATING_CONFIG 597, NOT_CALIBRATED 2, NO_REFERENCE 12; see [How to read](#how-to-read)). ERROR: 0.

| Variants | PASS | FAIL | DEVIATING_CONFIG | NOT_CALIBRATED | NO_REFERENCE | ERROR |
|---:|---:|---:|---:|---:|---:|---:|
| 2610 | 474 | 1525 | 597 | 2 | 12 | 0 |

## Results per group

| Group | Variants | PASS | FAIL | DEVIATING_CONFIG | NOT_CALIBRATED | NO_REFERENCE | ERROR |
|---|---:|---:|---:|---:|---:|---:|---:|
| [Agnus/Blitter](Agnus_Blitter.md) | 233 | 48 | 185 | 0 | 0 | 0 | 0 |
| [Agnus/Copper](Agnus_Copper.md) | 223 | 86 | 137 | 0 | 0 | 0 | 0 |
| [Agnus/DDF](Agnus_DDF.md) | 124 | 35 | 89 | 0 | 0 | 0 | 0 |
| [Agnus/DIW](Agnus_DIW.md) | 62 | 46 | 16 | 0 | 0 | 0 | 0 |
| [Agnus/Misc](Agnus_Misc.md) | 12 | 7 | 5 | 0 | 0 | 0 | 0 |
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
| [Denise/Misc](Denise_Misc.md) | 9 | 4 | 5 | 0 | 0 | 0 | 0 |
| [Denise/Registers](Denise_Registers.md) | 68 | 8 | 60 | 0 | 0 | 0 | 0 |
| [Denise/Sprites](Denise_Sprites.md) | 214 | 106 | 106 | 0 | 0 | 2 | 0 |
| [Mainboard/Ports](Mainboard_Ports.md) | 29 | 16 | 13 | 0 | 0 | 0 | 0 |
| [Mainboard/UART](Mainboard_UART.md) | 44 | 0 | 44 | 0 | 0 | 0 | 0 |
| [Memory/Ram](Memory_Ram.md) | 5 | 0 | 5 | 0 | 0 | 0 | 0 |
| [Memory/Rom](Memory_Rom.md) | 4 | 0 | 4 | 0 | 0 | 0 | 0 |
| [Misc/Init](Misc_Init.md) | 5 | 1 | 3 | 1 | 0 | 0 | 0 |
| [Paula/Audio](Paula_Audio.md) | 16 | 0 | 16 | 0 | 0 | 0 | 0 |
| [Paula/Drive](Paula_Drive.md) | 7 | 0 | 6 | 1 | 0 | 0 | 0 |
| [Paula/Interrupts](Paula_Interrupts.md) | 164 | 24 | 140 | 0 | 0 | 0 | 0 |
| [Paula/Registers](Paula_Registers.md) | 2 | 2 | 0 | 0 | 0 | 0 | 0 |
| **Total** | **2610** | **474** | **1525** | **597** | **2** | **12** | **0** |

## Where to start

The 10 FAILs closest to the reference. Each is one test that reruns in about 15 minutes; the test links to its source, description and hardware photos in vAmigaTS, and *Where* is the area of the differing pixels in vAmiga's coordinates (see the image):

| Test | Variant | Machine | Differing px | Where | Image |
|---|---|---|---:|---|---|
| [Mainboard/Ports/POT/stop1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Mainboard/Ports/POT/stop1) | stop1 | A500 ECS | 2 | x 256–257, y 40 | [stop1.png](Mainboard/Ports/POT/stop1/stop1.png) |
| [Agnus/Copper/Wait/waitblt1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/Wait/waitblt1) | waitblt1_ecs | A500 ECS | 4 | x 196–199, y 178 | [waitblt1_ecs.png](Agnus/Copper/Wait/waitblt1/waitblt1_ecs.png) |
| [Agnus/Copper/Wait/waitblt1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/Wait/waitblt1) | waitblt1_ocs | A500 OCS | 4 | x 196–199, y 178 | [waitblt1_ocs.png](Agnus/Copper/Wait/waitblt1/waitblt1_ocs.png) |
| [Agnus/Copper/Wait/waitblt4](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/Wait/waitblt4) | waitblt4_ecs | A500 ECS | 4 | x 384–421, y 240–274 | [waitblt4_ecs.png](Agnus/Copper/Wait/waitblt4/waitblt4_ecs.png) |
| [Agnus/Copper/Wait/waitblt4](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/Wait/waitblt4) | waitblt4_ocs | A500 OCS | 4 | x 384–421, y 240–274 | [waitblt4_ocs.png](Agnus/Copper/Wait/waitblt4/waitblt4_ocs.png) |
| [Denise/Registers/BPLCON1/overscan6](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Denise/Registers/BPLCON1/overscan6) | overscan6 | A500 ECS | 4 | x 890–893, y 144–256 | [overscan6.png](Denise/Registers/BPLCON1/overscan6/overscan6.png) |
| [Memory/Ram/byteacc/byteacc1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Memory/Ram/byteacc/byteacc1) | byteacc1 | A500 ECS | 4 | x 224–225, y 208–224 | [byteacc1.png](Memory/Ram/byteacc/byteacc1/byteacc1.png) |
| [Agnus/DDF/DDF/farright1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/farright1) | farright1_ecs | A500 ECS | 6 | x 890–896, y 144–256 | [farright1_ecs.png](Agnus/DDF/DDF/farright1/farright1_ecs.png) |
| [Agnus/DDF/DDF/farright1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/farright1) | farright1_ocs | A500 OCS | 6 | x 890–896, y 144–256 | [farright1_ocs.png](Agnus/DDF/DDF/farright1/farright1_ocs.png) |
| [Agnus/DDF/DDF/farright3](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/farright3) | farright3_ocs | A500 OCS | 6 | x 892–897, y 144 | [farright3_ocs.png](Agnus/DDF/DDF/farright3/farright3_ocs.png) |

All 52 FAILs with 20 differing pixels or fewer: [Near misses](#near-misses).

**One routine behind many FAILs:** 632 of the 1525 FAILs come from tests whose source calls vAmigaTS's `synccpu` routine (`include/util.i`). It synchronises the CPU with the beam and draws the magenta bar at the top of the image. Where that bar differs, everything the CPU draws after it is shifted as well, so these FAILs may share one cause. That has not been established yet. Their rows carry the label `synccpu`.

## How far off the FAILs are

Differing pixels per FAIL, of the 716 x 285 = 204060 compared pixels. Most tests draw their result as Copper or DMA stripes, so a stripe one colour clock off already costs thousands of pixels: the size says more about the kind of difference than about how close NanoMig is.

| Group | PASS | FAIL <= 20 px | FAIL 21-200 px | FAIL 201-2000 px | FAIL 2001-20000 px | FAIL > 20000 px |
|---|---:|---:|---:|---:|---:|---:|
| Agnus/Blitter | 48 | 9 | 0 | 7 | 151 | 18 |
| Agnus/Copper | 86 | 10 | 18 | 14 | 87 | 8 |
| Agnus/DDF | 35 | 11 | 0 | 7 | 67 | 4 |
| Agnus/DIW | 46 | 0 | 1 | 7 | 1 | 7 |
| Agnus/Misc | 7 | 0 | 0 | 3 | 2 | 0 |
| Agnus/Registers | 42 | 14 | 6 | 14 | 113 | 58 |
| CPU/Exceptions | 15 | 0 | 0 | 0 | 0 | 0 |
| CPU/IPL | 2 | 0 | 0 | 0 | 172 | 41 |
| CPU/IPL2 | 0 | 0 | 0 | 0 | 3 | 0 |
| CPU/Misc | 6 | 1 | 0 | 3 | 10 | 1 |
| CPU/Timing | 0 | 0 | 0 | 0 | 243 | 0 |
| CPU/Timing2 | 0 | 0 | 0 | 0 | 6 | 1 |
| Denise/DIW | 24 | 0 | 0 | 1 | 0 | 0 |
| Denise/ECS | 2 | 0 | 0 | 0 | 0 | 4 |
| Denise/Misc | 4 | 0 | 0 | 0 | 5 | 0 |
| Denise/Registers | 8 | 2 | 8 | 11 | 20 | 19 |
| Denise/Sprites | 106 | 3 | 13 | 48 | 18 | 24 |
| Mainboard/Ports | 16 | 1 | 0 | 0 | 6 | 6 |
| Mainboard/UART | 0 | 0 | 0 | 0 | 44 | 0 |
| Memory/Ram | 0 | 1 | 0 | 0 | 1 | 3 |
| Memory/Rom | 0 | 0 | 0 | 0 | 4 | 0 |
| Misc/Init | 1 | 0 | 1 | 2 | 0 | 0 |
| Paula/Audio | 0 | 0 | 0 | 0 | 14 | 2 |
| Paula/Drive | 0 | 0 | 0 | 0 | 6 | 0 |
| Paula/Interrupts | 24 | 0 | 0 | 0 | 136 | 4 |
| Paula/Registers | 2 | 0 | 0 | 0 | 0 | 0 |
| **Total** | **474** | **52** | **47** | **117** | **1109** | **200** |

## How to read

- **Test and variant:** a test is a vAmigaTS test directory (one program); a variant is one of its scripts, usually one per machine. All counts are variants. Variant names come from vAmigaTS and follow no single scheme; the *Machine* column says which machine a variant runs.
- **PASS:** The frame is identical to the vAmigaTS reference at the Amiga's 4 bits per channel inside the cutout, the part of the screen the script compares. In all 474 PASS the `.raw` rebuilt from the capture is also byte-identical to the reference (`raw_status`).
- **FAIL:** Differences were found inside the compared area (cutout). The group pages give the number of differing pixels and link the image.
- **DEVIATING_CONFIG:** The script asks for something this run could not set NanoMig on a Tang Nano 20k up for, e.g. a 68010. Not simulated; the reason is on the group page.
- **NOT_CALIBRATED:** Simulated, but the raster has no verified crop yet, so it is not compared.
- **NTSC** frames are compared on the 237 rows an NTSC beam reaches.
- **NO_REFERENCE:** vAmigaTS ships no reference `.raw` for this variant; not simulated.
- **ERROR:** The simulation itself failed or exceeded its time limit. Rerun it.
- **`raw_status` "missing colours"** (in `.result.json`): NanoMig produced a colour that no reference uses, so no `.raw` can be rebuilt. The frame is still compared at 4 bits per channel.
- **The references are vAmiga screenshots**, not photos of real hardware: `PASS` means identical to vAmiga. See [REFERENCES.md](REFERENCES.md).
- **Labels** never change a result. `reference-uniform`: the reference is one single colour in the compared area (all NTSC `_ocs` references are black there), so a PASS only says that NanoMig draws that colour. `synccpu`: the test calls vAmigaTS's `synccpu` routine (see *Where to start*). `denise-ecs-sensitive`: an `_ecs` test that uses an ECS-only Denise feature; vAmiga's A500 ECS has an OCS Denise, NanoMig's ECS mode an ECS Denise. Where the test also has an `_plus` variant (A500+, ECS Denise on both sides), that variant is the like-for-like comparison: a FAIL it shares is not explained by the label. `reference-contradicts-photo`: the vAmigaTS hardware photo of this test shows something else than the reference; it puts the reference in doubt but does not explain a FAIL (see [REFERENCES.md](REFERENCES.md)). `keyboard-controller`: the test checks the keyboard's own controller (handshake, resync), which NanoMig does not have; its key codes come from the USB/HID path, where the harness feeds them.
- **Image titles** give positions in vAmiga's coordinates (x 196–911, y 26–310); in the 716 × 285 panels, subtract 196 from x and 26 from y.
- **Several machines** simulated this run (see *Simulated on*, and `simulated_on` in each `.result.json`). All ran the same harness binary, and a machine took part only after its captures of a control set were byte-identical with those of the publishing machine.
- **2024:** an earlier comparison by eye is kept in tag `manual-2024-08`; the exact comparison here replaces it.

## Near misses

All FAILs with 20 differing pixels or fewer, fewest first; the first 10 are those under *Where to start*.

| Test | Variant | Machine | Differing px | Where | Image |
|---|---|---|---:|---|---|
| [Mainboard/Ports/POT/stop1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Mainboard/Ports/POT/stop1) | stop1 | A500 ECS | 2 | x 256–257, y 40 | [stop1.png](Mainboard/Ports/POT/stop1/stop1.png) |
| [Agnus/Copper/Wait/waitblt1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/Wait/waitblt1) | waitblt1_ecs | A500 ECS | 4 | x 196–199, y 178 | [waitblt1_ecs.png](Agnus/Copper/Wait/waitblt1/waitblt1_ecs.png) |
| [Agnus/Copper/Wait/waitblt1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/Wait/waitblt1) | waitblt1_ocs | A500 OCS | 4 | x 196–199, y 178 | [waitblt1_ocs.png](Agnus/Copper/Wait/waitblt1/waitblt1_ocs.png) |
| [Agnus/Copper/Wait/waitblt4](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/Wait/waitblt4) | waitblt4_ecs | A500 ECS | 4 | x 384–421, y 240–274 | [waitblt4_ecs.png](Agnus/Copper/Wait/waitblt4/waitblt4_ecs.png) |
| [Agnus/Copper/Wait/waitblt4](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/Wait/waitblt4) | waitblt4_ocs | A500 OCS | 4 | x 384–421, y 240–274 | [waitblt4_ocs.png](Agnus/Copper/Wait/waitblt4/waitblt4_ocs.png) |
| [Denise/Registers/BPLCON1/overscan6](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Denise/Registers/BPLCON1/overscan6) | overscan6 | A500 ECS | 4 | x 890–893, y 144–256 | [overscan6.png](Denise/Registers/BPLCON1/overscan6/overscan6.png) |
| [Memory/Ram/byteacc/byteacc1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Memory/Ram/byteacc/byteacc1) | byteacc1 | A500 ECS | 4 | x 224–225, y 208–224 | [byteacc1.png](Memory/Ram/byteacc/byteacc1/byteacc1.png) |
| [Agnus/DDF/DDF/farright1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/farright1) | farright1_ecs | A500 ECS | 6 | x 890–896, y 144–256 | [farright1_ecs.png](Agnus/DDF/DDF/farright1/farright1_ecs.png) |
| [Agnus/DDF/DDF/farright1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/farright1) | farright1_ocs | A500 OCS | 6 | x 890–896, y 144–256 | [farright1_ocs.png](Agnus/DDF/DDF/farright1/farright1_ocs.png) |
| [Agnus/DDF/DDF/farright3](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/farright3) | farright3_ocs | A500 OCS | 6 | x 892–897, y 144 | [farright3_ocs.png](Agnus/DDF/DDF/farright3/farright3_ocs.png) |
| [Agnus/DDF/DDF/single1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/single1) | single1_ocs | A500 OCS | 6 | x 890–896, y 144–256 | [single1_ocs.png](Agnus/DDF/DDF/single1/single1_ocs.png) |
| [Agnus/DDF/DDF/single4](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/single4) | single4_ocs | A500 OCS | 6 | x 890–896, y 144–256 | [single4_ocs.png](Agnus/DDF/DDF/single4/single4_ocs.png) |
| [Agnus/DDF/DDF/single5](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/single5) | single5_ecs | A500 ECS | 6 | x 890–896, y 144–256 | [single5_ecs.png](Agnus/DDF/DDF/single5/single5_ecs.png) |
| [Agnus/Registers/DMACON/bpumod4](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/DMACON/bpumod4) | bpumod4_ecs | A500 ECS | 6 | x 412–417, y 80 | [bpumod4_ecs.png](Agnus/Registers/DMACON/bpumod4/bpumod4_ecs.png) |
| [Agnus/Registers/DMACON/bpumod4](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/DMACON/bpumod4) | bpumod4_ocs | A500 OCS | 6 | x 412–417, y 80 | [bpumod4_ocs.png](Agnus/Registers/DMACON/bpumod4/bpumod4_ocs.png) |
| [Denise/Registers/BPLCON1/overscan6b](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Denise/Registers/BPLCON1/overscan6b) | overscan6b | A500 ECS | 6 | x 890–897, y 144–256 | [overscan6b.png](Denise/Registers/BPLCON1/overscan6b/overscan6b.png) |
| [Denise/Sprites/clip/clip2h](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Denise/Sprites/clip/clip2h) | clip2h | A500 ECS | 6 | x 364–429, y 128–288 | [clip2h.png](Denise/Sprites/clip/clip2h/clip2h.png) |
| [Agnus/Blitter/dmacon/dmacon1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Blitter/dmacon/dmacon1) | dmacon1 | A500 ECS | 8 | x 232–673, y 160–208 | [dmacon1.png](Agnus/Blitter/dmacon/dmacon1/dmacon1.png) |
| [Agnus/Blitter/dmacon/dmacon2](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Blitter/dmacon/dmacon2) | dmacon2 | A500 ECS | 8 | x 232–665, y 160–208 | [dmacon2.png](Agnus/Blitter/dmacon/dmacon2/dmacon2.png) |
| [Agnus/Blitter/dmacon/dmacon3](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Blitter/dmacon/dmacon3) | dmacon3 | A500 ECS | 8 | x 232–665, y 160–208 | [dmacon3.png](Agnus/Blitter/dmacon/dmacon3/dmacon3.png) |
| [Agnus/Blitter/dmacon/dmacon4](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Blitter/dmacon/dmacon4) | dmacon4 | A500 ECS | 8 | x 232–665, y 160–208 | [dmacon4.png](Agnus/Blitter/dmacon/dmacon4/dmacon4.png) |
| [Agnus/Blitter/dmacon/dmacon5](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Blitter/dmacon/dmacon5) | dmacon5 | A500 ECS | 8 | x 232–665, y 160–208 | [dmacon5.png](Agnus/Blitter/dmacon/dmacon5/dmacon5.png) |
| [Agnus/Blitter/dmacon/dmacon6](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Blitter/dmacon/dmacon6) | dmacon6 | A500 ECS | 8 | x 232–665, y 160–208 | [dmacon6.png](Agnus/Blitter/dmacon/dmacon6/dmacon6.png) |
| [Agnus/Blitter/dmacon/dmacon7](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Blitter/dmacon/dmacon7) | dmacon7 | A500 ECS | 8 | x 232–673, y 160–208 | [dmacon7.png](Agnus/Blitter/dmacon/dmacon7/dmacon7.png) |
| [Agnus/Blitter/dmacon/dmacon8](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Blitter/dmacon/dmacon8) | dmacon8 | A500 ECS | 8 | x 232–665, y 160–208 | [dmacon8.png](Agnus/Blitter/dmacon/dmacon8/dmacon8.png) |
| [Agnus/Blitter/dmacon/dmacon9](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Blitter/dmacon/dmacon9) | dmacon9 | A500 ECS | 8 | x 232–665, y 160–162 | [dmacon9.png](Agnus/Blitter/dmacon/dmacon9/dmacon9.png) |
| [Agnus/Registers/oldDMACON/bplen1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/oldDMACON/bplen1) | bplen1_OCS | A500 OCS | 8 | x 698–705, y 256 | [bplen1_OCS.png](Agnus/Registers/oldDMACON/bplen1/bplen1_OCS.png) |
| [Agnus/Registers/oldDMACON/bplen2](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/oldDMACON/bplen2) | bplen2_ECS | A500 ECS | 8 | x 674–681, y 192 | [bplen2_ECS.png](Agnus/Registers/oldDMACON/bplen2/bplen2_ECS.png) |
| [Agnus/Registers/oldDMACON/oldbplen1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/oldDMACON/oldbplen1) | oldbplen1_OCS | A500 OCS | 8 | x 698–705, y 256 | [oldbplen1_OCS.png](Agnus/Registers/oldDMACON/oldbplen1/oldbplen1_OCS.png) |
| [Agnus/Registers/oldDMACON/oldbplen2](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/oldDMACON/oldbplen2) | oldbplen2_ECS | A500 ECS | 8 | x 674–681, y 192 | [oldbplen2_ECS.png](Agnus/Registers/oldDMACON/oldbplen2/oldbplen2_ECS.png) |
| [Agnus/Registers/DMACON/bpumod1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/DMACON/bpumod1) | bpumod1_ecs | A500 ECS | 12 | x 412–481, y 72–80 | [bpumod1_ecs.png](Agnus/Registers/DMACON/bpumod1/bpumod1_ecs.png) |
| [Agnus/Registers/DMACON/bpumod1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/DMACON/bpumod1) | bpumod1_ocs | A500 OCS | 12 | x 412–481, y 72–80 | [bpumod1_ocs.png](Agnus/Registers/DMACON/bpumod1/bpumod1_ocs.png) |
| [Agnus/Registers/DMACON/resmod3](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/DMACON/resmod3) | resmod3_ecs | A500 ECS | 15 | x 450–479, y 104–120 | [resmod3_ecs.png](Agnus/Registers/DMACON/resmod3/resmod3_ecs.png) |
| [Agnus/Registers/DMACON/resmod3](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/DMACON/resmod3) | resmod3_ocs | A500 OCS | 15 | x 450–479, y 104–120 | [resmod3_ocs.png](Agnus/Registers/DMACON/resmod3/resmod3_ocs.png) |
| [Agnus/Copper/Skip/copskip1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/Skip/copskip1) | copskip1_ecs | A500 ECS | 16 | x 196–911, y 171–172 | [copskip1_ecs.png](Agnus/Copper/Skip/copskip1/copskip1_ecs.png) |
| [Agnus/Copper/Skip/copskip1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/Skip/copskip1) | copskip1_ocs | A500 OCS | 16 | x 196–911, y 171–172 | [copskip1_ocs.png](Agnus/Copper/Skip/copskip1/copskip1_ocs.png) |
| [CPU/Misc/Order/moveorder1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Misc/Order/moveorder1) | moveorder1_68000 | A500 ECS | 16 | x 416–481, y 81–87 | [moveorder1_68000.png](CPU/Misc/Order/moveorder1/moveorder1_68000.png) |
| [Denise/Sprites/general/sprbpu1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Denise/Sprites/general/sprbpu1) | sprbpu1_ECS | A500 ECS | 16 | x 412–735, y 57–289 | [sprbpu1_ECS.png](Denise/Sprites/general/sprbpu1/sprbpu1_ECS.png) |
| [Denise/Sprites/general/sprbpu1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Denise/Sprites/general/sprbpu1) | sprbpu1_OCS | A500 OCS | 16 | x 412–735, y 57–289 | [sprbpu1_OCS.png](Denise/Sprites/general/sprbpu1/sprbpu1_OCS.png) |
| [Agnus/DDF/DDF/ddf10](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/ddf10) | ddf10_ecs | A500 ECS | 18 | x 890–911, y 144–256 | [ddf10_ecs.png](Agnus/DDF/DDF/ddf10/ddf10_ecs.png) |
| [Agnus/DDF/DDF/ddf2](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/ddf2) | ddf2_ecs | A500 ECS | 18 | x 890–911, y 144–256 | [ddf2_ecs.png](Agnus/DDF/DDF/ddf2/ddf2_ecs.png) |
| [Agnus/DDF/DDF/ddf3](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/ddf3) | ddf3_ecs | A500 ECS | 18 | x 890–911, y 144–256 | [ddf3_ecs.png](Agnus/DDF/DDF/ddf3/ddf3_ecs.png) |
| [Agnus/DDF/DDF/ddf6](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/ddf6) | ddf6_ecs | A500 ECS | 18 | x 890–911, y 144–256 | [ddf6_ecs.png](Agnus/DDF/DDF/ddf6/ddf6_ecs.png) |
| [Agnus/DDF/DDF/ddf7](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/DDF/DDF/ddf7) | ddf7_ecs | A500 ECS | 18 | x 890–911, y 144–256 | [ddf7_ecs.png](Agnus/DDF/DDF/ddf7/ddf7_ecs.png) |
| [Agnus/Registers/DMACON/bpumod2](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/DMACON/bpumod2) | bpumod2_ecs | A500 ECS | 18 | x 412–481, y 80–112 | [bpumod2_ecs.png](Agnus/Registers/DMACON/bpumod2/bpumod2_ecs.png) |
| [Agnus/Registers/DMACON/bpumod2](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/DMACON/bpumod2) | bpumod2_ocs | A500 OCS | 18 | x 412–481, y 80–112 | [bpumod2_ocs.png](Agnus/Registers/DMACON/bpumod2/bpumod2_ocs.png) |
| [Agnus/Registers/DMACON/bpumod3](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/DMACON/bpumod3) | bpumod3_ecs | A500 ECS | 18 | x 412–481, y 80–112 | [bpumod3_ecs.png](Agnus/Registers/DMACON/bpumod3/bpumod3_ecs.png) |
| [Agnus/Registers/DMACON/bpumod3](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Registers/DMACON/bpumod3) | bpumod3_ocs | A500 OCS | 18 | x 412–481, y 80–112 | [bpumod3_ocs.png](Agnus/Registers/DMACON/bpumod3/bpumod3_ocs.png) |
| [Agnus/Copper/Wait/waitblt5](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/Wait/waitblt5) | waitblt5_ecs | A500 ECS | 20 | x 420–855, y 240–260 | [waitblt5_ecs.png](Agnus/Copper/Wait/waitblt5/waitblt5_ecs.png) |
| [Agnus/Copper/Wait/waitblt5](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/Wait/waitblt5) | waitblt5_ocs | A500 OCS | 20 | x 420–855, y 240–260 | [waitblt5_ocs.png](Agnus/Copper/Wait/waitblt5/waitblt5_ocs.png) |
| [Agnus/Copper/oldJump/jump3a](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/oldJump/jump3a) | jump3a_ecs | A500 ECS | 20 | x 196–287, y 248–254 | [jump3a_ecs.png](Agnus/Copper/oldJump/jump3a/jump3a_ecs.png) |
| [Agnus/Copper/oldJump/jump3a](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Agnus/Copper/oldJump/jump3a) | jump3a_ocs | A500 OCS | 20 | x 196–287, y 248–254 | [jump3a_ocs.png](Agnus/Copper/oldJump/jump3a/jump3a_ocs.png) |
