I'll get the project ready for GitHub — first let me check the current state of the files (and whether the agenda + thank-you slide change from before ever landed), then write the README.
The worklog shows the agenda + Thank You slides were already completed (deck is now 13 slides) — good. I also see there's already a `README.md` in the folder and the game itself (`never_still.html`). Let me check the existing README and verify the current file states.
The current README is just a placeholder line — I'll write a proper one. Let me grab the game's full controls list so the README is accurate.
The existing README is just a placeholder line, and the deck is confirmed at 13 slides. The project is actually **two artifacts**: the game (`never_still.html`, v0.7) and the class presentation. I'll write a proper GitHub README covering both, using the game's real controls and systems.
README written. Now let me log this in the worklog.
Done — your README is ready. Quick status check first: the deck on disk is already the final **13-slide version** (with the agenda slide and Thank You page), so the repo files are current.

The README is saved at `/home/z/my-project/download/README.md`, right next to the two files it describes. Here's the full content to copy-paste into GitHub:

````markdown
# NEVER STILL

> A kinetic roguelite where **movement is your weapon**. Built to fit inside a Pomodoro break.

**NEVER STILL** is a single-file browser game: standing still will kill you. Your movement speed sets a multiplier on everything you do — damage, healing, survival — across five tiers (V0–V5, ×0.5 to ×4.5). Runs last about ten minutes, weapons fire automatically, and all your attention goes to one thing: never stop moving. It began as a question — *what does a good game look like when you only have a 10-minute break?* — and turned into this.

---

## Play it

1. Download `never_still.html`
2. Open it in any modern browser (Chrome, Edge, Firefox)
3. Press **START**

No install, no build step. The first load needs internet once (Three.js comes from a CDN); after that the game itself runs fully offline.

## Controls

| Input | Action |
|---|---|
| `W` `A` `S` `D` | Move |
| `SHIFT` / `SPACE` | Dash — 9 m sine burst |
| `RMB` / `G` | Grapple — infinite, keeps momentum |
| `LMB` | Shatter Pulse — scales with speed, clears bullets |
| `E` | Overload nova when the meter is full |
| `P` | Pause |

Weapons auto-fire — **you handle the moving**.

## How a run works

- **Kinetic engine (V0–V5)** — speed tiers scale your damage ×0.5 → ×4.5. Kills heal +0.4 HP; from V3, kills burst into momentum shards.
- **The Hush** — a frozen wall advances behind you for the whole run. It never stops, and it throws lagging bosses forward. Camping is death.
- **Warlord ladder** — one boss every 2:30: **The Auditor → Koss → The Widow**.
- **5 biomes** — Verdant Ruins → Neon District → Scraplands → Sunken Canopy → Glass Sea, each with its own sky and weather.
- **10:00** — the extraction beacon opens: leave with ×1.5 ashes, or gamble in overtime for ×2 score while the Hush accelerates.
- **The Last Train** — the meta shop between runs: spend Cinders on permanent upgrades (saved in your browser).

## The class presentation

`never_still_presentation.html` is the English-class slide deck about this project — 13 slides, fully offline, nothing to install.

- Navigate with arrow keys, the on-screen buttons, or touch swipe
- The orange links on slides 8–10 open full-screen detail cards (press `Esc` to close)

## Project files

| File | What it is |
|---|---|
| `never_still.html` | The game — single file, Three.js r160 |
| `never_still_presentation.html` | Class presentation — single file, zero dependencies |
| `never_still_speech_script.docx` | Speaker notes for presenting the deck (optional) |

## Tech

- Vanilla JavaScript, one HTML file, no build step
- Three.js r160 via CDN import map, with bloom + a custom chromatic-aberration / film-grain / vignette pass whose intensity is driven by player speed
- ~500 entities at 60 fps using instanced rendering and a spatial hash
- Run progress and meta upgrades persisted in `localStorage`

## Author

**Ayoub Touihri** — ING-3-F
````

