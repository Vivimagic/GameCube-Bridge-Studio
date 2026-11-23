# Vivimagic GC Suite — v2.0.0

**Next-Gen 4-Port GameCube Controller Adapter Driver, Live System Tray, Dual XInput/DS4 Emulation & Firmware SDK**

Supports **Official Nintendo WUP-028**, **Mayflash W012**, **MEIRIYFA**, **Nyko**, **Kelux / Piranha / Intec / Hitbox**, **Input Integrity Lossless / GC Pocket+**, plus **Universal Legacy PC-Mode / 2-Port / Raphnet / 8BitDo Gbros** fallback.

---

## Highlights & What's New in v2.0.0

### Redesigned Interface & Settings
- **Unified Vivimagic GC Suite Branding**: Consistent application and installer naming (`Vivimagic GC Suite.exe` on Windows, `Vivimagic GC Suite.app` on macOS, and native Linux desktop integration).
- **Dedicated Settings Pop-Up Window**: Replaced inline settings clutter with a clean icon-only Settings button featuring a full 360° hover rotation animation.
- **Separate Light & Dark Mode Buttons**: Dedicated Light Mode and Dark Mode toggle buttons with custom animated SVG icons, plus dark title bar support on Windows 10/11.
- **Persistent Live System Tray Toggle**: Turn the background Windows System Tray icon on or off anytime via a saved checkbox inside Settings without stopping the 4-port bridge.
- **Dark Mode Contrast Polish**: Custom `ThemedFlatButton` rendering keeps disabled button labels crisp white/light while install or update tasks are running, and restores literal `&` characters across all buttons and headings.

### Controller Engine & Input Fidelity
- **True Smooth 0–100% Analog Triggers**: Restored v1-faithful progressive L/R analog shoulder trigger scaling with exact WUP-028 `0x13` initialization order and full PC-mode HID/WinMM analog trigger support — pull smoothly from 0% to 100% at the exact speed of your press with zero artificial digital click snapping.
- **1000 Hz MMCSS Low-Jitter Polling**: Hardware timer precision (`timeBeginPeriod(1)` + `AvSetMmThreadCharacteristics("Games")`) for sub-millisecond consistency.
- **Dual Virtual Controller Backend**: Hot-switch between **Xbox 360 (XInput)** and **Sony DualShock 4 (`054C:05C4`)** via ViGEmBus.
- **Per-Port P1–P4 Calibration & Anti-Snapback**: 360° 8-notch octagonal gate calibration, per-port stick deadzones, and a configurable software anti-snapback velocity filter.
- **Sigma-Delta PWM Rumble Sculpting**: Smooth dual-motor force feedback mapping for GameCube controllers.

### Live Controller Tester & Diagnostics
- **GameCube-Authentic Button Grid**: Streamlined 5×2 layout showing only physical GameCube buttons (`A, B, X, Y, Z`, `START`, `UP, DOWN, LEFT, RIGHT`) — removed non-GameCube `L-CLK`, `R-CLK`, and `BACK` tiles.
- **Live Adapter & Controller Status**: Main status banner updates automatically in real time as soon as an adapter connects in Wii U / NS mode and controllers are ready.
- **Built-In GitHub Auto-Update Checker**: Check `Vivimagic/GameCube-Bridge-Studio` releases straight from Settings with one-click download and launch.
- **Window-Focus Dolphin Handover**: Seamlessly yields exclusive WinUSB access to Dolphin/Slippi when focused and reclaims XInput/DS4 immediately on alt-tab.
- **Cross-Platform Native Installers**: Native Windows WinForms `.exe`, macOS Universal `.dmg` / `.app.zip` (with optional Apple notarization), and Linux/Steam Deck `.deb` / `.tar.gz` / `.sh` with native `/dev/uinput` + `libusb-1.0` daemon.

---

## Downloads

| Platform | File | Notes |
| --- | --- | --- |
| **Windows 10 / 11 (64-bit)** | `Vivimagic-GC-Suite-v2.0.0-win-x64.exe` | Run directly — silent WinUSB binding + ViGEmBus + Live Tester |
| **macOS (Apple Silicon & Intel)** | `Vivimagic-GC-Suite-v2.0.0-macos-universal.dmg` | Open DMG and drag **Vivimagic GC Suite.app** to Applications |
| **macOS (Portable Archive)** | `Vivimagic-GC-Suite-v2.0.0-macos-app.zip` | Resource-fork-safe zip of `Vivimagic GC Suite.app` |
| **Linux (Debian / Ubuntu)** | `vivimagic-gc-suite_2.0.0_all.deb` | Native package with udev rules + `/dev/uinput` daemon |
| **Linux / Steam Deck (Portable)** | `Vivimagic-GC-Suite-v2.0.0-linux.tar.gz` | Includes GUI installer, SVG icon, and quick-start guide |
| **Linux (Direct Script)** | `Vivimagic-GC-Suite-v2.0.0-linux.sh` | Run `chmod +x` and execute directly |
| **Verification** | `SHA256SUMS.txt` | SHA-256 checksums for every release binary |

## Quick Start
1. Flip your GameCube adapter switch to **Wii U / Switch (NS)** mode and plug in **both** the Black (Data) and Gray (5V Rumble) USB cables.
2. Run the installer for your operating system above and click **Install Driver** (or **Reinstall Fresh Settings** if upgrading from v1).
3. Click **Test Pad** to verify smooth 0–100% analog triggers, sticks, all 10 GameCube buttons, and rumble motors live.

---
Copyright (c) 2026 Ashley Glover. All Rights Reserved.
