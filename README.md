# CityKids Plex Automation

Windows preview downloads for Metro City Church's CityKids Plex automation app.

## Download

Download the latest packaged Windows preview from the [Preview 3 release](https://github.com/pfteamboy24-source/citykids-plex-downloads/releases/tag/v0.1.0-preview.3).

Use **CityKids-Plex-Automation-v0.1.0-preview.3-Windows-x64.zip** under the release's **Assets** section.

Preview 3 fixes the Preview 2 regressions and adds safe in-app updates:

- The permanent local address is **http://127.0.0.1:8765/**. It remains valid after the app or computer restarts.
- **Start automatically with Windows** now uses the current user's normal Windows startup entry. It does not require administrator access or Task Scheduler.
- Automatic startup runs silently without leaving a CMD or PowerShell window open.
- Opening the desktop shortcut while the automation is already running reuses the existing control panel instead of starting a second copy.
- Saved Plex library section IDs and names survive app and PC restarts, including when Plex is temporarily unavailable during startup.
- The control panel includes **Stop CityKids**, **Restart CityKids**, **Check for Updates**, and **Install Update** controls.
- Errors shown in the browser are short; detailed diagnostics are written to the ProgramData log.

Do not use GitHub's automatically generated **Source code** downloads. They are not the ready-to-run Windows app.

## Install and start

1. Download the ZIP from the release.
2. Right-click the ZIP and select **Extract All**.
3. Move the extracted folder to a permanent location on the Plex computer.
4. Open the folder and double-click **Start CityKids Control Panel.cmd**.
5. The app opens its setup page and creates a **CityKids Plex Control** shortcut on the desktop.

After the first launch, use the desktop shortcut or bookmark **http://127.0.0.1:8765/**. The local app supplies the current browser credential automatically.

## Update from Preview 1 or Preview 2

1. Stop the existing CityKids automation. Keep the Preview 1 folder as a fallback until Preview 3 has been verified.
2. If an old Task Scheduler task named **CityKids Plex Automation** exists, disable or delete that exact task. Preview 3 does not use it.
3. Download and extract the Preview 3 ZIP to a new permanent folder. Do not extract it over Preview 1.
4. Run **Start CityKids Control Panel.cmd** from the new folder once.
5. Confirm the saved folders and Plex library selections, enable **Start automatically with Windows**, then save the settings.
6. Continue using the bookmark **http://127.0.0.1:8765/**.

Your folder settings, Plex library selections, and encrypted Plex token are stored separately under ProgramData, so installing Preview 3 in a new folder does not erase them.

## Future updates

After Preview 3 is installed, use **Check for Updates** and **Install Update** in the control panel. CityKids downloads the newer public GitHub release, verifies its SHA-256 checksum and internal file manifest, safely stops the old backend, backs up replaced application files, installs the update, and restarts CityKids.

The updater does not require Git and does not overwrite the ProgramData configuration or encrypted Plex token. If installation fails after replacing files, it restores the previous application files where practical.

No Python, Node.js, npm, administrator account, or separate FFmpeg installation is required.

Windows may show an **Unknown publisher** warning because this preview is not code-signed. Confirm that the download came from this repository before choosing to run it.

## Previous Preview 1 instructions

Preview 1 remains available from its historical release as a fallback. Do not delete its release or overwrite its package.

## What it does

- Watches the configured Kids, Preschool, and Music Videos folders.
- Converts JPG, JPEG, and PNG images into 30-second Plex-ready MP4 clips.
- Preserves and stages normal video files.
- Keeps lesson media and music-video media in separate Plex destinations.
- Moves successfully handled source media to the configured Processed Videos archive.
- Refreshes the selected Plex libraries.
- Builds an ordered Plex collection for each lesson week and uses the Theme image as its poster when available.

## Preview safety

Test the preview with copied media before using the live OneDrive folders. The app's settings and encrypted Plex token are stored locally on the Windows computer and are not included in this download repository.

The SHA-256 checksum published beside each release ZIP and in `SHA256SUMS.txt` can be used to verify the download.

## Source code

The application source is maintained in a separate private repository. This public repository contains only downloads and installation information.
