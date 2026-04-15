# Changelog

All notable changes to the Counsel Frameworks project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

---

## [2.0.0] - 2026-04-15

### Added
- **Meta-router architecture**: `/counsel` now acts as an intelligent routing layer that automatically selects the optimal framework(s) based on situation analysis
- **Multi-framework pipelines**: 8 predefined pipeline sequences for complex situations (anxiety, depression, inner conflict, grief, low motivation, relationship conflict, rumination, emotional dysregulation)
- **Detection Matrix**: Keyword and pattern-based framework matching for both English and Korean input
- **Framework Compatibility Matrix**: Synergy ratings and tension pair resolution rules for all 14 frameworks
- **Korean Cultural Adaptation Layer**: Collectivism, chemyeon (face), han, nunchi, filial piety, and shame culture adaptations
- **3 partial-implementation frameworks**: DBT Skills (skills module only), Gottman Method (pattern learning only), PCT (principle guidance only) with explicit scope disclaimers
- **Cross-router integration**: Links to `howtotalk` (NVC, Active Listening) and `think` (Systems Thinking) routers
- **Conflict resolution rules**: 5 priority rules for when frameworks have conflicting approaches
- **Decision flowchart**: Intensity-based gating that restricts available frameworks based on severity
- **`/counsel:select`**: Quick framework recommendation with fit percentages
- **`/counsel:practice`**: Structured self-exploration session with 10 preset scenarios
- **Professional referral guidelines**: 8 specific criteria with framework-specific referral notes
- **Comprehensive documentation**: README.md, README.ko.md, docs/FRAMEWORKS.md, docs/SAFETY.md, CHANGELOG.md

### Changed
- Router upgraded from simple selection to multi-framework pipeline design
- Crisis protocol expanded with more detection keywords (Korean and English)
- Safety disclaimer now bilingual (English + Korean) at every session start

## [1.0.0] - 2026-04-01

### Added
- **11 fully implemented frameworks**: CBT, REBT, ACT, SFBT, MI, PPT, MBSR, MBCT, Narrative Therapy, IFS, Worden's Grief Counseling
- **Crisis detection**: Suicide and self-harm keyword scanning with immediate safety protocol
- **Crisis hotlines**: Korea (1393, 1577-0199, 1588-9191), US (988), Japan, International (befrienders.org)
- **Session disclaimer**: "This tool does not replace professional psychotherapy" at every session
- **Bilingual support**: All frameworks support English and Korean input/output
- **Sub-commands**: Each framework has 2-4 specialized sub-commands (e.g., `/cbt:thought-record`, `/act:defusion`, `/ifs:parts`)
- **Structured output formats**: Consistent analysis format for each framework
- **Anti-patterns**: Each framework documents common misapplications to avoid
- **Academic references**: All frameworks cite primary sources

### Framework Details (v1.0.0)

| Framework | Key Features |
|-----------|-------------|
| CBT | 7-column thought record, 15 cognitive distortions, Socratic questioning, behavioral experiments |
| REBT | A-B-C-D-E model, irrational belief disputation, unconditional self-acceptance |
| ACT | Hexaflex model, 6 core processes, values clarification (10 domains), choice point, passengers on the bus |
| SFBT | Miracle question, scaling questions, exception finding, coping questions |
| MI | OARS, change talk, sustain talk, readiness ruler, decisional balance |
| PPT | PERMA model, VIA character strengths, three good things, gratitude letter |
| MBSR | Body scan, sitting meditation, walking meditation, mindful yoga |
| MBCT | 3-minute breathing space, decentering, pleasant/unpleasant events calendar |
| Narrative Therapy | Externalization, unique outcomes, re-authoring, outsider witness, tree of life |
| IFS | Parts model (exiles/managers/firefighters), Self (8 C's), 6 F's process, unburdening |
| Worden's Grief | Four tasks of mourning, continuing bonds, meaning reconstruction |
