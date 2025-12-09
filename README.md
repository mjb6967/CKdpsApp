# ツCKヤ DPS Meter

A real-time DPS meter for **Throne and Liberty**. Track damage, skills, and crits in real-time. Save encounters, tag your builds, and compare them side-by-side to optimize your setup. Party mode for group DPS. Reads combat logs only — no injection, fully local.

---

## 📸 Screenshots

| Live Dashboard | Skill Breakdown | Build Comparison |
|----------------|-----------------|------------------|
| ![Live](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/live.png) | ![Skills](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/skills.png) | ![Compare](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/compare.png) |

---

## ✨ Features

### Real-Time Tracking
- **Live DPS** — Updates automatically when combat logs are written
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

### How It Works
- **Log Location:** `%LOCALAPPDATA%\TL\Saved\CombatLogs` — plain text CSV files created by the game
- **Local Server:** Runs on `localhost:8765` — never exposed to the internet
- **Party Server:** `tl-party-production.up.railway.app` — optional, uses Discord login

### Why SmartScreen Warning?
Windows shows "Unknown Publisher" for apps without a code signing certificate ($300+/year). This is normal for indie tools. Click **"More info"** → **"Run anyway"** to proceed.

---

## 📥 Download & Install

### Quick Start
1. **[Download Latest Release](../../releases/latest)** — Get `CKDPS.zip`
2. **Extract** anywhere (e.g., `C:\Games\TL-DPS-Meter`)
3. **Run** `TL-DPS-Meter.exe`
4. **Dashboard** opens automatically in your browser

### Enable Combat Logging (Required)
The game must be configured to write combat logs:

1. Open **Throne and Liberty**
2. Go to **Ring Menu - Turn on Detailed Combat Log**
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

---

## ❓ FAQ

**Q: Is this bannable?**  
A: This tool only reads log files the game creates. It does not inject, modify, or interact with the game. Use at your own discretion.

**Q: Why no damage showing?**  
A: Make sure Combat Meter is enabled in-game (Ring Menu). Logs only write after leaving combat.

**Q: Party mode not connecting?**  
A: Disable and re-enable Party Broadcasting to refresh your Discord login.

**Q: Windows blocks the download?**  
A: Click "Keep" or "More info" → "Run anyway". This is normal for unsigned apps.

---

## ☕ Support

If you find this useful:

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-yellow?logo=buy-me-a-coffee)](https://buymeacoffee.com/SirPHz)

---

## 📬 Contact

- **Discord:** SirPHz
- **Issues:** [GitHub Issues](../../issues)

---

*This project is not affiliated with NCSoft or Amazon Games. Throne and Liberty is a trademark of NCSoft Corporation.*
