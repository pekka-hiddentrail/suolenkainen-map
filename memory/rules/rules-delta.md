# Rules Delta

Living notes for rule clarifications, contradictions, provisional rulings, and adopted rulings that have not yet been folded into `map-creation-rules.md`.

## Delta Candidate - Paired Card Numbers

Status: noticed during S001 Attunement; not yet interpreted or adopted.

Paired equal numbers across the two Awakening cards may have special meaning in a future rule. Examples include Green 5 with Blue 5, or Red 1 with Yellow 1. For now, equal pairs should be recorded when noticed, but they do not alter phase results until a later rule is written or adopted.

## Delta Candidate - Future Color Channel Rename

Status: planned by user after S001 Artifact Draw; not active yet.

The user intends to rename the Brown color channel to Orange and the Black color channel to Purple. This should not be applied in the current session or the next session, but should be prepared for adoption soon.

Until the change is explicitly adopted, all rules, logs, tables, and interpretations continue to use Brown and Black. When adopted, audit the rules, keyword list, session templates, and existing docs so the channel names are updated consistently without changing past draw meanings.

## Delta Candidate - Chronicle Task Audit

Status: requested after S001 Artifact Draw; future maintenance task.

Audit Chronicle tasks in a later session. The audit should check whether Chronicle and Artifact Draw outputs are practical, distinct, not overly redundant, and easy to complete as concrete artifacts. Do not perform the audit immediately unless the user explicitly asks for it.

## Adopted Delta - Brown Even Creates Last-Free New Tile

Status: adopted during S004 Awakening and folded into `map-creation-rules.md`. The rule itself still stands, but the S004/T004 worked example below was later found to rest on a walk-back error — see "Adopted Delta - Same-Sign Diagonal Walk-Back..." below for the correction.

When walk-back reaches an occupied coordinate and the Brown number is even, Brown still means that a new tile must be created. Do not stack a new tile on the occupied coordinate and do not convert the result into an existing-tile revisit.

Instead, the final target is the last empty coordinate in the walk-back path before the occupied coordinate.

S004 example (superseded — see correction below):

- Start from T003 at [1,-1].
- Raw target is [-4,-4].
- Walk-back path is [-4,-4] -> [-3,-3] -> [-2,-2] -> [-1,-1] -> [0,0].
- [0,0] is occupied by T001.
- Brown 4 is even, so a new tile is required.
- The last free coordinate before occupied [0,0] is [-1,-1].
- T004 appears at [-1,-1].

**Correction:** this walk-back path was wrong — it ticked both coordinates at once along a same-sign diagonal, which is not a real hex step (see the Same-Sign Diagonal entry below). Re-walked correctly, T004's Awakening never actually reaches occupied [0,0] at all — it touches the map one step earlier, at [-1,0]. So this example no longer demonstrates the last-free-coordinate mechanism in practice; it demonstrates the same-sign-diagonal error the next entry fixes. The rule above remains adopted for any future case where a walk-back genuinely lands on an occupied coordinate.

## Adopted Delta - S003 Inscription / Force / Seed Clarifications

Status: adopted into `map-creation-rules.md` after S003 Artifact Draw maintenance discussion.

Inscription table clarifications proposed:

- Scale 3 / Broad: A large part of the tile; field, zone, body, large structure, or strong feature.
- Form 2 / Thread: Line, route, road, river, border, seam, current, coastline, or crack.
- Behavior 2 / Spread: Grow, bleed, branch, multiply, expand, or continue.
- Relation 5 / Source: Card image, word, Attunement, Cartography, Surface, memory, omen, or archive.

Force matrix clarifications proposed:

- Reach 3 / On Neighbor: This tile reaches out to a neighbor to influence it.
- Mechanism 2 / Bleed: Whatever the tile holds on its edges continues as bleed to adjacent tile(s). The amount continued is measured in centimeters from the Red number; in S003 this is 2 cm.
- The third Force column is renamed from Collateral to Trace. Reach says how far the force goes; Mechanism says how it travels; Trace says what evidence or effect remains after it acts.
- S003 adopted ruling: when Force combines On Neighbor + Bleed + Marks edge/contact, the tile affects a neighbor by bleeding across an edge, and the crossing must leave visible evidence at the contact. The main feature does not always need to sit on the edge; a branch, extension, residue, echo, or stopped mark may carry the force to the contact.

