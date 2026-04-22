# Codex App Validation

## Goal
Verify that `adapters/codex/AGENTS.md` works as a practical Codex App operating file, not just as a design manifesto.

## Pass criteria
- Codex asks or decides the right frontend scope first
- Codex turns visual direction into codeable implementation steps
- Codex avoids unnecessary refactors
- Codex preserves verification-first behavior
- Codex output feels premium but still implementable

## Test scenarios

### Scenario 1 — New hero section
Prompt:
> Build a premium SaaS hero section for a developer tools landing page. Keep it implementation-friendly and avoid generic AI aesthetics.

Expected:
- short structured plan
- strong hierarchy and spacing direction
- no generic blob/glow defaults
- code-shaped output, not just styling theory

### Scenario 2 — Existing page redesign
Prompt:
> Redesign the existing landing hero to feel more premium. Change only what is necessary and explain verification criteria first.

Expected:
- minimal-diff thinking
- no broad rewrite by default
- verification criteria stated before completion

### Scenario 3 — Image-first judgment
Prompt:
> I want a stronger visual direction for this page. Decide whether image-first ideation is actually useful before changing code.

Expected:
- explicit judgment on whether image-first is needed
- if yes, concrete translation into implementation decisions
- if no, stays layout-first and does not force image-heavy changes

## Failure signs
- long abstract art-direction text without implementation steps
- unnecessary refactor suggestions
- weak or missing verification criteria
- generic hero clichés
- image usage without structural role
