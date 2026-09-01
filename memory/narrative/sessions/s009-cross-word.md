# S009 — T008 · Cross-word

## Awakening

Starting tile:

- T001 / AIKA at [0,0] — the last tile targeted (S008).
- Current occupied coordinates before S009: T001 / AIKA at [0,0], T002 / Ring at [1,0], T003 / The Canyon at [1,-1], T004 / Mirror at [-1,0], T005 / The Monster at [-1,-1], T006 / Shoreline at [0,-1], T007 / Mesa at [2,-2].

Drawn cards:

- C052, Water energy: Green 2, Blue 3, Red 4.
- C130: Yellow 3, Brown 4, Black 1.

Target calculation:

- NE-SW shift = Green 2 - Blue 3 = -1.
- SE-NW shift = Red 4 - Yellow 3 = 1.
- From T001 [0,0], the raw calculated target coordinate is [-1,1].

Adjustment:

- Raw target [-1,1] is empty. Checked against every occupied coordinate:
  - [-1,1]'s N neighbor ([-1,1] + [1,-1]) is [0,0] = T001.
  - [-1,1]'s NW neighbor ([-1,1] + [0,-1]) is [-1,0] = T004.
  - No other occupied coordinate is adjacent to [-1,1].
- The raw target already touches the map — to two tiles at once, T001 and T004 — before any walk-back step. Per the already-touching rule, skip stepping and go straight to the Brown-parity decision.
- Brown is 4, even. Per the established rule (every prior even-Brown already-touching landing — S005, S006, S007 — created a new tile on the spot), a new tile is created directly at [-1,1]. This session doesn't hit S008's odd-Brown exception.

Final target:

- Final target coordinate: [-1,1].
- Target tile: **T008 — a new tile**, touching T001 on T008's N / T001's S edge, and T004 on T008's NW / T004's SE edge.

Awakening notice:

- No color-6 pressures in this draw (Green 2, Blue 3, Red 4, Yellow 3, Brown 4, Black 1 — no 6 appears at all).
- T008's arrival on T001's S edge is notable: that is exactly the edge Dotti's corridor (built in S008) reaches but has no neighbor to bleed into yet — Dotti runs along T001's S, SW, and NW edges, and only the SW (T004) and NW (T006) portions have so far reached an actual neighbor. T008 is the first tile positioned to answer Dotti's still-unanswered S edge.
- T008 also touches T004 on T004's SE edge — a new relation, distinct from T004's existing NE/T001, N/T006, and NW/T005 edges.

## Cartography

Target: new tile T008. Phase 2.1 (New-Tile Cartography, the character-sheet model).

Cards reused from Awakening: C052, Water energy (Green 2, Blue 3, Red 4); C130 (Yellow 3, Brown 4, Black 1). Fixed color mapping: Green = Origin, Blue = Tether, Red = Entanglement, Yellow = Temper, Brown = Office, Black = Inheritance.

Results:

- Origin / Green 2: Void-Born. It resists surroundings and behaves separately.
- Tether / Blue 3: Reversed. Rotate 180°, or invert the expected relation.
- Entanglement / Red 4: Grid-Tangled. The tile is entangled with structure: grid, coordinates, repetition, measurement, lattice, or constructed order.
- Temper / Yellow 3: Hungry. It wants to pull, consume, spread, absorb, or demand more.
- Office / Brown 4: Gate. Tile must become a threshold, crossing, hinge, pass, bridge, or decision point.
- Inheritance / Black 1: Edge Inheritance. Something from a touching or nearby edge comes with it.

Grounding each result in T008's actual position:

