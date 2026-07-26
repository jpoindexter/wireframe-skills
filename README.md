# wireframe-skills

**The complete wireframing discipline — packaged as agent skills.**

Eight reference skills that teach coding agents (Claude Code, Codex, Gemini CLI, Copilot, Cursor, or anything that reads markdown) how to wireframe the way experienced designers do: structure before screens, divergent exploration before commitment, grayscale hierarchy before visual polish, annotation before handoff. Distilled from *Wireframing for Everyone* by Michael Angeles, Leon Barnard, and Billy Carlson (A Book Apart, 2023) and extended with production practice.

## Why

Agents asked to "design a screen" skip straight to polished UI: one layout, invented components, lorem ipsum over the decisions that matter, zero exploration. Wireframing exists precisely to prevent that failure mode — cheap structural iteration before anything looks finished enough to defend. These skills encode the full discipline so an agent explores, structures, critiques, and annotates instead of rendering the statistical average.

## The Skills

| Skill | Covers |
|---|---|
| [`wireframe`](skills/wireframe/SKILL.md) | **Dispatcher** — `/wireframe <what you're building>` runs the whole family + co-fires matching design skills |
| [`wireframe-fundamentals`](skills/wireframe-fundamentals/SKILL.md) | Why low fidelity wins, the fidelity ladder, wireframes across the process, tool choice |
| [`wireframe-ideation`](skills/wireframe-ideation/SKILL.md) | Structure before screens: flows, IA, content inventory; divergent idea generation |
| [`wireframe-elements`](skills/wireframe-elements/SKILL.md) | UI anatomy, the component vocabulary, patterns, page templates |
| [`wireframe-principles`](skills/wireframe-principles/SKILL.md) | Hierarchy, alignment, clarity at grayscale; the "just enough design" stop-line |
| [`wireframe-collaboration`](skills/wireframe-collaboration/SKILL.md) | Team wireframing sessions, roles and ownership, handling dominant voices |
| [`wireframe-feedback`](skills/wireframe-feedback/SKILL.md) | Asking for and giving feedback, running critique, acting on it |
| [`wireframe-handoff`](skills/wireframe-handoff/SKILL.md) | Presenting wireframes, annotation developers need, the handoff package |

## How it composes

The dispatcher is designed to co-fire with the rest of a design-skill library when present — [`ux-flow-skills`](https://github.com/jpoindexter/ux-flow-skills) for proven flows (`userflow`, `flow-*`), a visual family (`layout-and-composition`, `grid-and-spacing`, `components-and-states`), and a principles canon (`dec-*`). Without them it still runs standalone: the seven content skills carry the full wireframing method on their own.

## Format

Each skill follows the [Agent Skills specification](https://agentskills.io/specification): a directory with a `SKILL.md` containing YAML frontmatter (`name`, `description`) and a dense markdown body — When to Use, concrete rules, Quick Reference, Anti-Patterns, Companion Skills.

```
skills/
  wireframe/
    SKILL.md
  wireframe-fundamentals/
    SKILL.md
  ...
```

Plain markdown with standard frontmatter: skill-aware harnesses load them automatically; anything else can be pointed at a `SKILL.md` as context.

## Install

### Any agent (skills CLI)

```bash
npx skills add jpoindexter/wireframe-skills
```

### Claude Code (global, all sessions)

```bash
git clone https://github.com/jpoindexter/wireframe-skills.git
cd wireframe-skills
for d in skills/*/; do ln -sfn "$(pwd)/$d" ~/.claude/skills/$(basename "$d"); done
```

Then `/wireframe <what you're building>` in any session.

### Manual (any harness)

Point your agent at `skills/wireframe/SKILL.md` — it lists the rest of the family and when each applies.

## Traceability

[`skills/wireframe/references/source-map.md`](skills/wireframe/references/source-map.md) maps the book's chapters onto the skills, lists all 39 sources the book cites with the skill that carries each, and records where these skills deliberately diverge from the book's vocabulary. Claims should be attributable or declared as extension.

## Credit

Distilled from *Wireframing for Everyone* — Michael Angeles, Leon Barnard, Billy Carlson (A Book Apart, 2023). It's excellent, and these skills are an operational condensation for agents, not a substitute for the authors' full treatment.

**Where to get it now.** A Book Apart ceased operations in 2024 and no longer sells or distributes books; rights reverted to the individual authors, and many A Book Apart titles have since found new homes. *Wireframing for Everyone* is hosted by the authors at [balsamiq.com/learn/wireframing-book](https://balsamiq.com/learn/wireframing-book/) — Barnard and Angeles work at Balsamiq, where the book originated. Balsamiq's [Wireframing Academy](https://balsamiq.com/learn/) is a free, public companion resource by the same authors.

## License

MIT
