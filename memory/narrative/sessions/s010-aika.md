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