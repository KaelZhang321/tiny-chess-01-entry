# tiny-chess-01-entry

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/KaelZhang321/tiny-chess-01-entry/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/KaelZhang321/tiny-chess-01-entry/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python chess engine for make.fun's "Build the strongest chess engine in 4 KB of Python" bounty.

Negamax with alpha-beta pruning, killer-move ordering, quiescence search (captures, promotions, check evasions), iterative deepening to a fixed 50,000-node budget. The source is lzma-compressed and base85-encoded into `main.py`; the unpacker and payload both count toward the 4,096-byte cap. Standard library only, deterministic (no clock, no unseeded randomness).

## Run it

```sh
python3 -P -s main.py
```

The engine talks to the env at `MAKEFUN_ENV_URL`; it plays every game of the gauntlet through `POST /game` and `POST /move`.

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