- **Tether/Reversed, applied immediately:** per its Effect, T008's own compass directions flip at birth — North swaps with South, NE with SW, SE with NW. T008 physically touches T001 on the edge that would ordinarily be called North, and T004 on the edge that would ordinarily be called Northwest. After Reversed, any later rule referring to T008's own edges by direction uses the opposite: **T001 is recorded as being on T008's S edge, and T004 on T008's SE edge** — not their pre-flip labels. This is only about how T008's own edges are *named* going forward; the physical map layout and every other tile's own direction-naming are unaffected.
- **Office/Gate, named directly:** T008 stands as a threshold between **T001 and T004** — its only two neighbors. This echoes T006's own Gate role (standing between T001 and T003): the map now has two Gates, each mediating a different pair meeting at T001.
- **Inheritance/Edge Inheritance, tag chosen:** T008 copies the tag **"dotti"** from T001's record. This is the most concrete option available — T008 sits exactly on the Dotti corridor's still-unanswered S edge (flagged at Awakening), so inheriting that tag directly ties T008's birth to the one open thread it's actually positioned to answer.
- **Entanglement/Grid-Tangled:** T008's coordinate [-1,1] becomes a fixed reference point — any later rule counting distance, steps, or direction (a walk-back, a bleed's reach, a Black-number direction count) may be measured from T008 instead of from whatever tile it would otherwise use. A standing capability, not something that needs to be exercised this session.
- **Temper/Hungry:** once, T008 may copy one Effect already active on an adjacent tile (T001 or T004) onto itself, without removing it from the original. Unspent for now — available whenever a specific Effect makes sense to duplicate.
- **Origin/Void-Born, the tile's central tension:** Void-Born resists its surroundings and behaves separately — if T008 ever moved, it would be unaffected by any other tile. That sits in direct tension with everything else this draw produced: Grid-Tangled ties it into the coordinate system, Edge Inheritance ties it to T001's Dotti tag, and Gate exists specifically to mediate between two neighbors. T008 is a tile whose birth insists it stands apart, immediately surrounded by mechanisms that tie it in. This tension is the tile's identity, not a contradiction to resolve away.

Interpretation: T008 arrives exactly where Dotti's still-unanswered S edge meets a new tile — and inherits Dotti's own tag as its birthright. But its Tether flips its own sense of direction at the moment of birth, and its Origin insists it resists entanglement even as its Office makes it a hinge between the two tiles touching it. A tile born reversed, gated, and hungry, carrying one inherited tag, while narratively refusing to belong to either side.

Obligations for later phases:

- Attunement and Surface must engage with T008's inherited "dotti" tag — this is the tile's actual answer to Dotti's open S edge, not a coincidence to leave unaddressed.
- Gate's naming (T001 and T004) should be reflected physically at some point — a crossing, hinge, or threshold feature, echoing but not duplicating T006's own Gate treatment.
- Reversed's direction-flip must be used consistently from here on: T008's own S edge = the T001 contact, T008's own SE edge = the T004 contact.
- Hungry's one-time copy effect and Grid-Tangled's reference-point capability remain unspent, standing options for future phases or sessions.

Loggable note:

S009 Cartography births T008 as a Void-Born, Reversed, Grid-Tangled, Hungry tile with a Gate office standing between T001 and T004, inheriting T001's own "dotti" tag on its birth edge — the first tile positioned to answer Dotti's still-open S edge, even as its own Origin insists it stands apart from both neighbors touching it.

## Attunement

Numbers reused from Awakening: Green 2, Blue 3, Red 4 (C052, Water energy); Yellow 3, Brown 4, Black 1 (C130, Robot details). Fixed color mapping: Green = Echo, Blue = Matter, Red = Mirror, Yellow = Omen, Brown = Pressure, Black = Provision.

Results:

- Echo / Green 2: Continuation. Choose one existing line, road, border, river, grid, or pattern that may continue into the target tile.
- Matter / Blue 3: Family. Select one material family for the session.
- Mirror / Red 4: Phrase. Find one written note, phrase, title, or old prompt that may guide the session indirectly.
- Omen / Yellow 3: Question. If the card/sign is unfinished, choose one unfinished part as a question the tile may answer.
- Pressure / Brown 4: Conflict. Identify one conflict in the tile's current situation. Later work must answer it.
- Provision / Black 1: Mark. Prepare one blank label, tag, marker, or notation piece for possible later use.

Interpreting the results:

- **Echo/Continuation:** the existing line chosen is T004's own frayed fabric zone — specifically its permanently-unsealed edge, a binding restriction created by T004's own Substance Matrix result (Fragile/Precise/Create a rule-or-debt) back in S004. T004's frayed zone sits on the side opposite its T001-facing technical zone, which is exactly the side facing T008's new SE contact. If the fraying actually continues onto T008, the two tiles become permanently linked by it (per Continuation's own Effect); if it stops at the edge instead, that stop must be marked explicitly rather than left ambiguous.
- **Matter/Family:** **Textile** — chosen to match the Echo continuation directly. If T008's Surface picks up T004's fraying, it should do so in the same material family, not merely in the same visual idea.
- **Mirror/Phrase:** C130's own card note, *"Robot detail, poorly cut"* — a literal scrap of text already on the deck. Read indirectly: something "poorly cut" resonates with an unsealed, still-fraying edge, and "robot detail" echoes T004's technical-hexagon register on the other side of that same tile. Recorded here; it doesn't need to appear physically on T008.
- **Omen/Question:** C130's own card is explicitly "poorly cut" — an unfinished part of the card itself. The question drawn from it: *what was cut away, and did it matter?* Stays open until a later phase or session answers it.
- **Pressure/Conflict:** named as **blank vs. marked** — the literal state of T008 right now, a coordinate with no physical body yet. This is also the surface form of the deeper conflict Cartography already set up: Void-Born (separate) vs. Gate (joined). Surface is where blank-vs-marked gets a first answer; whether it also answers separate-vs-joined is not guaranteed by the same gesture, and should be checked rather than assumed.
- **Provision/Mark:** a blank marker is prepared now, reserved for whatever word or symbol eventually marks T008's Gate crossing between T001 and T004 — the same pattern T001's own Provision/Mark followed in S008, later filled with "Amedda."

Story of Attunement:

1. Echo: T004's own frayed, permanently-unsealed edge is the thread available to continue onto T008.
2. Matter: textile is this session's material family, matching that continuation directly.
3. Mirror: C130's own card note, "Robot detail, poorly cut," is set aside as an indirect guide.
4. Omen: the card's own unfinished cut becomes a live question — what was cut away, and did it matter?
5. Pressure: blank vs. marked names T008's literal present state, standing in for the deeper Void-Born-vs-Gate conflict underneath it.
6. Provision: a blank marker waits, prepared now, for whatever eventually names T008's Gate crossing.

Attunement todo list (session-scoped prep, not the persistent queue):

- Check T004's frayed fabric zone at the SE edge (T008's own SE contact) before Surface — confirm whether that's actually where the permanently-unsealed edge sits, and decide whether the fraying continues onto T008 or stops there.
- Reserve textile as this session's governing material family.
- Keep "Robot detail, poorly cut" in mind as an indirect guide; it does not need to appear on the tile.
- Leave the "what was cut away" question open — do not force an answer this session unless Surface or Inscription genuinely produces one.
- At Surface, decide explicitly whether blank-vs-marked's resolution also touches Void-Born-vs-Gate, or whether the two conflicts resolve separately.
- Prepare a physical blank marker now, unfilled, reserved for T008's eventual Gate-crossing word or symbol.

## Surface

Numbers reused from Awakening: Green 2, Blue 3, Red 4 (C052, Water energy); Yellow 3, Brown 4, Black 1 (C130, Robot details). Fixed color mapping: Green = Ground, Blue = Substance, Red = Application, Yellow = Treatment, Brown = Structure, Black = Opening.

First Mark: T008 is a new tile, so before any of the six results below, place the anchor point — a mark anywhere on the tile, set with a black marker at a essentially random location. Physical action, not yet done.

Results:

- Ground / Green 2: Washed. Let the foundation be softened by a general tone, stain, haze, atmosphere, or veil.
- Substance / Blue 3: Rough. Choose something torn, fibrous, gritty, uneven, raw, scraped, or handmade-feeling.
- Application / Red 4: Interrupted. Break, skip, mask, tear, stop, misalign, or leave gaps in the application.
- Treatment / Yellow 3: Contrasted. Use opposition: light/dark, warm/cool, clean/dirty, blank/marked, old/new.
- Structure / Brown 4: Division. Establish zones, regions, sectors, quadrants, bands, split fields, or borders.
- Opening / Black 1: Closed. The foundation is whole, sealed, settled, or complete for now.

Interpreting the six results together:

