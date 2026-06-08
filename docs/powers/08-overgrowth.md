# Power 08 — Overgrowth

**Identity:** *Turn the battlefield itself against them. Vines erupt, roots seize ankles, thorns
bristle from the ground — and what you grow doesn't stop growing. Win by making the terrain a
weapon that spreads while they panic.*

- **Domain:** Biological
- **Specificity:** Narrow medium (plant life), broad application — generative, grows from ambient life
- **Material:** None — generative like fire, but *denial*-counterable (barren ground starves it)
- **Role:** Controller / terrain
- **Intrinsic tags:** `Biological` `Generative` `Control` `Terrain-Shaper` `Sustained`

> **The engine concept this power forces — SPREADING ZONES.** Every zone so far is *placed* and
> *fixed*: `On-Fire` and `Gravity Well` sit on the band you put them on and tick down. `Overgrown`
> is **alive** — at end of round it **propagates to an adjacent band**, so an unattended thicket
> creeps across the field on its own. The engine generalizes a zone from a static tag into one with
> a *growth rule*: each round it re-evaluates and may expand. Now terrain has momentum — leave it
> and it takes the map; the enemy has to *spend actions cutting through* what you spent one action
> seeding.

## Expressions

### ◈ Offense — Strangle *(starter)*
Vines whip from the ground and constrict a target: `Slashing` + `Entangled` on a Control check
(`Rooted` that *also* bleeds — a living `Bleeding` from the thorns squeezing tighter each round).
Seeds `Overgrown` on the target's band.
- Reads a `Plant-Rich`/`Overgrown` band → bonus + guaranteed `Entangled`.
- **Cost:** low Strain.

### ◈ Defense — Thicket
Grow a bramble wall: `Cover` for a position **plus `Thorns`** — anyone who strikes through it (or
is Engaged with you) takes retaliatory `Piercing`. Living `Destructible Terrain` that regrows a
little each round.
- **Cost:** medium Strain.
- **Unlock (natural):** survive melee behind thorns several times.

### ◈ Utility — Verdant Path
Let growth solve the map: bridge a `Chasm` with vines, force `Barred`/`Locked` doors apart with
roots, smother a `Hazard`, or carpet a band into `Plant-Rich`/`Overgrown` terrain to fight on.
- **Cost:** trivial Strain. Auto-solves `Chasm`/`Barred`/`Locked`/`Overgrown` obstacle tags.

### ◈ Support — Symbiosis
Grow *for* an ally: bristle them with `Thorns` + `Cover`, or sprout a restorative bloom — a small
`Regenerating` tick (the same signed-DoT Wren uses, borrowed via biology).
- **Cost:** medium Strain.
- **Unlock:** support-use milestone.

### ◈ Signature — Worldroot *(capstone)*
The whole zone erupts at once: `Overgrown` floods every band, **every enemy is `Entangled`**, and
the growth keeps `Spreading` and damaging for a duration. Lock the entire enemy force in living
terrain while the squad dismantles them.
- **The control payoff** — pairs straight into Gravity Anchor (gather, then root the cluster) and
  any AoE.
- **Cost:** huge Strain, Backlash risk (the bloom drains *you* — self `Exhausted`).
- **Unlock:** story milestone + "Entangled 3+ enemies in one fight."

## Material rules
None carried — generative, grown from ambient life and spores. **The trade (like fire): denial.**
`Featureless`/`Concrete`/barren and fire-scorched ground starve it; it thrives on living, damp,
`Plant-Rich` terrain. **Resolve** caps the sustain; nothing to carry, but a dead world is its weakness.

## Combos
- **Sets up:** `Entangled`/`Rooted`, `Thorns`, and **spreading `Overgrown`/`Plant-Rich` zones** that
  deny ground over time.
- **Pays off (the squad's spine):** **Gravity Anchor `Pull`s the enemy into one band → Overgrowth
  `Entangle`s the whole cluster** → they can't flee Glasstorm's shred, Radiance's beams, or the
  spread. Gravity gathers, vines hold, everyone else reaps.
- **Cancelled by:** **fire** (burns vines — see tension), `Acid`/`Corroded`, barren/`Concrete`
  zones, `Flying` foes.
- **Tension (double-edged, free from the engine):** `Overgrown`/`Plant-Rich` is **fuel** — an
  allied *or* enemy Pyromancer can turn your control terrain into a `Conflagration`. Your roots set
  the table for a fire you don't control. Coordinate, or watch your battlefield burn.

## Environment
- **Loves:** `Plant-Rich` · `Enclosed` · `Rain`/damp · `Rubble` (cracks to root into)
- **Hates:** `Concrete` · `Featureless` · `On-Fire`/scorched · `Open Sky` (nothing to climb)

## Strain profile
Cheap to seed, sustained to hold. The interesting spend is *patience*: a thicket left to `Spread`
does work for free across several rounds, so the skilled play is **seeding early and letting the
map close on its own** — the inverse of burst, and a natural fit beside Gravity Anchor's slow pull.

## Tags minted
- **Zone:** `Overgrown` *(first **spreading** zone — propagates to an adjacent band each round)*;
  `Plant-Rich` *(already in dict from Pyro — Overgrowth is now its owner/creator)*
- **Status:** `Entangled` *(`Rooted` + a constricting DoT)*, `Thorns` *(retaliation — strikers eat damage)*
- **Mechanical:** `Spreading` *(the growth rule — a zone that expands over rounds)*

*(`*` = referenced here but owned by a power not yet designed.)*
