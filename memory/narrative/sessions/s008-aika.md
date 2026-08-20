# S008 — T001 · AIKA (revisit)

## Awakening

Starting tile:

- T007 / Mesa at [2,-2] — the last tile targeted (S007).
- Current occupied coordinates before S008: T001 / AIKA at [0,0], T002 / Ring at [1,0], T003 / The Canyon at [1,-1], T004 / Mirror at [-1,0], T005 / The Monster at [-1,-1], T006 / Shoreline at [0,-1], T007 / Mesa at [2,-2].

Drawn cards:

- C101, Green power leaf: Green 3, Blue 5, Red 5.
- C100, Zombie: Yellow 2, Brown 5, Black 1.

Target calculation:

- NE-SW shift = Green 3 - Blue 5 = -2.
- SE-NW shift = Red 5 - Yellow 2 = 3.
- From T007 [2,-2], the raw calculated target coordinate is [0,1].

Adjustment:

- Raw target [0,1] is empty. Checked against every occupied coordinate:
  - [0,1]'s NW neighbor is [0,0] = T001.
  - [0,1]'s N neighbor is [1,0] = T002.
  - No other neighbor coordinate is occupied.
- So the raw target already touches the map — to two tiles at once — before any walk-back step. Per the already-touching rule, skip stepping and go straight to the Brown-parity decision.
- **New case, first encountered here:** every prior already-touching landing (S005, S006, S007) rolled an even Brown, so the tile was simply created on the spot. This time Brown is 5, odd. The odd branch ("the target moves one step further") was written for the ordinary walk-back flow, where a direction of travel is already established from prior steps — but no steps were taken here at all.
- Resolution (now folded into `../../rules/map-creation-rules.md`'s walk-back section): identify the raw target's nearest reference line the same way the ordinary mechanism would. [0,1] sits exactly on one already — the axis where the first coordinate is zero (distance 0, versus 1 for the other two candidate lines). Taking one real hex step further along that axis, back toward the map, means stepping NW: [0,1] + NW offset [0,-1] = [0,0].
- [0,0] is occupied — by T001. Per the odd branch's own stated outcomes ("might land on an existing tile"), the session revisits T001.

Final target:

- Final target coordinate: [0,0].
- Target tile: **T001 / AIKA — an existing-tile revisit**, the first one this campaign has ever had. Phase 2.2 (Existing-Tile Cartography, the causal-chain redesign) gets its first real use this session.

Awakening notice:

- No color-6 pressures in this draw (Green 3, Blue 5, Red 5, Yellow 2, Brown 5, Black 1 — no 6 appears at all).
- T001 already carries several open threads worth checking against this revisit: its long-standing Unresolved question (whether the S002 warning-strip bleed into T002 satisfies its own warning-checker return condition), and the newer S006/S007 neighbor effects (Shoreline's silver hexagon over the AIKA text; T004 and T006/T007's various edge relations).

## Cartography

Target: existing tile T001, revisited for the first time. This is the first session ever to use Phase 2.2 (Existing-Tile Cartography, the causal-chain model) instead of new-tile Cartography.

Cards reused from Awakening: C101, Green power leaf (Green 3, Blue 5, Red 5); C100, Zombie (Yellow 2, Brown 5, Black 1). Fixed color mapping: Green = Activation, Blue = Tile Effect, Red = Map Effect, Yellow = Constraint, Brown = Cost, Black = Carry-Forward.

Results:

- Activation / Green 3: Name Spoken. A keyword or omen already attached to the tile is invoked by this session's cards.
- Tile Effect / Blue 5: Content Change. An actual named feature (mark, region, label) is added, renamed, or reassigned.
- Map Effect / Red 5: Radiating. Something concrete (a mark, a bleed, a pressure) actually crosses into a neighbor.
- Constraint / Yellow 2: Identity Locked. An established Origin/Tether/Entanglement/Temper/Office/Inheritance trait cannot be reinterpreted this session.
- Cost / Brown 5: Relational Cost. A bond to a neighbor becomes a hard obligation, binding future work.
- Carry-Forward / Black 1: Attunement must read and respond to the Activation.

Constraint collision check: Identity Locked protects T001's six founding traits (Contagious, Tidebound, Region-Tangled, Dense, Proclaim/By-Mark/Burial-Cost, Edge Inheritance) specifically. Neither Content Change (a named *feature*, not a founding trait) nor Radiating (a pressure crossing an edge) touches that axis, so no collision — both stand fully as rolled.

Grounding each result in T001's actual record:

- **Activation / Name Spoken:** C100's own card name, Zombie, invokes **K007 Burial Cost** — T001's Office was always Proclaim by Mark, paid for with a Burial Cost ("something must be covered, layered over, submerged, deferred, or made latent to pay for it"). A zombie is the literal image of a burial cost refusing to stay paid. The old cost is stirring, not being renegotiated (Constraint forbids that) — just invoked as a live pressure again.
- **Tile Effect / Content Change:** the "bottom archaic-symbol area" — one of T001's own named features — has quietly become a palimpsest over three sessions: T004 rewrote part of it in S004, and T006/Shoreline's silver hexagon reached into it in S006. It has never been reassigned as what it actually is now. Content Change formally renames it: the bottom archaic-symbol area becomes the **archaic-symbol palimpsest** — a named feature that is explicitly, permanently multiply-modified, rather than a single untouched zone that merely happens to have things pushed onto it.
- **Map Effect / Radiating:** the newly-renamed palimpsest doesn't just sit there passively — something concrete crosses back out from it, into **T006 / Shoreline**, the most recent tile to reach into that zone. This is T001 finally answering from its own side, rather than continuing to leave its long-standing warning-checker question sitting entirely on Shoreline's side of the ledger (per T001's own Unresolved field: "it may get answered from Shoreline's side instead" — that passive framing changes here).
- **Constraint / Identity Locked:** confirmed — this session invokes Burial Cost and modifies a feature, but does not redefine what Contagious, Tidebound, Region-Tangled, Dense, Proclaim, By-Mark, Burial Cost, or Edge Inheritance actually mean for T001.
- **Cost / Relational Cost:** the T001–T006 bond stops being an open, floating question and becomes a **hard, binding obligation** on both tiles — whatever crosses this session must actually be answered by both records, not left as another deferred maybe.
- **Carry-Forward:** Attunement must directly engage with the Burial-Cost / Zombie Activation — not drift onto an unrelated pressure.

Interpretation: T001's oldest unresolved question has sat still since S002, technically inherited but never really acted on by T001 itself. This session's cards use the tile's own accumulated history (a genuinely multiply-modified corner, a matching keyword already on record, a card that names the theme outright) to finally make T001 the one that acts — sending something back toward Shoreline instead of waiting on it. Nothing about what T001 fundamentally *is* changes; what changes is that one of its features gets a true name, and one of its relationships stops being able to stay quietly unresolved.

Obligations for later phases:

- Attunement must read and respond to the Burial Cost / Zombie Activation directly (Carry-Forward).
- The archaic-symbol palimpsest is now a formally named feature — later phases should treat it as such, not as an unnamed zone that happens to be modified.
- Something must physically radiate from T001 toward T006/Shoreline this session — Surface or Inscription needs to give it a real body.
- The T001–T006 relational bond is now a hard obligation on both tiles' records, not an optional thread.

Loggable note:

S008 Cartography — the first existing-tile revisit and the first real use of Phase 2.2 — wakes T001's Burial Cost via the Zombie card, formally names its multiply-modified archaic-symbol corner as a palimpsest, and sends a pressure back toward T006/Shoreline, turning T001's oldest open question into a hard bond between the two tiles instead of a one-sided debt.

## Attunement

Numbers reused from Awakening: Green 3, Blue 5, Red 5 (C101, Green power leaf); Yellow 2, Brown 5, Black 1 (C100, Zombie). Fixed color mapping: Green = Echo, Blue = Matter, Red = Mirror, Yellow = Omen, Brown = Pressure, Black = Provision.

Results:

- Echo / Green 3: Unresolved. Choose one unresolved previous-session obligation that may influence this tile.
- Matter / Blue 5: Acquire. Order, acquire, wishlist, or deliberately seek one interesting material/tool for future sessions.
- Mirror / Red 5: Prepared Mirror. Prepare one reference for actual use: print it, crop it, save it, place it nearby, or attach it to the session notes.
- Omen / Yellow 2: Hue. Choose one color from the card/sign. It becomes a color bias, absence, or contrast.
- Pressure / Brown 5: Correction. Choose one correction the tile seems to demand: connect it, quiet it, disturb it, divide it, bury something, reveal something, or make it stranger.
- Provision / Black 1: Mark. Prepare one blank label, tag, marker, or notation piece for possible later use.

Interpreting the results — all six genuinely engage Cartography's Carry-Forward demand (Attunement must read and respond to the Burial Cost / Zombie Activation), not just one:

- **Echo/Unresolved:** the obligation chosen is the same one Cartography already activated — the T001↔T006 warning-strip question, now a hard Relational Cost bond rather than a one-sided deferral. Echo reinforces it with a second, independent hook rather than reaching for a different thread.
- **Matter/Acquire:** an unearthed-feeling material — rust tone, bone-white, aged or weathered paper — something that reads as *dug up* rather than freshly made. Not needed this session; reserved for whenever the palimpsest needs further physical treatment.
- **Mirror/Prepared Mirror:** a fragment of C100's own Zombie artwork — specifically its decayed, cracked texture, not the whole image — set aside as the actual visual reference for how the radiating mark toward T006 should read.
- **Omen/Hue — a deliberate color echo:** sickly, undead green. This isn't just "the zombie's color" in isolation — it's the same register T006/Shoreline's own emerald river-grooves already speak in. Crowning it here means whatever radiates toward T006 can visually agree with what's already there, rather than introducing a fourth unrelated color.
- **Pressure/Correction — Reveal something:** the archaic-symbol palimpsest has only ever been *covered* across three sessions (T004's rewrite, T006's hex-push) — never opened back up. The correction this session demands is the opposite motion: expose or reveal part of what's underneath, even while a piece of it is simultaneously sent outward to Shoreline.
- **Provision/Mark — given real purpose, not a generic reserve:** the blank marker is prepared now specifically to carry whatever word or symbol ends up being the actual content of the Radiating response to T006. It stays blank until Inscription decides what that content is.

Story of Attunement:

1. Echo: the old, one-sided warning-strip question with T006 returns, already promoted to a hard bond by Cartography, and Attunement doesn't look away from it.
2. Matter: an unearthed material — rust, bone, aged paper — is marked down for a future session, not spent now.
3. Mirror: a cracked, decayed fragment of the Zombie card itself becomes the real visual reference for the mark that will travel to T006.
4. Omen: sickly undead green is crowned, chosen because it already agrees with the emerald T006 speaks in.
5. Pressure: something in the palimpsest must be revealed, not buried further, even as part of it travels outward.
6. Provision: a blank marker waits, prepared now, for whatever finally crosses over to Shoreline.

Attunement todo list (session-scoped prep, not the persistent queue):

- Treat the T001↔T006 warning-strip/Radiating obligation as this session's central answerable question — don't let a later phase drift onto something else.
- Note down (not yet acquire) an unearthed-feeling material — rust, bone-white, aged paper — as a future-session want.
- Set aside a fragment of C100's Zombie card, specifically its cracked/decayed texture, as the actual working reference for Surface/Inscription.
- Reserve sickly undead green as the governing hue, deliberately matched to T006's existing emerald.
- Decide, at Surface or Inscription, what part of the archaic-symbol palimpsest gets exposed rather than covered further.
- Prepare a physical blank marker now, reserved for whatever word or symbol ends up crossing to T006, unfilled until that's decided.

Concrete material decisions made ahead of Surface:

- **Matter/Acquire:** metallic paint added to the shopping list — reads as unearthed/tarnished metal, and also echoes T006's own silver hexagon.
- **Omen/Hue + Pressure/Correction, combined:** green tissue paper (already on hand) does double duty — its translucency lets it tint the surface sickly green while also letting a hint of what's underneath show through, serving as the non-destructive Reveal option in one material rather than two separate treatments.
- **Mirror/Prepared Mirror:** super glue on silk paper, to create a crackle effect for the decayed texture reference — brittle, fast-drying glue should produce sharper, less even cracks than a slower crackle medium, which suits "decayed" better than a neat crackle would.

## Surface

Numbers reused from Awakening: Green 3, Blue 5, Red 5 (C101, Green power leaf); Yellow 2, Brown 5, Black 1 (C100, Zombie). Fixed color mapping: Green = Ground, Blue = Substance, Red = Application, Yellow = Treatment, Brown = Structure, Black = Opening.

No First Mark this session — that rule is specific to a tile's birth, and T001 already has one from S001.

Results:

- Ground / Green 3: Divided. Let the foundation begin with zones, halves, bands, sectors, or competing fields.
- Substance / Blue 5: Strange. Choose something unexpected, found, artificial, excessive, awkward, or not normally map-material.
- Application / Red 5: Edgeward. Apply it from edges, seams, borders, routes, or contact zones inward/outward.
- Treatment / Yellow 2: Stained. Let color or tone behave like residue, seepage, contamination, shadow, or memory.
- Structure / Brown 5: Shape. Establish a larger geometry: circle, triangle, square, spiral, arc, corridor, ring, patch.
- Opening / Black 1: Closed. The foundation is whole, sealed, settled, or complete for now.

Interpreting the six results together, for a revisit rather than a birth:

- **Ground/Divided** reads as the whole tile splitting into two zones this session: the untouched original AIKA surface (S001's own work, left alone) versus a new intervention zone where this session's event actually happens. This isn't a new foundation — it's a division of *where this session is allowed to touch*.
- **Structure/Shape** gives that intervention zone its own geometry: a **corridor**, running from the archaic-symbol palimpsest to T001's NW edge (the T006 contact). A corridor is the most literal shape for something that has to travel from one point to another, which is exactly what Radiating requires.
- **Application/Edgeward**, read together with Structure, gives the corridor a direction: apply the new material starting at the palimpsest (the source) and working outward toward the NW edge (the destination) — matching the direction the Radiating pressure actually needs to travel, not the reverse.
- **Substance/Strange — user finding, retroactive:** rather than needing a brand-new material, Strange is already sitting on the tile — the actual fan-brush epoxy-glued to T001 since S001 is exactly "not normally map-material." This session adds to it rather than replacing it: a small tissue-paper wrap around the brush's stem, bristles still showing.
- **Treatment/Stained** is also already built into the plan: the tissue paper's translucency naturally behaves like residue or memory rather than a flat clean color, since it's meant to let the palimpsest underneath show through.
- **Opening/Closed** asks that the corridor's own coverage read as complete and settled, not left sparse or interrupted — this is a real, decisive event, not another deferred pressure. Any remaining incompleteness belongs to Inscription's own marks, not to this base layer.

**The corridor is named Dotti** — found embedded inside "Ehdotti" (from the AIKA book), the way a word can hide a smaller word inside itself. Fitting, given the corridor's whole job is partially exposing what's hidden inside something older.

**Revised scope, user decision:** the corridor runs along three consecutive edges, not just one — **S, SW (facing T004), and NW (facing T006)** — a continuous arc across T001's lower-left, read as a corridor or meadow rather than a single narrow path. This still satisfies Structure/Shape (one recognizable geometry) and Application/Edgeward (it still originates from edge contact, now three edges instead of one), just at a larger scale than first proposed.

Surface instruction, updated:

1. Leave the rest of T001's original S001 surface completely untouched (Ground: Divided) — this session's work is confined to Dotti.
2. Mark out Dotti as a corridor/meadow running along the S, SW, and NW edges, touching the archaic-symbol palimpsest along the way (Structure: Shape).
3. Wrap a small piece of tissue paper around the existing fan-brush's stem, bristles still visible — Substance/Strange made physical as an addition to what's already there, not a new import.
4. Cut the green tissue paper into strips; superglue the strip edges, and stain the paper itself lightly with CA glue to stiffen and harden it (Treatment: Stained, and Mirror's decayed-crackle quality built directly into the working material rather than kept as a separate reference).
5. Lay the strips across Dotti. Where strips don't touch, fill the gaps with marker work. The natural gaps between strips are the honest place for a sliver of the archaic text to still show through, since the strips themselves will likely read more opaque once hardened than a single soft sheet would have.
6. Where Dotti reaches the T006-facing NW edge, draw hexagons directly over the green paper — a deliberate visual echo of Shoreline's own hex convergence, giving Radiating a recognizable answer in T006's own visual language.
7. Apply metallic paint somewhere within Dotti — a tarnished, unearthed-reading accent, not a clean bright metallic finish.
8. If Inscription's own Force result allows it, let a little of the green bleed across the S/SW/NW edges into T004 and T006 themselves — kept small, not decided as mandatory yet.
9. Accept, without forcing a fix, that the archaic-symbol palimpsest will end up substantially covered by Dotti rather than cleanly revealed — a real tension against Pressure/Correction's demand, held rather than resolved.

This leaves Inscription with real, concrete work still to do: actually marking the crossing at the NW edge itself (the corridor reaches the edge, but nothing has crossed it yet), and deciding what, if anything, gets written on the blank Provision marker.

Actual Surface materials and layout:

- **CA glue on the tissue paper itself was abandoned** — brittle glue on thin paper without a stiff backing didn't work. Paper glue was used to adhere the tissue strips instead; the CA-glue-hardening idea for Treatment/Stained was dropped in favor of a different technique (below).
- Green marker scribbles were added directly to the surface within Dotti, partially covered by the tissue strips laid over them afterward — this layered peek-through does the job Treatment/Stained and the decayed-texture reference were originally reaching for, just via a different material than planned.
- Green tissue paper cut into strips, edges superglued (the CA glue worked fine for bonding strip edges to each other — it was specifically hardening the sheet itself that failed), then the strips glued down across Dotti with paper glue.
- Black pen used to draw Dotti's own boundary edges — a real, drawn Structure/Shape line, not just an implied zone.
- A "Dotti" text label physically glued onto the tile, naming the corridor directly rather than only in documentation.
- The fan-brush's stem was wrapped in a small piece of tissue paper, with a little of it left showing through the surrounding scribbles — bristles still visible, Substance/Strange built onto what was already there rather than importing something new.
- Metallic paint was not used — still a wishlist acquisition, specifically intended for the hexagons rather than general use.
- New echo hexagons were drawn near the T006-facing NW edge, over the green paper, alongside reinforcing the existing S006 silver hexagon mark where Dotti's tissue had covered it. Neither used metallic material this time; the silver treatment is deferred until the paint is acquired.
- Some tissue strips physically extend a little onto **both T004 and T006**, not just T006 — Radiating over-delivered relative to the minimum (one neighbor) the result required.
- Part of the "A" in the AIKA anchor text got covered by Dotti's material; a small yellow mark was added where it used to be, extending T001's own established Treatment (Stained: "yellow/orange hue behaves as residue... memory") to a new instance of exactly that.

Surface is complete. Pressure/Correction's Reveal demand did not resolve cleanly — between the still-covered archaic text and now a partially-covered AIKA letter, this session leans further toward "covered" than "revealed," acknowledged as a held tension rather than forced into a clean answer. Obligations carried into Inscription: the actual crossing at the NW edge (the tissue physically reaches T006, but nothing has been formally marked as crossing yet), the still-blank Provision marker, and the silver/metallic treatment for the echo hexagons once that material arrives.

Post-Surface note: clear coat applied to the tissue strips darkened them more than expected — accepted as fine, and if anything it pushes the color further toward sickly/decayed than the original bright green would have.

## Inscription

Numbers reused from Awakening: Green 3, Blue 5, Red 5 (C101, Green power leaf); Yellow 2, Brown 5, Black 1 (C100, Zombie). Fixed color mapping: Green = Scale, Blue = Form, Red = Behavior, Yellow = Relation, Brown = Force, Black = Residue.

Results:

- Scale / Green 3: Broad. A large part of the tile; field, zone, body, large structure, or strong feature.
- Form / Blue 5: Sign. Name, number, glyph, label, arrow, omen, icon, keyword, or written mark.
- Behavior / Red 5: Mutate. Bend, corrupt, transform, twist, misalign, hybridize.
- Relation / Yellow 2: Edge. One edge, seam, border, contact side, or opening.
- Force / Brown 5: Propagating (the plain result — no 6 appears anywhere in this draw, so the Force Matrix is not invoked). "It may affect 2–6 other tiles through route, region, shape, weather, or bleed logic."
- Residue / Black 1: Mark. The residue is a plain, permanent mark on the tile itself — a small trace with no larger claim than being visibly present.

Interpreting the six results together — this draw resolves almost everything Surface left open, cleanly:

- **Scale/Broad** simply confirms what's already true: Dotti already spans three edges, a genuinely large part of the tile. Nothing new required.
- **Relation/Edge** names exactly what's still unfinished from Surface: the NW edge, where Dotti physically reaches T006 but nothing has been formally marked as *crossing* yet.
- **Force/Propagating** retroactively validates what Surface already did rather than demanding something new: the effect isn't confined to one bridge or a single named neighbor — it spreads via route/region/bleed logic exactly the way the tissue actually behaved, reaching T004 and T006 both rather than staying confined to the one neighbor Cartography's Radiating obligation named.
- **Form/Sign** is the vehicle for finally answering Relation/Edge: this is the moment to inscribe Attunement's still-blank Provision marker with an actual word, and place it at the NW edge — the formal act of marking the crossing that Surface left undone.
- **Behavior/Mutate** governs how that mark should look and read: not settled or resolved (the way T007/Mesa's own Inscription landed on Settle), but actively transforming, twisted, not fully stable — consistent with Zombie/Burial-Cost being *invoked*, not *paid off*.
- **Residue/Mark** confirms the whole thing resolves into something modest and permanent: the inscribed marker itself, once placed, is the plain, small, lasting trace — not a new debt or a big unresolved claim.

**Proposed word for the marker: "RISEN."** It's the most literal possible answer to a Zombie-invoked Burial Cost — not paid, not settled, just awake and crossing. It also refuses Settle's finality, matching Mutate: something risen isn't done changing.

Inscription instruction:

1. Write "RISEN" on the previously-blank Provision marker.
2. Place it physically at Dotti's NW edge, where the corridor already meets T006 — the literal crossing point.
3. Let the mark itself (or the hex shapes nearest it) read as slightly warped or misaligned rather than clean, echoing Behavior/Mutate and T004's own precedent of a distorted hexagon.
4. No further material changes required elsewhere — Scale, Force/Propagating, and Residue are all already satisfied by what Surface built; name the actually-reached tiles (T004, T006) rather than leaving it as "nearby ones," per Propagating's own Effect.

This closes the loop Cartography opened: Activation invoked Burial Cost, Map Effect demanded something radiate to T006, and Inscription now gives that radiation its actual, permanent, physical word.

**Actual Inscription:**

- **Form/Sign, word chosen: "Amedda"** — not "RISEN" as proposed. Drawn from a *Star Wars* novel, chosen without an intended meaning attached. This still satisfies Form/Sign (a legible, discrete word) and arguably suits Behavior/Mutate even better than the original proposal: a name grafted on from entirely outside the tile's own vocabulary is its own kind of hybridization, unsettled rather than resolved. Placed at Dotti's NW edge, the T006 crossing point, as planned.
- **Sprout scribbles:** small branching marks were added spanning out from the green tissue strips, reading like little sprouts growing from the green area — an unplanned addition, but consistent with Behavior/Mutate (something still changing, not settled) and with Substance/Strange's material already being alive-feeling (the wrapped fan-brush).
- **Black warning-strip spread grew, but stays within T001:** the existing black warning-checker spread grew a little further toward the eastern/NE and north edges this session — negligibly in both directions. Correction: this stays entirely within T001 itself; it does not cross into T002 or T003. No change needed on either neighbor's own record.

Inscription is complete.

## Chronicle

Numbers reused from Awakening: Green 3, Blue 5, Red 5 (C101, Green power leaf); Yellow 2, Brown 5, Black 1 (C100, Zombie). Fixed color mapping: Green = Record, Blue = Witness, Red = Meaning, Yellow = Publication, Brown = Maintenance, Black = Seed.

Results:

- Record / Green 3: Change list. List what physically changed during the session. Include target tile and any other affected tiles.
- Witness / Blue 5: Archive object. Preserve a physical or digital object from the session.
- Meaning / Red 5: Myth/rumor. Write a more legendary, distorted, oral, symbolic, or unreliable version of what happened.
- Publication / Yellow 2: Website update. Update the map website, tile page, project page, gallery, index, or progress log.
- Maintenance / Brown 5: Physical maintenance. Repair, clean, flatten, glue, protect, label, sleeve, store, magnet-check, felt-check, or stabilize materials.
- Seed / Black 1: Keyword. A word, phrase, tag, motif, pressure, or concept may return later.

Interpreting the results:

- **Record (Change list):** T001 (target) — Cartography renamed the "bottom archaic-symbol area" to the archaic-symbol palimpsest and re-invoked K007 Burial Cost via Name Spoken; Surface and Inscription built the Dotti corridor along the S/SW/NW edges (green tissue strips, black-pen boundary, glued "Dotti" label, tissue-wrapped fan-brush stem, green marker scribbles, sprout scribbles, echo hexagons, reinforced S006 silver hexagon, a small yellow mark over the partly-covered "A" in AIKA); Inscription placed the marker word "Amedda" at Dotti's NW edge; the existing black warning-checker spread grew slightly toward the NE/N edges, staying entirely within T001. T004/Mirror and T006/Shoreline each received a little of Dotti's tissue-strip bleed — already cross-referenced on their own records during Surface. T002/Ring and T003/The Canyon were not affected this session (an earlier draft of this session's notes said otherwise; corrected).
- **Witness (Archive object):** a physical fragment from this session's central material — a small offcut of the green tissue paper used for Dotti — is the natural archive object. Left as a physical action for you to do when convenient: set the scrap aside, labeled "S008 / T001 Dotti tissue," in the material tray.
- **Meaning (Myth/rumor):** *They say AIKA never truly buried what it swallowed. In the season the corridor opened — the one they call Dotti, a word hidden inside a longer one meaning "suggested" — a name arrived that belonged to no local tongue: Amedda. No elder claims it; no card explains it. The old sentries at the northern and eastern borders stirred at its arrival, testing their own edges as if remembering how to reach further, though they did not yet dare cross. Some say Amedda is a visitor's name, spoken by accident and now stuck like a splinter. Others say it is the name the buried thing chooses for itself, now that it has finally been given a mouth to speak with.*
- **Publication (Website update):** `../../website-drafts/t001-aika-artifact.md` — the S001 artifact draft page for T001 — gets an S008 addendum documenting the revisit, so the page reflects the tile's current state rather than only its S001 birth. The user also made a small update to the live website directly, and scheduled posts — the actual publication side of this result, done independently of this draft.
- **Maintenance (Physical maintenance):** given this session's own note that clear coat darkened the tissue strips more than expected, and that CA glue was used to bond strip edges (though not the sheet itself), the fitting physical-maintenance action is to check the newly-worked Dotti material for anything that needs stabilizing: confirm the CA-glued strip edges are holding, and that the glued "Dotti" label isn't lifting at a corner. Left as a physical action for you to do and report back.
- **Seed (Keyword):** creating keyword **K035**, proposed name **"Amedda"** — the imported, deliberately meaningless word inscribed at Dotti's NW edge. Return condition: if the name Amedda appears again anywhere on the map, or when T001 or T006 is next targeted, decide whether it ever gains an in-world meaning or stays permanently foreign.

**Actual Chronicle:**

- **Witness (Archive object):** the green Dotti tissue-paper offcut is stored for future sessions, as proposed.
- **Maintenance (Physical maintenance):** clear coat was applied to all of this session's changes, protecting and stabilizing the new material (tissue strips, scribbles, Dotti label, Amedda marker) as a single pass rather than a targeted edge-check.

Chronicle's main draw is complete.

## Artifact Draw

Card drawn: C016 — Green 1, Blue 3, Red 4, Yellow 6, Brown 3, Black 5.

Brown 3 selects Maintenance row 3 directly from the main Chronicle table (not the Matrix, since Brown ≠ 6):

> **Rule/documentation note:** Write or revise a rule note, clarify a table, record an ambiguity, or update documentation.

Actual artifact: a new clarifying note added to `../../rules/map-creation-rules.md`'s Force section, "Confirming a Matrix trigger" — directly addressing this session's own Force-result mistake (Brown 5 misread as the Force Matrix trigger, when only a 6 calls it). The note states the general rule and the correction procedure (revert any TBD-cell fill made on a false matrix invocation) so the same mistake is easier to catch and fix cleanly if it recurs in a future session. Distinct from Chronicle's own Maintenance action (the physical clear-coat pass), so the two draws don't compete for the same ground.

Chronicle is complete for T001 / AIKA's S008 revisit: all six phases plus the Artifact Draw.
