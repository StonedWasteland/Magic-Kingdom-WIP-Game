# Magic Worlds — Design Document

*Working title. Browser-based, text-driven, tactical party RPG.*

**Version:** 0.1 (initial draft)
**Status:** Pre-production design

---

## 1. High Concept

A browser-based, text-driven tactical RPG in which the player commands a four-character squad of "Gifted" — people born with bespoke magical powers — in a world facing a slow-burn invasion from somewhere beyond reality. The game blends:

- **XCOM:** turn-based squad combat with escalating threat and a meta-layer doom clock
- **Torn:** browser-friendly, energy-gated, text-first presentation
- **Darkest Dungeon:** expedition loop, roster management, recovery cycles
- **Worm / My Hero Academia / One Piece:** deeply specific, idiosyncratic powers where creativity beats raw force

The pitch in one line: *Run a squad of strange specialists, send them on expeditions, fight an invasion that doesn't play by your rules.*

---

## 2. World & Setting

### The Gifted World

Magic is a fact of life. People are born with powers — anything from "super strong" to "controls cement" to "can manipulate already-burning flames." Society has adapted: insurance covers clothing-manipulation assaults, schools track students by power class, cartels are organized around dominant gifts, and crafters of magical goods are a normal career.

### The Sundering

Something tore open. *Things* are coming through — entities that don't fit the world's magical taxonomy. Their powers operate on rules nobody understands. Normal humans can't fight them. Even most Gifted can't. Your squad is part of a response organization.

The Sundering provides:
- A central threat with escalation pressure
- An excuse for unusual loot, mysterious tech, and weird enemies
- A reason for the player's squad to exist as a specialist unit
- Long-term narrative payoff (what *is* the Sundering, can it be closed)

### Tone

To be locked in during prototyping. Working direction: **grounded urban-fantasy with pulp combat energy.** Think a world where magic is mundane enough to be regulated, dangerous enough that specialist squads exist, and the invasion brings genuine horror. Not grimdark, not heroic — somewhere in the middle, with room for both serious stakes and the inherent absurdity of fighting a god with a cement backpack.

### Open Worldbuilding Questions
- Modern day, near-future, or alternate-history industrial era?
- One city or multiple regions?
- Are the Gifted a minority or is everyone Gifted?

---

## 3. Core Gameplay Loop

### Session Loop (minutes)
1. Check energy and roster status at base
2. Select an expedition from available contracts
3. Choose squad composition (4 characters)
4. Resolve expedition through encounter sequence (combat + narrative choices)
5. Return with loot, injuries, experience
6. Spend resources at base (heal, craft, train, research)

### Meta Loop (sessions)
1. Build out roster (more characters = more flexibility)
2. Develop characters (techniques, secondary powers, gear)
3. Engage with faction politics (reputation gates content)
4. Track Sundering escalation (regional threat, doom clock)
5. Progress main story through key expeditions

---

## 4. Character System

### Creation
At creation, each character has:
- **Identity:** name, physical description (text), background tag, voice tag
- **Attributes:** point-buy across six stats (see below)
- **Primary Power:** the defining gift (chosen or rolled)
- **Starting Equipment:** light, themed to background
- **Profession Tag:** flavor + minor mechanical effects ("The Scholar," "The Brawler," "The Veteran," "The Smuggler," etc.)

Secondary powers unlock later through story milestones, training, or rare items.

### Attributes

| Attribute | Governs |
|---|---|
| **Power** | Raw output of physical and magical strikes |
| **Control** | Precision of power use, status effect chance, complex techniques |
| **Resolve** | Mental defense, max Strain, resistance to psychic/fear effects |
| **Wits** | Initiative, perception, exploration checks |
| **Reflex** | Action points, dodge chance, ranged accuracy |
| **Vitality** | Max HP, physical resistance, encumbrance capacity |

