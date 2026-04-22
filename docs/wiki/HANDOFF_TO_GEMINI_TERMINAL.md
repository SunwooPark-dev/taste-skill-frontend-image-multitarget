# Handoff to Gemini Terminal

이 문서는 **Gemini terminal workflow가 이 저장소를 바로 사용하도록 넘길 때** 쓰는 handoff 문서입니다.

---

## 저장소 접근 위치

### 로컬 경로
`C:\Users\sunwo\taste-skill-frontend-image-multitarget`

### GitHub
`https://github.com/SunwooPark-dev/taste-skill-frontend-image-multitarget`

### 기본 브랜치
`main`

---

## 이 저장소가 하는 일

이 저장소는 standalone app이 아니라, 아래 목적을 가진 **재사용 자산 저장소**입니다.

- 원본 import 보관
- Codex / Antigravity / Gemini용 adapter 보관
- validation 기준 문서 보관
- validation 결과 문서 보관
- usage / scenarios / final prompts 보관
- wiki 기반 운영 문서 보관

즉, Gemini terminal workflow는 이 저장소를 **짧고 실행 중심적인 프롬프트 + 검증 자산 저장소**로 사용해야 합니다.

---

## Gemini terminal이 먼저 읽어야 할 파일

우선순위 순서:

1. `docs/wiki/Home.md`
2. `docs/wiki/Quick-Start.md`
3. `adapters/gemini/GEMINI_PROMPT.md`
4. `docs/migration/FINAL_PROMPTS.md`
5. `docs/migration/SCENARIOS.md`
6. `docs/wiki/Validation-System.md`

핵심만 빠르게 보려면:
- 시작 프롬프트 → `adapters/gemini/GEMINI_PROMPT.md`
- 바로 쓸 문장 → `docs/migration/FINAL_PROMPTS.md`
- 테스트 예시 → `docs/migration/SCENARIOS.md`

---

## Gemini terminal workflow가 이 저장소를 사용할 때 해야 할 일

### 허용되는 사용 방식
- Gemini용 adapter를 세션 시작 프롬프트로 사용하기
- final prompt block을 그대로 사용하거나 가볍게 수정해서 쓰기
- scenario를 실행해보고 결과를 validation 문서에 반영하기
- prompt / wiki / validation 문서를 개선하기

### 피해야 할 것
- `source/original/` 내용을 함부로 덮어쓰기
- 긴 이론 설명으로 흐르기
- 추측으로 구조를 바꾸기
- validation/result 문서 업데이트 없이 완료 선언하기

---

## 권장 작업 흐름

1. `main`에서 새 브랜치를 만든다
   - 예: `validate/gemini-pass-02`
   - 예: `docs/gemini-handoff-update`
2. `adapters/gemini/GEMINI_PROMPT.md`를 기준으로 시작한다
3. `FINAL_PROMPTS.md` 또는 `SCENARIOS.md`에서 프롬프트를 고른다
4. 실제 세션 결과를 만든다
5. `GEMINI_RESULTS.md` 또는 새 `GEMINI_LIVE_VALIDATION_0X.md`에 기록한다
6. wiki/usage 문서가 바뀌었으면 같이 업데이트한다

---

## Gemini terminal에게 바로 전달할 수 있는 지시문

```text
다음 저장소를 작업 기준으로 사용해:
https://github.com/SunwooPark-dev/taste-skill-frontend-image-multitarget

목적:
- 이 저장소를 standalone app으로 보지 말고
- frontend 감각 / adapter / validation 자산 저장소로 사용해

우선 읽을 파일:
1. docs/wiki/Home.md
2. docs/wiki/Quick-Start.md
3. adapters/gemini/GEMINI_PROMPT.md
4. docs/migration/FINAL_PROMPTS.md
5. docs/migration/SCENARIOS.md
6. docs/wiki/Validation-System.md
7. docs/wiki/HANDOFF_TO_GEMINI_TERMINAL.md

작업 규칙:
- adapters/gemini/GEMINI_PROMPT.md를 우선 기준으로 사용
- 짧고 실행 중심적으로
- 추측 금지
- 기존 구조 존중
- 결과가 생기면 docs/migration/GEMINI_RESULTS.md 또는 새 live validation 문서에 남겨

금지:
- source/original/ 무단 재작성
- 근거 없는 구조 변경
- validation 기록 없이 완료 선언

권장 브랜치 전략:
- main에서 새 브랜치 생성 후 작업
- 예: validate/gemini-pass-02
```

---

## 가장 쉬운 시작 시나리오

```text
adapters/gemini/GEMINI_PROMPT.md 기준으로 작업해.
hero만 개선해.
기존 구조는 유지하고, 변경 후 검증 방식까지 적어.
```

---

## 업데이트 규칙

Gemini terminal이 이 저장소에 의미 있는 작업을 했으면 최소한 아래 중 하나는 업데이트해야 합니다.

- `docs/migration/GEMINI_RESULTS.md`
- `docs/migration/GEMINI_LIVE_VALIDATION_0X.md`
- `docs/wiki/Prompt-Library.md`
- `docs/wiki/Validation-System.md`
- `docs/wiki/Quick-Start.md`

즉, **사용만 하고 기록을 안 남기는 방식은 금지**입니다.
