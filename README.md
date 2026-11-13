# Tiny Chess — make.fun tiny-chess-01

A chess engine in at most 4,096 bytes of Python, built for the
[make.fun](https://make.fun) bounty "Build the strongest chess engine in
4 KB of Python" (tiny-chess-01, $500, deadline 2026-11-24).

`main.py` is the whole engine: 0x88 board, alpha-beta with transposition
table, MVV-LVA + killer move ordering, null-move pruning, LMR, quiescence
(captures, promotions and check evasions), tapered king piece-square
tables. It plays the house gauntlet through the env at `MAKEFUN_ENV_URL`.

License: MIT.
