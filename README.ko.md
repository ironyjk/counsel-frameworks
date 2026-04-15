# Counsel Frameworks

**14개 근거 기반 심리 프레임워크 + 자동 라우팅 시스템**

고민을 말하면 `/counsel`이 최적의 프레임워크를 자동 선택하고, 다중 프레임워크 파이프라인을 설계하여, 구조화된 자기 탐색을 안내합니다.

> **이것은 치료가 아닙니다.** 심리 프레임워크를 배우고 자기 탐색에 활용하는 학습 도구입니다. 전문 심리치료를 대체하지 않습니다.

---

## 빠른 시작

```
/counsel 자꾸 같은 생각이 맴돌고 미래가 불안해서 잠을 못 자겠어
```

AI가 자동으로:
1. 위기 신호 스크리닝 (감지 시 즉시 안전 프로토콜)
2. 상황 분석 (감정 유형, 강도, 기간, 맥락)
3. 14개 프레임워크 중 최적 1~3개 선택
4. 복합 상황을 위한 다중 프레임워크 파이프라인 설계
5. 구체적 기법을 활용한 구조화된 자기 탐색 가이드
6. 자기 연습 과제 배정 + 전문가 상담 필요성 판단

---

## 설치

### Claude Code (권장)

```bash
# 저장소 클론
git clone https://github.com/ironyjk/counsel-frameworks.git /tmp/counsel-frameworks

# 모든 스킬을 프로젝트에 복사
for dir in counsel cbt rebt act sfbt mi ppt mbsr mbct narrative-therapy ifs worden-grief dbt-skills gottman pct; do
  cp -r /tmp/counsel-frameworks/$dir .claude/skills/
done
```

### Claude Projects (claude.ai)

1. 저장소를 ZIP으로 다운로드
2. 각 `SKILL.md` 파일을 열어서
3. Claude 프로젝트의 **프로젝트 지식(Project Knowledge)** 섹션에 붙여넣기

### 기타 AI 플랫폼

각 프레임워크는 독립적인 마크다운 파일(`SKILL.md`)입니다. 사용하는 플랫폼의 시스템 프롬프트, 지식 베이스, 또는 지시사항 필드에 내용을 복사하세요. 라우터(`counsel/SKILL.md`)는 `Skill` 도구를 통해 하위 스킬을 호출합니다 -- 플랫폼에 맞게 호출 방식을 조정하세요.

---

## 명령어

| 명령어 | 설명 |
|--------|------|
| `/counsel` | 전체 상황 분석, 프레임워크 선택, 다중 프레임워크 가이드 탐색 |
| `/counsel:select` | 빠른 프레임워크 추천 (적합도 퍼센트 포함) |
| `/counsel:practice` | 구조화된 자기 탐색 세션 (5~10회 대화형 교환) |

각 하위 프레임워크도 자체 명령어를 가지고 있습니다 (라우터가 자동 호출, 직접 사용 불가):

| 프레임워크 | 하위 명령어 |
|-----------|------------|
| CBT | `/cbt`, `/cbt:thought-record`, `/cbt:distortions`, `/cbt:experiment` |
| ACT | `/act`, `/act:defusion`, `/act:values`, `/act:plan` |
| IFS | `/ifs`, `/ifs:parts`, `/ifs:self`, `/ifs:dialogue` |
| SFBT | `/sfbt`, `/sfbt:miracle`, `/sfbt:scaling`, `/sfbt:exceptions` |
| REBT | `/rebt`, `/rebt:abc`, `/rebt:dispute`, `/rebt:beliefs` |
| PCT | `/pct`, `/pct:reflect`, `/pct:conditions` |
| ... | (각 프레임워크마다 2~4개의 하위 명령어) |

---

## 14개 프레임워크

### 완전 구현 (11개)

AI 에이전트가 구조화된 기법, 연습, 가이드 세션을 완전히 제공할 수 있는 프레임워크입니다.

