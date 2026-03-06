<div align="center">

<img src="icon.ico" width="80" height="80" alt="RBXL Extractor Logo"/>

# RBXL Extractor

**Extract every Lua script from any Roblox place file — instantly.**

[![Discord](https://img.shields.io/badge/Discord-Join%20Server-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/AFJdJ3YCc3)
[![Python](https://img.shields.io/badge/Python-3.12+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Platform](https://img.shields.io/badge/Platform-Windows-0078D4?style=for-the-badge&logo=windows&logoColor=white)](https://github.com)
[![Version](https://img.shields.io/badge/Version-1.0-white?style=for-the-badge)](https://github.com)

---

*A sleek, modern desktop tool for extracting and analysing Lua scripts from `.rbxl` and `.rbxlx` Roblox place files.*

</div>

---

## ✦ What It Does

RBXL Extractor scans any Roblox place file and pulls out every single Lua script inside it. Whether you're auditing a game for backdoors, studying how a game is built, or archiving scripts — this tool does it in seconds.

- Supports both `.rbxl` (binary) and `.rbxlx` (XML) formats
- Extracts hundreds or thousands of scripts at once
- Automatically saves scripts to an organised folder structure
- Flags suspicious code patterns like `loadstring`, HTTP calls, and obfuscation

---

## ✦ Features

| Feature | Description |
|---|---|
| 🔍 **Script Extraction** | Pulls every `ProtectedString` source from any place file |
| ⚠️ **Security Analysis** | Flags `loadstring`, `HttpService`, `getfenv`, `require(id)`, `base64` |
| 📁 **Auto Save** | Scripts saved automatically to `rblxparser/extracted_scripts/<placename>/` |
| 📦 **Export as .zip** | Download all scripts as a single zip file |
| 🖥️ **Modern UI** | Clean black & white desktop interface built with CustomTkinter |
| 💬 **Discord** | One-click link to the community Discord server |

---

## ✦ Screenshots

> *Clean, minimal black UI with script list, security flags, and export options.*

---

## ✦ Getting Started

### Option A — Run from source

**1. Make sure you have Python 3.12+ installed**
Download from [python.org](https://python.org) — tick **"Add Python to PATH"** during install.

**2. Clone this repo**
```bash
git clone https://github.com/yourusername/rbxl-extractor.git
cd rbxl-extractor
```

**3. Install dependencies**
```bash
pip install customtkinter pillow
```

**4. Run the app**
```bash
python main.py
```

---

### Option B — Download the .exe

1. Go to the [Releases](https://github.com/aaadsad7/rblxparser/releases) page
2. Download `RBXL Extractor.exe`
3. Double click and run — no Python needed

---

## ✦ How To Use

```
1.  Launch the app
2.  Click "Choose File"
3.  Select your .rbxl or .rbxlx place file
4.  Wait for extraction to complete
5.  Scripts are automatically saved to:
         rblxparser/
         └── extracted_scripts/
             └── YourPlaceName/
                 ├── script_0.lua
                 ├── script_1.lua
                 └── ...
6.  Click "Open Extracted Folder" to browse scripts
7.  Optionally click "Save as .zip" to export everything
```

---

## ✦ Security Flags

The tool automatically scans every script and highlights suspicious patterns:

| Flag | What It Means |
|---|---|
| `loadstring` | Executes arbitrary code at runtime — common backdoor vector |
| `http call` | Script makes HTTP requests — could be phoning home |
| `getfenv` | Environment manipulation — often used by obfuscators |
| `require(id)` | Loads an external module by asset ID — can pull remote code |
| `base64` | Encoded strings — may be hiding obfuscated payloads |

---

## ✦ Folder Structure

When you run the app, it automatically creates:

```
rblxparser/
├── extracted_scripts/
│   └── YourPlaceName/
│       ├── script_0.lua
│       ├── script_1.lua
│       └── ...
└── discord.png
```

---

## ✦ Building from Source (.exe)

```bash
pip install pyinstaller
pyinstaller --onefile --windowed --name "RBXL Extractor" --icon "icon.ico" main.py
```

Your `.exe` will be in the `dist/` folder.

---

## ✦ Requirements

- Windows 10 / 11
- Python 3.12+ *(only if running from source)*
- `customtkinter`
- `pillow`

---

## ✦ Join the Community

Have questions, found a bug, or want to suggest a feature?

[![Discord](https://img.shields.io/badge/Join%20Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/AFJdJ3YCc3)

---

<div align="center">

Made with 🖤 &nbsp;|&nbsp; RBXL Extractor v1.0

</div>
