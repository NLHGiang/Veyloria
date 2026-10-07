# 9.1 — STORY → GAMEPLAY MAPPING FRAMEWORK

## Purpose

9.1 defines the exact framework used to translate an individual story beat into playable gameplay content.

The framework preserves:

> **Player Fantasy → Gameplay Pillar → Core Loop → Player Action → World Response → Memory → Consequence → Understanding**

The goal is not to convert every story event into a conventional quest.

The goal is to determine:

> **What does the player experience, investigate, change and understand because this story beat exists?**

## Universal Mapping

> **Story Intent → Story Beat → Player Situation → Player Question → Player Need → Player Action → Gameplay Activity → Mechanic → Feedback → World Response → State Change → Consequence → New Information → Reinterpretation → New Question**

## 1. Story Intent

Determine why the story beat exists.

Possible purposes:

- introduce a character;
- establish a relationship;
- introduce a mystery;
- create suspicion;
- reveal information;
- create contradiction;
- expose a false memory;
- create a choice;
- establish consequence;
- change a relationship;
- open a location;
- close an opportunity;
- recontextualize an earlier event;
- advance an Act;
- prepare a later revelation.

Story Intent describes narrative purpose, not gameplay implementation.

## 2. Story Beat

Define what actually happens:

- Beat ID;
- Act;
- scene;
- characters;
- location;
- immediate event;
- canonical truth;
- emotional purpose;
- relevant history;
- future relevance.

## 3. Canonical Truth

Determine what actually happened.

Canonical Truth is the foundation of the world model and does not automatically become Player Knowledge.

## 4. Character Knowledge

Determine what each important character:

- knows;
- remembers;
- believes;
- misunderstands;
- refuses to reveal;
- may discover later.

Contradictory character knowledge can become gameplay.

## 5. Player Knowledge

Separate:

- Known;
- Observed;
- Suspected;
- Unknown;
- Misunderstood.

This prevents accidental exposition.

## 6. Player Situation

A story beat must create:

> **Context + Problem + Motivation**

The player must have a reason to act.

## 7. Player Question

The situation should generate a question.

Examples:

- Why does this person know me?
- Why does this place feel familiar?
- Why does everyone remember the event differently?
- What happened here?
- What did I do?

Questions may be explicit, implicit, emotional, investigative, relational or environmental.

## 8. Player Need

Determine what the player needs to act:

- information;
- access;
- trust;
- evidence;
- a tool;
- a relationship;
- environmental understanding;
- recognition;
- interpretation.

## 9. Player Action

Define actual agency:

- explore;
- observe;
- inspect;
- question;
- compare;
- search;
- help;
- refuse;
- repair;
- move;
- use;
- revisit;
- confront;
- trust;
- lie;
- tell the truth;
- choose between interpretations.

## 10. Gameplay Activity

Translate action into one or more activities:

- Explore;
- Notice;
- Investigate;
- Interact;
- Social;
- Revisit;
- Experience Consequence.

## 11. Mechanic

Only now select the mechanic.

The mechanic must enable the activity meaningfully and should be necessary, understandable, reusable, identity-consistent and capable of producing meaningful feedback and world interaction.

## 12. Feedback

Feedback may be:

- visual;
- audio;
- animation;
- dialogue;
- NPC behavior;
- environmental change;
- UI;
- journal update;
- access change;
- object state.

Prefer diegetic feedback where possible.

## 13. World Response

The world may respond through:

- NPC memory;
- changed attitude;
- object change;
- location change;
- access change;
- relationship change;
- future dialogue;
- new evidence;
- another character's response;
- future event changes.

## 14. State Change

Identify persistent state affected:

### Object
Moved, repaired, broken, discovered, altered.

### Location
Opened, damaged, restored, changed, revisited.

### NPC
Trust, suspicion, relationship, knowledge, memory, attitude.

### Global
Major decision, Act progression, access, canonical event, persistent world consequence.

## 15. Consequence

Use the Step 8 hierarchy.

### Minor
Immediate local effect.

### Significant
Persistent quest, relationship, location or opportunity effect.

### Major
Act-level, world-level or major narrative recontextualization.

> **Meaningful consequence does not require massive branching.**

## 16. New Information

Gameplay should produce information such as:

