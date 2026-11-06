# Changelog

## 0.1.17 + r13.3 (2026-11-03)

Installation and distribution revision. Prompting and speech following are unchanged.

- Added complete third-party license and attribution files, distributed with the installer.
- Published SHA-256 checksums so downloads can be verified.
- Improved package provenance details for build and version checks.
- System requirements and installation flow unchanged; in-place upgrade supported.
- Completed installation lifecycle and core automated regression checks.
- Scripts, settings, and local models are preserved through an upgrade.

Known limitations: live human-read following quality, visual review across DPI and multi-monitor setups, external devices, and a fully offline first-model scenario have not been verified.

## 0.1.17 + r13.2 (2026-10-30)

- Fixed an unresponsive Start button during state transitions.
- Start/play control now updates by state, reducing unnecessary redraws.
- Product version remains 0.1.17; the install revision increments and in-place upgrade is supported.
- Speech following, script data, and the reading workflow are unchanged.

## 0.1.17 (base release)

- Refined the teleprompter workbench, floating window, and script management.
- Speech following, continuous scrolling, and reading preferences available.
- Retained continuous text following and local processing.

## 0.1.16

- Tuned following behavior at the start of a session.
- Script structure and usage flow unchanged.

## 0.1.15

- Tuned following cadence to improve visual continuity while reading.