Residue matrix clarifications proposed:

- Remainder 3 / Keyword: The residue affects a keyword representing this tile's general behavior or feature.
- Visibility 2 / Exposed: What is unfinished is left obvious and feels like it governs an area.
- Future Effect 2 / Must be answered: The residue remains mandatory the next time this tile is worked on.

Seed / todo clarification adopted:

- Seed creates a future-work item, not just a vague unresolved obligation.
- Seed items are either triggered todos, with a return condition, or unscheduled todos, which sit in the general todo list until Maintenance or the user chooses them.
- Chronicle Maintenance result 4 is now Todo list / future-work queue instead of Tile index update in the main Chronicle table.
- Maintenance can force queue processing: pick one todo item and complete, update, reschedule, assign a trigger, or move it into the next-session queue.

## Adopted Delta - Same-Sign Diagonal Walk-Back and North/South Tie-Break

Status: adopted during a post-S004 rules-maintenance review and folded into `map-creation-rules.md`.

The walk-back rule's own worked example only ever demonstrated the opposite-sign diagonal (e.g. [-4, 5] to [-1, 1]), where each coordinate tick is also a real single hex step (N or S). It never covered the same-sign diagonal (e.g. [-4, -4]), where a tile's six real sides are only N, NE, SE, S, SW, NW — there is no direct E or W step, so a [+1,+1] or [-1,-1] tick is not a real move at all. Walking that diagonal back requires alternating NE/SE (heading toward positive/east) or SW/NW (heading toward negative/west), and checking for map contact after every real step rather than after each two-coordinate tick.

This was discovered because S004's recorded walk-back for T004 followed the same-sign diagonal tick-by-tick ([-4,-4] -> [-3,-3] -> [-2,-2] -> [-1,-1] -> [0,0]) without ever taking a real hex step, and stopped one step too late: [-1,-1] does not actually touch any existing tile. Re-walking with real NE/SE steps reaches map contact one step earlier, at a tie between [-1,0] (T001's SW neighbor) and [0,-1] (T001's NW neighbor) — both 7 real steps out, differing only in whether the deciding extra step was NE-side or SE-side.

Adopted tie-break: when a same-sign-diagonal walk-back ties between a north-side contact point (extra NE or NW step) and a south-side contact point (extra SE or SW step), the black card number decides — odd goes north-bound, even goes south-bound. For T004, Black 6 is even, so the tie resolves south-bound: T004's corrected final target is [-1,0], not [-1,-1]. All T004 records, the coordinate map, and the map diagram have been corrected to [-1,0] accordingly.

## Adopted Delta - Keyword Recurrence Rule

Status: adopted during a keyword/tag audit and folded into `keyword-list.md`.

Checked how many times each of the 31 keyword IDs then in `keyword-list.md` (K001-K031) was actually referenced anywhere in the whole memory tree, outside its own bookkeeping (its own definition row, its own tile record's Keywords field, its own tile-data.md row). 26 of them appeared in exactly those 3 places and nowhere else — never referenced from another tile, another session, or any obligation. Only 5 recurred: K003 (Region-Tangled) and K007 (Burial Cost), each independently drawn by two different tiles, and K016 (Ring), K024 (Star-Canyon Grid), K025 (The Canyon), each created by Chronicle's Seed mechanism as an explicit future return condition.

Adopted rule: a result earns a keyword ID only when a second tile independently draws the same result, or Chronicle's Seed mechanism creates it as a return condition on creation. A one-off Cartography result that belongs to exactly one tile and isn't a Seed return condition stays a plain tag on that tile's own record instead.

Applied retroactively: K001, K002, K004-K006, K008-K015, K017-K023, and K026-K031 were removed from `keyword-list.md`. Nothing was lost — every one was already present as a plain tag on its own tile's record. Retired IDs are not reused or renumbered; the next new keyword continues from K032.
