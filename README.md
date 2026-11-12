# 📦 Official List of Juka Packages

This repository contains the official list of **Juka Packages** that appear inside the Juka application.  
All packages are defined in **`packages.json`**, which the Juka runtime reads to display and manage available packages.

---

## 🗂 Editing `packages.json`

To add your own package, simply edit **`packages.json`** and append a new entry following the structure below.

Each package entry must include:

- **name** – Display name of the package  
- **author** – Creator or maintainer  
- **description** – Short explanation of what the package does  
- **date** – Release date (`YYYY-MM-DD`)  
- **version** – Package version  
- **dependencies** – Array of required packages (or empty array)  
- **mainfilename** – The `.sh` file that serves as the entry point  
- **download** – URL to the package repository or download location  
- **device** – Supported devices (`"all"` or list of specific devices, e.g. `trimui_smart_pro`, `trimui_smart_pro_s`, `trimui_brick`, `trimui_brick_pro`)

Optional fields:

- **icon** – HTTPS link to a picture shown on the package's card in the Juka store (PNG, JPG, WebP or BMP, **1 MB at most**). Packages without one show a letter tile. Link to the app's own icon in its GitHub repository, pinned to a commit so the link keeps working if files move:
  `https://raw.githubusercontent.com/<owner>/<repo>/<commit-sha>/<path>/icon.png`

  Icons for the games below are copied from each game's own zip and hosted in this repository's [`icons/`](icons) folder, because those games' upstream repos don't ship a matching icon file.

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
    "device": ["all"],
    "icon": "https://raw.githubusercontent.com/jukaLang/Example/<commit-sha>/icon.png"
  }
]
```

---

## ❌ Requesting Package Removal

If you would like a package removed from the official list, please **[submit a Pull Request](../../pulls)** that removes the relevant entry from `packages.json`.  
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

### hugorosario — [BrickTools](https://github.com/hugorosario/BrickTools)

| Name | Description |
|------|-------------|
| **BrickTools** | Tools and system apps for the TrimUI Brick that match the stock theme: utilities, network, user interface, LED control and system menus, customizable through `menu.json`. Works on stock firmware and StockMix/CrossMix. |

---

### rommapp — [Grout](https://github.com/rommapp/grout)

| Name | Description |
|------|-------------|
| **Grout** | RomM client for retro handhelds. Browse your RomM library and download games to the device over Wi-Fi. Install the TrimUI stock OS build on the TrimUI Brick or Smart Pro. |

---

### nlkcodenew

| Name | Source | Description |
|------|--------|-------------|
| **Trimui-XiaoZhi** | [trimui-xiaozhi](https://github.com/nlkcodenew/trimui-xiaozhi) | Unofficial Xiaozhi voice assistant for the TrimUI Smart Pro S on stock OS, with chat history, settings and an optional web chat. |
| **Trimui Terminal** | [trimui-terminal](https://github.com/nlkcodenew/trimui-terminal) | SDL2 terminal with a built-in Bluetooth gamepad survey tool. Brick Pro on stock OS is the primary target; Smart Pro S is not fully tested. |
| **Music Player** | [Music-Player](https://github.com/nlkcodenew/Music-Player) | Self-contained music player for the TrimUI Brick Pro on stock OS, with Google Drive folders, playlists, synced lyrics and an equalizer. |

---

### ro8inmorgan — [LedControl](https://github.com/ro8inmorgan/LedControl)

| Name | Description |
|------|-------------|
| **LED Control** | Controls the TrimUI Brick's LEDs from the device. Works on stock OS, StockMix/CrossMix and MinUI; includes an uninstaller. |

---

### pierceTee — [TrimuiLEDController](https://github.com/pierceTee/TrimuiLEDController)

| Name | Description |
|------|-------------|
| **Brick LED Controller** | Configures TrimUI Brick LED brightness, color and effects, plus the low-battery warning. Works on stock OS and MinUI. |

### nlkcodenew — more

| Name | Source | Description |
|------|--------|-------------|
| **Trimui Remote** | [trimui-remote](https://github.com/nlkcodenew/trimui-remote) | SSH (dropbear) access for the TrimUI Brick Pro and Smart Pro S on stock OS. |

---

### joyrider3774 — [trimui_smart_pro_games](https://github.com/joyrider3774/trimui_smart_pro_games)

> ℹ️ Stock OS games for the TrimUI Smart Pro. Each zip is extracted into `Apps`.

| Name | Description |
|------|-------------|
| **Blips** | Blips Playdate. |
| **Blockdude** | Blockdude Playdate. |
| **cglpSDL2** | Crisp Games Library Portable. |
| **Checkers** | Checkers Playdate. |
| **Dynamate** | Dynamate Playdate. |
| **Formula 1 G&W** | Formula 1 Game & Watch Playdate. |
| **MazeThingie** | Maze generator and player. |
| **Playdoban** | Playdoban Playdate. |
| **Puztrix** | Puztrix Playdate. |
| **Puzzle Land** | Puzzle Land Playdate. |
| **Retrotime** | Retrotime. |
| **Rubido** | Rubido Playdate. |
| **Waternet** | Waternet Playdate. |
| **Worm** | Worm Playdate. |
| **Znax** | Znax. |

---

### 32Blit games — [32blit_trimui](https://github.com/joyrider3774/32blit_trimui)

> ℹ️ [32Blit SDK](https://github.com/32blit) games ported to the TrimUI by joyrider3774 (Smart Pro and Brick, stock OS). The original authors and repositories are listed below.

| Name | Original author |
|------|-----------------|
| **2048 (32Blit)** | ArtemHarkusha |
| **32Blox (32Blit)** | ahnlak-blit32 |
| **4 in a Row (32Blit)** | lummi01 |
| **Jumpy Squirrel (32Blit)** | ThePythonator |
| **Ping (32Blit)** | ThePythonator |
| **Snake (32Blit)** | lummi01 |
| **Solitaire (32Blit)** | ThatOtherOtherBob |
| **Super Square Bros (32Blit)** | ThePythonator |
| **Tower Defense (32Blit)** | Blackhawk-TA |
| **Alien Attack (32Blit)** | lummi01 |
| **A-Maze (32Blit)** | andreban |
| **Asteroids (32Blit)** | lummi01 |
| **Super Blit Kart (32Blit)** | Daft-Freak |
| **Blit Racers (32Blit)** | shane-powell |
| **Bounce (32Blit)** | lummi01 |
| **Cannonhead (32Blit)** | lummi01 |
| **Car Sprint (32Blit)** | mikerr |
| **Save the Castle (32Blit)** | lummi01 |
| **Dino (32Blit)** | lummi01 |
| **Dodgeem (32Blit)** | lummi01 |
| **Dots (32Blit)** | Gadgetoid |
| **Dune II (32Blit)** | mikerr |
| **Fourblock Descent (32Blit)** | Daft-Freak |
| **Geometry (32Blit)** | 32blit |
| **Game of Life (32Blit)** | lummi01 |
| **Pitfall Harry (32Blit)** | lummi01 |
| **Indy 500 (32Blit)** | lummi01 |
| **Invader (32Blit)** | lummi01 |
| **Jetpac (32Blit)** | mikerr |
| **Knight Lore (32Blit)** | mikerr |
| **Match 3 (32Blit)** | deckerego |
| **Minesweeper (32Blit)** | ArtemHarkusha |
| **Missile Command (32Blit)** | lummi01 |
| **Raycaster (32Blit)** | 32blit |
| **Rocks and Diamonds (32Blit)** | 32blit |
| **Scrolly Tile (32Blit)** | 32blit |
| **Simon Says (32Blit)** | lummi01 |
| **Snake Race (32Blit)** | lummi01 |
| **Sokoblit (32Blit)** | ahnlak-blit32 |
| **Tower (32Blit)** | lummi01 |
| **Wakka Wakka (32Blit)** | mikerr |
| **Willy (32Blit)** | mikerr |

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
- **hugorosario** — BrickTools
- **rommapp** — Grout
- **nlkcodenew** — Trimui-XiaoZhi, Trimui Terminal and Music Player
- **ro8inmorgan** — LED Control
- **pierceTee** — Brick LED Controller
- **joyrider3774** — TrimUI Smart Pro games and the 32Blit TrimUI ports
- **The 32Blit game authors** — ArtemHarkusha, ThePythonator, ahnlak-blit32, lummi01, Daft-Freak, mikerr, Gadgetoid, andreban, Blackhawk-TA, ThatOtherOtherBob, deckerego, shane-powell and the 32blit team
