# Forza Horizon 6 - Legacy Hardware & FHE01 Fix Wrapper 🏎️💨

[![GitHub Release](https://img.shields.io/github/v/release/Quantum1-dev/Forza-Horizon-6-UNIVERSAL-Fix-For-AMD)](https://github.com/Quantum1-dev/Forza-Horizon-6-UNIVERSAL-Fix-For-AMD/releases/latest)
[![Discord](https://img.shields.io/badge/Discord-Join%20Us-7289DA?logo=discord&logoColor=white&style=flat-square)](https://discord.gg/arP3DjMQGC)

A refined, high-performance DirectX 12 proxy wrapper designed to bypass compatibility blocks and resolve initialization crashes (**FHE01 Context 190000 / 030000**) in *Forza Horizon 6*. 

Optimized specifically for legacy GPU architectures (such as AMD Polaris RX 400/500 series) to ensure proper Feature Level translation and un-throttled VRAM allocation without triggering internal anti-tamper memory flags.

---

## ✨ Features

- **Clean Proxy Design:** Uses native system export forwarding to eliminate aggressive runtime memory patching (`VirtualProtect` hooks), completely preventing anti-tamper security violations.
- **Optimized Memory Profiling:** Removes artificial 4GB limitations, unlocking a stable **8GB memory profile allocation** to prevent streaming asset choked crashes.
- **Zero-Footprint Execution:** Mutes active folder text logging routines that trigger dynamic verification scanner blocks on game boot.
- **DirectX Feature Level Spoofing:** Safely forces the engine handshake to recognize target feature parameters required for initialization.

---

## 📥 Installation

Follow these steps carefully to apply the fix:

1. Go to the [Releases](https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPO_NAME/releases) page and download the latest zip archive.
2. Extract the files to reveal `d3d12.dll` (and `dxgi.dll` if included in your build).
3. Navigate to your main **Forza Horizon 6** game installation directory (where the main game executable file is located).
4. Paste the custom `.dll` files directly into that folder.
5. Launch the game normally.

> ⚠️ **Important Note on Drivers:** It is highly recommended to perform a clean driver wipe using **DDU (Display Driver Uninstaller)** and install updated community-modified graphics drivers before applying this fix. If Windows displays a WHQL digital signature warning during your driver setup, click **"Install Anyway"**.

---

## ❌ Troubleshooting (Cache Purge Guide)

If you have used older versions of hardware fixes or encounter sudden engine allocation exceptions, you must clear your local temporary cache:

1. Press **`Win + R`** on your keyboard to open the Run dialog box.
2. Type `%localappdata%` and press Enter. Locate and completely **delete** the `ForzaHorizon6` folder.
3. Open the Run dialog box again (**`Win + R`**), type `%temp%`, and press Enter.
4. Locate and delete the file named `ForteTemp.scratch` (if present).
5. Re-paste the refined fix files into your game directory and restart the game.

## Sources & Credits

This project builds upon existing open-source proxy mechanics. Full credit for the foundation of this tool belongs to the original authors:

* **Original Proxy Source Code:** [Megadroidgames / JuniorD-Isael] 
  * *Contribution:* Core DXGI/D3D12 architecture, VTable hooking structures, and the DirectX 12.1 / Mesh Shader bypass logic.

* **Modifications by Quantum1-dev:** * *Contribution:* Removed the forced 4GB/8GB iGPU VRAM spoofing present in the original source. This modified version safely passes your actual GPU memory directly to the engine, maximizing stability and preventing crashes specifically for users with Dedicated GPUs.
---
