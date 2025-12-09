# ツCKヤ DPS Meter

A real-time DPS meter for **Throne and Liberty**. Track damage, skills, and crits in real-time. Save encounters, tag your builds, and compare them side-by-side to optimize your setup. Party mode for group DPS. Reads combat logs only — no injection, fully local.

[![VirusTotal](https://img.shields.io/badge/VirusTotal-0%2F72%20Clean-brightgreen)](YOUR_VIRUSTOTAL_LINK_HERE)
[![License](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/Version-0.14--beta-orange)]()

---

## 📸 Screenshots

| Live Dashboard | Skill Breakdown | Build Comparison |
|----------------|-----------------|------------------|
|![image](https://github.com/mjb6967/CKdpsApp/blob/screenshots/live.png)| ![image](https://github.com/mjb6967/CKdpsApp/blob/screenshots/skills.png) | ![image](https://github.com/mjb6967/CKdpsApp/blob/screenshots/compare.png) |

---

## ✨ Features

### Real-Time Tracking
- **Live DPS** — Updates every 500ms as you fight
- **Skill Breakdown** — Damage per skill with hit counts, crit rates, heavy rates
- **Crit & Heavy Analysis** — Dedicated tabs for deep stat analysis
- **Timeline** — Visual DPS graph over encounter duration
- **Top Hits** — Your biggest hits with medals 🥇🥈🥉
- **Target Breakdown** — Damage split by enemy

### Build Optimization
- **Save Encounters** — Store your runs with custom build tags
- **Compare Builds** — Side-by-side comparison of first 60 seconds
- **Filter & Sort** — Find saved encounters by build name or DPS
- **Track Progress** — See how gear/skill changes affect performance

### Party Mode
- **Group DPS Sync** — Compare damage with party members in real-time
- **No Setup Required** — Built into the app, just enable and login with Discord
- **Leader Controls** — Party leader starts/ends encounters for everyone

---

## 🔒 Safety & Trust

This tool is **completely safe** and does not interact with the game in any way:

| What it does | What it does NOT do |
|--------------|---------------------|
| ✅ Reads combat log text files | ❌ No memory reading |
| ✅ Runs a local web server on your PC | ❌ No game injection |
| ✅ Opens dashboard in your browser | ❌ No packet sniffing |
| ✅ Connects to party server (optional) | ❌ No game file modification |

### Technical Details
- **Log Location:** `%LOCALAPPDATA%\TL\Saved\CombatLogs`
- **Local Server:** `localhost:8765` (never exposed to internet)
- **Party Server:** `tl-party-production.up.railway.app` (optional, Discord OAuth)

### Verify Yourself
- 🔍 [VirusTotal Scan](YOUR_VIRUSTOTAL_LINK_HERE) — 0/72 detections
- 📖 Source code is right here — inspect it yourself
- 🛡️ Windows SmartScreen warning is normal for unsigned apps — click "More info" → "Run anyway"

---

## 📥 Download & Install

### Quick Start
1. **[Download Latest Release](../../releases/latest)** — Get `TL-DPS-Meter.zip`
2. **Extract** anywhere (e.g., `C:\Games\TL-DPS-Meter`)
3. **Run** `TL-DPS-Meter.exe`
4. **Dashboard** opens automatically in your browser

### Enable Combat Logging (Required)
The game must be configured to write combat logs:

1. Open **Throne and Liberty**
2. Go to **Settings → Shortcuts → Ring Menu Settings**
3. Add **"Combat Meter"** to a Ring Menu slot
4. In-game, open Ring Menu and **activate Combat Meter**
5. Logs will appear in `%LOCALAPPDATA%\TL\Saved\CombatLogs`

> ⚠️ Logs are only written **after you leave combat** (zone out or wait between pulls)

---

## 🎮 How to Use

### Basic Usage
1. **Start the app** before playing
2. **Enter combat** — stats appear automatically
3. **Click Reset** before each boss/encounter for clean data
4. **View tabs** — Skills, Crits, Heavy, Timeline, Targets

### Saving & Comparing Builds
1. After an encounter, click **Save Encounter**
2. Add a **build tag** (e.g., "GS/Dagger Crit Build")
3. Go to **Saved** tab to view history
4. Select two encounters → Click **Compare**
5. See side-by-side stats for the **first 60 seconds** of each

### Party Mode
1. Go to **Party** tab
2. Enable **Party Broadcasting**
3. **Login with Discord** (first time only)
4. **Create** or **Join** a party with the 4-letter code
5. Party leader clicks **Start/End Encounter**
6. Results sync automatically!

---

## ⌨️ Hotkeys

| Hotkey | Action |
|--------|--------|
| `Ctrl+Tab` | Reset encounter (configurable in Settings) |

---

## 🔧 Configuration

Settings are stored in `config.json` next to the exe:

```json
{
  "log_path": "auto",
  "player_name": "",
  "hotkey": "ctrl+tab",
  "party_enabled": false
}
```

| Setting | Description |
|---------|-------------|
| `log_path` | Path to combat logs folder, or `"auto"` for default |
| `player_name` | Filter to only show your damage (leave empty for all) |
| `hotkey` | Reset hotkey combo |
| `party_enabled` | Remember party broadcasting state |

---

## 🏗️ Building from Source

If you prefer to run from source:

### Requirements
- Python 3.10+
- Dependencies: `pip install -r requirements.txt`

### Run
```bash
python server.py
```

### Build Executable
```bash
pip install pyinstaller
build.bat
```

Output will be in `dist/` folder.

---

## 📋 Changelog

### v0.14-beta
- **NEW:** Party broadcasting built into main app (no separate agent)
- **NEW:** Discord OAuth for party authentication
- **IMPROVED:** Auto-reconnect to party server
- **FIX:** Various bug fixes and stability improvements

### v0.13-beta
- **NEW:** Build comparison feature
- **NEW:** First 60 seconds tracking for fair comparisons
- **IMPROVED:** Skill breakdown UI

[Full Changelog](CHANGELOG.md)

---

## 🤝 Contributing

Contributions welcome! Feel free to:
- 🐛 Report bugs via [Issues](../../issues)
- 💡 Suggest features
- 🔧 Submit pull requests

---

## 📄 License

This project is licensed under the **GPL v3 License** — see [LICENSE](LICENSE) for details.

This means you can:
- ✅ Use it freely
- ✅ Modify it
- ✅ Distribute it
- ⚠️ But you must also open source any modifications

---

## ☕ Support

If you find this useful, consider:

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-yellow?logo=buy-me-a-coffee)](https://buymeacoffee.com/SirPHz)

---

## 📬 Contact

- **Discord:** [Your Discord Server](YOUR_DISCORD_LINK)
- **Issues:** [GitHub Issues](../../issues)

---

*This project is not affiliated with NCSoft or Amazon Games. Throne and Liberty is a trademark of NCSoft Corporation.*
