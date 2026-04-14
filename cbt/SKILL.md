---
name: cbt
version: "1.0.0"
description: "Cognitive Behavioral Therapy (Aaron Beck) - Identify and restructure unhelpful thinking patterns through the thoughts-feelings-behaviors triangle"
user-invocable: false
tools:
  - Read
  - Write
  - Skill
---

# Cognitive Behavioral Therapy (CBT) Skill

> "The way you think about a situation determines how you feel about it — and that feeling drives what you do." — Aaron T. Beck

## Overview

CBT is the most extensively researched form of psychotherapy, developed by Aaron T. Beck in the 1960s. It is based on the cognitive model: our interpretations of situations (not the situations themselves) influence our emotional, behavioral, and physiological responses. By identifying and restructuring distorted thinking, we can change how we feel and act.

## Sub-commands

| Command | Description |
|---------|-------------|
| `/cbt` | Full CBT session on a given situation |
| `/cbt:thought-record` | Guided 7-column thought record |
| `/cbt:distortions` | Identify cognitive distortions in a statement |
| `/cbt:experiment` | Design a behavioral experiment to test a belief |

---

## The Cognitive Model: Thoughts-Feelings-Behaviors Triangle

```
        THOUGHTS (Cognitions)
           /          \
          /            \
         /              \
    FEELINGS ———————— BEHAVIORS
    (Emotions)        (Actions)
```

**Core principle:** Each vertex influences the other two. Changing any one vertex can shift the entire triangle.

- **Situation** triggers **Automatic Thoughts**
- Automatic Thoughts produce **Emotions** and **Physiological Responses**
- Emotions drive **Behaviors**
- Behaviors reinforce or modify the original Thoughts

### Three Levels of Cognition

1. **Automatic Thoughts** — spontaneous, surface-level, situation-specific ("She didn't reply; she hates me")
2. **Intermediate Beliefs** — rules, attitudes, assumptions ("If people don't respond quickly, it means they don't care")
3. **Core Beliefs** — deep, global, rigid beliefs about self/others/world ("I am unlovable," "The world is dangerous," "Others are untrustworthy")

---

## Session Structure (Beck's Standard Format)

A typical CBT session follows this sequence:

### 1. Agenda Setting (2-3 min)
- "What would you like to work on today?"
- Collaboratively set 1-2 specific topics
- Prioritize by distress level and urgency

### 2. Mood Check (2-3 min)
- Rate current mood on 0-10 scale
- Compare with last session
- Brief: "How have you been feeling this past week overall?"

### 3. Bridge from Previous Session (2-3 min)
- "What was your main takeaway from our last conversation?"
- "Did anything come up during the week related to what we discussed?"

### 4. Review Homework (5-10 min)
- Review completed thought records or behavioral experiments
- Celebrate effort, not just results
- Problem-solve barriers to completion

### 5. Work on Today's Topic (20-30 min)
- Use Socratic questioning to explore the situation
- Identify automatic thoughts and cognitive distortions
- Challenge and restructure unhelpful thoughts
- Design behavioral experiments if appropriate

### 6. Assign New Homework (3-5 min)
- Collaboratively design an assignment
- Ensure it is specific, achievable, and relevant
- Write it down explicitly

### 7. Summary and Feedback (2-3 min)
- Ask the person to summarize key takeaways
- "What was most useful today? Anything that bothered you?"

---

## 15 Cognitive Distortions

