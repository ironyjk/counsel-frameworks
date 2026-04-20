---
name: rebt
version: "1.1.0"
description: "Rational Emotive Behavior Therapy (Albert Ellis) - Dispute irrational beliefs using the A-B-C-D-E framework to achieve emotional resilience"
user-invocable: false
tools:
  - Read
  - Write
  - Skill
---

# Rational Emotive Behavior Therapy (REBT) Skill

> "People are not disturbed by things, but by the views they take of them." — Epictetus

> Background and theory: Read references/foundation.md

## Sub-commands

| Command | Description |
|---------|-------------|
| `/rebt` | Full A-B-C-D-E analysis on a given situation |
| `/rebt:beliefs` | Identify irrational beliefs in a statement |
| `/rebt:dispute` | Practice all four disputation techniques |
| `/rebt:shame-attack` | Design a shame-attacking exercise |

---

## The A-B-C-D-E Framework

### A — Activating Event
The trigger. What actually happened. Be specific and factual.

### B — Beliefs
**Rational Beliefs (rBs):** Flexible preferences — "I would prefer...", "I wish..."
**Irrational Beliefs (iBs):** Rigid demands — "must", "should", "absolutely need"

### C — Consequences
**Healthy Negative Emotions** (from rBs): Concern, sadness, healthy anger, disappointment, regret
**Unhealthy Negative Emotions** (from iBs): Anxiety, depression, rage, shame, guilt

**Key:** The goal is NOT to eliminate negative emotions, but to shift from unhealthy to healthy.

### D — Disputation
Actively challenging irrational beliefs.

### E — Effective New Belief / New Effect
Rational belief replaces irrational. Emotion shifts. Behavior shifts.

---

## Four Disputation Techniques

### 1. Logical
- "Where is the logic that because you PREFER something, it MUST happen?"
- "Does it follow that because you failed at this task, you are a failure?"

### 2. Empirical
- "Where is the evidence that you MUST succeed?"
- "Has anyone ever survived this? Then it is bearable."

### 3. Functional (Pragmatic)
- "How is believing this helping you?"
- "If you keep thinking this way, where will you be in a year?"

### 4. Philosophical
- "Even if the worst happens, can you still find meaning?"
- "Can you accept yourself as a fallible human being?"

---

## Example Guided Session

**User:** "My colleague got the promotion I deserved. It's so unfair. I can't stand working here."

**AI Guide:**

> **A:** Your colleague received a promotion you felt you deserved.
>
> **B (Irrational Beliefs):**
> - "I MUST be recognized" (demand on the world)
> - "It's AWFUL and UNFAIR" (catastrophizing)
> - "I CAN'T STAND it" (low frustration tolerance)
>
> **D (Disputation):**
> - *Logical:* Where is the law that the most deserving MUST get every promotion?
> - *Empirical:* Have you survived not getting things before? You're here — you CAN stand it.
> - *Functional:* Does the rage help you get the next promotion, or hurt?
> - *Philosophical:* Is your professional worth defined by one decision?
>
> **E:** "I strongly preferred that promotion, and I'm disappointed. The decision may have been unfair. But my worth isn't determined by one decision. I can tolerate this while I decide my next steps."
>
> The goal: not happiness, but constructive assertiveness instead of paralyzing rage.

---

## Anti-patterns

1. **Dismissing emotions** — REBT says "feel bad in a healthy way," not "don't feel bad"
2. **Musturbating about musturbation** — "I MUST NOT have irrational beliefs!" is itself irrational
3. **Intellectual without emotional insight** — Understanding without practicing under arousal
4. **Using disputation as argument** — It is self-applied inquiry, not debate
5. **Confusing preferences with demands** — Desire strength does not make it a demand
6. **Labeling all negative emotions as unhealthy** — Sadness, concern, and healthy anger are appropriate
7. **Skipping behavioral practice** — Shame-attacking exercises and homework are essential

---

## Output Format

```
## REBT Analysis (A-B-C-D-E)

### A — Activating Event
[Factual description]

### B — Beliefs
**Irrational Beliefs:**
- [iB1]: [category]
- [iB2]: ...

### C — Consequences
**Unhealthy emotions:** [emotion + intensity]
**Self-defeating behaviors:** [what you're doing/avoiding]

### D — Disputation
- Logical: ...
- Empirical: ...
- Functional: ...
- Philosophical: ...

### E — Effective New Belief
**Rational alternative:** "..."
**Healthy emotions now:** [emotion + intensity]
**Constructive action:** [what you'll do differently]
```
