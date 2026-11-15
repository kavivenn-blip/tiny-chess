# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/kavivenn-blip/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/kavivenn-blip/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python chess engine for the make.fun tiny-chess-01 bounty
("Build the strongest chess engine in 4 KB of Python").

`main.py` is the whole engine: a 10x12 mailbox board rotated after every
move so the side to move is always "white", negamax with alpha-beta and
iterative deepening to a fixed node budget, quiescence on captures and
promotions, a transposition table with killer/history move ordering, and a
material + piece-square evaluation with a tapered king table, bishop-pair
bonus, and full rules (castling, en passant, underpromotion, repetition).

The engine talks to the bounty environment over HTTP (`MAKEFUN_ENV_URL`).
It is deterministic: a fixed node budget, no clock, no randomness.

## Run it

```sh
python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=hp1z0q8b&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
