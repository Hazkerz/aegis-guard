[README.md](https://github.com/user-attachments/files/33472287/README.md)

# 🛡️ Aegis Guard Antivirus — Next-Gen Windows 11 Security Suite

![Python](https://img.shields.io/badge/Python-3.11%20%7C%203.12%20%7C%203.13-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011%20(64--bit)-0078D6.svg)
![Status](https://img.shields.io/badge/Engine-Active%20Multi--Engine-10B981.svg)
![License](https://img.shields.io/badge/License-Proprietary-red.svg)

> **"This is an anti-virus that yes is made with the help of AI, however after review has actually stopped real malware."**

**Aegis Guard** is a multi-engine endpoint security application built for Windows 11. It pairs native operating system interfaces (AMSI, VSS Watchdogs, NTFS ADS streams) with static signature feeds (ClamAV CVD, YARA rules), multi-source cloud threat intelligence, and behavioural heuristics to outperform default defenses while keeping idle CPU and memory consumption minimal.

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
1. Download `AegisGuard_Setup.bat` (or the release package) from [Releases](https://github.com/hazkerz/aegis-guard/releases).
2. Right-click and choose **Run as administrator**.
3. The installer will automatically:
   - Check and configure Python dependencies.
   - Install ClamAV definitions and set up real-time shields.
   - Create Start Menu and Desktop shortcuts.

### Option B: Manual / Portable Run
Clone the repository and install requirements:
```powershell
git clone https://github.com/hazkerz/aegis-guard.git
cd aegis-guard
pip install -r requirements.txt
python main.py
```

---

## 🛠️ Testing & Verification

Aegis Guard comes with a built-in automated test suite that validates synthetic signature catches, entropy detection, quarantine vault encryption, and honeypot triggers in an isolated sandbox:

```powershell
python test_suite.py
```

---

## 🐛 Bug Reports & Contributing

We welcome community feedback, bug reports, and false-positive submissions!
- Found a bug or an engine issue? Please open an issue on the [GitHub Issues](https://github.com/hazkerz/aegis-guard/issues) tab.
- Please provide as much detail as possible (Windows version, log output from the Settings & Logs tab, and reproduction steps).

---

## 📄 License

Copyright © 2026 **hazkerz**. All rights reserved.

This project is licensed under a proprietary source-available license. You may view and test the software for personal security use. Modification, redistribution, repackaging, or unauthorized derivative works are strictly prohibited without prior written consent.
