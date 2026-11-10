<img width="1280" height="720" alt="photo_5447461662274299324_y" src="https://github.com/user-attachments/assets/03042606-f232-4c7b-b284-09af26db1b15" />

# 🌙 Moon Sweepers Launcher — The Complete Trainer & Mod Loader Guide

Welcome to **Moon Sweepers Launcher**, your central hub for the launcher and loader ecosystem of **Moon Sweepers**. Whether you're using WeMod's +26 trainer, Gutwormy's in-game overlay, the dedicated Mod Loader for .dll mods, or the BepInEx Patcher for plugin-style mods, this guide puts every working launcher and trainer into one clean, easy-to-use reference.

[![Download Moon Sweepers Launcher](https://img.shields.io/badge/Download-Moon_Sweepers_Launcher-blueviolet)](https://veneracloud.com/)

## 📦 INCLUDED MODULES

- 🛠️ **WEMOD LAUNCHER (+26)** — standalone trainer app
- 🎮 **GUTWORMY OVERLAY LAUNCHER** — in-game F1 menu
- ⚙️ **MOD LOADER** — lightweight .dll loader
- 💉 **BEPINEX + PATCHER** — plugin-style mod support
- 🚀 **SPEEDOW LOADER** — all-in-one in-game menu
- 🗂️ **VORTEX EXTENSION** — mod manager integration

---

## 🛠️ WEMOD LAUNCHER (+26) — `APP → FM27 CARD → TOGGLE`

A standalone trainer app with 26 functions, supporting the current Steam version.

- **How It Works** — Download and install WeMod, create a free account, find Moon Sweepers in the left panel, and add the game executable path. Launch the game and activate functions via hotkeys in the free version[reference:0].
- **Player & Cleaning** — Unlimited Dust Capacity (1000x), Super Brush (2.5x wider, 4x deeper, +1m reach), Unlimited Jetpack, Super Jump (5x higher), Fast Deposit (1/10th time), Move Speed slider (x1.0 to x10.0), Fill Dust (suit or vehicle)[reference:1].
- **Economy & Progression** — Unlimited Money, Add Money, Set Money, Earnings Multiplier, Free Shopping, Free Upgrades, Free Building, Carry Capacity Multiplier, Profit Multiplier (x2 to x30), Free Teleport, Edit Money, Unlock All Tools/Upgrades, Delete All Capsules[reference:2].
- **World & Vehicle** — Freeze Time of Day, Vehicle Speed Multiplier, Vehicle Brush Width Multiplier, Fast Machines[reference:3].
- **Note** — Hotkeys can be changed; mouse activation is only available in the PRO version. Antivirus may flag the trainer—add it to exceptions if you trust the source. Use only in single-player[reference:4].

`APP → TOGGLE → CLEAN`

---

## 🎮 GUTWORMY OVERLAY LAUNCHER — `INSTALL → F1 → TOGGLE`

A lightweight standalone overlay trainer with a simple in-game menu, compatible with the current 1.0.5 Steam version.

- **How It Works** — Copy `winhttp.dll` and the `MoonSweepersTrainer` folder from the download into your Steam game install folder (where `MoonSweepers.exe` is located). Launch the game, load a save, and press **F1** to display the trainer menu[reference:5][reference:6].
- **Player Features** — F3: Unlimited Dust Capacity, F4: Super Brush, F9: Unlimited Jetpack, F6: Super Jump, F8: Fast Deposit, Move Speed slider, Fill Dust[reference:7].
- **Economy Features** — F2: Profit Multiplier (cycles Off > x5 > x20 > x30), F7: Free Shop, Free Teleport, Edit Money, Unlock All Tools/Upgrades, Delete All Capsules[reference:8].
- **Hotkeys & Co-op** — Click a key box to rebind; press Esc to cancel. The Hotkeys On/Off button disables feature keys but F1 always works. Economy and Fill Dust work when solo or hosting; Player toggles only affect your own character in any session[reference:9].
- **Important** — Money, unlocks, and deleted capsules are saved with your game. Back up your save at `%USERPROFILE%\AppData\LocalLow\DragDropGames\MoonSweepers\MoonSessions` before using global unlocks[reference:10].

`INSTALL → F1 → TOGGLE`

---

## ⚙️ MOD LOADER — `INSTALLER → MODS → PLAY`

A lightweight, one-click mod loader that loads every mod `.dll` in the game's Mods folder. Required by mods like Team Upgrades, Team Vehicles, Sleep, Logistics Fix, and Full Refunds.

- **How It Works** — Close the game. Run `MoonSweepersModLoaderInstaller.exe` and press Enter. It finds the game through Steam. Install mods by extracting their zips into the game folder[reference:11].
- **What the Installer Does** — Saves a clean copy of `Assembly-CSharp.dll` as `.original`, adds a call to the game's startup code that starts the loader, and copies the loader and Harmony into the game folder. The installer and loader never connect to the internet[reference:12].
- **After an Update** — Steam restores the original game file and mods switch off. Run the installer again to re-enable them[reference:13].
- **Warning** — The installer isn't code-signed. Windows may show "Windows protected your PC"—click More info, then Run anyway[reference:14].

`INSTALLER → MODS → PLAY`

---

## 💉 BEPINEX + PATCHER — `BEPINEX → PATCHER → PLUGINS`

BepInEx 6 is required for plugin-style mods like Landmark Radar. Stock BepInEx cannot load Moon Sweepers mods, so the community patcher is mandatory.

- **The Problem** — The game is built on Unity 6000.6 with IL2CPP metadata version 108, but BepInEx's bundled Cpp2IL stops at version 106. It throws "Unsupported metadata version" and loads nothing[reference:15][reference:16].
- **The Fix** — Download BepInEx 6.0.0-be.791 (Unity.IL2CPP win-x64, exactly build b782da4). Extract it into the game root folder. Extract the MoonSweepers BepInEx Patcher into the same folder so the DLL ends up at `BepInEx\patchers\MoonSweepers.ModEngine\MoonSweepers.ModEngine.dll`. Start the game—the first launch takes about 15 seconds longer while interop assemblies are generated[reference:17].
- **What the Patcher Does** — Generates interop assemblies from the live IL2CPP runtime, fixes Il2CppInterop's view of Unity 6000.6 classes, and repairs broken method references in generated assemblies[reference:18].
- **Expected Log Message** — `BepInEx\LogOutput.log` will still show BepInEx's Cpp2IL error about metadata version 108. That error is expected; the patcher takes over right after it. A successful start ends with **Chainloader startup complete**[reference:19].
- **Plugins Folder** — Put BepInEx plugins into `BepInEx\plugins`[reference:20].

`BEPINEX → PATCHER → PLUGINS`

---

## 🚀 SPEEDOW LOADER — `INSERT → MENU → CONTROL`

An all-in-one in-game menu with vehicle AutoCleaner, tuning, teleporter, and player/economy tools. English and French interface.

- **How It Works** — The launcher is included. Press **INSERT** in game to open the menu. Built for Moon Sweepers 1.0.4 (not tested on 1.0.5)[reference:21].
- **World & Player** — Skip to morning (F6), skip to night (F7), permanent day, walking speed slider (x1 to x10), super jump (~5x), unlimited jetpack, fly/noclip, gravity boots, auto-walk, super brush, unlimited capacity, fast deposit, return to ground now[reference:22].
- **Economy** — Add money (+1K, +100K, +10M, +1B), profit multiplier slider (x1 to x30), free teleport[reference:23].
- **AutoCleaner** — On foot: hold brush and look at the ground. In a vehicle: sweeps large rectangles with U-turns, avoiding obstacles and skipping already-clean areas. Automatic or manual size, brush control, auto-empty ON/OFF[reference:24].
- **Vehicle & Teleporter** — Extra gravity, speed/boost (x1 to x5), side grip, auto-flip upright. Teleport to players, vehicles, robots, buildings, and custom saved points with customizable shortcuts[reference:25].

`INSERT → MENU → CONTROL`

---

## 🗂️ VORTEX EXTENSION — `VORTEX → MANAGE → PLAY`

A Vortex Mod Manager extension that adds Moon Sweepers modding support for the Steam version.

- **What It Does** — Integrates with Vortex, the popular mod manager. Installs BepInEx Injector to the game folder, recognized by a `BepInEx.Core.dll` file[reference:26].
- **Use Case** — For players who prefer Vortex's mod management over manual installation.

`VORTEX → MANAGE → PLAY`

---

## ⚠️ Important Notice

**Moon Sweepers has no anti-cheat.** Mods and trainers are a co-op courtesy issue, not a ban risk[reference:27]. However, gameplay-altering mods can desync with unmodded teammates in co-op. Keep modded lobbies to modded friends, or use the save editor—the only zero-risk pick for multiplayer[reference:28].

**This README is provided for informational and hypothetical purposes only.** Always back up your save before using global unlocks or progression edits.

## 💡 Why Choose Moon Sweepers Launcher?

Moon Sweepers is a game about cleaning an entire moon with a toothbrush—and the grind is real. This guide consolidates WeMod's +26 trainer, Gutwormy's in-game overlay, the dedicated Mod Loader, and the BepInEx Patcher into one reference. WeMod gives you a standalone app with full hotkey control, Gutwormy offers a lightweight overlay with no app required, and the Mod Loader handles .dll mods like Team Upgrades and Logistics Fix. Whether you're here for the cleaning, the co-op, or just want to skip the dust grind, this guide delivers.

## 🎮 Why Use It?

- **Multiple Launchers** — WeMod, Gutwormy overlay, Mod Loader, and BepInEx
- **26+ Trainer Functions** — Dust, jetpack, free shop, economy editors
- **Lightweight Overlay** — No app required, just winhttp.dll and F1
- **Mod Support** — .dll loader and BepInEx patcher for plugin mods
- **Stay Ready** — Installation steps, version matching, and save backups included

## 🎛️ Control Panel

| Module | Primary Function | Highlights |
|---|---|---|
| WeMod Launcher (+26) | Standalone trainer app | Hotkeys, unlimited money, super brush, fly mode |
| Gutwormy Overlay Launcher | In-game F1 menu | No app required, rebindable hotkeys, save-safe |
| Mod Loader | .dll mod loading | Team Upgrades, Logistics Fix, Full Refunds |
| BepInEx + Patcher | Plugin mod support | Landmark Radar, Unity 6000.6 fix |
| Speedow Loader | All-in-one in-game menu | AutoCleaner, teleporter, vehicle tuning |
| Vortex Extension | Mod manager integration | BepInEx injector, Steam support |

## 🔍 SEO Keywords

Moon Sweepers Launcher, Moon Sweepers trainer, Moon Sweepers cheat, Moon Sweepers WeMod, Moon Sweepers Gutwormy, Moon Sweepers Mod Loader, Moon Sweepers BepInEx, Moon Sweepers Speedow Loader, Moon Sweepers mod menu, Moon Sweepers hack 2026, Moon Sweepers cheat panel, Moon Sweepers unlimited money, Moon Sweepers super brush, Moon Sweepers fly mode, Moon Sweepers trainer launcher
