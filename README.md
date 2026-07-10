# ⚽ World Cup Simulator

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
