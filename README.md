# PB Viewer

A personal pickleball analytics tool built on [PBVision](https://pb.vision) game exports.

**[→ Open PB Viewer](https://YOUR-USERNAME.github.io/pbviewer)**
*(replace YOUR-USERNAME with your GitHub username after deploying)*

---

## What it does

- **Court Viewer** — visualizes shot patterns on a full court. Filter by shot type, outcome, movement category, and date range. Highlights retreating vs advancing vs lateral movement.
- **Coaching Insights** — automatically computed and ranked based on your data: 3rd shot selection, kitchen transition gap, retreating shot patterns, poach discipline, and more.
- **Dashboard** — win rate, accuracy, rating over time, and shot mix across all games.
- **My Games** — full game library with per-game stats.

## Data

49 games (Oct 2025 – Mar 2026) are pre-loaded. Use **+ Add Games** to import additional PBVision JSON exports directly in the browser.

> **Privacy note:** All data stays in your browser. Nothing is sent to any server.

## Deployment

This is a single self-contained HTML file — no build step, no dependencies, no backend.

Hosted via [GitHub Pages](https://pages.github.com).

## Updating

When you have a new version of the file:
1. Replace `index.html` in this repo with the new version
2. Commit and push — GitHub Pages redeploys automatically within ~60 seconds
