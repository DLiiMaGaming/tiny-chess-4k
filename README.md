[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/DLiiMaGaming/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard)
[![reward](https://make.fun/badge/tiny-chess-01/DLiiMaGaming/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01)

# Tiny Chess 4K

An original chess engine in under 4 KB of Python: negamax alpha-beta search
with principal-variation search, null-move pruning and late-move reductions
with full re-search, quiescence over captures, promotions and check evasions
(with delta pruning and futility), check extensions, a Zobrist transposition
table, killer move ordering and MVV-LVA captures, over material plus
piece-square-table evaluation (midgame and endgame king tables, bishop pair),
with repetition scored as a draw inside the search and at the root. Move
legality is checked lazily inside the search loop so no move is made twice.
Built for the make.fun
[tiny-chess-01](https://make.fun/bounty/tiny-chess-01) bounty: the strongest
chess engine that fits in 4,096 bytes of Python.

`main.py` is the whole engine (3,906 bytes). It talks to the competition env
over HTTP and plays the house gauntlet one game after another. Local
gauntlet (practice trial-0 + trial-1, 12 games): 6/12, Elo ~1,277 — trial-0
2.5/6 (Elo 1,191, above the 1,154 practice floor), trial-1 3.5/6
(Elo 1,364); wins against depth-2 and depth-3, draws against depth-4 and
nodes-100k/250k. MIT licensed.

Run it with:

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:PORT python3 main.py
```
