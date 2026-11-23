# Changelog

All notable changes to **Vivimagic GC Suite** (`Vivimagic/GameCube-Bridge-Studio`) are documented in this file.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and [Semantic Versioning](https://semver.org/).

---

## [v2.0.0] — 2026-11-23

### Added
- **Vivimagic GC Suite v2.0 Desktop Experience**: Unified installer and desktop suite naming (`Vivimagic GC Suite.exe` on Windows, `Vivimagic GC Suite.app` on macOS, and native Linux GUI).
- **Pop-Up Settings Dialog & Animated Icon Controls**: Single-icon Settings button with a smooth 360° hover rotation animation opening a dedicated Settings modal.
- **Separate Light & Dark Mode Buttons**: Dedicated Light Mode and Dark Mode toggle controls with animated SVG sun/moon icons and Windows 10/11 dark title bar styling.
- **Live System Tray Toggle**: Added a persistent **Enable Live System Tray icon & hot-reload menu** checkbox in Settings that immediately shows or hides the tray icon while keeping the 4-port bridge running.
- **1000 Hz MMCSS Low-Jitter Polling**: Hardware timer precision (`timeBeginPeriod(1)` + Windows `Games` MMCSS thread priority).
- **Dual Virtual Controller Backend**: Hot-switch between **Xbox 360 (XInput)** and **Sony DualShock 4 (`054C:05C4`)** via ViGEmBus.
- **Per-Port P1–P4 Calibration & Anti-Snapback Filter**: Individual deadzone/gate calibration and configurable velocity snapback suppression.
- **Sigma-Delta PWM Rumble Sculpting**: Fine-grained dual-motor force feedback translation for GameCube controllers.
- **Window-Focus Dolphin Auto-Handover**: Automatically releases WinUSB when Dolphin/Slippi is focused and reclaims XInput/DS4 on alt-tab.
- **Built-In GitHub Auto-Update Checker**: Queries `Vivimagic/GameCube-Bridge-Studio` releases from Settings with one-click download and launch.
- **Native Linux `/dev/uinput` + `libusb-1.0` Daemon**: Full 4-port GameCube bridge on Ubuntu, Fedora, Arch, and Steam Deck / SteamOS.
- **Safety-Gated RP2040 Firmware & SDK Workbench**: Preset builder, live C/header SDK export, and offline firmware binary inspector.

### Changed
- **True Smooth 0–100% Analog Triggers**: Restored v1-faithful progressive L/R analog trigger ramp without digital click snapping across the WinUSB WUP-028 `0x13` path, PC-mode HID/WinMM fallback, and web calibration tools.
- **GameCube-Authentic Live Controller Tester**: Removed non-GameCube `L-CLK`, `R-CLK`, and `BACK` tiles across Windows, macOS, and Linux testers, organizing the 10 physical GameCube buttons (`A, B, X, Y, Z`, `START`, `UP, DOWN, LEFT, RIGHT`) into a clean 5×2 grid.
- **Automated Cross-Platform Cloud Release Pipeline**: GitHub Actions workflow builds Windows (`.exe`), macOS (`.dmg` + `.app.zip`), Linux (`.deb` + `.tar.gz` + `.sh`), and `SHA256SUMS.txt` in parallel on Node 24 runners.

### Fixed
- **Dark Mode Disabled Button Contrast**: Replaced standard WinForms button painting with `ThemedFlatButton` so disabled buttons retain crisp white/light text while install, reinstall, uninstall, or update tasks are running.
- **Missing `&` Symbols in WinForms UI**: Disabled WinForms mnemonic parsing on buttons and labels so labels like `Firmware & SDK`, `Download & Update`, `Config & Presets`, and `SDK Code & Export` render their `&` symbol properly.
- **Live Adapter Status Synchronization**: Main window status banner now updates live as soon as the adapter connects in Wii U / NS mode and controllers are active.
- **PowerShell Ampersand Parsing**: Properly quoted status strings inside `setup.ps1` to prevent parser errors during installation.
- **Live System Tray Persistence**: Unticking the System Tray option now saves reliably and hides the running tray icon immediately.
- **EXE Builder Diagnostics**: `Vivimagic-Build-Setup-EXE.cmd` keeps errors visible and writes full build logs to `Vivimagic-Build-Setup-EXE.log`.

---

## [v1.0.0] — Initial Release
- 4-port GameCube Controller Adapter (`057E:0337`) silent WinUSB installer and ViGEmBus XInput bridge for Windows, macOS, and Linux.
- Smooth 0–100% analog shoulder trigger support and basic Dolphin USB handover.
- Built-in Live Controller Tester with stick, button, trigger, and rumble verification.

---
Copyright (c) 2026 Ashley Glover. All Rights Reserved.
