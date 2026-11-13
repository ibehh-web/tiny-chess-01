# Tiny Chess — make.fun tiny-chess-01

A chess engine in at most 4,096 bytes of Python, built for the
[make.fun](https://make.fun) bounty "Build the strongest chess engine in
4 KB of Python" (tiny-chess-01, $500, deadline 2026-11-24).

`main.py` is the whole engine: 0x88 board, alpha-beta with transposition
table, MVV-LVA + killer move ordering, null-move pruning, LMR, quiescence
(captures, promotions and check evasions), tapered king piece-square
tables, history heuristic, and repetition contempt: avoid a draw when
ahead (+40cp or more), seek one when behind (-40cp or more). It plays
the house gauntlet through the env at `MAKEFUN_ENV_URL`.

Local practice Elo (v5): mean 1321 — trial-0 1326, trial-1 1464,
trial-2 1173 (above the 1154 floor). v6 adds the repetition contempt
to fix trial-2's draws against weaker anchors.

License: MIT.
