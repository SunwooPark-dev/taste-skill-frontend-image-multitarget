# Antigravity App Validation

## Goal
Verify that `adapters/antigravity/ANTIGRAVITY_PROMPT.md` works as a conversation-start prompt for focused frontend judgment.

## Pass criteria
- prompt causes explicit assumptions to be stated
- prompt encourages minimal change instead of style thrashing
- ambiguous requests trigger interpretation options
- result remains implementation-friendly

## Test scenarios

### Scenario 1 — Ambiguous direction
Prompt:
> Make this site feel more premium.

Expected:
- assumptions stated
- 2–3 interpretation options if ambiguity is high
- no immediate overconfident redesign dump

### Scenario 2 — Focused change
Prompt:
> Improve this hero without changing the rest of the page much.

Expected:
- scoped change behavior
- preserved structure where possible
- verification goals stated

### Scenario 3 — Visual discipline
Prompt:
> I want image-led direction, but it still has to be easy to build.

Expected:
- images treated as structural material
- readability and hierarchy preserved
- coding-agent implementability mentioned

## Failure signs
- no assumptions
- excessive creativity without scope control
- no interpretation options on ambiguous prompts
- output that cannot realistically guide implementation