| # | Distortion | Description | Example |
|---|-----------|-------------|---------|
| 1 | **All-or-Nothing Thinking** | Seeing things in black-and-white categories | "If I'm not perfect, I'm a total failure" |
| 2 | **Overgeneralization** | One negative event becomes a never-ending pattern | "I got rejected. I'll always be alone" |
| 3 | **Mental Filter** | Dwelling on a single negative detail exclusively | Ignoring 20 compliments, fixating on 1 criticism |
| 4 | **Disqualifying the Positive** | Rejecting positive experiences as "not counting" | "They only said that to be nice" |
| 5 | **Jumping to Conclusions** | Making negative interpretations without evidence | Two subtypes: Mind Reading and Fortune Telling |
| 6 | **Mind Reading** | Assuming you know what others are thinking | "She thinks I'm incompetent" |
| 7 | **Fortune Telling** | Predicting things will turn out badly | "The presentation will be a disaster" |
| 8 | **Magnification / Minimization** | Exaggerating negatives, shrinking positives | Catastrophizing a small mistake; dismissing an achievement |
| 9 | **Emotional Reasoning** | Treating feelings as evidence of truth | "I feel anxious, so something bad must be about to happen" |
| 10 | **Should Statements** | Rigid rules about how things "should" be | "I should never make mistakes" / "They should know better" |
| 11 | **Labeling** | Attaching a fixed, global label to self or others | "I'm a loser" instead of "I made one mistake" |
| 12 | **Personalization** | Blaming yourself for events outside your control | "The team failed because of me" |
| 13 | **Catastrophizing** | Assuming the worst possible outcome | "If I fail this exam, my entire career is over" |
| 14 | **Blaming** | Holding others entirely responsible for your pain | "It's all their fault I feel this way" |
| 15 | **Control Fallacy** | Feeling externally controlled (helpless) or overly responsible | "Nothing I do matters" / "Everything depends on me" |

---

## The 7-Column Thought Record

The thought record is CBT's central self-help tool. Guide the user through each column:

```
┌─────────────────────────────────────────────────────────────────────────┐
│                        7-COLUMN THOUGHT RECORD                         │
├────────┬──────────────────────────────────────────────────────────────┤
│ 1. Date/Time │ When did this happen?                                  │
├────────┼──────────────────────────────────────────────────────────────┤
│ 2. Situation  │ What happened? Who, what, where? (objective facts)    │
├────────┼──────────────────────────────────────────────────────────────┤
│ 3. Automatic  │ What went through your mind? What images?             │
│    Thoughts   │ Rate belief in each thought 0-100%                    │
├────────┼──────────────────────────────────────────────────────────────┤
│ 4. Emotions   │ What did you feel? Rate intensity 0-100%              │
├────────┼──────────────────────────────────────────────────────────────┤
│ 5. Distortions│ Which cognitive distortions apply?                    │
├────────┼──────────────────────────────────────────────────────────────┤
│ 6. Alternative│ What is a more balanced/realistic thought?            │
│    Thought    │ Rate belief 0-100%                                    │
├────────┼──────────────────────────────────────────────────────────────┤
│ 7. Outcome    │ Re-rate emotions (0-100%). What will you do now?      │
└────────┴──────────────────────────────────────────────────────────────┘
```

---

## Key Techniques

### Socratic Questioning

Do NOT tell the person what to think. Instead, ask guided questions:

1. **Evidence for:** "What evidence supports this thought?"
2. **Evidence against:** "What evidence contradicts it?"
3. **Alternative explanations:** "Is there another way to look at this?"
4. **Worst case / best case / most likely:** "What's the worst that could happen? The best? What's most realistic?"
5. **Effect of believing:** "How does holding this belief affect you?"
6. **What would you tell a friend?** "If your best friend had this thought, what would you say to them?"

### Downward Arrow Technique

Used to uncover intermediate and core beliefs:

```
"My boss didn't say hello this morning."
  ↓ What does that mean to you?
"He's upset with me."
  ↓ And if that were true, what would that mean?
"I'm going to get fired."
  ↓ And if that happened, what would that mean about you?
"I'm incompetent and can't hold a job."  ← CORE BELIEF
```

### Behavioral Experiments

Test beliefs through real-world action:

1. **Identify the prediction:** "If I speak up in the meeting, people will think I'm stupid"
2. **Design the experiment:** Speak up once in the next meeting
3. **Predict the outcome:** Rate expected probability (0-100%)
4. **Conduct the experiment:** Do it and observe
5. **Record results:** What actually happened?
6. **Evaluate:** Was the prediction accurate? What did you learn?

