# S005 — T005 · The Monster

## Awakening

Starting tile:

- T004 / Mirror at [-1,0] — the last tile targeted (S004).
- Current occupied coordinates before S005: T001 / AIKA at [0,0], T002 / Ring at [1,0], T003 / The Canyon at [1,-1], T004 / Mirror at [-1,0].

Drawn cards:

- C170, Knight: Green 5, Blue 5, Red 2.
- C113, Leaves: Yellow 3, Brown 6, Black 4.

Target calculation:

- NE-SW shift = Green 5 - Blue 5 = 0.
- SE-NW shift = Red 2 - Yellow 3 = -1.
- From T004 [-1,0], the raw calculated target coordinate is [-1,-1].

Adjustment:

- Raw target [-1,-1] is empty. Per `coordinate-map.md`, [0,-1] is the NW step, so [-1,-1] = T004's [-1,0] + one NW step — the raw target is already the NW neighbor of T004, i.e. already touching the existing map, despite being unoccupied.
- **Rules gap found and resolved:** every prior walk-back (S002-S004) only ever needed to handle a raw target that started out isolated from the map. The written walk-back procedure ("identify nearest reference line, step toward it, check touch") never explicitly covers a raw target that is empty but already adjacent to the map before any step is taken. Two readings were possible: (a) already-touching counts as reached contact, skip stepping, go straight to the Brown-parity decision; or (b) follow the literal mechanism anyway, which would force a first step along the same-sign diagonal (since [-1,-1] sits exactly on it), tying between an NE-first path to [0,-1] and an SE-first path landing back on occupied T004 itself — Black 4 (even) would resolve that tie south-bound, turning S005 into a straight revisit of last session's own tile.
- User decision: reading (a) is adopted — the walk-back's stated purpose is to reach the map, and [-1,-1] already does. This is now folded directly into `../../rules/map-creation-rules.md`'s walk-back section.
- Brown 6 is even, so a new tile is required. [-1,-1] is itself empty, so it becomes the final target directly (no occupied coordinate was reached).

Final target:

