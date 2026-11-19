# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/guytas39-sudo/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/guytas39-sudo/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A complete chess engine in 4,037 bytes of Python — `main.py` is the whole engine, standard library only, packed with the kit's `makefun compress` from a readable minified source. Inside: a 0x88 board with full legal move generation, negamax alpha-beta search with iterative deepening, PVS, null-move pruning, late-move reductions, quiescence over captures and check evasions, a transposition table, and a tapered evaluation with piece-square tables and pawn-structure terms.

It is deterministic by design: fixed node budgets (120k / 70k / 40k by game length), no wall clock, no unseeded randomness — a replayed trial makes the same moves. On the kit's local practice trial it scored 5 wins, 1 draw, 0 losses against the house gauntlet (depth-2 through nodes-500k), a practice Elo of 1809 against a final-qualification floor of 1154.

Entered in [make.fun's "strongest chess engine in 4 KB of Python" bounty](https://make.fun/bounty/tiny-chess-01).

## Run it

```sh
python3 main.py
```

The engine plays its games through the env at `MAKEFUN_ENV_URL` (POST /game, /move, /resign), as the bounty harness drives it.

---

<sub>Entered on [make.fun](https://make.fun/?ref=g2zdh0s8&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
