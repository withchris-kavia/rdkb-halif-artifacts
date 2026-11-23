# RDK-B HAL Interface Artifacts

This repository contains [rdkb-halif-spec_l1l2_tests.zip](rdkb-halif-spec_l1l2_tests.zip), a bundle of RDK-B Hardware Abstraction Layer (HAL) specifications, interface headers, and L1/L2 C test sources.

## Archive contents

- `Halspecdocs/`: Per-component Markdown HAL specifications and supporting diagrams.
- `L1-L2TEST/`: Per-component interface headers (`include/`), test sources and support files (`ut/`), and build entry points (`build_ut.sh`).
- `__MACOSX/` and `.DS_Store`: macOS archive metadata; not project content.

Components include Wi-Fi, eMMC, MSO management, cable modem, MTA, bridge utilities, cellular, cellular modem, platform, DHCPv4 client, DHCPv6 client, Ethernet switch, EPON, firmware upgrade, MoCA, and LPA.

## Getting started

1. Extract the ZIP into a separate working directory.
2. Read the relevant specification under `Halspecdocs/rdkb-halif-<component>/`.
3. Inspect the matching headers, `ut/README.md`, build scripts, and Makefile under `L1-L2TEST/rdkb-halif-<component>/` before building.

This is an artifact bundle, not a standalone test distribution. For example, the eMMC test Makefile requires an existing `ut-core` setup with CUnit and `ut-control`; its Linux target uses skeleton implementations, while its ARM target links a vendor HAL library. Build and runtime requirements should be checked per component.

Preserve the bundled `LICENSE` and `NOTICE` files when reusing test material.
