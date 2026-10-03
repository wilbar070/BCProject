# AGENTS.md

## Project

Reverse-engineering project for the Bad Company Hybrid Engine. Targets Xbox 360 and PS3 binaries.

## Structure

- `analysis/xbox360/` — Xbox 360 binary analysis artifacts
- `analysis/ps3/` — PS3 binary analysis artifacts
- `analysis/functions/` — recovered function signatures and data
- `analysis/structures/` — recovered structure definitions
- `analysis/matches/` — cross-references and pattern matches
- `src/` — reconstructed source code
- `include/` — reconstructed headers
- `tests/` — verification tests
- `tools/` — analysis and decompiler tooling
- `docs/` — documentation
- `CMakeLists.txt` — build configuration (CMake)

## Build

Use CMake. Run `cmake` to configure, then build the desired target. Verify compilation succeeds after any source change.

## Workflow

1. Start from evidence in `analysis/`; never invent structures, symbols, or function semantics.
2. Distinguish evidence levels: CONFIRMED (proven), PROBABLE (strong indicators), SPECULATIVE (unresolved).
3. Cross-reference Xbox 360 and PS3 analysis — related but not identical.
4. Do not modify or overwrite analysis artifacts.
5. Keep source changes localized to the task at hand.
6. Build affected targets and run focused tests after any change.
7. Report what was verified and what remains uncertain.

## Git

Never push to remote. Keep commits logically grouped. Do not rewrite history.