| # | 프레임워크 | 창시자 | 핵심 아이디어 | 적합한 상황 |
|---|-----------|--------|-------------|------------|
| 1 | **CBT** 인지행동치료 | Aaron Beck | 사고-감정-행동 삼각형; 인지 왜곡 교정 | 불안, 우울, 걱정, 자동적 사고 |
| 2 | **REBT** 합리적 정서행동치료 | Albert Ellis | 비합리적 신념 논박 (A-B-C-D-E 모델) | 완벽주의, "해야 한다" 사고, 분노 |
| 3 | **ACT** 수용전념치료 | Steven Hayes | 심리적 유연성; 수용 + 가치 기반 행동 | 회피, 반추, 가치 혼란, 만성 통증 |
| 4 | **SFBT** 해결중심 단기치료 | de Shazer & Berg | 문제가 아닌 해결에 집중; 기적 질문 | 빠른 변화, 구체적 목표, 동기 부족 |
| 5 | **MI** 동기강화상담 | Miller & Rollnick | 내적 동기 유발; 양가감정 탐색 | 변화 저항, 중독, 건강 행동 |
| 6 | **PPT** 긍정심리치료 | Martin Seligman | PERMA를 통한 웰빙: 강점, 의미, 성취 | 번아웃, 의미 상실, 무기력 |
| 7 | **MBSR** 마음챙김 스트레스 감소 | Jon Kabat-Zinn | 마음챙김 명상; 몸-마음 연결 | 스트레스, 만성 통증, 수면, 신체 긴장 |
| 8 | **MBCT** 마음챙김 인지치료 | Segal, Williams, Teasdale | 마음챙김 + 인지치료; 탈중심화 | 우울 재발 방지, 반추 고리 |
| 9 | **내러티브 치료** | White & Epston | 문제 외재화; 삶의 이야기 재구성 | 정체성, 낙인, 트라우마 재프레이밍 |
| 10 | **IFS** 내면가족체계 | Richard Schwartz | 내면 파트 대화; Self 리더십 (8C) | 내적 갈등, 자기비판, 복합 감정 |
| 11 | **Worden 애도 상담** | J. William Worden | 능동적 애도의 4가지 과업 | 사별, 상실, 이별, 죽음 |

### 부분 구현 (3개)

AI로 전달할 때 본질적 한계가 있는 프레임워크입니다. 사용 시 제한 사항이 명시됩니다.

| # | 프레임워크 | 창시자 | 범위 | 제한 사항 |
|---|-----------|--------|------|----------|
| 12 | **DBT 스킬** | Marsha Linehan | 4개 스킬 모듈: 마음챙김, 고통감내, 감정조절, 대인관계 효과성 | 스킬 교육만 가능. 개인치료, 전화 코칭, 치료자 자문 불가. |
| 13 | **가트만 방식** | John & Julie Gottman | 건강한 관계의 집, 네 기수, 사랑의 지도, 회복 | 관계 패턴 학습만. 실제 커플치료 불가. |
| 14 | **PCT** 인간중심치료 | Carl Rogers | 무조건적 긍정적 존중, 공감적 이해, 진실성 | 치료적 관계 자체가 핵심 메커니즘. AI로 완전 구현 불가. |

---

## 아키텍처

```
사용자가 상황을 설명
         |
         v
  /counsel (메타 라우터)
    |
    +-- 위기 감지 ----------> 안전 프로토콜 (위기상담전화, 중단)
    |
    +-- 상황 분석 ----------> 감지 매트릭스 (키워드 + 패턴)
    |
    +-- 프레임워크 선택 -----> 1~3개 프레임워크 + 적합도 점수
    |
    +-- 파이프라인 설계 -----> 다중 프레임워크 실행 순서
    |
    v
  하위 스킬 (자동 호출, 사용자 직접 접근 불가)
    |
    +-- 완전 구현: CBT, REBT, ACT, SFBT, MI, PPT, MBSR, MBCT,
    |              내러티브 치료, IFS, Worden 애도
    |
    +-- 부분 구현: DBT 스킬, 가트만, PCT
    |
    v
  통합 가이드
    +-- 각 프레임워크의 기법 & 연습
    +-- 자기 연습 과제
    +-- 전문가 연계 필요성 판단
```

### 다중 프레임워크 파이프라인

복합 상황에서는 프레임워크를 순차적으로 연결합니다:

| 파이프라인 | 상황 | 순서 |
|-----------|------|------|
| 불안 & 걱정 | 지속적인 불안한 생각 | CBT (인지 분석) -> MBCT (탈중심화) -> ACT (가치 기반 행동) |
| 우울 & 무기력 | 동기 저하, 무기력 | CBT (재구성) -> PPT (강점) -> SFBT (작은 변화) |
| 내적 갈등 | 자기비판, 두 마음 | IFS (파트 탐색) -> ACT (수용) -> PPT (자기자비) |
| 애도 & 상실 | 사별, 죽음, 이별 | PCT (공감적 경청) -> Worden (애도 과업) -> 내러티브 (의미 재구성) |
| 동기 부족 | 변화 저항 | MI (양가감정) -> SFBT (예외 찾기) -> ACT (가치) |
| 관계 갈등 | 부부/커플 문제 | 가트만 (진단) -> NVC (표현) -> MI (상대 관점) |
| 반추 고리 | 같은 생각 반복 | MBCT (마음챙김) -> CBT (사고 기록) -> MBSR (바디 스캔) |
| 감정 조절 어려움 | 폭발적, 충동적 | DBT 스킬 (TIPP/STOP) -> MBSR (안정화) -> IFS (이해) |

