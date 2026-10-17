# nanomig-vamigats-results

Results of running the [vAmiga Test Suite](https://github.com/dirkwhoffmann/vAmigaTS) (vAmigaTS) against the [NanoMig](https://github.com/harbaum/NanoMig) core in a Verilator simulation.

NanoMig is based on the [MiSTer Minimig-AGA](https://github.com/MiSTer-devel/Minimig-AGA_MiSTer) code (NanoMig's README says so), so a FAIL here may concern other Minimig-derived cores as well. Whether it does has to be checked on that core.

Every frame is compared pixel by pixel with the test's `.raw` reference. **These references are screenshots made by the vAmiga emulator**, the baselines vAmigaTS uses for vAmiga's own regression tests. A `PASS` therefore means *identical to vAmiga*. The vAmigaTS test folders also hold photos of real Amiga screens (`*_A500_*.JPG`); only those show real hardware. [REFERENCES.md](./REFERENCES.md) explains this, which machines are compared, and the known cases where a reference contradicts the photo.

👉 **Start at [TestReport.md](./TestReport.md)**: the FAILs closest to the reference first, then the summary, the results per group and how far off the FAILs are.

## Contents

- **Group pages (`<Chip>_<Group>.md`):** one row per compared variant with machine, result, differing pixels, labels, the 2024 hand verdict where one exists, and a link to the image; the variants that were not compared follow at the end, with the reason.
- **Images (`.png`)**, per compared variant: NanoMig | vAmigaTS reference | differences (differing pixels red, area outside the compared cutout shaded blue). Positions in the titles are vAmiga's coordinates (x 196–911, y 26–310).
- **Captures (`.frame.vga.gz`):** NanoMig's raw VGA frame, so the comparison can be repeated without simulating.
- **`.result.json`:** per variant: class, differing pixels, machine, labels, configuration, versions and timing.

## Running it yourself

The harness, the comparison and the commands are in [nanomig-vamigats-regression](https://github.com/darius600/nanomig-vamigats-regression). Its README shows how to run one test or a group, also against your own NanoMig checkout, and how to compare that run with these results (`loader.vs_published`).

## Historical Hand Comparison (2024-08)

The previous manual comparison from August 2024 is preserved in git tag `manual-2024-08`. Note that `_ecs` screenshots in that tag originated from a simulation run without an ECS mode.
