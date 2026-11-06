# Installation Guide

## System Requirements

- Windows 10 or Windows 11, 64-bit
- x64 architecture
- MSI installer

The installer is self-contained. No separate runtime, VC++ redistributable, or developer tooling is required.

Speech following uses the on-device Speech Engine. The installer includes two compact starter models (about 101.7 MB combined); the primary speech model (about 900 MB) is downloaded in-app on first use. Once it is available, speech following works offline.

## Installation

1. Download the MSI and `SHA256SUMS.txt` from the [Release page](https://github.com/ShowKang/QingCue-Downloads/releases/tag/v0.1.17-r13.3).
2. Verify the installer against `SHA256SUMS.txt`, or follow the [verification steps](../README.md#verification) in the README.
3. Double-click the MSI and follow the setup wizard, or install from the command line:

   ```bat
   msiexec /i "<downloaded-installer>.msi"
   ```

4. The app installs per user under `%LOCALAPPDATA%\Programs\QingCue` and creates Start menu and desktop entries.

## Upgrading

Keep the upgrade identity unchanged and increment the install revision. The new MSI installs over an existing version and keeps the existing user data directory.

## Uninstalling

Open **Settings → Apps → Installed apps**, find QingCue, and choose Uninstall.

Uninstall keeps `%LOCALAPPDATA%\QingCue` by default (scripts, settings, and local models). Delete that folder manually if you want a complete removal.

## Data Locations

- **Installed app:** `%LOCALAPPDATA%\QingCue` holds scripts, settings, diagnostics, and local models.
- **Portable mode:** a `portable.flag` file next to the executable redirects data to a `Data` folder in the same directory. Exit the app before moving it and copy `Data` along with the program.
- **Speech models:** downloaded on demand in the app and stored in the data directory. Fixed-speed prompting does not need a model.

## Third-Party Licenses

License texts and attributions for bundled components are available in the installation directory:

- `ThirdParty\` — license texts, sources, and verification details for bundled components (see `ThirdParty\SOURCES.md` for the itemized list).
- `wwwroot\licenses\` — license notices for interface components.

The notices cover the components actually packaged and ship with the installer.

## Notes

- The installer is not commercially code-signed. Windows may show a SmartScreen warning on first run. Verify the source and SHA-256 value before continuing, and do not disable system security checks.
- Installation and uninstallation have been verified through automated checks. Live human-read following, visual regression, multi-DPI, external devices, and offline scenarios remain out of the verified scope; see [TESTING.md](TESTING.md).
- The first model download requires a network connection. Speech following works offline afterwards.
