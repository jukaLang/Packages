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

### djware

| Name | Description |
|------|-------------|
| **FTP** | Starts an FTP server on the device; auto-times out after 5 min of inactivity. |
| **FTP Enable** | Enables persistent FTP access at every boot. Run again to disable. |
| **Telnetd** | Installs a static telnetd binary and enables Telnet access on port 23 at every boot. |
| **Random Game** | Picks a random emulator + ROM and launches it. |
| **Max CPU** | Forces the Performance CPU governor and keeps it active across resets. |
| **Reboot** | Quickly restarts the TrimUI Smart Pro from within the menu. |
| **Mac Update** | Fixes Wi-Fi MAC address across reboots (not needed on firmware ≥ 1.0.4 hotfix 20240414). |
| **RainbowLEDs** | Cycles joystick and middle LEDs through a continuous rainbow effect. |
| **LED Temp** | Colors LEDs to show CPU temperature in real time (green → red). |
| **LED Batt** | Colors LEDs to show battery percentage in real time (green → red). |
| **UDISK** | Formats the internal UDISK partition as FAT32 (~6 GB). **USE AT YOUR OWN RISK.** |
| **Bootlogo Updater** | Replaces the startup boot image with a custom BMP file. |

### schmurtzm

| Name | Description |
|------|-------------|
| **EmuCleaner** | Hides emulators with no ROMs and shows those that do; keeps your console list tidy. |
| **BootLogo** | User-friendly app for flashing a custom boot logo at startup. |
| **System Tools** | Hub app centralizing multiple utility scripts, including a PSX Analog Detector. |
| **Resume at Boot** | Adds a resume-last-game feature so the device relaunches your last game on startup. |
| **Scraper** | Command-line ScreenScraper client that downloads box art for your ROM library. |
