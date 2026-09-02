# S010 — T001 · AIKA (second revisit)

## Awakening

Starting tile:

- T008 / Cross-word at [-1,1] — the last tile targeted (S009).
- Current occupied coordinates before S010: T001 / AIKA at [0,0], T002 / Ring at [1,0], T003 / The Canyon at [1,-1], T004 / Mirror at [-1,0], T005 / The Monster at [-1,-1], T006 / Shoreline at [0,-1], T007 / Mesa at [2,-2], T008 / Cross-word at [-1,1].

Drawn cards:

- C200: Green 6, Blue 4, Red 2.
- C150: Yellow 1, Brown 5, Black 4.

Target calculation:

- NE-SW shift = Green 6 - Blue 4 = 2.
- SE-NW shift = Red 2 - Yellow 1 = 1.
- From T008 [-1,1], the raw calculated target coordinate is [1,2].

Adjustment:

- Raw target [1,2] is empty and does not touch any occupied coordinate — a real walk-back is required.
- Distances to the four candidate reference lines: axis q=0 → |q|=1; axis r=0 → |r|=2; same-sign diagonal (q=r) → |q-r|=1; opposite-sign diagonal (q=-r) → |q+r|=3. Nearest distance is 1, tied between the axis q=0 and the same-sign diagonal — the first time an axis and a diagonal have tied (previous ties were only ever between two diagonal step-paths).
- Resolved by working out, and then folding into `../../rules/map-creation-rules.md`, a general rule for this tie: the axis and diagonal rays sit on a fixed 8-ray clockwise wheel (N, NE, [same-sign-diagonal+], SE, S, SW, [same-sign-diagonal−], NW). A tie only ever happens between adjacent rays on this wheel — an axis and its neighboring diagonal, never axis-vs-axis or diagonal-vs-diagonal. Even black sends the target to whichever tied ray is next clockwise; odd black to whichever is next counter-clockwise.
- Here, the axis q=0 (SE side) sits clockwise of the same-sign diagonal (E side). Black is 4, even → clockwise → **the axis wins**.
- Walking along axis q=0 toward the origin: [1,2] → [0,2] (not touching anything) → [0,1]. [0,1] touches **three** tiles at once: T001 (NW neighbor), T002 (N neighbor), and T008 (SW neighbor).
- Brown is 5, odd — per the odd-Brown rule, the target moves one further step in the same established direction (continuing NW): [0,1] → [0,0]. [0,0] is occupied — by **T001**.

Final target:

- Final target coordinate: [0,0].
- Target tile: **T001 / AIKA — its second existing-tile revisit** (first was S008). Phase 2.2 (Existing-Tile Cartography) applies again.

Awakening notice:

- Green is 6 in this draw. For a new tile that would call the Origin Matrix, but this is an existing-tile revisit — Phase 2.2 has no cross-color Matrix tier, so Green 6 simply reads as Activation's own row 6 (Convergence) directly, same as any other number. Handled at Cartography, not flagged specially here.
- The walk-back passed directly through the neighborhood of T008's own coordinate and briefly touched three tiles at once ([0,1]: T001, T002, T008) before the odd-Brown step landed on T001 specifically — worth noting that T002 and T008 were both "in view" during this walk without being chosen.

## Cartography

Target: existing tile T001, second revisit. Phase 2.2 (Existing-Tile Cartography, the causal-chain model).

Cards reused from Awakening: C200 (Green 6, Blue 4, Red 2); C150 (Yellow 1, Brown 5, Black 4). Fixed color mapping: Green = Activation, Blue = Tile Effect, Red = Map Effect, Yellow = Constraint, Brown = Cost, Black = Carry-Forward.

Results:

- Activation / Green 6: Convergence. Two old pressures wake at once and must be reconciled together.
- Tile Effect / Blue 4: Structural Change. A recorded change to the tile's actual structure — anchor, edge count, division.
- Map Effect / Red 2: Attention Drawn. One neighbor is marked as watched/relevant, rules unchanged.
- Constraint / Yellow 1: Feature Locked. A specific already-named feature cannot be altered this session, regardless of what Tile Effect or Map Effect rolled.
- Cost / Brown 5: Relational Cost. A bond to a neighbor becomes a hard obligation, binding future work.
- Carry-Forward / Black 1: Chronicle must formally record the Cost.

