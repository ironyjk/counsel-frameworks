---
name: counsel-router-prompt
version: "1.0.0"
description: "LLM-as-Router prompt template for selecting the optimal evidence-based counseling framework given a situation. Replaces keyword-matching DETECTION_MATRIX."
type: router_prompt
target_repo: counsel-frameworks
---

# Counsel Router — LLM Selection Prompt

This file is consumed by `pag_pipeline.py::route(repo="counsel", question, router_llm)`.
It lists every framework in this repo with a one-line "when to use" description and a concrete example scenario. The router LLM is asked to return **exactly one framework name**.

---

## System Prompt

```
You are a psychological counseling expert acting as a framework selector.
Given a situation, pick the SINGLE framework that best fits.

Output ONLY the framework name (lowercase, exactly as listed below). No explanation, no punctuation, no quotes.

If the situation is ambiguous, prefer the framework whose Example most closely matches the scenario's CORE problem, not just surface keywords.
```

---

## Framework Catalog

Each entry: `name` — **when to use** (one line) / **example** (one concrete scenario).

### Cognitive & Behavioral (thoughts, beliefs, action)

**cbt** — Automatic negative thoughts or cognitive distortions are driving depression/anxiety; need structured thought-record work.
Example: "Every time my boss emails me, I assume I'm about to be fired and spiral into panic. How do I challenge this?"

**rebt** — A rigid irrational belief ("must/should/can't stand it") is generating disturbance; need A-B-C-D-E dispute.
Example: "I absolutely must be perfect at my job or I'm worthless. This belief is crushing me."

**act** — Client is over-fighting unwanted thoughts/feelings; needs acceptance, defusion, and values-based committed action rather than symptom removal.
Example: "I've tried to get rid of my anxiety for 10 years and it's only gotten worse. I want to live meaningfully anyway."

### Solution, Motivation & Strengths (forward-looking)

**sfbt** — Client is stuck ruminating on problems; shift to exceptions, miracle question, small next-step solutions.
Example: "I just want to stop dwelling on what's broken and figure out one small thing I can do differently this week."

**mi** — Client is ambivalent about a behavior change (substance, exercise, medication, leaving a job); need to elicit change talk without pushing.
Example: "Part of me knows I should quit drinking, but part of me doesn't want to. I keep going back and forth."

**ppt** — Client is functional but flat/languishing; build well-being through strengths, gratitude, engagement, meaning (PERMA).
Example: "I'm not depressed, but life feels grey and purposeless. How do I build something that actually feels good?"

### Mindfulness & Present-Moment (awareness-based)

**mbsr** — Chronic stress, pain, or reactivity; general mindfulness training to change the relationship to experience.
Example: "My chronic back pain and work stress are consuming me. I want to learn meditation-based stress reduction."

**mbct** — Client has recovered from depression but keeps relapsing when negative mood returns; relapse-prevention focus.
Example: "I've had three depressive episodes. When sadness creeps back I get pulled under again. How do I break the cycle?"

### Parts, Narrative & Self (inner systems, meaning-making)

**ifs** — Client describes inner conflict as "a part of me wants X, another part wants Y"; need parts dialogue and Self-leadership.
Example: "There's a critical voice inside that attacks me whenever I rest, and a child-like part that just wants to hide."

**narrative-therapy** — Problem has become the client's identity ("I AM depressed/anxious/a failure"); need externalization and re-authoring.
Example: "I've always been 'the anxious one' in my family. It feels like who I am. Can I separate myself from this story?"

**pct** — Client primarily needs to feel deeply heard and accepted; non-directive empathic presence is the intervention itself.
Example: "I just need someone to truly listen without fixing or advising me. I'm not sure what I need yet — I need space to find it."

### Relationships, Skills & Loss (specific life domains)

**gottman** — Couple in recurring conflict, criticism, contempt, stonewalling; need research-based relationship repair.
Example: "My partner and I keep having the same fight for 5 years. We criticize and shut down. Is this fixable?"

**dbt-skills** — Emotional dysregulation, impulsivity, or interpersonal chaos; need concrete skills (distress tolerance, emotion regulation, interpersonal effectiveness).
Example: "My emotions swing wildly and I lash out, then feel ashamed. I need practical skills to get through crisis moments."

**worden-grief** — Client is grieving a death or major loss; need task-based mourning framework (accept reality, process pain, adjust, find ongoing connection).
Example: "My mother died 8 months ago and I still can't function. I don't know how to move through this grief."

---

## User Prompt Template

```
## Situation
{scenario}

## Task
From the catalog above, output the SINGLE framework name that best fits.

Answer (one word, lowercase):
```

---

## Routing Notes (for maintainers, not shown to LLM)

- **SAFETY-CRITICAL — Crisis routing**: Any scenario involving suicidal ideation, self-harm intent, homicidal thoughts, active psychosis, or child abuse MUST NOT be handled by this router alone. The caller pipeline is responsible for crisis detection BEFORE routing. Regardless of which framework the router returns, the caller must prepend crisis-resource guidance (e.g., Korea: 자살예방상담전화 1393 / 정신건강상담 1577-0199; US: 988 Suicide & Crisis Lifeline). This was a regression point in a previous experiment — do not remove this safeguard.
- **Ambiguous cases deliberately kept**: e.g., "I feel empty and stuck" could be `sfbt` (stuckness) or `ppt` (languishing). Prefer `ppt` when the scenario emphasizes meaning/flatness without a clear problem focus; prefer `sfbt` when the client wants actionable next steps.
- **`mi` vs `cbt`**: If the client is *ambivalent* about changing, route to `mi`. If they have *already decided* to change and want to fight negative thinking, route to `cbt`.
- **`ifs` vs `pct`**: `ifs` when client spontaneously uses parts language. `pct` when client needs unconditional listening without technique.
- **`mbsr` vs `mbct`**: `mbct` only for depressive relapse prevention. All other mindfulness use cases → `mbsr`.
- **`gottman` is couples-only** — individual relationship distress without a participating partner leans to `cbt`, `ifs`, or `pct`.
- **Exclusive routing**: Router picks ONE. Pipeline combination (e.g., `mi` → `cbt`) is handled in Layer 3.
- **Not included here**: `counsel` itself (this IS counsel).

---

## Maintenance Protocol

Adding a new framework requires:
1. Add an entry to Framework Catalog above (name + when + example).
2. Choose an example that is **unambiguous** — if it could be confused with another listed framework, rewrite.
3. Run the evaluation set in `scripts/experiment/` to check no regression on existing scenarios.
4. Re-verify the crisis-routing safeguard in Routing Notes still applies.
