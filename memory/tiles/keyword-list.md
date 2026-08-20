# Keyword List

Stable keyword index for Suolenkainen's Map. Status values:

- Active: currently binding the active tile or session.
- Omitted: drawn but not applied.
- Pending: unresolved, waiting on a later phase.
- Resolved: answered, no longer open.

## Recurrence Rule

A result earns a keyword ID only when it does real cross-referencing work — either:

- a second tile independently draws the same result (so the ID lets both tiles point at one shared entry instead of restating it twice), or
- Chronicle's Seed mechanism creates it explicitly as a future return condition (an Artifact-Draw name, a Residue keyword) — this earns its ID on creation, since it's designed to recur even before it actually does.

A one-off Cartography result that belongs to exactly one tile, isn't shared, and isn't a Seed return condition stays a plain tag on that tile's own record. The tile's own Cartography fields already hold the full detail; a separate keyword ID would only restate it without giving anyone a reason to look it up. See "Adopted Delta - Keyword Recurrence Rule" in `rules-delta.md`.

This was applied retroactively: K001, K002, K004–K006, K008–K015, K017–K023, and K026–K031 were removed as keywords under this rule. Nothing was lost — every one of them is already present as a plain tag on its own tile's record (see `tile-data.md` / `records/`). Retired IDs are not reused or renumbered, so gaps in the sequence below are expected; the next new keyword continues from K032.

| ID | Keyword | Status | Phase | Rule / meaning | Practical effect | How to read it |
| --- | --- | --- | --- | --- | --- | --- |
| K003 | Region-Tangled | Active | Cartography | Entanglement result: the tile is tangled with a larger area, territory, biome, district, color field, zone, or atmosphere. | Make the governed tile feel like one visible part of a broader region. For T002, prepare a district/zone pressure that exceeds the single tile. | Read as larger-than-one-tile pressure entering through the tile. |
| K007 | Burial Cost | Active | Cartography / Office Matrix | Office matrix cost: something must be covered, layered over, submerged, deferred, or made latent. | Something required by the tile's office must be hidden, buried, covered, or delayed. For T002, the passage created by Open by Layer must cost a covered mark, buried state, or deferred answer. | Read as the price of function: the tile may act, but something goes underneath or waits. |
| K016 | Ring | Active | Inscription / Artifact Draw | Named T002 figure and artifact keyword: the central ring/sinkhole/mountain marks the Court arena relic that existed in the void before T002 emerged. | Return to T002 when Ring, circles/ovals, arena pressure, spectator text, black warning bleed, or a relevant 6 appears. Keep Ring available as a keyword seed for later sessions. | Read as a named relic, not just a shape: Ring is a void-old arena threshold that the map uncovered. |
| K024 | Star-Canyon Grid | Active | Inscription / Residue | T003 inscription residue keyword: five yellow star-spokes/routes spread from a point in the dried valley, following canyon grids; one stray yellow route leaves the canyon wall as a hidden tunnel. | Return to T003 when yellow routes, star patterns, hidden tunnels, canyon grids, silver grid bleed, or exposed unfinished city-route pressure appears. The exposed residue must be answered next time T003 is worked on. | Read as T003's governing route behavior: a bright source spreads through a canyon grid, with one route escaping into hidden passage. |
| K025 | The Canyon | Active | Chronicle / Artifact Draw | Name and artifact keyword for T003: the dried river valley, cliff-bounded canyon grid, bright city-foundation, hidden tunnel, red-circle inheritance, and neighbor bleeds into/from T001. | Use as the stable name for T003 and its Docs/archive page. Return when The Canyon, canyon routes, cliff borders, hidden tunnel, star routes, black warning bleed, silver grid bleed, or C074/C127 pressure appears. | Read as T003's archive identity: not merely a canyon landform, but a named route-vault where warning, grid, star, and hidden passage meet. |
| K032 | Schematic Rewrite | Active | Chronicle / Seed Matrix | Seed keyword created by T004/Mirror's S004 Chronicle (Green 1: Keyword, Blue 6: Hidden archive, Red 1: May return normally): T004's Inscription rewrote some of T001's archaic symbols in T004's own schematic-hexagon pattern — a transformation, not an erasure, that doubles as preserving what T004 inherited from that edge. What the original archaic symbols meant, and what the rewrite specifically changes about that meaning, is deliberately left unexplained for now. | Return to either T001 or T004/Mirror when archaic symbols, schematic hexagons, cross-tile rewriting, or an inheritance-preservation question appears again. | Read as evidence kept deliberately incomplete: something real changed between two tiles, but why it changed is a question later work gets to answer, not one Chronicle is settling now. |
| K033 | Hex Tideline | Active | Chronicle / Seed | Seed keyword created by T006/Shoreline's S006 Chronicle (Black 1: Keyword): Shoreline's Inscription grew two deliberately misaligned hex grids — 8 black hexagons (30mm spacing) and 4 silver hexagons (24mm spacing) — out of the mismatched black-warning-bleed and silver-grid-bleed lines it inherited from T001 and T003. Neither grid is resolved as dominant; the tension between them is the point. | Return to T006/Shoreline when it is next targeted, to decide whether the black grid or the silver grid wins, or whether they remain in permanent tension. | Read as an unresolved contest given a permanent, named body: two inherited histories occupying the same tile without reconciling. |
| K034 | First Settlement | Active | Chronicle / Seed | Seed keyword created by T007/Mesa's S007 Chronicle (Black 1: Keyword): Mesa's Inscription reread its own yellow lines as roads and added black-square buildings, the map's first depiction of an actual built settlement after six tiles of purely geological, technical, or abstract imagery — resolving Mesa's violence-vs-calm tension cleanly toward calm in the same gesture. | Return when settlement, road, or building imagery appears again anywhere on the map, or when Mesa (T007) is targeted again — decide whether it expands, connects to Mesa, or remains an isolated origin point. Also carries Mesa's still-unpaid Office Quiet Cost. | Read as the map's founding civilization moment: not just a tile detail, but a marker for whenever settled, built imagery recurs elsewhere. |
| K035 | Amedda | Active | Chronicle / Seed | Seed keyword created by T001/AIKA's S008 Chronicle (Black 1: Keyword): Inscription's Form/Sign result gave T001's long-blank Provision marker an actual word — "Amedda," taken from a *Star Wars* novel and chosen with no intended meaning — placed at Dotti's NW edge, the literal crossing point toward T006/Shoreline. | Return when the name Amedda appears again anywhere on the map, or when T001 or T006 is next targeted — decide whether it ever gains an in-world meaning or stays permanently foreign. | Read as a deliberately imported, meaningless sign: a name grafted onto the tile from entirely outside its own vocabulary, left open for a later session to explain or leave unexplained. |

