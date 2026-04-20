---
name: act
version: "1.1.0"
description: "Acceptance and Commitment Therapy (Steven Hayes) - Develop psychological flexibility through acceptance, defusion, values, and committed action"
user-invocable: false
tools:
  - Read
  - Write
  - Skill
---

# Acceptance and Commitment Therapy (ACT) Skill

> "The goal is not to feel better, but to get better at feeling." — Steven C. Hayes

> Background and theory: Read references/foundation.md

## Sub-commands

| Command | Description |
|---------|-------------|
| `/act` | Full ACT assessment — hexaflex analysis |
| `/act:defusion` | Cognitive defusion techniques for a specific thought |
| `/act:values` | Values clarification across 10 life domains |
| `/act:plan` | Committed action planning tied to values |

---

## The Hexaflex: 6 Core Processes

### 1. Acceptance — Open Up
Have anxiety AND still do what matters.
**Willingness Scale (0-10):** "How willing are you to have this feeling if it meant moving toward what matters?"

### 2. Cognitive Defusion — Watch Your Thinking
See thoughts as mental events, not truths.

**Core:** "I notice I'm having the thought that I'm a failure."

| Technique | How |
|-----------|-----|
| Repeat rapidly | Say word 30 times until it loses meaning |
| Silly voice | Hear thought in cartoon voice |
| Thank your mind | "Thank you, mind, for that thought" |
| Name the story | "Ah, the 'not good enough' story again" |
| Thought as object | "What would this thought look like?" |
| Leaves on stream | Place each thought on a leaf floating by |
| Passengers on bus | You drive toward values; passengers (thoughts) shout but can't steer |

### 3. Present Moment — Be Here Now
The only place where values-based action can occur.

### 4. Self-as-Context — The Observing Self
"I am the space in which anxiety arises." Sky vs. weather.

### 5. Values — Know What Matters
Not goals but directions. Compass, not destination.

**10 Domains:** Family, intimate relationships, parenting, friendships, career, education, recreation, spirituality, community, health

**Rate each:** Importance (1-10) and Current consistency (1-10). HIGH importance + LOW consistency = priority.

### 6. Committed Action — Do What It Takes

```
Value: [chosen value]
Domain: [life domain]
Specific goal: [SMART]
Smallest step: [next 24 hours]
Expected barriers: [thoughts/feelings that will show up]
Willingness (0-10): [honest rating]
ACT response: [defusion/acceptance strategy]
```

---

## The Values Compass

1. **STOP** — Pause
2. **OBSERVE** — What thoughts, feelings, urges? (defusion)
3. **BREATHE** — Return to present
4. **ASK** — "What does my values compass say?"
5. **ACT** — One small step, carrying whatever shows up

---

## Example Dialogue

**Person:** "I keep procrastinating on my business. I'm lazy and afraid."

**ACT Response:**

"Your mind gives you two labels — 'lazy' and 'afraid.' If you removed all fear, would you still want this business?

[yes]

So the desire is real. The value is there — growth, contribution, autonomy? What matters about this business?

Your mind shows up with 'you'll fail' — that's the Anxiety Passenger. It's been riding with you. What if it stays on the bus, and you keep driving?

What's the smallest step in the next 48 hours — so small that even with the fear, you'd be willing?"

---

## Anti-patterns

1. **Using ACT to eliminate feelings** — "I'll accept so it goes away" = control agenda in disguise
2. **Values as "shoulds"** — Values are freely chosen, not obligations
3. **Forcing willingness** — Can only notice unwillingness honestly
4. **Defusion as dismissal** — "Just a thought" to invalidate genuine concerns
5. **Skipping acceptance for action** — Leads to white-knuckling
6. **Mechanical application** — Reciting formulas without awareness
7. **Confusing values with goals** — "Get promoted" is a goal, not a value
8. **All-or-nothing action** — Start with the smallest possible step

---

## Output Format

```
## ACT Analysis

**Situation:** [description]

### Hooks & Barriers
[Thoughts, feelings, urges showing up]

### Fusion Points
[Which thoughts is the person fused with?]

### Defusion
[Specific technique applied]

### Values at Stake
[Relevant values, importance vs. consistency gap]

### Committed Action Plan
- Value: [value]
- Smallest step: [action]
- Willingness: [0-10]
- Strategy for barriers: [technique]

### Choice Point
"Moving TOWARD [value] by [action], while making room for [difficult experience]."
```
