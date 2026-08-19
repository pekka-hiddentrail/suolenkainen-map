# Coordinate Map

Durable coordinate and physical-placement reference for Suolenkainen's Map.

## Current Occupied Coordinates

| Tile | Name | Coordinate | Physical placement |
| --- | --- | --- | --- |
| T001 | AIKA | [0,0] | Origin tile |
| T002 | Ring | [1,0] | NE of T001; touches T001 on T002 SW / T001 NE edge |
| T003 | The Canyon | [1,-1] | North of T001 and NW of T002; touches T001 on T003 S / T001 N edge and T002 on T003 SE / T002 NW edge |
| T004 | Mirror | [-1,0] | Touches T001 directly on T004's NE / T001's SW edge. Corrected from an originally-recorded [-1,-1] (see Notes below) — the real walk-back reaches map contact one step earlier than the tick-by-tick coordinate math suggested |
| T005 | The Monster | [-1,-1] | Touches T004 directly on T005's SE / T004's NW edge. Raw Awakening target was already adjacent to T004 despite being empty, so no walk-back steps were needed (see Notes below). Also touches T006/Shoreline on T005's NE / T006's SW edge — not recognized until after S006's Chronicle (see T006's own entry) |
| T006 | Shoreline | [0,-1] | Touches four existing tiles at once: T001's NW / T006's SE edge, T003's SW / T006's NE edge, T004's N / T006's S edge, and T005's NE / T006's SW edge. Raw Awakening target was already adjacent to all four despite being empty, so no walk-back steps were needed — the first time an already-touching raw target has touched more than one tile (see Notes below). The T005 relation was missed during S006's own Awakening (only T001/T003/T004 were checked) and found afterward while verifying a corrected `map-diagram.md`; see `../tracking/open-obligations.md` for the resulting Contagious-bleed debt. |
| T007 | Mesa | [2,-2] | Touches only T003, on T007's S / T003's N edge. Reached via a real walk-back (opposite-sign diagonal: two SE steps to the diagonal, one S step to contact) rather than an already-touching landing. Sits due north of T003 by the same pure-N relationship T003 has to T001, twice over — using `map-diagram.md`'s verified formula, T007 is 12 rows above and 0 columns offset from T001, the same "no horizontal shift" pattern as T003. |

## Coordinate Step To Physical Edge

This mapping is inferred from the confirmed placements of T001, T002, and T003.

| Coordinate step | Physical direction |
| --- | --- |
| [1,-1] | N |
| [1,0] | NE |
| [0,1] | SE |
| [-1,1] | S |
| [-1,0] | SW |
| [0,-1] | NW |

## Notes

- Keep this file synchronized with `tile-data.md` and `map-diagram.md` whenever Awakening creates, targets, or repositions a tile.
- When a calculated walk-back result touches or lands on an existing coordinate, check this table before deciding whether the coordinate is adjacent.
- S004 adopted ruling: if Brown even requires a new tile but walk-back reaches an occupied coordinate, the new tile appears at the last free coordinate before the occupied coordinate.
- Same-sign-diagonal correction: a raw target like [-4,-4] (both coordinates negative) sits on the same-sign diagonal, where there is no direct E/W hex step — walking it back means alternating NE/SE (or SW/NW) real steps, not ticking both coordinates at once. Re-walking T004's S004 target this way reaches map contact at [-1,0], one step before the originally-recorded [-1,-1] (which was never actually touching a tile). A same-sign-diagonal tie between a north-side and south-side contact point is broken by the black card: odd north-bound, even south-bound. T004's Black 6 (even) resolved south-bound to [-1,0]. Full reasoning is in `../rules/rules-delta.md`.
- Already-touching raw target: if a raw calculated coordinate is empty but already adjacent to an existing tile before any walk-back step, no stepping is needed at all — go straight to the Brown-parity decision. T005's S005 raw target [-1,-1] was already T004's NW neighbor despite being empty, so it became the contact coordinate directly. See `../rules/map-creation-rules.md`'s walk-back section.
- T006's S006 raw target [0,-1] extended this further: it was already adjacent to four existing tiles at once (T001, T003, T004, and T005), not just one — though only three were actually checked and recognized during S006's own Awakening. The rule doesn't care how many tiles an already-touching target touches, only that it touches at least one, so the same skip-straight-to-Brown-parity handling applied without needing any new ruling. The missed T005 relation was found afterward while verifying a corrected `map-diagram.md` against all placed tiles — a reminder to check a raw target against every occupied coordinate, not just the ones a first pass happens to notice.
