# Counsel Frameworks

**14 evidence-based psychological frameworks with intelligent auto-routing for AI agents.**

Describe your situation. `/counsel` selects the best framework(s), designs a multi-framework pipeline, and guides you through structured self-exploration.

> **This is NOT therapy.** This is a framework learning tool for self-exploration and psychological education. It does not replace professional psychotherapy.

---

## Quick Start

```
/counsel I keep having the same anxious thoughts and can't stop worrying about the future
```

The router automatically:
1. Screens for crisis signals (immediate safety protocol if detected)
2. Analyzes the situation (emotion type, intensity, duration, context)
3. Selects the best 1-3 frameworks from the 14 available
4. Designs a multi-framework pipeline for complex situations
5. Guides structured self-exploration with specific techniques
6. Assigns self-practice exercises and assesses need for professional referral

---

## Installation

> 💡 **짧은 이름**: [래퍼 설정](https://github.com/ironyjk/claude-frameworks-marketplace#짧은-이름으로-쓰기-optional) 후 `/counsel`로 호출 가능

### Claude Code (recommended)

```bash
# Clone the repository
git clone https://github.com/ironyjk/counsel-frameworks.git /tmp/counsel-frameworks

# Copy all skills into your project
for dir in counsel cbt rebt act sfbt mi ppt mbsr mbct narrative-therapy ifs worden-grief dbt-skills gottman pct; do
  cp -r /tmp/counsel-frameworks/$dir .claude/skills/
done
```

### Claude Projects (claude.ai)

1. Download the repository as a ZIP
2. Open each `SKILL.md` file
3. Paste into your Claude Project's **Project Knowledge** section

### Other AI Platforms

Each framework is a self-contained Markdown file (`SKILL.md`). Copy the contents into your platform's system prompt, knowledge base, or instruction field. The router (`counsel/SKILL.md`) references sub-skills by name via the `Skill` tool -- adapt the invocation mechanism to your platform.

---

## Commands

| Command | What It Does |
|---------|-------------|
| `/counsel` | Full situation analysis, framework selection, multi-framework guided exploration |
| `/counsel:select` | Quick framework recommendation with fit percentages |
| `/counsel:practice` | Structured self-exploration session (5-10 interactive exchanges) |

Each sub-framework also has its own commands (not user-invocable directly -- the router calls them):

| Framework | Sub-commands |
|-----------|-------------|
| CBT | `/cbt`, `/cbt:thought-record`, `/cbt:distortions`, `/cbt:experiment` |
| ACT | `/act`, `/act:defusion`, `/act:values`, `/act:plan` |
| IFS | `/ifs`, `/ifs:parts`, `/ifs:self`, `/ifs:dialogue` |
| SFBT | `/sfbt`, `/sfbt:miracle`, `/sfbt:scaling`, `/sfbt:exceptions` |
| REBT | `/rebt`, `/rebt:abc`, `/rebt:dispute`, `/rebt:beliefs` |
| PCT | `/pct`, `/pct:reflect`, `/pct:conditions` |
| ... | (each framework has 2-4 sub-commands) |

---

## The 14 Frameworks

### Full Implementation (11 frameworks)

These are fully implementable by an AI agent with structured techniques, exercises, and guided sessions.

| # | Framework | Founder | Core Idea | Best For |
|---|-----------|---------|-----------|----------|
| 1 | **CBT** | Aaron Beck | Thoughts-feelings-behaviors triangle; correct cognitive distortions | Anxiety, depression, worry, automatic thoughts |
| 2 | **REBT** | Albert Ellis | Dispute irrational beliefs (A-B-C-D-E model) | Perfectionism, "must" thinking, anger, self-demands |
| 3 | **ACT** | Steven Hayes | Psychological flexibility; acceptance + values-based action | Avoidance, rumination, values confusion, chronic pain |
| 4 | **SFBT** | de Shazer & Berg | Focus on solutions, not problems; miracle question | Quick change, specific goals, low motivation |
| 5 | **MI** | Miller & Rollnick | Elicit intrinsic motivation; explore ambivalence | Resistance to change, addiction, health behavior |
| 6 | **PPT** | Martin Seligman | Well-being via PERMA: strengths, meaning, accomplishment | Burnout, meaning loss, lethargy, strength-building |
| 7 | **MBSR** | Jon Kabat-Zinn | Mindfulness meditation; body-mind connection | Stress, chronic pain, sleep, physical tension |
| 8 | **MBCT** | Segal, Williams, Teasdale | Mindfulness + cognitive therapy; decentering | Depression relapse prevention, rumination loops |
| 9 | **Narrative Therapy** | White & Epston | Externalize problems; re-author life stories | Identity, stigma, trauma reframing |
| 10 | **IFS** | Richard Schwartz | Inner parts dialogue; Self leadership (8 C's) | Inner conflict, self-criticism, complex emotions |
| 11 | **Worden's Grief** | J. William Worden | Four active tasks of mourning | Bereavement, loss, separation, death |

### Partial Implementation (3 frameworks)

These have inherent limitations when delivered by AI. Limitations are explicitly stated during use.

| # | Framework | Founder | Scope | Limitation |
|---|-----------|---------|-------|------------|
| 12 | **DBT Skills** | Marsha Linehan | Four skills modules: mindfulness, distress tolerance, emotion regulation, interpersonal effectiveness | Skills training only. Cannot provide individual therapy, phone coaching, or therapist consultation. |
| 13 | **Gottman Method** | John & Julie Gottman | Sound Relationship House, Four Horsemen, Love Maps, repair | Relationship pattern learning only. Cannot conduct actual couples therapy. |
| 14 | **PCT** | Carl Rogers | Unconditional positive regard, empathic understanding, congruence | The therapeutic relationship itself is the mechanism. Full AI implementation is impossible. Principle guidance only. |

---

## Architecture

```
User describes situation
         |
         v
  /counsel (meta-router)
    |
    +-- Crisis Detection -----> Safety Protocol (hotlines, STOP)
    |
    +-- Situation Analysis ----> Detection Matrix (keywords + patterns)
    |
    +-- Framework Selection ---> 1-3 frameworks with fit scores
    |
    +-- Pipeline Design -------> Multi-framework execution sequence
    |
    v
  Sub-skills (auto-invoked, not user-facing)
    |
    +-- Full: CBT, REBT, ACT, SFBT, MI, PPT, MBSR, MBCT,
    |         Narrative Therapy, IFS, Worden's Grief
    |
    +-- Partial: DBT Skills, Gottman, PCT
    |
    v
  Integrated Guide
    +-- Techniques & exercises from each framework
    +-- Self-practice assignments
    +-- Professional referral assessment
```

### Multi-Framework Pipelines

For complex situations, the router chains frameworks in sequence:

| Pipeline | Situation | Sequence |
|----------|-----------|----------|
| Anxiety & Worry | Persistent anxious thoughts | CBT (cognitive analysis) -> MBCT (decentering) -> ACT (values-based action) |
| Depression & Apathy | Low motivation, lethargy | CBT (restructuring) -> PPT (strengths) -> SFBT (small changes) |
| Inner Conflict | Self-criticism, two minds | IFS (parts exploration) -> ACT (acceptance) -> PPT (self-compassion) |
| Grief & Loss | Bereavement, death, breakup | PCT (empathic listening) -> Worden (mourning tasks) -> Narrative (meaning) |
| Low Motivation | Resistance to change | MI (ambivalence) -> SFBT (exceptions) -> ACT (values) |
| Relationship Conflict | Couple fights, partner issues | Gottman (diagnosis) -> NVC (expression) -> MI (perspective) |
| Rumination Loop | Same thoughts circling | MBCT (mindfulness) -> CBT (thought record) -> MBSR (body scan) |
| Emotional Dysregulation | Explosive, impulsive | DBT Skills (TIPP/STOP) -> MBSR (stabilize) -> IFS (understand) |

---

## Usage Examples

### Example 1: Work Anxiety

```
/counsel I have a presentation tomorrow and I'm convinced I'll freeze up
and everyone will think I'm incompetent
```

**Router selects:** CBT (primary -- fortune telling, mind reading distortions) + MBCT (secondary -- decentering from catastrophic thoughts)

The session walks through a thought record, identifies cognitive distortions, applies Socratic questioning, and provides a grounding exercise for the morning of the presentation.

### Example 2: Grief After Loss

```
/counsel My father passed away three months ago and I feel guilty that
some days I don't think about him at all
```

**Router selects:** Worden's Grief (primary -- Task II: processing pain) + PCT (support -- empathic listening) + Narrative Therapy (secondary -- meaning reconstruction)

The session normalizes the guilt, explores the grief tasks, and helps reconstruct the continuing bond with the lost person.

### Example 3: Procrastination and Self-Criticism

```
/counsel I keep putting off starting my side project and then I hate myself
for wasting time
```

**Router selects:** IFS (primary -- inner critic part vs. procrastinator part) + ACT (secondary -- defusion from "lazy" story, values clarification)

The session maps the inner parts, facilitates dialogue between the critic and the protector, and connects the project to core values with a smallest-possible-step action plan.

### Example 4: Relationship Conflict (Korean context)

```
/counsel 남편이랑 매일 싸우는데 이혼하고 싶다가도 아이들 생각에 참게 돼요
```

**Router selects:** Gottman (primary -- Four Horsemen patterns) + IFS (secondary -- conflicting inner parts: duty vs. self-care) with Korean cultural adaptation (collectivism, filial duty, chemyeon)

The session identifies destructive communication patterns, explores the internal conflict without binary framing, and provides culturally-adapted communication techniques.

---

## Safety

Safety is the highest priority in this system.

### Crisis Detection

Every user input is scanned for suicide and self-harm signals. Detection triggers an immediate safety protocol with crisis hotline numbers. **No framework analysis proceeds after crisis detection.**

Keywords monitored include: suicide, self-harm, kill myself, want to die, end it all, and Korean equivalents.

### Crisis Hotlines

| Region | Service | Number |
|--------|---------|--------|
| Korea | Suicide Prevention | 1393 (24h) |
| Korea | Mental Health Crisis | 1577-0199 (24h) |
| Korea | Lifeline | 1588-9191 |
| US | Suicide & Crisis Lifeline | 988 |
| Japan | Inochi no Denwa | 0570-064-556 |
| International | Befrienders | befrienders.org/find-support |

### Professional Referral Triggers

The system recommends professional consultation when:
- Symptoms persist 2+ weeks affecting daily functioning
- Emotional intensity is "overwhelming"
- Substance/alcohol dependence patterns
- Trauma-related flashbacks or dissociation
- Relationship violence
- Eating disorder patterns

### Session Disclaimer

Every session begins with a bilingual disclaimer:

> This is a psychological framework learning tool and does NOT replace professional psychotherapy. If you are experiencing serious psychological distress, please seek professional help.

See [docs/SAFETY.md](docs/SAFETY.md) for full safety guidelines.

---

## Korean Cultural Adaptation

The router includes a cultural adaptation layer for Korean users:

| Concept | Adaptation |
|---------|-----------|
| **Collectivism** | Normalize guilt when exploring individual needs; include "myself within relationships" in values work |
| **Chemyeon** (face) | Reframe emotions as "information" not "weakness"; start with situation-focused questions |
| **Han** | Do not pathologize; understand within cultural context; externalize in Narrative Therapy |
| **Nunchi** (social awareness) | Infer unstated concerns from context; use gentle probes |
| **Filial Piety** | Seek integrative solutions rather than binary "parents vs. me" framing |
| **Shame Culture** | Maintain "framework learning" positioning; avoid therapy-associated terminology |

---

## Framework Compatibility

### High Synergy Pairs
- CBT + MBCT -- cognitive restructuring + mindfulness (gold standard for depression/anxiety)
- ACT + MI -- acceptance + motivation (strongest for resistance to change)
- IFS + Narrative Therapy -- parts + stories (core of identity work)
- SFBT + PPT -- solutions + strengths (positive change accelerator)
- Worden's Grief + PCT -- mourning tasks + acceptance (foundation of loss work)
- DBT Skills + MBSR -- emotion regulation + mindfulness (anchor in emotional storms)

### Tension Pairs (used carefully with resolution rules)
- CBT + PCT -- change vs. acceptance (resolve: accept first via PCT, then restructure via CBT)
- REBT + ACT -- dispute beliefs vs. change relationship to beliefs (resolve: use ACT defusion on REBT's "musts")
- SFBT + Narrative Therapy -- quick solutions vs. deep stories (resolve: start SFBT, deepen with Narrative)
- MI + REBT -- non-directive vs. active disputing (resolve: confirm readiness via MI before REBT)

See [docs/FRAMEWORKS.md](docs/FRAMEWORKS.md) for the full comparison and compatibility matrix.

---

## Conflict Resolution Rules

When frameworks have conflicting approaches:

1. **Safety First** -- Crisis/overwhelm -> DBT Skills > all other frameworks
2. **Accept Before Change** -- ACT/PCT acceptance -> then CBT/REBT restructuring
3. **Relationship Over Technique** -- Verify the person feels heard before applying any technique
4. **Culture Over Textbook** -- Adjust techniques that feel unnatural in the user's cultural context
5. **Intensity Determines Approach** -- Overwhelming: PCT + DBT only; High: MBSR/ACT first; Moderate: all available; Mild: CBT/REBT/SFBT

---

## Related Projects

| Project | Frameworks | Router |
|---------|-----------|--------|
| **[counsel-frameworks](https://github.com/ironyjk/counsel-frameworks)** | 14 psychological frameworks | `/counsel` |
| **[strategy-frameworks](https://github.com/ironyjk/strategy-frameworks)** | 29 strategy frameworks | `/think` |
| **[howtotalk](https://github.com/ironyjk/howtotalk)** | 13 communication frameworks | `/howtotalk` |
| **[parenting-frameworks](https://github.com/ironyjk/parenting-frameworks)** | 16 education/parenting frameworks | `/parenting` |
| **[toc-agents](https://github.com/ironyjk/toc-agents)** | 10 TOC tools | `/toc` |
| **[triz-agents](https://github.com/ironyjk/triz-agents)** | 9 TRIZ tools | `/triz` |

---

## Cross-Router Integration

Counsel integrates with sibling routers when appropriate:

- **howtotalk** -- For relationship conflicts, Gottman can route to NVC or Active Listening for communication techniques
- **think** -- When workplace stress is a structural/organizational issue, route to systems-thinking for systemic analysis

---

## References

### Core Texts

1. Beck, J.S. (2020). *Cognitive Behavior Therapy: Basics and Beyond* (3rd ed.). Guilford Press.
2. Ellis, A. & Harper, R.A. (1975). *A New Guide to Rational Living*. Wilshire.
3. Hayes, S.C. (2019). *A Liberated Mind*. Avery.
4. de Shazer, S. (1985). *Keys to Solution in Brief Therapy*. W.W. Norton.
5. Miller, W.R. & Rollnick, S. (2013). *Motivational Interviewing* (3rd ed.). Guilford Press.
6. Seligman, M.E.P. (2011). *Flourish*. Free Press.
7. Kabat-Zinn, J. (2013). *Full Catastrophe Living* (rev. ed.). Bantam.
8. Segal, Z.V. et al. (2013). *Mindfulness-Based Cognitive Therapy for Depression* (2nd ed.). Guilford Press.
9. White, M. & Epston, D. (1990). *Narrative Means to Therapeutic Ends*. W.W. Norton.
10. Schwartz, R.C. & Sweezy, M. (2020). *Internal Family Systems Therapy* (2nd ed.). Guilford Press.
11. Worden, J.W. (2018). *Grief Counseling and Grief Therapy* (5th ed.). Springer.
12. Linehan, M.M. (2015). *DBT Skills Training Manual* (2nd ed.). Guilford Press.
13. Gottman, J.M. & Silver, N. (2015). *The Seven Principles for Making Marriage Work* (rev. ed.). Harmony.
14. Rogers, C.R. (1961). *On Becoming a Person*. Houghton Mifflin.

### Meta/Integration

- Norcross, J.C. & Goldfried, M.R. (2019). *Handbook of Psychotherapy Integration* (3rd ed.). Oxford.
- Wampold, B.E. (2015). *The Great Psychotherapy Debate* (2nd ed.). Routledge.

---

## Disclaimer

These files are educational framework guides for learning and self-reflection purposes only. They do not constitute, and are not a substitute for, professional psychotherapy, counseling, or medical treatment. If you are in a mental health crisis, please contact a licensed professional or call your local crisis hotline immediately.

## License

MIT

## Author

@ironyjk x Claude Code
