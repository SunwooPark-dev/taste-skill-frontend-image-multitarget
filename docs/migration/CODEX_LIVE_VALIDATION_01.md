# Codex Live Validation 01

## Validation target
`adapters/codex/AGENTS.md`

## Goal
Run one practical Codex-oriented validation pass instead of stopping at prompt-theory review.

## Scenario
Use the adapter principles to improve a bland hero section while:
- keeping scope minimal
- avoiding unnecessary refactors
- translating visual direction into codeable decisions
- preserving verification-first behavior

## Fixture
- Before: `validation-fixtures/codex-hero-01/before.html`
- After: `validation-fixtures/codex-hero-01/after.html`

## Validation prompt
> Redesign the existing landing hero to feel more premium. Change only what is necessary and explain verification criteria first.

## Observed implementation behavior
- The hero stayed as a single-section change instead of expanding into a full landing page rewrite.
- The update translated design direction into concrete frontend decisions:
  - stronger hierarchy
  - more controlled spacing
  - image with structural role
  - clearer CTA emphasis
  - cleaner visual rhythm
- The output avoided generic AI clichés such as blob-heavy gradients and meaningless decorative clutter.
- The resulting markup remains straightforward to implement and reason about.

## What changed
- moved from centered single-column hero to a more premium two-column hero
- replaced generic headline/copy with tighter statement-style messaging
- made the visual element structural rather than decorative
- improved CTA contrast and button hierarchy
- increased whitespace and section breathing room

## What did not change
- no broad repo restructuring
- no unrelated file changes
- no component abstraction pass
- no unnecessary JavaScript added

## Verification criteria used
- hierarchy is stronger than the baseline
- section spacing is visibly more controlled
- image usage has a structural role
- implementation remains simple HTML/CSS
- change stays scoped to the hero fixture only

## Verdict
- PASS

## Confidence
- Medium-high for Codex-oriented behavior

## Remaining limitation
This is still a fixture-based validation inside a Codex+OMX session. A future pass should validate the adapter against a real project file in a live frontend repository.
