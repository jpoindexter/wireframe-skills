---
name: wireframe-feedback
description: "Use when requesting or giving feedback on wireframes, running or facilitating a design critique, or preparing wireframes for stakeholder review. Also fires when feedback arrives vague ('make it pop', 'I don't like it'), as solutions instead of problems ('just move it to settings'), when deciding which feedback to act on after a review, or when a review session went sideways — loud voices dominating, defensiveness, or the same debates repeating without decisions."
---

# Wireframe Feedback & Critique

## Overview
Creating and analyzing are different processes — never do both at once (Corita Kent's rule 8). Critique is structured analysis: evaluate the design against defined criteria, gather enough actionable information to fuel the next creative pass, then stop. The goal is a better design for the user, not consensus, approval, or defense of the current version. You are not your design.

## When to Use
- Requesting feedback at any wireframe stage — early concepts through near-final detail
- Facilitating a team critique, stakeholder review, or async comment round
- Translating vague or solution-shaped feedback into usable problems
- Triaging a pile of post-review comments into a plan
- **NOT for:** usability testing — critique is expert/team analysis; user evidence needs real users on real tasks
- **NOT for:** sign-off meetings — critique improves the design; approval is a separate decision forum with different stakes

## Asking for Feedback

### Frame the ask — goal, stage, question
- **Never ask "any thoughts?"** Open asks produce reactive taste comments. State three things: the user goal the screen serves, how done the work is, and the specific question. "This is the checkout flow for guest users, about 30% done. Is the step order right, and is anything missing before payment?"
- **The 30/90 rule** (Jason Freedman, 42Floors): request "thirty percent feedback" early — reviewers agree details are unfinished and focus on structure and direction — and "ninety percent feedback" near completion — no big swings, catch the details. Two checkpoints minimum per design.
- **Fidelity signals the feedback level.** Low-fi sketches invite structural input; polished wireframes invite pixel nitpicks. Presenting hi-fi when you want directional feedback guarantees you get comments on the wrong layer.
- **Say what's out of bounds.** "Visual style is placeholder — ignore fonts and spacing" prevents an entire class of wasted comments.
- **Ask when you've taken the idea as far as you can alone.** That stall is the signal. Early asks are the hardest (fear of showing unfinished work) and the most valuable — set the precedent at 30%, not 90%.

### Match reviewer to question
- **Team members** (PM, dev, research, design) — flow logic, feasibility, consistency; they advocate for user and product, and can double as notetakers
- **Subject matter experts** — domain correctness (an order-flow expert for a trading app); invite early, they rarely get asked and usually welcome it
- **Stakeholders** — goal alignment and constraints; actively-involved ones early, higher-ups later for awareness
- **If you don't want someone's opinion, don't invite them.** Every invitee is expected to participate; spectators dilute the room and inflate the comment pile.

## Giving Constructive Feedback

The five characteristics below come from Adam Connor and Aaron Irizarry's *Discussing Design*, as adapted by the source. Constructive feedback is **trust-based** (shared goal: improve the product), **analytical** (breaks the design into parts and traces effect on the task), **specific** (names the element and the failure), **open-ended** (states the problem, leaves the solution to the designer), **objective** (argues from user goals, not personal taste), and **actionable** (usable in the next iteration). Two counterproductive modes to catch: **reactive** ("I hate this" — pure emotion, no analysis) and **directional** ("just put it in settings" — a solution with no stated problem).

### Problem, not solution
Lead with the observation, tie it to the user's goal, leave the fix open. If you must suggest, give the why first — a suggestion without its underlying problem can't be evaluated or improved on.

### Phrasing rewrites
| Bad (reactive/vague/directional) | Good (analytical, tied to the user) |
|---|---|
| "The nav is confusing" | "The nav hides the path to privacy settings — the thing our research says users come here for" |
| "I don't like this button" | "'Cancel' could read as canceling the subscription instead of canceling the edits" |
| "Make the CTA pop" | "The CTA isn't visually prominent; if it's the primary action on this screen, users will miss it" |
| "Move this to the settings page" | "This block interrupts the checkout task — what led to placing it inline rather than in settings?" |
| "This form won't work internationally" | "Non-US users can't map these address fields; consider localizing labels per country" |
| "I love it!" | "The single-column layout keeps the task linear — keep that quality through the rest of checkout" |

Positive feedback earns its place only when specific: name *what* works and *why*, so it survives iteration instead of being accidentally designed away.

### Questions before verdicts
Open with questions that surface the designer's reasoning: Why this pattern here? How does it align with the user's intent in this scenario? Does it solve the right problem? What isn't feasible? What other directions were considered? Is anything missing? — then evaluate.

### Receiving feedback
- **Active listening:** reflect back what you heard ("So the concern is the label, not the placement?") until the giver confirms. It keeps you listening instead of rehearsing a defense, and forces vague comments into precision.
- **Mine counterproductive feedback, don't dismiss it.** Reactive and directional comments usually contain a real problem. "What do you mean by that?" and "How does this affect the user's task?" convert them.
- **Capture, don't rebut.** Defending each comment live burns the session; clarify, log, decide later.

## Running a Critique

### Structure (45 min for a flow-sized review)
1. **Frame — 5 min.** Goal, stage (30% or 90%), the specific questions, ground rules (problems not solutions; comments during or after the walkthrough — announce which).
2. **Walkthrough — 10 min.** Overview of features and flow first, then screen-by-screen, narrated in the user's terms: "When the user arrives here, they can do X by selecting Y." Never open cold on screen one of twelve.
3. **Discussion — 25 min.** Facilitated analysis against the framed questions.
4. **Close — 5 min.** Thank participants, state what happens next, promise the summary.

### Roles
- **Facilitator** (usually the presenter): presenter, mediator, timekeeper in one. Guides the conversation — establishes the frame, keeps discussion on analysis, moves it forward when stuck, harvests actionable detail. Guides, never defends.
- **Notetaker — dedicated, never the facilitator.** Facilitation and detailed capture are incompatible. Per item: which wireframe, which region of the screen, the comment, who said it. Sticky notes or live comments in the wireframing tool, visible to the room; tag commenters by name so they can verify capture.
- **Participants:** active contributors, each invited for a reason they know.

### Facilitation moves
- **Round Robin** to open: each person in turn — prevents the loudest voice from setting the frame.
- **Actively solicit quiet members**; offer an async channel afterward for anyone who processes slowly or won't speak in a group. Costs follow-up time, buys full coverage.
- **Keep a valid path for dissent** (David Dylan Thomas) — if disagreement has no legitimate outlet in the session, it resurfaces later as a veto.
- **Redirect "I would…" to the user.** Personal preference comments get "what would *the user* do here, based on what we know?"
- **Model the feedback you want** and reset explicitly when the discussion drifts to taste or solutions.
- **The design failing the critique is a success of the critique.** If analysis shows the design doesn't meet objectives, you've saved an iteration — say so and move on.
- **Async critique** works: reviewers comment callouts pinned to wireframe regions on their own time; facilitator consolidates, tags, and follows up on unclear items. Same rules — framed ask, specific questions, named comments.

## Acting on Feedback

### Triage every item
Log all feedback in one shared sheet — item, screen, who said it, status. Donna Spencer's five statuses (*Presenting Design Work*):

| Status | Meaning | Next action |
|---|---|---|
| Agree — now | Accepted, straightforward | Fold into the next pass |
| Agree — later | Accepted, not this iteration | Backlog with a target stage |
| Needs research | Can't decide on current information | Name the question and the method |
| Clarify | Comment not understood (common in async) | Go back to the commenter |
| No | Will not implement | Record the reason, tied to goal or problem statement |

- **Declining is a legitimate outcome** — but only with a recorded reason. Silent drops destroy the trust the process runs on.
- **Circle back to the problem statement** before adopting any new direction. Does it serve the user's goal, or the whims of whoever spoke last? Design by committee is rarely successful.
- **Wrong-assumption feedback triggers research, not patching.** If the critique revealed a missing case (the signup flow never handled "verification email didn't arrive"), review the options — possibly a technical review — before redrawing.

### Close the loop
- Share the summary with participants: what was reviewed, who attended, each item's status. Give people time to respond, clarify, or add before you redraw.
- On the next round, show **old and new side-by-side** with the feedback that drove each change — reviewers instantly see what moved and why.
- **Feedback is a cycle:** integrate → redraw → critique again. Regular critique during wireframing is the cheapest risk reduction in the whole design process.

## Required Context

- **What kind of response you want** — exploration, a choice between concepts, or analysis of one design.
- **The fidelity**, and what it signals about how settled things are.
- **The goals and constraints** the reviewers need in order to judge against something.
- **Who is in the room and why each is there.** Everyone-invited produces noise.
- **What is already decided and not up for debate.** Say it, or it gets relitigated.

## Evaluation Procedure

1. Frame the ask: what stage, what decision, what you specifically want examined.
2. Give reviewers the goal and constraints before the artifact.
3. Run the critique on analysis, not preference — redirect solutions back to problems.
4. Test each piece of feedback against the five characteristics: trust-based, analytical, clear and specific, open-ended, objective.
5. Translate vague reactions into observations tied to a user task before acting.
6. Decide what to act on, what to defer, what to decline — **declines get a recorded reason**.
7. Close the loop: tell reviewers what changed and what didn't.

## Output Format

```
Asked for: <exploration | selection | analysis> on <specific area>
Context given: goals <…> constraints <…> decided-already <…>
Feedback received → restated as observation:
  "<raw>" → "<analytical, tied to a user task>"
Acting on: <list>  ·  Deferred: <list>  ·  Declined: <item — reason>
Loop closed with: <who was told what changed>
```

## Quick Reference

| Situation | Pattern |
|---|---|
| Early concept, direction unclear | 30% ask — structure only, low-fi artifact, details declared unfinished |
| Near-final wireframes | 90% ask — detail correction, no big swings |
| Vague feedback ("make it pop") | Clarifying question: "what problem does the current version cause for the user?" |
| Solution-shaped feedback | Ask for the underlying problem before evaluating the solution |
| Reviewer says "I would…" | Redirect to the user: "what would the user do, per our research?" |
| Loud voices dominate | Round Robin; solicit quiet members by name |
| Reviewer won't speak in a group | Async follow-up channel, consolidated by the facilitator |
| Distributed / timezone-split team | Async critique via pinned callout comments, named and followed up |
| Presenting a complex multi-screen flow | Flow overview first, then screens, narrated in the user's terms |
| Feedback pile after a review | Five-status triage: now / later / research / clarify / no-with-reason |
| Stakeholder taste vs user goal | Arbitrate against the problem statement, in writing |
| Session ends | Thank + next steps + summary with per-item status |
| Next review round | Old vs new side-by-side with the driving feedback |

## Anti-Patterns

| Mistake | Fix |
|---|---|
| "Any thoughts?" as the ask | State goal, stage, and one or two specific questions |
| Hi-fi wireframes for a direction question | Match fidelity to the feedback level you want |
| Waiting until 90% for the first review | 30% checkpoint — early feedback before changes get expensive |
| Facilitator taking the notes | Dedicated notetaker; capture wireframe + region + comment + who |
| Defending each comment live | Clarify, capture, decide in triage |
| Redesigning in the meeting | Critique analyzes; creation is a separate pass after reflection |
| Inviting everyone "for visibility" | Invite only people whose opinion advances this stage |
| Dismissing reactive/directional comments | Mine them: "what do you mean?" / "how does this affect the user's task?" |
| Incorporating every comment | Triage against the problem statement; design by committee fails |
| Silently dropping feedback | Every item gets a status; "no" gets a recorded reason |
| Only critical comments | Name what works and why, so it survives iteration |
| Treating critique as an approval gate | Separate forums: critique improves, sign-off decides |

## Companion Skills

| Situation | Co-fire |
|---|---|
| Presenting, versioning, or sharing wireframes around the critique | wireframe-collaboration |
| Grounding critique comments in named heuristics instead of taste | dec-nielsen-heuristics, usability-heuristics |
| Delivering a hard critique so it lands as closable, not personal | si-corrective-feedback |
| Before marking feedback "no" — state the strongest version first | blind-steelman |
| All feedback confirms the current direction | blind-consider-the-opposite |

*Distilled from* Wireframing for Everyone *(Michael Angeles, Leon Barnard, Billy Carlson — A Book Apart, 2023), extended with production practice.*
