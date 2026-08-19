# S007 — T007 · Mesa

## Awakening

Starting tile:

- T006 / Shoreline at [0,-1] — the last tile targeted (S006).
- Current occupied coordinates before S007: T001 / AIKA at [0,0], T002 / Ring at [1,0], T003 / The Canyon at [1,-1], T004 / Mirror at [-1,0], T005 / The Monster at [-1,-1], T006 / Shoreline at [0,-1].

Drawn cards:

- C109, Violent Lion: Green 4, Blue 1, Red 1.
- C131, Armoured dragon lizard: Yellow 5, Brown 6, Black 1.

Target calculation:

- NE-SW shift = Green 4 - Blue 1 = 3.
- SE-NW shift = Red 1 - Yellow 5 = -4.
- From T006 [0,-1], the raw calculated target coordinate is [3,-5].

Adjustment:

- Raw target [3,-5] is empty. Checked against every occupied coordinate (per the completeness note just added to `../../rules/map-creation-rules.md` after S006's own miss) — not adjacent to any of T001–T006. Walk-back is needed.
- Nearest reference line: comparing distances — diagonal (||y|-|x|| = |5-3| = 2), the [0,-1]-axis where x=0 (distance |x| = 3), and the axis where y=0 (distance |y| = 5). The diagonal is nearest at distance 2, no tie.
- [3,-5] sits on the opposite-sign diagonal (x positive, y negative), so each step toward and along it is a real single hex move.
- Step 1 (SE, closing the gap to the diagonal): [3,-5] → [3,-4]. Not touching any tile.
- Step 2 (SE, reaching the diagonal at |x|=|y|=3): [3,-4] → [3,-3]. Not touching any tile.
- Step 3 (S, walking the diagonal toward the origin cluster): [3,-3] → [2,-2]. Touches T003 at [1,-1] — [2,-2]'s S neighbor is exactly [1,-1]. Stop.
- Brown 6 is even, so a new tile is required. [2,-2] is itself empty (no occupied coordinate was reached along the way), so it becomes the final target directly.

Final target:

- Final target coordinate: [2,-2].
- Target tile: T007, new tile.
- [2,-2] touches T003 / The Canyon at [1,-1]: T007's S edge / T003's N edge. Checked against all six occupied coordinates — no other tile is adjacent.

Awakening notice:

- No color-6 pressures in this draw (Green 4, Blue 1, Red 1, Yellow 5, Brown 6, Black 1 — Brown 6 is the only 6, and it's already doing its ordinary job as the new-tile/existing-tile decision, not an extra pressure to flag the way a *second* 6 alongside it would be).
- T007 touches only one existing tile (T003), a return to the simpler single-neighbor case after T006's four-way (three recognized at the time, four in fact) already-touching landing.

## Cartography

Target: new tile T007 at [2,-2].

Cards reused from Awakening: C109, Violent Lion (Green 4, Blue 1, Red 1); C131, Armoured dragon lizard (Yellow 5, Brown 6, Black 1).

Results:

- Origin / Green 4: Edge-Starved. "Contact edges feed it; non-contact edges become barren/strange." Effect: when T007 is worked, edges without a connecting tile are left untouched or minimal.
- Tether / Blue 1: Anchored. "The tile is firmly bound to its coordinate. It does not drift or rotate unless another rule later moves it." Effect: T007 cannot be moved, rotated, or pulled by any other tile's Effect; any such attempt is negated.
- Entanglement / Red 1: Neighbor-Tangled. "The tile is entangled with one or more adjacent tiles." Effect: any Effect that refers to "a neighboring tile" of T007 applies to every tile physically touching it at once — moot for now, since T007 only has one neighbor (T003), but binding if it ever gains more.
- Temper / Yellow 5: Bright. "It carries attention, signal, shine, power, celebration, danger, or visibility." Effect: any narrative-only or hidden Effect on a tile touching T007 becomes active and visible the moment the two tiles make contact — see the flagged question below, since this lands directly on T003.
- Office / Brown 6: Office Matrix, read using the other card's numbers (Green 4, Blue 1, Red 1): Open + By Edge + Quiet Cost. "Open: it exists to make passage, crossing, threshold, hinge, choice, or access. It performs that job through one edge, border, seam, contact side, or boundary — however, something must be softened, reduced, hidden, or made less dominant to pay for it. The connection only holds if something else agrees to be quieter." Narrative only — no mechanical effect of its own.
- Inheritance / Black 1: Edge Inheritance. "Something from a touching or nearby edge comes with it." Effect: at Cartography, copy one tag from a touching neighbor's record onto T007's own Tags, now shared and permanent on both tiles.

Applying Temper and Inheritance now (both require an immediate concrete read, not a deferral):

- **Temper / Bright — resolved, already satisfied:** T007 touches only T003, and T003 has three narrative-only/hidden results sitting on its own record: Origin (Twist-Born), Office (Hold by Route + Boundary Cost), and Inheritance (Layer + Line + Answer). Bright's effect says contact makes these "active and visible" — **user decision: already satisfied.** T003's Inscription already gave all of this a visible body (the star-canyon grid and hidden tunnel most concretely answer Layer+Line+Answer; Twist-Born and the Office Matrix are narrative framing already present throughout T003's record). Bright's contact confirms and illuminates what's already there rather than demanding something new. No change needed to T003's own record.
- **Inheritance / Edge Inheritance — proposed tag:** "dried-river-valley", copied from T003's record (`t003-the-canyon.md`). T007 sits due north of T003 (T007's S edge / T003's N edge), and T003's own Surface/Inscription already established that its held route — a dried river valley bordered by cliffs — enters T003 specifically from the north. That's exactly where T007 now sits. Proposing T007 as the river's unbuilt source/origin point, rather than picking an arbitrary tag.

Reading the six results together: T007 is an edge-starved, anchored, neighbor-tangled tile whose one real edge (touching T003) is doing all the work — Office frames it as a quiet, passage-opening threshold, and Inheritance ties it directly to the one feature on T003 that already needed a northern source. Origin's Edge-Starved result reinforces this: since T007 only has one connecting edge, its other five edges are expected to stay barren or minimal, keeping this tile's identity concentrated entirely on its relationship with T003.

Map-object instruction:

T007 is an edge-starved, anchored, neighbor-tangled tile standing due north of T003, structurally poised to answer where The Canyon's dried river valley actually comes from. Its Bright Temper raises an open question about whether T003's own dormant narrative-only results are now forced into the light. Its Office (Open, by Edge, Quiet Cost) suggests T007 itself should stay quiet or recede so the passage/river can be the loud thing instead.

Obligations for later phases:

- T007's non-T003 edges (five of six) should stay untouched or minimal, per Edge-Starved.
- Decide whether Bright's contact effect requires any new action on T003, or is satisfied by what's already visible there.
- The river-valley connection (Edge Inheritance) obligates T007 to eventually give the dried river valley a source, origin, or headwater — not necessarily immediately, but it's now part of T007's own inherited history.
- Office's Quiet Cost is unresolved: something (on T007, or paid by T007) must become quieter for the Open/By-Edge passage to hold.

Loggable note:

S007 Cartography births T007 as an edge-starved, anchored, neighbor-tangled tile standing at T003's northern edge, inheriting T003's "dried-river-valley" tag and raising an open question about whether its Bright Temper activates anything dormant on T003.

## Attunement

Numbers reused from Awakening: Green 4, Blue 1, Red 1 (C109, Violent Lion); Yellow 5, Brown 6, Black 1 (C131, Armoured dragon lizard). Fixed color mapping: Green = Echo, Blue = Matter, Red = Mirror, Yellow = Omen, Brown = Pressure, Black = Provision.

Results:

- Echo / Green 4: Claim. Choose one region, route, grid, shape, stack, or layer system that may claim the target tile.
- Matter / Blue 1: Unused. Find or select one material that has not been used recently. It becomes available for this session.
- Mirror / Red 1: Reference. Find one visual reference for texture, shape, color, layout, or pattern.
- Omen / Yellow 5: Weather. Choose the strongest mood of the card/sign. Later work must reflect, resist, or corrupt it.
- Pressure / Brown 6: Pressure Matrix, read using the other card's numbers (Green 4, Blue 1, Red 1): Drift + Edge + Soothe. Something is disconnected, wandering, isolated, or lacking relation; seated at a border, seam, or contact edge; later work must reduce, quiet, soften, or loosen it.
- Provision / Black 1: Mark. Prepare one blank label, tag, marker, or notation piece for possible later use.

Interpreting the results — finalized:

- **Echo/Claim:** the dried-river-valley/route system itself claims T007 — a second, independent hook (alongside Cartography's own Edge Inheritance) confirming T007 belongs to that system as its source, not just a tile that happens to touch T003. **User framing:** this could be read as the civilization-origin point for the whole map — the headwater a settled world would eventually trace itself back to, even though nothing is built here yet. Worth carrying forward as a real lore direction for T007, not just a mechanical claim.
- **Matter/Unused — user decision:** actual sand, or a texture paste worked to a really rough texture. Not used recently on any other tile, and it sits naturally in T003's stony-desert register without yet committing to a specific hue.
- **Mirror/Reference — user decision:** the reference is **stone**, continuing T003's own dry, rocky register — but with an added reference to *flowing water* worked into the same surface, physically achievable with the same rough texture paste plus brush strokes that suggest movement/current across the stone rather than a separate blue wash. This merges what were two competing options (continuity vs. contrast) into one: the stone is what T007 *is*, the brushed water-motion is what it *remembers*. Matter and Mirror converge on one technique.
- **Pressure/Drift+Edge+Soothe, in plain terms:** T007 currently feels adrift — isolated, disconnected, not really belonging anywhere yet. That isolation is specifically located at the one place T007 does connect to anything: its edge with T003. Whatever happens later should calm that feeling down there — make the edge gentler, quieter, less sharp — rather than using the edge to emphasize how cut-off T007 otherwise is.
- **Omen/Weather — still open, with concrete options offered:** the strongest mood from this session's cards (Violent Lion, Armoured dragon lizard) is aggressive and armored. Physically, violence doesn't have to mean red or dramatic — it can live in *method*: torn rather than cut edges, claw-like raking through wet texture paste (a fork or comb dragged through it), forced-looking cracks rather than naturally weathered ones, sharp angular gouges, or a harsh slash of contrasting color/mark cutting across the calm stone surface. One option worth considering later (not decided now): let violence and calm occupy different edges — soothed specifically where T007 touches T003 (per Pressure), while whatever's violent shows up on the barren, Edge-Starved sides instead, rather than blending the two in one place.
- **Provision/Mark — given real purpose, not left blank-for-nothing:** the blank label isn't just a generic reserve. It's proposed as a **cornerstone marker** — physically prepared now, left blank on purpose, to be inscribed later with whichever word, mark, or color ends up representing how the violence-vs-calm question actually resolves. If T007 really is the map's civilization-origin point, a blank cornerstone waiting for its own founding inscription fits both the lore and the mechanic at once, rather than sitting unused the way past tokens have.

**Open question carried forward, explicitly not resolved here:** violence vs. calm — Omen's aggressive governing mood against Pressure's demand to soothe T007's one real connection to the map. Surface or Inscription must decide how, or whether, these coexist.

Story of Attunement:

1. Echo: the dried river valley's own route system reaches out and claims T007 as its source — possibly the civilization-origin point this whole map would one day trace itself back to.
2. Matter: actual sand, or a texture paste worked rough, becomes the tile's material — dry, stony, unused elsewhere on the map.
3. Mirror: stone is what T007 is; brushed strokes suggesting flowing water, worked into that same rough surface, are what it still remembers.
4. Omen: an aggressive, armored mood governs the tile from its own cards, sitting uneasily against everything else pulling toward quiet.
5. Pressure: T007's isolation must be soothed exactly where it touches T003 — its one real connection to the map — rather than left sharp.
6. Provision: a blank cornerstone waits, prepared now, for whichever word finally settles the violence-vs-calm question.

Attunement todo list (session-scoped prep, not the persistent queue):

- Source or prepare actual sand or a rough-textured texture paste for T007's Surface work.
- Plan the stone-plus-water-brushwork technique: rough paste as the stone register, brush strokes worked into it to suggest current or flow, not a separate wash.
- Decide, at Surface or Inscription, how violence and calm coexist — possibly by letting them occupy different edges (soothed at the T003 contact, violent at the barren Edge-Starved sides) rather than blending them.
- Prepare a physical blank cornerstone-style marker now, reserved for a later inscription once the violence-vs-calm question resolves.
- Keep the "civilization origins" framing in view for Inscription and Chronicle — it's a lore direction worth deciding whether to commit to, not yet locked in.

## Surface

Numbers reused from Awakening: Green 4, Blue 1, Red 1 (C109, Violent Lion); Yellow 5, Brown 6, Black 1 (C131, Armoured dragon lizard). Fixed color mapping: Green = Ground, Blue = Substance, Red = Application, Yellow = Treatment, Brown = Structure, Black = Opening.

Results:

- Ground / Green 4: Clouded. Let the foundation be uneven, mottled, foggy, uncertain, weathered, or shifting.
- Substance / Blue 1: Plain. Choose something ordinary, neutral, humble, background-like, or low-status.
- Application / Red 1: Evenly. Apply it calmly, broadly, smoothly, or with balanced coverage.
- Treatment / Yellow 5: Luminous. Let something glow, shine, signal, sing, sparkle, brighten, or draw attention.
- Structure / Brown 6: Structure Matrix, read using the other card's numbers (Green 4, Blue 1, Red 1): Region + Axis + Too faint. All three cells were TBD; newly interpreted this session and folded into `../../rules/map-creation-rules.md`'s Structure Matrix.
- Opening / Black 1: Closed. The foundation is whole, sealed, settled, or complete for now.

Interpreting the six results together:

- **Substance/Plain confirms Attunement's Matter choice** (sand or rough-textured paste) — an ordinary, humble, low-status material fits exactly what Edge-Starved, Quiet Cost, and Pressure's Soothe have all been asking for.
- **Application/Evenly** reinforces the same thing physically: calm, balanced, smooth coverage — not sparse, not interrupted — matching Pressure's demand to soothe rather than dramatize.
- **Ground/Clouded** — the rough paste itself should read as uneven, mottled, weathered, uncertain, which is just what a dry, worn stone surface naturally does.
- **Structure/Region + Axis + Too faint** — the foundation is organized by a single main direction (Axis), read at the scale of the larger river-valley region rather than just this one tile (Region — echoing Attunement's Echo/Claim, where the whole route system claims T007), and that axis stays understated rather than bold (Too faint). Concretely: a north-south axis running toward T007's S edge (the T003 contact) — the implied direction the dried river would still flow, even absent, kept faint rather than emphasized.
- **Mirror's water-brushwork technique lands exactly on this Axis**: brush strokes suggesting current or flow, worked into the rough paste along that same north-south line, physically fusing Structure and Mirror into one gesture instead of two separate marks.
- **Treatment/Luminous is the one result that pulls against all of the above** — instead of quiet and plain, it wants something to shine, glow, or draw attention. Proposed as the physical seed for the still-open violence-vs-calm question: one luminous, glinting accent — a bright mineral-like fleck, a metallic streak, something that catches light like a blade or a claw — worked into the otherwise calm, plain, evenly-applied stone. This doesn't resolve which side wins; it just gives the aggressive card-omen a physical foothold inside the same calm material, ready for Inscription to develop further in either direction.
- **Opening/Closed** — the foundation itself should read as whole and settled, not left with a literal gap or breach. This doesn't remove Inscription's job (the cornerstone marker and the violence-vs-calm resolution are both still open), it just means those additions land on top of a complete base rather than requiring an unfinished patch to fill.

Surface instruction:

1. Place the First Mark anchor point anywhere on the tile before any other physical work.
2. Prepare the sand or rough-textured paste (per Attunement's Matter) and apply it evenly and calmly across the whole tile — full, settled coverage, no sparse patches or gaps (Application: Evenly, Opening: Closed).
3. Let the paste's own drying/working process read as uneven, mottled, and weathered (Ground: Clouded) — this can be the material's natural behavior rather than a deliberately engineered effect.
4. While the paste is still workable, brush strokes running along a single north-south axis toward T007's S edge (facing T003) — suggesting current or flow without literal water — kept understated rather than bold (Structure: Axis + Too faint, fused with Mirror's water reference).
5. Add one luminous or glinting accent somewhere in the stone — a bright fleck, metallic streak, or reflective mark that catches light (Treatment: Luminous) — the physical seed of the violence side of the still-open question, left for Inscription to develop.
6. The blank cornerstone marker (Provision) stays off-tile for now, physically prepared but not placed — it's reserved for whenever the violence-vs-calm question actually resolves, which may happen at Inscription or later.

This leaves Inscription with real, concrete work: developing the luminous accent (toward violence, toward calm, or held in tension), and eventually inscribing the cornerstone once that's decided.

Actual Surface materials and layout:

- Texture paste spread across the whole tile — full coverage, satisfying Application: Evenly and Opening: Closed.
- A corrugated thick-cardboard mesa plateau glued into the NW corner (seeded by the First Mark anchor point), edges smoothed into the surrounding paste so the raised plateau reads as part of the same foundation rather than an applied add-on.
- The main field textured rocky/uneven (Ground: Clouded); north-south grooves dragged through the wet paste with a fork, giving Structure's Axis a real, subtle-but-present line (Too Faint) across the whole tile toward the S/T003 edge.
- A white paint base over everything, unifying the whole surface before color went on.
- Brown and tan marker work adding variation across the surface — grounding Substance's Plain directly in T003's own dry-stone register.
- Tan watercolor sprayed generally, with **emerald green** sprayed specifically into the river-groove areas — a deliberate departure from the blue suggested earlier. Emerald reads as something more alive than plain water: fertile, mossy, verdant — which fits the "civilization origins" framing even better than blue would have, since it suggests the first hint of life at the map's own headwater rather than just water-memory.
- Yellow lines added to the mesa plateau specifically — Treatment's Luminous accent landing exactly where planned, on the one smooth, elevated feature rather than across the whole rough field.

Surface is complete. The mesa/grooved-field split gives the still-open violence-vs-calm question a real physical stage (smooth and bright vs. rough and subtle) without deciding it. The cornerstone marker remains unmade and unplaced, reserved for Inscription or later. Obligations carried into Inscription: develop the yellow-lit mesa and the green river-grooves into whatever actually resolves (or deliberately doesn't resolve) violence vs. calm, and decide whether this is the session the cornerstone gets inscribed.

## Naming

Right after Surface, the user named T007 **Mesa** — for the smooth cardboard plateau built into its NW corner. Tile record and session file renamed accordingly (`t007-mesa.md`, `s007-mesa.md`); `tile-data.md`'s Tile Index and T003's own cross-reference updated to match.

## Inscription

Numbers reused from Awakening: Green 4, Blue 1, Red 1 (C109, Violent Lion); Yellow 5, Brown 6, Black 1 (C131, Armoured dragon lizard). Fixed color mapping: Green = Scale, Blue = Form, Red = Behavior, Yellow = Relation, Brown = Force, Black = Residue.

Results:

- Scale / Green 4: Edge-Reaching. It touches or approaches one or more edges.
- Form / Blue 1: Mass. Area, region, color body, terrain, atmosphere, zone, patch, field.
- Behavior / Red 1: Settle. Stabilize, complete, calm, clarify, anchor, make legible.
- Relation / Yellow 5: Source. Card image, word, Attunement, Cartography, Surface, memory, omen, archive.
- Force / Brown 6: Force Matrix, read using the other card's numbers (Green 4, Blue 1, Red 1): Route/chain + Pressure + Alter local balance. All three cells were TBD; newly interpreted this session and folded into `../../rules/map-creation-rules.md`'s Force Matrix.
- Residue / Black 1: Mark. The residue is a plain, permanent mark on the tile itself — a small trace with no larger claim than being visibly present.

**A strong, unanimous signal in this draw:** every one of the six results points toward calm rather than violence. Behavior is literally Settle ("stabilize, complete, calm, clarify, anchor"). Force's own three cells — Route/chain, Pressure, Alter local balance — describe an influence that follows the river-route toward T003 without physically crossing into it (Pressure, not Bleed), leaving no mark anywhere but locally, inside Mesa itself (Alter local balance). Residue is a small, plain, permanent Mark, nothing more. Scale (Edge-Reaching) and Form (Mass) are both modest, area-level results rather than anything dramatic. Nothing here reflects or amplifies the Violent Lion / Armoured dragon lizard mood from Attunement's Omen — the draw reads, unprompted, as a resolution toward the **resist** option Omen itself offered ("later work must reflect, resist, or corrupt it").

**Proposed reading, pending confirmation:** the violence-vs-calm question resolves toward calm. Mesa settles into being the quiet, stabilizing headwater its Office (Quiet Cost), Origin (Edge-Starved), and Pressure (Soothe) have been pointing toward all along — the aggressive card-omen is present in the tile's history (it's still the governing Omen) but actively resisted rather than expressed. Concretely: the inscription mark is a broad-area (Mass) treatment reaching toward the S/T003 edge (Edge-Reaching) — extending or deepening the existing color zones (the emerald river-grooves, the mesa's yellow) as they approach that edge, reading as the moment the tile visibly settles into its calm identity, sourced from (Relation: Source) everything already established at Attunement and Cartography rather than inventing anything new. The Residue Mark and Force's local-only trace both suggest this stays modest and self-contained — nothing crosses into T003 itself, matching the already-resolved Bright/Cartography decision that T003 needs nothing further from this tile.

**The cornerstone marker:** since the question it was reserved for now has a strongly-supported answer, this could be the session it gets inscribed — a single word or mark meaning something like "settled," "quiet," or "source," placed near the S edge as the literal marker of where the calm headwater begins. Not decided yet — flagging it as ready rather than assuming it.

Actual Inscription:

- The mesa's existing yellow lines were accentuated and reread as **roads**, not water or abstract marks.
- A few small **black squares** were added along them as **buildings** — the map's first literal architecture. Everything before now (AIKA's circuits, Ring's arena relic, the Canyon's star-routes, Mirror's hexagons, the Monster's fortification, Shoreline's hex-tide) has been geological, technical, or abstract; Mesa is the first tile to depict an actual built settlement.
- The word **"Source"** was written directly onto the tile.
- No cornerstone marker or separate token was made — a direct, deliberate choice, consistent with the user's broader wish (logged in `../../rules/rules-delta.md`) to drop the token/Provision mechanic. Provision's own Attunement result goes unfulfilled here by choice, not oversight.

This lands the six results more precisely than the wash-and-stone plan proposed above:

- **Behavior/Settle** turns out to be a direct pun neither of us called explicitly: a **settlement** literally settles. Buildings and roads are the most concrete possible reading of "stabilize, complete, calm, clarify, anchor, make legible."
- **Relation/Source + Residue/Mark** are answered by the same single gesture — the word "Source" is both the tile naming its own Relation category outright and a plain, permanent, legible mark on the tile itself, exactly as Residue specified.
- **Force's local-only trace (Route/chain + Pressure + Alter local balance)** holds: nothing physically crosses into T003. The whole settlement, its roads, and the word stay entirely on Mesa.
- **Violence vs. calm resolves cleanly toward calm** — and decisively so. Nothing violent was added anywhere, not even as a suppressed trace. The governing Omen (Violent Lion, Armoured dragon lizard) is present in the tile's history but fully unexpressed here: a clean resist, not a resist-with-residue.

Inscription is complete. Mesa is now, narratively, the first hint of civilization on the whole map — a small settlement at the literal source of the river The Canyon depends on, calm and self-contained, naming itself "Source" without needing to cross into its only neighbor.
