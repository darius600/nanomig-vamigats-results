# Paula/Drive

- **NanoMig:** [4315acba5e9f1e15103037627aa78b3460cae8af](https://github.com/MiSTle-Dev/NanoMig/commit/4315acba5e9f1e15103037627aa78b3460cae8af) | **vAmigaTS:** [e807e3256d73135f1960e7f9aef2c16d8a6a56b4](https://github.com/dirkwhoffmann/vAmigaTS/commit/e807e3256d73135f1960e7f9aef2c16d8a6a56b4)
- **Compared:** 6 (PASS 0, FAIL 6) | **ERROR:** 0 | **Not compared:** 1 (DEVIATING_CONFIG 1, NOT_CALIBRATED 0, NO_REFERENCE 0; listed at the end)
- **How to read:** a PASS is identical to vAmiga's screenshot of the test, not to a photo of real hardware; classes and labels are explained in [TestReport.md](TestReport.md#how-to-read), the references in [REFERENCES.md](REFERENCES.md).

| Test | Variant | Machine | Result | Differing px | Labels | Image |
|---|---|---|---|---|---|---|
| [Paula/Drive/read/read1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Paula/Drive/read/read1) | read1 | A500 ECS | FAIL | 3936 | `synccpu` | [read1.png](Paula/Drive/read/read1/read1.png) |
| [Paula/Drive/read/read2](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Paula/Drive/read/read2) | read2 | A500 ECS | FAIL | 3936 | `synccpu` | [read2.png](Paula/Drive/read/read2/read2.png) |
| [Paula/Drive/step/step1](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Paula/Drive/step/step1) | step1 | A500 ECS | FAIL | 8148 | `synccpu` | [step1.png](Paula/Drive/step/step1/step1.png) |
| [Paula/Drive/step/step2](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Paula/Drive/step/step2) | step2 | A500 ECS | FAIL | 9672 | `synccpu` | [step2.png](Paula/Drive/step/step2/step2.png) |
| [Paula/Drive/step/step3](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Paula/Drive/step/step3) | step3 | A500 ECS | FAIL | 16070 | `synccpu` | [step3.png](Paula/Drive/step/step3/step3.png) |
| [Paula/Drive/step/step4](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Paula/Drive/step/step4) | step4 | A500 ECS | FAIL | 8148 | `synccpu` | [step4.png](Paula/Drive/step/step4/step4.png) |

## Not compared

| Test | Variant | Machine | Result | Reason | Labels |
|---|---|---|---|---|---|
| [Paula/Drive/step/step5](https://github.com/dirkwhoffmann/vAmigaTS/tree/e807e3256d73135f1960e7f9aef2c16d8a6a56b4/Paula/Drive/step/step5) | step5 | A500 ECS | DEVIATING_CONFIG | df1-3 |  |
