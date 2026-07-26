---
name: wireframe-ideation
description: "Use when starting a screen design from a blank canvas, jumping straight into one layout, or treating the first idea as the final idea — or when structure is missing before screens (no user flow, sitemap, or content inventory yet). Also fires when layout alternatives are needed, when divergent exploration should precede committing to a direction, when ideation stalls after one or two sketches, or when stakeholders debate what belongs on a page before anything is drawn."
---

# Wireframe Ideation — Structure Before Screens

## Overview
The first draft's only job is to get ideas out of your head and onto the screen. Structure (flows, IA, content) comes before frames; quantity comes before quality; converging comes last. Connections between screens are more expensive to rethink than the screens themselves — validate them first.

## When to Use
- Kicking off any multi-screen design: app feature, site section, redesign, new product
- One screen with an unknown layout — before drawing the "obvious" version
- A team arguing about page content or navigation with nothing visual on the table
- Breaking "first sketch became the shipped design" habits — forcing real alternatives
- **NOT for:** refining a chosen direction — that's layout/composition work, past ideation
- **NOT for:** visual design, spacing, type, or color decisions — wrong fidelity entirely
- **NOT for:** validating whether the problem is worth solving — do discovery first

## Structure First: Flows, IA, Content Inventory

### Pick the entry artifact
- Small project (≤3 screens, one task): sketch directly — structure artifacts are overhead.
- Multi-step or multi-screen: outline first. Designing screens independently loses the connections between them; the connections are the product.
- Litmus test: if you can't narrate the design as a flow of logic ("user arrives from X, does Y, sees Z"), it isn't reasoned yet. Flow it out before sketching anything.

### Sitemap — system structure
- Boxes + lines showing parent-child and sibling page relationships. Truncate to the top 2–3 levels; deeper rarely informs wireframes.
- Count children per category before designing navigation — 4 children and 4,000 need different nav patterns.
- Redesigning an existing product: sitemap the *current* state first. It exposes confusing groupings, consolidation candidates, and alternative categorizations for free.
- A sitemap shows hierarchy, not behavior. Never derive navigation solely from it — users cut across hierarchy constantly.

### User flow — task structure
- One flow per concrete use case with a clear destination (post a photo, complete checkout). Pull use cases from the goals/problems list, not from the nav.
- Build backward: draw the success end-state screen first, then work back step by step to the entry point (home page, search result, shared link). Backward construction keeps the path optimal instead of accreting steps.
- Then walk the happy path forward and branch: what fails at each step, what else the user might do (password recovery, empty results, timeout, abandon).
- Don't diagram every scenario — but write down each flow you exclude. Exclusions must be decisions, not omissions.

### Wireflow — both at once
- A row of deliberately low-detail wireframes joined by arrows: the user's path plus just enough UI to anchor it.
- Record only where and when the interface *changes* — those change-points are the screens worth wireframing. Skip intermediate interactions.
- If a wireflow step is hard to draw, the flow is wrong, not the frame. Fix the flow.

### Content inventory
- List every content block the screen needs (sticky notes, real or digital, or a plain text list): headline, price, hours, CTA, social proof — concepts and purposes, not final copy.
- Order the blocks top-to-bottom by priority. This ordering *is* the proto-layout; placement decisions later become mechanical.
- Overflow test: if the ordered list clearly exceeds one page, force the "what HAS to be here" debate now. Demote losers to another page or delete them.
- Circulate the prioritized list to stakeholders before drawing anything. Priority disagreements are cheapest to resolve while they're still sticky notes.

## Laying the Foundation

### Content before layout
- Content is the organ; the wireframe is the skeleton. Never draw the frame before knowing what fills it, its priority, and its purpose — arbitrary boxes never match their contents.
- Give content the form it wants; don't force it into a structure drawn first. For content-heavy screens, place *only* the content on the canvas with zero layout chrome, then let structure emerge.
- Space budgeting is impossible without content: you can't size a region for a paragraph you haven't identified.
- The named technique is **content modeling**. Derek Gillette's working definition: a content model "uses blocks (think of these like sticky-notes) to lay out the must-haves, priorities, and order of the page… not actual final copy, but the high-level concepts, ideas, and purposes of each section." Blocks and priority order — no prose, no layout.

