# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Vincent030306/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Vincent030306/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python chess engine: alpha-beta search with quiescence, piece-square eval, fixed node budget, no clock.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

## Engine

v8: 0x88 board, negamax alpha-beta with PVS and quiescence, MVV-LVA + killer/history move ordering, Zobrist transposition table, fixed 80,000-node budget (no clock). Eval is material plus centre-weighted piece-square tables, pawn advance and passed-pawn bonuses, bishop-pair bonus, and a king term whose sign flips with the phase — centralising the king is penalised in the middlegame and bonused in the endgame (the signs were inverted before v8). A precomputed centre table makes it about 10% faster than the first version. Practice trials: 997 / 1191 / 1191 Elo.

---

<sub>Entered on [make.fun](https://make.fun/?ref=742q33yd&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
