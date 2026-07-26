---
name: wireframe
description: "Use when the user invokes /wireframe, asks to wireframe, sketch, or block out a screen, flow, or app before high-fidelity design or code — or when a build is jumping straight to polished UI without structural exploration, stakeholders demand pixel-perfect too early, or an existing wireframe needs review, critique, or handoff. Dispatcher that runs the full wireframe-* family and co-fires the matching design skills."
---

# Wireframe — Full-Family Dispatcher

## Overview

Entry point for the `wireframe-*` skill set — the complete wireframing discipline distilled from *Wireframing for Everyone* (A Book Apart, 2023): fundamentals → ideation → elements → principles → collaboration → feedback → handoff. `/wireframe` loads the **whole family** so every phase of the work is governed, then co-fires the companion design skills the task touches. Router plus canon, not a recital.

## When to Use

- `/wireframe` invoked, with or without arguments
- Any request to wireframe, sketch, mock up structure, or "block out" screens before visual design
- A project is skipping ideation — first idea heading straight to high fidelity or code
- Reviewing, critiquing, presenting, or handing off wireframes
- **NOT for** visual styling decisions (color, type, elevation) — that's /design territory after structure is settled
- **NOT for** pure flow-logic questions with no screen structure at stake — use userflow directly

## The Dispatch Process

1. **Resolve the target.** Argument text first; else the surface active in the conversation; else inspect the project (routes, screens). Ask at most one question, only if it changes the work.
2. **Load the entire wireframe family** via the Skill tool (read `skills/<name>/SKILL.md` in other harnesses) — all seven, in this order:
   - `wireframe-fundamentals` — fidelity choice, tool choice, what "good" means
   - `wireframe-ideation` — structure before screens; divergent exploration
   - `wireframe-elements` — components, patterns, page templates
   - `wireframe-principles` — hierarchy, alignment, clarity at grayscale
   - `wireframe-collaboration` — team sessions, roles, ownership
   - `wireframe-feedback` — critique structure, acting on feedback
   - `wireframe-handoff` — presenting, annotation, shipping to build
3. **Co-fire companion design skills** from the routing table below — max 4 per pass, chosen by what the task actually touches.
4. **State the load in one line** ("Running wireframe family + flow-app-shell, components-and-states") and do the work under their combined rules. Phase-specific skill wins conflicts (wireframe-handoff beats wireframe-ideation on an annotation question).
5. **Check output against every loaded skill's Anti-Patterns section** before presenting.

## Companion Routing Table

| Task signal | Co-fire |
|---|---|
| New app / greenfield screens | userflow (routes flow-app-shell, flow-navigation, flow-onboarding), layout-and-composition |
| A specific flow (auth, checkout, search, settings...) | userflow — it routes the right flow-* skill |
| Component-level questions (what control, what states) | components-and-states |
| Layout, spacing, grid decisions at wireframe fidelity | layout-and-composition, grid-and-spacing |
| Information architecture, nav structure | flow-navigation |
| Labels, microcopy, real-content-over-lorem calls | ux-writing-and-content |
| Critique or design-review session | dec-nielsen-heuristics, usability-heuristics |
| Named-principle reasoning (hierarchy "why", cognitive load) | dec (routes the dec-* canon) |
| Moving up-fidelity after wireframes are approved | design (routes the visual family), hallmark for taste stakes |
| Wireframing an iOS-native surface | ios (routes the ios-* family) — wireframe family still governs structure |
| Pre-commit sanity check on a chosen direction | blind-premortem, blind-consider-the-opposite |

## Traceability

`references/source-map.md` maps the book's seven chapters onto these seven skills
and lists all 39 sources the book cites, with the skill that carries each. Use it
to attribute a claim, or to check whether something is the book's position or this
pack's extension. Sibling skills reach it at `../wireframe/references/source-map.md`.

**Rule:** if you state something as the book's, name the origin. If you state
something the book doesn't say, mark it as production practice. The skills are
explicitly "extended," and that extension must stay visible.

## Deliverable

For any request that produces or reviews wireframes, emit the wireframe as structured output the user can act on:

- **ASCII/box wireframes** inline for quick structural discussion — every region labeled, hierarchy shown by position and size
- **HTML grayscale wireframes** (single self-contained file, no color beyond grays, real labels, no lorem where a decision hides) when the user wants something clickable or presentable
- Always accompanied by: screen inventory (purpose / primary action / empty-loading-error states), open questions, and annotations per wireframe-handoff when build is the next step

## Required Context

Establish before dispatching:
- **The surface** — which screen, flow, or app. Argument text, else the active surface, else inspect the repo.
- **The phase** — is structure unknown (ideation), agreed (elements/principles), or settled (handoff)?
- **The audience for the output** — you, the team, stakeholders, or developers. Fidelity follows.
- **Whether an artifact already exists** to review, or this is greenfield.
- **Constraints that pre-decide things** — an existing design system, platform, or locked IA.

If one line and ambiguous, dispatch on the most likely reading and state the assumption.

## Evaluation Procedure

1. Resolve the target and name the phase.
2. Load the family; pick ≤4 companions from the routing table.
3. Do the work under the combined rules; phase-specific skill wins conflicts.
4. Check the output against **every loaded skill's Anti-Patterns table** before presenting.
5. Confirm the deliverable carries a screen inventory and open questions, not just frames.
6. State what you did **not** resolve — the open questions are part of the artifact.

## Output Format

```
Loaded: wireframe family + <companions>
Phase: <ideation | structure | principles | handoff>  ·  Fidelity: <no-fi…late-phase>
<the wireframe — ASCII/box inline, or grayscale HTML if it must be presentable>
Screen inventory: <screen> — purpose / primary action / empty+loading+error
Open questions: <what this artifact does not yet answer>
Anti-pattern check: <which skills' tables were applied>
```

## Quick Reference

| Situation | Action |
|---|---|
| `/wireframe a settings page for X` | Load family + userflow(flow-settings) + components-and-states; produce wireframe + inventory |
| `/wireframe` mid-project, no args | Infer surface from recent work; inspect repo if needed |
| "Review this wireframe" | Family + dec-nielsen-heuristics; audit against every Anti-Patterns section |
| "Ready for build" | wireframe-handoff leads; produce annotation package |
| User named a specific wireframe-* skill | Invoke it directly — skip the dispatcher |

## Anti-Patterns

| Mistake | Fix |
|---|---|
| Summarizing family skills from memory | Load every SKILL.md — the value is in the specifics |
| Jumping to visual design because the tool renders pretty | Grayscale, boxes, real labels; /design comes after approval |
| Co-firing every companion skill "to be safe" | Family always; companions max 4, chosen by the routing table |
| Producing one layout and calling it done | wireframe-ideation demands divergent alternatives before converging |
| Shipping a wireframe with lorem over key decisions | Real labels wherever a word IS the design decision |

*Part of the wireframe-skills family — github.com/jpoindexter/wireframe-skills.*
