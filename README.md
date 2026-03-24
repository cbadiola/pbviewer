# PB Viewer

A personal pickleball analytics tool built on [PBVision](https://pb.vision) game exports.

**[→ Open PB Viewer](https://YOUR-USERNAME.github.io/pbviewer)**
*(replace YOUR-USERNAME with your GitHub username after deploying)*

---

## Repository structure

```
pbviewer/
├── index.html          # App code (~131KB)
└── data/
    ├── games.json      # Game library with all shot data (~2.2MB)
    └── ratings.json    # Ratings timeline (~6KB)
```

The app loads `data/games.json` on startup. Update that file to add new games — the app picks up the new data on next page load without touching `index.html`.

## What it does

- **Court Viewer** — visualizes shot patterns on a full court with movement highlights, color modes, and coaching insights
- **Coaching Insights** — automatically computed: 3rd shot selection, kitchen transition gap, retreating patterns, poach discipline
- **Dashboard** — win rate, accuracy, rating over time, shot mix
- **My Games** — full game library

## Updating game data

When you have new PBVision exports, rebuild `data/games.json` using the Python script below (or ask Claude to do it):

1. Export your full game library from PBVision as JSON
2. Run the prebake script (coming soon) or rebuild via Claude
3. Replace `data/games.json` in this repo and commit

> Games imported via **+ Add Games** in the browser are saved to your local browser storage and merged with the repo data on load — they're not shared with other users.

## Deployment

Hosted via [GitHub Pages](https://pages.github.com) — no build step, no server.

On push to `main`, GitHub Pages redeploys automatically within ~60 seconds.

## Privacy

The app fetches `data/games.json` from this repo (same domain). No data is sent anywhere. `localStorage` is used only to cache user-imported games on their own device.