### Inside-out design
- Start with the smallest unit of content (one news item, one product card, one list row) and design *it* fully. Build outward: unit → group → section → screen. Draw the device/browser box last.
- Outside-in (screen box → sections → details) shifts you into fit-and-polish thinking before content thinking. It is the default human habit; resist it deliberately.
- While designing the unit, ask content questions ("does this need an image? button or link?") — not layout questions ("does this fit?").

### Critical interaction first
- If the product has one make-or-break interaction (checkout, record creation, the step users churn on), wireframe *that* first — ignore how the user got there.
- All-or-nothing task sequences (order placement, form submission) fail entirely on friction at one step; that step deserves detail before anything else gets breadth.
- You don't owe the whole flow equal attention at the start. Depth on the cornerstone, breadth later.

### Prior art
- Search for how others solved the same problem before inventing (file restore → look at Dropbox's version history). Borrow the *pattern*, never the pixels.
- Look outside your industry on purpose: a music app's playlist structure can seed a food-ordering screen. Cross-domain borrowing produces less derivative results than competitor-copying.
- Keep a screenshot collection during research; it feeds the collage technique below.

## Generating Ideas

### Quantity mechanics
- Timer rounds: 1–3 minutes per sketch. Short enough to hurt, long enough to produce something recognizable.
- Minimum 4 rounds per screen or design problem; expect diminishing returns at 5–8 variations. Do not converge before at least 4–5 *structurally distinct* layouts exist — restyled versions of one skeleton count as one.
- Crazy 8s / 8-Up: fold or template 8 panels, 8 ideas in 8 minutes. The forced pace bypasses the inner critic.
- Originality arrives late in a session — the most original ideas come after the obvious ones are exhausted. When you want to stop: make exactly one more, deliberately stranger than the rest. One extra early idea propagates into five later.
- Fidelity cap during ideation: boxes, lines, scribbled labels. The moment you adjust spacing or choose type, you've left ideation — stop and return to volume.
- Bad ideas are working material, not waste: you often can't see a design dead end until you've sketched into it. A cheap sketch is the cheapest place to discover one.

### Variation prompts
- When variations converge on one shape, jolt with a "What if…?" constraint — impractical is fine; the goal is a different frame, not a real requirement:
  - What if it were voice-only? No imagery allowed? Used only by teenagers? Had a personality (stoic, generous)?
- Stress-case prompts double as free QA — sketch for the worst case, not the demo case:
  - What if the table has 10,000 rows? The connection is dial-up slow? The device is the smallest sold? All text is German-length? Font sizes are doubled?
  - Rule of extremes: treat anything that can be big as colossal and anything small as microscopic; a layout that survives both ends scales.
- When the problem statement itself is narrow ("get more Signup clicks"), reframe as "How might we…?" ("…increase subscribers?") — it legitimately widens the solution space to landing pages, referral loops, flow improvements.

### Anything-goes inputs
- Ideation sketches are for you and a few teammates only. Collage is legal: screenshots + sticky notes + text fragments + wireframe pieces, arrows between them.
- Screenshot-plus-wireframe collage is the fastest way to sketch new functionality inside an existing product — real context, zero redrawing.
- A "good" ideation artifact is one that provokes a productive conversation. That is the entire quality bar at this stage.

## Converging

- Health check before converging: many good ideas plus a few terrible ones = correct. All good → you never actually diverged. All bad → the foundation (flow/content) is missing; go back a phase.
- Stuck mid-ideation = an unanswered question, not a creativity failure. Name the question, get the answer (existing research, SME, stakeholder), then resume. Don't sketch around a knowledge gap.
- Flagged ideas get a note — what's unresolved, what the next step would be — so returning to them costs nothing.
- Output of ideation is **several** directions, not one: keep ≥3 distinct wireframes worth developing, discard the weak ones, and record the flows/ideas you're consciously dropping.
- Selection criteria, in order: honors the prioritized content order → survives the stress prompts → fewest flow steps to the user's goal → sparks the best stakeholder conversation. Visual appeal is not on the list.

## Quick Reference

| Situation | Move |
|---|---|
| Multi-screen project, nothing mapped | User flow before any frames; build it backward from success |
| Hierarchy/navigation questions | Sitemap, truncated to top 2–3 levels; count children per category |
| Flow agreed, screens next | Wireflow — low-detail frames + arrows at interface change-points |
| Unknown page content | Content inventory → priority-ordered blocks → overflow debate |
| Blank-canvas paralysis | Timer: 1–3 min rounds, ≥4 rounds; 8 ideas in 8 minutes |
| Layout won't fit content | Inside-out: design the smallest content unit first, screen box last |
| One make-or-break step | Wireframe the critical interaction first; ignore the entry path |
| Variations all look the same | "What if…?" prompt (voice-only, no imagery, personality) |
| Robustness unknown | Stress prompts: 10k rows, slow net, smallest device, German text, 2× fonts |
| Problem statement too narrow | Reframe as "How might we…?" |
| Want to stop after 2–3 sketches | One more, deliberately stranger — originality peaks late |
| Existing-product feature | Screenshot + wireframe collage for instant context |
| Solved-elsewhere problem | Borrow the pattern (cross-industry too), never the pixels |
| Stuck mid-session | Name the unanswered question; get the answer, then resume |
| Ready to move on | Keep ≥3 distinct directions; log excluded flows and dropped ideas |

## Anti-Patterns

| Mistake | Fix |
|---|---|
| Drawing the browser/device box first | Inside-out: smallest content unit first, container last |
| Deriving navigation straight from the sitemap | Sitemap ≠ user paths; design nav from flows + IA |
| Designing only the happy path | Walk the flow forward; branch errors/recovery; log exclusions explicitly |
| Boxes before content ("we'll fill it later") | Content inventory + priority order before any frame |
| First sketch becomes the design | ≥4–5 structurally distinct variations before converging |
| Polishing during ideation (spacing, type, color) | Fidelity cap: boxes, lines, scribbles only |
| Stopping at the first good idea | Power through: +1 stranger sketch; originality arrives late |
| Designing each screen independently | Wireflow the connections; they're costlier to change than screens |
| Judging ideas while generating them | Separate diverge from converge; critique only after the timer rounds |
| Copying a competitor's screen wholesale | Extract the pattern; recombine; look outside the industry |
| Sketching around an unanswered question | Stop, name it, get the answer from research/SME, resume |
| Demo-case-only sketches | Stress-case prompts; design for colossal and microscopic |
| Converging to a single winner immediately | Carry ≥3 directions into the next fidelity step |
| Treating rough output as embarrassing | Early frames are conversation tools; provoking discussion IS the quality bar |

## Companion Skills

| Situation | Co-fire |
|---|---|
| Mapping task paths before screens | userflow |
| Navigation structure emerging from the sitemap | flow-navigation |
| Choosing the overall layout shell after converging | flow-app-shell |
| Deep IA: labeling, hierarchy, findability | flow-navigation |
| Validating the idea is worth wireframing at all | dec-discovery-validation |
| Why a rough layout reads as grouped or scattered | dec-gestalt-principles |
| Turning the chosen sketch into a composed screen | layout-and-composition |
| Falling in love with the first direction | blind-consider-the-opposite |

*Distilled from* Wireframing for Everyone *(Michael Angeles, Leon Barnard, Billy Carlson — A Book Apart, 2023), extended with production practice.*
