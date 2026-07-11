# ⚽ Football Project

Two self-contained apps, each a **single HTML file** — no frameworks, no build step, no server.

- **`index.html`** — the World Cup **Simulator** (create teams, simulate matches & tournaments, stats, save/load). Details below.
- **`game.html`** — a playable **2D arcade soccer game** with real-time controls, AI, ball physics, hand-drawn player sprites, and its own tournament mode. Open it and pick *Play Match* or *Tournament Mode*.
- **`baseball.html`** — a playable **2D arcade baseball game**. You bat and pitch (fielding & base-running are automatic); full stadium, sprites, HUD, exhibition (3/6/9 innings + extra innings), team creator, and a tournament mode (4/8/16/32 teams, drag bracket, Play / Simulate / Watch, stat leaders).

### ⚾ baseball.html — controls
| Mode | Keys |
|------|------|
| **Batting** | `← →` aim · `Space` swing · `Shift` power swing · `E` bunt |
| **Pitching** | `← ↑ ↓ →` aim · `1` fastball `2` curve `3` slider `4` changeup · `Space` throw (`Shift` = max velocity) |

You bat in the top of each inning and pitch in the bottom (vs CPU). Choose *Watch CPU vs CPU* to spectate. Runs in the current session only — no saving.

There's also an **🎓 Academy**: three basic prospects (each with one maxed signature skill and one decent focus stat) that you can **train** to raise their ratings, then **add to any team's roster**.

### 🎮 game.html — the playable game
Open in a browser and use the keyboard:

| Key | Action |
|-----|--------|
| `W A S D` | Move |
| `Space` | Shoot (hold to power up) / slide tackle when defending |
| `E` | Pass |
| `Shift` | Sprint |
| `Q` | Switch player |

Modes: **Play Match** (pick teams, 3/5/10-min games, difficulty, or watch AI vs AI), **Team Creator** (name, colours, ratings, signature stats), **Tournament Mode** (4/8/16/32 teams — build & drag your own bracket, then Play / Simulate / Watch each tie). Canvas rendering targets ~60 FPS; runs only in the current session (no saving, by design). Offside is intentionally not enforced in the arcade match for smoother flow.

---

# ⚽ World Cup Simulator (`index.html`)

An interactive FIFA-style World Cup simulator in a **single HTML file** — no frameworks, no build step, no server. Just open `index.html` in any browser.

## Features

- **Team & Player creator** — build national squads. Every player has a position (GK/DEF/MID/FWD), an overall rating (1–100), and **one signature stat locked at 100** (Pace, Dribbling, Finishing, Goalkeeping, Free Kicks, …). All other stats are generated from the overall, biased by position.
- **16 preset nations** with real-world star players so you can play instantly.
- **Match engine** — minute-by-minute simulation using player ratings, signature stats, momentum and weighted randomness. Extra time and penalty shootouts supported. No two matches are ever identical, and underdogs can win.
- **Match report** — final score, goal scorers with minutes, possession, shots, shots on target, corners, cards, offsides, a full match timeline, and Man of the Match.
- **Realistic events** — goals, headers, long shots, free kicks, breakaways, saved/missed penalties, yellow & red cards (incl. second yellows), injuries, substitutions, offside goals, and own goals.
- **Tournament mode** — group stage → knockouts (R16/QF/SF) → third-place playoff → final, with automatic standings (points, goal difference), qualification and bracket building.
- **Statistics** — top scorers, assists, saves, clean sheets, cards, Man of the Match, and team records tracked across the whole tournament.
- **Dark, football-themed responsive UI** — flags, badges, standings tables, bracket view, animated score updates.
- **Save system** — save/load to the browser plus JSON export/import.

## Usage

Open `index.html` in a browser. Head to **Teams → Load 16 preset nations**, then jump into **Match** for an exhibition or **Tournament** to run a full World Cup.

## Code structure

All in `index.html`, organised into modules: `Player`, `Team`, `MatchEngine`, `TournamentEngine`, `StatisticsEngine`, `SaveManager`, and a `UI` manager.
