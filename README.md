# Tiny Chess

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

Built for the make.fun bounty — see https://make.fun/bounty/tiny-chess-01.