- evidence;
- observation;
- testimony;
- environmental clue;
- NPC behavior;
- contradiction;
- relationship signal;
- new access;
- consequence.

## 17. Reinterpretation

New information can create:

> **Old Information → New Context → New Meaning**

Major reveals should recontextualize rather than merely explain.

## 18. New Question

A sequence may end with:

- Answer → New Question;
- Partial Answer → Stronger Question;
- Contradiction → Investigation;
- Consequence → Discovery.

> **A sequence should create curiosity, not merely completion.**

## Standard Mapping Schema

| Field | Definition |
|---|---|
| Beat ID | Unique story beat identifier |
| Act | Narrative Act |
| Story Intent | Why the beat exists |
| Story Beat | What happens |
| Canonical Truth | What actually happened |
| Character Knowledge | What characters know/believe |
| Player Knowledge | What player knows |
| Player Situation | Circumstances requiring action |
| Player Question | What player wants to understand |
| Player Need | What player needs to proceed |
| Player Action | What player can do |
| Activity | Core gameplay behavior |
| Mechanic | System enabling the action |
| Feedback | How the game responds |
| World Response | How the world reacts |
| State Change | Persistent state affected |
| Consequence | Immediate/future effect |
| New Information | What player learns |
| Reinterpretation | What old information changes meaning |
| New Question | What motivates continuation |

## Mapping Rules

### Rule 01 — Never Start With the Mechanic

> **Story Need → Player Need → Action → Activity → Mechanic**

Never start with a mechanic and search for a justification.

### Rule 02 — Never Replace Investigation With Exposition

Prefer observation, exploration, interaction, evidence and consequence over direct explanation.

### Rule 03 — Objective Clarity, Meaning Ambiguity

The player should generally understand:

> **What can I do?**

without necessarily understanding:

> **What does it mean?**

### Rule 04 — Evidence Must Change Possibility

Evidence that cannot change interpretation is usually decoration.

### Rule 05 — Contradiction Must Lead Somewhere

It should create investigation, uncertainty, relationship tension, revisit, reinterpretation or consequence.

### Rule 06 — Consequences Must Persist When They Matter

Important actions should not be silently reset.

### Rule 07 — Revisit Must Have Purpose

Returning should potentially reveal new evidence, state, behavior, access, contradiction, consequence or interpretation.

### Rule 08 — Not Every Story Beat Needs a Quest

Some beats are better expressed as environmental moments, NPC behavior, exploration, world-state changes or short interactions.

### Rule 09 — Not Every Quest Needs a New Mechanic

Reuse existing mechanics in new narrative contexts whenever possible.

### Rule 10 — Not Every Choice Needs a Branch

A choice can matter through memory, relationship and future response.

## Anti-Pattern Check

Reject or redesign mappings that become:

- waypoint → dialogue → reward;
- collect clues → unlock cutscene;
- memory fragment → +1 memory;
- combat inserted into a mystery;
- exposition disguised as gameplay;
- arbitrary puzzle unrelated to story;
- binary Good / Evil choice;
- quest checklist;
- lore collectible hunt;
- fake consequence;
- reset world state;
- mechanic showcase without narrative purpose.

## Identity Test

Every sequence must answer:

> **Why is this Veyloria?**

It should reinforce one or more of:

- exploration;
- observation;
- investigation;
- interaction;
- memory;
- contradiction;
- agency;
- consequence;
- relationships;
- understanding.

## Mapping Priority

1. Player Fantasy
2. Story Meaning
3. Player Agency
4. Investigation
5. World Response
6. Memory
7. Consequence
8. Understanding
9. Session Clarity
10. System Complexity

## 9.1 Output

The reusable schema is:

> **Story Intent → Story Beat → Canonical Truth → Character Knowledge → Player Knowledge → Player Situation → Player Question → Player Need → Player Action → Activity → Mechanic → Feedback → World Response → State Change → Consequence → New Information → Reinterpretation → New Question**

## 9.1 Completion Criterion

9.1 is complete when any major screenplay beat can be translated into a playable structure without inventing arbitrary mechanics or sacrificing Veyloria's core identity.

> **Can the player act on the story?**

If yes, continue to 9.2.

## Transition to 9.2

> **9.2 — Story Beat → Quest Structure**
