# Contexts

A **context** is a self-contained branch of an HCP profile: its own file set, templates, manifest, and audience. Human Core is the root; contexts extend it for specific evaluation scenarios without touching it.

## Live Contexts

| Context | Audience | Files | Manifest |
|---------|----------|-------|----------|
| `pro` | External evaluators — recruiters, partners, investors | 5 | [pro/MANIFEST.md](pro/MANIFEST.md) |
| `speaker` | Event organizers and their agents | 3 | [speaker/MANIFEST.md](speaker/MANIFEST.md) |

Planned: entrepreneur, sport, research — added as first-class branches.

## What Makes a Context

1. **A manifest** — audience, file set, sensitivity defaults, rubric.
2. **Templates** — one markdown template per file, with structural comments.
3. **Unique file names** — file names are globally unique across all contexts (this is what lets a single storage layer and MCP server serve all of them).
4. **Its own META.md rules** — each context's META is auto-generated and tailored to its readers (e.g. HCP-pro's META carries a routing matrix for evaluator agents).

## Design Rule

Contexts split by **audience**, not by data type. Before adding a context, answer: *whose agent reads this, and what decision is it making?* If the answer matches an existing context, extend that one instead.
