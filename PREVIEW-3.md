# CityKids Plex Automation Preview 3

Preview 3 is the fixed Windows x64 preview for the campus Plex computer. It replaces Preview 2 as the recommended download while keeping Preview 1 available as a fallback.

## Download

Choose `CityKids-Plex-Automation-v0.1.0-preview.3-Windows-x64.zip` under **Assets**. Do not use GitHub's automatically generated source-code archives.

SHA-256:

`729d681d4f449d9a7ccf1cae7a76ced8538f8ec293053ecf94b799de2c988f84`

## What changed

- Keeps the control panel permanently available at `http://127.0.0.1:8765/`.
- Replaces the failing administrator-dependent Scheduled Task workflow with normal-user Windows startup after sign-in.
- Runs automatic startup in the background without a CMD or PowerShell window.
- Prevents duplicate backends and opens the existing control panel when CityKids is already running.
- Persists Plex section IDs and display names across app/PC restarts.
- Preserves saved Plex libraries while Plex is temporarily unavailable during Windows startup.
- Shows short browser errors and writes detailed rotating logs under ProgramData.
- Adds backend PID visibility and full Stop/Restart controls.
- Adds verified GitHub update checking and automatic installation with application-file backup and rollback protection.
- Keeps machine configuration, folder paths, Plex libraries, and the encrypted token outside the versioned application folder.
- Includes FFmpeg and requires no Python, Git, Node.js, or separate runtime installation on the campus PC.

## Install from Preview 1 or Preview 2

1. Keep Preview 1 as a fallback until Preview 3 has been tested.
2. Stop the currently running CityKids backend.
3. Disable or delete the old Task Scheduler task named `CityKids Plex Automation` if it exists.
4. Extract the Preview 3 ZIP into a new permanent folder.
5. Run `Start CityKids Control Panel.cmd` once.
6. Open `http://127.0.0.1:8765/`, confirm the saved folders and Plex libraries, and save with **Start automatically with Windows** enabled.

Later releases can be installed through **Check for Updates** and **Install Update** in the control panel. The updater verifies the public release checksums, stops and restarts CityKids, and leaves ProgramData configuration untouched.

## Validation

- 51 automated tests passed.
- Windows x64 PyInstaller build passed.
- FFmpeg, package checksums, internal file manifest, and config exclusion were verified.
- Packaged stable-URL, duplicate-instance, stop, restart, PID, and diagnostics-log smoke tests passed.

This remains preview software. Test with copied media before using live OneDrive folders.