### Customization Focus
- **Physical features:** text descriptors (height, build, hair, eyes, skin, scars, posture, voice). Generated identity card (silhouette + color palette + power symbol) for visual flair without art assets.
- **Build identity:** power choice, attribute spread, technique loadout, signature item
- **Clothing/cosmetics:** deferred for v1

### Defeat & Recovery (No Permadeath)

When a character drops to 0 HP, they are **Downed** rather than dead. Time-based penalty on return:

| Severity | Downtime | Effect on Return |
|---|---|---|
| **Light Defeat** | 2–4 hours | Reduced max HP for one expedition |
| **Heavy Defeat** | 12–24 hours | Lingering Injury (debuff fading over days) |
| **Catastrophic Defeat** | 24–72 hours or rescue mission | Story scar, possible new minor power |

Downtime can be reduced via base facilities (medbay, healer NPCs, support powers).

---

## 5. The Power System

This is the heart of the game and the highest-priority engineering challenge.

### Structure

Each power has three layers:

**Domain** — broad category:
- Elemental (fire, water, electricity, etc.)
- Material (cement, metal, plants, etc.)
- Biological (super strength, regeneration, etc.)
- Conceptual (manipulate luck, gravity, time-in-small-ways, etc.)
- Kinetic (telekinesis, super speed, force fields, etc.)
- Sensory (heightened senses, telepathy, illusion, etc.)
- Spatial (teleportation, dimensional pockets, etc.)

**Specificity** — how narrow the power is. Narrow powers are stronger but situational:
- *Pyrokinesis* (broad) vs. *Control of Already-Burning Flames* (narrow, stronger when applicable)
- Affects power tier, technique availability, and encounter design

**Expressions** — different ways to use the power. Each power has multiple, unlocked over time:
- **Offense:** how it damages
- **Defense:** how it protects
- **Utility:** out-of-combat applications
- **Support:** how it helps allies
- **Signature:** capstone technique unique to the character's growth

### Expression Unlocking

Two paths:
1. **Natural growth:** repeated use in combat unlocks new expressions ("Used Fire defensively 10 times → Unlock: Searing Aegis")
2. **Insight moments:** narrative events, mentors, books, rival encounters

This rewards creative play. A player who spams the same attack gets fewer options than one who experiments.

### Material/Carry System

Many powers require a medium to manipulate. Carrying that medium is a strategic choice:

- **Material Reserve:** how much fuel/medium a character brings (cement, water, ink, sand, salt, metal shavings, oil, blood vials, etc.)
- **Vitality** governs carry capacity without movement penalty
- **Encumbrance** is soft: over-loading reduces Reflex and movement
- **Resupply** at base or scavenged in-expedition

**Example build implications for a Cement-mage:**
| Build | Loadout | Playstyle |
|---|---|---|
| **Fortress** | Heavy cement pack + plate armor + reserves | Walking bunker, slow, devastating in fixed positions |
| **Skirmisher** | Small flask, light armor | Mobile, environment-dependent, hit-and-run |
| **Environmentalist** | No carried cement | Free movement, completely terrain-locked, scouts maps for usable cement |

Same logic applies to plant-mages (seed pouches), water-mages (canteens), metal-mages (ingots), blood-mages (vials or own HP), ink-mages (inkwells), etc.

Powers that don't require material (telekinesis, super strength, fire generation, sensory powers) have no carry constraints beyond armor.

### Power Catalog Goal

For the vertical slice: **10–15 powers fully fleshed out** (5 expressions each, full expression tree, material rules). Long-term: a curated catalog of ~50 launch powers with room for community/expansion additions.

---

## 6. Combat System

### Structure
Turn-based. Initiative order rolled per encounter based on Wits + Reflex. Each character gets:
- **Move:** changes position between range bands or zones
- **Action:** primary action (attack, technique, item use)
- **Free Action:** minor (drop item, shout, simple gesture)

Higher Reflex grants bonus action points.

### Range Bands (no grid)

Position described in prose using four bands:
- **Engaged:** melee range
- **Near:** short range, a few steps
- **Far:** across the room
- **Distant:** sniper range

