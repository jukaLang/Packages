# 📦 Official List of Juka Packages

This repository contains the official list of **Juka Packages** that appear inside the Juka application.  
All packages are defined in **`Packages.json`**, which the Juka runtime reads to display and manage available packages.

---

## 🗂 Editing `Packages.json`

To add your own package, simply edit **`Packages.json`** and append a new entry following the structure below.

Each package entry must include:

- **name** – Display name of the package  
- **author** – Creator or maintainer  
- **description** – Short explanation of what the package does  
- **date** – Release date (`YYYY-MM-DD`)  
- **version** – Package version  
- **dependencies** – Array of required packages (or empty array)  
- **mainfilename** – The `.sh` file that serves as the entry point  
- **download** – URL to the package repository or download location  
- **device** – Supported devices (`"all"` or list of specific devices)

### ✅ Example Entry

```json
[
  {
    "name": "Example",
    "author": "Juka",
    "description": "An example of a Juka package",
    "date": "2024-07-22",
    "version": "1.0",
    "dependencies": [],
    "mainfilename": "launch.sh",
    "download": "https://github.com/jukaLang/Example",
    "device": ["all"]
  }
]
```

---

## ❌ Requesting Package Removal

If you would like a package removed from the official list, please **[submit a Pull Request](../../pulls)** that removes the relevant entry from `Packages.json`.  
Include a brief reason for the removal in your PR description (e.g. deprecated, broken download link, author request).  
All removal requests will be reviewed by the maintainers before merging.

---

## 📋 Current Packages

### djware — [TrimUITools](https://github.com/djware/TrimUITools)

| Name | Description |
|------|-------------|
| **FTP** | Starts an on-demand FTP server; auto-times out after 5 min of inactivity. |
| **FTP Enable** | Enables persistent FTP access at every boot (user: root / pass: root). Run again to disable. |
| **Telnetd** | Installs a static telnetd binary and enables Telnet access on port 23 at every boot. |
| **Random Game** | Picks a random emulator and matching ROM and launches it. |
| **Max CPU** | Forces Performance CPU governor and keeps it active across resets and FN presses. |
| **Reboot** | Quickly restarts the TrimUI Smart Pro from within the menu. |
| **Mac Update** | Fixes Wi-Fi MAC address persistence across reboots (not needed on firmware ≥ 1.0.4 hotfix 20240414). |
| **RainbowLEDs** | Cycles joystick and middle LEDs through a continuous rainbow effect. |
| **LED Temp** | Colors LEDs to show CPU temperature in real time (green → red). |
| **LED Batt** | Colors LEDs to show battery percentage in real time (green → red). |
| **UDISK** | Formats the internal UDISK partition as FAT32 (~6 GB). **USE AT YOUR OWN RISK.** |
| **Bootlogo Updater** | Replaces the startup boot image with a custom BMP file (max 1280×720, under 6 MB). |

---

### schmurtzm — [TrimUI-Smart-Pro](https://github.com/schmurtzm/TrimUI-Smart-Pro)

| Name | Description |
|------|-------------|
| **EmuCleaner** | Hides emulators with no ROMs and shows those that do; keeps your console list tidy. Compatible with stock MainUI manual overrides. |
| **BootLogo** | User-friendly app for flashing a custom boot logo at startup. |
| **System Tools** | Hub app centralizing multiple utility scripts, including a PSX Analog Detector for auto-configuring analog-compatible games. |
| **Resume at Boot** | Adds a resume-last-game feature so the device automatically relaunches your last played game on startup. |
| **Scraper** | Command-line ScreenScraper client that downloads box art and media for your ROM library directly on the device. |

---

### SneakyTwitch — [TrimUI-Apps](https://github.com/SneakyTwitch/TrimUI-Apps)

> ℹ️ All four apps are included in the same release download.

| Name | Description |
|------|-------------|
| **Backup Config Files** | Creates a timestamped backup of PPSSPP, DraStic (NDS), and RetroArch configs — including button mappings, core settings, and shaders. |
| **Restore Config Files** | Restores a previously backed-up config set. Edit `ForRestoring.txt` to target a specific backup version. |
| **BGM Start/Stop** | Toggles background music on/off for the currently active theme. Per-theme state is remembered. |
| **BGM Swap** | Replaces the active theme's BGM with a custom `bgm.mp3` from the root of your SDCARD. Original is backed up as `bgm-bak.mp3`. |

---

### rkr87 — [CollaGen](https://github.com/rkr87/CollaGen)

| Name | Description |
|------|-------------|
| **CollaGen** | CLI-based game collection generator. Dynamically builds named ROM collections using keyword include/exclude filters. Works on CrossMix-OS and Stock OS (with minor edits). |

---

### Primitheus — [OctoLair](https://github.com/Primitheus/OctoLair)

| Name | Description |
|------|-------------|
| **OctoLair** | Downloads ROMs directly onto the device via a controller-friendly SDL2 UI. Browse systems, select games, and download without touching a PC. |

---

### ahmadteeb

| Name | Source | Description |
|------|--------|-------------|
| **EmuDrop** | [EmuDrop](https://github.com/ahmadteeb/EmuDrop) | Full-featured ROM downloader with a built-in screen scraper. Supports Stock OS, CrossMix-OS, and Knulli. Compatible with TrimUI Smart Pro and TrimUI Brick. |
| **DNS Changer** | [TSP_DNSChanger](https://github.com/ahmadteeb/TSP_DNSChanger) | Changes DNS server settings on-device via a controller-friendly UI. Useful for improving connectivity or bypassing regional restrictions. |

---

### veckia9x — [Trimui-X](https://github.com/veckia9x/Trimui-X)

> ⚠️ These apps require **TRIMUI_EX** or **TomatoOS** to function.

| Name | Description |
|------|-------------|
| **ThemixPro** | Automatically updates system icons, selection-state icons, and backgrounds whenever the active theme changes. Ships with the GREYS-DARK theme. |
| **Syncthing** | Runs Syncthing on the device for wireless file sync with a PC or phone. Supports optional boot startup. Default credentials: `trimui` / `trimuisync`. |

---

## 🙏 Credits

Thanks to all the community contributors who build and maintain these tools:

- **djware** — foundational tools and LED utilities
- **schmurtzm** — EmuCleaner, BootLogo, System Tools, Resume at Boot, Scraper
- **SneakyTwitch** — config backup/restore and BGM tools
- **rkr87** — CollaGen collection manager
- **Primitheus** — OctoLair ROM downloader
- **ahmadteeb** — EmuDrop and DNS Changer
- **veckia9x** — ThemixPro and Syncthing
