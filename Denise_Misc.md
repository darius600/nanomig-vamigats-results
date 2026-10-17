# Denise_Misc

- **NanoMig:** [0f3d2fdac8dd7097127d07d78029c31f3758c32c](https://github.com/harbaum/NanoMig/commit/0f3d2fdac8dd7097127d07d78029c31f3758c32c) | **vAmigaTS:** [e807e3256d73135f1960e7f9aef2c16d8a6a56b4](https://github.com/dirkwhoffmann/vAmigaTS/commit/e807e3256d73135f1960e7f9aef2c16d8a6a56b4)
- **Compared:** 7 (PASS 4, FAIL 3) | **ERROR:** 0 | **Not compared:** 2 (DEVIATING_CONFIG 2, NOT_CALIBRATED 0, NO_REFERENCE 0; listed at the end)

| Test | Variant | Machine | Result | Differing px | Labels | Hand 2024 | Hand comment | Image |
|---|---|---|---|---|---|---|---|---|
| Denise/Misc/Id/agacheck | agacheck_ecs | A500 ECS | PASS | 0 | `denise-ecs-sensitive` |  |  | [agacheck_ecs.png](Denise/Misc/Id/agacheck/agacheck_ecs.png) |
| Denise/Misc/Id/agacheck | agacheck_ocs | A500 OCS | PASS | 0 |  |  |  | [agacheck_ocs.png](Denise/Misc/Id/agacheck/agacheck_ocs.png) |
| Denise/Misc/Id/deniseid | deniseid_ecs | A500 ECS | FAIL | 10040 | `denise-ecs-sensitive` |  |  | [deniseid_ecs.png](Denise/Misc/Id/deniseid/deniseid_ecs.png) |
| Denise/Misc/Id/deniseid | deniseid_ocs | A500 OCS | PASS | 0 |  |  |  | [deniseid_ocs.png](Denise/Misc/Id/deniseid/deniseid_ocs.png) |
| Denise/Misc/Overscan/overscan2 | overscan2 | A500 ECS | PASS | 0 | `denise-ecs-sensitive` |  |  | [overscan2.png](Denise/Misc/Overscan/overscan2/overscan2.png) |
| Denise/Misc/ThirdParty/losso | bplcon_rmb_ECS | A500 ECS | FAIL | 3020 |  |  |  | [bplcon_rmb_ECS.png](Denise/Misc/ThirdParty/losso/bplcon_rmb_ECS.png) |
| Denise/Misc/ThirdParty/losso | bplcon_rmb_OCS | A500 OCS | FAIL | 3020 |  |  |  | [bplcon_rmb_OCS.png](Denise/Misc/ThirdParty/losso/bplcon_rmb_OCS.png) |

## Not compared

| Test | Variant | Machine | Result | Reason | Labels |
|---|---|---|---|---|---|
| Denise/Misc/ThirdParty/losso | bplcon_rmb2_ECS | A500 ECS | DEVIATING_CONFIG | input |  |
| Denise/Misc/ThirdParty/losso | bplcon_rmb2_OCS | A500 OCS | DEVIATING_CONFIG | input |  |