Combat log describes positioning naturally: *"The cement-mage stands at Far range from the Echo, behind cover. Your striker is Engaged with two cultists."*

Some powers/abilities collapse range bands (super speed, teleport, grappling hook).

### Zones & Environmental Tags

Each encounter has 2–5 named zones with tags that powers interact with:

| Zone | Tags |
|---|---|
| Rooftop | Elevated, Exposed, Open Sky |
| Alley | Cover, Narrow, Urban |
| Fountain Plaza | Water Source, Open, Urban |
| Warehouse | Cover, Enclosed, Metal Structures |
| Greenhouse | Plant-Rich, Enclosed, Fragile |

Tags drive power interaction. A plant-mage in Greenhouse gets bonuses; in a steel warehouse, they rely on their carry pouch.

### Damage Types

**Physical:** Blunt, Slashing, Piercing, Crushing
**Magical:** Fire, Cold, Lightning, Acid, Force, Psychic, Void/Sundering
**Status/DoT:** Bleeding, Burning, Frozen, Poisoned, Shocked, Corroded, Terrified, Confused, Sundered

Each enemy and armor type has resistances/vulnerabilities expressed as simple multipliers (0.5x, 1x, 1.5x, 2x). Depth comes from damage type variety in the party, not bigger numbers.

Sundering creatures resist conventional damage types in unusual patterns, forcing creative party composition.

### Strain & Backlash

Using powers builds Strain (capped by Resolve). Pushing past the cap triggers Backlash:
- Minor: nosebleed, brief disorientation, small HP loss
- Moderate: power misfire, action lost, status effect on self
- Severe: collapse, character Downed regardless of HP

Strain creates tension around power use — you can't just spam the strongest move.

### Combos

The system rewards setup → payoff interactions:
- Wet enemy → electrify for bonus damage
- Cover enemy in oil → ignite
- Slow enemy with cement → melee finisher gets crit window
- Plant root-bind → archer free-fire window

Encourages party diversity in damage types and expressions.

---

## 7. Expedition System

### Energy

Real-time regeneration (rate TBD during prototyping). Energy is spent to launch expeditions. Different expedition types cost different amounts.

### Expedition Types

| Type | Length | Risk | Reward Profile |
|---|---|---|---|
| **Sweep** | Short | Low | Common gear, currency, minor XP |
| **Delve** | Medium | Medium | Crafting mats, uncommon gear, minor story |
| **Contract** | Medium-High | Medium | Faction reputation, rare gear, story branches |
| **Incursion** | Long | High | Legendary gear, major story, rare materials |
| **Anomaly** | Variable | High | Sundering-related drops, unique encounters, timed |

### Encounter Structure

Each expedition is a node sequence:
- Combat encounter
- Skill check (Wits, Reflex, Power, Control, Vitality, Resolve)
- Narrative branch (choice with consequence)
- Environmental puzzle (often solved by specific power types)
- Optional rest/scavenge node

Branches respond to party composition. *"You have a plant-controller — the overgrown corridor parts before you."* Powers should regularly trivialize content they're suited for. That's the reward for build specialization.

---

## 8. Loot, Crafting & Economy

### Magical Gear

Every weapon and piece of armor has a maker, a story, and potentially a quirk. Examples:
- A sword forged by a Grief-Smith does extra damage when wielded by the bereaved
- Armor woven from a Spider-Gifted's silk resists piercing
- A pistol with bullets crafted by a Pyromancer-Smith inflicts Burning

### Crafting Pathways
- Hire NPC crafters with materials (currency-gated)
- Recruit Gifted crafters into your roster (build-affecting)
- Find pre-made items as expedition loot

### Materials
- Mundane (steel, leather, cloth) — easy
- Magical (essence of fire-elemental, sundered ore, sentient ink) — expedition-gated
- Story (named relics, character-bonded items) — quest-gated

---

## 9. Base / Hub Layer

