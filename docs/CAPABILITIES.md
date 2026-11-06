# Capabilities and Boundaries

This document describes what QingCue does, the conditions under which behavior is not guaranteed, and which areas remain unverified. Unverified areas are listed in [TESTING.md](TESTING.md).

Status definitions:

- **Available** — the feature is usable in the installed app.
- **Conditional** — works under specific conditions; outside them, no guarantee is made.
- **Not verified** — no live human or hardware evidence yet; not a commitment.

## 1. Natural Speech Following

**Available; the local speech model is conditional.**

With the microphone enabled, read the script aloud and the view advances with your voice. No manual paging is needed. Speech recognition runs on your device.

**Conditional:** the installer includes two compact starter models (about 101.7 MB combined). The primary speech model (about 900 MB) is downloaded in-app on first use; speech following works offline afterwards. Fixed-speed prompting does not require any model.

**Not guaranteed when:**

- ambient noise is at or above reading volume, or several people speak at once;
- the microphone is too far away, gain is too low, or another application holds exclusive access;
- the reading differs substantially from the script (free improvisation, long passages outside the script);
- dialects, accents, or dense technical terminology fall outside the model's coverage.

## 2. Word-level Highlighting and Continuous Scrolling

**Available.** The highlight moves word by word, the view scrolls continuously, and surrounding lines stay in view.

**Boundaries:**

- Appearance across window sizes, scaling factors, and display DPI has not been verified item by item.
- Very narrow windows or very large text reduce the visible area and affect reading rhythm.

## 3. Pauses, Repeats, Re-reads, and Skips

| Behavior | Status | What the user sees |
| --- | --- | --- |
| Normal pause | Available | The view holds its position and does not jump during silence. |
| Repeating a sentence | Available | Progress stays on the current sentence instead of moving ahead. |
| Re-reading the previous sentence | Conditional | The position is usually kept; large re-reads are not strongly guaranteed. |
| Skipping a sentence or paragraph | Conditional | The view catches up when later text is read; large jumps may hold first, then catch up. |
| Slips of the tongue and corrections | Conditional | Progress usually stays anchored; many consecutive corrections may hold it in place. |
| Speaking outside the script | Not guaranteed | Off-script speech does not advance the view; extended departures may hold it in place. |

Live human-read behavior for these cases has not been verified.

## 4. Sentence Handoff

**Available.** When the current sentence is finished, the highlight moves forward and the view scrolls to the next sentence.

- Depends on sensible script segmentation; unusually long sentences or irregular paragraph structure reduce the quality of the handoff.

## 5. Floating Teleprompter Window

**Available.** A separate always-on-top window with adjustable position and size that can run alongside other applications.

- Whether the floating window and main window overlap is controlled by the user.
- Window behavior on multiple monitors and mixed DPI is not verified.

## 6. Fixed-Speed Prompting

**Available.** With speech following disabled, the script advances at a configured pace.

- Needs no model and no microphone.
- Drift from your actual speaking pace is inherent to this mode.

## 7. Scripts and Data

**Available.** Plain text and Markdown scripts can be imported; scripts, settings, and models stay on your device.

**Boundaries:**

- Tables, nested lists, and mixed media layouts are treated as plain text and are not reproduced faithfully.
- First-screen loading and search for very long scripts are not specifically optimized.

## 8. Runtime Environment

**Available.** Windows 10 / 11 x64, MSI installation, self-contained runtime, no separate VC++ redistributable.

**Conditional / not verified:**

- interface behavior under enterprise policy restrictions;
- multiple monitors with mixed DPI;
- external devices such as phones or remotes;
- first model download while offline (offline use works once all models are present).

## 9. Explicit Non-Goals

- multi-user collaboration, cloud sync, or accounts;
- automatic script generation, rewriting, or semantic question answering;
- uploading or archiving readings, or using them for training;
- scoring the quality of a delivery (volume, emotion, pacing).
