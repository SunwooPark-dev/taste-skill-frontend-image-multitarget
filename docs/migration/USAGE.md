# USAGE

이 저장소는 **실행 앱**이 아니라, 아래 3개 환경에서 바로 재사용할 수 있는 **운영 자산 저장소**입니다.

- Codex App
- Antigravity App
- Gemini terminal workflow

핵심 아이디어는 간단합니다.

1. 이 저장소에서 **환경별 adapter 파일**을 꺼낸다
2. 대상 도구에 맞게 **붙여넣거나 참조**한다
3. `docs/migration/*_VALIDATION.md`의 시나리오로 검증한다
4. 실제 사용 결과를 `*_RESULTS.md`에 기록한다

---

## 빠른 시작

### 어떤 파일을 쓰면 되나

| 대상 도구 | 바로 쓸 파일 | 용도 |
|---|---|---|
| Codex App | `adapters/codex/AGENTS.md` | Codex 작업 규칙/운영 기준 |
| Antigravity App | `adapters/antigravity/ANTIGRAVITY_PROMPT.md` | 새 대화창 시작 프롬프트 |
| Gemini terminal workflow | `adapters/gemini/GEMINI_PROMPT.md` | 터미널 세션 시작 프롬프트 |

---

## 1. Codex App에서 사용하는 방법

### 언제 쓰나
- landing page 개선
- hero section 개선
- 프리미엄 느낌의 UI 정리
- image-led 방향을 코드 가능한 구조로 바꾸고 싶을 때

### 어떻게 쓰나
가장 쉬운 방법은 `adapters/codex/AGENTS.md` 내용을 **작업 기준**으로 삼는 것입니다.

예시:

```text
이 저장소의 adapters/codex/AGENTS.md 기준으로 작업해.
기존 landing hero를 더 프리미엄하게 바꿔줘.
나머지는 크게 건드리지 말고, 검증 기준부터 먼저 제시해.
```

또는:

```text
adapters/codex/AGENTS.md 기준으로 판단해.
이 페이지가 image-first 접근이 필요한지 먼저 결정하고,
필요할 때만 구조적으로 반영해줘.
```

### Codex에서 기대하는 동작
- 생각 먼저 하기
- 최소 구현 우선
- 필요한 부분만 수정
- verification 먼저 정의
- generic AI 레이아웃 회피
- 코드 가능한 결과로 번역

### Codex 검증 문서
- 기준: `docs/migration/CODEX_VALIDATION.md`
- 현재 결과: `docs/migration/CODEX_RESULTS.md`
- 실제 fixture 검증: `docs/migration/CODEX_LIVE_VALIDATION_01.md`

---

## 2. Antigravity App에서 사용하는 방법

### 언제 쓰나
- 작업 전에 방향부터 정리하고 싶을 때
- 디자인 해석 옵션을 먼저 보고 싶을 때
- 과잉 리디자인 없이 범위를 통제하고 싶을 때

### 어떻게 쓰나
1. 새 Antigravity 대화창을 연다
2. `adapters/antigravity/ANTIGRAVITY_PROMPT.md` 전체를 붙여넣는다
3. 이어서 실제 작업을 입력한다

예시:

```text
기존 hero를 더 프리미엄하게 만들고 싶어.
다른 섹션은 크게 바꾸지 말아줘.
```

또는:

```text
이 사이트를 더 premium하게 만들고 싶은데,
먼저 어떤 해석이 가능한지 2~3개 옵션부터 제시해줘.
```

### Antigravity에서 기대하는 동작
- 작업 전 판단
- 가정 명시
- 최소 변경
- 검증 가능한 목표 정의
- 모호하면 해석 옵션 제시

### Antigravity 검증 문서
- 기준: `docs/migration/ANTIGRAVITY_VALIDATION.md`
- 현재 결과: `docs/migration/ANTIGRAVITY_RESULTS.md`
- 1차 검증 메모: `docs/migration/ANTIGRAVITY_LIVE_VALIDATION_01.md`

---

## 3. Gemini terminal workflow에서 사용하는 방법

### 언제 쓰나
- 짧고 실행 중심적인 지시가 필요할 때
- 터미널 기반 작업 흐름에 맞춘 프롬프트가 필요할 때
- “추측 금지 / 구조 존중 / 검증 명시”가 중요할 때

### 어떻게 쓰나
1. Gemini terminal 세션 시작 시
2. `adapters/gemini/GEMINI_PROMPT.md`를 먼저 넣는다
3. 그 다음 실제 작업을 짧게 입력한다

예시:

```text
adapters/gemini/GEMINI_PROMPT.md 기준으로 작업해.
landing hero spacing과 hierarchy만 개선해.
구조는 유지하고, 변경 후 검증 방식도 같이 적어.
```

또는:

```text
기존 구조를 유지한 채 hero를 더 premium하게 만들어.
추측하지 말고, 불확실하면 먼저 가정을 적어.
```

### Gemini에서 기대하는 동작
- 짧고 실행 중심적
- terminal-first
- 추측 금지
- 기존 구조 존중
- 변경 후 검증 형식 명시

### Gemini 검증 문서
- 기준: `docs/migration/GEMINI_VALIDATION.md`
- 현재 결과: `docs/migration/GEMINI_RESULTS.md`
- 환각 체크 포함 1차 검증: `docs/migration/GEMINI_LIVE_VALIDATION_01.md`

---

## 추천 사용 순서

이 저장소를 실제로 활용할 때는 아래 순서가 제일 좋습니다.

1. **Codex App에서 먼저 사용**
   - 가장 직접적으로 구현 작업과 연결됨
2. **Antigravity에서 방향/해석 검증**
   - 모호한 디자인 요청 정리에 좋음
3. **Gemini terminal에서 짧은 실행 워크플로우 검증**
   - 실제 터미널 작업 스타일 검증에 적합

---

## 아직 남아 있는 한계

현재 이 저장소는 아래 수준까지 완료되었습니다.

- adapter 파일 생성 완료
- validation 기준 문서 완료
- 1차 결과 문서 완료
- Gemini 쪽은 텍스트 기반 hallucination audit 완료

하지만 아직 아래는 남아 있습니다.

- Antigravity 실제 앱 런타임 검증
- Gemini 실제 터미널 세션 검증
- Codex 실제 제품 코드베이스 live pass 추가

즉, **지금은 “바로 써볼 수 있는 상태”는 맞지만, 각 환경 100% 최종 확정 상태는 아닙니다.**

---

## 가장 쉬운 시작 시나리오

### Codex App
```text
이 저장소의 adapters/codex/AGENTS.md 기준으로 작업해.
기존 landing hero를 더 프리미엄하게 바꿔줘.
나머지는 크게 건드리지 말고, 검증 기준부터 먼저 제시해.
```

### Antigravity App
```text
기존 hero를 더 premium하게 만들고 싶어.
다른 섹션은 크게 바꾸지 말아줘.
```

### Gemini terminal workflow
```text
adapters/gemini/GEMINI_PROMPT.md 기준으로 작업해.
landing hero spacing과 hierarchy만 개선해.
구조는 유지하고, 변경 후 검증 방식도 같이 적어.
```

---

## 운영 원칙

이 저장소는 앞으로도 아래 방식으로 확장하면 됩니다.

1. 원본 자산 import
2. 환경별 adapter 작성
3. validation 기준 작성
4. results 기록
5. 필요 시 adapter 수정

즉, 이 repo는 단순 문서 모음이 아니라:

> **멀티-타겟 재사용 자산 + 검증 ledger 저장소**

로 운영하면 됩니다.
