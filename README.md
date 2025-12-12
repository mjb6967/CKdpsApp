# ツCKヤ DPS Meter

A real-time DPS meter for **Throne and Liberty**. Track damage, skills, and crits in real-time. Analyze your rotation with piano-roll timelines. Save encounters, tag your builds, and compare up to 4 side-by-side. Party mode for group DPS. Reads combat logs only — no injection, fully local.

---

## 📸 Screenshots

| Dashboard |
|-----------|
| ![Dashboard](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/dashboard.png) |

| Skills | Top Hits | Rotation |
|--------|----------|----------|
| ![Skills](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/skills.png) | ![Top Hits](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/top-hits.png) | ![Rotation](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/rotation.png) |

| Timeline | Saved | Compare |
|----------|-------|---------|
| ![Timeline](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/timeline.png) | ![Saved](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/saved.png) | ![Compare](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/compare.png) |

| Skill Settings | Log File | Party DPS |
|----------------|----------|-----------|
| ![Skill Settings](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/skill-settings.png) | ![Log File](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/log-file.png) | ![Party DPS](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/party-dps.png) |

| Weapon Stats | Skill Assign |  |
|--------------|--------------|--|
| ![Weapon Stats](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/weapon-stats.png) | ![Skill Assign](https://raw.githubusercontent.com/mjb6967/CKdpsApp/screenshots/skill-assign.png) |  |

---

## ✨ Features

### Real-Time Tracking
- **Live DPS** — Updates automatically when combat logs are written
- **1-Min DPS** — First 60 seconds tracked separately for fair comparisons
- **Skill Breakdown** — Damage per skill with hit counts, crit rates, heavy rates
- **Crit & Heavy Analysis** — Normal, Crit, Heavy, and Crit+Heavy tracking
- **Timeline** — Visual DPS graph and piano-roll skill timeline
- **Top Hits** — Your biggest hits with medals 🥇🥈🥉
- **Target Breakdown** — Damage split by enemy

### Rotation Analysis
- **Piano Roll** — See exactly when each skill was used over 60 seconds
- **Gap Detection** — Identify downtime periods in your rotation
- **Segment Breakdown** — DPS split into quarters (0-15s, 15-30s, etc.)
- **Activity Rate** — Percentage of time dealing damage
- **Peak 5s DPS** — Find your highest burst window
- **Performance Insights** — Automated tips based on your data

### Weapon Stats *(New in v0.18)*
- **Damage by Weapon** — See how much each weapon contributes
- **Skill Assignment** — Drag-and-drop skills to categorize by weapon
- **Mastery Category** — For weapon-neutral abilities like passives
- **Persistent Config** — Assignments saved to `weapon_config.json`

### Build Optimization
- **Save Encounters** — Store your runs with custom build tags
- **Load Encounters** — View saved encounters in the main dashboard
- **Compare 2-4 Builds** — Side-by-side comparison with rankings
- **Filter & Sort** — Find saved encounters by build name or DPS
- **Skill Settings** — Mark skills that can't crit/heavy for accurate rates

### Party Mode *(Beta)*
- **Group DPS Sync** — Compare damage with party members in real-time
- **No Setup Required** — Built into the app, just enable and login with Discord
- **Leader Controls** — Party leader starts/ends encounters for everyone
- **Per-Target Results** — See who topped damage on each enemy

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
3. **Click Reset** (or press `Ctrl+Tab`) before each encounter for clean data
4. **View tabs** — Skills, Top Hits, Rotation, Timeline, Weapons

### Understanding the Header Stats
| Stat | Meaning |
|------|---------|
| **DPS** | Total damage ÷ duration (all time) |
| **1-Min DPS** | First 60 seconds only — standard for comparisons |
| **Normal** | Hits that were neither crit nor heavy |
| **Crit Rate** | Adjusted % (excludes skills marked "cannot crit") |
| **Heavy Rate** | Adjusted % (excludes skills marked "cannot heavy") |
| **Crit+Heavy** | Hits that were BOTH crit AND heavy |

### Saving & Comparing Builds
1. After an encounter, click **Save Encounter**
2. Add a **build tag** (e.g., "GS/Dagger Crit Build")
3. Go to **Saved** tab to view history
4. Go to **Compare** tab → select 2-4 encounters
5. See side-by-side stats for the **first 60 seconds** of each

### Weapon Stats
1. Go to **Skill Assign** tab
2. **Drag skills** to their weapon category (Greatsword, Dagger, etc.)
3. Use **Mastery** for weapon-neutral abilities (passives, buffs)
4. Go to **Weapon Stats** tab to see damage breakdown by weapon
5. Assignments persist across sessions

### Skill Settings
1. Go to **Skill Settings** tab
2. Mark skills that **cannot crit** or **cannot heavy**
3. Header rates will adjust to exclude these skills
4. If a skill later crits/heavies, the setting auto-removes

### Party Mode
1. Go to **Party DPS** tab
2. Toggle **Party Broadcasting** ON
3. **Login with Discord** (first time only)
4. **Create** or **Join** a party with the 4-letter code
5. Party leader clicks **Start/End Encounter**
6. Results sync automatically!

---

## ⌨️ Hotkeys

| Hotkey | Action |
|--------|--------|
| `Ctrl+Tab` | Reset encounter (global, works in-game) |

Configure in Settings. A beep confirms the reset.

---

## 🔧 Configuration

Settings are stored in `config.json` next to the exe:

```json
{
  "log_path": "auto",
  "player_name": "",
  "hotkey_enabled": true,
  "hotkey": "ctrl+tab",
  "hotkey_sound": true,
  "party_enabled": false
}
```

| Setting | Description |
|---------|-------------|
| `log_path` | Path to combat logs folder, or `"auto"` for default |
| `player_name` | Filter to only show your damage (leave empty for all) |
| `hotkey_enabled` | Enable/disable global hotkey |
| `hotkey` | Reset hotkey combo (`ctrl+tab`, `ctrl+r`, `f9`-`f12`, etc.) |
| `hotkey_sound` | Play beep on hotkey press |
| `party_enabled` | Remember party broadcasting state |

### Other Data Files
| File | Purpose |
|------|---------|
| `encounters.json` | Saved encounter history |
| `skill_settings.json` | Skills marked as cannot crit/heavy |
| `weapon_config.json` | Skill-to-weapon assignments |

---

## 📋 Changelog

### v0.19-beta *(Latest)*
- **FIX:** Drag-and-drop skill assignment now works properly
- **NEW:** Skill assignments persist to `weapon_config.json`
- **IMPROVED:** Prevents UI re-rendering during drag operations

### v0.18-beta
- **NEW:** Weapon Stats tab — see damage breakdown by weapon
- **NEW:** Skill Assign tab — drag-and-drop skills to weapons
- **NEW:** Mastery category for weapon-neutral skills
- **IMPROVED:** Visual weapon cards with damage percentages

### v0.17-beta
- **FIX:** Party Broadcasting now works properly with Discord OAuth
- **FIX:** Token refresh and auto-reconnect
- **IMPROVED:** Better status indicators for party connection

### v0.14-beta
- **NEW:** Party broadcasting built into main app
- **NEW:** Discord OAuth for party authentication
- **NEW:** Load Encounter — view saved encounters in main UI
- **NEW:** Piano-roll skill timeline visualization
- **NEW:** Rotation analysis with gap detection
- **NEW:** Compare up to 4 encounters (was 2)
- **NEW:** Skill Settings for accurate crit/heavy rates

### v0.13-beta
- **NEW:** Guide modal with comprehensive documentation
- **NEW:** Normal hits tracking in header
- **IMPROVED:** Segment breakdown with color-coded bars

---

## ❓ FAQ

**Q: Is this bannable?**  
A: This tool only reads log files the game creates. It does not inject, modify, or interact with the game. Use at your own discretion.

**Q: Why no damage showing?**  
A: Make sure Combat Meter is enabled in-game (Ring Menu). Logs only write after leaving combat.

**Q: Why are my crit/heavy rates wrong?**  
A: Some skills can't crit or heavy. Go to Skill Settings tab and mark them — the rates will adjust.

**Q: Party mode not connecting?**  
A: Disable and re-enable Party Broadcasting to refresh your Discord login.

**Q: Drag-and-drop not working?**  
A: Make sure you're on v0.19 or later. Earlier versions had a bug.

**Q: Windows blocks the download?**  
A: Click "Keep" or "More info" → "Run anyway". This is normal for unsigned apps.

**Q: How do I reset my data?**  
A: Delete `encounters.json`, `skill_settings.json`, and `weapon_config.json` next to the exe.

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
