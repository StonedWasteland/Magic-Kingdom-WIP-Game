# Power 06 — Probability Pull

**Identity:** *You don't control the world — you load its dice. Every battle deals you a fresh
hand of fortune; you play the odds you're dealt, bend them when it counts, and press your luck
when the moment's right. The wildcard who's a little bit of everyone, by chance.*

- **Domain:** Conceptual (luck)
- **Specificity:** Broad but indirect — touches the probability layer, never raw force
- **Material:** None — runs on a **Luck** meter + a per-battle **Fortune** hand (see Draw system)
- **Role:** Wildcard / flex — adapts to the hand instead of executing a fixed plan
- **Intrinsic tags:** `Conceptual` `Luck` `Drawn-Kit` `Fortune` `No-Material`

> **The engine concept this power forces — the DRAW system.** Every power so far has a *fixed*
> kit: five Expressions you unlock and keep. Probability Pull is the first whose kit is **rolled
> at battle start** from a pool. Its five Expressions aren't five techniques — they're five *ways
> of interacting with the draw* (play a Fortune, steer the hand, bank/lend Luck, go all-in). The
> engine generalizes "a power's kit" from a fixed list into a **distribution sampled per
> encounter** — powers become data you can draw from. The design rule that makes this *fun* rather
> than *swingy*: **no dead entries in the pool.** Every Fortune is a real tool; variance is in
> *which direction* you're handed, never in *whether* you got something useful. You adapt to the
> hand — that's the whole loop. The Fortunes deliberately echo other powers' resource systems
> (`Find` spawns an `Object`/`Charge`, `Mend` is a small regen tick), so the wildcard is faintly
> every teammate at once.

## Expressions

### ◈ Offense — Wild Card *(starter)*
Spend a drawn offensive Fortune. What it *does* depends on the hand — `Edge` (next strike crits),
`Slip` (force the target's next attack to whiff), a variable-type bolt. High swing, played from
whatever you hold.
- **Cost:** 1 Fortune, low Strain. Reckless by design — you can afford the variance.

### ◈ Defense — Hedge
Tilt a roll your way: spend `Luck` to make an incoming attack **miss** (`Ward`), or convert a bad
result into a coin-flip you're favored to win. Survival by bending the odds, not blocking.
- **Cost:** `Luck`, low Strain. The steering-for-survival use.

### ◈ Utility — Press Your Luck
The roguelike steering verb. **Draw 3, keep 1**; **reroll** the hand; or **gamble** a Fortune
double-or-nothing. Out of combat: lucky finds, force a `Locked` open, stumble onto resources.
- **Cost:** `Luck` per reroll/draw. The skill expression — turns a slot machine into press-your-luck.

### ◈ Support — Lend Luck
Hand your fortune to a teammate: give an ally a `Ward`, an `Edge`, or **a reroll on their own
failed check** — let the Pyromancer re-roll a missed Conflagration, hand the tank a save.
- **Cost:** a banked Fortune or `Luck`, medium Strain.
- **Unlock:** spend luck on allies a few times (natural). *This is where field-luck begins.*

### ◈ Signature — Jackpot *(capstone)*
Go all-in: for one turn, force the **best case for the whole party** — no one misses, everyone
crits, every check lands. The press-your-luck payoff scaled to the squad.
- **Cost:** dumps your `Luck` + high Strain. **Backlash is literal bad luck:** on a poor roll it
  **backfires** — you take `Jinxed` (your rolls go against you for several turns) and the bet's
  cost lands anyway. The bigger the gamble, the bigger the swing, both ways.
- **Unlock:** story milestone + "won a battle off a clutch gamble."

## Material rules — the Draw / Gamble model (a fifth resource model)
None carried. **Clean slate each battle:** draw a fresh **Fortune** hand (the roguelike roll),
plus a **Luck** meter you spend to *steer* (reroll, draw-keep, hedge, lend). Luck refreshes per
encounter and builds as you take favorable risks. **Resolve/Wits** sets hand size and Luck cap —
the gambler's-nerve attribute. This is distinct from Generate/Carry/Scavenge/Metabolize: the
resource is **variance you manage**, and the real cost of pressing your luck is **tempo** when it
backfires (the doom clock cashes a bad roll).

## Combos
- **Sets up:** `Edge`/`Ward`/`Slip` and rerolls handed to allies; `Find` spawns `Object`s
  (Strength ammo) / `Charge`s (Cement) / small `Mend` ticks — the wildcard feeds every kit.
- **Pays off:** any high-variance party play — guarantee the Mausoleum lands, re-roll a missed
  Conflagration, force the clutch crit on a `Slowed` target that can't dodge.
- **Cancelled by:** **determinism / anti-luck** — `Sealed Fate`* (fixed outcomes, owned by a
  future power), `Suppressed` (can't draw), bosses with "fixed fate" immunity; and its own bad
  rolls / `Jinxed`.
- **Tension (the cost of variance):** sometimes the hand is *wrong for the moment* — a defensive
  draw when you needed burst. Over-gambling the Signature can backfire and **burn party tempo**
  against the clock. The character that bends luck is also the one most exposed to it.

## Environment
- **Loves:** `Unstable` · `Fragile` · `Object`-rich / `Urban` (more for luck to grab and `Find`) ·
  chaotic zones where outcomes are already swingy
- **Hates:** `Sealed`/locked-down deterministic arenas · `Featureless` (nothing to luck into) ·
  boss fights with fixed-fate mechanics

## Strain profile
Strain is moderate; the real currency is **variance management** — when to bank `Luck` vs spend,
when to press, when to fold. Unlike the four prior models there's no fuel to run dry and no
medium to carry — there's a *gamble to time.* A good Probability player reads when the squad can
afford a swing and when a bad beat would lose the clock.

## Tags minted
- **Fortunes (the drawn pool — all viable, different directions):** `Fortune:Edge` (crit),
  `Fortune:Ward` (negate next hit), `Fortune:Slip` (enemy miss), `Fortune:Haste` (extra action),
  `Fortune:Find` (spawn `Object`/`Charge`), `Fortune:Mend` (small heal)
- **Status:** `Lucky` / `Blessed` (rolls favor you), `Jinxed` *(backlash — rolls against you)*,
  `Sealed Fate`* *(anti-luck counter — owned by a power not yet designed)*
- **Mechanical:** `Conceptual`, `Luck` *(resource)*, `Drawn-Kit`, `Fortune` *(drawn-effect
  category)*, `Gamble` *(fifth resource model)*, `Variance`

*(`*` = referenced here but owned by a power not yet designed.)*
