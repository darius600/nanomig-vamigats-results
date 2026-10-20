# nanomig-vamigats-results

Results of running the [vAmiga Test Suite](https://github.com/dirkwhoffmann/vAmigaTS) (vAmigaTS) against the [NanoMig](https://github.com/MiSTle-Dev/NanoMig) core in a Verilator simulation.

NanoMig is based on the [MiSTer Minimig-AGA](https://github.com/MiSTer-devel/Minimig-AGA_MiSTer) code (NanoMig's README says so), so a FAIL here may concern other Minimig-derived cores as well. Whether it does has to be checked on that core.

Every frame is compared pixel by pixel with the test's `.raw` reference. **These references are screenshots made by the vAmiga emulator**, the baselines vAmigaTS uses for vAmiga's own regression tests. A `PASS` therefore means *identical to vAmiga*. The vAmigaTS test folders also hold photos of real Amiga screens (`*_A500_*.JPG`); only those show real hardware. [REFERENCES.md](./REFERENCES.md) explains this, which machines are compared, and the known cases where a reference contradicts the photo.

👉 **Start at [TestReport.md](./TestReport.md)**: summary, results per group, then where to start (the FAILs closest to the reference) and how far off the FAILs are.

## Contents

- **Group pages (`<Chip>_<Group>.md`):** one row per compared variant with its test (linked to vAmigaTS), machine, result, differing pixels, labels and a link to the image; the variants that were not compared follow at the end, with the reason.
- **Images (`.png`)**, per compared variant: NanoMig | vAmigaTS reference | differences (differing pixels red, area outside the compared cutout shaded blue). Positions in the titles are vAmiga's coordinates (x 196–911, y 26–310).
- **Captures (`.frame.vga.gz`):** NanoMig's raw VGA frame, so the comparison can be repeated without simulating: with a checkout of nanomig-vamigats-regression, `python3 -m loader.side_by_side <path>/<variant>.frame.vga.gz --out /tmp/check` compares a capture again and draws its image.
- **`.result.json`:** per variant: class, differing pixels, machine, labels, configuration, versions and timing.

## Running it yourself

The harness, the comparison and the commands are in [nanomig-vamigats-regression](https://github.com/darius600/nanomig-vamigats-regression). Its README shows how to run one test or a group, also against your own NanoMig checkout, and how to compare that run with these results (`loader.vs_published`).
