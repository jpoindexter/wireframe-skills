---
name: wireframe-handoff
description: "Use when presenting wireframes to stakeholders, clients, or executives; when wireframes are ready for build and developers need a handoff; when a developer asks \"what happens when...\"; when annotating behavior, states, data sources, validation, or edge cases; when built screens drift from the wireframes during development; or when deciding what to spec in the wireframe versus leave to the build team. Also fires when preparing design alternatives for a sign-off meeting."
---

# Wireframe Handoff — Present, Annotate, Ship

## Overview
A wireframe isn't done when it's drawn — it's done when it survives three gates: presented to the people it affects, annotated so developers never guess, and followed through until the shipped screen matches the intent. Most product damage happens *between* phases (handoffs), not within them; this skill hardens the seams.

## When to Use
- Presenting wireframes for sign-off, alignment, or pitch — executives, clients, support, sales, QA
- Preparing the package developers build from: annotations, states, edge cases, flows
- During build: behavior questions, wireframe-to-code drift, last-minute changes
- Post-release: feedback loops and retro on where communication broke
- **NOT for:** in-progress design critique among the product triad — that's earlier-phase exploratory feedback, not a handoff gate
- **NOT for:** hi-fi visual spec handoff (redlines, spacing, color values) — that's design-tokens territory, downstream of wireframes

## Presenting Wireframes

### Establish context before screen one
- Say explicitly that structure-over-style is a deliberate choice: it keeps the room solving user problems instead of debating colors and branding.
- Say wireframes are cheap to revise — this licenses feedback people would withhold from anything that looks finished. Late input that fixes an oversight is a win, not a derailment.
- Show a brief evolution (problem statement → structural outline → concepts → proposal). Jumping straight to the answer is jarring to first-time viewers; origins prove diligence and build credibility.

### Narrative order: problem → goal → flow → screens
1. **Project background** — what created the need: the version that missed, the tool that aged out, the feature that had to land. One clear purpose statement.
2. **The user and their problem** — a specific persona or use case, stated plainly. Decisions anchored to a real user read as evidence; decisions without one read as opinion.
3. **The goal** — what success looks like for that user and for the business metric it moves.
4. **The flow, then the screens** — walk the user's actual tasks end to end, narrating the improvement at each decision point. Show only relevant steps and forks; a complete tour of everything you tried loses the room.

### Audience tailoring
| Audience | Lead with | They will probe |
|---|---|---|
| Executives / clients | Business metric moved, cost, risk, timeline | Scope, what slips, why now |
| Developers | Flows, states, feasibility, novel interactions | Edge cases, data sources, effort |
| Support / documentation | What changes for existing users | Migration pain, ticket volume |
| Sales / marketing | What's promisable and when | Demos, differentiators, dates |
| QA | Expected behavior per state | Boundaries, error paths, permissions |

### Alternatives and trust
- **Admit uncertainty.** Name the areas with open questions. In a room of experts, having all the answers reads as dismissive; an incorporated suggestion converts a skeptic into an advocate.
- **Bring prepared alternatives** for any area likely to face resistance — including a cheaper-to-build fallback you keep in your back pocket. Considered-and-compared beats defended-and-cornered.
- **Address the negatives yourself:** tech debt incurred, deadlines at risk, teams temporarily burdened. Volunteering the costs buys the credibility your benefits claims spend.
- **Listen without defending.** Understand the objection fully before responding; feeling unheard destroys goodwill faster than any design flaw.
- **Close with a recap:** decisions made, questions parked, owner and next step for each. The recap *is* the deliverable of the meeting.

## Annotation That Developers Need
A wireframe shows the happy path at rest. Annotations carry everything else. The rule: **annotate anything a developer would otherwise have to guess** — and nothing a standard component already defines.

| Annotation type | What to specify | Example |
|---|---|---|
| Interaction | What every control does on click/tap/enter/hover; destination or result | "Row click opens detail panel; chevron expands inline" |
| Component states | Default, hover, focus, active, disabled, selected — and what triggers each | "Save disabled until any field is dirty" |
| Screen states | Empty, loading, partial, error, ideal — all five, per screen | "Empty list: illustration + 'Create your first…' CTA" |
| Data source | Where each value originates: API field, user input, computed, cached | "Balance = `accounts.available`, refreshed on focus" |
| Data rules | Formats, truncation, default sort, pagination size, max lengths | "Names truncate at 40 chars with tooltip; 25/page" |
| Validation | When it fires, the rule, exact error copy (or copy owner) | "On blur; 'Card number must be 16 digits'" |
| Edge cases | Long values, zero items, 10k items, offline, concurrent edit | "Two editors: last-write-wins + stale banner" |
| Conditional logic | What shows/hides/changes per prior answer or context | "Business account? → show VAT field, skip step 3" |
| Permissions | Who sees/does what; unauthorized behavior: hide vs disable vs explain | "Viewers: export hidden; editors: disabled + tooltip" |
| Motion | What transitions between states, duration intent, reduced-motion fallback | "Panel slides in ~200ms; instant if reduced-motion" |
| Responsive | What reflows, collapses, or hides per breakpoint; touch vs pointer deltas | "Table → cards below 640px; hover actions inline" |
| System behavior | Back button, refresh, deep link, unsaved-changes, session expiry | "Back mid-wizard restores step with data intact" |
| Content | Real copy vs placeholder, and who owns final wording by when | "Error strings final; marketing owns hero copy" |
| Accessibility | Focus order, announcements, labels for icon-only controls | "On error, focus moves to summary; `role=alert`" |
| Persistence | What survives refresh, navigation, session end | "Draft autosaved per step; survives logout" |

