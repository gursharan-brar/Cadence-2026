# Cadence

Adaptive skill-learning — one move at a time. Multi-screen, fully client-side, no backend.

## Running locally

No build step. No server required.

```bash
git clone https://github.com/gursharan-brar/Cadence-2026.git
cd Cadence-2026
open index.html       # macOS
xdg-open index.html   # Linux
# or just double-click index.html in your file manager
```

> **Tip:** Some browsers block `fetch` on `file://` URLs. If API calls fail, serve it locally:
> ```bash
> npx serve .        # Node.js
> python3 -m http.server 8080
> ```
> Then open `http://localhost:8080`.

## Your Anthropic API key

Cadence calls [Claude Haiku](https://docs.anthropic.com) directly from your browser. You supply your own key:

1. Get a key at **[console.anthropic.com](https://console.anthropic.com)**
2. Paste it into the key entry screen on first load
3. The key lives in `sessionStorage` only — cleared when the tab closes, never sent anywhere except directly to Anthropic

Each check-in costs roughly one Haiku API call (~300 tokens, well under $0.01).

## What it does

Enter a skill → answer 3 calibration questions → get one focused move per session. Check in after each move:

| Outcome | Effect |
|---------|--------|
| Done | Advance, same difficulty |
| Done easily | Advance, pull finish line in, difficulty up |
| Took longer | Advance, push finish line out |
| Got stuck | Advance day, but next step is **smaller and more concrete** |
| Skipped | Advance day, push finish line out, move is lightly reframed |

No streaks. No badges. Just momentum.

## Screens

- **Key entry** — paste your Anthropic key once per tab session
- **Home** — see all in-progress skills, resume any with one tap
- **Calibrate** — name a skill, set your level, hours, and goal
- **Loop** — your one move, progress bar, check-in row
- **History** — full log of every check-in with outcome badges
