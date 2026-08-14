# Coordinate Map

Durable coordinate and physical-placement reference for Suolenkainen's Map.

## Current Occupied Coordinates

| Tile | Name | Coordinate | Physical placement |
| --- | --- | --- | --- |
| T001 | AIKA | [0,0] | Origin tile |
| T002 | Ring | [1,0] | NE of T001; touches T001 on T002 SW / T001 NE edge |
| T003 | The Canyon | [1,-1] | North of T001 and NW of T002; touches T001 on T003 S / T001 N edge and T002 on T003 SE / T002 NW edge |
| T004 |  | [-1,-1] | Created by S004 as the last free coordinate before occupied [0,0] during walk-back; the coordinate math puts it two steps from T001 (via empty [-1,0] or [0,-1]) and two steps from T003 (via empty [0,-1]) — it does not touch any existing tile by a single shared edge yet, which is why physical placement still needs confirmation |

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
- S004 adopted ruling: if Brown even requires a new tile but walk-back reaches an occupied coordinate, the new tile appears at the last free coordinate before the occupied coordinate. For S004, walk-back reached occupied [0,0], so T004 appears at [-1,-1].
