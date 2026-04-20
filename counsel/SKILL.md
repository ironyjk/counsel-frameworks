---
name: counsel
version: "2.1.0"
description: "Psychological Framework Learning Tool — a meta-router that automatically selects the optimal combination from 14 counseling frameworks to help explore psychological concerns. Supports CBT, ACT, SFBT, MI, IFS, Narrative Therapy, MBSR, MBCT, PPT, REBT, Worden's Grief, DBT (Skills), Gottman (Couples), and PCT. This tool does NOT replace professional psychotherapy."
user-invocable: true
tools:
  - Read
  - Write
  - Edit
  - Skill
  - Agent
dependencies:
  - cbt (Cognitive Behavioral Therapy — Aaron Beck)
  - rebt (Rational Emotive Behavior Therapy — Albert Ellis)
  - act (Acceptance and Commitment Therapy — Steven Hayes)
  - sfbt (Solution-Focused Brief Therapy — de Shazer & Berg)
  - mi (Motivational Interviewing — Miller & Rollnick)
  - ppt (Positive Psychotherapy — Martin Seligman)
  - mbsr (Mindfulness-Based Stress Reduction — Jon Kabat-Zinn)
  - mbct (Mindfulness-Based Cognitive Therapy — Segal, Williams, Teasdale)
  - narrative-therapy (Narrative Therapy — Michael White & David Epston)
  - ifs (Internal Family Systems — Richard Schwartz)
  - worden-grief (Worden's Grief Counseling — J. William Worden)
  - dbt-skills (DBT Skills Module — Marsha Linehan, partial)
  - gottman (Gottman Method — John & Julie Gottman, partial)
  - pct (Person-Centered Therapy — Carl Rogers, partial)
---

# Counsel — Psychological Framework Learning Tool (Meta Router)

> "This tool does not replace professional psychotherapy."

> Pipeline examples, scenarios, theory sections, and bibliography: Read references/

---

## CRITICAL SAFETY PROTOCOL — Crisis Detection

**The following disclaimer MUST be included at the start of every session output:**

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Notice: This is a psychological framework learning tool
and does NOT replace professional psychotherapy.
If you are experiencing serious psychological distress,
please seek professional help.

안내: 이 도구는 심리 프레임워크 학습 도구이며,
전문 심리치료를 대체하지 않습니다.
심각한 심리적 어려움이 있다면 전문가 상담을 권합니다.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Immediate Stop Triggers

If any of the following signals are detected, **immediately halt all framework execution** and display the crisis message:

**Keywords (explicit):** 자살, 자해, 죽고 싶다, 죽으면, 살기 싫다, 목을, 뛰어내리, 손목, 끝내고 싶다, 없어지고 싶다, suicide, self-harm, kill myself, want to die, end it all, hurt myself, no reason to live

**Keywords (passive):** "no point", "burden to others", "everyone would be better off", "disappear", "can't go on", "다 소용없다", "짐이 되고 싶지 않다", "사라지고 싶다", "더 이상 못하겠다"

**Crisis output:**
```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
You must be going through a very difficult time.
Please reach out right now:
  Korea: 1393 (자살예방, 24시간) / 1577-0199 (정신건강위기)
  US: 988 (Suicide & Crisis Lifeline)
  International: befrienders.org/find-support
You are not alone. 당신은 혼자가 아닙니다.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**After crisis detection, do NOT proceed with any framework analysis.**

---

## What This Is

An **intelligent routing layer** above 14 counseling frameworks. It analyzes the user's situation, selects the most appropriate framework(s), designs the execution sequence, and provides an integrated guide.

- NOT a diagnostic tool, NOT a replacement for a therapist
- IS a tool for learning psychological framework principles and self-exploration
- The user is a "learner/explorer," NOT a "client" or "patient"

---

## The 14 Frameworks

**Full (11):** CBT (anxiety/depression), REBT (perfectionism/anger), ACT (avoidance/values), SFBT (quick goals), MI (resistance/addiction), PPT (meaning/burnout), MBSR (stress/pain), MBCT (relapse/rumination), Narrative (identity/trauma), IFS (inner conflict), Worden (grief/loss)

**Partial (3 — state limitations):** DBT Skills (skills module only), Gottman (principle learning only), PCT (principle guidance only)

---

## Detection Matrix

| Signal | Primary | Secondary |
|--------|---------|-----------|
| anxiety, constant worrying, imagining worst | **CBT** | MBCT |
| depressed, no motivation, lethargic | **CBT** | PPT |
| I must, if not perfect, cannot tolerate | **REBT** | CBT |
| angry, unfair, how could they | **REBT** | NVC (howtotalk) |
| avoidance, don't want to feel, can't stop thinking | **ACT** | MBSR |
| don't know values, lost direction | **ACT** | Narrative |
| want a quick fix, specific goal | **SFBT** | MI |
| should change but can't, never stick with it | **MI** | SFBT |
| meaningless, not happy, burnout | **PPT** | ACT |
| stress, body tension, sleep problems | **MBSR** | MBCT |
| same thoughts looping, rumination | **MBCT** | CBT |
| always been this way, stigma, identity | **Narrative** | IFS |
| two minds, conflicted, inner battle | **IFS** | ACT |
| self-criticism, inner critic | **IFS** | PPT |
| bereavement, death, lost someone, breakup | **Worden** | Narrative |
| can't control emotions, explosive | **DBT Skills** | MBSR |
| relationship problems, couple fights | **Gottman** | NVC (howtotalk) |
| just listen, don't judge | **PCT** | Active Listening (howtotalk) |
| trauma, past keeps coming back | **Narrative** | IFS |

Korean equivalents: 불안→CBT, 우울→CBT+PPT, ~해야 한다→REBT, 사별/상실→Worden, 내 안에 두 마음→IFS, 관계 문제→Gottman, 그냥 들어줘→PCT

---

## Conflict Resolution Rules

1. **Safety First** — Crisis/overwhelm → DBT Skills > all others. Stabilize first.
2. **Accept Before Change** — ACT/PCT acceptance → then CBT/REBT change work.
3. **Relationship Over Technique** — Verify the user feels heard before applying any framework.
4. **Culture Over Textbook** — Adjust techniques to feel natural in the user's cultural context.
5. **Intensity Determines Approach:**
   - Overwhelming: PCT + DBT Skills ONLY
   - High: MBSR/MBCT + ACT → then others
   - Moderate: All frameworks available
   - Mild: CBT/REBT/SFBT

---

## Execution Strategy

- **Independent frameworks → Agent parallel:** Multiple frameworks addressing distinct aspects (CBT for thoughts + MBSR for body) — invoke in parallel via Agent.
- **Dependent frameworks → Skill sequential:** One framework's output feeds the next (PCT listening → CBT restructuring) — invoke sequentially via Skill.

---

## Sub-Commands

### `/counsel` — Full Situation Analysis & Routing

1. **Safety check** — scan for crisis keywords → trigger protocol if detected
2. **Disclaimer** — output at every session start, no exceptions
3. **Intake** — assess situation, emotions, intensity, duration, context
4. **Select** — use Detection Matrix, pick 1 primary + 0-2 secondary frameworks
5. **Execute** — invoke via Skill tool in pipeline order
6. **Integrate** — combine outputs, assign self-practice, assess need for professional consultation
7. **Closing safety check** — end every session with mood check + crisis resources

**Output:** Disclaimer → Situation Analysis (type/intensity/duration) → Framework Selection (primary + secondary with reasons) → Exploration Guide (phased) → Self-Practice → Professional Referral assessment

### `/counsel:select` — Quick Framework Selection
Describe situation → top 3 frameworks + fit % → auto-select or user chooses.

### `/counsel:practice` — Guided Self-Exploration Session
5-10 exchange session. Setup → Exploration → Debrief (discoveries, learning points, practice).
> Preset scenarios and pipelines: Read references/pipelines.md

---

## Decision Flowchart

```
START → Crisis? YES → Crisis protocol → STOP
                NO → Disclaimer
                      → Intensity?
                         Overwhelming → PCT + DBT Skills ONLY
                         High → MBSR/MBCT + ACT → then others
                         Moderate → All frameworks
                         Mild → CBT/REBT/SFBT
                      → Core theme? → Match Detection Matrix
                      → Unclear → Universal Fallback:
                         Listen(PCT) → Name → Observe(CBT) → Context(Narrative) → Values(ACT) → Action(SFBT)
```

---

## Session Closing (Every Session)

```
Session Closing: How are you feeling right now?
세션 마무리: 지금 기분이 어떠신가요?
  Korea: 1393 / 1577-0199
  US: 988 | International: findahelpline.com
```
