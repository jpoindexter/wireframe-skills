---
name: wireframe-principles
description: "Use when a wireframe reads flat and everything looks equally important, when boxes or text edges are misaligned and the layout feels thrown together, when reviewers can't tell what's clickable or where to look first, when greeked/lorem text is hiding real content decisions, when color or typography starts sneaking into a wireframe, or when reviewing any wireframe's visual logic — hierarchy, alignment, clarity — before sharing it."
---

# Wireframe Design Principles — Hierarchy, Alignment, Clarity

## Overview
A wireframe's job is to make importance, order, and action obvious in grayscale boxes. Users judge a screen subconsciously before they read it; these three principles decide what that judgment lands on. If a viewer can't tell what matters, what's grouped, and what's clickable within five seconds, no amount of later visual design will fix it — hierarchy problems survive the handoff.

## When to Use
- Sketching or reviewing any wireframe: screen layout, form, landing page, dashboard, mobile view
- Deciding what should dominate a screen, what groups together, what to hide or cut
- Diagnosing "it feels cluttered / I don't know where to look" feedback on low-fi work
- **NOT for:** visual design — color palettes, type pairing, imagery, brand. That's hi-fi work; see Just Enough Design for the stop-line
- **NOT for:** flow-level questions (which screens exist, in what order) — this governs a single screen's visual logic

## Hierarchy
Hierarchy is the order the eye visits elements. You can't control what users click, but hierarchy suggests the path — and the subconscious usually follows it.

### The levers at wireframe fidelity
| Lever | How to use it in grayscale |
|---|---|
| Size | Largest element wins attention regardless of position. One dominant element per screen; headline 2–3× body size. |
| Weight / value | Bold + dark gray = primary; regular + mid-gray = secondary; light gray = tertiary. Value contrast replaces color at this fidelity. |
| Position | Top and left read first (F/Z scan paths in LTR locales); edges and below-the-fold read last. The #1 message lives in the first screenful. |
| White space | Isolation elevates: generous empty space around an element outranks it over crowded neighbors. Crowded elements compete and all lose. |
| Grouping | Proximity makes related items read as one unit (Gestalt); a group occupies one hierarchy slot instead of N competing ones. |

### Rules
- **Three levels max per screen:** primary (exactly one element), secondary (2–4), tertiary (everything else). Needing a fourth level means the screen holds too much — cut or split it.
- **Exactly one #1.** If two elements compete for primary (two big CTAs, two headlines), demote one. Two firsts = no first.
- **Combine levers; never rely on position alone.** A large, isolated, high-contrast element mid-screen beats small text at the top — the Spotify Play button pattern.
- **If everything is bold, nothing is.** Emphasis budget: ≤10% of a screen's text gets weight emphasis.

### Test it
- **Five-second test:** show the wireframe for 5 seconds, ask what they remember. If the answer isn't your primary element, re-lever.
- **Squint/blur test:** blur the image or squint. The shapes that survive must be the most important ones. Zero setup, run it solo on every screen before sharing.

## Alignment
Good alignment is invisible; misalignment is what people mean by "looks thrown together." Shared edges are rails for the scanning eye.

### Edge discipline
- **Vertical-line audit:** draw a vertical line at the left edge of every text block and at both edges of every other element. Every distinct line is a cost. Merge edges until the count is minimal — a clean screen needs 2–4 alignment lines, not 10.
- **Left-align any text block over three lines.** Centered long text is slower to read; reserve centering for short standalone units (heading + one-liner + button).
- **Top-align blocks across columns.** In multi-column rows, headings and body starts share a horizontal edge so the eye can sweep across sections.
- **Consistent margins on both sides.** Edge elements snap to the margin, never to eyeballed positions.
- **Equalize widths to merge edges.** Same-length inputs, same-width cards; consolidate short fields (city / zip) into one row so outer edges line up with the long fields.

### Grid use
- Pick a column grid before placing boxes (see grid-and-spacing) and snap everything to it — even rough tools reward a 12-column or simple halves/thirds discipline.
- Reuse the same grid across every screen of a flow. Consistency between screens is alignment at the product level: a control that shifts 20px between screens reads as a different control.

### Misalignment as a weapon
- Breaking alignment attracts the eye — distracting when accidental, powerful when deliberate. Budget: at most ONE intentionally out-of-alignment element per screen (an error message, a critical alert). Two breaks and both become noise.
- The weapon only works if everything else is aligned first. Ambient sloppiness spends the attention you were saving.

## Clarity
Clarity is how well what the design communicates matches what the user receives (Tidwell). The bar is Krug's: self-evident — or failing that, self-explanatory. Boost signal, cut noise: users should find what they need, see their options, and predict what an action will do.

### The three kinds of clarity
The source names three, and they fail independently — check each:

| Kind | What it means | Wireframe test |
|---|---|---|
| **Structure** | Recognizable, repeated patterns and templates appropriate to the content and context | Could a user who has never seen this screen predict where things are? |
| **Content** | Only what's essential to do the job; extraneous copy, images, icons, and controls removed | What can be deleted without losing the task? |
| **Action** | The most important or frequent action is the most prominent | Can you point to the one primary action in under a second? |

**One call to action per page** is the book's worked example of clarity of action —
one "Save," "Next," or "Buy." More than one primary action means the hierarchy hasn't
been decided yet. Secondary actions stay visibly secondary.

