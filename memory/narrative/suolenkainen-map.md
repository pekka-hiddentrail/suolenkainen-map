# Suolenkainen's Map

Lightweight continuity file for map coordinates, tile IDs, and session state.

## Coordinate System

- Origin tile: T001 at [0,0]
- NE-SW axis: Green minus Blue
- SE-NW axis: Red minus Yellow
- Hex sides, counting clockwise from the top: N, NE, SE, S, SW, NW
- Keep the coordinate-to-physical-direction mapping explicit in the log whenever a target is calculated or adjusted.

Current tile index and occupied-coordinate tables are tracked in `../tiles/tile-data.md` and `../tiles/coordinate-map.md`; keep those files, not this one, as the source of truth for tile/coordinate state.

## Sessions

Phase-by-phase session narrative lives one file per session in `sessions/`:

- [S001 — Breaking the Void (T001 · AIKA)](sessions/s001-breaking-the-void.md)
- [S002 — T002 · Ring](sessions/s002-ring.md)
- [S003 — T003 · The Canyon](sessions/s003-the-canyon.md)
- [S004 — T004](sessions/s004-t004.md)

Add a new file to `sessions/` for each new session rather than appending here.
