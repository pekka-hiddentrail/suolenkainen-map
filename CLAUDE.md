# Instructions for Claude

This repo tracks Suolenkainen's Map, a physical hex-tile map built one session at a time by drawing cards and running the results through a six-phase ritual. Full rules live in `memory/rules/`; this file is only about *what to do, in order, and where to write it down*.

## Before doing anything

Read, in this order:

1. `memory/tracking/map-todo.md` — Next-Session Queue and any Triggered todos that match the current target tile.
2. `memory/tracking/open-obligations.md` — unresolved debts for the current target tile.
3. `memory/tiles/tile-data.md` (Tile Index) and the target tile's file in `memory/tiles/records/` — current status, keywords, unresolved items.
4. `memory/rules/map-creation-rules.md` — the phase you're about to run — plus `memory/rules/rules-delta.md` for clarifications not yet folded into the main rules, and `memory/rules/prompt-interpretation-notes.md` if a prompt result is unclear.

Then create the session file: `memory/narrative/sessions/sNNN-slug.md` (slug = the tile's name once known, e.g. `s002-ring.md`; use the tile ID if it has no name yet, e.g. `s004-t004.md`). Add a link to it from `memory/narrative/suolenkainen-map.md`.

## The six phases

For each phase, write results into the session file under a `## PhaseName` heading, in this order, then do the listed follow-up writes.

| # | Phase | What happens | Also update |
| --- | --- | --- | --- |
| 1 | **Awakening** | Draw two cards, read the six colored numbers, calculate the target coordinate, walk it back to the map if empty, decide new tile vs existing tile. | Nothing yet — this is the session file's first section. |
| 2 | **Cartography** | New tile: answer the six birth questions (Origin, Tether, Entanglement, Temper, Office, Inheritance). Existing tile: answer the six adjustment questions instead. | Tile's summary row in `memory/tiles/tile-data.md`; tile's full record in `memory/tiles/records/`. If it's a brand-new tile, add both. |
| 3 | **Attunement** | Read the Cartography state, produce the six-result story and a concrete todo list. | Nothing outside the session file — this todo list is session-scoped prep, not the persistent queue. |
| 4 | **Surface** | Physical foundation work; record the instruction, then the actual materials once done. | Tile record's Surface fields in `memory/tiles/records/`. |
| 5 | **Inscription** | Marks and meaning; record the instruction, then the actual inscription once done. | Tile record's Inscription fields; new keywords added to `memory/tiles/keyword-list.md`. |
| 6 | **Chronicle** | Final session log, future obligations, and — if triggered — an Artifact Draw. | See below. |

### Chronicle also means:

- Copy this session's "Future obligations" into `memory/tracking/open-obligations.md`, under that tile's section.
- If Seed produced a future-work item, add it to `memory/tracking/map-todo.md` (Triggered if it has a return condition, Unscheduled if not).
- If a rule was clarified or adopted, record it in `memory/rules/rules-delta.md` (and fold it into `memory/rules/map-creation-rules.md` once it's stable).
- If Artifact Draw was triggered, add `## Artifact Draw` to the session file and, if it produces a publish-ready page, write that to `memory/website-drafts/`.
- If a new tile or coordinate was placed, sync `memory/tiles/coordinate-map.md`, the Tile Index in `memory/tiles/tile-data.md`, and the ASCII layout in `memory/tiles/map-diagram.md`.

## Creating new files

### New session file

Path: `memory/narrative/sessions/sNNN-slug.md` (slug = the tile's name once known, e.g. `s002-ring.md`; use the tile ID alone if it has no name yet, e.g. `s004-t004.md`).

Structure — one `##` heading per phase, in order, only for phases actually run so far:

```
# SNNN — TNNN · Tile Name

## Awakening
...

## Cartography
...

## Attunement
...

## Surface
...

## Inscription
...

## Chronicle
...

## Artifact Draw
(only if Chronicle's Seed/Maintenance result triggers one)

## Maintenance Addendum
(only if end-of-session rule/documentation maintenance is done as a separate step, as in S003)
```

Drop the "SNNN - " prefix from each phase heading — the session number is already in the H1 and the filename. Add a link to the new file under Sessions in `memory/narrative/suolenkainen-map.md`.

### New tile record

Path: `memory/tiles/records/tNNN-slug.md` (slug = the tile's name once known, e.g. `t002-ring.md`; use the tile ID alone if unnamed, e.g. `t004.md`).

This is a single `| Field | Value |` table that grows one field at a time as phases complete — a record after S002 (2 phases run) looks different from one after S004's Chronicle (all 6 run). It is not a fixed template. Start it when Cartography first creates the tile, with:

- `Tile ID`, `Name`, `Coordinate`, `Layer / stack`, `Current phase`, `Current map-object identity`, `General description`, `Neighbor tiles`
- One field per Cartography result: `Cartography origin`, `Cartography tether`, `Cartography entanglement`, `Cartography temper`, `Cartography office`, `Cartography inheritance`
- If the Awakening calculation was non-trivial (walk-back, adjustment), also record it: `Awakening cards`, `Awakening calculation`, `Coordinate-to-physical direction`, `Awakening notes`

(T001's record predates this per-field convention and folds Cartography's results into `General description` instead of separate fields — use T002–T004 as the reference shape, not T001.)

As each later phase completes, add its fields the same way — `<Phase> <result name>` per result (e.g. `Surface ground`, `Inscription scale`) — plus one `Actual <phase>` field once the physical work is done, and one `Chronicle <result name>` field per Chronicle result.

Always keep these last, and update them every phase: `Omen sources`, `Active token`, `Keywords`, `Tags`, `Unresolved`, `Last updated by session`.

Also add or update the tile's row in the Tile Index table in `memory/tiles/tile-data.md`.

### Filling in a TBD matrix cell

Several second-tier matrices in `memory/rules/map-creation-rules.md` (Surface's Ground/Substance/Application/Treatment/Structure/Opening; Inscription's Scale/Form/Behavior/Relation/Force/Residue) are still mostly placeholder `TBD` cells — they get filled in one cell at a time, only when a real session's card numbers actually land on that cell. Chronicle's six sub-matrices are already fully written and need no further filling.

When a session hits a `TBD` cell:

1. Write the real interpretation directly into that cell in `map-creation-rules.md`, replacing `TBD`. Keep it generic and reusable — phrased the same way as the filled-in cells already next to it, not tied to this session's specific tile or cards.
2. If the concrete worked example is worth preserving beyond this one session, add it to `memory/rules/prompt-interpretation-notes.md`'s session-specific interpretive notes instead of folding it into the rules cell itself — don't duplicate the generic gloss there, just the example.
3. Continue writing the session's actual result into the session file as normal; the matrix-cell fill is in addition to that, not instead of it.

A whole-column rename (like the Force matrix's third column already being renamed from Collateral to Trace) is a bigger edit than a single cell: record it in `memory/rules/rules-delta.md` first, then fold it into `map-creation-rules.md` once adopted, per the normal rules-delta flow above.

### New blog post

Path: `blog/blog-NN-slug.md`, continuing the highest existing number in `blog/`. Blog posts aren't automatic per session — write one only when asked. Follow `blog/blog-post-ruleset.md` in full for structure and the two-voice format; that file is the complete spec, this is just the pointer to it.

## After the session

- If a blog post is wanted, write it per "New blog post" above.
- Update `README.md`'s status table if a tile's status or the current next-step changed.

## Other things this system supports

Beyond running phases and creating the files above, Claude can also be asked to:

- **Answer questions about current state** — "what's still open on T002?", "what's next?", "what keywords are active on T003?" — read from `memory/tracking/open-obligations.md`, `memory/tracking/map-todo.md`, `memory/tiles/tile-data.md` / `memory/tiles/records/`, and `memory/tiles/keyword-list.md`. No file needs to change for this.
- **Explain past decisions** — e.g. "why is T004 at [-1,-1]?" — reconstruct the reasoning from the relevant file in `memory/narrative/sessions/`, which has the full calculation trail.
- **Sanity-check a proposed move** — walk a card draw through the Awakening logic in `memory/rules/map-creation-rules.md` before it's acted on physically.
- **Manage the card deck** (`memory/narrative/cards/Cards.csv`) — look up a card by ID, log which cards get drawn each session, note physical alterations to a card (e.g. a glued-on image, as C074 got in S003), or help with deck maintenance/reset during a Maintenance result.
- **Translate a phase result into a physical to-do** — turn an abstract Surface/Inscription result into concrete "what to do with your hands and materials next," per the Surface/Inscription interpretation rules in `memory/rules/prompt-interpretation-notes.md`.
- **Check continuity across tiles** — when working one tile, check whether it answers, complicates, or merely witnesses another tile's still-open return condition; see each tile's `Unresolved` field in `memory/tiles/records/`.
- **Process the todo queue during a Maintenance result** — pick one item from `memory/tracking/map-todo.md` and complete, update, reschedule, retrigger, or move it into the next-session queue, per the Seed Matrix rule in `map-creation-rules.md`.
- **Do a documentation audit** — periodically check for stale cross-references, orphaned files, duplicated content (like the coordinate-table and gloss duplication already found and fixed), or gaps (like the missing `blog-02`).
- **Draft social captions** — shareable copy (e.g. Instagram descriptions) tied to a specific tile's photo, as part of or after its Artifact Draw / Publication result.
- **Lore and creative brainstorming** — answer or explore the Open Lore Questions in `memory/narrative/lore.md`, staying inside its "record absence, don't invent canon" discipline: mark anything not user-confirmed as provisional.

Known pending rule-maintenance tasks (already queued, not hypothetical):

- Audit whether Chronicle's Record/Witness/Meaning/Publication/Maintenance/Seed results are overlapping or impractical (flagged in `memory/rules/rules-delta.md`).
- Adopt the planned Brown→Orange, Black→Purple color-channel rename once the user decides — must touch `map-creation-rules.md`, `keyword-list.md`, and every past reference consistently, not just the rulebook.

Latent, not yet built: the rules assume "for every map tile, there is a web page." `memory/website-drafts/` is markdown, not a live site — turning it into one is a real possible future use, just not started.
