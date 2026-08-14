# Suolenkainen's Map

A physical hex-tile map, built one tile and one session at a time. Each session draws two cards, reads six colored numbers off them, and lets those numbers run through a six-phase ritual — Awakening, Cartography, Attunement, Surface, Inscription, Chronicle — that decides where the map grows next and what happens there. The process is chronicled in public as it happens.

## Current status

4 tiles exist so far:

| Tile | Name | Coordinate | Status |
| --- | --- | --- | --- |
| T001 | AIKA | [0,0] | Complete (S001) |
| T002 | Ring | [1,0] | Complete (S002) |
| T003 | The Canyon | [1,-1] | Complete (S003) |
| T004 | *(unnamed)* | [-1,-1] | In progress (S004) — Cartography done; Attunement, Surface, Inscription, and Chronicle still open |

15 blog posts have been published narrating S001–S003 (`blog/blog-01-here-it-starts.md` through `blog-16-a-ring-is-named-and-a-session-ends.md`).

Next up per `memory/tracking/map-todo.md`: S004 Attunement — identify the neighbor condition holding T004, and confirm its physical edge placement before Surface.

## Repository layout

- **`blog/`** — public-facing session posts, plus `blog-post-ruleset.md`, the style guide for writing them.
- **`memory/`** — the project's continuity/working-memory files, split by role:
  - `rules/` — the stable rulebook (`map-creation-rules-v1.md`), pending clarifications (`rules-delta.md`), a practical how-to-apply-the-rules companion (`prompt-interpretation-notes.md`), and one superseded audit note. Several of the rulebook's secondary interpretation matrices (Surface's and Inscription's) are still placeholder `TBD` cells — they get filled in one cell at a time as a session's cards actually land on them.
  - `tiles/` — the tile index (`tile-data.md`), coordinate reference (`coordinate-map.md`), keyword index (`keyword-list.md`), and one detail record per tile in `records/`.
  - `narrative/` — general lore/cosmology (`lore.md`) and the session log, split one file per session in `sessions/`.
  - `tracking/` — the active todo queue (`map-todo.md`) and the open-obligations ledger (`open-obligations.md`).
  - `website-drafts/` — publish-ready per-tile page drafts produced by the Artifact Draw phase.
  - `cards/Cards.csv` — the card-deck data referenced by ID (C001, C002, ...) throughout session logs.

## Where to start

- Instructions for Claude (what to do first, what to do next, and where to document each step): [`CLAUDE.md`](CLAUDE.md)
- Rules: [`memory/rules/map-creation-rules-v1.md`](memory/rules/map-creation-rules-v1.md)
- What's next: [`memory/tracking/map-todo.md`](memory/tracking/map-todo.md)
- Open threads: [`memory/tracking/open-obligations.md`](memory/tracking/open-obligations.md)
- Session history: [`memory/narrative/suolenkainen-map.md`](memory/narrative/suolenkainen-map.md)
