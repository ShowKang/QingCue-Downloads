# Verification Scope and Known Limitations

This document states what has been verified and what has not. Automated results do not represent every user's experience in every environment.

## 1. Completed (Automated)

- Full lifecycle verification: install, launch, uninstall, and reinstall;
- Core functional regression: script loading, start and pause, sentence advancement, settings persistence, and diagnostics export;
- Installer integrity: SHA-256 matches the published value;
- Third-party licenses and attribution files ship with the package;
- Model delivery: the installer includes two compact starter models (about 101.7 MB combined); the primary model is downloaded in-app on first use and works offline afterwards.

No failures were found in this round of verification.

## 2. Not Verified (Must Not Be Treated as Passed)

1. Following quality and physical response latency during live human reading (measured from speaking to visual response).
2. Behavior with fast or slow speech, pauses, repetition, re-reading, and skipped passages in live reading.
3. Page-by-page human visual review of interface changes.
4. Layout and scrolling across DPI settings, multiple monitors, and scaling levels.
5. External devices such as phones or remotes.
6. Real offline scenarios, including failure and recovery of the first model download.
7. Commercial code signing: the installer is currently unsigned, so a SmartScreen prompt may appear on first run.
8. Interface behavior and model download under enterprise network policies or proxies.

## 3. How to Read These Results

- Automated verification covers determinable behavior and flows, not subjective experience or physical latency.
- "No failures found" does not mean the experience has been accepted; public statements should reference the unverified list as well.
- Before production use, read a short section of your own script on your own device.

Detailed records remain in internal materials and are not distributed with this public repository.
