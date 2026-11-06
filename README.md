<p align="center">
  <img src="./assets/brand/qingcue-logo-banner.png" alt="QingCue" width="520">
</p>

<h1 align="center">QingCue</h1>

<p align="center"><strong>A Natural Speech-Following Teleprompter for Windows.</strong></p>

<p align="center"><strong>Let your words keep pace with your voice.</strong></p>

<p align="center">QingCue is a Windows desktop teleprompter that follows your natural speech in real time, keeping your script synchronized with your delivery.</p>

<p align="center">
  <a href="https://github.com/ShowKang/QingCue-Teleprompter/releases/tag/v0.1.17-r13.3"><strong>Download for Windows</strong></a>
  &nbsp;·&nbsp; <code>0.1.17 + r13.3</code> &nbsp;·&nbsp; Windows 10 / 11 · x64
</p>

<p align="center">
  <img src="./assets/brand/badge-version.png" alt="Version 0.1.17 + r13.3" height="22">
  <img src="./assets/brand/badge-platform.png" alt="Windows 10 / 11 x64" height="22">
</p>

<p align="center"><strong>English</strong> | <a href="./README.zh-CN.md">简体中文</a></p>

---

## Why QingCue

Reading from a script usually means choosing between your message and your audience. QingCue removes that trade-off: your script stays in front of you, and the highlight moves with your voice instead of a timer or a foot pedal.

- **Your pace, not a preset speed.** Speak faster, slow down, pause, or repeat a line. The script waits for you and moves when you do.
- **Eyes where they belong.** The current line stays readable and the next sentence is already in view, so you never hunt for your place mid-sentence.
- **Nothing leaves your computer.** Microphone audio, speech recognition, and script data stay on your device. No account, no cloud round trip.
- **Works offline once set up.** After the primary speech model is downloaded, speech following keeps working without a network connection.

<p align="center">
  <img src="./assets/screenshots/workbench.png" alt="QingCue teleprompter workbench" width="100%">
</p>

The workbench brings the script tree, the current sentence, surrounding context, reading preferences, and progress into one window, so a session starts as soon as the app opens.

---

## See It in Action

<p align="center">
  <img src="./assets/demos/follow-demo.gif" alt="Natural speech following demo: start, pause, resume, and sentence handoff" width="880">
</p>

<p align="center"><sub><strong>Demo driven by a replayed audio sample, not a live human reading.</strong> The sample audio is generated locally; the interface is recorded from the running application without frame stitching.</sub></p>

The sequence shows the behavior that matters most: the highlight starts moving when you speak, freezes when you stop, resumes from the same place, and hands off to the next sentence without a visible jump.

---

## Key Features

| Feature | What it does |
| --- | --- |
| **Natural Speech Following** | Advances the highlight and scrolling at your real speaking pace. No foot pedal, remote, or manual paging. |
| **Word-level Highlighting** | The highlight moves word by word, so your eye never scans a full line to find its place. |
| **Continuous Text Following** | Text scrolls continuously between sentences; the reading position stays stable through sentence handoffs. |
| **Sentence Handoff** | When a sentence is finished, the highlight moves forward and the view scrolls to the next line without a visible jump. |
| **Pause and Repeat Tolerance** | Pauses hold the position; repeated lines, re-reads, and quick corrections keep progress anchored to the current sentence. |
| **Fixed-speed Prompting** | With speech following off, the script advances at a set pace. No model and no microphone required. |
| **Floating Teleprompter Window** | A separate always-on-top window that can sit beside your camera or recording app. |
| **Script Management** | Import plain text and Markdown scripts, organize them in folders, and keep the original text untouched. |
| **Reading Preferences** | Adjust font size, line height, paragraph spacing, colors, and following behavior for your screen and viewing distance. |
| **On-device Speech Recognition & Diagnostics** | Speech is recognized locally with no audio upload, and microphone/recognition status is surfaced for troubleshooting. |

Speech following uses the on-device Speech Engine. Fixed-speed mode works without it, so you can rehearse even before the primary model is ready.

---

## How Natural Speech Following Works

