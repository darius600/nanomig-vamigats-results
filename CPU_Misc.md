# CPU_Misc

- **NanoMig:** [4315acba5e9f1e15103037627aa78b3460cae8af](https://github.com/harbaum/NanoMig/commit/4315acba5e9f1e15103037627aa78b3460cae8af) | **vAmigaTS:** [e807e3256d73135f1960e7f9aef2c16d8a6a56b4](https://github.com/dirkwhoffmann/vAmigaTS/commit/e807e3256d73135f1960e7f9aef2c16d8a6a56b4)
- **Compared:** 21 (PASS 6, FAIL 15) | **ERROR:** 0 | **Not compared:** 20 (DEVIATING_CONFIG 20, NOT_CALIBRATED 0, NO_REFERENCE 0; listed at the end)

| Test | Variant | Machine | Result | Differing px | Labels | Hand 2024 | Hand comment | Image |
|---|---|---|---|---|---|---|---|---|
| CPU/Misc/Btstipl/btst_ipl | btst_ipl | A500 ECS | FAIL | 276 |  |  |  | [btst_ipl.png](CPU/Misc/Btstipl/btst_ipl/btst_ipl.png) |
| CPU/Misc/Order/moveorder1 | moveorder1_68000 | A500 ECS | FAIL | 16 |  |  |  | [moveorder1_68000.png](CPU/Misc/Order/moveorder1/moveorder1_68000.png) |
| CPU/Misc/Prefetch/prefetch1 | prefetch1_68000 | A500 ECS | PASS | 0 |  |  |  | [prefetch1_68000.png](CPU/Misc/Prefetch/prefetch1/prefetch1_68000.png) |
| CPU/Misc/Prefetch/prefetch2 | prefetch2_68000 | A500 ECS | PASS | 0 |  |  |  | [prefetch2_68000.png](CPU/Misc/Prefetch/prefetch2/prefetch2_68000.png) |
| CPU/Misc/Prefetch/prefetch3 | prefetch3_68000 | A500 ECS | PASS | 0 |  |  |  | [prefetch3_68000.png](CPU/Misc/Prefetch/prefetch3/prefetch3_68000.png) |
| CPU/Misc/Prefetch/prefetch4 | prefetch4_68000 | A500 ECS | PASS | 0 |  |  |  | [prefetch4_68000.png](CPU/Misc/Prefetch/prefetch4/prefetch4_68000.png) |
| CPU/Misc/Prefetch/prefetch5 | prefetch5_68000 | A500 ECS | PASS | 0 |  |  |  | [prefetch5_68000.png](CPU/Misc/Prefetch/prefetch5/prefetch5_68000.png) |
| CPU/Misc/Prefetch/prefetch6 | prefetch6_68000 | A500 ECS | PASS | 0 |  |  |  | [prefetch6_68000.png](CPU/Misc/Prefetch/prefetch6/prefetch6_68000.png) |
| CPU/Misc/Timing/timing1 | timing1_68000 | A500 ECS | FAIL | 64902 |  |  |  | [timing1_68000.png](CPU/Misc/Timing/timing1/timing1_68000.png) |
| CPU/Misc/Timing/timing2 | timing2_68000 | A500 ECS | FAIL | 9548 |  |  |  | [timing2_68000.png](CPU/Misc/Timing/timing2/timing2_68000.png) |
| CPU/Misc/Timing/timing3 | timing3_68000 | A500 ECS | FAIL | 8968 |  |  |  | [timing3_68000.png](CPU/Misc/Timing/timing3/timing3_68000.png) |
| CPU/Misc/Timing/timing4 | timing4_68000 | A500 ECS | FAIL | 9700 |  |  |  | [timing4_68000.png](CPU/Misc/Timing/timing4/timing4_68000.png) |
| CPU/Misc/Timing/timing5 | timing5_68000 | A500 ECS | FAIL | 9790 |  |  |  | [timing5_68000.png](CPU/Misc/Timing/timing5/timing5_68000.png) |
| CPU/Misc/Timing/timing6 | timing6_68000 | A500 ECS | FAIL | 5978 |  |  |  | [timing6_68000.png](CPU/Misc/Timing/timing6/timing6_68000.png) |
| CPU/Misc/Timing/timing7 | timing7_68000 | A500 ECS | FAIL | 3926 |  |  |  | [timing7_68000.png](CPU/Misc/Timing/timing7/timing7_68000.png) |
| CPU/Misc/Trace/trace4 | trace4_68000 | A500 ECS | FAIL | 3354 |  |  |  | [trace4_68000.png](CPU/Misc/Trace/trace4/trace4_68000.png) |
| CPU/Misc/Trace/trace4b | trace4b_68000 | A500 ECS | FAIL | 3314 |  |  |  | [trace4b_68000.png](CPU/Misc/Trace/trace4b/trace4b_68000.png) |
| CPU/Misc/Trace/trace5 | trace5_68000 | A500 ECS | FAIL | 1310 |  |  |  | [trace5_68000.png](CPU/Misc/Trace/trace5/trace5_68000.png) |
| CPU/Misc/Trace/trace5b | trace5b_68000 | A500 ECS | FAIL | 4698 |  |  |  | [trace5b_68000.png](CPU/Misc/Trace/trace5b/trace5b_68000.png) |
| CPU/Misc/Trace/trace6 | trace6_68000 | A500 ECS | FAIL | 1124 |  |  |  | [trace6_68000.png](CPU/Misc/Trace/trace6/trace6_68000.png) |
| CPU/Misc/Trace/trace6b | trace6b_68000 | A500 ECS | FAIL | 3360 |  |  |  | [trace6b_68000.png](CPU/Misc/Trace/trace6b/trace6b_68000.png) |

## Not compared

| Test | Variant | Machine | Result | Reason | Labels |
|---|---|---|---|---|---|
| CPU/Misc/Order/moveorder1 | moveorder1_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Prefetch/prefetch1 | prefetch1_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Prefetch/prefetch2 | prefetch2_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Prefetch/prefetch3 | prefetch3_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Prefetch/prefetch4 | prefetch4_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Prefetch/prefetch5 | prefetch5_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Prefetch/prefetch6 | prefetch6_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Timing/timing1 | timing1_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Timing/timing2 | timing2_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Timing/timing3 | timing3_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Timing/timing4 | timing4_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Timing/timing5 | timing5_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Timing/timing6 | timing6_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Timing/timing7 | timing7_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Trace/trace4 | trace4_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Trace/trace4b | trace4b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Trace/trace5 | trace5_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Trace/trace5b | trace5b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Trace/trace6 | trace6_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
| CPU/Misc/Trace/trace6b | trace6b_68010 | A500 ECS | DEVIATING_CONFIG | cpu 68010 |  |