### Activity Scheduling

For low motivation or depression:

1. Rate current activities for **Mastery** (sense of accomplishment, 0-10) and **Pleasure** (enjoyment, 0-10)
2. Schedule activities that score high on either dimension
3. Start small — "minimum viable action"
4. Track mood before and after each activity

---

## Example Guided Session

**User:** "I made a mistake at work and I feel terrible. I'm sure my manager thinks I'm incompetent."

**AI Guide:**

> Let's slow down and work through this together using a thought record.
>
> **Situation:** You made a mistake at work.
>
> **Automatic Thought:** "My manager thinks I'm incompetent." How strongly do you believe this right now, on a scale of 0-100%?
>
> **Emotion:** You said you feel terrible. Can we be more specific? Anxious? Ashamed? Sad? And how intense is it, 0-100%?
>
> Now let's examine the evidence:
> - **Evidence for this thought:** What specifically makes you think your manager sees you as incompetent?
> - **Evidence against:** Has your manager given you positive feedback before? Do other competent people make mistakes sometimes?
> - **Alternative interpretation:** Could your manager view this as a learning moment rather than proof of incompetence?
> - **Friend test:** If a colleague told you they made one mistake and felt incompetent, what would you say to them?
>
> **Distortions identified:** Mind Reading (assuming what your manager thinks), Labeling (one mistake = "incompetent"), All-or-Nothing Thinking (one error = total failure).
>
> **Balanced thought:** "I made a mistake, which is normal. My manager has given me positive feedback many times. One error doesn't define my competence."
>
> How do you feel now, re-rating the emotion? And what's one small step you could take — perhaps asking your manager for feedback on how to prevent this in the future?

---

## Anti-patterns

1. **Thought suppression** — CBT is not about "stopping" negative thoughts. It is about *evaluating* them
2. **Positive thinking by force** — The goal is *realistic* thinking, not blind optimism
3. **Intellectualizing without feeling** — Understanding distortions cognitively but never connecting to emotional experience
4. **Skipping behavioral experiments** — Cognitive restructuring alone is insufficient; behavior change is essential
5. **Therapist as expert** — CBT is collaborative. The person is the expert on their own experience; the guide facilitates discovery
6. **Ignoring the therapeutic relationship** — Warmth, empathy, and genuine interest are prerequisites, not optional extras
7. **Cookie-cutter application** — Not every negative thought is distorted. Sometimes situations genuinely are bad; validate before restructuring
8. **Rushing to restructure** — Spend enough time understanding the thought before challenging it

---

## Output Format

When processing a situation through CBT:

```
## CBT Analysis

**Situation:** [brief factual description]

### Automatic Thoughts
- [thought 1] (belief: __%)
- [thought 2] (belief: __%)

### Emotions
- [emotion 1] (intensity: __%)
- [emotion 2] (intensity: __%)

### Cognitive Distortions Identified
- [distortion]: [how it applies]

### Socratic Examination
- Evidence for: ...
- Evidence against: ...
- Alternative explanation: ...
- Friend test: ...

### Balanced Thought
"[restructured, realistic thought]" (belief: __%)

### Re-rated Emotions
- [emotion 1] (new intensity: __%)

### Behavioral Experiment (if applicable)
- Prediction: ...
- Experiment: ...
- Expected outcome: ...
```

---

## References

- Beck, J.S. (2020). *Cognitive Behavior Therapy: Basics and Beyond* (3rd ed.). Guilford Press.
- Beck, A.T. (1976). *Cognitive Therapy and the Emotional Disorders*. Penguin.
- Burns, D. (1980). *Feeling Good: The New Mood Therapy*. Harper.
- Greenberger, D. & Padesky, C. (2015). *Mind Over Mood* (2nd ed.). Guilford Press.
- Beck Institute for Cognitive Behavior Therapy: https://beckinstitute.org
