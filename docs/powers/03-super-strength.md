# Power 03 — Super Strength

**Identity:** *Lift, throw, smash, charge. You carry no fuel and change no shape — but anything
you can pick up becomes a weapon, and anything in your way becomes debris.*

- **Domain:** Physical
- **Specificity:** Broad (raw output, always-on)
- **Material:** None — but **appropriates the environment as ammo**
- **Role:** Melee striker
- **Intrinsic tags:** `Physical` `Melee` `Crushing` `Object-Wielder` `Range-Collapser` `No-Material`

> **Engine concepts this power forces.** (1) A *third* resource model: it scavenges the zone's
> furniture — its ammo is whatever `Object` tags the room holds, each with a `Mass` tag that
> scales the hit. In a `Featureless` field it's just fists. The inverse of Cement: Cement
> brings material, Strength finds it — and **consumes terrain** (throw the wall, lose the
> `Cover`). (2) **Forced movement** — knockback, launches, gap-closing leaps: the positioning
> verbs the range-band system implied.

## Expressions

### ◈ Offense — Haymaker *(starter)*
Brutal `Crushing` melee, Engaged. On a Control check, choose `Knockback` (shove target out a
range band — breaks their Engaged combos, exposes them) or `Staggered` (lose an action). Raw
force gives partial `Armor-Pierce`.
- **Cost:** low Strain.
- **Movement:** the `Range-Collapser` tag lets you **leap Far → Engaged as your Move** —
  critical for reaching enemy artillery before it cooks the squad.

### ◈ Defense — Brace
Plant and become `Anchored`: immune to forced movement, and your body becomes `Cover` for
allies behind you (intercept hits, reduce incoming `Crushing`).
- **Cost:** medium Strain, sustainable.

### ◈ Utility — Heave
Move what others can't: clear `Rubble`, force `Barred`/`Locked` doors, hold up a `Collapse`,
carry a Downed ally out fast. Solves `Heavy Obstacle`, `Barred`, `Collapse` tags.
- **Cost:** trivial Strain.

### ◈ Support — Fastball Special
Hurl an *ally* to a distant range band — get the Pyromancer to high ground, drop the medic
next to a Downed teammate, or launch the bruiser into a charge. Consensual forced-reposition.
- **Cost:** medium Strain.
- **Unlock:** bond/trust milestone with the thrown ally (XCOM-style).

### ◈ Signature — Wrecking Throw *(capstone)*
Grab the biggest thing available — a car, a wall, an *enemy* — and throw it. Damage scales with
the object's `Mass`; huge objects hit an area; thrown enemies damage both bodies. Or
ground-slam to convert the zone to `Unstable` + `Rubble` (feeds Cement's scavenge, Pyro's
footing).
- **Cost:** high Strain + **Backlash is bodily** (throw your back out → self `Injury`/Strain
  spike).
- **Unlock:** story milestone + "threw an object/enemy for a kill."

## Material rules — environment-supplied ordnance

| Zone supply | Effect |
|-------------|--------|
| `Object`-rich (`Urban`, `Rubble`, `Warehouse`) | Full power — heavy ammo, big throws |
| Sparse | Light objects only; Signature weakened |
| `Featureless` / `Open` | Fists only — Wrecking Throw needs an enemy as the projectile |

**Vitality** governs the `Mass` ceiling (how heavy you can throw without penalty). Strain stays
Resolve-capped.

## Combos
- **Sets up:** `Knockback` (shatters enemy formations & their Engaged combos), `Staggered`,
  `Unstable`/`Rubble` zones (free ammo for Cement, footing for Pyro).
- **Pays off:** throw an `Oiled` object → Pyro ignites it mid-air; chuck an enemy into an
  `On-Fire` zone; a `Slowed` target can't dodge the throw.
- **Cancelled by:** `Featureless` zones (no ammo), `Anchored`/colossal enemies, water/
  `Submerged` (mass dampened).
- **Tension:** throwing the Cement-mage's wall destroys your own `Cover`.

## Environment
- **Loves:** `Urban` · `Rubble` · `Warehouse` · `Enclosed` · `Fragile` · any `Object`-rich zone
- **Hates:** `Featureless` · `Open Sky` · `Submerged` · `Distant`-heavy fights

## Strain profile
Cheap and reliable at the basic level (innate, not channeled). Spikes are the throws and leaps.
The real limiter is the **zone**, not the body — a good Strength player reads the room for ammo
before the fight.

## Tags minted
- **Status / forced-move:** `Knockback`, `Staggered`, `Anchored`
- **Object/zone:** `Object`, `Mass`, `Car`, `Lamppost`, `Debris`, `Featureless`, `Unstable`,
  `Submerged`, `Collapse`, `Barred`
- **Mechanical:** `Object-Wielder`, `Range-Collapser`, `Armor-Pierce`, `No-Material`
