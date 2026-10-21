# CPU/Timing2

- **NanoMig:** [4315acba5e9f1e15103037627aa78b3460cae8af](https://github.com/MiSTle-Dev/NanoMig/commit/4315acba5e9f1e15103037627aa78b3460cae8af) | **vAmigaTS:** [e807e3256d73135f1960e7f9aef2c16d8a6a56b4](https://github.com/dirkwhoffmann/vAmigaTS/commit/e807e3256d73135f1960e7f9aef2c16d8a6a56b4)
- **Compared:** 7 (PASS 0, FAIL 7) | **ERROR:** 0 | **Not compared:** 37 (DEVIATING_CONFIG 37, NOT_CALIBRATED 0, NO_REFERENCE 0; listed at the end)
- **How to read:** a PASS is identical to vAmiga's screenshot of the test, not to a photo of real hardware; classes and labels are explained in [TestReport.md](TestReport.md#how-to-read), the references in [REFERENCES.md](REFERENCES.md).

| Test | Variant | Machine | Result | Differing px | Labels | Image |
|---|---|---|---|---|---|---|
| [CPU/Timing2/BKPT/BKPT1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/BKPT/BKPT1) | BKPT1_68000 | A500 ECS | FAIL | 12992 |  | [BKPT1_68000.png](CPU/Timing2/BKPT/BKPT1/BKPT1_68000.png) |
| [CPU/Timing2/MOVECCR/MOVECCR1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVECCR/MOVECCR1) | MOVECCR1_68000 | A500 ECS | FAIL | 12992 |  | [MOVECCR1_68000.png](CPU/Timing2/MOVECCR/MOVECCR1/MOVECCR1_68000.png) |
| [CPU/Timing2/MOVECCR/MOVECCR2](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVECCR/MOVECCR2) | MOVECCR2_68000 | A500 ECS | FAIL | 12992 |  | [MOVECCR2_68000.png](CPU/Timing2/MOVECCR/MOVECCR2/MOVECCR2_68000.png) |
| [CPU/Timing2/MOVECCR/MOVECCR3](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVECCR/MOVECCR3) | MOVECCR3_68000 | A500 ECS | FAIL | 12852 |  | [MOVECCR3_68000.png](CPU/Timing2/MOVECCR/MOVECCR3/MOVECCR3_68000.png) |
| [CPU/Timing2/MOVECCR/MOVECCR4](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVECCR/MOVECCR4) | MOVECCR4_68000 | A500 ECS | FAIL | 10214 |  | [MOVECCR4_68000.png](CPU/Timing2/MOVECCR/MOVECCR4/MOVECCR4_68000.png) |
| [CPU/Timing2/SEQ/SEQ1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/SEQ/SEQ1) | SEQ1_68000 | A500 ECS | FAIL | 27160 |  | [SEQ1_68000.png](CPU/Timing2/SEQ/SEQ1/SEQ1_68000.png) |
| [CPU/Timing2/SEQ/SEQ2](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/SEQ/SEQ2) | SEQ2_68000 | A500 ECS | FAIL | 12762 |  | [SEQ2_68000.png](CPU/Timing2/SEQ/SEQ2/SEQ2_68000.png) |

## Not compared

| Test | Variant | Machine | Result | Reason | Labels |
|---|---|---|---|---|---|
| [CPU/Timing2/BKPT/BKPT1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/BKPT/BKPT1) | BKPT1_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVECCR/MOVECCR1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVECCR/MOVECCR1) | MOVECCR1_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVECCR/MOVECCR2](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVECCR/MOVECCR2) | MOVECCR2_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVECCR/MOVECCR3](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVECCR/MOVECCR3) | MOVECCR3_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVECCR/MOVECCR4](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVECCR/MOVECCR4) | MOVECCR4_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES10b](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES10b) | MOVES10b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES10l](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES10l) | MOVES10l_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES10w](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES10w) | MOVES10w_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES11b](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES11b) | MOVES11b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES11l](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES11l) | MOVES11l_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES11w](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES11w) | MOVES11w_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES12b](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES12b) | MOVES12b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES12l](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES12l) | MOVES12l_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES12w](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES12w) | MOVES12w_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES1b](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES1b) | MOVES1b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES1l](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES1l) | MOVES1l_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES2b](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES2b) | MOVES2b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES2l](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES2l) | MOVES2l_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES3b](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES3b) | MOVES3b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES3l](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES3l) | MOVES3l_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES4b](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES4b) | MOVES4b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES4l](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES4l) | MOVES4l_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES5b](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES5b) | MOVES5b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES5l](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES5l) | MOVES5l_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES6b](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES6b) | MOVES6b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES6l](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES6l) | MOVES6l_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES7b](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES7b) | MOVES7b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES7l](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES7l) | MOVES7l_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES7w](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES7w) | MOVES7w_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES8b](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES8b) | MOVES8b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES8l](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES8l) | MOVES8l_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES8w](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES8w) | MOVES8w_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES9b](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES9b) | MOVES9b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES9l](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES9l) | MOVES9l_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/MOVES/MOVES9w](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/MOVES/MOVES9w) | MOVES9w_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/SEQ/SEQ1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/SEQ/SEQ1) | SEQ1_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| [CPU/Timing2/SEQ/SEQ2](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/CPU/Timing2/SEQ/SEQ2) | SEQ2_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