1. **Start reading.** Press Start and speak at your normal pace; the current sentence highlights within a moment.
2. **Pause freely.** The reading position holds while you think, sip water, or check a note, then continues from the same line when you speak again.
3. **Repeat or rephrase.** Repeating a sentence, correcting a word, or improvising briefly keeps the progress anchored to the current sentence instead of jumping ahead.
4. **Finish the sentence.** The highlight moves to the next sentence and the view scrolls to it, with the next line prepared before you get there.

QingCue is deliberately biased toward stability: when the evidence from speech is ambiguous, the view stays put rather than guessing. A short lag is less disruptive than a jump to the wrong line.

<p align="center">
  <img src="./assets/screenshots/follow.png" alt="Word-level highlighting during speech following" width="100%">
</p>

Paragraphs and sentences are the anchors; words are the units of progress. Streaming recognition results are revised as you speak, and QingCue keeps the displayed position monotonic: it may hold or advance, but it does not roll back in front of the reader.

<p align="center">
  <img src="./assets/screenshots/follow-scroll.png" alt="Continuous scrolling keeps surrounding lines in view" width="100%">
</p>

Scrolling is viewport-bounded: the page moves only when the highlight approaches the edge of the comfortable reading area, and surrounding lines remain visible. The result is steady motion during fast passages and a stable frame during pauses.

---

## A Closer Look

<p align="center">
  <img src="./assets/screenshots/library-folders.png" alt="Script library organized in folders" width="100%">
</p>

Scripts are organized in folders with an expandable tree. The original text is never rewritten; folders are just a local way to organize your material. Plain text and Markdown are treated as text, so complex formatting is not reproduced faithfully.

<p align="center">
  <img src="./assets/screenshots/preferences.png" alt="Reading preferences and on-device settings" width="100%">
</p>

Settings separate what affects *following* from what affects *reading*: input device, following mode, and local model management on one side; font size, line height, paragraph spacing, colors, and highlight style on the other.

<p align="center">
  <img src="./assets/screenshots/floating-bar.png" alt="Floating teleprompter window" width="100%">
</p>

The floating window stays on top with an adjustable size and position, which keeps it beside your camera or on a second display without covering the main view.

---

## Use Cases

- **Short-form video.** One take, one chance. Keep your script in sight and your attention on delivery, expression, and camera.
- **Recording sessions.** Stop to reset a take and resume without losing your place, with both hands free.
- **Presentations and talks.** The next sentence is always visible, so you can speak to the room instead of checking where you are.
- **Script writing and rehearsal.** Draft, revise, and read through in the same app, with folders and a visible reading position for long scripts.

---

## Privacy and Local Processing

- **Audio stays on device.** Microphone input is processed in memory and is not recorded, uploaded, or used to train anything.
- **Recognition runs locally.** There is no cloud speech service in the loop, so no third party holds your recording.
- **Scripts stay local.** Scripts, folders, settings, and diagnostics live in your user data directory. There is no account system and no cloud sync.
- **No telemetry on your content.** QingCue does not archive transcripts or score the quality of your reading.
- **Offline by design.** Once the primary model is available, disconnecting from the network does not affect prompting or speech following.

---

## System Requirements

| Item | Requirement |
| --- | --- |
| Operating system | Windows 10 or Windows 11, 64-bit |
| Architecture | x64 |
| Installer | MSI |
| Runtime | Self-contained; no separate runtime or VC++ redistributable required |
| Display | 1920×1080 or higher recommended; text size and spacing are adjustable |
| Audio | A microphone or other audio input device (required only for speech following) |
| Disk | About 1 GB for the application, plus about 900 MB for the primary speech model |
| Network | Only for the first model download; offline use afterwards |

---

## Download and Installation

