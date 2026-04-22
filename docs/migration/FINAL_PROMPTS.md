# FINAL PROMPTS

아래 프롬프트들은 바로 복붙해서 쓸 수 있는 최종 프롬프트 블록입니다.

---

## 1. Codex App용 최종 프롬프트

```text
이 작업은 taste-skill frontend image adapter 기준으로 진행해.

운영 기준:
- think before acting
- minimum viable implementation first
- only modify what is necessary
- verification before completion
- ask when uncertainty materially affects correctness
- no unnecessary refactors

디자인 기준:
- premium, image-led when appropriate
- anti-slop layout discipline
- implementation-friendly structure
- strong spacing, hierarchy, rhythm, and composition
- avoid generic AI aesthetics
- avoid cloned section patterns
- avoid decorative image spam
- avoid dense, overfilled layouts

작업 방식:
1. 먼저 이 작업이 image-first가 필요한지 판단해.
2. 필요한 경우에만 이미지 방향을 구조적으로 반영해.
3. visual direction을 반드시 codeable decisions로 번역해.
   - section ordering
   - text hierarchy
   - spacing rhythm
   - component grouping
   - image placement
   - CTA priority
4. 최소 변경 원칙을 지켜.
5. 검증 기준을 먼저 제시한 뒤 작업해.

응답 형식:
- 판단
- 최소 변경 계획
- 구현 포인트
- 검증 기준
- 실제 변경안

작업:
기존 landing hero를 더 프리미엄하게 바꿔줘.
다른 섹션은 건드리지 말고, 과한 리팩터링 없이 진행해.
```

### Codex App 짧은 버전

```text
taste-skill codex adapter 기준으로 작업해.
기존 hero만 premium하게 개선해.
최소 변경 원칙, verification-first, no unnecessary refactor.
```

---

## 2. Antigravity App용 최종 프롬프트

```text
너는 taste-skill frontend image adapter를 적용한 상태로 작업한다.

필수 규칙:
- evaluate before acting
- state assumptions explicitly
- minimize changes
- define verifiable goals
- if ambiguous, stop and present interpretation options

디자인 목표:
- premium
- art-directed
- readable
- structured
- implementation-friendly
- image-led only when it truly helps

작업 규칙:
- strong composition over generic SaaS patterns
- images are structural design material, not filler
- keep spacing and section rhythm deliberate
- avoid repetitive AI aesthetics
- avoid over-designed noise
- do not force extra style if the current structure is already strong

시작 전 반드시 적을 것:
1. 어떤 종류의 페이지/섹션인지
2. 어떤 가정을 두고 있는지
3. 가장 작은 유효 변경이 무엇인지
4. 무엇으로 성공을 검증할지

모호하면:
- 바로 진행하지 말고
- 가능한 해석 옵션 2~3개를 먼저 제시해

작업:
기존 hero를 더 premium하게 만들고 싶어.
다른 섹션은 크게 바꾸지 말아줘.
먼저 가정과 최소 변경 방향부터 제시해줘.
```

### Antigravity App 짧은 버전

```text
taste-skill antigravity adapter 기준으로 진행해.
가정 명시, 최소 변경, 검증 목표 우선.
모호하면 해석 옵션부터 제시해.
```

---

## 3. Gemini terminal workflow용 최종 프롬프트

```text
Use the taste-skill frontend image adapter for this task.

Rules:
- be short and execution-oriented
- work terminal-first
- do not guess
- respect the existing structure
- state how you will verify changes after editing

Core objective:
- preserve premium frontend taste
- use image-first direction only when useful
- keep anti-slop layout discipline
- keep output implementation-friendly

Working pattern:
1. state the exact frontend target
2. state assumptions
3. decide whether image-first ideation is necessary
4. make only the minimal structural/design change needed
5. verify with concrete checks

Optimize for:
- codeable layout decisions
- strong hierarchy
- controlled spacing
- structural image use
- clean hero composition

Avoid:
- generic AI-looking heroes
- cloned section blocks
- decorative image spam
- dense overfilled composition
- long abstract explanations

After changes, report:
- what changed
- what files changed
- what verification was run
- remaining uncertainty

Task:
Improve the landing hero only.
Keep the current structure.
Reduce generic AI 느낌 and make it feel more premium.
Do not guess.
```

### Gemini terminal workflow 짧은 버전

```text
taste-skill gemini adapter 기준으로 작업해.
짧고 실행 중심적으로.
추측 금지, 구조 유지, 변경 후 검증 명시.
```

---

## 추천 사용 순서

1. Codex App에서 먼저 테스트
2. Antigravity App에서 방향성 검증
3. Gemini terminal workflow에서 짧은 실행 흐름 검증
