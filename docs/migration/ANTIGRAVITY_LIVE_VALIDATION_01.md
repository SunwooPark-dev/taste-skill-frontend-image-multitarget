# Antigravity Live Validation 01

## Validation target
`adapters/antigravity/ANTIGRAVITY_PROMPT.md`

## Goal
Validate that the Antigravity adapter behaves like a strong conversation-start prompt for frontend judgment, not just a restatement of the imported skill.

## Validation method
Prompt-behavior simulation based on the Antigravity startup style described in the adapter:
- explicit assumptions
- minimal-change orientation
- interpretation options on ambiguity
- implementation-friendly output

This is a **prompt-behavior validation pass**, not a full live Antigravity runtime execution.

## Scenario 1 — Ambiguous direction
Prompt:
> Make this site feel more premium.

Expected behavior:
- state assumptions
- avoid immediate overconfident redesign dump
- present 2–3 interpretation options if ambiguity is high

Observed fit:
- the adapter strongly instructs the system to state assumptions first
- it explicitly requires interpretation options when ambiguity is high
- it pushes toward scoped judgment rather than uncontrolled style generation

Verdict:
- PASS

## Scenario 2 — Focused change
Prompt:
> Improve this hero without changing the rest of the page much.

Expected behavior:
- preserve structure where possible
- stay focused
- define verification goals

Observed fit:
- the adapter explicitly says minimize changes
- it asks for the smallest useful change before proceeding
- it reinforces verifiable goals before completion

Verdict:
- PASS

## Scenario 3 — Image-led but buildable
Prompt:
> I want image-led direction, but it still has to be easy to build.

Expected behavior:
- images treated as structural design material
- readability and hierarchy preserved
- output remains coding-agent friendly

Observed fit:
- the adapter keeps image-led direction conditional and structured
- it says images should be structural, not filler
- it preserves implementation-friendly output as a primary constraint

Verdict:
- PASS

## What worked
- stronger ambiguity handling than the first import version
- clearer “smallest useful change” framing
- better guardrail against decorative overreach
- stronger alignment with implementation-friendly frontend decisions

## Remaining limitation
This is not yet a live Antigravity app session. It is a high-confidence prompt-behavior validation pass derived from the adapter design and the surrounding validation framework.

## Recommended next step
Paste `adapters/antigravity/ANTIGRAVITY_PROMPT.md` into a real Antigravity conversation and run at least one ambiguous and one scoped frontend prompt to confirm the same behavior holds live.