Constraint collision check: Feature Locked protects the **AIKA anchor text** specifically — the one feature that has stayed untouchable across every session so far ("refuses burial"). Neither Structural Change nor Attention Drawn targets that anchor, so no collision; both stand as rolled.

**Explaining Convergence:** Grounded directly in T001's own recorded Unresolved field, which currently holds exactly two open items — not three, not an invented third thread:

1. Whether the S002 warning-strip bleed into T002 ever actually satisfied, complicated, or extended T001's founding warning-checker return condition. S008's Radiating result answered this from T001's own side toward T006 (and T004), but the record itself already says this only "closes the passive half of this question" — whether it fully resolves the *original* T002-facing condition was left explicitly open.
2. Whether "Amedda" — the word S008's Inscription placed at Dotti's NW edge, answering that same Radiating obligation — ever gains an in-world meaning, or stays a deliberately foreign, unexplained name (K035's own return condition).

These two items look separate on the page, but they were never really independent: Amedda *is* the concrete result of trying to answer the warning-checker question from the T006 side. Convergence's demand is to stop treating them as two isolated open threads and recognize they're the same pressure, still unresolved on both of its ends. Because Amedda hasn't settled into a meaning, the *original* T002-facing side of the warning-checker question — dormant since S002 — wakes back up too: T001 can't fully close either end while the other is still open.

- **Map Effect/Attention Drawn**, grounded in that reading: **T002** — not T006 or T004 — is marked watched/relevant this session. T002 is the *original* neighbor from S002, the one side of this old question that Amedda's arrival never actually touched.
- **Cost/Relational Cost**, paired with it: the long-dormant T001–T002 bond, watched but otherwise unchanged in S002 through S009, now becomes a **hard obligation** — the same move S008 already made for the T001–T006 side of this same question. Both ends of the original warning-checker thread are now hard-bound, not just watched.
- **Tile Effect/Structural Change**, resolved as a Division: T001's own internal layout formally recognizes, for the first time, that its NE/N-facing Spread-points zone (the warning-checkers, the safety line) and its S/SW/NW-facing Dotti corridor are **one structural system**, not two unrelated historical episodes from different sessions. A recorded state change — not physical craft yet, that's Surface's job.
- **Carry-Forward**: Chronicle must formally record the new Relational Cost with T002, the same way S008's Chronicle recorded T001–T006's.

Interpretation: this session doesn't invent a new pressure — it forces two already-written-down open questions to admit they were always one question, split across two neighbors and three sessions (S002, S008, and now S010). Nothing about T001's founding identity changes (Feature Locked protects the AIKA anchor specifically), but its own internal bookkeeping now treats the warning-checker mechanism and the Dotti corridor as a single connected structure, and both of the old question's neighbor-facing ends — T002 and T006 — are hard-bound rather than one watched and one settled.

Obligations for later phases:

- Attunement and Surface must engage with the T001–T002 bond directly — it's now a hard obligation, not a passive watch.
- Structural Change's new unified reading (Spread-points + Dotti as one system) should inform how later phases treat both zones — not as separate named areas doing unrelated things.
- The AIKA anchor stays off-limits this session (Feature Locked).
- Amedda's own open question (does it ever gain meaning) is not resolved by this Cartography — Convergence explains *why* it's still open, but doesn't close it.

Loggable note:

S010 Cartography reads Green 6 as Convergence, recognizing that T001's two currently-open Unresolved items — the original S002 T002-facing warning-checker question and S008's Amedda-meaning question — were never actually separate, and hard-binds the long-dormant T001–T002 side of that question the same way S008 already hard-bound the T006 side.

## Attunement

Numbers reused from Awakening: Green 6, Blue 4, Red 2 (C200, Yellow energy); Yellow 1, Brown 5, Black 4 (C150, Dragon). Fixed color mapping: Green = Echo, Blue = Matter, Red = Mirror, Yellow = Omen, Brown = Pressure, Black = Provision.

Green rolls a 6, calling the Echo Matrix, read using this session's own Yellow/Brown/Black (Yellow 1, Brown 5, Black 4):

- Yellow — Feeling, row 1: **Calm**. The echo feels settled, quiet, balanced, or resolved.
- Brown — Boundary, row 5: **Region**. The echo belongs to a larger area, field, territory, grid, cluster, or shape.
- Black — Distortion, row 4: **Infected**. The echo is contaminated by another color, material, region, pattern, or idea.

Results:

- Echo / Green 6: Echo Matrix — Calm + Region + Infected.
- Matter / Blue 4: Reserve. Store one found material, scrap, texture, image, or object in the active reserve for future use.
- Mirror / Red 2: Old Mirror. Find one older tile, scan, photo, or layer that the target tile should echo or resist.
- Omen / Yellow 1: Sign. Choose one visible element from the card/image/sign. It becomes an omen for later work.
- Pressure / Brown 5: Correction. Choose one correction the tile seems to demand.
- Provision / Black 4: Token. Create one pending token, card, note, or marker for an unresolved effect.

Interpreting the results — and this is one of those sessions where the matrix result and the physical instinct arrived at the same place independently:

- **Echo Matrix (Calm + Region + Infected):** the old warning-checker/Amedda pressure feels dormant and settled on its surface (Calm) — it's been quietly watched for years without incident — but it actually belongs to a whole region-level structure now (Region: the newly-recognized Spread-points-plus-Dotti system, not a single edge), and that calm is deceptive, because the region is Infected: contaminated by a color or material from somewhere else. This reads directly as the user's own proposed physical image: T002's own material — yellowish and blackish, echoing its buried-threshold/black-warning-bleed identity — spreading in as a contaminating root system, unsettling a boundary that had looked calm and settled.
- **Mirror/Old Mirror:** **T002/Ring itself** — its plastic ring, dark center, black warning-strip bleed, and void-relic Court-arena lore. Decided now, per the result's own Effect: **echo, not resistance**. Convergence is about reconciling two old pressures, not fighting them, so T001 should echo T002's own visual language (yellowish/blackish, buried/root/mountain material) rather than push back against it.
- **Omen/Sign, revised:** not the Dragon — **"Yellow energy" itself** (C200's own concept, a burst/glow/radiating yellow force), used with no further card-art detail beyond the name. This actually fits the physical plan more directly than the Dragon did: the governing sign is now literally the same color doing the tainting, rather than a creature standing in for it.
- **Matter/Reserve:** a length of yellow-and-black material (yarn, wire, or dyed root-like scrap) reserved now, specifically earmarked as the "root" material for this convergence — available through next session if not used immediately.
- **Pressure/Correction — Connect it:** the plainest possible reading, and it matches Cartography's own Structural Change exactly: Surface's required action is to physically **connect** the two zones (Spread-points and Dotti) rather than leave them as two separate named areas that merely happen to share a Cartography note.
- **Provision/Token — ignored, forced retcon:** the user does not want the token mechanic to exist. For this session, Provision/Token is simply skipped — no token gets created. This escalates (but does not yet resolve) the existing S007 Delta Candidate "Remove the Token/Provision System" in `../../rules/rules-delta.md`; still not a finalized rule, and past tiles' existing token references are left untouched as historical record.

Story of Attunement:

1. Echo: the old pressure feels calm on the surface, but it belongs to a whole region now, and that calm is infected by a foreign color already waiting to spread in.
2. Matter: a yellow-and-black root-like scrap is reserved, earmarked for this specific convergence.
3. Mirror: T002/Ring is the old mirror, to be echoed rather than resisted.
4. Omen: "Yellow energy" itself becomes the governing sign — the same color doing the tainting, not a creature standing in for it.
5. Pressure: the two zones must be connected, not merely cross-referenced on paper.
6. Provision: ignored this session, per the user's forced retcon — no token gets created.

Attunement todo list (session-scoped prep, not the persistent queue):

- Reserve a yellow-and-black root-like scrap (yarn, wire, dyed paper, or similar) for this session's use.
- Treat T002/Ring as the working visual reference — echo its buried/root/mountain material language, don't resist it.
- Keep "Yellow energy" itself in mind as the governing sign for how the root/taint material should read.
- At Surface, physically connect the Spread-points zone and the Dotti corridor — a required action, not optional.
- No Provision/token prep needed this session.

Concrete material decisions made ahead of Surface, per the user's own proposed direction:

- T002/Ring's own mountain becomes tainted with yellow and black, and that taint travels down T001's eastern edges (the NE contact with T002, curving along toward the S/SW where Dotti sits) rather than cutting straight across.
- Dotti's own material extends to meet that taint partway, giving Structural Change and Pressure/Correction's "connect it" a literal physical route.
- Both routes bend around the AIKA anchor rather than crossing it directly — satisfying Constraint/Feature Locked without needing to think about it as a separate restriction.
- Floated, not yet decided: treating **Dotti as a nation/region** in its own right. This would be a strong, concrete way to finally exercise T001's own Region-Tangled Entanglement (from S001) — its Effect ("Name the region this tile belongs to...") has sat unspent since the tile's birth. Worth deciding explicitly rather than drifting into it.
- Explicitly preliminary — to be refined once Surface actually begins.

## Surface

Numbers reused from Awakening: Green 6, Blue 4, Red 2 (C200, Yellow energy); Yellow 1, Brown 5, Black 4 (C150, Dragon). Fixed color mapping: Green = Ground, Blue = Substance, Red = Application, Yellow = Treatment, Brown = Structure, Black = Opening.

No First Mark this session — that rule is specific to a tile's birth, and T001 already has one from S001.

Green rolls a 6, calling the Ground Matrix — never touched before this session, so all three landed cells were TBD and are now newly interpreted and folded into `../../rules/map-creation-rules.md`:

- Yellow — Source, row 1: **Edge**. The ground's condition comes from a contact edge already active on the tile, not an outside card/omen or an unrelated internal source.
- Brown — Behavior, row 5: **Stains**. The ground's condition behaves like a stain — seeping, discoloring, spreading the way a spill or contamination would.
- Black — Consequence, row 4: **Be protected**. The resulting condition becomes load-bearing: later Application, Treatment, or Structure choices must not override or erase it.

Results:

- Ground / Green 6: Ground Matrix — Edge + Stains + Be protected.
- Substance / Blue 4: Precise. Choose something clean, measured, sharp, ruled, geometric, controlled, or technical.
- Application / Red 2: Sparingly. Apply it in small amounts, fragments, hints, partial marks, or minimal touches.
- Treatment / Yellow 1: Muted. Keep hue, contrast, texture, or finish quiet, pale, softened, or restrained.
- Structure / Brown 5: Shape. Establish a larger geometry, recognizable at a glance.
- Opening / Black 4: Breach. Create or imply a cut, tear, gap, rupture, void, window, or broken continuity — must actually interrupt the foundation's continuity somewhere real.

Interpreting the six results together:

- **Ground Matrix (Edge + Stains + Be protected)** names exactly what's already been decided: the ground's condition originates at the **T002 edge** (the NE contact — the newly-filled Source cell describes precisely this), behaves like a **stain** spreading down toward Dotti rather than a clean application, and once laid down, that tainted condition must be **protected** — later phases can't just paint over or erase the connection. This last part gives Pressure/Correction's "connect it" real teeth: once the two zones are joined, the join has to stay.
- **Substance/Precise**, in real tension with the "organic root/stain" image: resolved by rendering the taint in a *technical* register rather than a loose organic one — wire, ruled lines, or cut geometric shapes standing in for roots, echoing T002's own buried-threshold material and the campaign's established schematic/technical vocabulary (T001's own electrical scraps, T004's schematic hexagons). A precise, controlled root, not a sloppy bleed.
- **Application/Sparingly** tempers the whole route: the taint appears as scattered small marks or fragments along its path, not a solid thick line — consistent with roots being thin, reaching tendrils rather than a mass. Clearly more untouched tile than touched, along the whole route.
- **Treatment/Muted**, in tension with wanting bold yellow and black: resolved by keeping everything *else* on the tile quiet and restrained, so the taint reads as the deliberate exception the result's own Effect explicitly allows for — it stands out precisely because the baseline stays muted.
- **Structure/Shape**: the route reads as a recognizable **arc** — curving from the T002/NE edge down around the AIKA anchor to the S/SW where Dotti sits. Not a straight cut, an actual bend, matching both the "circle around AIKA" plan and Dotti's own established corridor identity.
- **Opening/Breach**, in real tension with Pressure/Correction's "connect it": the arc is real and mostly continuous, but carries **one deliberate gap** somewhere along its length — an honest acknowledgment that reconciling two old pressures doesn't mean total, seamless connection. Something stays torn even as the two zones are joined.

Surface instruction:

1. Along T001's NE edge (T002 contact) curving down around the AIKA anchor to the S/SW (Dotti), lay a sparse, technical-looking root/taint: wire, ruled lines, or cut geometric fragments rather than an organic bleed — small scattered marks, not a solid line (Substance: Precise; Application: Sparingly).
2. Color the taint yellow and black, and keep everything else on the tile muted/restrained so the taint reads as the deliberate exception (Treatment: Muted).
3. Shape the whole route as a recognizable arc at a glance (Structure: Shape) — bending around the AIKA anchor rather than crossing it (Constraint: Feature Locked, already established at Cartography).
4. Leave one real, deliberate gap somewhere along the arc's length — the connection is genuine but not total (Opening: Breach).
5. Once laid down, treat the taint as load-bearing: it should not be casually covered or erased by anything else done to the tile this session or later (Ground Matrix: Be protected).

This is a starting proposal — adjust materials or the arc's exact path based on what's actually on hand.

Actual Surface:

- **The connection runs both directions, as planned:** Dotti's own green paper continues along T001's eastern edge up toward T002 — with a small leak into T008 — while T002's own "mountain ridges" flow the other way onto T001, accentuated with white tissue paper. The two materials genuinely meet rather than one simply arriving.
- **Real cross-tile cost on T002:** the incoming green covers parts of T002's own red circle, black circle, and the roadway around the ring. Not erased — the user expects these to be redrawn or otherwise answered at Inscription, which is exactly what Ground Matrix's "Be protected" asks for: the connection, once made, isn't something later work casually erases back to how T002 looked before.
- **T002's ridge material covers T001's own warning strip** on the NE edge — a second real, physical consequence, this time landing on T001 itself rather than a neighbor.
- **Structure/Shape, physically resolved:** a compass-drawn circle following roughly Dotti's own edges, with a second green point spreading along it. The far edge of that painted strip is deliberately uneven — a real, physical irregularity, not a clean line. This also reads as Opening/Breach: the uneven edge is the real interruption the result asked for, not merely implied.
- **Substance/Precise, honestly reconciled:** the paint and tissue themselves read as organic, not technical — but the compass-drawn circle is a genuinely deliberate, controlled, measured method, which is where Precise actually shows up this session, rather than in the material's own texture.
- **Application/Sparingly, mixed result:** the yellow-and-black bleed onto T002 is explicitly described as subtle markers — a clean match. But the green paper/tissue/stippling covers more ground than "small amounts, hints, minimal touches" would suggest. Recorded honestly as a partial resolution, not forced.
- **Treatment/Muted, live tension:** the yellow/black stays quiet, satisfying Muted directly. But the green material is trending toward dominance rather than staying a quiet baseline — especially now that it's reading as a forest. Left as an open tension, not resolved.
- **Small additional bleeds:** the green paint also reaches a little further onto T004 and T006 — continuing, not replacing, the relationships already established in S008.
- **A new direction, arriving mid-craft:** lighter green stippled over the existing green areas is starting to read as **Dotti becoming a forest nation** — with buildings floated as a possible future addition. This gives T001's long-unspent Region-Tangled Effect (name the region this tile belongs to) its first real, physically-grounded candidate: not just "Dotti," but specifically a forest nation. Not yet formally locked in — a strong candidate for Inscription or Chronicle to confirm.

Surface is complete.

## Inscription

Numbers reused from Awakening: Green 6, Blue 4, Red 2 (C200, Yellow energy); Yellow 1, Brown 5, Black 4 (C150, Dragon). Fixed color mapping: Green = Scale, Blue = Form, Red = Behavior, Yellow = Relation, Brown = Force, Black = Residue.

Green rolls a 6, calling the Scale Matrix — never touched before this session, so all three landed cells were TBD and are now newly interpreted and folded into `../../rules/map-creation-rules.md`:

- Yellow — Extent, row 1: **Seed**. The inscription starts from a single small point or kernel, not yet spread or reaching any edge.
- Brown — Expansion law, row 5: **Jumps by relation**. It doesn't travel by continuous contact — it appears at a related tile or feature elsewhere because of a shared relation, skipping the space in between.
- Black — Limit, row 4: **Breaks at seam**. Its reach stops exactly at a seam or division already present on the tile, even where it could otherwise continue.

Results:

- Scale / Green 6: Scale Matrix — Seed + Jumps by relation + Breaks at seam.
- Form / Blue 4: Pattern. Grid, patchwork, repetition, cells, hatching, texture, district logic, weave.
- Behavior / Red 2: Spread. Grow, bleed, branch, multiply, expand, continue.
- Relation / Yellow 1: Self. The tile itself: its surface, center, wound, mood, or internal logic.
- Force / Brown 5: Propagating. The force spreads outward through multiple connected tiles at once, rather than one bridge or transmission line.
- Residue / Black 4: Debt. Creates a future obligation for Chronicle or another session.

Interpreting the results — this draw is the moment Dotti's forest-nation direction, floated at Surface, gets a physical and mechanical answer:

- **Form/Pattern + Scale Matrix's Seed + Behavior/Spread, combined:** one small seed-mark planted within Dotti — the literal first building or tree — from which a few repeating building/tree-like marks grow outward. This is also the map's second-ever settlement-style imagery, directly triggering T007/Mesa's own **K034 First Settlement** return condition ("when settlement, road, or building imagery appears again anywhere on the map").
- **Scale Matrix's Breaks at seam:** this growing pattern stays entirely on Dotti's own side of the internal seam Cartography's Structural Change created — it does not cross into the Spread-points/warning-checker zone, and does not cross the AIKA anchor (Feature Locked, already established).
- **Relation/Self:** the meaning of this mark is intrinsic to T001 — it's about what Dotti *is* becoming, not something that needs T002's or T006's own record to make sense.
- **Force/Propagating + Scale Matrix's Jumps by relation, combined:** the forest-nation identity itself doesn't need to travel continuously to reach T004, T006, and T008 — small matching seed-marks can simply appear on each of them, because a relation already exists (the small green bleeds already delivered this session and in S008/S009). Naming the actually-reached tiles, per Propagating's own Effect: **T004, T006, T008**.
- **This is the moment to formally exercise T001's own Region-Tangled Entanglement**, unspent since S001. Its Effect: "Name the region this tile belongs to. If a later tile is ever identified as part of the same region, both tiles gain a shared keyword marking that region." **Named: Dotti — a forest nation.**
- **Residue/Debt**, named concretely: Region-Tangled's own Effect requires a real *identification* decision, not just a bleed — so the debt is deciding whether T004, T006, and T008 (all already touched by Dotti material) actually get identified as part of the same forest-nation region, or stay merely adjacent to it. Not resolved now; recorded as a real Chronicle debt.

Inscription instruction:

1. Plant one small seed-mark within Dotti — the literal first building or tree — near the compass-circle's own uneven edge from Surface.
2. From that seed, add a few small repeating building/tree-like marks (at least a few, to read as a pattern rather than a coincidence).
3. Keep the whole pattern on Dotti's own side of the internal seam; do not let it cross into the Spread-points zone or touch the AIKA anchor.
4. Optionally, add one small matching seed-mark each on T004, T006, and T008 — not connected by a continuous line, appearing there because a relation already exists.
5. No further material changes required elsewhere — Relation, Force, and Residue are already satisfied by naming Dotti's forest-nation identity and flagging the T004/T006/T008 identification question as a real debt.

This closes the loop Attunement opened with the floated "Dotti as a nation" idea: Region-Tangled finally gets named, and the debt of who else belongs to that region is handed to Chronicle rather than quietly assumed.

Actual Inscription:

- **T002's covered features fully redrawn:** the red circle, black circle, and roadway/driveway that Surface's incoming green had covered were all restored. Ground Matrix's "Be protected" reading holds — the connection stays, but T002's own identity wasn't erased by it.
- **Seven buildings drawn under the Dotti sign** — a concrete, countable repeating pattern (Form/Pattern, satisfying its own Effect's "repeats at least a few times" requirement outright), confirming the map's second-ever settlement-style imagery and triggering T007/Mesa's K034 First Settlement return condition for real, not just provisionally.
- **The AIKA text was clarified again** where the forest had slightly covered it — the same "refuses burial" move this anchor has made every time something threatens to cover it, now against its own tile's forest rather than an outside material.
- **Scale Matrix's Jumps by relation did not happen this session:** no seed-marks were added to T004, T006, or T008. Left honestly unresolved rather than assumed — Force/Propagating's own reach still stands on Surface's already-delivered paint bleeds, but the Inscription-level "jump" specifically stays undone, a live option for a future session rather than something quietly completed here.

Inscription is complete.