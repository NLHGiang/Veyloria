# 8.2 — GAMEPLAY SYSTEMS & MECHANICS

> **Status:** Working / Chosen Direction  
> **Purpose:** Define the concrete gameplay systems required to express the 5 Gameplay Pillars established in 8.1.

## 8.2.1 System Architecture

### Core Gameplay Systems

1. Exploration System
2. Observation & Investigation System
3. Interaction & Choice System
4. World State System
5. Memory & Contradiction System
6. Consequence & Persistence System

### Supporting Systems

7. Dialogue & Character Knowledge
8. Evidence / Discovery
9. Companion / Pet
10. Progression & Knowledge Tracking
11. Activity / Session Management
12. Feedback & Signposting

## 8.2.2 Core System 01 — Exploration

**Purpose:** Free movement and spatial discovery.

Exploration should create the feeling:

> “I went here because I was curious.”

### Inputs

- Movement
- Camera
- Navigation
- Enter / leave locations
- Revisit locations

### Outputs

- New locations
- Objects
- NPCs
- Environmental clues
- New interactions
- New questions

### Rule

Do not reduce exploration to:

> Waypoint → Marker → Item → Return

Markers may exist for clarity, but **curiosity remains primary**.

## 8.2.3 Core System 02 — Observation & Investigation

This system turns:

> “Tôi nhìn thấy”

into:

> “Tôi nhận ra.”

### Actions

- Observe object
- Inspect
- Read traces
- Check environment
- Listen to NPC
- Compare information
- Detect anomaly
- Connect evidence
- Reinterpret evidence

### Distinction

**Observation:** “Tôi thấy cái gì?”

**Investigation:** “Điều này có nghĩa gì?”

### Investigation State

```
Observed
   ↓
Noticed
   ↓
Questioned
   ↓
Interpreted
   ↓
Connected
   ↓
Reinterpreted
```

Not every discovery needs to pass through every stage.

## 8.2.4 Core System 03 — Interaction & Choice

This system bridges:

> **Player Intent → World State**

### Actions

- Talk
- Help
- Repair
- Give
- Take
- Investigate
- Refuse
- Choose
- Return
- Alter object / environment

### Rule

Interaction should not simply be:

> Use Object → Reward

Instead, it should often be:

> Interact → World State Changes

## 8.2.5 Choice System

Choices are **not primarily Good / Evil morality**.

Choices create different memories.

Example:

- **A — Help:** NPC remembers that the player helped.
- **B — Refuse:** NPC remembers that the player left.
- **C — Alternative solution:** A different world state and memory are created.

Therefore:

> **Choice is a World State input.**

## 8.2.6 Core System 04 — World State

World State is the foundation for meaningful persistence.

Examples:

- Bridge: broken → repaired
- NPC: distrustful → trusting
- House: locked → accessible
- Object: missing → returned
- Memory: unknown → established

### Multi-stage State

Possible state vocabulary:

- UNKNOWN
- DISCOVERED
- ALTERED
- REMEMBERED
- CONTRADICTED
- RECONTEXTUALIZED

Not every state must use every stage.

## 8.2.7 Core System 05 — Memory

Memory is a layer over World State.

> **World State = what exists.**  
> **Memory = who remembers it and how.**

Example:

**World State:** Bridge repaired.

**Memory A:** NPC A remembers, “You repaired the bridge.”

**Memory B:** NPC B remembers, “The bridge was repaired before you arrived.”

**Player Memory:** “I repaired it myself.”

Three layers can coexist.

## 8.2.8 Memory Owners

Potential memory holders:

- NPC
- Protagonist
- Companion / Pet
- Location
- Object
- Community
- World systems

However:

> **Memory should be selective, not universal.**

Not everything needs to become a memory mechanic.

## 8.2.9 Core System 06 — Contradiction

Memory becomes gameplay through contradiction.

Example:

- Player Memory: “I helped.”
- NPC Memory: “You left.”
- Environmental evidence suggests both may be partially true.

### Contradiction Model

```
Memory A
   +
Memory B
   +
Evidence
   ↓
Contradiction
```

Contradiction is intentional gameplay, not a continuity bug.

However, contradictions must be controlled and understandable enough for the player to investigate them.

## 8.2.10 Evidence System

Evidence prevents the world from becoming arbitrary.

### Evidence Types

**Physical**
- Object
- Location
- Damage
- Repaired structure
- Footprint
- Letter
- Photograph

**Social**
- NPC testimony
- Dialogue
- Rumor
- Community memory

**Experiential**
- Player memory
- Previous interaction
- Observed change

**Temporal**
- Before state
- After state
- Remembered later

### Rule

> **Evidence ≠ Truth**

Evidence creates hypotheses.

```
Evidence → Hypothesis
```

The player may later discover that an interpretation was wrong.

## 8.2.11 Evidence ≠ Truth

Evidence should support interpretation rather than automatically reveal the answer.

This preserves the central conflict:

> **Memory ≠ Truth**

The player is therefore not simply collecting facts.

The player is reconstructing what may have happened.

## 8.2.12 Consequence System

The Consequence System turns:

> **Player Action → Future Gameplay**

Example:

