# Map Diagram

An ASCII drawing of the physical map, laid out by real coordinate, not just listed in a table. Coordinate math and the tile index live in `coordinate-map.md` and `tile-data.md`; this file is the visual complement — regenerate it whenever a tile is placed or repositioned.

## Current map

```
                   _____ 
                  /     \
                 /       \
           _____/ [ 1,-1] \_____ 
          /     \   T003  /     \
         /       \       /       \
   _____/ [ 0,-1] \_____/ [ 1, 0] \
  /     \   T006  /     \   T002  /
 /       \       /       \       /
/ [-1,-1] \_____/ [ 0, 0] \_____/
\  T005   /     \   T001  /
 \       /       \       /
  \_____/ [-1, 0] \_____/
        \   T004  /
         \       /
          \_____/
```

| ID | Name | Coordinate |
| --- | --- | --- |
| T001 | AIKA | [0,0] |
| T002 | Ring | [1,0] |
| T003 | The Canyon | [1,-1] |
| T004 | Mirror | [-1,0] |
| T005 | The Monster | [-1,-1] |
| T006 | Shoreline | [0,-1] |

T004 is drawn attached to this cluster now, touching T001 directly on T004's NE / T001's SW edge. Its coordinate was originally recorded as [-1,-1] — two steps from T001 and not touching anything — but that walk-back had ticked both coordinates of a same-sign diagonal at once, which isn't a real single hex step (there is no direct E/W side). Re-walking with real NE/SE steps found map contact one step earlier, at [-1,0]; see `../rules/rules-delta.md`'s same-sign-diagonal entry for the full derivation.

T005 / The Monster and T006 / Shoreline are now both drawn in, added by the user directly against the physical tiles. Checking the result against every hex's position resolved the diagram's own long-standing inconsistency: the previously-stated rule ("NE-SW axis shifts columns, SE-NW axis shifts rows, independently") was simply wrong — real hex geometry needs both axes to combine on a diagonal move. The correct formula, verified against all six placed tiles with no exceptions, is documented below. This also surfaced a fact neither the user nor Claude had checked before: **T005 and T006 are themselves neighbors** — T006 [0,-1] minus T005 [-1,-1] is exactly the NE offset [1,0], so T006 touches T005 on T006's SW edge / T005's NE edge, visible in the diagram as the shared edge between their two hexes. This wasn't caught during S006's own Awakening (which only checked T006 against T001, T003, and T004) and has a real mechanical consequence — see `../tracking/open-obligations.md`'s T005 and T006 sections for the resulting Contagious-bleed debt.

## How to draw or extend this

Each hex is a 7-line, 11-character-wide block — a coordinate line (`/ [ q, r] \`) and a label line below it (`\  T###  /`, blank when no tile is placed), the same format as `map-diagram-reference.md`:

```
       _____ 
      /     \
     /       \
    / [ q, r] \
    \  T###   /
     \       /
      \_____/
```

To place a second hex relative to a first one, convert the coordinate difference into a character offset and a line offset, then merge overlapping lines by keeping whichever character isn't blank (the two hexes are sharing an edge at that point, so both blocks agree there anyway).

Let q = the NE-SW axis value (green minus blue) and r = the SE-NW axis value (red minus yellow), both relative to the hex you're placing from. The correct, verified formula — combining both axes, since a real hex grid needs that for any diagonal move — is:

- **row offset = 3 × (r − q)** (rows count downward, so a negative offset moves up)
- **col offset = 8 × (q + r)** (a negative offset moves left)

This is the same formula as `map-diagram-reference.md`'s, since this file now uses the same 11-character-wide block. It replaces an earlier, incorrect version of this rule (from when this file used a narrower, tile-name-only block) that treated the two axes as independently controlling row and column — that version could not actually reproduce a consistent hex grid and was the source of a long-standing unresolved inconsistency. The formula above was checked against all six tiles placed as of S006 (T001–T006) with no exceptions. Per-direction shortcuts, for convenience:

| Direction | q, r | (row, col) offset |
| --- | --- | --- |
| N | +1, -1 | (-6, 0) |
| NE | +1, 0 | (-3, +8) |
| SE | 0, +1 | (+3, +8) |
| S | -1, +1 | (+6, 0) |
| SW | -1, 0 | (+3, -8) |
| NW | 0, -1 | (-3, -8) |

A tile's own six sides run N, NE, SE, S, SW, NW (per `map-creation-rules.md` Phase 1) — N and S are the only directions with zero horizontal shift; every other direction moves both row and column at once.

This same technique — small ASCII diagrams built from a repeating block, offset by a measured per-step rule, merged at the seams — isn't only for the hex map. Use it anywhere a spatial or sequential relationship is easier to show than to describe in prose (e.g. a session's phase order, a tile's edge-contact map to its neighbors).
