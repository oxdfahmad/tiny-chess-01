# tiny-chess-01

A compact chess engine in a single 4,076-byte `main.py`, written from scratch
for the make.fun tiny-chess-01 bounty.

## Engine

- 0x88 board, alpha-beta + quiescence, transposition table, null-move pruning,
  killer moves, piece-square tables, binary-phase king eval.
- Deterministic: fixed node budget (200,000 nodes/move), no wall clock, no
  randomness. Every move derives only from the position and the game moves.
- Talks to the environment over HTTP (`POST /game`, `/move`, `/resign`) with
  UCI moves, as specified in the competition rules.

## Files

- `main.py` — the engine (4,076 bytes; lzma-compressed payload + unpacker).
- `LICENSE` — MIT.