- Final target coordinate: [-1,-1].
- Target tile: T005, new tile.
- [-1,-1] touches T004 / Mirror at [-1,0] directly: T005's SE edge / T004's NW edge (per `coordinate-map.md`'s [0,-1] = NW mapping).
- No other existing tile is adjacent to [-1,-1] (checked against T001 [0,0], T002 [1,0], T003 [1,-1] using the six neighbor offsets — none match).

Awakening notice: Brown rolled 6, a color-6 pressure (per the S003 precedent of flagging these even when the tile that drew them isn't the one a return condition names). This triggers `../../tracking/map-todo.md`'s Triggered Todo to review the S003 T003/T001 two-way bleed — reviewed and closed there: T005 doesn't touch T001 or T003, so the existing bleed record is unaffected.

## Cartography

Target: new tile T005 at [-1,-1].

Results:

- Origin / Green 5: Contagious. "It carries a force that may later bleed outward." Every time a neighboring tile is changed, T005 bleeds something random to it.
- Tether / Blue 5: Tidebound. "The tile is bound to another moving condition: coastline, bleed, region, route, stack, card result, or neighboring tile state." Narrative only — no mechanical effect.
- Entanglement / Red 2: Route-Tangled. "The tile is entangled with movement: road, river, coast, path, current, procession, or drift-line." A road/river/coast/current this tile belongs to must be named; anything that triggers for another tile on that route triggers for T005 too, even without adjacency.
- Temper / Yellow 3: Hungry. "It wants to pull, consume, spread, absorb, or demand more." Once, T005 may copy one Effect already active on an adjacent tile onto itself.
- Office / Brown 6: Office Matrix, read using the other card's numbers (Green 5, Blue 5, Red 2): Proclaim + By Mark + Boundary Cost. T005 exists to announce, name, warn, signal, shine, attract, or reveal, and performs that job by mark — symbol, name, label, sign, number, wound, note, icon, or visible marker — however, something must be cut, bordered, separated, framed, or contained to pay for it. Division always needs a line drawn somewhere first.
- Inheritance / Black 4: Omen Inheritance. "It carries the current omen, sign, hue, phrase, mood, or card-image pressure." T005 permanently carries this session's two Awakening cards (C170 Knight, C113 Leaves) as its governing omen.

Map-object instruction:

T005 is a contagious, tidebound, route-tangled, hungry proclaiming tile, born directly adjacent to T004 rather than through a long walk-back. Its Office is unusually loaded: it exists to announce or mark something, but that job is paid for with a boundary/division cost — so whatever T005 proclaims, it can't do so without also drawing a line somewhere. Its governing omen (Knight, Leaves) is now permanently fixed by Inheritance.

Obligations for later phases:

- Contagious Origin means later work on a neighboring tile can trigger a random bleed from T005 outward — a mechanism to keep available, even if unused yet.
- Route-Tangled Entanglement requires naming a road/river/coast/current T005 belongs to.
- Hungry Temper's one-time copy-effect is available but unspent.
- Office (Proclaim/By Mark/Boundary Cost) requires an eventual mark that announces something, paid for with a boundary/division line.
- Inheritance fixes C170 Knight and C113 Leaves as T005's permanent governing omen.

Loggable note:

S005 Cartography births T005 as a contagious, tidebound, route-tangled, hungry tile whose Office is Proclaim, paid for with a Boundary Cost, and whose omen is permanently fixed to the Knight/Leaves card pair.

Post-Cartography discussion:

- Contagious in practice: this works the same way as T001's own Contagious Origin (T001 carries the identical result). The Effect fires when a tile *touching* T005 is changed — created, Surfaced, or Inscribed — at which point T005 bleeds something random onto it, matching how T001's black warning-marker bled into T002 and T003 when they were worked on. It is currently dormant: T004 finished all its work in S004, before T005 existed, so there is nothing to retroactively bleed onto. It will next fire whenever a tile touching T005 is worked on again.
- Route-Tangled resolved as coast: T004 does not hand T005 a route to continue, so rather than force one, the entangling route is read as a **coast** — one of the rule's own four named options (road/river/coast/current) — on one of T005's non-T004 edges. Which edge, and what the coast concretely is, stays open (see the monster reading below).
- Hungry status: confirmed **unspent**. Copying is only available from Effects T004 actually has standing right now (its Tether and Inheritance results were both Matrix rolls, narrative-only, so only Cartography's other four apply): Drawn-In, Neighbor-Tangled, Divided, or Gate. No copy has been made; T005 remains Hungry.
- Office phrasing confirmed: "Tile exists to announce, name, warn, signal, shine, attract, or reveal. It performs that job through symbol, name, label, sign, number, wound, note, icon, or visible marker, however, something must be cut, bordered, separated, framed, or contained to pay for it. Division always needs a line drawn somewhere first." — same content as the Function+Method+Cost passage above, restated in one connected sentence.

Working creative direction (thematic, not yet locked into Surface/Inscription):

- Omen (Knight + Leaves) read as a castle/bastion in a wooded area — military presence among trees.
- The Route-Tangled coast is reimagined not as plain shoreline but as a toothed, monstrous coastline — a creature whose body forms T005's entangling edge; the individual teeth may be named.
- Contagious's "bleeds something random to a changed neighbor" is read as that monster's own reach or bite extending onto whatever tile gets worked next to T005, rather than an abstract material bleed.
- Office's Boundary Cost becomes the fortification (wall/line) the bastion must hold to pay for its Proclaim/By Mark announcement — the line drawn to keep the monster's teeth back.
- The knights/bastion (Omen) are read as the defenders paying that Boundary Cost, fighting the coastline's teeth back.
- Hungry remaining unspent is read as a standing warning: the tile hasn't "bitten" yet — whichever T004 Effect it eventually copies is the moment that changes.
- Tidebound (narrative-only) sits outside this reading as pure atmosphere; nothing else forces it to resolve.
- Open/undecided: which edge of T005 is the coast, what the teeth are named, and whether/when the Hungry copy is spent.

## Attunement

Numbers reused from Awakening: Green 5, Blue 5, Red 2 (C170, Knight); Yellow 3, Brown 6, Black 4 (C113, Leaves). Fixed color mapping: Green = Echo, Blue = Matter, Red = Mirror, Yellow = Omen, Brown = Pressure, Black = Provision.

Results:

- Echo / Green 5: Trace. Choose one old mark, buried element, retired state, or palimpsest trace that must remain influential.
- Matter / Blue 5: Acquire. Order, acquire, wishlist, or deliberately seek one interesting material/tool for future sessions.
- Mirror / Red 2: Old Mirror. Find one older tile, scan, photo, or layer that T005 should echo or resist.
- Omen / Yellow 3: Question. If the card/sign is unfinished, choose one unfinished part as a question T005 may answer.
- Pressure / Brown 6: Pressure Matrix, read using the other card's numbers (Green 5, Blue 5, Red 2): Weight + Depth + Sharpen. Something is too heavy, central, fixed, or controlling, seated in a layer, stack, buried state, or hidden structure — later work must sharpen it: make it clearer, stronger, more deliberate, more visible.
- Provision / Black 4: Token. Create one pending token, card, note, or marker for an unresolved effect.

Interpreting the open results — user decisions (supersede the earlier proposals above):

- Echo/Trace: the old, buried mark is a **ruined wall** — the bastion itself, read as already-ruined rather than intact. This is what must remain influential on T005, not the T001/T004 archaic-symbol layer originally proposed.
- Matter/Acquire: **acrylic paints**, currently on order/incoming. Once they arrive, using them becomes an obligation — a "must" — for at least one future session, not merely kept in reserve unused.
- Mirror/Old Mirror: **T002 / Ring**, not T004. T005 echoes T002's specific technique of embedding a real physical 3D object directly onto the tile surface (T002's plastic ring) and its ancient-void-relic lore, but trades the ring for a wall shape — another Ancient structure, this time a fortification rather than an arena relic.
- Omen/Question: the unfinished part is physically real, not invented — **C113 (Leaves) has an unfinished face on its card art.** The open question: does T005's own work eventually cause that face to *conform* — complete or take shape — to match the tile, rather than the tile answering to the card? Left genuinely unresolved.
- Pressure Matrix (Weight + Depth + Sharpen): the ruined wall doubles as both **Weight** (the heavy, controlling mass) and the **old mark/Depth** reading (already buried, aged, layered) in one physical object — the same wall serves both. **Sharpen** requires visible, deliberate high-contrast passages between the wall and the surrounding nature — stone against growth, not a soft blend.
- General decision: the tile must be **substantially covered in greenery** — this is the "surrounding nature" the wall needs to cut against for Sharpen to read, and it ties directly to the Leaves card and the wooded-bastion theme.

Story of Attunement:

1. Echo: A ruined wall — the bastion itself, already fallen — carries forward as T005's old, buried mark, the thing that must remain influential under whatever else gets built around it.
2. Matter: Acrylic paints are arriving; once they do, using them becomes a standing obligation to spend at least once in a future session, not just a reserve kept on hand.
3. Mirror: T005 echoes T002's real embedded 3D object and ancient-relic lore, but trades the ring for a wall — another Ancient structure, this time a fortification rather than a Court-arena relic.
4. Omen: The Leaves card's own unfinished face becomes the open question — whether T005's work will eventually make that face conform to the tile, rather than the tile answering to the card.
5. Pressure: The ruined wall is at once T005's Weight and its old buried mark, and it must stand in sharp, deliberate contrast against the greenery growing around it.
6. Provision: One pending token, marker, or note for an unresolved effect — a named tooth of the coastline, or the still-unspent Hungry copy — remains prepared and set aside before Surface begins.

Attunement todo list (session-scoped prep, not the persistent queue):

- Track the incoming acrylic paints as the acquired Matter; once they arrive, using them at least once in a future session becomes a real obligation — worth promoting to a Chronicle-level future obligation once acquired, not just left in this session's notes.
- Plan a real 3D wall-shaped object to embed into T005's physical surface, echoing T002's plastic-ring technique and Ancient-relic lore.
- Plan substantial greenery coverage across the tile, sharp-contrasted against the ruined wall.
- Leave the Leaves-card unfinished-face question open; do not resolve whether the tile conforms the card yet.
- Decide which edge of T005 carries the coast/monster, and whether any teeth get individual names (carried over from Cartography discussion, still open).
- Prepare one pending token/marker for an unresolved effect — a named tooth, or the unspent Hungry copy — to be spent later.

## Surface

Numbers reused from Awakening: Green 5, Blue 5, Red 2 (C170, Knight); Yellow 3, Brown 6, Black 4 (C113, Leaves). Fixed color mapping: Green = Ground, Blue = Substance, Red = Application, Yellow = Treatment, Brown = Structure, Black = Opening.

Results:

- Ground / Green 5: Weighted. Let the foundation feel heavy, dense, built-up, compressed, darkened, or charged.
- Substance / Blue 5: Strange. Choose something unexpected, found, artificial, excessive, awkward, or not normally map-material.
- Application / Red 2: Sparingly. Apply it in small amounts, fragments, hints, partial marks, or minimal touches.
- Treatment / Yellow 3: Contrasted. Use opposition: light/dark, warm/cool, clean/dirty, blank/marked, old/new.
- Structure / Brown 6: Structure Matrix, read using the other card's numbers (Green 5, Blue 5, Red 2): Shape + Repetition + Misaligned. An overall geometric form organizes the foundation instead of coordinate/neighbor/route/region/hidden-source; that form is built from repeated units or motifs; the flaw is that those repeated units sit offset, out of register, or wrongly connected. Newly interpreted this session and folded into `../../rules/map-creation-rules.md`'s Structure Matrix (previously TBD).
- Opening / Black 4: Breach. Create or imply a cut, tear, gap, rupture, void, window, or broken continuity.

First Mark: placed, per the user, somewhere within this session's work — exact spot not separately logged.

Actual Surface materials and layout:

- A bland greenish paper base covers the tile.
- Card C113 (Leaves) was loosely taped on top of that base.
- Several stacks of cards were taped down to form mounds — the ruined ancient-wall/bastion structure (Attunement's Echo/Trace and Mirror echo of T002's embedded-object technique). The walls are physically present as real 3D objects, matching T002's plastic-ring precedent, but end up buried under later layers rather than left exposed.
- Greenery was glued over the entire tile, including over the top of C113 and the wall mounds — fulfilling Attunement's "substantially covered in greenery" decision.
- Fiery triangle shapes were glued onto T005's SE edge (touching T004) and S edge (open, no neighbor yet), portraying hunger. Confirmed: this is atmosphere only — T005's one-time Hungry copy-effect remains unspent, and neither edge is thereby decided as the Route-Tangled coast. That naming stays fully open for a later phase (likely Inscription).
- Finally, card C113 was physically cut out of the tile, leaving a card-shaped hole that exposes a lighter background underneath.

Mapping actual work back to the six results:

- Weighted: realized as a charged, ominous color mix — greens, browns, and burning reds — rather than literal material heft.
- Strange: the embedded card itself (C113) serves as the "not normally map-material" substance.
- Sparingly: applies specifically to the wall-relic — only a small number of card-stack blocks — not to the tile's overall coverage (greenery is separate and much denser).
- Contrasted: the light patch left by the card cutout stands against the darker glued-greenery patches.
- Structure (Shape + Repetition + Misaligned): the glued forest-green patches (roughly 1in/1.5in/1in squares) supply Repetition; the fire triangles supply a distinct Shape; the patches' inconsistent sizing against each other supplies the Misaligned flaw.
- Breach: physically executed as the literal cut-out hole where C113 used to be.

Open note carried to Inscription: cutting C113 out rather than leaving it to visually "conform" is a strong physical move against Attunement's open Omen/Question ("does the tile make the Leaves-card face conform to it?"). It reads as a candidate answer — the tile didn't make the face conform, it excised it, leaving light/absence instead — but this is left for Inscription to confirm or complicate rather than treated as settled here.

Obligations for Inscription:

- Decide what the card-shaped Breach hole means, and whether it resolves or deepens the Leaves-card omen question.
- Name the Route-Tangled road/river/coast/current — still fully open; the fire-triangle edges were confirmed not to settle this.
- Office (Proclaim/By Mark/Boundary Cost) still needs its actual mark and boundary line placed — not yet addressed by Surface.
- Hungry's one-time copy-effect remains unspent, available whenever it makes sense.
- Acrylic paints remain an incoming-material obligation for a future session, separate from this one.
