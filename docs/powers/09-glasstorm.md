# Power 09 — Glasstorm

**Identity:** *Conjure a screaming storm of razor glass and grit. It doesn't just cut — it wears
everything down: armor flakes away, footing clogs, eyes blind. You don't kill the enemy. You make
them soft, and let the squad do the rest.*

- **Domain:** Material (glass / sand)
- **Specificity:** Broad AoE — area damage *and* battlefield debuff
- **Material:** Generative (conjures glass), but **escalates** where there's grit to whip up
- **Role:** Artillery / AoE / debuffer
- **Intrinsic tags:** `Material` `Ranged` `Area-Capable` `Control` `Sustained`

> **The engine concept this power forces — the AMPLIFIER (`Shred`).** Every effect so far does a
> thing *itself*: deals damage, locks a target, heals, moves a unit. `Shred` does nothing on its
> own — it **makes every *other* source hit harder.** It's stacking armor/defense reduction: each
> application peels a layer, so a `Shred 3` target takes more from Mason's slam, Atlas's fist,
> Radiance's beam, the fire, the thorns — *all of it.* The first **force-multiplier** in the
> dictionary, and the perfect role for the squad's reaper: don't out-damage the gathered cluster,
> **soften it** so everyone else's numbers spike. It's also the clean answer to armor (Steele,
> Living Stone, any `Armored` tank): grind the plating off.

## Expressions

### ◈ Offense — Flensing Gale *(starter)*
A scything band of glass: `Slashing`/`Piercing` to **everything in a target band** + applies a
stack of `Shred` (−armor, stacks) to each. The cluster-softener — best on a gathered group.
- Reads `Rubble`/`Concrete`/`Sand` in the zone → bonus grit, extra `Shred`.
- **Cost:** medium Strain.

### ◈ Defense — Mirror-Haze
Wreathe yourself in swirling glass: ranged attackers eat an accuracy penalty (whiteout) and
`Slashing` retaliation when they fire through it.
- **Cost:** medium Strain, sustained.
- **Unlock (natural):** survive ranged fire inside the haze several times.

### ◈ Utility — Etch
Abrade the map: grind through `Barred`/`Sealed`/`Destructible Terrain`, scour sensors `Blinded`,
or carpet a band into `Sand`/`Glass` footing for later storms to feed on.
- **Cost:** trivial Strain. Auto-solves `Barred`/`Sealed` obstacle tags.

### ◈ Support — Screen
Raise a wall of suspended grit: blocks enemy ranged **sightlines** (concealment `Cover` for the
squad) and `Slows` anything that crosses it. Battlefield control without a scratch of damage.
- **Cost:** medium Strain.
- **Unlock:** shield allies from ranged fire a few times.

### ◈ Signature — Glasstorm *(capstone)*
The full tempest: a persistent `Glasstorm` zone tears across the bands. Everything inside takes
abrasive damage each round, is `Slowed`, fights `Blinded` (accuracy penalty), and gains `Shred`
stacks — and the storm **intensifies the longer it rages.** The whole enemy force softened, slowed,
and bleeding while the squad cleans up.
- **Cost:** high Strain + per-round upkeep. **Backlash:** the storm doesn't discriminate when it
  collapses — you're caught in the last gust (self `Slashing` + `Blinded`).
- **Unlock:** story milestone + "Shredded 3+ enemies at once."

## Material rules
Generative — conjured from Strain — but **escalates with grit**: `Rubble`, `Concrete`, `Sand`,
`Glass`, `Urban` zones feed bigger storms; clean rooms and `Open Sky` give thin ones. **The hard
counter is water:** `Wet`/`Rain`/`Submerged` clumps the sand and kills the storm. **Resolve** caps
the sustain.

## Combos
- **Sets up:** `Shred` (amplifies the *entire* squad's damage), `Slowed`, `Blinded`, concealment
  `Cover`.
- **Pays off (the reaper slot):** the gathered, `Entangled` cluster (Gravity Anchor + Overgrowth)
  can't dodge the band-wide gale — **`Shred` it, and every hit that follows spikes**: Mason's
  Crushing, Atlas's Hurl, Radiance's beams, the thorns, all amplified at once. Lay the `Glasstorm`
  zone *over* a `Gravity Well`/`Overgrown` band and the trapped enemies eat stacked hazards.
- **Cancelled by:** `Wet`/`Submerged`/`Rain` (dampens the grit), `Sealed`/clean rooms (no material),
  `Anchored` foes shrug the `Slow`.
- **Tension:** the storm blinds and slows **everyone** in the band, allies included — don't gale
  the lane your own melee are fighting in. (And like all this squad's terrain, a `Glasstorm` over
  `Overgrown` is fine, but over a fire zone the heat-haze and grit fight each other.)

## Environment
- **Loves:** `Rubble` · `Concrete` · `Urban` · `Featureless` *desert*/`Sand` · `Enclosed`
- **Hates:** `Water Source` · `Rain` · `Submerged` · `Open Sky` (grit disperses)

## Strain profile
Medium-to-heavy, escalating: a held `Glasstorm` bleeds Resolve but compounds — each round it shreds
deeper. The decision is *how long to feed the storm* versus banking Strain, and whether to gale a
band your own squad needs to stand in.

## Tags minted
- **Mechanical:** `Shred` *(the first AMPLIFIER — stacking defense-reduction; makes the target take
  more from **all** sources)*
- **Zone:** `Glasstorm` *(abrasive DoT + `Slowed` + `Blinded`; intensifies over rounds)*
- **Status:** `Blinded` *(accuracy penalty — sand/glare; reusable by future light/sensory powers)*
- **Object/terrain:** `Sand`, `Glass`

*(`*` = referenced here but owned by a power not yet designed.)*
