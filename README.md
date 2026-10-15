# 🛡️ Kavalon Antivirus — Next-Gen Windows 11 Security Suite

![Python](https://img.shields.io/badge/Python-3.11%20%7C%203.12%20%7C%203.13-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011%20(64--bit)-0078D6.svg)
![Status](https://img.shields.io/badge/Engine-Active%20Multi--Engine-10B981.svg)
![License](https://img.shields.io/badge/License-Proprietary-red.svg)

> **"This is an anti-virus that yes is made with the help of AI, however after review has actually stopped real malware."**

**Kavalon** is a multi-engine endpoint security application built for Windows 11. It pairs native operating system interfaces (AMSI, VSS Watchdogs, NTFS ADS streams) with static signature feeds (ClamAV CVD, YARA rules), multi-source cloud threat intelligence, and behavioural heuristics to outperform default defenses while keeping idle CPU and memory consumption minimal.

---

## ⚡ Highlights & Key Features

- 🧬 **Multi-Engine Synergy:** Combines custom YARA rules, Shannon entropy packed-binary detection, and Cisco ClamAV's database (3.6M+ threat signatures).
- 🪟 **Microsoft AMSI Native Integration:** Hooks into Windows `amsi.dll` to inspect in-memory PowerShell, VBScript, and Office macros directly before execution.
- 🎭 **Magic-Byte Masquerade Hunter:** Rapidly inspects true raw file headers (Magic Numbers). Files pretending to be `.png`, `.jpg`, or `.mp4` that secretly contain Windows Portable Executables (`MZ/PE`) or ELF binaries are flagged and neutralized instantly.
- 🪤 **Active Ransomware Honeypot & Burst Rate Limiter:** Deploys encrypted canary tripwires across user folders and terminates malicious process trees attempting unauthorized mass encryption within milliseconds.
- ⚡ **Low-Resource Footprint:** Optimized background monitoring that outperforms Windows Defender's typical idle resource usage.
- 🚀 **Built-in Over-The-Air (OTA) Updates:** Download definitions and engine updates with 1 click directly from GitHub Releases.
- ☣️ **AES/XOR Encrypted Quarantine Vault:** Quarantines threats in a secure `.qvault` format with safe restoration capabilities.

---

## 📦 Installation & Setup

You can choose between **Running the Standalone App** or running the **Automated Setup Installer**.

### Option A: Automated Setup (Recommended)
1. Download `Kavalon_Setup.bat` (and `Kavalon.exe`) from [Releases](https://github.com/hazkerz/kavalon/releases).
2. Right-click `Kavalon_Setup.bat` and choose **Run as administrator**.
3. The installer will automatically:
   - Copy `Kavalon.exe` to `C:\Program Files\Kavalon\`
   - Check and configure ClamAV multi-engine components
   - Create Start Menu and Desktop shortcuts

### Option B: Standalone Portable Executable
1. Download `Kavalon.exe` from [Releases](https://github.com/hazkerz/kavalon/releases).
2. Run `Kavalon.exe` directly anywhere on your system — all configurations and signature assets are embedded inside the executable.

### Option C: Source Code Execution
Clone the repository and install requirements:
```powershell
git clone https://github.com/hazkerz/kavalon.git
cd kavalon
pip install -r requirements.txt
python main.py
```

---

## 🛠️ Testing & Verification

Kavalon comes with a built-in automated test suite that validates synthetic signature catches, entropy detection, quarantine vault encryption, and honeypot triggers in an isolated sandbox:

```powershell
python test_suite.py
```

---

## 🐛 Bug Reports & Contributing

We welcome bug reports, false positive reports, and performance feedback! Please submit any issues via the GitHub Issues tab.

---

## 📄 License & Intellectual Property

Copyright © 2026 **hazkerz**. All Rights Reserved.  
This software is provided under a proprietary license for personal and non-commercial security use. You may run and report bugs on this software, but unauthorized redistribution, modification, reverse engineering, or re-branding of the binaries or source code is strictly prohibited. See [LICENSE](LICENSE) for full details.
