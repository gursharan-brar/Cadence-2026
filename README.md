# Cadence

Adaptive skill-learning — one concrete move at a time. Warm editorial design, no backend, no build step.

## Running locally

```bash
git clone https://github.com/gursharan-brar/Cadence-2026.git
cd Cadence-2026
open index.html        # macOS
xdg-open index.html    # Linux
```

Or serve it to avoid any browser `file://` fetch restrictions:

```bash
npx serve .
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## Your Anthropic key

On first load you'll be asked for an Anthropic API key.

1. Get one free at **[console.anthropic.com](https://console.anthropic.com)**
2. Paste it into the key screen — it's stored in `sessionStorage` only (cleared when the tab closes)
3. All API calls go directly from your browser to Anthropic — nothing passes through a server

Model: `claude-haiku-4-5`. Each check-in is ~300 tokens, well under a cent.

## Screens

| Screen | What it is |
|--------|-----------|
| Key entry | Paste your key once per tab session |
| Home | See in-progress skills, resume any with one click |
| Calibrate | Sequential intake — skill, level, hours, goal |
| Loop | One move card, progress bar, five check-in outcomes |
| History | Full color-coded log of every check-in |

## How it adapts

| Check-in | Effect |
|----------|--------|
| Done | Advance, same difficulty |
| Done easily | Advance, pull finish line in, step up difficulty |
| Took longer | Advance, push finish line out |
| Got stuck | Advance day — next move is **smaller and more concrete** |
| Skipped | Advance day, push finish line out, move is reframed |

No streaks. No badges. Just momentum.