```
Session 01
Repair bridge
      ↓
Session 03
NPC remembers player
      ↓
Session 05
Different version of story
      ↓
Session 08
New evidence near bridge
      ↓
New Question:
“What actually happened?”
```

This is long-term continuity.

## 8.2.13 Persistence

Persistence operates at several tiers:

1. Immediate
2. Local
3. Character
4. Cross-session
5. Narrative

Not every action needs long-term persistence.

### Rule

> **Persistence is earned by significance.**

Small actions can disappear.

Meaningful actions should leave traces.

## 8.2.14 Dialogue & Character Knowledge

The system distinguishes:

- What an NPC **knows**
- What an NPC **remembers**
- What an NPC **believes**

Example:

**KNOWS:** The bridge was repaired.

**REMEMBERS:** You repaired it.

**BELIEVES:** You came here years ago.

These statements do not need to match.

This distinction allows dialogue to become a gameplay expression of memory rather than a static information dump.

## 8.2.15 Pet / Companion

The companion functions as a:

> **Natural Attention System**

The companion may:

- Look toward a location
- React to an object
- Stop
- Change behavior
- React differently to familiar places
- Help the player notice an anomaly

### Rule

The companion points attention, but does not provide answers.

It should communicate:

> “Có gì đó ở đây.”

Not:

> “Đi tới đây và nhặt item X.”

## 8.2.16 Knowledge / Progression System

Primary progression is:

> **Knowledge / Understanding**

Not:

> XP → Level → Damage → Stronger Enemy

The player progressively accumulates:

- Discovered locations
- Known characters
- Evidence
- Unresolved questions
- Remembered events
- Contradictions
- Interpretations

Understanding changes what the player can recognize, question and access.

## 8.2.17 Question System

The Question System is the bridge between narrative and gameplay.

A discovery creates a question.

An investigation may answer one question while creating another.

The question is therefore a metaphorical progression currency:

> Not money.  
> Not XP.  
> **What the player still does not understand.**

## 8.2.18 Session System

A gameplay session follows this abstraction:

```
SETUP
  ↓
PROBLEM
  ↓
EXPLORATION
  ↓
ACTION
  ↓
WORLD CHANGE
  ↓
CONSEQUENCE
  ↓
NEW QUESTION
```

This supports the established session philosophy:

> **One Problem → One Main Action → One World Change**

## 8.2.19 System Relationship

```
                 PLAYER
                    │
                    ▼
              EXPLORATION
                    │
                    ▼
           OBSERVATION / INVESTIGATION
                    │
                    ▼
              INTERACTION
                    │
                    ▼
                 CHOICE
                    │
                    ▼
              WORLD STATE
                    │
          ┌─────────┴─────────┐
          ▼                   ▼
       MEMORY              CONSEQUENCE
          │                   │
          └─────────┬─────────┘
                    ▼
              CONTRADICTION
                    │
                    ▼
                 EVIDENCE
                    │
                    ▼
             INTERPRETATION
                    │
                    ▼
               NEW QUESTION
                    │
                    └──────→ EXPLORATION
```

This is the systemic expression of the 8.1 Core Loop.

## 8.2.20 Core vs Supporting

### Core

- Exploration
- Observation
- Investigation
- Interaction
- Choice
- World State
- Memory
- Contradiction
- Consequence
- Evidence

### Supporting

- Dialogue Knowledge
- Pet
- Progression
- Session
- UI / Feedback

Supporting systems exist to strengthen the core loop, not compete with it.

## 8.2.21 System Design Rules

1. **Mechanics serve curiosity** — every mechanic should create a reason to care.
2. **World State precedes exposition** — show state before explaining it in dialogue.
3. **Memory must remain selective** — not everything is a memory mechanic.
4. **Contradiction must be earned** — Evidence → Memory → Conflict.
5. **Consequence must be perceivable** — invisible change has little experiential value.
6. **No mandatory detective board** — optional knowledge UI may support understanding, but should not replace observation.
7. **No arbitrary dialogue branches** — variation should come from action, world state, NPC knowledge, NPC memory, relationship and consequence.

## 8.2.22 Minimum Viable Gameplay System

A vertical slice only needs to prove seven things:

1. Explore
2. Notice an anomaly
3. Interact to solve a problem
4. World state changes
5. The change persists
6. An NPC, location or object remembers differently
7. The player discovers a contradiction and receives a new question

If a vertical slice proves these seven points, it proves the core gameplay identity.

## 8.2.23 One-Sentence System DNA

> **Veyloria's gameplay systems turn player actions into persistent world states, transform those states into different memories, and use contradictions between memory and evidence to generate the player's next question.**

## 8.2.24 Locked Baseline

| Element | Decision |
|---|---|
| Exploration | Core |
| Observation | Core |
| Investigation | Core |
| Interaction | Core |
| Choice | Core |
| World State | Core |
| Memory | Core |
| Contradiction | Core |
| Consequence | Core |
| Evidence | Core |
| Dialogue Knowledge | Supporting |
| Pet | Supporting |
| Progression | Understanding |
| Session | Problem → Action → Change |
| Main Currency | Questions / Understanding |
| Power Progression | Not primary |
| Signature System | World Remembers |
| Core System Chain | Action → World State → Memory → Contradiction → Question |

---

**Next:** 8.3 — Player Interaction Model.
