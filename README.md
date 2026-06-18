# FindFast Pluss

**Lightning fast search for apps, files, and folders on Windows.**

Press `Ctrl+Space` from anywhere, type your query, and instantly get ranked results across all your drives, programs, and files. No bloat, no ads, no subscriptions — just fast, local search that works.

---

## Download

- **Microsoft Store:** [Download FindFast Pluss](https://apps.microsoft.com/store/detail/9MZFB26S5PRQ?cid=DevShareMCLPCS)
- **Standalone Installer:** Built from source via `build.bat` → `installer_output\FindFast_Setup.exe`
- **MSIX Package:** Built via `build_msix.bat`

---

## How to Use

1. **Install and launch** FindFast Pluss — it runs in the system tray.
2. Press **`Ctrl+Space`** (or your custom hotkey) from anywhere in Windows.
3. **Start typing** — results appear instantly, ranked by relevance.
4. Press **`Enter`** to launch the selected item.
5. Press **`Esc`** to dismiss the window and return to what you were doing.

On first launch, the Settings window appears for initial setup (theme, shortcuts).

---

## Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl+Space` | Open / hide the search overlay |
| `Enter` | Launch / open the selected result |
| `Escape` | Dismiss / close the search window |
| `Up Arrow` | Navigate selection up |
| `Down Arrow` | Navigate selection down |
| `Ctrl+F` | Show in File Explorer |
| `Ctrl+C` | Open CMD at file location |
| `Tab` | Auto-complete top result |

### Search Filters

| Filter | Description |
|---|---|
| `/f <query>` | Filter to files only |
| `/a <query>` | Filter to apps only |
| `/d <query>` | Filter to directories/folders only |
| `C:\path\...` | Type a path to show only direct children |

### Result Actions

| Action | Description |
|---|---|
| `Enter` | Launch / open the selected result |
| `Ctrl+F` | Show in File Explorer (opens folder + selects file) |
| `Ctrl+C` | Open CMD at the file/folder's directory |
| Right-click | Context menu: Open, Run as Admin, Show in Explorer, Open in CMD |

---

## Changing Shortcuts

### Method 1: Settings Window (Recommended)
1. Open FindFast (`Ctrl+Space`)
2. Type "FindFast Settings" and press Enter, or right-click tray icon → Settings
3. In the SHORTCUTS section, click an edit box and press your desired key combination
4. Click **Save & Launch FindFast** to restart with new shortcuts

### Method 2: Config File (Manual)
Edit `findfast_config.ini` while FindFast is closed:
- **MSIX mode:** `%LOCALAPPDATA%\FindFast\findfast_config.ini`
- **Standalone:** `%APPDATA%\FindFast\findfast_config.ini`

Modifier flags: `1`=Alt, `2`=Ctrl, `4`=Shift, `8`=Win

---

## Features

- **Global Hotkey** — show/hide from anywhere with `Ctrl+Space` (customizable)
- **Instant Type-to-Search** — results appear as you type
- **Smart Ranking** — scored 0–7 by relevance (exact matches first)
- **Full File System Indexing** — all drives, all file types (documents, images, video, audio, archives, code, etc.)
- **Application Detection** — indexes `.exe`, `.lnk`, `.url` from Registry, PATH, and common locations
- **Real-Time File Watching** — index updates automatically as files change
- **50+ Windows Settings Shortcuts** — Display, Sound, Bluetooth, Network, Personalization, and more
- **40+ System Commands** — Task Manager, Registry Editor, CMD, PowerShell, Control Panel, etc.
- **Dark & Light Themes** — auto-detects system preference, adapts to Windows accent color
- **System Tray Integration** — with left-click show / right-click context menu
- **Auto-Start** — via Windows StartupTask (MSIX) or Registry (standalone)
- **100% Offline & Private** — zero telemetry, no internet access, all local processing
- **Tiny & Portable** — single ~1.7 MB executable, no runtime dependencies

---


## Tech Stack

- **Language:** C++17
- **Compiler:** MSVC (Visual Studio 2022)
- **Size:** ~1.7 MB static executable
- **Core Libraries:** Win32 API, SQLite (bundled), GDI, Shell API
- **Threading:** Parallel drive scanning via `std::async`, dedicated file watcher thread, per-query search threads

---

## System Requirements

- Windows 10 version 1809 or later (x64)
- 100 MB disk space for index
- 50 MB RAM

---

## License

Copyright © 2026 mueezejaz (Mueez Ejaz). All rights reserved.

FindFast Pluss is a trademark of mueezejaz.
Windows is a registered trademark of Microsoft Corporation.
