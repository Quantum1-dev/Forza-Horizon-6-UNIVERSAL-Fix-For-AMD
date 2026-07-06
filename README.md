# Forza Horizon 6 - Legacy Hardware & FHE01 Fix Wrapper 🏎️💨 [EXPERIMENTAL]

[![GitHub Release](https://img.shields.io/github/v/release/Quantum1-dev/Forza-Horizon-6-UNIVERSAL-Fix-For-AMD)](https://github.com/Quantum1-dev/Forza-Horizon-6-UNIVERSAL-Fix-For-AMD/releases/latest)
[![Discord](https://img.shields.io/badge/Discord-Join%20Us-7289DA?logo=discord&logoColor=white&style=flat-square)](https://discord.gg/arP3DjMQGC)
[![Status](https://img.shields.io/badge/Status-Experimental-red?style=flat-square)](#)

# Forza Horizon 6 — Legacy AMD Hardware Bypass 🏎️💨
### Optimized for Polaris/GCN Architectures (RX 400/500 Series & Vega iGPUs)

This repository contains the system-level `d3d12.dll` engine-handshake proxy module designed to bypass severe API verification deadlocks in *Forza Horizon 6* running on the modern ForzaTech engine. 

By spoofing critical API instructions (Shader Model 6.6+, Enhanced Barriers, Tier 3 Tiled Resources) alongside a highly specific runtime environment, this fix forces the game to communicate cleanly with older AMD architectures instead of freezing on a silent black screen.

---

## 🛑 Critical Driver Requirement (Do Not Skip!)

For this proxy fix to execute without causing an instant system-level rendering crash, you must be running a driver that handles advanced Agility SDK functions (like Work Graphs and Enhanced Barriers) on older architectures. 

### Recommended Driver Paths:
1. **The Official Preview Route:** `AMD Software: Adrenalin Edition 23.10.01.14 (DirectX 12 Agility SDK Support)`. This specific release natively bridges experimental Work Graphs 1.0 pipelines down to legacy silicon blocks.
2. **The Community Modded Route (Highly Recommended):** The absolute **latest modded drivers custom-optimized for the RX 500 series** are available directly on the **Quantum Gaming Discord**. These community-modified driver packages contain specialized performance tweaks, improved frame stability, and updated Vulkan/DX12 instruction sets for older architectures.

---

## 🛠️ Step-by-Step Installation Guide

### Step 1: Clean Current Drivers
1. Download **Display Driver Uninstaller (DDU)**.
2. Boot Windows into **Safe Mode**, run DDU, and select "Clean and Restart" to completely wipe your current graphics driver block.

### Step 2: Install the Driver Setup
1. Install either the official **23.10.01.14 preview driver** OR grab the specialized **RX 500 series modded drivers** from our Discord.
2. **Restart your PC** immediately after the installation finishes to solidify the display layer configuration.

### Step 3: Apply the Proxy Files
1. Download the custom **`d3d12.dll`** and **`dxgi.dll`** file from this fix bundle.
2. Navigate directly to your root game directory:
   * **Forza Horizon 6:** Paste it right next to the primary executable (`forzahorizon6.exe`).
3. Launch the game!

---

## ⚠️ Critical Troubleshooting & Stability Tweaks

### 1. Game Runs but Crashes After Sometime
* Keep the **`Shader Qualtiy`** at **Low** or **Medium**.
* Higher **`Shader Qualtiy`** Cause Crashes.


---

## 💬 Community Support & Video Tutorial

🎥 **Step-by-Step Video Guide:** For a full operational breakdown, video benchmarks, and visual confirmation of the fix running live, watch the official tutorial here: [Quantum Gaming - Video Guide](https://youtu.be/NGAN-pKYFa4)

📢 **Get the Latest Modded Drivers:** Head over to the **Quantum Gaming Discord Server** to fetch the newest custom GPU driver packages, share your performance optimization setups, and get direct assistance from fellow hardware creators!

## 🤝 Sources & Credits

This project builds upon existing open-source proxy mechanics. Full credit for the foundation of this tool belongs to the original authors:

* **Original Proxy Source Code:** [Megadroidgames / JuniorD-Isael] 
  * *Contribution:* Core DXGI/D3D12 architecture, VTable hooking structures, and the DirectX 12.1 / Mesh Shader bypass logic.

* **Modifications by Quantum1-dev:** 
  * *Contribution:* Removed the forced 4GB/8GB iGPU VRAM spoofing present in the original source. This modified version safely passes your actual GPU memory directly to the engine, maximizing stability and preventing crashes specifically for users with Dedicated GPUs.

[Source Code](https://github.com/Megadroidgames/Forza-Horizon-6-RX-580-FH201-FH205-Fix)  