## Tags In Use

Add tags here as they appear. Synced against every tile record's Tags field; add new ones here whenever a record's Tags field grows.

- AIKA
- already-touching
- alter-local-balance
- Amedda
- anchor-point
- anchored
- appetite
- archaic-symbol-palimpsest
- archaic-symbols
- axis
- becomes-too-fixed
- black-circle
- black-hex-grid
- black-warning-bleed
- blank
- boundary
- boundary-cost
- bright
- bright-city-foundation
- broad
- buildings
- burial-cost
- by-edge
- by-mark
- C074-moonscape
- clean
- cliffs
- closed
- clouded
- color-6-notice
- conditional-neighbor-wander
- contagious
- contamination
- Court-arena
- dark-center
- dashed-red-circle
- defer-and-record
- dense
- diagonal-return
- diamond-shape
- divided
- division
- Dotti
- drawn-in
- dried-river-valley
- edge-inheritance
- edge-reaching
- edge-starved
- emerald-river
- emerging
- evenly
- fan-brush
- first-civilization
- flooded-coastline
- gate
- green-bleed
- green-earth
- green-felt
- hex-grid
- hidden-tunnel
- hold-by-route
- hungry
- layer-line-inheritance
- light-turquoise
- loosely-held
- luminous
- mark
- mass
- material
- Mesa
- mesa
- misaligned-grids
- mountain
- mutation
- neighbor-rule-inheritance
- neighbor-tangled
- new-tile
- north-south-tiebreak
- nowhere-many-points
- ns-grooves
- omen-inheritance
- open
- open-by-layer
- partial
- plain
- plastic-ring
- postal-consignment-list
- pressure
- proclaim
- pushing
- quiet-cost
- region
- region-tangled
- resistance
- returns
- reversed
- Ring
- roads
- roadway
- rock-giant
- rockstar-bass
- route-chain
- route-region
- route-tangled
- S003
- S004
- S006
- S007
- safety-line
- same-sign-diagonal
- settle
- settlement
- Shoreline
- show
- silver-grid-bleed
- silver-hex-grid
- sinkhole
- soft
- source
- spread-points
- sprout-scribbles
- stain
- star-canyon-grid
- stops-short
- stranger
- supernova-city
- T001-warning-bleed
- T002
- T002-red-circle-inheritance
- T003
- T004
- T006
- T006-silver-hex-bleed
- T007
- texture-paste
- The-Canyon
- thread
- tidebound
- too-faint
- twist-born
- undercity-map
- unstable
- unstable-finish
- void-relic
- walk-back
- warning-checkers
