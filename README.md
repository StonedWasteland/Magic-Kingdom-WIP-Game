# Magic Kingdom Game

*Folder working name. In-doc title is currently "Magic Worlds" — final title TBD.*

A browser-based, text-driven tactical party RPG. Command a four-character squad of "Gifted"
on energy-gated expeditions against a slow-burn invasion (the Sundering). Blends XCOM's doom
clock, Darkest Dungeon's expedition loop, Torn's text-first browser presentation, and
Worm-grade idiosyncratic powers.

## Status

**Pre-production / design.** No code yet. Current work: designing the power system bottom-up.

## How this folder is organized

```
Magic Kingdom Game/
├── README.md                     ← you are here (orientation + index)
├── DESIGN.md                     ← master design document (the source of truth)
└── docs/
    └── powers/
        ├── _format-and-tags.md   ← power spec format + the MASTER TAG DICTIONARY
        ├── 01-pyrokinesis.md
        ├── 02-cement-control.md
        └── 03-super-strength.md
```

When we scaffold actual code, the `client/ server/ shared/ content/` structure from
`DESIGN.md` §12 gets added alongside these. Note the distinction the doc draws:
- `docs/powers/` = **design** docs (prose, the thinking) ← what we're writing now
- `content/powers/` = **data** files (JSON/YAML the engine loads) ← comes later

## The design approach (why powers come first)

We're designing the power system **bottom-up**: write concrete, fully-specified powers first
and let the **tag vocabulary emerge** from real cases. That emergent tag dictionary *is* the
Power System spec `DESIGN.md` keeps deferring — we get the hard system as a byproduct of
designing fun things.

**The one engine idea:** everything is a tag reading other tags. Damage types, statuses,
enemy traits, and zone properties are all tags. An Expression is a function: *given the tags
in scope (target, zone, allies), produce an effect.* Combos and resistances aren't
special-cased — they're tags noticing each other.

## The starter roster (5 powers)

A deliberately coherent starting squad with full role coverage:

| Power | Domain | Role | Status |
|-------|--------|------|--------|
| Pyrokinesis | Elemental | Artillery / AoE | ✅ designed |
| Cement Control | Material | Controller / terrain | ✅ designed |
| Super Strength | Physical | Melee striker | ✅ designed |
| Metal Skin | Morph | Tank / frontline | ⬜ next |
| Regeneration | Biological | Sustain / medic | ⬜ todo |

**Deferred for a later batch:** Probability Pull (luck/conceptual), Blink (spatial).

## Open taxonomy note

The roster introduced two domains not in `DESIGN.md` §5: **Morph** (form-alteration) and a
**Physical / Biological split** (raw body output vs. life processes). §5's domain list needs
updating to match.
