# Engineering Challenges and Local Processing Requirements

This document explains, at a direction-setting level, the engineering problems QingCue addresses and the trade-offs behind its behavior. It does not provide reproducible implementation details.

## 1. Real-Time Speech Processing

Speech arrives continuously, while recognition results arrive in segments. Keeping the view in step with the speaker requires all three of the following:

- **Real time** — the gap between speaking and visual response must stay within a perceptible, reasonable range.
- **Sustained stability** — over extended sessions, performance must not degrade or memory grow without bound.
- **On-device execution** — inference runs on ordinary user hardware with limited compute and memory.

These goals pull against each other: more responsiveness calls for more frequent updates, while stability calls for more restrained movement.

## 2. Natural Delivery vs. Text Synchronization

Real reading is not uniform text playback:

- pace changes, including sudden acceleration or slowing mid-sentence;
- pauses, thinking, repetition, re-reading, and skipped passages;
- slips of the tongue, corrections, and off-script improvisation.

A teleprompter cannot check every character; it has to deliver a trustworthy reading position under these conditions. The difficulty is that recognition output is uncertain while the displayed position must be definite, continuous, and dependable.

## 3. Visual Continuity of Reading

Recognition produces discrete events; reading is continuous visual motion, and the two have inherently different granularity.

- updating too often makes the view jitter;
- updating too slowly lags noticeably during fast reading;
- over-smoothing fails to keep up when the pace changes abruptly.

QingCue favors stability: it would rather lag briefly than bounce the view back and forth. This choice directly shapes fast passages, pauses, and sentence handoffs.

## 4. Local Processing Requirements

- Speech recognition depends on local models: two compact starter models ship with the installer (about 101.7 MB combined), and the primary model is downloaded in-app on first use (about 900 MB). Offline use is available afterwards.
- Model loading and inference consume memory and CPU; performance on low-end hardware is affected.
- Audio, scripts, and settings stay on the device; no account is required and nothing passes through the cloud.
- The installer is self-contained, so users do not need to install developer tools or extra runtimes.

## 5. Trade-Offs

| Goal | Choice | Cost |
| --- | --- | --- |
| Privacy and control | Local recognition, no audio upload | Depends on user hardware performance |
| Reading stability | Stability takes priority for progress | Brief lag possible during abrupt pace changes |
| Broad compatibility | Self-contained installer | Larger installer size |
| Long-term availability | Models stored locally, usable offline | Model download required on first use |

## 6. Out of Scope for Public Documentation

Recognition and synchronization methods, decision thresholds, parameter values, debugging procedures, internal evaluation material, and diagnostic field definitions remain in a private repository and are not described publicly.

For feature scope see [CAPABILITIES.md](CAPABILITIES.md), and for verification scope see [TESTING.md](TESTING.md).
