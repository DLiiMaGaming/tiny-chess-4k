[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/DLiiMaGaming/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard)
[![reward](https://make.fun/badge/tiny-chess-01/DLiiMaGaming/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01)

# Tiny Chess 4K

An original chess engine in under 4 KB of Python: negamax alpha-beta search with
quiescence (captures, promotions and check evasions), check extensions, a Zobrist
transposition table, aggressive late-move reductions with full re-search, killer
move ordering, MVV-LVA captures, and repetition-aware search (in-search and
game-history), over material plus piece-square-table evaluation, driven by a
fixed 60,000-node budget per move (6 s guard) so every move is deterministic.
Built for the make.fun
[tiny-chess-01](https://make.fun/bounty/tiny-chess-01) bounty: the strongest
chess engine that fits in 4,096 bytes of Python.

`main.py` is the whole engine (3,869 bytes). It talks to the competition env
over HTTP and plays the house gauntlet one game after another. Local
gauntlet (practice trial-0 + trial-1, 12 games): 6.5/12, Elo 1,321 — wins
against depth-2/3/4 and nodes-100k. MIT licensed.

Run it with:

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:PORT python3 main.py
```
