### vAmiga Test Executions

This is a work in progress. So far, the test cases under [Agnus/Blitter](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter) have been executed.

### Blitter Test Cases
NanoMig Verilator results under: [Agnus/Blitter](https://github.com/darius600/NanoMig-vAmigaTS-Results/tree/main/Agnus/Blitter)    

| vAmiga Test Cases                                                                                               | Status   | Comment  |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|
| [Agnus/Blitter/bbusy](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/bbusy)                | Executed | Slight differences in timing.  |
| [Agnus/Blitter/bltint](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/bltint)              | Executed | Different results for `bltint1`, `bltint4`, and `bltint5`; otherwise, slight differences in timing.  |
| [Agnus/Blitter/bususage](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/bususage)          | Executed | Slight differences in timing.   |
| [Agnus/Blitter/cputim](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/cputim)              | Executed | `cputim*` and `invible*` show differences in timing.   |
| [Agnus/Blitter/dmacon](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/dmacon)              | Executed | `dmaoff1` slightly different in the first lines; `dmacon*` are *identical*.  |
| [Agnus/Blitter/fill](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/fill)                  | Executed | *identical*  |
| [Agnus/Blitter/irqtim](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/irqtim)              | Executed | `irqtim1l` crashes Amiga in Verilator; otherwise slight differences in timing; `irqtim11l1`, `irqtim15l1` differ ("These tests are special because they run the line Blitter with an unusual width of 1").  |
| [Agnus/Blitter/line](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/line)                  | Executed | `bsh1` and `bsh2` *identical*; `bsh3` and `bsh4` different; `channels4` *identical*; `channels1`-`3` different; `combined*` *identical*; `line1`-`11` *identical*; `line12` and `line13`different; `mask*` *identical*; `start*` *identical*; `zero1` *identical*  |
| [Agnus/Blitter/misc](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/misc)                  | Executed | *identical*   |
| [Agnus/Blitter/race](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/race)                  | Executed | `race*`, `toggle1` slight differences   |
| [Agnus/Blitter/sblit](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/sblit)                | Executed | *identical*   |
| [Agnus/Blitter/timing](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/timing)              | Executed | *identical*; execpt for `timing1l`, `timing11l1`, `timing11l3`, `timing11l4`, `timing15l1`, `timing15l3`, `timing15l4`; `timing1l` crashes Amiga in Verilator. ("These tests are special because they run the line Blitter with an unsual width of 1, 3, or 4, respectively.") |
| [Agnus/Blitter/undocumented](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/undocumented)  | Executed | Differences in the red bars.   |
| [Agnus/Blitter/wrap](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/wrap)                  | Executed | *identical* (besides varying cutout).   |

### Copper Test Cases
NanoMig Verilator results under: [Agnus/Blitter](https://github.com/darius600/NanoMig-vAmigaTS-Results/tree/main/Agnus/Copper)    

| vAmiga Test Cases                                                                                            | Status   | Comment  |
|--------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Agnus/Copper/CopDma](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/CopDma)             | Open     |                                                                                                                                                         |
| [Agnus/Copper/Irq](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/Irq)                   | Open     |                                                                                                                                                         |
| [Agnus/Copper/Skip](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/Skip)                 | Open     |                                                                                                                                                         |
| [Agnus/Copper/Wait](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/Wait)                 | Open     |                                                                                                                                                         |
| [Agnus/Copper/copbpl](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/copbpl)             | Open     | `copbpl*` different                                                                                                                                                        |
| [Agnus/Copper/coprace](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/coprace)           | Open     |                                                                                                                                                         |
| [Agnus/Copper/coptim](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/coptim)             | Open     |                                                                                                                                                         |
| [Agnus/Copper/copvbl](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/copvbl)             | Open     |                                                                                                                                                         |
| [Agnus/Copper/cross](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/cross)               | Open     |                                                                                                                                                         |
| [Agnus/Copper/halt](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/halt)                 | Open     |                                                                                                                                                         |
| [Agnus/Copper/lc](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/lc)                     | Open     |                                                                                                                                                         |
| [Agnus/Copper/mask](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/mask)                 | Open     |                                                                                                                                                         |
| [Agnus/Copper/oldJump](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/oldJump)          | Open     |                                                                                                                                                         |

copblt1* *identical*


### DDF Test Cases
NanoMig Verilator results under: [Agnus/DDF](https://github.com/darius600/NanoMig-vAmigaTS-Results/tree/main/Agnus/DDF)    

| vAmiga Test Cases                                                                           | Status   | Comment  |
|--------------------------------------------------------------------------------------------------------|----------|
| [Agnus/DDF/DDF](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/DDF/DDF)        | Executed |  `ddf*`, `dmaslots*`, `farright*`, `lupo1*`, `reenable*`, `shift*`, `single*` *identical* (except 1,2,4 ECS); `hwstop*`, `oldhwstop*` (except 3,4 OCS); `hwstop1_ECS`, `hwstop2_ECS`, `hwstop3_OCS`, `hwstop4_OCS`, `hwstop5_OCS`, `hwstop6_OCS`, `hwstop8_ECS`, `oldhwstop3_OCS`, `oldhwstop4_OCS`, `single1_ECS`, `single2_ECS`, `single4_ECS`  different |
| [Agnus/DDF/DDFTIM](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/DDF/DDFTIM)  | Executed | `ddftimcop*` *identical*; `ddftimcpu*` different |


### DIW Test Cases
NanoMig Verilator results under: [Agnus/DIW](https://github.com/darius600/NanoMig-vAmigaTS-Results/tree/main/Agnus/DIW)    

| vAmiga Test Cases                                                                                                   | Status   | Comment                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Agnus/DIW/DIWV](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/DIW/DIWV)             | Open     |                                                                                                                                                         |
| [Agnus/DIW/OLDDIW](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/DIW/OLDDIW)             | Open     |                                                                                                                                                         |



### Misc Test Cases
NanoMig Verilator results under: [Agnus/Misc](https://github.com/darius600/NanoMig-vAmigaTS-Results/tree/main/Agnus/Misc)    

| vAmiga Test Cases                                                                                                   | Status   | Comment                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Agnus/Misc/NTSC](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Misc/NTSC)             | Open     |                                                                                                                                                         |


### Registers Test Cases
NanoMig Verilator results under: [Agnus/Registers](https://github.com/darius600/NanoMig-vAmigaTS-Results/tree/main/Agnus/Registers)    

| vAmiga Test Cases                                                                                                   | Status   | Comment                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Agnus/Registers/BPLMOD](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Registers/BPLMOD)             | Open     |                                                                                                                                                         |
| [Agnus/Registers/BPLPTR](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Registers/BPLPTR)                   | Open     |                                                                                                                                                         |
| [Agnus/Registers/DMACON](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Registers/DMACON)                 | Open     |                                                                                                                                                         |
| [Agnus/Registers/VPOS](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Registers/VPOS)                 | Open     | ersy2 hangs the Verilator simulation "frame line length unexpectedly changed from 908 to 1343"; vhpos5 crashes Verilator simulation with "Segmentation fault" |


