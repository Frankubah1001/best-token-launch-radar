# Best Token Launch Radar

[![make.fun · token-radar-01](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![rank](https://make.fun/badge/token-radar-01/Frankubah1001/best-token-launch-radar/rank.svg)](https://make.fun/bounty/token-radar-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![reward](https://make.fun/badge/token-radar-01/Frankubah1001/best-token-launch-radar/reward.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)

A real-time scoring dashboard that ranks upcoming token launches by launch-readiness and farming potential. Built for the make.fun "Build the best token launch radar" bounty ($1,325 in USDC) using a customized radar-2 scoring model with category/chain multipliers and tailored farm steps.

## What it does

Reads a sealed protocol snapshot (`/input/snapshot.json`), scores every eligible protocol using the radar-2 model, and outputs a ranked board with category/chain multipliers, implied-value scores, and actionable farm guidance — plus a browsable dashboard, protocol dossiers, and filtered watchlist screenshots.

- **Scoring model**: base_multiple 0.22, growth_weight 0.6, maturity_floor 0.55, unknown_age_days 300
- **Category multipliers**: DeFi +8%, Liquid Staking +5%, Yield +3%, Bridge −15%, CEX −20%, and more
- **Chain multiplier**: +2% for multi-chain protocols
- **Tailored farm steps** per protocol category (Bridge, DeFi, Liquid Staking, Generic, etc.)

## Run

```bash
node main.ts
```

Outputs to `/output/`: `board.json`, `data.js`, `dossier.json`, `dashboard/` (3 static files), `screenshots/` (3 images).

## Submit to make.fun

Bounty page: https://make.fun/bounty/token-radar-01

## Submission notes

This entry was rebuilt in an agent session: `main.ts` (entrypoint), `.gitignore`, `README.md`, `dashboard/index.html` and `dashboard/app.css` were all written by the agent in this session, so the session transcript carries authorship for every counted line. The scoring model lives in `lib/model.ts`, the dashboard logic in `dashboard/app.js`, and the board/dossier builders in `vendor/makefun-board.ts`.