# Power Spec Format & Master Tag Dictionary

This file does double duty: it defines the **format** every power doc follows, and it
maintains the **master tag dictionary** — the union of every tag minted by a designed power.
As the roster grows, this dictionary becomes the de facto Power System spec.

## Spec format

Each power doc contains, in order:

1. **Identity** — the fantasy in one line.
2. **Domain / Specificity / Material** — taxonomy + whether it needs a carried medium.
3. **Intrinsic tags** — what the engine "sees" the power as.
4. **Expressions** — exactly five: **Offense / Defense / Utility / Support / Signature**.
   Each has prose, mechanics, cost, and an unlock condition.
5. **Material rules** — carry/resource model (or "none").
6. **Combos** — *sets up* (tags it applies), *pays off* (setups it exploits), *cancelled by*.
7. **Environment** — zones it loves / hates.
8. **Strain profile** — what's cheap, what's expensive, what gates it.
9. **Tags minted** — every new tag this power adds to the dictionary below.

## Resource models discovered so far

The engine already supports three distinct ways a power is "fuelled" — an emergent strength:

- **Generate** (Pyrokinesis) — Strain-only. Never runs dry; countered by *denial* (environment).
- **Carry** (Cement) — Strain **+ Charges** (a carried reserve). Countered by *running out*.
- **Scavenge** (Super Strength) — Strain + zone `Object`s as ammo. Countered by *bare rooms*.

Plus two cross-cutting systems:
- **Strain** (capped by Resolve) → **Backlash** when exceeded. Universal.
- **Forced movement** (`Knockback`, `Launch`, range-collapse) — the positioning layer over range bands.

## Master tag dictionary

Tags are grouped by category. `*` marks a tag referenced by a designed power but "owned"
(fully defined) by a power not yet written.

### Damage types
`Fire` · `Crushing` · `Acid`*

### Statuses & DoTs
`Burning` · `Bleeding`* · `Frozen`* · `Chilled`* · `Slowed` · `Rooted` · `Suppressed` ·
`Staggered` · `Knockback` · `Corroded`* · `Injury`

### Target / body states
`Oiled` · `Wet` · `Doused` · `Flammable` · `Anchored`

### Position & defense
`Cover` · `Armored` · `Entrenched` · `Destructible Terrain` · `Sealed`

### Zone tags
`On-Fire` · `Water Source` · `Rain` · `Open Sky` · `Enclosed` · `Plant-Rich` ·
`Metal Structures` · `Gas` · `Cement Source` · `Rubble` · `Concrete` · `Urban` · `Chasm` ·
`Flooding` · `Warehouse` · `Featureless` · `Unstable` · `Fragile` · `Submerged` ·
`Collapse` · `Barred` · `Locked`

### Objects (for scavenge/throw)
`Object` · `Mass` · `Car` · `Lamppost` · `Debris`

### Mechanical / intrinsic
`Generative` · `Ranged` · `Area-Capable` · `Combo-Igniter` · `Sustained` · `Hazard` ·
`Carry-Gated` · `Material:Cement` · `Charge` · `Encumbrance` · `Control` · `Terrain-Shaper` ·
`Physical` · `Melee` · `Object-Wielder` · `Range-Collapser` · `Armor-Pierce` · `No-Material`

## Combo chains confirmed (cross-power)

- **Cement → Pyro:** `Rooted` enemy + `On-Fire` zone (Conflagration) = can't flee, cooks.
- **Strength → Pyro:** thrown `Oiled` object ignites mid-air; throw enemy *into* `On-Fire`.
- **Strength → field:** `Knockback` breaks enemy Engaged combos; ground-slam makes `Rubble`
  (feeds Cement scavenge) and `Unstable` footing (feeds Pyro).
- **Water (future) ↔ Pyro:** `Wet`/`Doused` cancels `Burning` (party-comp tension), but
  `Wet` makes Cement set faster (synergy). Same tag, opposite effects — the engine handles it
  with no special-casing.
