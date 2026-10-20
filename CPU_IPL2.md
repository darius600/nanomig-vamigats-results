# CPU_IPL2

- **NanoMig:** [4315acba5e9f1e15103037627aa78b3460cae8af](https://github.com/harbaum/NanoMig/commit/4315acba5e9f1e15103037627aa78b3460cae8af) | **vAmigaTS:** [e807e3256d73135f1960e7f9aef2c16d8a6a56b4](https://github.com/dirkwhoffmann/vAmigaTS/commit/e807e3256d73135f1960e7f9aef2c16d8a6a56b4)
- **Compared:** 3 (PASS 0, FAIL 3) | **ERROR:** 0 | **Not compared:** 3 (DEVIATING_CONFIG 3, NOT_CALIBRATED 0, NO_REFERENCE 0; listed at the end)

| Test | Variant | Machine | Result | Differing px | Labels | Hand 2024 | Hand comment | Image |
|---|---|---|---|---|---|---|---|---|
| CPU/IPL2/AND/ANDCCR | ANDCCR_68000 | A500 ECS | FAIL | 3542 |  |  |  | [ANDCCR_68000.png](CPU/IPL2/AND/ANDCCR/ANDCCR_68000.png) |
| CPU/IPL2/BKPT/BKPT1 | BKPT1_68000 | A500 ECS | FAIL | 3268 |  |  |  | [BKPT1_68000.png](CPU/IPL2/BKPT/BKPT1/BKPT1_68000.png) |
| CPU/IPL2/MOVE1/moveRgRg | moveRgRg_68000 | A500 ECS | FAIL | 7036 |  |  |  | [moveRgRg_68000.png](CPU/IPL2/MOVE1/moveRgRg/moveRgRg_68000.png) |

## Not compared

| Test | Variant | Machine | Result | Reason | Labels |
|---|---|---|---|---|---|
| CPU/IPL2/AND/ANDCCR | ANDCCR_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/IPL2/BKPT/BKPT1 | BKPT1_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/IPL2/MOVE1/moveRgRg | moveRgRg_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
