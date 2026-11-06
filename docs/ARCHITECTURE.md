# Architecture Overview

This document describes QingCue at the product level: how the application is put together and which design directions it follows. It does not cover implementation methods, internal parameters, or internal workflows.

## 1. Form Factor

QingCue is a Windows desktop application for Windows 10 / 11 x64. Once installed it runs locally; the interface, speech processing, and data all stay on the user's machine.

## 2. Main Components

- **Desktop shell** — windows, always-on-top behavior, single-instance handling, shortcuts, and installation/upgrade.
- **Local interface** — script layout, continuous scrolling, highlighting, and reading presentation.
- **Local speech processing** — captures microphone input, performs speech recognition on the device, and reports reading progress to the interface.
- **Local data management** — stores scripts, settings, and diagnostics; data does not leave the device.

Components cooperate through in-process interfaces and do not depend on cloud services.

## 3. Privacy and Security Design

- Speech recognition runs on the device; audio is not uploaded.
- Scripts, settings, and diagnostics are stored locally and managed by the user.
- No account is required; there is no account system or cloud sync.
- Apart from the first model download, everyday use needs no external network connection.
- The installer is not commercially code-signed; SHA-256 verification is published with each release.

## 4. Distribution and Operation

- **Installed app** — per-user installation with data in the user directory; uninstall keeps data by default.
- **Portable mode** — data stored beside the program for easy relocation.
- **Offline operation** — once the local speech models are ready, losing the network does not affect prompting or speech following.

## 5. Design Principles

1. **Local first.** Anything that can run on the device does not run in the cloud.
2. **Graceful degradation.** If a model or microphone is unavailable, the app still works as a fixed-speed teleprompter.
3. **Experience first.** Architecture choices serve reading continuity rather than asking the user to adapt to technical constraints.

## 6. Public Boundary

This document does not describe recognition or synchronization methods, implementation values, internal module names, or diagnostic field definitions; those remain in a private repository. For feature scope see [CAPABILITIES.md](CAPABILITIES.md), and for verification scope see [TESTING.md](TESTING.md).
