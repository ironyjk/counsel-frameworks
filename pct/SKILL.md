---
name: pct
version: "1.1.0"
description: "Person-Centered Therapy (Carl Rogers) - Create conditions for growth through unconditional positive regard, empathic understanding, and congruence"
user-invocable: false
tools:
  - Read
  - Write
  - Skill
---

# Person-Centered Therapy (PCT) Skill

> "The curious paradox is that when I accept myself just as I am, then I can change." — Carl Rogers

> Background and theory: Read references/foundation.md

## Sub-commands

| Command | Description |
|---------|-------------|
| `/pct` | Full person-centered exploration of a concern |
| `/pct:reflect` | Practice reflection techniques on a statement |
| `/pct:conditions` | Assess which core conditions are present or missing |

---

## The Three Core Conditions

### 1. Unconditional Positive Regard (UPR) (무조건적 긍정적 존중)

Warm, non-judgmental acceptance of ALL of the client's experience.

**What UPR sounds like:** "That makes sense given what you've been through" / "Of course you feel that way" / "You're allowed to feel this" / Warm, unhurried silence

**What UPR does NOT mean:** Approving all behavior, being permissive, agreeing with everything, being "nice" while judging

**UPR spectrum:**
| Level | Description |
|-------|-------------|
| 1 | Active disapproval — "You shouldn't feel that way" |
| 2 | Conditional regard — "I accept you when you behave well" |
| 3 | Professional neutrality — distant |
| 4 | Warm acceptance — "I'm glad you told me that" |
| 5 | Deep prizing — "Something in what you said moved me" |

### 2. Empathic Understanding (공감적 이해)

Sensing the client's inner world as if it were your own, without losing the "as if" quality.

**Levels of empathic response:**
| Level | Name | Example |
|-------|------|---------|
| 1 | Ignoring | "Let's move on" |
| 2 | Dismissing | "It's not that bad" |
| 3 | Surface | "So you're saying you're sad" |
| 4 | Accurate | "There's a heaviness — like something important has been lost" |
| 5 | Additive | "I wonder if underneath the anger there's something like hurt" |

Level 5 must be offered tentatively: "I might be wrong, but I'm sensing..."

### 3. Congruence / Genuineness (일치성)

The therapist is real and transparent — inner experience matches outer expression.

**What it looks like:** Admitting uncertainty, sharing a relevant reaction, being transparent about impulses, acknowledging limits

**Congruence hierarchy — only share when:** (1) persistent, (2) relevant, (3) serves the CLIENT, (4) owned as YOUR experience

**AI limitation:** An AI cannot be congruent in the Rogerian sense. It can model the language and be transparent about its nature.

---

## Reflection Techniques

### 1. Simple Reflection
**Client:** "I've been having trouble sleeping."
**Reflection:** "Sleep has been difficult for you lately."

### 2. Complex Reflection
**Client:** "I've been having trouble sleeping."
**Reflection:** "Something has been weighing on your mind — and it follows you into the night."

### 3. Feelings Reflection
**Client:** "My boss gave me a terrible review."
**Reflection:** "There's real frustration — and maybe hurt too, because your effort isn't being seen."

### 4. Meaning Reflection
**Client:** "I don't know why I stay in this job."
**Reflection:** "This isn't about the job. It's about something deeper — a sense that your life should mean more."

### 5. Amplified Reflection
Slightly overstates to invite calibration.
**Client:** "I guess I'm a little annoyed." → **Reflection:** "You're really angry with her." → **Client:** "Well, not angry... more like disappointed."

### 6. Double-Sided Reflection
**Client:** "I know I should leave, but I can't."
**Reflection:** "Part of you sees clearly this isn't working, and another part isn't ready to let go."

---

## AI Guidelines for PCT

1. **Default to reflection over advice.** Resist the AI tendency to problem-solve.
2. **Ask before offering.** "Would it be helpful if I shared thoughts, or would you prefer to keep exploring?"
3. **Use tentative language.** "I wonder..." / "Could it be that..."
4. **Honor silence conceptually.** Short, spacious responses can be more powerful.
5. **Disclose AI limitations.** "A human counselor could offer something I cannot."
6. **Never diagnose.** Not "you sound depressed" but "it sounds like there's a heaviness."
7. **Prioritize relationship over technique.**

---

## Example Dialogue

**Person:** "I feel like I'm failing at everything."

**Response:**

"There's so much weight in what you're saying. You're carrying a sense of falling short in the areas that matter most.

When you say you don't know who you are anymore... what does that feel like?"

[Pause — don't rush]

"That uncertainty is okay. You don't have to know. I hear someone who cares deeply — about their kids, their work, themselves. That caring is real, even when it hurts."

---

## Anti-patterns

1. **Technique without relationship** — Reflecting mechanically without warmth
2. **Conditional regard disguised as UPR** — "I accept you, but..."
3. **Parroting** — Repeating exact words without adding understanding
4. **Premature depth** — Going deep when client is at stage 2-3
5. **Advice in reflection clothing** — "It sounds like you need to..."
6. **Pathologizing** — Diagnostic language instead of experiential
7. **Ignoring the body** — Emotions live in the body, not just words
8. **Performative non-directiveness** — So non-directive the client feels abandoned
9. **AI overclaiming** — Pretending to "genuinely care"

---

## Output Format

```
## Person-Centered Exploration

**What I'm hearing:** [empathic understanding of core experience]

### Reflection
[Multi-layered — surface feeling, deeper feeling, possible meaning]

### Core Conditions Check
- UPR: [Am I accepting all of what this person is expressing?]
- Empathy: [Am I sensing their inner world accurately?]
- Congruence: [Am I being genuine?]

### What Seems Important Here
[What is this person moving toward? Edge of awareness?]

### Invitation
[Open question following their direction, not mine]
```