---

## 사용 예시

### 예시 1: 업무 불안

```
/counsel 내일 프레젠테이션인데 머리가 하얘질 것 같고 다들 나를 무능하다고 생각할 것 같아
```

**라우터 선택:** CBT (주 -- 점쟁이 오류, 독심술 왜곡) + MBCT (보조 -- 파국적 사고 탈중심화)

사고 기록지를 작성하고, 인지 왜곡을 식별하며, 소크라테스식 질문을 적용하고, 발표 당일 아침 그라운딩 연습을 제공합니다.

### 예시 2: 상실 후 애도

```
/counsel 아버지가 돌아가신 지 3개월인데 가끔 아버지 생각을 안 하는 날이 있으면 죄책감이 들어요
```

**라우터 선택:** Worden 애도 (주 -- 과업 II: 고통 처리) + PCT (지지 -- 공감적 경청) + 내러티브 (보조 -- 의미 재구성)

죄책감을 정상화하고, 애도 과업을 탐색하며, 상실한 대상과의 지속적 유대를 재구성하도록 돕습니다.

### 예시 3: 미루기와 자기비판

```
/counsel 사이드 프로젝트를 계속 미루다가 시간 낭비한 자신이 한심해
```

**라우터 선택:** IFS (주 -- 내적 비평가 vs. 미루기 파트) + ACT (보조 -- "게으르다" 이야기에서 탈융합, 가치 명확화)

내면의 파트를 매핑하고, 비평가와 보호자 사이의 대화를 촉진하며, 핵심 가치와 연결된 가장 작은 한 걸음 행동 계획을 세웁니다.

### 예시 4: 관계 갈등

```
/counsel 남편이랑 매일 싸우는데 이혼하고 싶다가도 아이들 생각에 참게 돼요
```

**라우터 선택:** 가트만 (주 -- 네 기수 패턴) + IFS (보조 -- 갈등하는 내면 파트: 의무 vs. 자기 돌봄), 한국 문화 적응 적용

파괴적 의사소통 패턴을 식별하고, 이분법적 프레이밍 없이 내적 갈등을 탐색하며, 문화적으로 적합한 의사소통 기법을 제공합니다.

---

## 안전

이 시스템에서 안전이 최우선입니다.

### 위기 감지

모든 사용자 입력에서 자살 및 자해 신호를 스캔합니다. 감지 시 즉시 위기 상담 전화번호와 함께 안전 프로토콜이 작동합니다. **위기 감지 후에는 어떤 프레임워크 분석도 진행하지 않습니다.**

### 위기 상담 전화

| 지역 | 서비스 | 번호 |
|------|--------|------|
| 한국 | 자살예방상담전화 | 1393 (24시간) |
| 한국 | 정신건강위기상담전화 | 1577-0199 (24시간) |
| 한국 | 생명의전화 | 1588-9191 |
| 미국 | Suicide & Crisis Lifeline | 988 |
| 일본 | いのちの電話 | 0570-064-556 |
| 국제 | Befrienders | befrienders.org/find-support |

### 전문가 상담 권장 기준

다음 상황에서 전문 상담을 권장합니다:
- 증상이 2주 이상 지속되며 일상 기능(수면, 식사, 업무)에 영향
- 감정 강도가 "압도적"
- 물질/알코올 의존 패턴
- 트라우마 관련 플래시백 또는 해리 증상
- 관계 내 폭력
- 섭식 장애 패턴

### 세션 면책 조항

모든 세션은 다음 면책 조항으로 시작합니다:

> 이 도구는 심리 프레임워크 학습 도구이며, 전문 심리치료를 대체하지 않습니다. 심각한 심리적 어려움이 있다면 전문가 상담을 권합니다.

전체 안전 가이드라인은 [docs/SAFETY.md](docs/SAFETY.md)를 참조하세요.

---

## 한국 문화 적응

라우터에는 한국 사용자를 위한 문화 적응 레이어가 포함되어 있습니다:

| 개념 | 적응 방식 |
|------|----------|
| **집단주의** | 개인 욕구 탐색 시 죄책감 정상화; 가치 작업에서 "관계 속의 나" 포함 |
| **체면** | 감정을 "약함"이 아닌 "정보"로 재프레이밍; 상황 중심 질문으로 시작 |
| **한** | 병리화하지 않음; 문화적 맥락에서 이해; 내러티브 치료에서 외재화 |
| **눈치** | 직접 말하지 않는 부분을 맥락에서 추론; 부드러운 탐색 질문 사용 |
| **효도** | "부모 vs. 나"가 아닌 통합적 해결책 추구 |
| **수치심 문화** | "프레임워크 학습" 포지셔닝 유지; 치료 관련 용어 지양 |

