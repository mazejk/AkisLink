# Release verification — 2026-10-01

AkisLink 2.0.0-preview.2 is a saved local preview, not a claim of completed device/network certification.

Passed:
- Final assembleRelease + lintRelease: build successful; lint 0 errors, 44 warnings (including legacy/platform widget and API compatibility suggestions).
- Release APK cryptographic verification: one RSA 3072 signer, APK v2 signature verified. Package app.akislink.hotspot.release, versionCode 13, versionName 2.0.0-preview.2, label AkisLink, ARM64, minSdk 29 / targetSdk 34; no debuggable flag.
- Android JVM tests: 4 tests, 0 failures/errors. Includes 3 hotspot regression tests for input validation, Default/Bypass/Custom mapping, redaction and bilingual state/recovery messages.
- Windows source GUI and final embedded EXE smoke test: real EN/TR buttons overwrite an existing settings file successfully; drafts survive language changes; invalid IPv4 and port show inline errors; settings lock while connecting; Connect/Cancel/Disconnect match in window and tray. All four pages rendered in EN/TR and light/dark themes and were visually inspected.
- Packaged EXE extraction and embedded SHA-256 verification: UI_PASSED. This test does not require the source checkout to supply the client/engine.
- Conflicting desktop helper: CLIENT_ALREADY_RUNNING is reported without starting routing.
- Generated sing-box configurations validate for IPv4 and the experimental IPv6 option; these checks change no routes or adapter DNS.
- Windows Authenticode status confirmed NotSigned and documented.

Outstanding:
- Phone disconnected from ADB during final packaging: latest release installation and end-to-end forwarding have not been tested on hardware.
- Carrier sharing allowance accounting, sustained/screen-off stability, game/voice performance, GSBWIFI/eduroam compatibility and general IPv6 support remain unverified.
- Earlier development transport passed short HTTPS/UDP probes; those are not evidence of this release's sustained performance or billing behavior.

The original settings-save failure was separately reproduced on Windows PowerShell 5.1 before the fix: File.Replace(source, destination, $null) coerced the backup path to an invalid empty string. The GUI regression now exercises repeated actual language clicks through the corrected C# atomic save operation.
