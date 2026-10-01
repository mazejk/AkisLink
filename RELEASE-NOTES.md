# AkisLink 2.0.0-preview.2 release notes

- New AkisLink name and shared A logo for phone, Windows executable, window and tray.
- Windows interface rebuilt with WPF: rounded borderless window, custom window controls, sidebar navigation, light/dark/system themes and matching tray popup.
- One context-aware Connect / Cancel / Disconnect action in both the window and tray.
- Fixed language switching when a settings file already exists. C# performs the atomic replacement with a literal null backup path, avoiding PowerShell 5.1 null-to-empty-string conversion. UI errors appear inline.
- Visible English/Türkçe switching preserves drafts. Added inline port validation and tested settings locking while connecting.
- New installs use Default with DPI bypass off. Default + DPI Bypass explicitly enables OOB. Custom settings remain available.
- Signed non-debuggable Android release, separate application package, self-contained Windows launcher, SHA-256 manifests, public signing certificate and accompanying source archives.
- Release scope and unverified network/hardware behaviors are described in README. No public upload has been made.

The release directory is a frozen snapshot. Continue development in android/ and windows/; create a new version instead of replacing these release files.
