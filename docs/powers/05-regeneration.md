# Power 05 — Regeneration

**Identity:** *Wounds knit shut, blood clots on command, lost flesh grows back. You don't win
fights fast — you win them by still standing when everyone else has bled out. But the clock
keeps ticking while you heal, and some wounds the body refuses to forget.*

- **Domain:** Biological
- **Specificity:** Narrow effect (self-repair), broad application (sustain, revive, endurance)
- **Material:** None — fuelled by the body's own clock (see Metabolize)
- **Role:** Sustain tank / medic / attritionist
- **Intrinsic tags:** `Biological` `Self-Sustain` `Sustained` `Metabolize` `No-Material`

> **Two engine concepts this power forces.**
> **(1) Heal-over-time = a *signed* DoT.** `Burning` and `Bleeding` tick damage each turn;
> `Regenerating` ticks it *back*. Rather than special-case healing, the engine generalizes a DoT
> into a periodic effect with a sign — a heal is just negative damage on a clock. Every system
> already built for `Burning` (duration, suppression, stacking) now works for regen for free.
> **(2) A fourth resource model — Metabolize.** Pyro *generates*, Cement *carries*, Strength
> *scavenges*. Regeneration spends almost no Strain — its true cost is **time**. In an XCOM
> doom-clock game, tempo *is* the scarcest currency: every turn you spend healing, the clock
> advances and the objective slips. Countered not by running dry but by **out-burst** (kill the
> tick faster than it heals) and by **heal-suppression** tags (`Cauterized`, `Corroded`).

## Expressions

### ◈ Defense — Knit *(starter — the core toggle)*
Enter `Regenerating`: a per-turn self-heal HoT. While held, it clears `Bleeding` on its own and
slowly works `Injury` down toward zero.
- **Buffs:** steady recovery, immune to `Bleeding` while active (clots faster than it opens).
- **Limits:** does nothing against a single big hit (heals the *aftermath*, not the spike);
  **suppressed** while `Cauterized` (`Burning`/`Fire`) or `Corroded` (`Acid`) is on you.
- **Cost:** low Strain **per turn** to sustain. The real cost is the turns themselves.

### ◈ Offense — Rend
Grow claws/bone-spurs and tear in, Engaged. `Slashing` + `Bleeding` on a Control check. The
attrition play: open a bleed war you're built to win — they bleed and you don't.
- **Cost:** low Strain. Encourages reckless Engaged risk you can afford to heal back.

### ◈ Utility — Endure
Metabolize your way through what stops others: ignore `Injury`/`Slowed` action penalties for a
turn, hold breath and walk through `Gas`/`Hazard`/`Toxic` zones (purge the poison), shrug
`Exhausted`, or pull free of an impaling `Anchored`/`Rooted` by tearing loose and healing it.
- **Cost:** trivial Strain. Auto-solves `Gas`/`Toxic`/`Hazard` exploration tags.

### ◈ Support — Graft
Give of yourself: apply `Regenerating` to a wounded ally for a few turns, or transfuse — spend
*your own* Vitality to **revive a `Downed` teammate** to their feet. The medic role no other
starter fills.
- **Cost:** medium Strain + a real chunk of your own Vitality (you heal them by depleting you).
- **Unlock:** revive or sustained-heal an ally a few times (natural).

### ◈ Signature — Undying *(capstone)*
For a short duration, refuse death: massive `Regenerating++`, cannot be `Downed` (drop to zero
and stand back up next turn), and regrow even `Grievous` wounds the normal tick can't touch.
The attritionist's apotheosis — outlast a whole encounter.
- **Cost:** trivial Strain to fire — **but Backlash is bodily and delayed.** When it ends the
  body cashes the check: `Exhausted`, `Regenerating` **suppressed** for several turns, and a
  `Grievous` `Injury` that won't heal until you've rested. You bought those turns on credit.
- **Unlock:** story milestone + "regrew from near-zero / survived a killing blow."

## Material rules — Metabolize (time as the resource)
None carried, never runs dry. The cost is **tempo**: healing means turns spent *not* advancing
the objective while the doom clock ticks. **Vitality** is the engine attribute — it sets the
HoT tick rate, the `Injury` ceiling you can clear, and how much you can transfuse before
risking your own collapse. Strain stays Resolve-capped but is rarely the limiter.

## Combos
- **Sets up:** `Bleeding` (Rend — and now the dictionary's *owner* of it), `Regenerating` on
  allies, revived bodies back in the fight.
- **Pays off:** any frontline tag that lets you stand in the open and soak (Metal Skin's
  `Guarded`, Strength's `Cover`) — sustain only works if you survive long enough to tick.
  A `Slowed`/`Rooted` enemy can't escape your bleed war.
- **Cancelled by:** **burst damage** (out-damage the tick in one blow — its structural counter),
  `Cauterized` (an enemy Pyro, or your own ally's `Fire`, sears wounds shut and **stops regen**),
  `Corroded`/`Acid` (rot outpaces repair), and `Grievous` wounds the tick can't reach.
- **Tension (emergent, free from the tag engine):** an allied **Pyromancer's `Burning` suppresses
  a regenerator's heal** — same `Fire`-hurts-the-tank shape as Metal Skin's `Conductive`.
  Forge-Heart cauterizing *your* `Bleeding` also shuts off *your* `Regenerating`. Coordinate, or
  your own medic-fire freezes your healing.

## Environment
- **Loves:** `Plant-Rich` (biomass to draw on) · `Enclosed`/`Urban` (somewhere to turtle and
  tick) · any zone the squad can hold while you outlast
- **Hates:** `On-Fire`/`Electrified` (`Cauterized` shuts regen off) · `Acid` zones (`Corroded`) ·
  `Open Sky` (no cover to survive the turns healing costs) · burst-heavy fights

## Strain profile
The inverse of every power so far: **Strain is almost free; *time* is the bill.** A Regeneration
player's tension isn't "can I afford this?" but "can I afford to *wait*?" — every healing turn is
a turn the doom clock wins. The skill is knowing when to stop fighting and tick, and when the
clock says you can't.

## Tags minted
- **Status (now owned here):** `Bleeding` *(was referenced by Pyro/Metal — Regeneration owns it)*
- **Status / state:** `Regenerating` *(first heal-over-time — a signed DoT)*, `Cauterized`,
  `Grievous`, `Exhausted`, `Downed` *(formalized — the revive target)*, `Toxic`
- **Mechanical:** `Biological`, `Self-Sustain`, `Metabolize` *(fourth resource model)*

*(`*` = referenced here but owned by a power not yet designed.)*
