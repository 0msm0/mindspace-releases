# MindSpace releases

Installers and the auto-update feed for MindSpace. The source code is kept elsewhere; this repo holds only release files.

MindSpace is in **private beta**. The builds are not code-signed yet, so Windows SmartScreen will warn when you run the installer.

Each platform has its own update feed, so one platform can ship a fix without the other. The app reads `feeds/<channel>/<os>-<arch>.json` from this repo's `main` branch:

| Platform | Beta feed | Stable feed |
|---|---|---|
| Windows x64 | `feeds/beta/windows-x86_64.json` | `feeds/stable/windows-x86_64.json` |
| macOS Apple Silicon | `feeds/beta/darwin-aarch64.json` | `feeds/stable/darwin-aarch64.json` |
| macOS Intel | `feeds/beta/darwin-x86_64.json` | `feeds/stable/darwin-x86_64.json` |

A feed file appears once that platform has its first release. Each release's notes list the platforms it includes and the source commit it was built from. A version number always means the same source code on every platform.

Don't edit these files by hand: `scripts/publish-release.ps1` in the source repo writes them.
