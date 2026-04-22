# AGENTS.md — Codex App adapter for Taste Skill frontend image workflow

## Purpose
Use the imported frontend image skill as a **premium frontend reference discipline**.

Do **not** treat it as a generic image-generation gimmick. Its value is in helping Codex produce frontend work that feels:
- premium
- image-led when appropriate
- strongly structured
- anti-slop
- implementation-friendly

## Core rules
1. Think before acting.
2. Start with the minimum viable implementation.
3. Only modify what is necessary.
4. Set verification criteria before calling the task done.
5. If uncertainty materially affects correctness, ask.
6. Do not perform unnecessary refactors.

## When to use this adapter
Use this guidance when the task involves:
- hero section design
- landing page structure
- premium marketing site direction
- redesigning weak frontend layouts
- translating image-first design ideas into codeable UI

Do **not** over-apply it to unrelated backend or infrastructure work.

## Operating style
When the task is frontend-heavy:
- prefer premium, implementation-friendly design references over generic filler
- avoid repetitive AI aesthetics, dashboard-card spam, weak hierarchy, and dense clutter
- preserve strong whitespace, visual rhythm, and image-led composition
- keep outputs structured enough that a developer can implement them directly

## Preferred workflow
1. Clarify the exact frontend target:
   - one section
   - one page
   - redesign of existing UI
2. Decide whether image-first ideation is actually useful.
3. If it is useful, derive a concrete design direction:
   - theme paradigm
   - hero structure
   - section rhythm
   - typography character
   - image treatment
4. Convert the direction into minimal implementation steps.
5. Implement only the necessary scope.
6. Verify layout, hierarchy, spacing, and readability after changes.

## Translation rule
Always translate visual direction into codeable decisions such as:
- section ordering
- text hierarchy
- spacing rhythm
- component grouping
- image placement
- CTA priority
- contrast and readability constraints

Avoid stopping at “moodboard language.”

## Anti-slop constraints
- No generic purple/blue AI glow unless clearly justified.
- No cloned section patterns without a reason.
- No dense, overfilled layouts.
- No weak headline hierarchy.
- No image use as meaningless decoration.
- No implementation-unfriendly mood art when the task is frontend.
- No “premium” that is just beige serif text with no structure.
- No fake complexity that hides weak composition.

## Required decision questions
Before changing code, decide:
1. Is this task image-first, layout-first, or redesign-first?
2. What is the smallest change that improves quality materially?
3. What proof will show the result is better?

## Verification checklist
Before completion, confirm:
- hierarchy is obvious
- hero is clean and intentional
- imagery supports structure
- section spacing is controlled
- layout is implementable
- output avoids obvious AI-template patterns
- the diff stayed scoped
- no unnecessary structural rewrite happened

## Response preference
For Codex work, prefer:
- concrete implementation steps
- file-aware suggestions
- minimal, testable diffs
- short rationale

Avoid:
- abstract art-direction monologues
- broad redesign proposals without execution shape
