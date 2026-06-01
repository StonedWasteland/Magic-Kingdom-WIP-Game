# Power 04 — Metal Skin

**Identity:** *Turn your body to living metal. Nigh-unbreakable and immovable — but heavy, slow,
and a lightning rod. The shield the squad hides behind.*

- **Domain:** Morph
- **Specificity:** Broad (whole-body transformation, versatile defensively)
- **Material:** None — but the transformation carries its own weight (upkeep + encumbrance)
- **Role:** Tank / frontline
- **Intrinsic tags:** `Morph` `Stance-Based` `Sustained` `Metal` `Conductive`

> **Engine concept this power forces — the STANCE / MODE system.** Every power so far has been
> discrete *actions*. Metal Skin is a *state you enter and hold*: a toggle that applies a
> persistent `Stance:Metal` tag, which then modifies all your other actions and all incoming
> effects until you drop it. And it's the first **double-edged toggle** — one switch applies a
> bundle of *both* buffs (`Armored`, `No-Bleed`) *and* vulnerabilities (`Conductive`, `Heavy`).
> The tag engine handles this for free: while `Stance:Metal` is in scope, any `Lightning` or
> `Fire` in the same scope reads the vulnerability automatically. No special-casing.

## Expressions

### ◈ Defense — Ironhide *(starter — the core toggle)*
Enter `Stance:Metal`. While held:
- **Buffs:** `Armored` (heavy reduction vs `Crushing`/`Slashing`/`Piercing`/`Physical`),
  `No-Bleed` (immune to `Bleeding`).
- **Costs:** `Conductive` (`Lightning`/`Shocked` hit harder; sustained `Fire` heats the metal
  → ongoing burn), `Heavy` + `Encumbrance` (−Reflex, −dodge, slower Move, sinks in water).
- **Cost:** an action to enter/exit; low Strain **per turn** to sustain.

### ◈ Offense — Sledge
While in `Stance:Metal`, melee strikes gain `Crushing` + `Armor-Pierce` from sheer mass, can
`Stagger`. Out of stance, just ordinary punches — offense *scales with the mode*.
- **Cost:** low Strain.

### ◈ Utility — Deadweight
Use the mass: `Anchored` against forced movement, ram through `Barred` doors and
`Destructible Terrain`, or wade through a `Hazard`/`Gas` zone unbothered to cross or clear it.
- **Cost:** trivial while already in stance.

### ◈ Support — Aegis
Become mobile `Cover` and **guard** an ally: apply `Guarded` to a teammate, redirecting attacks
aimed at them onto your armored body. The tank's defining role — soak so Pyro/Cement work free.
- **Cost:** medium Strain.
- **Unlock:** protect a Downed/low ally a few times (natural).

### ◈ Signature — Living Fortress *(capstone)*
Become an immovable bulwark for the zone: `Armored++`, immune to forced movement, **taunt the
whole enemy group**, and split the battlefield with your body (like Cement's `Sealed`, but
mobile). Reflect some `Crushing` back at attackers.
- **Cost:** high Strain. **Backlash is mode-locked:** stuck in `Stance:Metal` for several turns,
  unable to drop it — fully exposed to that one Lightning-user.
- **Unlock:** story milestone + "guarded allies through a near-wipe."

## Material rules
None carried. The cost is **upkeep** (Strain per turn while transformed) and **mass tradeoffs**
(`Encumbrance`, sinks when `Submerged`). **Vitality** governs how well you carry the weight
(less Reflex penalty) — the tanky-build attribute.

## Combos
- **Sets up:** `Guarded`, `Cover`, `Staggered`. Holds the line so artillery/control operate
  safely.
- **Pays off:** with Super Strength (two frontliners — one holds, one throws); with Cement
  (double-wall a chokepoint and seal it).
- **Cancelled by:** `Lightning`/`Shocked` (**its hard counter** via `Conductive`),
  `Acid`/`Corroded` (eats metal — shared weakness with Cement), `Submerged` (sinks),
  `Armor-Pierce` enemies.
- **Tension (emergent, free from the tag engine):** an allied **Pyromancer's heat hurts a
  metal-skinned teammate** — `Fire` + `Conductive` in the same scope = friendly burn. Same
  shape as the fire/water tension; coordinate or cook your tank.

## Environment
- **Loves:** `Enclosed` · `Urban` (chokepoints to hold) · `Metal Structures` (reinforce armor)
- **Hates:** `Water Source` / `Submerged` (sinks) · `Electrified` zones (conductivity) ·
  `Open Sky` (a wall in the open is just flanked) · `Acid`

## Strain profile
A new rhythm: **low but constant upkeep.** A long fight bleeds Resolve just by staying armored.
The decision is *when to drop the stance to recover* — and risk the turn you spend exposed.
Distinct from Pyro's burst Strain and Cement's Charges.

## Tags minted
- **Damage (physical subtypes formalized):** `Slashing`, `Piercing` · referenced: `Lightning`*
- **State / status:** `Stance:Metal` *(first stance tag)*, `Guarded`, `No-Bleed`, `Conductive`,
  `Heavy`, `Shocked`*
- **Zone:** `Electrified`*
- **Mechanical:** `Morph`, `Stance-Based`, `Metal`

*(`*` = referenced here but owned by a power not yet designed.)*
