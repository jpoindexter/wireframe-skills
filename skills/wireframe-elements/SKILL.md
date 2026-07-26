---
name: wireframe-elements
description: "Use when choosing which UI component represents a need in a wireframe, tempted to invent a custom control where a standard one exists, unsure what belongs on a screen type (dashboard, list, detail, form, settings), deciding between list, table, tiles, or cards, picking horizontal vs vertical navigation, representing components at low fidelity, or consolidating repeated screens into page templates."
---

# Wireframe Elements — Components, Patterns, Templates

## Overview
Every box in a wireframe stands for something with a name. Users arrive trained by every other product they use (Jakob's Law), so the fastest wireframe is assembled from the standard vocabulary: **components** (the atoms — text, buttons, selectors) combine into **patterns** (navigation, content, input groups that solve one problem) which combine into **page templates** (screen archetypes reused across the product). Wireframing is choosing the right existing element, not drawing a new one.

## When to Use
- Turning rough idea-sketches into named interface objects
- Deciding what a shape in a wireframe *is* — button, link, dropdown, card
- Choosing the content pattern (list vs table vs tiles vs cards) or navigation orientation for a screen
- Blocking out a standard screen type: home, list/browse, detail, form, dashboard, settings
- **NOT for:** visual design — color, type, spacing polish (layout-and-composition)
- **NOT for:** deciding which screens the product needs at all (userflow)
- **NOT for:** deep per-pattern mechanics — validation timing, sort behavior (flow-forms, flow-tables)

## UI Anatomy
A screen is regions before it is components. Block these out first; each region hosts specific pattern types:

| Region | Hosts | Notes |
|---|---|---|
| Header / app bar | Logo, primary nav, search, account entry | Persistent across screens; every pixel here competes with content |
| Content area | The screen's one job: content + input patterns | The part the user came for — give it the most space |
| Sidebar | Secondary nav or filters | Left in LTR cultures; always visually below/inside primary nav's hierarchy |
| Footer | Mega-menu-style nav + legal, contact | Navigation of last resort — anything users must find also goes near the top |
| Overlay layer | Modals, prompts, cart previews, flyout menus | Interrupts everything below; earn its use |

## Component Vocabulary
The heart of the skill: need → standard component → how to draw it at low fidelity. Rule of thumb for text: **real words for anything the user acts on** (headings, buttons, nav items, option labels — these ARE design decisions); lorem/squiggle lines only for body copy whose content you don't control.

| Need | Standard component | Low-fi representation |
|---|---|---|
| Tell users where they are | Page title / heading | Largest text on screen, top; real words; exactly one per page |
| Explain or narrate | Body text | Horizontal squiggle/lorem lines broken by real subheads — never one solid block |
| Say what an input wants | Label | Real short noun above the field; never placed inside the field |
| Suggest valid input | Helper text | Gray example inside or below field ("e.g. jane@acme.com") |
| Explain on demand | Tooltip | Small ? circle; draw the bubble only if its content matters to the review |
| The one desired action | Primary button | Filled rectangle, real verb label ("Pay", "Reply" — never "Submit" or lorem); one per screen |
| Alternative action | Secondary button | Outlined (unfilled) rectangle beside/below the primary |
| Low-priority action | Text button | Plain text placed like a button, no box (e.g. "Undo" in a toast) |
| Navigate away | Link | Underlined text; link the key words only, never a whole sentence |
| Pick exactly one of 2–5 | Radio group | Vertical stack of ○ + real option labels; show the default filled ● |
| Pick many or none | Checkboxes | Vertical stack of ☐ + real option labels |
| Pick one from a long list | Dropdown | Rectangle with caret ▾, default value shown inside; use when options > 3–5 or space is tight |
| Discover by topic/category | Tags | Small pill outlines containing real category words |
| Enter short free text | Text input | Empty rectangle, label above, width matching expected answer length |
| Enter long free text | Text area | Taller rectangle, label above |
| Find anything | Search bar | Outlined field + magnifying-glass icon + the word "Search"; top of screen |
| Show a picture | Image placeholder | Box with an X corner-to-corner; annotate subject if it matters |
| Show a symbol | Icon placeholder | Small square or circle; label its meaning when it's load-bearing |

**Defaults:** every selector gets a sensible pre-selection when one exists — most common, or last-used. Base the default on the *user's* likely intent, never on what benefits you (pre-selecting expensive shipping is manipulation, not design).

**Buttons vs links:** buttons perform actions, links go places; the web has blurred this — pick a convention and hold it consistently across the product.

## Patterns
A pattern is a reusable group of components that fulfills one function — components alone do nothing (a text box needs its Send button). Three families cover most screens:

### Navigation patterns
Choose only after you know the rough breadth and depth of the sitemap:

- **Horizontal bar** — a handful of top-level items. Prominent and persistent, so every extra item taxes attention. Mobile: ≤4 items for tap targets; overflow into scroll or a "More" menu, reluctantly.
- **Vertical sidebar** — many or unknown items, or hierarchy. Scrolls naturally; shows nested levels as flyout overlays, accordions, or a fully expanded tree.
- **Secondary nav** — local (items within the selected section) and contextual (changes per section). Two shallow levels → a second horizontal row with both levels' selection visible; deeper/wider → dropdown or mega-menu, or a sidebar rendered *below* the primary bar so it can't be mistaken for it.
- **Breadcrumbs** — text links separated by arrows; current page is the last item, plain text, never linked; always repeat the page name as the heading below — breadcrumbs are too small to be the only "you are here."
- **Footer nav** — full-width mega-menu plus legal/contact. Last resort: users go there when they've failed everywhere else.

Navigation's job is signposts, not teleportation — like highway signs, list the main destinations, not every exit.

### Content patterns
Let the content dictate the pattern, not the reverse. All of these depend on items being similar in size — long prose forced into any of them breaks scanning.

| Pattern | Use when | Low-fi |
|---|---|---|
| List | Large/unknown count of brief, similar items (files, emails); optional per-row icons/actions | Stacked single-line rows, small leading icon squares |
| Table | Multi-dimensional data; per-row actions (edit, delete, export) | Grid with a bolded header row; show only columns users act on |
| Tiles | Imagery alone identifies each item (media browsing); scrolls in one dimension | Row of X-boxes, edge one cut off to signal scroll |
| Cards | Image + title + description + actions; wraps as a grid | Box: X-box top, one bold title line, 1–2 squiggle lines, optional button |

For tables: decide the most important columns first, push the rest to the detail page, and optimize around what the user *does* with the data, not what you could display.

### Input patterns
- **Forms** — the components combined: labels + inputs + selectors + one primary button. Ask only what you absolutely need; split long forms into logical steps; single column; labels above (or left, for long forms) — never inside the field; double the whitespace you think you need. Depth: flow-forms.
- **Modals / prompts** — interrupt to ask a question or force a decision. Plain language, conventional button placement, default = the *least destructive* action. Users resent them; use only when the task truly blocks continuing.
- **Search bar** — omnipresent, top of screen, boringly standard in appearance; helper text and autocomplete/predictive suggestions earn trust. Depth: flow-search.
- **Filters** — selection components that narrow results. Group options by type (Price, Brand, Rating); always show which filters are applied; always offer clear-all. Few filters → horizontal above results; many → vertical panel beside results.

## Page Templates
Templates are pattern collections representing screen archetypes. Even thousand-page sites run on fewer than ten. Wireframe templates **last** — let them emerge from repeated pattern combinations, then consolidate lookalike screens into one template. Contents below in priority order (top of screen first):

| Template | Contents, in priority order |
|---|---|
| Home / landing | Identity + value proposition → primary nav + search → featured entry-point content → footer |
| List / browse / category | Page title → filters + sort → one content pattern (list/table/tiles/cards) → pagination or load-more. Reuse this same template for search results |
| Detail | Breadcrumbs → title → primary media or data → primary action (buy, edit, share) → supporting detail sections → related items |
| Form / create-edit | Title naming the task → single-column fields grouped by topic → primary + secondary buttons at the end |
| Dashboard | Title + scope (date range) → key metrics as cards → charts/tables → recent-activity list. Most-glanced information first |
| Settings | Vertical section nav → one topic per pane → grouped controls, saved immediately or via one explicit button |

## Required Context

- **The content each region must hold** — component choice follows content, never the reverse.
- **Breadth and depth of the sitemap** — this decides the navigation pattern, and nothing else should.
- **Platform conventions** in play (web, iOS, Android, desktop).
- **The existing design system**, if one constrains the component vocabulary.
- **Which states exist** — empty, loading, error, partial, over-long — before choosing a control.

## Evaluation Procedure

1. For each region, state the content and the job before naming a component.
2. Choose navigation only after breadth and depth are known: broad → vertical, few items → horizontal.
3. Check every component against a known pattern before inventing one.
4. Render each element with its **longest realistic content**, and with none.
5. Confirm real text on buttons, nav items, headings, and labels; lorem only in body copy.
6. Check that what's clickable reads as clickable at grayscale fidelity.
7. Confirm every interactive element has its states accounted for, even if unstyled.

## Output Format

```
Region: <name> — content: <what it holds> — component: <choice> — because <job>
Navigation: <pattern> — from breadth <n> × depth <n>
Patterns reused: <named patterns>  ·  Invented: <any, with justification>
States covered: empty / loading / error / long-content
Real text where required: <yes | list of remaining lorem>
```

## Quick Reference

| Decision | Rule |
|---|---|
| Nav: many/unknown items or hierarchy | Vertical sidebar |
| Nav: a handful of flat items | Horizontal bar |
| Mobile nav bar | ≤4 items; overflow to "More"/hamburger |
| Two shallow nav levels | Second horizontal row, both selections highlighted |
| Deep or wide sub-nav | Dropdown/mega-menu, or sidebar below the primary bar |
| Brief similar items, unknown count | List |
| Multi-column data + row actions | Table |
| Image is the identifier | Tiles |
| Image + text + actions in a grid | Cards |
| One-of choice, ≤5 options | Radio group |
| Many-of choice | Checkboxes |
| One-of choice, long list or tight space | Dropdown with a default shown |
| Selector default | Most common or last-used, in the user's interest |
| Interrupting question | Modal; default button = least destructive |
| Few filter groups | Horizontal, above results |
| Many filter groups | Vertical panel beside results |
| Search placement | Top, omnipresent, standard field + icon |
| Button/nav/heading text in a wireframe | Real words, always |
| Body copy in a wireframe | Squiggles or lorem is fine |
| Template count for whole product | Fewest possible; consolidate lookalike screens |

## Anti-Patterns

| Mistake | Fix |
|---|---|
| Inventing a custom control where a standard exists | Use the convention — Jakob's Law means novel controls tax every user |
| Unlabeled buttons or input fields | Every actionable element gets real text, even at lowest fidelity |
| Lorem ipsum on buttons, nav items, headings | Real labels — the words are the design decision being tested |
| Label placed inside the input field | Label above the field; helper text inside is for examples only |
| Two primary buttons on one screen | One filled primary; demote the rest to secondary/text buttons |
| Linking a whole sentence | Link only the meaningful words |
| Dropdown for 2–3 options | Radio group — don't hide options that fit on screen |
| No default selection in a selector | Pre-select the most common or last-used choice |
| Default chosen for the business, not the user | Default to the user's likely intent (never the priciest option) |
| Picking a nav pattern before knowing the sitemap | Sketch breadth/depth first; the structure chooses the pattern |
| Secondary nav rendered above/level with primary | Place it below primary so hierarchy reads correctly |
| Breadcrumbs as the only location indicator | Repeat the page name as the heading; last crumb plain text |
| Key content reachable only via footer | Footer is last resort — duplicate the path near the top |
| Long prose forced into lists or cards | Similar-sized brief items only; prose gets a body-text page |
| Text overlaid on images without contrast | Add a scrim, or move the text off the image |
| Modal for anything non-blocking | Inline the message; modals only when continuing requires an answer |
| Destructive action as the modal default | Default = least destructive; make deletion the deliberate click |
| A unique layout for every screen | Consolidate into <10 templates; repetition is what users learn |
| Wireframing templates first | Patterns first; templates emerge from repeated combinations |

## Companion Skills

| Situation | Co-fire |
|---|---|
| Deciding which screens/flows the product needs | userflow |
| Component interaction states (hover, disabled, error) | components-and-states |
| Form fields, validation, wizard steps in depth | flow-forms |
| Table sorting, filtering, bulk actions in depth | flow-tables |
| Search behavior, results, zero-result handling | flow-search |
| Nav architecture, menu depth, IA restructuring | flow-navigation |
| Overall shell: sidebar+main, panes, responsive collapse | flow-app-shell |
| Screens before data arrives (empty, loading, error) | flow-empty-states |
| Arranging patterns on the page, hierarchy, whitespace | layout-and-composition |
| Icon placeholders becoming a real icon system | iconography-and-imagery |
| Replacing placeholder labels with real copy | ux-writing-and-content |
| Formalizing component→pattern→template into a system | design-tokens, components-and-states |

*Distilled from* Wireframing for Everyone *(Michael Angeles, Leon Barnard, Billy Carlson — A Book Apart, 2023), extended with production practice.*
