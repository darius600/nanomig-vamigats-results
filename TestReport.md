### vAmiga Test Executions

This is a work in progress. So far, the test cases under [Agnus/Blitter](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter) have been executed.

### Blitter Test Cases
NanoMig Verilator results under: [Agnus/Blitter](https://github.com/darius600/NanoMig-vAmigaTS-Results/tree/main/Agnus/Blitter)    

| vAmiga Test Cases                                                                                               | Status   | Comment  |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|
| [Agnus/Blitter/bbusy](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/bbusy)                | Executed | `bbusy*` **❌ Different** Slight differences in timing.  |
| [Agnus/Blitter/bltint](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/bltint)              | Executed | `bltint*` **❌ Different** results for `bltint1`, `bltint4`, and `bltint5`<BR> otherwise, slight differences in timing.  |
| [Agnus/Blitter/bususage](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/bususage)          | Executed | `bususage*` **❌ Different** Slight differences in timing.   |
| [Agnus/Blitter/cputim](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/cputim)              | Executed | `cputim*`**❌ Different**<BR> `invible*` **❌ Different** |
| [Agnus/Blitter/dmacon](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/dmacon)              | Executed | `dmaoff1` **❌ Different** slightly in the first lines<BR> `dmacon*` **✅ Identical** |
| [Agnus/Blitter/fill](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/fill)                  | Executed | **✅ Identical**  |
| [Agnus/Blitter/irqtim](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/irqtim)              | Executed | **⚠️** `irqtim1l` crashes Amiga in Verilator;<BR>**❌ Different** Slight differences in timing; `irqtim11l1`, `irqtim15l1` differ ("These tests are special because they run the line Blitter with an unusual width of 1").  |
| [Agnus/Blitter/line](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/line)                  | Executed | `bsh1` and `bsh2` **✅ Identical**<BR> `bsh3` and `bsh4` **❌ Different**<BR> `channels4` **✅ Identical**<BR> `channels1`-`3` **❌ Different**<BR> `combined*` **✅ Identical**<BR> `line1`-`11` **✅ Identical**<BR> `line12` and `line13`**❌ Different**<BR> `mask*` **✅ Identical**<BR> `start*` **✅ Identical**<BR> `zero1` **✅ Identical**  |
| [Agnus/Blitter/misc](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/misc)                  | Executed | `barrel1` **✅ Identical** |
| [Agnus/Blitter/race](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/race)                  | Executed | `race*`**❌ Different** slight differences<BR> `toggle1` **❌ Different** slight differences   |
| [Agnus/Blitter/sblit](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/sblit)                | Executed | `sblit` **✅ Identical** |
| [Agnus/Blitter/timing](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/timing)              | Executed | `timing*` **✅ Identical**<BR> **❌** except for `timing1l`, `timing11l1`, `timing11l3`, `timing11l4`, `timing15l1`, `timing15l3`, `timing15l4`<BR> **⚠️** `timing1l` crashes Amiga in Verilator. ("These tests are special because they run the line Blitter with an unsual width of 1, 3, or 4, respectively.") |
| [Agnus/Blitter/undocumented](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/undocumented)  | Executed | `undocumented` **❌ Different** in the red bars.   |
| [Agnus/Blitter/wrap](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/wrap)                  | Executed | `wrap` **✅ Identical** (besides varying cutout).   |

### Copper Test Cases
NanoMig Verilator results under: [Agnus/Blitter](https://github.com/darius600/NanoMig-vAmigaTS-Results/tree/main/Agnus/Copper)    

| vAmiga Test Cases                                                                                            | Status   | Comment  |
|--------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Agnus/Copper/CopDma](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/CopDma)             | Executed | `cycleE0` **✅ Identical**<BR> `dasdma*` **✅ Identical**<BR> `dmatoggle1` **❌ Different**                                                                              |
| [Agnus/Copper/Irq](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/Irq)                   | Executed | `irq` **✅ Identical**                                                                                                                                       |
| [Agnus/Copper/Skip](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/Skip)                 | Executed | `copskip1*`**✅ Identical**<BR> `copstrt*`**✅ Identical**<BR> `skipbfd*`**✅ Identical**<BR>                                                                          |
| [Agnus/Copper/Wait](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/Wait)                 | Executed | `copwait*`**✅ Identical**<BR> `waitblt*` **✅ Identical**                                                                                                        |
| [Agnus/Copper/copbpl](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/copbpl)             | Executed | `copbpl*` **❌ Different**                                                                                                                                     |
| [Agnus/Copper/coprace](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/coprace)           | Executed | `coprace1` **✅ Identical**<BR> `coprace2_OCS` **✅ Identical**<BR> `coprace2_ECS` **❌ Different**                                                                            |
| [Agnus/Copper/coptim](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/coptim)             | Executed | `copblt1` **✅ Identical**<BR> `copcpu1` **❌ Different**<BR>  `coptim1` **✅ Identical**<BR> `oldcoptim` **✅ Identical**                                                    |
| [Agnus/Copper/copvbl](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/copvbl)             | Executed | `copvbl*` **❌ Different** in the grey bars (bit pattern beam position register VPOSR or VHPOSR)                                                             |
| [Agnus/Copper/cross](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/cross)               | Executed | `cross*` **✅ Identical**<BR> `steal*` **✅ Identical**                                                                                                             |
| [Agnus/Copper/halt](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/halt)                 | Executed | `halt*` **✅ Identical**                                                                                                                                                        |
| [Agnus/Copper/lc](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/lc)                     | Executed | `coplc*` **✅ Identical**, execept for<BR> **❌ Different**`coplc1b` and `coplc2b `("second Copper list")                                                                                                                                                       |
| [Agnus/Copper/mask](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Copper/mask)                 | Open     |                                                                                                                                                         |
| [Agnus/Copper/oldJump](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Blitter/oldJump)          | Executed |  `jump*` **✅ Identical**<BR> `jumpbpu*` **✅ Identical**                                                                                                                                                     |


### DDF Test Cases
NanoMig Verilator results under: [Agnus/DDF](https://github.com/darius600/NanoMig-vAmigaTS-Results/tree/main/Agnus/DDF)    

| vAmiga Test Cases                                                                      | Status   | Comment                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Agnus/DDF/DDF](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/DDF/DDF)    | Executed | `ddf*` **✅ Identical**<br> `dmaslots*` **✅ Identical**<br> `farright*` **✅ Identical**<br> `hwstop*` **✅ Identical**<br> `lupo1*` **✅ Identical**<br> `oldhwstop*` **✅ Identical** <br>`reenable*` **✅ Identical**<br> `shift*` **✅ Identical**<br> `single*` (except 1,2,4 ECS) **✅ Identical**<br><br> `doublematch1` **❌ Different**<br> `hwstop1_ECS`, `hwstop2_ECS`, `hwstop3_OCS`, `hwstop4_OCS`, `hwstop5_OCS`, `hwstop6_OCS`, `hwstop8_ECS` **❌ Different**<br> `oldhwstop3_OCS`, `oldhwstop4_OCS` **❌ Different**<br>  `single1_ECS`, `single2_ECS`, `single4_ECS` **❌ Different**<br> |
| [Agnus/DDF/DDFTIM](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/DDF/DDFTIM) | Executed | `ddftimcop*` **✅ Identical**<br> `ddftimcpu*` **❌ Different**                                                                                                                                                                                                    |




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
| [Agnus/Registers/VPOS](https://github.com/dirkwhoffmann/vAmigaTS/tree/master/Agnus/Registers/VPOS)                 | Open     | **⚠️** ersy2 hangs the Verilator simulation "frame line length unexpectedly changed from 908 to 1343"; **⚠️** vhpos5 crashes Verilator simulation with "Segmentation fault" |


