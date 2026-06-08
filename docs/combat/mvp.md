# Combat MVP — the Vertical Slice

The smallest playable encounter that proves the core thesis: **tags reading tags produces
emergent fun.** Not a combat system — *one fight*, built to answer a single question. If rooting
an enemy into a fire feels emergent rather than scripted, the engine bet holds and every power
becomes content for a loop that works. If it doesn't, we found out after one screen.

> **Status:** design spec, pre-code. All numbers below are **playtest dials**, not balance —
> placeholders chosen to make the slice runnable, to be tuned the moment it's playable.

## The slice

- **Party:** 2 characters — **Pyrokinesis** + **Cement Control** (they share the headline combo).
- **Enemy:** 2 **Raiders** — dumb melee. Close to Engaged, hit. One test of counterplay, no more.
- **Zone:** one room with a couple of zone tags (e.g. `Enclosed`, a `Cement Source`).
- **Goal:** drop both Raiders **before the doom clock hits 0.**
- **Lose:** both characters `Downed`, or doom reaches 0.

Everything not needed to prove the combo is **out of scope**: no roster select, no progression,
no inventory, no exploration, no second encounter. Six powers exist on paper; the slice runs two.

## Core resolution — the Control check

Every action that *applies a tag* rolls a check. Raw, automatic effects (a wall just goes up)
don't roll. The check is **2d6 + modifiers**, read against **fixed thresholds**:

| Roll | Tier | Result |
|------|------|--------|
| **10+** | Full | the strong outcome — apply the full/upgraded tag |
| **7–9** | Partial | the soft outcome — weaker tag, *or* full effect at a cost (Strain / exposure) |
| **6−** | Fail | miss, or it lands but the enemy reacts / you pay for it |

**Modifiers are where the engine lives.** No per-action difficulty number — instead, every tag
in scope is a **±1**:

