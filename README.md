# Cadence

Adaptive skill-learning — one move at a time.

## Running locally

No build step, no server, no dependencies.

```
git clone <repo>
open cadence/index.html   # macOS
# or: double-click index.html in your file manager
# or: use any static server: npx serve .
```

Open `index.html` directly in any modern browser. That's it.

## Your API key

Cadence uses the [Anthropic API](https://docs.anthropic.com) (Claude Haiku) to generate your next move. You supply your own key:

1. Get a key at **[console.anthropic.com](https://console.anthropic.com)**
2. On first load, paste it into the key entry screen
3. The key is held in `sessionStorage` only — it disappears when you close the tab and is never sent anywhere except directly to Anthropic's API

Each check-in makes one API call (~300 tokens). At Haiku pricing this costs well under a cent per session.

## What it does

Enter a skill → answer 3 calibration questions → get one focused move per day. Check in after each move (Done / Done easily / Took longer / Got stuck / Skipped). The plan adapts: the finish line shifts, "stuck" produces a smaller bridging step, "fast" pulls the deadline in. No streaks, no badges — just momentum.
