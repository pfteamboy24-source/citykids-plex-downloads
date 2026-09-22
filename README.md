# CityKids Plex Automation

Windows preview downloads for Metro City Church's CityKids Plex automation app.

## Download

Download the latest packaged Windows preview from the [Releases page](https://github.com/pfteamboy24-source/citykids-plex-downloads/releases/latest).

For Preview 1, use **CityKids-Plex-Automation-v0.1.0-preview.1-Windows-x64.zip** from the [Preview 1 release](https://github.com/pfteamboy24-source/citykids-plex-downloads/releases/tag/v0.1.0-preview.1).

Do not use GitHub's automatically generated **Source code** downloads. They are not the ready-to-run Windows app.

## Install and start

1. Download the ZIP from the release.
2. Right-click the ZIP and select **Extract All**.
3. Move the extracted folder to a permanent location on the Plex computer.
4. Open the folder and double-click **Start CityKids Control Panel.cmd**.
5. The app opens its setup page and creates a **CityKids Plex Control** shortcut on the desktop.
6. Keep the black app window open while the automation is running.

After the first launch, use the desktop shortcut. It starts the app and opens a fresh secure local control-panel address each time.

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
