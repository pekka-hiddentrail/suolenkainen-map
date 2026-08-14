# Hex Map Reference Grid

A reference-only ASCII grid showing every coordinate within hex radius 4 of the origin (61 cells: the origin plus rings 1–4), using axial coordinates `[q,r]` where `q` is the NE-SW axis (green minus blue) and `r` is the SE-NW axis (red minus yellow), per `coordinate-map.md`.

This is separate from `map-diagram.md`, which draws only the tiles actually placed on the physical map. This file exists purely to visualize the coordinate space itself — most cells are empty and may never be filled.

## Grid

```
                                   _____
                                  /     \
                                 /       \
                           _____/ [ 4,-4] \_____
                          /     \         /     \
                         /       \       /       \
                   _____/ [ 3,-4] \_____/ [ 4,-3] \_____
                  /     \         /     \         /     \
                 /       \       /       \       /       \
           _____/ [ 2,-4] \_____/ [ 3,-3] \_____/ [ 4,-2] \_____
          /     \         /     \         /     \         /     \
         /       \       /       \       /       \       /       \
   _____/ [ 1,-4] \_____/ [ 2,-3] \_____/ [ 3,-2] \_____/ [ 4,-1] \_____
  /     \         /     \         /     \         /     \         /     \
 /       \       /       \       /       \       /       \       /       \
/ [ 0,-4] \_____/ [ 1,-3] \_____/ [ 2,-2] \_____/ [ 3,-1] \_____/ [ 4, 0] \
\         /     \         /     \         /     \         /     \         /
 \       /       \       /       \       /       \       /       \       /
  \_____/ [ 0,-3] \_____/ [ 1,-2] \_____/ [ 2,-1] \_____/ [ 3, 0] \_____/
  /     \         /     \         /     \         /     \         /     \
 /       \       /       \       /       \       /       \       /       \
/ [-1,-3] \_____/ [ 0,-2] \_____/ [ 1,-1] \_____/ [ 2, 0] \_____/ [ 3, 1] \
\         /     \         /     \  T003   /     \         /     \         /
 \       /       \       /       \       /       \       /       \       /
  \_____/ [-1,-2] \_____/ [ 0,-1] \_____/ [ 1, 0] \_____/ [ 2, 1] \_____/
  /     \         /     \         /     \  T002   /     \         /     \
 /       \       /       \       /       \       /       \       /       \
/ [-2,-2] \_____/ [-1,-1] \_____/ [ 0, 0] \_____/ [ 1, 1] \_____/ [ 2, 2] \
\         /     \         /     \  T001   /     \         /     \         /
 \       /       \       /       \       /       \       /       \       /
  \_____/ [-2,-1] \_____/ [-1, 0] \_____/ [ 0, 1] \_____/ [ 1, 2] \_____/
  /     \         /     \  T004   /     \         /     \         /     \
 /       \       /       \       /       \       /       \       /       \
/ [-3,-1] \_____/ [-2, 0] \_____/ [-1, 1] \_____/ [ 0, 2] \_____/ [ 1, 3] \
\         /     \         /     \         /     \         /     \         /
 \       /       \       /       \       /       \       /       \       /
  \_____/ [-3, 0] \_____/ [-2, 1] \_____/ [-1, 2] \_____/ [ 0, 3] \_____/
  /     \         /     \         /     \         /     \         /     \
 /       \       /       \       /       \       /       \       /       \
/ [-4, 0] \_____/ [-3, 1] \_____/ [-2, 2] \_____/ [-1, 3] \_____/ [ 0, 4] \
\         /     \         /     \         /     \         /     \         /
 \       /       \       /       \       /       \       /       \       /
  \_____/ [-4, 1] \_____/ [-3, 2] \_____/ [-2, 3] \_____/ [-1, 4] \_____/
        \         /     \         /     \         /     \         /
         \       /       \       /       \       /       \       /
          \_____/ [-4, 2] \_____/ [-3, 3] \_____/ [-2, 4] \_____/
                \         /     \         /     \         /
                 \       /       \       /       \       /
                  \_____/ [-4, 3] \_____/ [-3, 4] \_____/
                        \         /     \         /
                         \       /       \       /
                          \_____/ [-4, 4] \_____/
                                \         /
                                 \       /
                                  \_____/
```

## Placed tiles

| ID | Name | Coordinate |
| --- | --- | --- |
| T001 | AIKA | [0,0] |
| T002 | Ring | [1,0] |
| T003 | The Canyon | [1,-1] |
| T004 |  | [-1,0] |

All 57 remaining cells show only their coordinate; none are placeholders for planned tiles. (T004 was corrected from [-1,-1] to [-1,0] during post-S004 rules maintenance — see `../rules/rules-delta.md`'s same-sign-diagonal entry.)

## How this is generated

Each hex is a 7-line, 11-character-wide block: a coordinate line (`/ [ q, r] \`) and a label line below it (`\  T###  /`, blank when no tile is placed). Numbers are right-aligned to width 2 (`-4`..` 4`) so every bracketed pair is exactly 7 characters (`[nn,nn]`) and every hex is the same size — this is a deliberate departure from the freehand sample, which used minimal-width numbers and wasn't uniform enough to tile cleanly at this scale.

Position of a hex's top-left corner, relative to the origin hex, in (row, column) character offsets:

- `row(q, r) = 3 * (r - q)`
- `col(q, r) = 8 * (q + r)`

These were derived directly from the sample by measuring the offsets between its seven hand-drawn hexes, then generalized. Adjacent hexes are merged by overwriting only non-space characters, so shared edges (slashes, underscores) always agree. The generating script is disposable — this file is the durable artifact; regenerate by re-deriving the same two formulas if the radius or coordinate range ever needs to change.

Radius 4 means every `[q,r]` where `max(|q|, |r|, |q+r|) <= 4` — i.e. up to 4 steps from the origin along any of the six directions.
