# Counsel — Psychology Frameworks for AI Agents

14 evidence-based counseling frameworks, one auto-routing entry point.
Describe your situation — `/counsel` picks the best approach.

> **This is NOT therapy.** This is a framework learning tool for self-exploration and psychological education.

## `/counsel` — One Command, 14 Frameworks

```
/counsel I keep having the same anxious thoughts and can't stop worrying about the future
```

The AI automatically:
1. Screens for crisis signals (immediate safety protocol if detected)
2. Analyzes the situation (emotion type, intensity, duration, context)
3. Selects the best 1-3 frameworks
4. Guides you through structured self-exploration
5. Suggests self-practice exercises

## Commands

| Command | What It Does |
|---------|-------------|
| `/counsel` | Full analysis → framework selection → guided exploration |
| `/counsel:select` | Quick framework recommendation only |
| `/counsel:practice` | Structured self-exploration session (5-10 exchanges) |

## The 14 Frameworks

### Fully Implementable (11)

| # | Framework | Best For |
|---|-----------|----------|
| 1 | **CBT** (Beck) | Anxiety, depression, automatic thoughts, cognitive distortions |
| 2 | **REBT** (Ellis) | Perfectionism, "must" thinking, anger, self-criticism |
| 3 | **ACT** (Hayes) | Avoidance, values confusion, acceptance, chronic pain |
| 4 | **SFBT** (de Shazer) | Quick change, concrete goals, finding exceptions |
| 5 | **MI** (Miller & Rollnick) | Resistance to change, addiction, ambivalence |
| 6 | **PPT** (Seligman) | Burnout, meaning loss, strength-building, wellbeing |
| 7 | **MBSR** (Kabat-Zinn) | Stress, chronic pain, sleep, body-mind connection |
| 8 | **MBCT** (Segal et al.) | Depression relapse prevention, rumination |
| 9 | **Narrative Therapy** (White & Epston) | Identity, stigma, re-authoring life stories |
| 10 | **IFS** (Schwartz) | Inner conflict, self-criticism, complex emotions |
| 11 | **Worden's Grief** | Bereavement, loss, separation |

### Partial Implementation (3)

| # | Framework | Scope | Limitation |
|---|-----------|-------|------------|
| 12 | **DBT Skills** (Linehan) | Emotion regulation, distress tolerance skills only | No individual therapy/phone coaching |
| 13 | **Gottman Method** | Couple relationship patterns, Four Horsemen | Principle learning only, not couples therapy |
| 14 | **PCT** (Rogers) | Unconditional positive regard, empathic understanding | AI cannot fully replicate therapeutic relationship |

## Safety Features

- **Crisis detection**: Suicide/self-harm keywords trigger immediate crisis protocol
- **Korean crisis lines**: 1393 (24h), 1577-0199 (24h), 1588-9191
- **International**: 988 (US), befrienders.org
- **Disclaimer**: Every session starts with "This is not therapy"
- **Professional referral**: Clear guidelines for when to recommend a professional

## Architecture

```
/counsel (meta-router — user-invocable)
└── 14 frameworks (internal, auto-selected by /counsel)
    ├── CBT, REBT, ACT, SFBT, MI
    ├── PPT, MBSR, MBCT
    ├── Narrative Therapy, IFS, Worden's Grief
    └── DBT (skills), Gottman (partial), PCT (partial)
```

## Installation

```bash
cd /path/to/your/project
git clone https://github.com/ironyjk/counsel-frameworks.git /tmp/cf
cp -r /tmp/cf/counsel .claude/skills/
```

## Cultural Adaptation

Includes Korean cultural adaptation layer:
- Collectivism (집단주의) — navigating individual needs vs. group harmony
- Chemyeon (체면) — face and emotional expression barriers
- Han (한) — culturally-specific emotional complex
- Nunchi (눈치) — indirect communication patterns
- Shame culture — "framework learning" positioning to reduce stigma

## Related Projects

- **[strategy-frameworks](https://github.com/ironyjk/strategy-frameworks)** — 29 strategy frameworks + `/think`
- **[howtotalk](https://github.com/ironyjk/howtotalk)** — 13 communication frameworks + `/howtotalk`
- **[parenting-frameworks](https://github.com/ironyjk/parenting-frameworks)** — 16 education/parenting frameworks + `/parenting`
- **[toc-agents](https://github.com/ironyjk/toc-agents)** — Theory of Constraints, 10 tools
- **[triz-agents](https://github.com/ironyjk/triz-agents)** — TRIZ, 9 tools

## Disclaimer

These files are educational framework guides for learning and self-reflection purposes only. They do not constitute, and are not a substitute for, professional psychotherapy, counseling, or medical treatment. If you are in a mental health crisis, contact a licensed professional immediately.

## License

MIT

## Author

@ironyjk × Claude Code
