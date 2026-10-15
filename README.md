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
