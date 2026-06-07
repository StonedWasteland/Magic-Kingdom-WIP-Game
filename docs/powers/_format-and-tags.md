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
- **Metabolize** (Regeneration) — Strain-cheap; the real cost is **time/tempo** against the doom
  clock. Countered by *out-burst* (kill faster than it ticks) and *heal-suppression* tags.

Plus four cross-cutting systems:
- **Strain** (capped by Resolve) → **Backlash** when exceeded. Universal.
- **Forced movement** (`Knockback`, `Launch`, range-collapse) — the positioning layer over range bands.
- **Stances / modes** (Metal Skin) — a power can put the character into a persistent state tag
  (e.g. `Stance:Metal`) that modifies all their actions and incoming effects until toggled off.
  Stances can be **double-edged**: one toggle applies both buff tags (`Armored`) and
  vulnerability tags (`Conductive`, `Heavy`). Upkeep is a per-turn Strain drain.
- **Signed DoTs / heal-over-time** (Regeneration) — a periodic effect carries a *sign*. `Burning`
  ticks damage; `Regenerating` ticks it back. No special heal path — the engine reuses the DoT
  machinery (duration, stacking, suppression) for healing for free. Heal-suppression tags
  (`Cauterized`, `Corroded`) simply zero out positive ticks in scope.

## Master tag dictionary

Tags are grouped by category. `*` marks a tag referenced by a designed power but "owned"
(fully defined) by a power not yet written.

### Damage types
`Fire` · `Crushing` · `Slashing` · `Piercing` · `Acid`* · `Lightning`*

### Statuses & DoTs
`Burning` · `Bleeding` · `Frozen`* · `Chilled`* · `Slowed` · `Rooted` · `Suppressed` ·
`Staggered` · `Knockback` · `Corroded`* · `Injury` · `Shocked`* · `Guarded` · `Conductive` ·
`No-Bleed` · `Regenerating` *(first heal-over-time — a signed DoT)* · `Cauterized` ·
`Grievous` · `Exhausted` · `Downed` · `Toxic`

### Stances / modes
`Stance:Metal` *(first stance tag — double-edged; see Stances system above)*

### Target / body states
`Oiled` · `Wet` · `Doused` · `Flammable` · `Anchored` · `Heavy`

### Position & defense
`Cover` · `Armored` · `Entrenched` · `Destructible Terrain` · `Sealed`

### Zone tags
`On-Fire` · `Water Source` · `Rain` · `Open Sky` · `Enclosed` · `Plant-Rich` ·
`Metal Structures` · `Gas` · `Cement Source` · `Rubble` · `Concrete` · `Urban` · `Chasm` ·
`Flooding` · `Warehouse` · `Featureless` · `Unstable` · `Fragile` · `Submerged` ·
`Collapse` · `Barred` · `Locked` · `Electrified`* · `Hazard`

### Objects (for scavenge/throw)
`Object` · `Mass` · `Car` · `Lamppost` · `Debris`

### Mechanical / intrinsic
`Generative` · `Ranged` · `Area-Capable` · `Combo-Igniter` · `Sustained` · `Hazard` ·
`Carry-Gated` · `Material:Cement` · `Charge` · `Encumbrance` · `Control` · `Terrain-Shaper` ·
`Physical` · `Melee` · `Object-Wielder` · `Range-Collapser` · `Armor-Pierce` · `No-Material` ·
`Morph` · `Stance-Based` · `Metal` · `Biological` · `Self-Sustain` · `Metabolize`

## Combo chains confirmed (cross-power)

- **Cement → Pyro:** `Rooted` enemy + `On-Fire` zone (Conflagration) = can't flee, cooks.
- **Strength → Pyro:** thrown `Oiled` object ignites mid-air; throw enemy *into* `On-Fire`.
- **Strength → field:** `Knockback` breaks enemy Engaged combos; ground-slam makes `Rubble`
  (feeds Cement scavenge) and `Unstable` footing (feeds Pyro).
- **Water (future) ↔ Pyro:** `Wet`/`Doused` cancels `Burning` (party-comp tension), but
  `Wet` makes Cement set faster (synergy). Same tag, opposite effects — the engine handles it
  with no special-casing.
- **Metal Skin → squad:** `Guarded`/`Cover` lets Pyro & Cement operate from safety; pairs with
  Strength (one holds, one throws) and Cement (double-wall + seal a chokepoint).
- **Pyro ↔ Metal Skin (tension):** `Fire` + `Conductive` in the same scope = friendly burn on a
  metal-skinned ally. Same shape as fire/water — coordinate or cook your tank.
- **Lightning (future) → Metal Skin:** `Conductive` makes `Lightning`/`Shocked` the tank's hard
  counter. Pure emergent counterplay from one shared tag.
- **Regeneration → frontline:** sustain only pays off behind a soak — `Guarded` (Metal Skin) or
  `Cover` (Strength) buys the turns the HoT needs. Revive (`Downed` → up) refills the line.
- **Pyro ↔ Regeneration (tension, free from the engine):** `Fire`/`Burning` reads as `Cauterized`
  and **suppresses `Regenerating`** — same shape as Pyro↔Metal Skin. The kicker: Forge-Heart
  cauterizing an ally's `Bleeding` *also* shuts off that ally's regen. The medic-fire dilemma.
- **Acid (future) → Regeneration:** `Corroded` outpaces the tick — rot is the regenerator's hard
  counter, mirroring how `Acid` already eats Cement and Metal Skin. One tag, three victims.
- **Strength/Rend → bleed economy:** `Bleeding` (now owned by Regeneration) is an attrition tag —
  a regenerator wins any bleed war it starts, since it heals the same DoT it inflicts.
