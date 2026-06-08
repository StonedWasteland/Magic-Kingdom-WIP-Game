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
- **Gamble** (Probability Pull) — no fuel, no medium: draw a fresh `Fortune` hand each battle +
  spend a `Luck` meter to steer it. The cost is **variance you manage**; pressing your luck burns
  *tempo* when it backfires. Countered by *determinism* (`Sealed Fate`, fixed-fate enemies).

Plus five cross-cutting systems:
- **Strain** (capped by Resolve) → **Backlash** when exceeded. Universal.
- **Forced movement** (`Knockback`/`Launch` = *away*, `Pull` = *toward*, range-collapse) — the
  positioning layer over range bands. Atlas pushes; Gravity Anchor pulls; both just move a unit a
  band. Resisted by `Anchored`.
- **Stances / modes** (Metal Skin) — a power can put the character into a persistent state tag
  (e.g. `Stance:Metal`) that modifies all their actions and incoming effects until toggled off.
  Stances can be **double-edged**: one toggle applies both buff tags (`Armored`) and
  vulnerability tags (`Conductive`, `Heavy`). Upkeep is a per-turn Strain drain.
- **Signed DoTs / heal-over-time** (Regeneration) — a periodic effect carries a *sign*. `Burning`
  ticks damage; `Regenerating` ticks it back. No special heal path — the engine reuses the DoT
  machinery (duration, stacking, suppression) for healing for free. Heal-suppression tags
  (`Cauterized`, `Corroded`) simply zero out positive ticks in scope.
- **The Draw / rolled kit** (Probability Pull) — a power's kit need not be fixed. The engine
  generalizes "kit" from a static list of Expressions into a **distribution sampled per
  encounter**: at battle start you draw a hand of `Fortune` effects from a pool. Powers become
  data you can draw from. Design invariant: **no dead entries** — every drawable Fortune is
  viable, so variance is *direction*, never *quality*. Anti-luck (`Sealed Fate`) suppresses the
  draw the way heal-suppression zeroes a HoT.
- **Spreading zones** (Overgrowth) — a zone tag need not be static. Most zones (`On-Fire`,
  `Gravity Well`) sit where placed and tick down; an `Overgrown` zone carries a **growth rule** and
  **propagates to an adjacent band each round**. The engine re-evaluates zones per round and lets
  them expand — terrain with momentum. Countered by *denial* (barren ground) and *fire* (burns it).
- **Amplifiers** (Glasstorm's `Shred`) — a tag that does nothing itself but **multiplies every
  other source.** `Shred` is stacking defense-reduction: a `Shred N` target takes more from *all*
  incoming damage (every ally, every DoT, every zone). The first force-multiplier — resolution reads
  the target's `Shred` stacks as a damage-taken modifier. The clean answer to `Armored` tanks.

## Master tag dictionary

Tags are grouped by category. `*` marks a tag referenced by a designed power but "owned"
(fully defined) by a power not yet written.

### Damage types
`Fire` · `Crushing` · `Slashing` · `Piercing` · `Acid`* · `Lightning`*

### Statuses & DoTs
`Burning` · `Bleeding` · `Frozen`* · `Chilled`* · `Slowed` · `Rooted` · `Suppressed` ·
`Staggered` · `Knockback` · `Corroded`* · `Injury` · `Shocked`* · `Guarded` · `Conductive` ·
`No-Bleed` · `Regenerating` *(first heal-over-time — a signed DoT)* · `Cauterized` ·
`Grievous` · `Exhausted` · `Downed` · `Toxic` · `Lucky`/`Blessed` · `Jinxed` · `Sealed Fate`* ·
`Taunting` *(aggro — enemy target-selection is forced onto the taunter; first surfaced in the combat MVP)* ·
`Entangled` *(`Rooted` + a constricting DoT)* · `Thorns` *(retaliation — strikers eat damage)* ·
`Shred` *(AMPLIFIER — stacking −armor; target takes more from all sources)* · `Blinded` *(accuracy penalty)*

### Stances / modes
`Stance:Metal` *(first stance tag — double-edged; see Stances system above)*

### Fortunes (Probability Pull's drawn pool — all viable, different directions)
`Fortune:Edge` (crit) · `Fortune:Ward` (negate next hit) · `Fortune:Slip` (enemy miss) ·
`Fortune:Haste` (extra action) · `Fortune:Find` (spawn `Object`/`Charge`) ·
`Fortune:Mend` (small heal) *(pool is open-ended; these are the seed entries)*

### Target / body states
`Oiled` · `Wet` · `Doused` · `Flammable` · `Anchored` · `Heavy`

### Position & defense
`Cover` · `Armored` · `Entrenched` · `Destructible Terrain` · `Sealed`

### Zone tags
`On-Fire` · `Water Source` · `Rain` · `Open Sky` · `Enclosed` · `Plant-Rich` ·
`Metal Structures` · `Gas` · `Cement Source` · `Rubble` · `Concrete` · `Urban` · `Chasm` ·
`Flooding` · `Warehouse` · `Featureless` · `Unstable` · `Fragile` · `Submerged` ·
`Collapse` · `Barred` · `Locked` · `Electrified`* · `Hazard` · `Gravity Well` *(pulls + weighs each round)* ·
`Overgrown` *(spreading — propagates to an adjacent band each round)* ·
`Glasstorm` *(abrasive DoT + `Slowed` + `Blinded`; intensifies over rounds)*

### Objects (for scavenge/throw)
`Object` · `Mass` · `Car` · `Lamppost` · `Debris` · `Sand` · `Glass`

### Mechanical / intrinsic
`Generative` · `Ranged` · `Area-Capable` · `Combo-Igniter` · `Sustained` · `Hazard` ·
`Carry-Gated` · `Material:Cement` · `Charge` · `Encumbrance` · `Control` · `Terrain-Shaper` ·
`Physical` · `Melee` · `Object-Wielder` · `Range-Collapser` · `Armor-Pierce` · `No-Material` ·
`Morph` · `Stance-Based` · `Metal` · `Biological` · `Self-Sustain` · `Metabolize` ·
`Conceptual` · `Luck` · `Drawn-Kit` · `Fortune` · `Gamble` · `Variance` ·
`Gravity` · `Pull` *(forced movement toward — inverse of `Knockback`)* · `Singularity` ·
`Spreading` *(zone growth rule — expands to an adjacent band each round)*

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
- **Probability Pull → everyone:** the wildcard feeds every kit by chance — `Fortune:Find` spawns
  an `Object` (Strength ammo) or `Charge` (Cement); `Fortune:Mend` is a borrowed regen tick;
  `Edge`/`Ward`/rerolls handed to allies (Lend Luck) turn any high-variance play reliable —
  re-roll a missed Conflagration, guarantee the Mausoleum lands.
- **Determinism → Probability Pull (counter):** `Sealed Fate`* and fixed-fate bosses suppress the
  draw the way `Cauterized` stops regen — anti-luck is the gambler's hard counter.
- **Gravity Anchor → zone-makers (the gather-and-reap engine):** `Pull` drags the enemy force into
  one band; whoever owns that band's hazard reaps. Drag foes into Glasstorm's shred, Overgrowth's
  roots, or a fire zone — gravity gathers, terrain kills. `Heavy`/clustered targets also can't dodge
  AoE or beams. The signature pairing of the second squad.
