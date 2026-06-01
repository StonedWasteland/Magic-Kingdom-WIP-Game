# Power 02 — Cement Control

**Identity:** *Command wet cement that hardens on your word — raise a bunker, entomb a foe,
bridge a chasm. But you can only shape what you carry or what the world gives you.*

- **Domain:** Material
- **Specificity:** Narrow medium, broad application (needs cement, but does a lot with it)
- **Material:** **Yes — the flagship carry power**
- **Role:** Controller / terrain
- **Intrinsic tags:** `Material:Cement` `Carry-Gated` `Control` `Terrain-Shaper` `Crushing`

> **Engine concept this power forces — a second resource axis.** Pyrokinesis is Strain-only.
> Cement is Strain **and Charges** (how much cement you brought). Run dry and you're a strong
> guy with no cement. This is the carry system, and it's what makes the loadout choice a real
> strategic decision instead of flavor.

## Expressions

### ◈ Offense — Cement Slam *(starter)*
Hurl a hardened slug or set an enemy's footing. `Crushing` damage; applies `Slowed` on a
Control check, or spend +1 Charge to upgrade to `Rooted`. Engaged/Near.
- Reads `Wet` / `Water Source` → cement sets faster, bonus damage.
- **Cost:** 1 Charge, low Strain.

### ◈ Defense — Bulwark
Raise a wall or encase yourself. Applies `Cover` to a position (blocks a range band / line of
sight) or `Armored: Crushing-Resist` to self. The wall is `Destructible Terrain`.
- **Cost:** 2 Charges, medium Strain.

### ◈ Utility — Mason's Hand
Bridge gaps, seal doors, dam a flood, repair. Exploration: auto-solves `Chasm`, `Locked`,
`Flooding` obstacle tags.
- **Cost:** Charges scale with size, trivial Strain.

### ◈ Support — Set the Line
Fortify an ally's position (`Cover` + `Entrenched`) or cement-cast a splint (reduce an ally's
`Injury` / `Slowed`).
- **Cost:** 2 Charges, medium Strain.
- **Unlock:** support-use milestone.

### ◈ Signature — Mausoleum *(capstone)*
Entomb a single target — hard `Rooted` + `Suppressed` (can't act or flee) for a duration — or
seal a whole zone (`Sealed`: splits the enemy force, fight them piecemeal).
- **The control payoff:** lock the boss while the squad burns it down. Pairs directly into
  Pyro's Conflagration.
- **Cost:** huge Charge dump, high Strain, Backlash risk.
- **Unlock:** story milestone + "rooted 2+ enemies in one fight."

## Material rules — the loadout decision

| Build | Reserve | Encumbrance | Playstyle |
|-------|---------|-------------|-----------|
| **Fortress** | Heavy pack | −Reflex, slow | Walking bunker; devastating in fixed positions, bad in a chase |
| **Skirmisher** | Small flask | None | Mobile, must ration; hit-and-run control |
| **Environmentalist** | Zero carried | None, full Reflex | Free movement but terrain-locked; scavenges `Cement Source`/`Rubble`/`Concrete` |

Resupply at base (Quartermaster) or scavenge zone tags mid-run.

## Combos
- **Sets up:** `Slowed`, `Rooted`, `Sealed`, `Cover`. **Headline synergy:** root → Pyro
  Conflagration.
- **Pays off:** a `Wet` target/zone (water-mage, rain) sets your cement instantly.
- **Cancelled by:** `Acid`/`Corroded` dissolves cement walls; `Crushing-Resist` enemies shrug
  the slam; running out of Charges.
- **Tension:** a Super Strength ally can smash through your own walls if uncoordinated.

## Environment
- **Loves:** `Cement Source` · `Rubble` · `Concrete` · `Urban` · `Enclosed` · `Water Source`
- **Hates:** `Open Sky` / open field · `Acid` · `Fragile` floors

## Strain profile
**Dual-gated.** Strain limits the big sets; Charges limit everything. The interesting decision
happens before the expedition (loadout) and during (spend now or save for Mausoleum).

## Tags minted
- **Damage:** `Crushing`
- **Status:** `Slowed`, `Rooted`, `Suppressed`, `Injury`
- **Position/defense:** `Cover`, `Armored`, `Entrenched`, `Destructible Terrain`, `Sealed`
- **Zone:** `Cement Source`, `Rubble`, `Concrete`, `Urban`, `Chasm`, `Flooding`
- **Counter-tags:** `Acid`*, `Corroded`*
- **Mechanical:** `Carry-Gated`, `Material:Cement`, `Charge` *(new resource type)*,
  `Encumbrance`

*(`*` = referenced here but owned by a power not yet designed.)*
