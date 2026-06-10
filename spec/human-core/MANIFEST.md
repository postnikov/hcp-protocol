# Human Core — Context Manifest

**Audience:** your own AI agents (INSIDE).
**Context ID:** `human-core`
**Files:** 10, across four layers.

Human Core is the context you build for the AI tools that serve *you* — Claude Desktop, ChatGPT, Cursor, custom agents. It is allowed to contain candid, sensitive, unpolished material, because its reader works for you.

## File Set

| Layer | File | Purpose | Sensitivity |
|-------|------|---------|-------------|
| core | `WHO.md` | Role, core drive, values (with `for_agent` instructions) | medium |
| core | `VOICE.md` | Language, tone, speech rules, AI irritants | medium |
| core | `NOW.md` | Current focus, active projects, this season | medium |
| core | `GOALS.md` | Where you're heading, success criteria | medium |
| identity | `INFLUENCES.md` | Books, people, ideas that shaped your thinking | medium |
| identity | `INTERESTS.md` | What pulls your attention | low |
| identity | `PEOPLE.md` | Who matters in your world and how to handle them | **high** |
| deep | `PATTERNS.md` | Decision-making and behavior patterns | **high** |
| deep | `BOUNDARIES.md` | Hard limits — what agents must not do | **high** |
| meta | `META.md` | Auto-generated navigation (do not hand-edit) | low |

Start with the four `core/` files. The rest are progressive depth.

## The `for_agent` Pattern

Human Core's signature design: every YAML block carries explicit instructions for the consuming agent, co-located with the data it annotates.

```yaml
- label: short value name
  in_action: |
    What this looks like in practice. Concrete patterns. (≥30 chars)
  trigger: |
    What activates it.
  anti_trigger: |
    What dampens it. What you avoid.
  for_agent: |
    Direct instruction for the AI agent working with you.
```

An agent reading the file never has to guess how to apply what it learned.

## Sensitivity & Access

- `low` + `medium` files: safe defaults for any agent you connect.
- `high` files (`PEOPLE`, `PATTERNS`, `BOUNDARIES`): contain material about third parties and your inner mechanics. Share only with agents you fully control; external agents require explicit consent per file.

## Progression Rubric (5 levels)

```
empty → draft → normalno → ponyatno → idealno
```

Status is **auto-assessed from content** on every save — sections filled, YAML blocks present, concrete examples (no self-marking). The reference implementation lives in `lib/human-core/rubric.ts` of the production app. Human Core is a self-reflection tool: progression should feel like deepening, not box-ticking.

## META.md Rules

`META.md` is regenerated on every save and must never be hand-edited. It contains:

- owner block (display name, profile URL, last review date)
- file status table
- reading order **filtered to files that actually have content** — an agent following META never hits an empty file
- sensitivity table

## Templates

See [`templates/`](templates/) — exported verbatim from production code, organized by layer (`core/`, `identity/`, `deep/`).
