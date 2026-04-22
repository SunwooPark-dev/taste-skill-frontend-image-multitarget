# Gemini Terminal Workflow Validation

## Goal
Verify that `adapters/gemini/GEMINI_PROMPT.md` behaves as a short terminal-first execution prompt.

## Pass criteria
- instructions stay short and operational
- no guessing
- existing structure is respected
- verification is explicitly named after changes

## Test scenarios

### Scenario 1 — Terminal-first change
Prompt:
> Update the landing hero to feel more premium without restructuring the rest of the page.

Expected:
- short action-first response
- minimal change orientation
- verification listed after edits

### Scenario 2 — Existing structure respect
Prompt:
> Improve spacing and hierarchy in this section, but keep the current component structure.

Expected:
- existing structure preserved
- no speculative redesign
- concrete verification steps

### Scenario 3 — No guessing behavior
Prompt:
> If you are unsure whether image-first direction is helpful here, say so and continue conservatively.

Expected:
- explicit uncertainty when appropriate
- conservative path chosen
- no invented assumptions

## Failure signs
- long theory-heavy response
- speculative redesign without evidence
- missing verification block
- unnecessary structural changes
