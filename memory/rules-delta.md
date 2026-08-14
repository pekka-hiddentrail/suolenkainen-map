# Rules Delta

Living notes for rule clarifications, contradictions, provisional rulings, and adopted rulings that have not yet been folded into `map-creation-rules-v1.md`.

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

Status: adopted during S004 Awakening and folded into `map-creation-rules-v1.md`.

When walk-back reaches an occupied coordinate and the Brown number is even, Brown still means that a new tile must be created. Do not stack a new tile on the occupied coordinate and do not convert the result into an existing-tile revisit.

Instead, the final target is the last empty coordinate in the walk-back path before the occupied coordinate.

S004 example:

- Start from T003 at [1,-1].
- Raw target is [-4,-4].
- Walk-back path is [-4,-4] -> [-3,-3] -> [-2,-2] -> [-1,-1] -> [0,0].
- [0,0] is occupied by T001.
- Brown 4 is even, so a new tile is required.
- The last free coordinate before occupied [0,0] is [-1,-1].
- T004 appears at [-1,-1].

## Adopted Delta - S003 Inscription / Force / Seed Clarifications

Status: adopted into `map-creation-rules-v1.md` after S003 Artifact Draw maintenance discussion.

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
