# Coordinate Map

Durable coordinate and physical-placement reference for Suolenkainen's Map.

## Current Occupied Coordinates

| Tile | Name | Coordinate | Physical placement |
| --- | --- | --- | --- |
| T001 | AIKA | [0,0] | Origin tile |
| T002 | Ring | [1,0] | NE of T001; touches T001 on T002 SW / T001 NE edge |
| T003 | The Canyon | [1,-1] | North of T001 and NW of T002; touches T001 on T003 S / T001 N edge and T002 on T003 SE / T002 NW edge |
| T004 |  | [-1,0] | Touches T001 directly on T004's NE / T001's SW edge. Corrected from an originally-recorded [-1,-1] (see Notes below) — the real walk-back reaches map contact one step earlier than the tick-by-tick coordinate math suggested |

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
