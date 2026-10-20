# Misc_Init

- **NanoMig:** [4315acba5e9f1e15103037627aa78b3460cae8af](https://github.com/harbaum/NanoMig/commit/4315acba5e9f1e15103037627aa78b3460cae8af) | **vAmigaTS:** [e807e3256d73135f1960e7f9aef2c16d8a6a56b4](https://github.com/dirkwhoffmann/vAmigaTS/commit/e807e3256d73135f1960e7f9aef2c16d8a6a56b4)
- **Compared:** 4 (PASS 1, FAIL 3) | **ERROR:** 0 | **Not compared:** 1 (DEVIATING_CONFIG 1, NOT_CALIBRATED 0, NO_REFERENCE 0; listed at the end)

| Test | Variant | Machine | Result | Differing px | Labels | Hand 2024 | Hand comment | Image |
|---|---|---|---|---|---|---|---|---|
| Misc/Init/Registers/showcia1 | showcia1 | A500 ECS | FAIL | 988 |  |  |  | [showcia1.png](Misc/Init/Registers/showcia1/showcia1.png) |
| Misc/Init/Registers/showcia2 | showcia2 | A500 ECS | FAIL | 1038 |  |  |  | [showcia2.png](Misc/Init/Registers/showcia2/showcia2.png) |
| Misc/Init/Registers/showocs | showocs | A500 ECS | FAIL | 44 | `denise-ecs-sensitive` |  |  | [showocs.png](Misc/Init/Registers/showocs/showocs.png) |
| Misc/Init/Registers/showregs | showregs1 | A500 ECS | PASS | 0 | `denise-ecs-sensitive` |  |  | [showregs1.png](Misc/Init/Registers/showregs/showregs1.png) |

## Not compared

| Test | Variant | Machine | Result | Reason | Labels |
|---|---|---|---|---|---|
| Misc/Init/Registers/showregs | showregs2 | A500 ECS | DEVIATING_CONFIG | unsupported: cpu set RESET_VAL 0xFFFFFFFF | `denise-ecs-sensitive` |