Get the installer from the [Release page](https://github.com/ShowKang/QingCue-Teleprompter/releases/tag/v0.1.17-r13.3):

- **QingCue 0.1.17 + r13.3 for Windows x64** — MSI installer, 434,040,993 bytes (about 414 MB)
- `SHA256SUMS.txt` — checksum file for verification
- `LICENSES-v0.1.17-r13.3.md` — third-party license and attribution information

**Install**

1. Download the MSI and `SHA256SUMS.txt` from the Release page.
2. Verify the installer using the [SHA-256 instructions](#verification).
3. Double-click the MSI and follow the setup wizard. Installation from the command line is also supported:

   ```bat
   msiexec /i "<downloaded-installer>.msi"
   ```

4. Launch QingCue from the Start menu or the desktop shortcut.

The installer places the app under your user profile and creates Start menu and desktop entries.

> The installer is not commercially code-signed, so Windows may show a SmartScreen warning. Confirm the file came from this repository and matches the SHA-256 value before choosing **More info → Run anyway**. Do not disable system security checks to install it.

**Upgrade** — Run the newer MSI over an existing installation. Scripts, settings, and local models are preserved.

**Uninstall** — Open **Settings → Apps → Installed apps**, find QingCue, and choose Uninstall. Your data in `%LOCALAPPDATA%\QingCue` is kept by default; delete that folder manually if you want a clean removal.

**Portable use** — Create a `portable.flag` file next to the executable to store data in a `Data` folder beside the program. Exit the app before moving the folder.

---

## First Run

1. **Choose your microphone** in Settings and confirm the input level responds when you speak.
2. **Download the primary speech model** when prompted (about 900 MB). The installer already includes two compact starter models (about 101.7 MB combined); the primary model provides full speech-following quality.
3. **Open or import a script**, then press Start and read a short paragraph aloud.
4. **Adjust reading preferences** — font size, line height, spacing, and colors — for your screen and distance.
5. **Try the floating window** if you record or present with another app in the foreground.

Fixed-speed prompting is available immediately and needs no model and no microphone.

---

## FAQ

**Speech following is not responding.**

Allow desktop apps to use the microphone in **Windows Settings → Privacy & security → Microphone**, then select the correct input device in QingCue. Make sure the primary speech model has finished downloading.

**Do I need to download the model?**

For speech following, yes. The installer includes two compact starter models, but the primary model (about 900 MB) is downloaded in-app on first use for full quality. Fixed-speed prompting needs neither a model nor a microphone.

**Can I use it offline?**

Yes. After the primary model is ready, prompting, following, and script management work without a network connection. Only the first model download requires internet access.

**I am moving to another computer. Can I avoid downloading the model again?**

Copy the model from your data directory and import it in Settings on the new machine.

**What happens if my reading differs from the script?**

QingCue anchors progress to the script and advances when it hears matching speech. Repeats, re-reads, and quick corrections keep the position on the current sentence; skipping ahead catches up when you reach later text. Long improvised passages that leave the script may hold the view in place until you return to the text.

**Does uninstalling remove my scripts?**

No. Uninstall keeps `%LOCALAPPDATA%\QingCue` (scripts, settings, and models). Delete that folder manually for a full cleanup.

**Where do I report a problem?**

Open an issue on [GitHub Issues](https://github.com/ShowKang/QingCue-Teleprompter/issues) using the bug report or installation help template. Include your QingCue version, Windows version, and steps to reproduce. Do not attach scripts or recordings that contain personal or confidential information.

---

## Verification

SHA-256 for the 0.1.17 + r13.3 Windows x64 installer:

```
9305BBFC7D29B4460F0C71048B7718D9EC44D02F9CB1C39230716850741014EC
```

In the download folder, run:

```powershell
$msi = Get-ChildItem .\QingCue-0.1.17-r13.3-*.msi | Select-Object -First 1
Get-FileHash $msi.FullName -Algorithm SHA256
```

In Command Prompt, run `certutil -hashfile <downloaded-installer>.msi SHA256`.

Compare the output with the value above. A mismatch means the file is incomplete or was altered; download it again instead of installing. `SHA256SUMS.txt` is published with every release for the same purpose.

---

## Changelog

**0.1.17 + r13.3** — Installation and distribution revision; prompting and speech following are unchanged. Adds complete third-party license files, SHA-256 verification, and provenance details to the package, and preserves scripts, settings, and models across an in-place upgrade.

See [CHANGELOG.md](./CHANGELOG.md) for the full release history.

---

## Support and Feedback

- **Bug reports and installation help:** [GitHub Issues](https://github.com/ShowKang/QingCue-Teleprompter/issues)
- **Installation details:** [docs/INSTALL.md](./docs/INSTALL.md)
- **Capabilities and boundaries:** [docs/CAPABILITIES.md](./docs/CAPABILITIES.md)

Support happens in public on GitHub. When reporting an issue, include your QingCue version, Windows build, and the steps that led to the problem.

---

<p align="center"><sub>QingCue · Windows 10 / 11 · x64 · 2026</sub></p>
