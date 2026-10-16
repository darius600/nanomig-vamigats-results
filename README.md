# nanomig-vamigats-results

Results of running the [vAmiga Test Suite](https://github.com/dirkwhoffmann/vAmigaTS) (vAmigaTS) against the [NanoMig](https://github.com/harbaum/NanoMig) core in a Verilator simulation.

Every frame is compared pixel by pixel with the test's `.raw` reference. **These references are screenshots made by the vAmiga emulator**, the baselines vAmigaTS uses for vAmiga's own regression tests. A `PASS` therefore means *identical to vAmiga*. The vAmigaTS test folders also hold photos of real Amiga screens (`*_A500_*.JPG`); only those show real hardware. [REFERENCES.md](./REFERENCES.md) explains this, which machines are compared, and the known cases where a reference contradicts the photo.

👉 **Start at [TestReport.md](./TestReport.md)**: summary, results per group, how far off the FAILs are.

## Contents

- **Group pages (`<Chip>_<Group>.md`):** one row per test variant with result, differing pixels, labels, the 2024 hand verdict where one exists, and a link to the image.
- **Images (`.png`)**, per compared variant: NanoMig | vAmigaTS reference | differences (differing pixels red, area outside the compared cutout shaded blue).
- **Captures (`.frame.vga.gz`):** NanoMig's raw VGA frame, so the comparison can be repeated without simulating.
- **`.result.json`:** per variant: class, differing pixels, configuration, versions and timing.

The simulation harness lives in a separate repository, which is private for now.

## Historical Hand Comparison (2024-08)

The previous manual comparison from August 2024 is preserved in git tag `manual-2024-08`. Note that `_ecs` screenshots in that tag originated from a simulation run without an ECS mode.
