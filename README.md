# CityKids Plex Automation

Windows preview downloads for Metro City Church's CityKids Plex automation app.

## Download

Download the latest packaged Windows preview from the [Preview 2 release](https://github.com/pfteamboy24-source/citykids-plex-downloads/releases/tag/v0.1.0-preview.2).

Use **CityKids-Plex-Automation-v0.1.0-preview.2-Windows-x64.zip** under the release's **Assets** section.

Preview 2 fixes the control panel bookmark and Windows startup behavior:

- The permanent local address is **http://127.0.0.1:8765/**. It remains valid after the app or computer restarts.
- **Start automatically with Windows** creates and maintains a hidden current-user startup task.
- Opening the desktop shortcut while the automation is already running reuses the existing control panel instead of starting a second copy.

Do not use GitHub's automatically generated **Source code** downloads. They are not the ready-to-run Windows app.

## Install and start

1. Download the ZIP from the release.
2. Right-click the ZIP and select **Extract All**.
3. Move the extracted folder to a permanent location on the Plex computer.
4. Open the folder and double-click **Start CityKids Control Panel.cmd**.
5. The app opens its setup page and creates a **CityKids Plex Control** shortcut on the desktop.
6. Keep the black app window open while the automation is running.

After the first launch, use the desktop shortcut or bookmark **http://127.0.0.1:8765/**. The local app supplies the current browser credential automatically.

## Update from Preview 1

1. Stop the existing CityKids automation or close its black app window.
2. Download and extract the Preview 2 ZIP to a permanent folder.
3. Run **Start CityKids Control Panel.cmd** from the new folder once.
4. Confirm **Start automatically with Windows** is checked, then save the settings.
5. Replace any old bookmark with **http://127.0.0.1:8765/**.

Your folder settings and encrypted Plex token are stored separately under ProgramData, so installing Preview 2 in a new folder does not erase them. After Preview 2 has been verified, the old Preview 1 application folder can be removed.

No Python, Node.js, npm, or separate FFmpeg installation is required.

Windows may show an **Unknown publisher** warning because this preview is not code-signed. Confirm that the download came from this repository before choosing to run it.

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

The SHA-256 checksum published beside each release ZIP can be used to verify the download.

## Source code

The application source is maintained in a separate private repository. This public repository contains only downloads and installation information.
