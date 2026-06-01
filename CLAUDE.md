# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this project is

**Magic Kingdom Game** (folder name; in-doc working title "Magic Worlds" — final title TBD).
A browser-based, text-driven tactical party RPG. The player commands a four-character squad of
"Gifted" — people born with bespoke magical powers — on energy-gated expeditions against a
slow-burn invasion from beyond reality (the Sundering). It blends XCOM's doom-clock squad
combat, Darkest Dungeon's expedition/recovery loop, Torn's text-first browser presentation,
and Worm-grade idiosyncratic powers where creativity beats raw force.

Unrelated to the TES/TEEM/TECH "Torn Elephant" family — this is an original game, not a Torn
tool. (Those are listed under Related projects only because they share a developer and
workspace conventions.)

`DESIGN.md` is the master design document and source of truth. Read it first.

## Current status

**Pre-production / design.** No application code yet. Active work: designing the power system
**bottom-up** — writing concrete, fully-specified powers and letting the tag vocabulary emerge
from real cases. See `README.md` for the live roster and status.

## Development workflow

While in design phase:
1. Edit `DESIGN.md` (master) and the docs under `docs/`.
2. Each power is one doc in `docs/powers/`, following the format in
   `docs/powers/_format-and-tags.md`.
3. After designing a power, update the **master tag dictionary** in `_format-and-tags.md` with
   any tags it minted. That file is the de facto Power System spec.

Once code is scaffolded, this section gets the build/run/test commands.

## Architecture

### Now (design docs)
```
Magic Kingdom Game/
├── DESIGN.md                 master design document
├── README.md                 orientation + roster index + status
└── docs/powers/              power design docs (prose) + master tag dictionary
```

### Later (from DESIGN.md §12 — do NOT pre-scaffold)
- **Frontend:** React + TypeScript + Tailwind
- **Backend:** Node (Express/Fastify) + TypeScript, server-authoritative combat
- **Data:** PostgreSQL + Redis
- Code layout: `client/ server/ shared/ content/` added alongside `docs/`.

**Key distinction:** `docs/powers/` holds **design** docs (prose, the thinking).
`content/powers/` (future) holds **data** files (JSON/YAML the engine loads). Don't conflate
them.

## Core design principles (from DESIGN.md)

- **Powers as tagged effects.** Everything is a tag reading other tags — damage types,
  statuses, enemy traits, zone properties are all tags. An Expression is a function from
  in-scope tags to an effect. Combos and resistances are tags noticing each other, never
  special-cased. This is the single most important architectural commitment.
- **Content as data.** Powers, enemies, expeditions, items live in data files, not code.
  Adding content shouldn't require code changes.
- **Combat log as prose.** The text output IS the game; combat resolution produces a readable
  narrative, not a stat dump.
- **Horizontal > vertical.** A new expression should feel as good as +5 to a stat.
- **No permadeath.** Defeat = Downed, with time-gated recovery penalties.

## Important constraints

- Design is not locked — `DESIGN.md` §14 lists open questions (tone, era, energy economy,
  squad size, monetization). Flag when a design decision depends on one of these.
- Don't pre-scaffold the full §12 stack while still in design phase. Build the engine out of
  concrete, designed cases first.
- Keep the master tag dictionary in sync with the per-power docs.

## Related projects (shared developer / workspace conventions, not shared code)

- **TES** — Torn's Elephant Solitaire, sibling workspace in the same `Dev/` folder.
- **TEEM** — Torn Elephant Economy Manager (market intel userscript).
- **TECH** — Torn Elephant Combat Helper (combat intel userscript).
