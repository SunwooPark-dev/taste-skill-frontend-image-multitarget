# Validation Plan

## Order
1. Codex App validation
2. Antigravity App validation
3. Gemini terminal workflow validation

## Why this order
- Codex is the most implementation-sensitive target and sets the baseline.
- Antigravity is next because it is prompt-first and assumption-sensitive.
- Gemini terminal is last because it benefits from the shortest, most operational final wording.

## Completion rule
Each target should pass at least one real usage test before broader expansion of this import.

## Next refinement trigger
If any target fails its validation scenarios:
- update only that adapter first
- re-test before changing the others
