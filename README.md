# PyStudio Python Toolchain

Thin build-entry repository for PyStudio Python runtime packages.

This repository does not contain a Termux package tree. It calls the reusable
workflow in `vg188/pystudio-termux-builds`, which selects one of the managed
source forks:

- `primary`: `vg188/pystudio-termux-source-termux`
- `secondary`: `vg188/pystudio-termux-source-pacman`

Each run selects exactly one source. The normal source is `primary`; the
orchestrator can dispatch the same workflow with `secondary` or `tur` when a
package profile needs a different source. Source patches live in the managed
source forks and are archived in `pystudio-termux-builds/patches/source-adapters/`.
