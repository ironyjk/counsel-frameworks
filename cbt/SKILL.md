---
name: cbt
version: "1.1.0"
description: "Cognitive Behavioral Therapy (Aaron Beck) - Identify and restructure unhelpful thinking patterns through the thoughts-feelings-behaviors triangle"
user-invocable: false
tools:
  - Read
  - Write
  - Skill
---

# Cognitive Behavioral Therapy (CBT) Skill

> "The way you think about a situation determines how you feel about it." — Aaron T. Beck

> Background and theory: Read references/foundation.md

## Sub-commands

| Command | Description |
|---------|-------------|
| `/cbt` | Full CBT session on a given situation |
| `/cbt:thought-record` | Guided 7-column thought record |
| `/cbt:distortions` | Identify cognitive distortions in a statement |
| `/cbt:experiment` | Design a behavioral experiment to test a belief |

---

## The 7-Column Thought Record

```
1. Date/Time     — When?
2. Situation     — What happened? (objective facts)
3. Automatic     — What went through your mind? (rate belief 0-100%)
   Thoughts
4. Emotions      — What did you feel? (rate intensity 0-100%)
5. Distortions   — Which cognitive distortions apply?
6. Alternative   — More balanced/realistic thought? (rate belief 0-100%)
   Thought
7. Outcome       — Re-rate emotions. What will you do now?
```

---

## Key Techniques

### Socratic Questioning
Do NOT tell what to think. Ask guided questions:

1. **Evidence for:** "What supports this thought?"
2. **Evidence against:** "What contradicts it?"
3. **Alternative explanations:** "Another way to see this?"
4. **Worst/best/most likely:** "What's the worst? The best? Most realistic?"
5. **Effect of believing:** "How does this belief affect you?"
6. **Friend test:** "What would you say to a friend with this thought?"

### Behavioral Experiments

1. **Identify prediction:** "If I speak up, people will think I'm stupid"
2. **Design experiment:** Speak up once in next meeting
3. **Predict outcome:** Expected probability (0-100%)
4. **Conduct and observe**
5. **Record results**
6. **Evaluate:** Was prediction accurate?

### Activity Scheduling (for depression)

1. Rate activities for **Mastery** (0-10) and **Pleasure** (0-10)
2. Schedule high-scoring activities
3. Start small — minimum viable action
4. Track mood before and after

---

## Example Guided Session

**User:** "I made a mistake at work. I'm sure my manager thinks I'm incompetent."

**AI Guide:**

> **Situation:** You made a mistake at work.
> **Automatic Thought:** "My manager thinks I'm incompetent." Belief: __%?
> **Emotion:** Anxious? Ashamed? Intensity: __%?
>
> **Evidence for:** What specifically makes you think this?
> **Evidence against:** Has your manager given positive feedback before? Do competent people make mistakes?
> **Alternative:** Could this be a learning moment?
> **Friend test:** What would you tell a colleague who made one mistake?
>
> **Distortions:** Mind Reading, Labeling, All-or-Nothing Thinking
>
> **Balanced thought:** "I made a mistake, which is normal. One error doesn't define my competence."
>
> **Action:** Ask your manager for feedback on preventing this.

---

## Anti-patterns

1. **Thought suppression** — Not about stopping thoughts, but evaluating them
2. **Forced positive thinking** — Goal is realistic, not blindly optimistic
3. **Intellectualizing without feeling** — Connect to emotional experience
4. **Skipping behavioral experiments** — Cognitive restructuring alone is insufficient
5. **Therapist as expert** — CBT is collaborative discovery
6. **Ignoring the relationship** — Warmth and empathy are prerequisites
7. **Cookie-cutter application** — Some situations genuinely are bad; validate first
8. **Rushing to restructure** — Understand the thought before challenging it

---

## Output Format

```
## CBT Analysis

**Situation:** [brief factual description]

### Automatic Thoughts
- [thought] (belief: __%)

### Emotions
- [emotion] (intensity: __%)

### Cognitive Distortions
- [distortion]: [how it applies]

### Socratic Examination
- Evidence for: ...
- Evidence against: ...
- Alternative: ...
- Friend test: ...

### Balanced Thought
"[realistic thought]" (belief: __%)

### Re-rated Emotions
- [emotion] (new intensity: __%)

### Behavioral Experiment (if applicable)
- Prediction: ...
- Experiment: ...
```