The player's headquarters. Persistent. Houses:

- **Roster:** view characters, manage assignments, swap squad
- **Medbay:** speeds recovery from defeats and injuries
- **Training Hall:** slowly improve attributes, unlock technique slots
- **Research Lab:** study captured artifacts, learn enemy weaknesses, unlock new crafting recipes
- **Forge / Workshop:** craft and modify gear (requires NPC or recruited crafter)
- **Apothecary:** consumables, healing items, antidotes
- **Quartermaster:** sell loot, buy supplies, restock material reserves
- **Strategic Map:** view faction control, Sundering hot zones, available expeditions
- **Recruitment Hall:** hire new characters or follow leads on rare candidates

Base upgrades unlock through story and resources. Some require Gifted residents (a Cement-mage fortifies your walls, a Plant-mage grows your apothecary, etc.).

---

## 10. Progression

### Character Progression
- **Attributes:** slow, gated by Training Hall + expedition use
- **Expressions:** unlocked through play patterns and insight moments
- **Techniques:** crafted/learned via items, mentors, story events
- **Secondary Power:** unlocked at a major milestone (suggested: character level threshold + story event)
- **Equipment:** primary axis of vertical progression

### Roster Progression
- Recruit more characters over time
- Bench rotation matters (downtime, story, training)
- Bonds between characters (XCOM-style) unlock combat synergies

### Meta Progression
- Faction reputation gates content and merchants
- Base upgrades unlock new options
- Sundering escalation forces strategic prioritization

### Design Principle: Horizontal > Vertical
Late-game enemies should counter common strategies, forcing creative builds and party rotation. Adding a new expression should feel as good as +5 to a stat.

---

## 11. Factions & The Sundering

### Human Factions (placeholder names)
- **The Watch:** official law/military, structured, conservative on power use
- **The Cartels:** organized crime, lots of resources, dangerous if crossed
- **The Sanctum:** mages' guild, knowledge-rich, politically tangled
- **The Free Companies:** mercenary networks, neutral-aligned
- **The Cults:** worship the Sundering, treat invasion as prophecy
- **The Sundered:** former-Gifted altered by exposure, refugees and threats both

Reputation with each unlocks contracts, merchants, and story. Reputation losses bring consequences (hit squads, locked merchants, story doors closed).

### The Sundering — Escalation System

- **Regional Panic:** zones gain Sundering presence over time if ignored
- **Doom Clock:** global threat level rises slowly; high threat unlocks nastier invasion types
- **Anomalies:** timed encounters that reset clocks if completed
- **Story Pillars:** named Sundering entities that drive the main narrative

The player can never fully suppress the Sundering — they're managing pressure, choosing where to push back, accepting losses elsewhere.

---

## 12. Technical Architecture

### Stack
- **Frontend:** React + TypeScript + Tailwind CSS
- **Backend:** Node.js (Express or Fastify) + TypeScript
- **Database:** PostgreSQL (persistent data) + Redis (sessions, energy timers)
- **Hosting:** Vercel (frontend) + Railway/Render (backend) + Supabase or managed Postgres
- **Dev Tools:** VS Code + Claude as pair programmer, GitHub for version control

### Project Structure

```
magic-worlds/
├── client/          React frontend
│   ├── src/
│   │   ├── components/
│   │   ├── screens/
│   │   ├── state/
│   │   └── api/
├── server/          Node backend
│   ├── src/
│   │   ├── routes/
│   │   ├── combat/
│   │   ├── expeditions/
│   │   └── state/
├── shared/          TypeScript types used by both
│   └── types/
├── content/         Data-driven game content (JSON/YAML)
│   ├── powers/
│   ├── enemies/
│   ├── expeditions/
│   └── items/
└── docs/            Design docs (this file lives here)
```

### Architecture Principles

