# MindSpace releases

Installers and the auto-update feed for MindSpace. The source code is kept elsewhere; this repo holds only release files.

MindSpace is in **private beta**. The builds are not code-signed yet, so Windows SmartScreen will warn when you run the installer.

Each platform has its own update feed, so one platform can ship a fix without the other:

| Platform | Feed |
|---|---|
| Windows x64 | `latest-windows-x86_64.json` |
| macOS Apple Silicon | `latest-darwin-aarch64.json` (not yet published) |
| macOS Intel | `latest-darwin-x86_64.json` (not yet published) |