---

## 프레임워크 호환성

### 높은 시너지 조합
- CBT + MBCT -- 인지 재구성 + 마음챙김 (우울/불안의 골드 스탠다드)
- ACT + MI -- 수용 + 동기 (변화 저항에 최강 조합)
- IFS + 내러티브 치료 -- 파트 + 이야기 (정체성 작업의 핵심)
- SFBT + PPT -- 해결 + 강점 (긍정적 변화 가속기)
- Worden 애도 + PCT -- 애도 과업 + 수용 (상실 작업의 기초)
- DBT 스킬 + MBSR -- 감정 조절 + 마음챙김 (감정 폭풍의 닻)

### 긴장 조합 (해결 규칙과 함께 신중하게 사용)
- CBT + PCT -- 변화 vs. 수용 (해결: PCT로 먼저 수용, 그 다음 CBT로 재구성)
- REBT + ACT -- 신념 논박 vs. 신념과의 관계 변화 (해결: ACT 탈융합으로 REBT의 "해야 한다" 처리)
- SFBT + 내러티브 -- 빠른 해결 vs. 깊은 이야기 (해결: SFBT로 시작, 내러티브로 심화)
- MI + REBT -- 비지시적 vs. 적극적 논박 (해결: MI로 준비도 확인 후 REBT)

전체 비교표 및 호환성 매트릭스는 [docs/FRAMEWORKS.md](docs/FRAMEWORKS.md)를 참조하세요.

---

## 갈등 해결 규칙

프레임워크 간 접근 방식이 충돌할 때:

1. **안전 우선** -- 위기/압도 -> DBT 스킬 > 다른 모든 프레임워크
2. **변화 전에 수용** -- ACT/PCT 수용 -> 그 다음 CBT/REBT 재구성
3. **기법보다 관계** -- 기법 적용 전에 상대가 충분히 들렸다고 느끼는지 확인
4. **교과서보다 문화** -- 사용자의 문화적 맥락에서 부자연스러운 기법은 조정
5. **강도에 따른 접근** -- 압도적: PCT + DBT만; 높음: MBSR/ACT 우선; 보통: 모두 가능; 가벼움: CBT/REBT/SFBT

---

## 관련 프로젝트

| 프로젝트 | 프레임워크 | 라우터 |
|---------|-----------|--------|
| **[counsel-frameworks](https://github.com/ironyjk/counsel-frameworks)** | 심리 14개 | `/counsel` |
| **[strategy-frameworks](https://github.com/ironyjk/strategy-frameworks)** | 전략 29개 | `/think` |
| **[howtotalk](https://github.com/ironyjk/howtotalk)** | 커뮤니케이션 13개 | `/howtotalk` |
| **[parenting-frameworks](https://github.com/ironyjk/parenting-frameworks)** | 교육/육아 16개 | `/parenting` |
| **[toc-agents](https://github.com/ironyjk/toc-agents)** | TOC 10개 | `/toc` |
| **[triz-agents](https://github.com/ironyjk/triz-agents)** | TRIZ 9개 | `/triz` |

---

## 교차 라우터 통합

Counsel은 적절한 경우 형제 라우터와 통합됩니다:

- **howtotalk** -- 관계 갈등 시 가트만이 NVC 또는 적극적 경청으로 라우팅
- **think** -- 직장 스트레스가 구조적/조직적 문제일 때 시스템 사고로 라우팅

---

## 참고 문헌

### 핵심 텍스트

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

### 한국 문화 맥락

- 최상진 (2011). *한국인의 심리학*. 학지사.
- 이동귀 외 (2018). *한국 상담 모형 연구*. 한국상담심리학회지.
- Kim, U. & Park, Y.S. (2006). *Indigenous and Cultural Psychology*. Springer.

### 메타/통합

- Norcross, J.C. & Goldfried, M.R. (2019). *Handbook of Psychotherapy Integration* (3rd ed.). Oxford.
- Wampold, B.E. (2015). *The Great Psychotherapy Debate* (2nd ed.). Routledge.

---

## 면책 조항

이 파일들은 교육적/자기계발 목적의 프레임워크 학습 가이드입니다. 전문적인 심리치료, 상담, 또는 의료 서비스를 구성하거나 대체하지 않습니다. 정신건강 위기 시 즉시 면허를 가진 전문가에게 연락하거나 지역 위기상담전화에 전화하십시오.

## 라이선스

MIT

## 만든 사람

@ironyjk x Claude Code
