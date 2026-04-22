# Gemini Live Validation 01

## Validation target
`adapters/gemini/GEMINI_PROMPT.md`

## Goal
Validate that the Gemini adapter behaves like a short, terminal-first operating prompt and check that the recorded claims stay grounded in the actual file.

## Validation method
Prompt-behavior simulation using the existing Gemini validation scenarios, plus a direct hallucination audit against the prompt text.

This is a **prompt-behavior validation pass**, not a live Gemini runtime execution.

## Scenario 1 — Terminal-first change
Prompt:
> Update the landing hero to feel more premium without restructuring the rest of the page.

Expected behavior:
- short action-first response
- minimal change orientation
- verification listed after edits

Observed fit:
- the adapter explicitly requires short, execution-oriented behavior
- it tells the system to make only the minimal structural/design change needed
- it requires reporting verification after changes

Verdict:
- PASS

## Scenario 2 — Existing structure respect
Prompt:
> Improve spacing and hierarchy in this section, but keep the current component structure.

Expected behavior:
- existing structure preserved
- no speculative redesign
- concrete verification steps

Observed fit:
- the adapter explicitly says to respect the existing structure
- it discourages unnecessary redesign by framing work as minimal change
- verification remains mandatory in the reporting block

Verdict:
- PASS

## Scenario 3 — No guessing behavior
Prompt:
> If you are unsure whether image-first direction is helpful here, say so and continue conservatively.

Expected behavior:
- explicit uncertainty when appropriate
- conservative path chosen
- no invented assumptions

Observed fit:
- the adapter explicitly says “Do not guess”
- it requires assumptions to be stated
- it keeps image-first direction conditional rather than mandatory

Verdict:
- PASS

## Hallucination audit
Claims checked against the actual prompt file:
- “short and execution-oriented” → present
- “do not guess” → present
- “respect the existing structure” → present
- “state assumptions” → present
- “minimal structural/design change” → present
- “report verification after changes” → present

Hallucination verdict:
- PASS
- No unsupported claim was recorded in this validation pass.

## What worked
- strong terminal-first tone
- concise verification/reporting format
- explicit anti-guessing constraint
- good preservation of existing structure

## Remaining limitation
This is not yet a live Gemini terminal workflow session. It is a grounded prompt-behavior validation pass with an explicit text-level hallucination check.

## Recommended next step
Use `adapters/gemini/GEMINI_PROMPT.md` in a real Gemini terminal session and compare the live output against the three scenario expectations plus the hallucination audit criteria.
