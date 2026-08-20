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
