[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/DLiiMaGaming/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard)
[![reward](https://make.fun/badge/tiny-chess-01/DLiiMaGaming/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01)

# Tiny Chess 4K

A chess engine in under 4 KiB: negamax with alpha-beta and PVS,
quiescence search, a transposition table, null-move pruning, LMR and
MVV-LVA ordering. Fully deterministic — a fixed 70,000-node budget per
move, Zobrist seed 42, no wall clock. It plays through the make.fun
env (`POST /game`, `/move`, `/resign`).

Run it with:

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:PORT python3 main.py
```
