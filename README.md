# 🧠 HCP — Human Context Protocol

**Your structured self, for every AI agent you work with.**

HCP is an open protocol for representing yourself as structured, machine-readable, continuously evolving context. Not a resume. Not a bio. A set of markdown files that tell AI agents — yours and everyone else's — who you are, how you speak, what you're working on, and how you decide.

> 🌐 **[humancontext.pro](https://humancontext.pro)** — Build your HCP through a guided AI interview. Every published profile is a live MCP server + A2A agent card.

---

## The Core Question: Whose Agent Is Reading?

Every interaction you have is increasingly mediated by AI agents. HCP organizes your context by **audience**, not by data type:

```
INSIDE — your own AI agents (Claude, ChatGPT, Cursor, ...)
  Your agents should know you deeply.
  → Human Core: 10 files, mixed sensitivity, built for daily AI tooling

OUTSIDE — third-party agents evaluating you (recruiters, partners, investors)
  External agents should assess your professional value clearly.
  → HCP-pro: 5 files, public-friendly, built as an evidence layer

SIDE — specific scenarios (speaking, future: entrepreneurship, sport, ...)
  Domain data sets for specific evaluators.
  → Speaker: 3 files; more contexts added as first-class branches
```

The old resume question — *"What have you done?"* — still matters, but it's one context among several. The question HCP answers first is: **"What does an AI agent need to know to work with you well?"**

## Why This Exists

- **You repeat yourself to every AI tool.** Claude doesn't know what ChatGPT knows. Every new chat starts from zero. Human Core is the context you write once and connect everywhere.
- **AI agents are on both sides of every evaluation.** Employers screen with AI, candidates apply with AI. Unstructured PDFs are noise; structured context is signal.
- **Instructions belong next to data.** Every YAML block in Human Core carries a `for_agent` field — a direct instruction to the consuming agent. No guessing.

## File Architecture (18 files total)

```
human-core/                    ← INSIDE: for your own AI agents
├── core/
│   ├── WHO.md                 # role, drive, values
│   ├── VOICE.md               # how you speak, AI irritants
│   ├── NOW.md                 # current focus
│   └── GOALS.md               # where you're heading
├── identity/
│   ├── INFLUENCES.md          # books, people, ideas that shaped you
│   ├── INTERESTS.md           # what pulls your attention
│   └── PEOPLE.md              # who matters in your world
├── deep/
│   ├── PATTERNS.md            # decision-making and behavior patterns
│   └── BOUNDARIES.md          # hard limits, what agents must not do
└── META.md                    # auto-generated navigation for agents

hcp-pro/                       ← OUTSIDE: for external evaluators
├── CAPABILITIES.md
├── COLLABORATION.md
├── PROJECTS.md
├── TRACK_RECORD.md
└── META.md                    # includes a routing matrix for evaluator agents

speaker/                       ← SIDE: optional extension
├── SPEAKER_TOPICS.md
├── SPEAKER_STYLE.md
└── SPEAKER_APPEARANCES.md
```

Most people start with just `human-core/core/` — four files — and grow from there.

## Design Principles

1. **Markdown + YAML, human-readable.** You can read, edit, and version your entire identity with a text editor and git.
2. **`for_agent` instructions co-located with data.** Each YAML block tells the consuming agent how to use it — anti-"AI must guess".
3. **Sensitivity levels per file.** `low` / `medium` / `high`. External agents get low+medium by default; `PEOPLE`, `PATTERNS`, `BOUNDARIES` require explicit consent.
4. **Progression, not perfection.** Human Core files move `empty → draft → normalno → ponyatno → idealno` against an objective rubric. HCP-pro is deliberately simpler (`empty → draft → idealno`) — it's a working artifact, not an exam.
5. **META is generated, never hand-written.** Navigation files are rebuilt on every save, listing only files that actually have content.
6. **Contexts are extensible.** Speaker proves the pattern: a new context is a self-contained branch with its own manifest and templates, no changes to the core.

## Spec Layout (this repo)

```
spec/
├── human-core/
│   ├── MANIFEST.md            # file set, layers, sensitivity, rubric
│   └── templates/             # 10 file templates
└── contexts/
    ├── README.md              # what a context is, how to add one
    ├── pro/
    │   ├── MANIFEST.md
    │   └── templates/         # 5 file templates
    └── speaker/
        ├── MANIFEST.md
        └── templates/         # 3 file templates
prompts/
└── bootstrap-human-core.md    # build your Human Core with any LLM
examples/
└── max-postnikov/             # the author's real Human Core, flattened for publication
```

Templates are **exported directly from the production code** of [humancontext.pro](https://humancontext.pro) — the spec and the live product cannot drift.

## Two Ways to Use HCP

**Hosted — [humancontext.pro](https://humancontext.pro)**
A guided AI interview (per-file, with the persona "Echo") builds your files. Every published profile gets:
- a public page at `humancontext.pro/p/{slug}`
- an **MCP server** (`/api/profiles/{slug}/mcp/mcp`) with 8 tools — `ask_question`, `match_opportunity`, `get_contacts`, `suggest_update`, and more
- an **A2A agent card** for agent-to-agent discovery

Connect your own profile to Claude Desktop:

```json
{ "mcpServers": { "hcp-me": { "url": "https://humancontext.pro/api/profiles/{slug}/mcp/mcp" } } }
```

**Self-hosted — plain markdown**
Copy `spec/human-core/templates/`, fill them in with any LLM using `prompts/bootstrap-human-core.md`, keep them in a git repo or your notes vault. Paste or mount them as context wherever you work with AI.

## Status

- Protocol: **v3** (Inside/Outside/Side architecture) — live in production
- Earlier versions: v1 (single profile), v2 (mindset/portfolio two-layer). v2 file names (`IDENTITY`, `RISKS`, `DECISIONS`, `FAILURES`) are retired; their meaning moved into Human Core (`WHO`, `PATTERNS`, `BOUNDARIES`).

## License

[MIT](LICENSE)