### Annotation discipline
- **Number annotations and point each at its element.** Prose paragraphs floating beside a screen don't survive contact with a sprint.
- **Annotate deltas, not defaults.** If the design system's dropdown already defines keyboard behavior, reference the component — don't re-spec it. Re-stating the obvious buries the one note that matters.
- **Spec vs leave to build:** spec *behavior, rules, copy, and states* (product decisions); leave *implementation approach, exact pixels, and standard component internals* to the build team and the design system. Over-specifying signals distrust and goes stale first.

## The Handoff Package
A complete handoff contains:

1. **Annotated wireframes** — every screen, every screen state (empty/loading/partial/error/ideal).
2. **Flow map** — how screens connect: entry points, exits, branches, and back-navigation behavior.
3. **Edge-case inventory** — the "what happens when…" list, answered in advance.
4. **Content status** — final copy in place, or a named owner and date for what's pending.
5. **Open-questions log** — decided vs pending, so devs know which gaps are intentional.
6. **Frontend prototype** for novel interactions — coded in the product's real stack, not a prototyping tool. It aligns the team and surfaces technical problems before production time is committed. Not a developer? Ask one for a rough version.
7. **Component mapping** — each wireframe control matched to its live code counterpart. Built up over a few projects, this becomes a library where translation is nearly free.
8. **Decision record** — what was considered and rejected, with why, so settled questions don't get re-litigated mid-sprint.

The package is necessary, not sufficient: **walk through it together** with the dev team. Combing through the experience side by side beats weeks of ticket and chat ping-pong (Jenny Wen's working-with-engineers advice, cited in the source).

## Following Through
- **Be present for early build.** Review the first coded screens against the wireframes while divergence is cheap to correct.
- **Budget slack for late changes.** New stress cases *will* surface during development; a schedule with zero iteration room converts each one into a crisis.
- **Handle drift by diagnosis, not objection.** When built ≠ wireframed, ask why first: a feasibility discovery is information (update the wireframe), a miscommunication is a process gap (fix the handoff channel). Only then is it an error.
- **A behavior question with no answer is a new wireframe.** When a developer asks "what happens when…" and the package is silent, the answer belongs in an updated frame or annotation — a chat reply evaporates and the next developer asks again.
- **Post-release, plug into the feedback stream.** Get access to the support team's issue tracker or regular reports; frequency × severity of reported problems is your next iteration's input. No research team required.
- **Retro on the seams.** Classify what went wrong: within a phase (wrong requirements, buggy code) or between phases (misunderstanding, misplaced expectations)? Within-phase imperfection usually ships fine; between-phase communication failure is what makes products suffer. Fix the handoff, assume good intent, never blame the person.

## Quick Reference

| Situation | Do |
|---|---|
| Opening a presentation | Context first: why structure over style, why feedback is still cheap |
| Ordering the presentation | Problem → goal → flow → screens; relevant decision points only |
| Contested design area | Bring prepared alternatives, including a cheaper fallback |
| Room full of experts | Name your open questions before they do |
| Q&A | Listen fully, don't defend; close with decisions + owners + next steps |
| Dev asks "what happens when X" | Answer in the wireframe (annotation or new frame), never only in chat |
| Novel interaction | Frontend prototype in the product's real stack |
| Deciding what to annotate | Anything a dev would guess; skip what the component library defines |
| Built screen differs from wireframe | Diagnose first: feasibility discovery vs miscommunication vs error |
| Coding has started | Stay engaged: joint walkthroughs, early-build reviews, slack for changes |
| Post-release | Issue-tracker access; rank feedback by frequency × severity |
| Project retro | Classify failures within-phase vs between-phase; fix the seam |

## Anti-Patterns

| Mistake | Fix |
|---|---|
| Jumping straight to the proposed design | Show brief evolution — origins build credibility |
| Touring every option you ever tried | Only the relevant steps and decision forks |
| Polished visuals at the approval stage | Reads as finished; structure invites the feedback you need |
| Projecting certainty on open questions | Name them — collaborators become advocates |
| Hiding the costs (debt, slipped dates) | Volunteer them; honesty compounds into trust |
| Handoff = file link dropped in chat | Annotated package + a live walkthrough together |
| Annotating only the happy path | Five screen states + edge-case inventory, per screen |
| Re-specifying standard component behavior | Annotate deltas; reference the design system |
| Answering behavior questions in chat | Update the wireframe — chat answers evaporate |
| Disappearing once coding starts | Early-build reviews; schedule slack for stress cases |
| Treating all drift as developer error | Diagnose: feasibility find vs miscommunication vs mistake |
| Blaming individuals in the retro | Team owns what ships; strengthen the handoff instead |
| Treating wireframes as the deliverable | They're a thinking-and-communication tool; the product is the deliverable |

## Companion Skills

| Situation | Co-fire |
|---|---|
| Choosing the controls that appear in the frames | wireframe-elements |
| Specifying the full per-component state matrix | components-and-states |
| Annotating empty, zero-data, and loading states | flow-empty-states |
| Annotating error states and writing error copy | flow-errors |
| Handing off visual specs (spacing, color, type) | design-tokens |
| Annotating focus order, announcements, labels | accessibility-and-inclusive-design |
| Final copy for labels, errors, empty states | ux-writing-and-content |
| Agreeing loading/failure architecture with devs | dec-rendering-architecture |

> "Design isn't finished until somebody is using it." — Brenda Laurel

Handoff is not the finish line; shipping to a user is. Everything in this skill exists to keep the idea intact across that last gap.

*Distilled from* Wireframing for Everyone *(Michael Angeles, Leon Barnard, Billy Carlson — A Book Apart, 2023), extended with production practice.*
