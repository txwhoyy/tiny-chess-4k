# tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/txwhoyy/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/txwhoyy/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in under 4 KB of Python. `main.py` is the whole engine:
a 0x88 board with incremental tapered evaluation (material +
piece-square tables), negamax alpha-beta with PVS, a transposition
table, null-move pruning, late-move reductions, MVV-LVA move ordering,
and a quiescence search over captures, promotions and check evasions.
Repetition and the fifty-move rule score 0 in search. It searches a
fixed budget of 55,000 nodes per move and never reads a clock, so a
replayed trial makes exactly the same moves. `main.py` is packed from
its readable source with the kit's `makefun compress`.

## Run it

```sh
MAKEFUN_ENV_URL=<env origin> MAKEFUN_PROMPT_FILE=/input/prompt.txt python3 -P -s main.py
```

It plays every game the env serves, one after another, then exits.

---

<sub>Entered on [make.fun](https://make.fun/?ref=1paa8b6t&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