### Label realism — when text must be real
| Element | Real text required? |
|---|---|
| Buttons, CTAs, links | Always. "Submit" vs "Pay €49" is a design decision, not copy polish. |
| Navigation and tab labels | Always — nav labels ARE the information architecture. |
| Headings, section titles | Always — they carry the hierarchy you just built. |
| Form field labels + errors | Always — field naming decides comprehension and field count. |
| Empty states, confirmations | Always — these screens are mostly words. |
| Data in tables/cards | Realistic samples at real lengths ("Jane Chen · $1,240.50", not "xxxx") — truncation and wrap problems must surface now. |
| Body copy / long paragraphs | Greeking acceptable ONLY if the paragraph's content drives no decision on this screen. If someone must read it to act, write it. |

Greeked text hides decisions: lorem in a button, nav item, or label means the real design question was skipped — and reviewers can't catch what isn't there.

### Affordance in grayscale
- Clickable must look clickable without color: button = bordered/filled box with a centered verb label; link = underlined; input = empty rectangle with a visible label; disabled = lighter value.
- One visual treatment per behavior, applied consistently: if one filled box is a button, every filled box is a button.
- One primary action per screen, the most prominent element in its region. Secondary actions visibly quieter — outline vs fill, smaller, dimmer.

### The clarity ladder — group, hide, remove
1. **Group:** cluster related elements (address fields; a card's title + meta + action) with proximity and shared alignment.
2. **Hide:** optional or rarely-used content collapses behind an accordion, dropdown, or "show more" — progressive disclosure.
3. **Remove:** an element that lost every hierarchy contest and serves no task on this screen gets deleted. Showing only what's essential is the cheapest clarity available.

## Just Enough Design
The stop-line: a wireframe specifies structure and communication, not appearance.

**In scope at wireframe fidelity:** relative size · weight (bold/regular) · gray values · position · spacing and grouping · real labels · box shapes that signal affordance.

**Out of scope — stop if you catch yourself doing any of these:**
- Choosing colors (beyond grayscale values) or building a palette
- Picking typefaces or tuning precise px type sizes
- Adding imagery or illustration; icons stay placeholder boxes or labeled glyphs
- Shadows, gradients, corner-radius tuning, pixel-perfect spacing passes
- Branding, mood, "make it pop"

Two signals fidelity has crept: (1) review comments turn aesthetic instead of structural; (2) you're nudging pixels instead of moving boxes. Either way — strip back, or graduate the artifact to visual design deliberately.

Applied consistently across screens, these principles become a subconscious instruction manual for the product — and they survive development because they're structural, not cosmetic.

## Quick Reference

| Situation | Rule |
|---|---|
| Nothing stands out | Pick ONE primary element; stack 2+ levers on it (size + isolation + weight) |
| Too many things stand out | Three hierarchy levels max; demote until exactly one #1 remains |
| Need emphasis without color | Value contrast: dark + bold primary, mid-gray secondary, light tertiary |
| Long text block | Left-align if >3 lines; center only short standalone units |
| Ragged, busy layout | Vertical-line audit; merge left edges; snap to grid and margins |
| Short fields breaking alignment | Consolidate into one row; equalize remaining widths |
| One element must grab attention | Break alignment deliberately — max one break per screen |
| Button/nav/heading/label text | Real words, always — never lorem |
| Body paragraph text | Greek only if its content drives no decision on this screen |
| Can't tell what's clickable | One consistent treatment per behavior; verb labels on buttons; underline links |
| Screen overwhelming | Group → hide behind disclosure → remove, in that order |
| Checking before sharing | Squint test + five-second test on every screen |
| Color or typeface creeping in | Stop — past the wireframe stop-line; return to grayscale structure |

## Anti-Patterns

| Mistake | Fix |
|---|---|
| Everything the same size and weight (flat wireframe) | Three-level hierarchy: one primary, 2–4 secondary, rest tertiary |
| Two competing primary CTAs | Demote one to secondary treatment (outline, smaller, dimmer) |
| Key content buried below the fold with no cue | Move it into the first screenful, or add a visible continuation cue |
| Elements packed edge-to-edge | White space is a hierarchy lever — isolate what matters most |
| Every text block centered | Left-align anything >3 lines; center only short grouped units |
| Boxes eyeballed into place | Grid + margin snap; run the vertical-line audit |
| Same control in a different spot each screen | Lock shared regions and the grid across the whole flow |
| Sloppy alignment everywhere, hoping the error still pops | Align everything first; break alignment only for the one critical element |
| Lorem ipsum in buttons, nav, or field labels | Write the real words — those labels are design decisions |
| "xxxx" or too-short fake data in tables | Realistic samples at real lengths so truncation surfaces now |
| Everything visible "so nothing gets lost" | Group, hide the optional behind disclosure, delete the unjustifiable |
| Clickable elements with no grayscale affordance | Button = bordered box + verb; link = underline; input = labeled empty box |
| Polishing colors and fonts in a wireframe | Out of scope — structure only; park visuals for hi-fi |
| Skipping the squint test because it "looks fine" | Run it — the blur shows what actually dominates, not what should |

## Companion Skills

| Situation | Co-fire |
|---|---|
| Composing the whole screen — scan patterns, whitespace, visual flow | layout-and-composition |
| Setting up the column grid, spacing scale, margins | grid-and-spacing |
| Deciding what reads as grouped or related | dec-gestalt-principles |
| Judging self-evidence; cutting words | dec-krug-laws |
| Screen feels overwhelming; what to simplify vs preserve | dec-cognitive-load |
| Placement psychology — serial position, Von Restorff, scan paths | dec-ux-laws |
| Contrast values, target sizes, reading order | accessibility-and-inclusive-design |
| Writing the real labels, CTAs, and empty states | ux-writing-and-content |

*Distilled from* Wireframing for Everyone *(Michael Angeles, Leon Barnard, Billy Carlson — A Book Apart, 2023), extended with production practice.*
