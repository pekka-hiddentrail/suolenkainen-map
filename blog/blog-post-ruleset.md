# Blog Post Ruleset — Suolenkainen's Map Chronicle

A working style guide for turning session material into blog posts. Use this alongside the project's own rules/tile-data/session files — this document governs voice and structure, not map content.

## 1. Structure

Every post is divided into numbered chapters using roman numerals as H2 headings:

```
## I. Chapter Title
## II. Chapter Title
## III. Chapter Title
```

A typical session post runs 4–6 chapters. Chapter count and order should follow whatever shape the actual session material suggests — not a fixed template. Rough defaults if nothing else dictates it:

- **Opening chapter**: where things stood before this session; what was open, unresolved, or waiting.
- **Middle chapters**: the session itself — Awakening's cards and target, Cartography's map-state changes, Attunement's pressures, Surface and Inscription's physical work, in whatever grouping makes sense. Not every phase needs its own chapter; group phases that share a beat.
- **Closing chapter**: what's now true that wasn't before, and what remains open for next time.

## 2. The Two Voices

Each chapter has two parts, always in this order:

**A. The epigraph (storyteller voice)**
- Italicized, sits directly under the chapter heading, no attribution.
- 4–5 sentences.
- Written as if it comes from inside the map's own mythology — a fragment of lore, a rumor, an omen, a line that could be quoted back later once the map has enough history to make it true.
- Never explains the mechanics. Never names real-world materials, tools, or techniques. Never uses the internal rules vocabulary (keyword IDs, phase names, card-color names) directly — translate those into image and myth instead.
- Should feel slightly ahead of or behind the literal facts — foreshadowing, mourning, wondering — rather than a plain restatement of what the artist-voice paragraph is about to say.

**B. The body (artist voice)**
- Plain prose, grounded, first person.
- This is where the real facts live: what card came up, what the resulting numbers meant, what material got used, what got glued/cut/painted, what decision got made and why.
- Can reference the rules system directly by name (Awakening, Cartography, keyword numbers, etc.) when useful, but should still read as a person talking, not as a copy of the internal documentation.
- Uncertainty is allowed and often more honest than resolution — if something is genuinely unresolved in the actual project state, say so plainly rather than resolving it early for the sake of the post.

## 3. Source Discipline

- Only chronicle things that have actually happened, as recorded in the real session files (`suolenkainen-map.md`, `tile-data.md`, `open-obligations.md`, `map-todo.md`, `rules-delta.md`) or in notes/photos provided directly for that post.
- Demo or reference material used earlier in planning is not canon and must never be treated as something that happened.
- If a detail isn't confirmed anywhere, leave it as an open question in the artist-voice section rather than inventing it in the epigraph. The epigraph can gesture at mystery; it should never quietly manufacture false history.
- Internal documentation language (keyword IDs like "K027", phase jargon, matrix table names) belongs in the artist-voice section only, and even there, translated into readable prose rather than pasted as-is.

## 4. Tone Notes

- The two voices should feel like the same person choosing to speak two different ways, not two different narrators.
- Avoid resolving in the epigraph what the body hasn't earned yet — the myth can foreshadow, but the facts still have to arrive in the prose.
- Favor concrete, sensory detail (materials, textures, physical actions) in the artist voice over abstract commentary.
- Favor mystery, motion, and implication over exposition in the storyteller voice — it should read like something half-remembered, not a summary.

## 5. Naming & File Convention

- Filenames: `NN-slug-title.md`, sequential, e.g. `02-the-first-cards.md`.
- Post title in the file as a single H1 (`# Title`), followed directly by the first chapter.
- Keep each post self-contained enough to read without the previous ones, but feel free to reference earlier chapters/tiles/events by name once they exist.