- **Acting attribute:** −1 … +2 (the character's proficiency with the check).
- **Tags in scope:** target `Oiled`/`Flammable` → **+1** to ignite; `Wet`/`Doused` → **−1**;
  `Staggered`/`Slowed` enemy → **+1** to land control; high ground, flanking, etc.
- **Push:** spend +1 Strain to add **+1** to the roll (press your luck — the universal lever
  Probability Pull later bends for free).

This is the thesis as arithmetic: a combo isn't special-cased, it's *the sum of the tags present.*

## Attributes (MVP-minimal — provisional)

Only what the two-power slice needs. The full attribute model is deferred until Strength/Morph/
luck enter (each wants its own — Might, Wits, etc.).

| Attribute | Does | MVP use |
|-----------|------|---------|
| **Focus** | channeled-power checks | Pyro & Cement roll Focus to apply tags |
| **Reflex** | dodge, initiative | enemy attacks vs your Reflex; sets turn order |
| **Resolve** | Strain cap | how much you can spend before Backlash |
| **Vitality** | HP | how much you can take before `Downed` |

Starting line (dials): **HP 20**, **Resolve 6**, **Focus +2**, **Reflex +0**.

At **Focus +2** a check lands **~42% full / ~42% partial / ~17% fail** — failures are uncommon and
you usually accomplish *something*. (At +1 the bell curve was punishing: ~28% full, ~28% whiff.)
**Push** — spend +1 Strain for +1 to the roll — lets you buy into ~58% full odds when a check
matters, at the cost of creeping toward Backlash. It's the lever that makes the Strain economy
bite, and a first taste of Probability Pull's identity.

We chose **2d6 over d20 deliberately:** on a bell curve each ±1 modifier shifts a lot of
probability, so every tag in scope matters — which *amplifies* the tag-stacking/combo play the
whole game is built on. d20's flat 5%-per-point would mute exactly that. The "feels low" we hit in
playtest was a too-low base modifier, not a flaw in 2d6 — fixed by the +2 base, not by changing dice.

## Round structure

Strict, side-based turns (initiative refinement deferred):

1. **Party turn** — each character: **1 Move** + **1 Action**.
   - *Move* = shift one range band, or reposition.
   - *Action* = one Expression (Firebolt, Cement Slam, Bulwark…). Rolls a Control check if it
     applies a tag.
2. **Enemy turn** — each Raider: close toward Engaged, attack if in range (check vs Reflex).
3. **End of round** — in order:
   a. **DoTs tick** — `Burning` deals its damage (signed-DoT engine, ready for heals later).
   b. **Combos resolve** — tags notice each other (the headline: `Rooted` + `On-Fire`).
   c. **Doom −1.**

## Range bands

Three abstract bands, no grid: **Engaged · Near · Far.** Move shifts one band/turn.

- Pyro operates **Near/Far** (artillery — wants distance).
- Cement operates **Engaged/Near**.
- Raiders must reach **Engaged** to hit — so *keeping them out* is itself a tactic, and `Rooted`
  (can't close) or `Slowed` (closes slower) directly buys survival.

## Strain & Backlash

Each Expression costs Strain; a running total is capped by **Resolve**. You *may* push past the
cap, but exceeding it triggers **Backlash**: the action still happens, then you take `Staggered`
(lose your next Action). MVP keeps Backlash to that one effect; richer/bodily backlash (per the
power docs) comes later.

## HP, damage, Downed

Health pools are **deliberately large** so no single hit ends anyone — fights are won by
attrition and control, not burst. This is what makes the combo engine the star: locking an enemy
and cooking it over rounds beats one big number.

- **HP 20** party, **16** Raiders (playtest dial — Raiders trimmed so a focused combo clears them inside the clock).
- Damage in chunks that are a *fraction* of the bar: **Firebolt ~4**, **Crushing Slam ~5**,
  **Raider hit ~4**, **Burning / On-Fire ~3 per round.** Roughly **5 hits** to drop someone, so
  positioning and tempo have room to matter.
- **0 HP → `Downed`** (removed from the slice — no death/bleed-out modelling yet). Both party
  members Downed = loss.

### Design rule — no one-shots (except the specialist)
**Baseline: no single hit may remove more than ~⅓ of a target's max HP.** Nobody gets deleted in
one click; every kill is *built*. Big capstone effects (Conflagration, Wrecking Throw, Jackpot)
swing fights through **area, DoT, and control** — not one deleting number.

**The exception is the payoff for commitment.** A build that *specializes hard* for burst — a
narrow power, all-in on damage, sacrificing survivability / utility / range — **can** break the
⅓ ceiling and one-shot. That's not a hole in the rule; it's the **Specificity axis** (narrow =
stronger but situational) expressed in the damage layer. The glass cannon earns its glass: fragile,
situational, resource-hungry, and punished hard the moment the one-shot setup isn't available.
The one-shot is a *reward you build toward*, never a default anyone carries.

## The doom clock

A visible counter starting at **6**. −1 each round end. At **0**: the slice is **lost** (stand-in
for "reinforcements arrive / objective fails"). Its whole job in the MVP is to make **tempo cost
real** — every turn spent maneuvering is a turn closer to losing, which is the pressure that
makes the Pyro+Cement *tempo* of "lock it, then burn it" matter.

## Affinity — same tag, opposite meaning by reader

A unit can carry an **affinity** that flips how it reads a tag. The Pyromancer has **fire
affinity**: `On-Fire` and `Burning` don't damage her — she's *immune*, and standing in an
On-Fire band makes her **Stoked** (+1 to her fire checks). It's the inverse of Metal Skin's
`Conductive` (which makes `Lightning` hurt *more*): the same tag, read as a buff by one unit and a
threat by another, with **no special-casing** — the effect just queries the reader's affinity.
Mason, no affinity, still cooks in the fire — so "don't park the cement-mage in the inferno" stays
a real positioning decision, consistent with the Pyro-hurts-allies tension in the power docs.

## Tank & aggro — making "hold the line" literal

A tank that can't *compel* attacks is just a durable body. **`Taunting`** is the aggro tag: while a
unit carries it, enemy target-selection reads it and is forced onto that unit — the Raiders don't
get to pick the squishy in the back. Paired with **`Stance:Metal`** (a persistent toggle: `Armored`
= −2 to every incoming hit and immune to `Staggered`, but `Heavy` so it can't move and bleeds
upkeep Strain each round), the tank does its whole job in two tags: *make them hit me* (`Taunting`)
and *make it not hurt* (`Armored`). Mason and Ember then operate untouched. The cost is real — two
setup actions plus an ongoing Strain drain — so turtling forever isn't free. Added a third Raider
so the aggro actually matters: one body can't bottleneck three attackers, but one *taunt* can.

## Medic & signed DoTs — healing as negative damage

Wren (Regeneration) proves the **signed-DoT** claim in running code: `Regenerating` is `Burning`
with the sign flipped — *same tick loop*, it just adds HP instead of subtracting. No separate heal
system. **Graft** applies it to an ally (or **revives** a Downed one to 6 HP); **Mend Self** turns
it inward; **Rend** opens a `Bleeding` DoT (the attrition the regenerator wins, since she out-heals
what she inflicts). The documented counter shows up for free: a unit that's `Burning` or standing
in an On-Fire band is **Cauterized** — its `Regenerating` is suppressed that round. So keep the
medic out of Ember's fire, and the tank+healer pairing (Wren tops up Steele while he soaks the
taunt) just *works* — two powers' tags interacting with nothing special-cased between them.

## The proof — what a winning line looks like

The slice exists to make this sequence *emerge*, not be scripted:

1. **Cement Slam** a Raider (Focus check). **10+** → `Rooted`; **7–9** → only `Slowed`.
2. **Firebolt** the zone/that Raider (Focus check, **+1** if it's near oil/`Flammable`) → `Burning`
   + the position gains `On-Fire`.
3. **End of round:** `Burning` ticks. The combo fires — a **`Rooted` enemy in an `On-Fire` zone
   can't flee and cooks** every round end. No special "if rooted and on fire" code: `Rooted`
   removes the escape option the AI would otherwise take, so it simply stays and eats the DoT.
4. Repeat / mop up before **doom 0.**

If that reads as *clever* when you play it — if you feel like *you* found the combo — the thesis
is proven.

## Open decisions (what playing the slice will force us to answer)

- **Numbers:** HP / Strain / damage / doom length are guesses. First playtest tunes them.
- **Threshold vs difficulty:** this spec uses **fixed 10+/7–9/6− thresholds** (tags = ±1). The
  alternative — roll vs a per-action target number — is still on the table if fixed thresholds
  feel too samey. *Recommended: keep fixed; it's the cleaner expression of "tags reading tags."*
- **Do all three range bands earn their keep,** or is Engaged/Not-Engaged enough for the MVP?
- **Initiative:** side-based now. Does the fight want per-character speed order, or is side-based
  fine through the slice?
- **Backlash depth:** one `Staggered` effect now. When does the richer per-power backlash land?
- **Where this doc lives later:** the proven rules graduate into `DESIGN.md §5` / the engine spec;
  this file stays as the slice's record.