- **Structure/Division** is the organizing move, and it directly echoes T004's own Surface structure back in S004 — T004 (also a Gate) divided into a T001-facing technical zone and an opposite frayed-fabric zone. T008 divides the same way, but the other direction: a **T001-facing zone** (carrying the inherited "dotti" tag) and a **T004-facing zone** (the SE side, where Attunement's Echo flagged T004's frayed edge as a possible continuation). Two Gate tiles, mirrored zone logic, meeting at the same corner.
- **Substance/Rough**, read against Matter/Family's Textile choice, means torn, fibrous, or frayed cloth specifically — not a rough material in some other family. This directly reinforces the Echo/Continuation thread rather than competing with it.
- **Application/Interrupted** governs how that rough textile actually gets laid down: in gaps, breaks, and skips rather than one continuous piece — leaving real untouched foundation between fragments, which also gives Treatment/Contrasted's blank-vs-marked reading (see Pressure, Attunement) a literal physical form.
- **Treatment/Contrasted**, named explicitly as **old vs. new**: the T004-facing zone should read as continuing something already-aged (matching T004's own worn, weathered frayed material), while the T001-facing zone should read as freshly new, unweathered. This stages the Continuation question physically — old material either does or doesn't cross into new territory — without deciding it yet.
- **Ground/Washed** sets the base condition under both zones: a general soft tone or haze across the whole foundation, applied before Division's zones are distinguished on top of it. This also gives Void-Born a physical register — an undifferentiated wash is the closest thing to "resisting surroundings" a base layer can do, before Structure imposes zones anyway.
- **Opening/Closed** keeps this session's foundation whole and settled — no breach, threshold, or reserved gap is left open at Surface. Any incompleteness (the frayed edge's fate, the Gate's actual crossing, the blank Provision marker) stays Inscription's job, not Surface's.

User's actual material plan, worked through together:

- **Ground/Washed, resolved as one continuous gradient glaze:** green concentrated at the T001-facing zone, transforming into beige and white toward the T004-facing zone — covering the whole tile (satisfying Washed's own "whole foundation, not a patch" requirement) while simultaneously doing Treatment/Contrasted's work: green reads as fresh/new (T001 side), beige/white as faded/old (T004 side). One gesture, two results.
- **Substance/Rough + Application/Interrupted, T004-facing zone:** frayed thread — white, green, and other colors — snaking from T004's edge toward the center or along the border, with real gaps deliberately left open. This resolves Attunement's open Continuation question: the fraying **does** continue onto T008, rather than stopping at the edge.
- **Application/Interrupted, T001-facing zone, second material:** scraps of old book pages related to time, placed near Dotti — torn/discontinuous rather than a whole piece of text. A deliberate callback: AIKA is Finnish for "time," so this zone's own interruption material speaks the same language as the neighbor it faces.
- **Structure/Division, resolved as a wall:** a physical wall, built from crossword puzzle paper — collaged/layered, some squares filled and some left blank. This single material answers three things at once: it's the literal Division boundary between the thread zone and the page-scrap zone; its grid nature is a direct, honest answer to Cartography's Grid-Tangled (a tile whose Entanglement is literally structure/lattice/measurement, built from an actual grid); and its blank-vs-filled squares physically embody Pressure's own blank-vs-marked conflict, right at the seam between the two zones.
- **Mirror/Phrase + Omen/Question, "poorly cut" and "robot":** the chemistry/science stencil provides torn schematic-looking fragments, layered into the wall or the thread zone — not literally robotic, but the same technical-diagram register T001 and T004 already both speak in (electrical scraps, schematic hexagons). An honest stand-in built from what's actually on hand.
- **Office/Gate, deliberately deferred:** no gate marker or symbol is placed this phase. The wall is built complete and solid, satisfying Opening/Closed (nothing deliberately unfinished this session) — and leaving Inscription a real, concrete obligation: an actual gate can be cut through this specific wall later, rather than a hole left pre-made now.
- Stamps, old map postcards: confirmed as general stock, not used on T008 this session.

Surface instruction:

1. Place the anchor point: one essentially-random black-marker mark, anywhere on the tile.
2. Apply one continuous gradient glaze across the whole tile: green at the T001-facing (S) zone, transforming into beige and white toward the T004-facing (SE) zone (Ground: Washed, whole-tile; doubles as Treatment: Contrasted, old vs. new).
3. Build a solid wall from collaged crossword-puzzle paper as the boundary between the two zones (Structure: Division) — leave some squares filled, some blank.
4. In the T004-facing zone: lay frayed thread (white, green, other colors) snaking from the T004 edge toward the center or along the border, leaving real gaps (Substance: Rough + Matter: Textile + Application: Interrupted). This continues T004's own unsealed fray onto T008.
5. In the T001-facing zone, near Dotti: place torn scraps of old time-related book pages (a second instance of Application: Interrupted, in this zone's own material).
6. Layer a few torn schematic/technical fragments from the chemistry-science stencil into the wall or thread zone (answers Mirror/Phrase and Omen/Question honestly, without forcing a literal robot image).
7. Leave the wall itself whole and uncut (Opening: Closed) — no gate opening yet. That's Inscription's obligation to create, not Surface's to pre-empt.

Actual Surface:

- Acrylic gradient painted green to beige to white, one continuous glaze across the whole tile (Ground: Washed, confirmed whole-tile).
- The crossword-puzzle strips and the green chemical schematics both sit on the **T001-facing zone** — the beige/white end of the gradient. The chemical-schematic layer is currently a first pass; the user is considering making it clearer/more legible in a follow-up touch.
- The frayed wool thread (grey and light green) sits on the **T004-facing zone** — the green end of the gradient — and physically continues the fray from T004's own frayed fabric, confirming Echo/Continuation as a real link between the two tiles. Glue used to flatten the thread left it uneven and "ugly-ish," matted rather than clean — an honest craft outcome, not the originally-planned neat snake, but still Substance: Rough and Application: Interrupted in spirit (real texture, real unevenness).
- **Treatment/Contrasted re-read against the actual materials, reversing the original guess:** the matted, aged-looking frayed thread (continuing old material from T004) is the tile's "old" register; the denser, newly-built crossword-and-schematic zone is its "new" register — old vs. new tracks with which zone is inherited material vs. which is freshly added, not with the green/beige-white color split as originally assumed.
- **First Mark, resolved as the Division line itself:** rather than a small isolated dot, the anchor mark became the actual boundary line creating a middle beige band between the two zones — crossword above it, thread below it. Structure/Division is literally seeded by First Mark, same pattern as T007/Mesa's own anchor point.
- Physically, the thread zone reads as facing S and SW on the tile itself, even though T008's own (post-Reversed) rule-naming records T004 as its SE edge — physical placement and the abstract edge-label don't have to align exactly; both are recorded here rather than forced to match.
- Time-related book-page scraps were left out of Surface entirely — an honest omission, not forgotten: the user plans to add a sticker reading **"MITÄ AIKA ON?"** ("What is time?" in Finnish) to the tile's northern edge during Inscription instead. Carried forward as an Inscription obligation.
- Opening/Closed holds: no wall was literally built as a separate object, but the crossword/thread zone boundary is whole and uncut — no gate exists yet. Still Inscription's job.
- Pressure/Conflict (blank vs. marked) is only partly answered: the crossword strips are described as filled, so the zone reads mostly as "marked" rather than a real blank/filled contrast. Left as an honest partial resolution rather than forced.

Surface is complete.

## Inscription

Numbers reused from Awakening: Green 2, Blue 3, Red 4 (C052, Water energy); Yellow 3, Brown 4, Black 1 (C130, Robot details). Fixed color mapping: Green = Scale, Blue = Form, Red = Behavior, Yellow = Relation, Brown = Force, Black = Residue.

Results:

- Scale / Green 2: Local. A contained area of the tile; noticeable but not dominant.
- Form / Blue 3: Figure. City, building, object, creature, landmark, island, cloud, shrine, focal thing.
- Behavior / Red 4: Absorb. Pull in, consume, inherit, cover, swallow, gather.
- Relation / Yellow 3: Neighbor. One or more adjacent tiles.
- Force / Brown 4: Pushing. It modifies, resists, or displaces something on another tile.
- Residue / Black 1: Clean. No major debt; the inscription resolves cleanly for now.

Interpreting the six results together — this draw finally gives Office/Gate its physical answer, deliberately deferred since Surface:

- **Form/Figure** is the vehicle: a real, nameable, recognizable **gate figure**, not an abstract mark. This is the moment Cartography's Gate office (T008 standing as a threshold between T001 and T004) stops being a standing rule and becomes an actual object.
- **Scale/Local** keeps the gate contained and bounded — placed along the existing Division seam (the beige band First Mark already created), not spreading to dominate the tile.
- **Behavior/Absorb** governs how the gate is physically built: it gathers a small piece from *both* existing zones — a scrap of crossword paper from the T001-facing side, a bit of frayed thread from the T004-facing side — into itself. Both lose their separate identity and become the gate's own material, rather than the gate sitting beside them as a third, unrelated thing. Literally: the threshold is built from what it stands between.
- **Relation/Neighbor**, named explicitly: **T001 and T004**, the same two tiles Cartography's Office/Gate already named. Recorded on this tile's own record and on both neighbors'.
- **Force/Pushing**, one specific modification named: a small schematic/chemistry-diagram fragment (echoing Mirror/Phrase's "robot detail, poorly cut" register) crosses from the newly-built gate figure onto **T004's own frayed zone**, at the shared edge. A small, real, physical addition to T004's own tile — recorded on both records.
- **Residue/Clean** confirms this closes cleanly: Gate's long-deferred obligation is finally paid in full this phase, and paying it doesn't create a new debt in the process.

The planned **"MITÄ AIKA ON?"** sticker (carried forward from Surface) sits separately, on the tile's own empty northern edge — no neighbor there to complicate it. It also loops back neatly to Attunement's still-open Omen/Question ("what was cut away, and did it matter?"): the sticker itself is a small cut/prepared object asking, in Finnish, what time even is — a second cut thing answering a question about cutting, rather than a plain factual answer.

Inscription instruction (draft):

1. Build a small, contained gate figure directly on the Division seam (the beige First-Mark band) — recognizable as an actual gate/threshold, not just decoration.
2. Construct it by absorbing real material from both zones: a torn crossword scrap and a piece of the frayed thread, physically merged into the gate figure itself.
3. Let a small schematic/chemistry-diagram fragment cross from the gate onto T004's own frayed zone, at the shared edge — this needs recording on T004's own record too.
4. Place the "MITÄ AIKA ON?" sticker on the tile's empty northern edge, separately from the gate.
5. No further debt to create — Residue/Clean means this should resolve, not open a new thread.

This is a starting proposal — let me know what you actually build, or adjust the gate's placement/material before doing it.

Actual Inscription:

- **Force/Pushing, resolved more precisely than drafted:** the schematic lines were emphasized in red, and that red bled across onto **T004's technical/schematic zone specifically** — not the frayed-fabric zone. A sharper choice than the original draft: schematic material crossing onto T004's own pre-existing schematic material, rather than crossing into the fray. Recorded on T004's own record.
- **A second continuation, unplanned but consistent:** the orange line T004 used at its own Inscription (S004) to settle its Division boundary was continued from T004 onto T008, traced along the edges of the matted thread zone. A second thread now runs between the two tiles alongside the frayed fabric itself — the same settling motif, carried across.
- The crossword-puzzle pieces were outlined in green — pulling the thread-zone's color across the Division seam into the crossword zone, visually knitting the two zones together rather than leaving Division as a hard cut.
- **Form/Figure, resolved as one object with the planned sticker:** rather than building a separate gate figure and placing the "MITÄ AIKA ON?" sticker elsewhere, the sticker itself *is* the gate — glued directly over the Division seam (the user's own term: "the rift"). This satisfies Behavior/Absorb through "cover" (one of its own listed readings): the gate/sticker covers the seam where both zones meet, gathering them under itself rather than sitting beside them as a third object. Simpler and more unified than the draft, and it fuses Form/Figure with the carried-forward time-question in a single gesture.
- **Naming, proposed by the user:** the tile could be named **Cross-word** — a pun that holds three readings at once: the crossword-puzzle material itself, a "crossed word" (the gate is literally a phrase — "MITÄ AIKA ON?" — laid across the rift), and "cross" as threshold/gate. Proposed, not yet locked in.

Inscription is complete. The tile is named **Cross-word**; its lower, T004-facing zone is named **Matted**.

## Chronicle

Numbers reused from Awakening: Green 2, Blue 3, Red 4 (C052, Water energy); Yellow 3, Brown 4, Black 1 (C130, Robot details). Fixed color mapping: Green = Record, Blue = Witness, Red = Meaning, Yellow = Publication, Brown = Maintenance, Black = Seed.

Results:

- Record / Green 2: Tile state. Record the final condition of the tile: level, surface, inscriptions, edges, bridges, wounds, names, unresolved effects.
- Witness / Blue 3: Before/after. Capture both the earlier state and the final state, or describe the difference if no before photo exists.
- Meaning / Red 4: Name/title. Name something: tile, path, region, wound, weather event, city part, bridge, rule, inscription, or session.
- Publication / Yellow 3: Short post. Write a short update: a caption, micro-blog, quick note, small progress entry.
- Maintenance / Brown 4: Todo list / future-work queue. Pick one todo item, update it, complete it, reschedule it, or move it into the next-session queue.
- Seed / Black 1: Keyword. A word, phrase, tag, motif, pressure, or concept may return later.

Interpreting the results:

- **Record (Tile state):** already fully captured in `../../tiles/records/t008-cross-word.md` — Cartography's six traits, Attunement's six pressures, Surface's gradient/zones/First-Mark-as-Division-line, and Inscription's sticker-gate over the rift. This Chronicle result confirms that record as complete and sufficient to reconstruct the tile without rereading the narrative.
- **Witness (Before/after):** no before photo exists — the tile didn't exist before this session. Before: an empty coordinate at [-1,1], already touching T001 and T004 but with no physical body. After: a gradient-washed tile split by a First-Mark-seeded boundary (the rift), crossword-and-schematic material on one side (Cross-word), matted frayed thread continuing T004's own old fray on the other (Matted), and a glued "MITÄ AIKA ON?" sticker standing as the gate itself, with a red-schematic bleed and an echoed orange line both crossing onto T004.
- **Meaning (Name/title):** this result is already satisfied by what happened organically during Inscription — naming the tile **Cross-word** and its lower zone **Matted**. Chronicle confirms both names as the tile's stable, permanent identity going forward, to be used consistently rather than "T008" alone.
- **Publication (Short post):** covered by the user's own blog post, `../../blog/blog-23-a-gate-born-already-facing-backward.md`, which already narrates this session in full. Not drafted separately here.
- **Maintenance (Todo list / future-work queue):** picked from `../../tracking/map-todo.md` — T004/Mirror's long-dormant "blog-18 extension" and "held-back T001/Mirror witness photo" item, open since S004 and never given a real trigger. Since this session worked with T004 directly again (the red-schematic bleed, the echoed orange line), it's a natural moment to stop letting it sit as a vague permanent note: rescheduled with an explicit trigger — next time T004/Mirror is itself the target tile.
- **Seed (Keyword):** creating keyword **K036**, name **"The Rift"** — the user's own term for the Division boundary that Surface built and Inscription then covered with a gate. Return condition: whenever a future tile's own boundary/division line later becomes, or is covered by, an actual crossing feature — or when Cross-word or Mirror is next targeted — revisit whether the Rift stays sealed under its sticker-gate or gets reopened.

Chronicle's main draw is complete.

## Artifact Draw

Card drawn: C071 — Green 2, Blue 6, Red 5, Yellow 5, Brown 1, Black 6.

Brown 1 selects Maintenance row 1 directly from the main Chronicle table (not the Matrix, since Brown ≠ 6):

> **Deck reset:** Shuffle, reset, sort, repair, update, or maintain the card/deck system.

Actual artifact: `../cards/Cards.csv` updated directly — C071 itself marked as used (Last used, Updated both set to 1.9.2026), the concrete deck-maintenance action this result asks for. Distinct from Chronicle's own Maintenance action (the T004 todo-rescheduling), so the two draws don't compete for the same ground.

Chronicle is complete for T008 / Cross-word: all six phases plus the Artifact Draw.