# Map Diagram

An ASCII drawing of the physical map, laid out by real coordinate, not just listed in a table. Coordinate math and the tile index live in `coordinate-map.md` and `tile-data.md`; this file is the visual complement — regenerate it whenever a tile is placed or repositioned.

## Current map

```
   ____ 
  /    \
 /      \
/  T003  \____ 
\        /    \
 \      /      \
  \____/  T002  \
  /    \        /
 /      \      /
/  T001  \____/
\        /
 \      /
  \____/
```

| ID | Name | Coordinate |
| --- | --- | --- |
| T001 | AIKA | [0,0] |
| T002 | Ring | [1,0] |
| T003 | The Canyon | [1,-1] |

T004 is not drawn attached to this cluster. Its coordinate, [-1,-1], is two steps from T001 (through either the empty [-1,0] or empty [0,-1] slot) and two steps from T003 (through the empty [0,-1] slot) — it does not touch any existing tile by a single shared edge under the coordinate math. That matches the open note in `tile-data.md` that T004's exact physical edge placement still needs confirming; draw it here once that's settled instead of guessing:

```
   ____ 
  /    \
 /      \
/  T004  \
\        /
 \      /
  \____/
```

## How to draw or extend this

Each hex is the same 7-line block, with a 6-character-wide label slot (pad shorter labels with spaces on both sides so they stay 6 characters — a 4-character tile ID like `T001` becomes `  T001  ` inside the slot):

```
   ____ 
  /    \
 /      \
/  LABEL \
\        /
 \      /
  \____/
```

To place a second hex relative to a first one, convert the coordinate difference into a character offset and a line offset, then merge overlapping lines by keeping whichever character isn't blank (the two hexes are sharing an edge at that point, so both blocks agree there anyway):

- Every +1 on the NE-SW axis (green minus blue) shifts the block **7 characters right**; -1 shifts left.
- Every +1 on the SE-NW axis (red minus yellow) shifts the block **3 lines up**; -1 shifts down.
- A tile's own six sides run N, NE, SE, S, SW, NW (per `map-creation-rules-v1.md` Phase 1) — N/S neighbors share a flat top/bottom edge with no horizontal shift at all, just a 6-line vertical offset (2 axis-steps); NE/SE/SW/NW neighbors shift diagonally using both offsets above.

These two constants (7 characters, 3 lines) were measured directly off a real 3-hex cluster, not guessed — if you add a hex and the seams don't line up, recheck the coordinate difference before assuming the constants are wrong.

This same technique — small ASCII diagrams built from a repeating block, offset by a measured per-step rule, merged at the seams — isn't only for the hex map. Use it anywhere a spatial or sequential relationship is easier to show than to describe in prose (e.g. a session's phase order, a tile's edge-contact map to its neighbors).