- **Content as data:** powers, enemies, expeditions, and items live in JSON/YAML files, not hardcoded. Adding content shouldn't require code changes.
- **Powers as tagged effects:** instead of writing a function per power, represent powers as bundles of tags that interact with environment tags, enemy tags, and other power tags. This is what makes "wide variety of weird powers" tractable.
- **Combat as a state machine:** clear transitions, replayable logs, easy to debug.
- **Combat log as prose:** the text output IS the game. Combat resolution should produce a readable narrative, not a stat dump.
- **Server-authoritative:** all combat resolution happens on the backend to prevent cheating.

---

## 13. Development Roadmap

### Phase 0: Design Lock (current)
- [x] Concept document (this file)
- [ ] Power system spec (detailed mechanics for the tag/expression system)
- [ ] Combat resolution spec (turn order, damage math, state machine)
- [ ] Data schemas (Character, Power, Expression, Enemy, Expedition, Item)
- [ ] 5 fully-designed example powers as reference

### Phase 1: Vertical Slice
**Goal:** prove the concept is fun before scaling content.

- [ ] Project scaffold (React + Node + TypeScript + shared types)
- [ ] 4 pre-made characters with full data
- [ ] 3 fully-implemented powers (different domains: one elemental, one material, one biological)
- [ ] 1 enemy faction with 3–5 enemy types
- [ ] 1 expedition type (Sweep) with 3 encounter templates
- [ ] Combat system end-to-end (turn order, actions, damage, status effects, defeat)
- [ ] Minimal base screen (roster + launch expedition)
- [ ] Save/load via database

**Success criteria:** can play a full expedition, fight enjoyable combat, return to base, and feel motivated to do it again.

### Phase 2: Depth
- [ ] Strain & Backlash system
- [ ] Material/carry system
- [ ] Expression unlocking
- [ ] Crafting and gear quirks
- [ ] More expedition types
- [ ] Faction reputation
- [ ] More powers (target: 15)

### Phase 3: Scale
- [ ] Sundering threat layer
- [ ] Base upgrades
- [ ] Secondary powers
- [ ] Story expeditions
- [ ] Recruitment system
- [ ] More enemies, more powers, more content

### Phase 4: Polish & Launch
- [ ] Tutorial and onboarding
- [ ] Balance pass
- [ ] Account system and persistence hardening
- [ ] Energy economy tuning
- [ ] Playtesting and iteration

---

## 14. Open Design Questions

Decisions to lock down before deep implementation:

1. **Tone:** grounded urban-fantasy with pulp edge — confirm or adjust?
2. **Setting era:** modern day, near-future, alt-history industrial?
3. **Power roll vs. design:** offer both, or pick one for v1?
4. **Energy regen rate:** how predatory? Once per day, real-time slow regen, or per-session?
5. **Squad size:** locked at 4, or scaling (e.g. 3 early, 4 mid, 5 late)?
6. **Difficulty modes:** Standard / Ironman (permadeath optional) / Story (lower stakes)?
7. **Multiplayer scope:** strictly single-player v1, or async PvP/co-op consideration?
8. **Monetization:** if any — premium one-time, F2P with cosmetics, subscription? (Affects energy design.)
9. **Specificity ratings:** how do narrow powers get balanced against broad? Tier system or case-by-case?
10. **Sundering damage type "Void":** does it have a normal counter or is it the special challenge type?

---

## 15. Inspirations & References

- **XCOM 2 / Long War:** squad management, mission pressure, doom clock
- **Darkest Dungeon:** expedition loop, roster rotation, recovery cycle
- **Torn / Hobo Wars:** browser-based, energy-gated, text-first UI
- **Wildbow's Worm:** specific, weird, mechanically-detailed powers
- **My Hero Academia:** wide variety of quirks, society shaped by powers
- **One Piece:** Devil Fruits as deeply specific abilities
- **Battle Brothers:** tactical depth, equipment matters, characters have identities
- **Citizen Sleeper:** text-driven narrative on a clock with energy management

---

*End of v0.1. Next pass should focus on Power System detailed spec — the highest-risk engineering area.*
