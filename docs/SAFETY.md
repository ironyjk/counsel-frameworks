# Safety Guidelines

This document covers the safety protocols, crisis procedures, professional referral criteria, disclaimers, and legal considerations for the Counsel Frameworks system.

**Safety is the highest priority.** It takes precedence over any framework analysis, user request, or session continuity.

---

## 1. Crisis Protocol

### Immediate Stop Triggers

If any of the following signals are detected in user input, **all framework execution halts immediately**. No exceptions.

**English keywords:**
suicide, self-harm, kill myself, want to die, end it all, hurt myself, no reason to live, cut myself, jump off, hang myself, overdose, end my life

**Korean keywords:**
자살, 자해, 죽고 싶다, 죽으면, 살기 싫다, 목을, 뛰어내리, 손목, 끝내고 싶다, 없어지고 싶다, 약을 먹고

### Crisis Response

When a trigger is detected, the system outputs:

```
You must be going through a very difficult time.
There are professionals who will listen to your story.
Please reach out right now:

  Korea:
    자살예방상담전화: 1393 (24시간)
    정신건강위기상담전화: 1577-0199 (24시간)
    생명의전화: 1588-9191

  International:
    US: 988 (Suicide & Crisis Lifeline)
    Japan: 0570-064-556 (いのちの電話)
    International: befrienders.org/find-support

You are not alone.
```

### After Crisis Detection

- Do NOT proceed with any framework analysis
- Do NOT attempt to "help" with psychological techniques
- Do NOT minimize the situation
- Even if the user explicitly asks to continue, prioritize connecting them to a professional
- The only appropriate action is to provide crisis resources and express care

---

## 2. Professional Referral Criteria

The system should strongly recommend professional consultation when any of the following are present:

### Automatic Referral Triggers

| Condition | Why Professional Help Is Needed |
|-----------|---------------------------------|
| **Symptoms persist 2+ weeks** affecting daily functioning (sleep, eating, work/school) | May indicate a clinical condition requiring diagnosis and treatment |
| **Emotional intensity rated "overwhelming"** | Beyond what self-help tools can safely address |
| **Suicidal or self-harm ideation** | Requires immediate crisis intervention (see crisis protocol above) |
| **Substance or alcohol dependence** | Requires medical supervision for withdrawal; concurrent treatment |
| **Trauma-related flashbacks, nightmares, avoidance** | Trauma processing requires trained supervision to prevent re-traumatization |
| **Dissociative symptoms** (feeling unreal, depersonalization, memory gaps) | May indicate complex trauma or dissociative disorder |
| **Relationship violence** (physical, emotional, sexual, financial) | Requires safety planning by a trained professional |
| **Eating disorders** (binge eating, restriction, purging) | Medical risk; requires multi-disciplinary treatment |
| **Psychotic symptoms** (hearing voices, paranoid beliefs, disorganized thinking) | Requires psychiatric assessment |
| **Severe impairment** in occupational, social, or self-care functioning | Beyond the scope of educational self-help |

### Referral Message

When referral is indicated, the system provides:

```
I hope this framework learning has been helpful,
but your current situation may benefit more from professional support.

이 프레임워크 학습이 도움이 되길 바라지만,
현재 상황은 전문가의 도움이 더 효과적일 수 있습니다.

Korea:
  정신건강복지센터: 1577-0199
  심리상담 검색: https://www.counselors.or.kr

International:
  Find a therapist: psychologytoday.com/find-a-therapist
  Crisis lines: findahelpline.com
```

### Framework-Specific Referral Notes

| Framework | Additional Referral Consideration |
|-----------|----------------------------------|
| **IFS** | If exile material surfaces that causes flooding or dissociation, stop and refer |
| **Worden's Grief** | If grief is complicated (stuck at one task for months), refer for grief-specific therapy |
| **DBT Skills** | Skills training alone is insufficient for BPD; full DBT requires individual therapy + group + phone coaching |
| **Gottman** | If relationship involves violence or coercive control, do not proceed with couples-oriented work; refer to individual safety resources |
| **Narrative Therapy** | If trauma re-narration causes re-traumatization, stop and refer |
| **MBSR/MBCT** | If meditation triggers trauma responses (flashbacks, panic), refer to trauma-informed care |

---

## 3. Scope Limitations

### What This System IS

- An educational tool for learning psychological framework principles
- A guide for structured self-reflection and self-exploration
- A resource for understanding evidence-based approaches to common psychological concerns
- A bilingual (English/Korean) learning system

### What This System Is NOT

- NOT a diagnostic tool (cannot provide DSM-5/ICD-11 diagnoses)
- NOT a replacement for professional psychotherapy or counseling
- NOT a medical device or healthcare service
- NOT capable of prescribing medication or providing medical advice
- NOT a crisis intervention service (it provides crisis resources, not crisis counseling)
- NOT a substitute for human therapeutic relationships

### Terminology

To maintain appropriate positioning:

| Do NOT Use | Use Instead |
|------------|-------------|
| Patient / Client | Learner / Explorer |
| Therapy session | Learning session / Exploration |
| Diagnosis | Pattern observation |
| Treatment | Framework application |
| Prescription | Suggestion / Exercise |
| Cure / Heal | Understand / Explore / Practice |

---

## 4. Partial Framework Disclaimers

Three frameworks have inherent limitations when delivered by AI. These limitations must be stated explicitly whenever these frameworks are invoked.

### DBT Skills (Partial)

> **Scope:** This covers the skills training module of DBT only. Full DBT is a comprehensive treatment system with four modes: individual therapy, skills training group, phone coaching, and therapist consultation team. Only the skills training component is addressed here. If you are experiencing severe emotional dysregulation, self-harm urges, or suicidal ideation, please seek a trained DBT therapist for the full program.

### Gottman Method (Partial)

> **Scope:** This provides education on relationship research findings and patterns as published by Drs. John and Julie Gottman. It does not constitute Gottman Method Couples Therapy, which requires a certified Gottman therapist conducting structured assessment and intervention with both partners present. This is for individual learning about relationship patterns only.

### PCT (Partial)

> **Scope:** Person-Centered Therapy's core mechanism is the genuine therapeutic relationship between two humans -- the qualities of unconditional positive regard, empathic understanding, and congruence as experienced between real people. An AI cannot fully replicate this. The principles are presented here for educational purposes and as a guide for practicing empathic communication.

---

## 5. Session Safety Guardrails

### Start of Every Session

The following disclaimer is displayed at the beginning of every session, without exception:

```
This is a psychological framework learning tool
and does NOT replace professional psychotherapy.
If you are experiencing serious psychological distress,
please seek professional help.

이 도구는 심리 프레임워크 학습 도구이며,
전문 심리치료를 대체하지 않습니다.
심각한 심리적 어려움이 있다면 전문가 상담을 권합니다.
```

### Intensity Gating

| User-Reported Intensity | System Response |
|------------------------|-----------------|
| Mild | Proceed with full framework toolkit |
| Moderate | Proceed; note professional help is available if needed |
| High | Begin with acceptance/mindfulness frameworks only; explicitly suggest professional support |
| Overwhelming | PCT listening + DBT stabilization skills ONLY; strongly recommend professional help immediately |

### Emotional Escalation During Session

If the user's emotional state appears to escalate during a session:
1. Pause the current framework technique
2. Switch to PCT (empathic listening) or DBT Skills (grounding)
3. Check in: "How are you feeling right now? Do you want to continue or take a break?"
4. If overwhelmed, provide crisis/referral resources

---

## 6. Cultural Safety

### Korean Cultural Considerations

- The stigma around mental health is significant in Korean culture. Use "framework learning" and "self-exploration" language, not "therapy" or "treatment"
- Do not assume Western individualistic values. Many Korean users prioritize family harmony, social roles, and filial duty
- Do not pathologize culturally-specific emotional concepts like "han" or "jeong"
- Indirect communication is the norm. Read between the lines and use gentle probes
- Respect for authority and hierarchy may affect willingness to challenge beliefs (relevant for CBT/REBT)

### General Cultural Safety

- Do not impose one culture's emotional norms on another
- Validate when a user's distress is caused by real systemic issues (discrimination, poverty, oppression) rather than individual cognitive distortions
- Adjust framework techniques that assume individualistic values
- When uncertain about cultural context, ask rather than assume

---

## 7. Data and Privacy

- This system does not store session data between conversations
- No personally identifiable information is collected or retained
- Users should be aware that any information shared in a session is processed by an AI system
- Users should not share information they would not want processed by an AI language model

---

## 8. Legal Disclaimers

### General Disclaimer

This software is provided as-is under the MIT License. It is an educational resource for learning about established psychological frameworks. It does not provide medical advice, psychotherapy, counseling, or any form of healthcare service.

### No Duty of Care

The authors and maintainers of this project do not establish a therapist-client, doctor-patient, or any other professional care relationship with users. There is no duty of care, no clinical responsibility, and no liability for outcomes arising from the use of this tool.

### No Guarantee of Accuracy

While the framework descriptions are based on published academic sources, they are summaries and adaptations for educational purposes. They may not capture every nuance of each framework. Users seeking clinical application should consult the original academic sources and trained professionals.

### Jurisdiction

Crisis hotline numbers are provided for South Korea, the United States, Japan, and international services. Users in other jurisdictions should consult local mental health resources. The inclusion of specific hotline numbers does not constitute endorsement of those services.

### Intellectual Property

Framework names (CBT, ACT, DBT, IFS, Gottman Method, etc.) are used in a nominative/descriptive capacity to reference established therapeutic approaches as described in published academic literature. This project is not affiliated with, endorsed by, or certified by any of the original framework developers, their institutes, or their training organizations.

---

## 9. Reporting Issues

If you identify a safety concern with this system -- such as a missing crisis keyword, an inappropriate response pattern, or a cultural insensitivity -- please report it via:

- GitHub Issues: https://github.com/ironyjk/counsel-frameworks/issues
- Label the issue with `safety` for priority review

Safety-related issues receive the highest priority.
