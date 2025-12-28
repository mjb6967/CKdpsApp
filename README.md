# ツCKヤ DPS Meter

A real-time DPS meter for **Throne and Liberty** that parses combat logs and displays detailed analytics through a web-based dashboard.

🌐 **[Visit Website](https://ckdps.netlify.app/)** · 📥 **[Download Latest Release](https://github.com/mjb6967/CKdpsApp/releases/latest/download/TL-DPS-Meter.zip)**

---

## About

ツCKヤ DPS Meter reads your Throne and Liberty combat logs and provides real-time damage tracking, build testing tools, and dungeon run analytics. It runs locally on your machine with a WebSocket server that connects to a browser-based dashboard.

---

## Features

### Core
- **Real-Time Tracking** — Live DPS updates every 500ms
- **Build Testing** — Standardized 60-second tests for consistent build comparisons
- **Skills Breakdown** — Per-skill damage, crit rates, and heavy attack stats
- **Weapon Stats** — Damage contribution by weapon type

### Analysis
- **Rotation View** — Timeline visualization of your skill usage with gap detection
- **Compare Builds** — Side-by-side comparison of 2-4 saved encounters
- **Top Hits** — Track your highest damage hits

### Dungeon Runs
- **Run Builder** — Record full dungeon runs by dragging encounters from timeline
- **Run Summary** — View saved runs with boss highlights and grouped adds
- **Target Assignment** — Categorize targets (Archboss, Raid Boss, Dungeon Boss, Adds, etc.)

### Other
- **Dashboard** — Lifetime stats, recent activity, and quick actions
- **Skill Assignment** — Assign skills to weapons for detailed weapon breakdowns
- **Party DPS (Beta)** — Share stats with party members via Discord
- **Hotkey Support** — Quick reset via customizable hotkey

---

## Requirements

- Windows 10 or 11
- Throne and Liberty with combat logging enabled
- Modern web browser (Chrome, Firefox, Edge)

---

## Installation

1. **Download** the [latest release](https://github.com/mjb6967/CKdpsApp/releases/latest/download/TL-DPS-Meter.zip)
2. **Extract** the zip to any folder
3. **Run** `TL-DPS-Meter.exe`
4. The dashboard opens automatically in your browser

No installation required — it's a standalone portable application.

---

## Setup

### Enable Combat Logging in Throne and Liberty

1. Open T&L Settings
2. Go to **Gameplay** → **Combat**
3. Enable **Combat Log**
4. Logs will be saved to: `%LOCALAPPDATA%/TL/Saved/CombatLogs`

### First Use

1. Launch the DPS Meter
2. Click **Reset** before starting combat
3. Fight something
4. Watch your stats update in real-time

---

## Usage Tips

- **Reset before each pull** — Ensures clean data for each encounter
- **Save builds with tags** — Filter and compare saved encounters by build name
- **Use 60-second tests** — Standardized duration for fair build comparisons
- **Assign skills to weapons** — Get per-weapon damage breakdowns
- **Categorize targets** — Different gap thresholds for bosses vs adds

---

## How It Works

1. T&L writes combat events to CSV log files
2. The DPS Meter parses these logs in real-time
3. Stats are broadcast via WebSocket to the browser dashboard
4. Data is stored locally in JSON files (encounters, runs, config)

All processing happens locally on your machine. No data is sent anywhere unless you opt into Party DPS.

---

## Files Created

The application creates these files in the same folder as the exe:

| File | Purpose |
|------|---------|
| `config.json` | Settings (log path, player filter, hotkey) |
| `encounters.json` | Saved build test encounters |
| `runs.json` | Saved dungeon runs |
| `dungeons.json` | Custom dungeon types |
| `skill_settings.json` | Skills that can't crit/heavy |
| `skill_assignments.json` | Skill-to-weapon mappings |
| `target_assignments.json` | Target categorizations |

---

## FAQ

**Q: Why is there a ~10 second delay?**  
A: Throne and Liberty buffers combat log writes. This is a game limitation, not the meter.

**Q: Can I get banned for using this?**  
A: The meter only reads log files that T&L creates. It doesn't inject, modify, or interact with the game in any way.

**Q: Why does my antivirus flag it?**  
A: PyInstaller executables are sometimes flagged as false positives. The app is safe.

**Q: How do I filter to only my character?**  
A: Settings → Enter your character name in the Player Filter field.

---

## Support

- **Issues & Bugs**: [GitHub Issues](https://github.com/mjb6967/CKdpsApp/issues)
- **Website**: [YOUR-SITE.netlify.app](https://ckdps.netlify.app/)

---

## License

This software is provided free for personal use. Not open source.

---

Made for the Throne and Liberty community.
