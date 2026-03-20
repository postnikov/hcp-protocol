# 🧠 HCP — Human Context Protocol

**Your resume is dead. Your HCP is alive.**

HCP is an open protocol for representing yourself as a structured, machine-readable, continuously evolving professional identity. Instead of sending a static PDF, you give agents access to your **context** — how you think, what you've done, and how you decide.

> 🌐 **[humancontext.pro](https://humancontext.pro)** — Build your HCP profile through an AI-guided interview. Upload your CV, have a conversation, get your professional API.

---

## Why HCP?

The hiring world is shifting:

- **AI agents on both sides** — employers use AI to screen, candidates use AI to apply
- **Resumes are commoditized** — everyone's CV looks the same because everyone uses AI to write it
- **Experience expires** — your tech stack from 5 years ago is irrelevant, but your decision-making patterns aren't
- **People become free agents** — working for multiple companies, solving diverse problems with AI tools

HCP solves this by providing two things the market needs:

1. **A cognitive profile** (Mindset) — how you think, collaborate, and handle risk. *This doesn't exist anywhere today.*
2. **A structured portfolio** (Portfolio) — what you built, with facts and metrics. *This exists but in unstructured, non-machine-readable formats.*

Together they answer two questions no resume can: **"Who are you?"** and **"What have you done?"**

---

## The Two-Layer Model

```
┌─────────────────────────────────────────────────┐
│  MINDSET — Who you are                          │
│  Thinking patterns, capabilities, collaboration │
│  style, risk profile                            │
├─────────────────────────────────────────────────┤
│  DECISIONS — How you choose (bridge)            │
│  Facts + meaning, connects both layers          │
├─────────────────────────────────────────────────┤
│  PORTFOLIO — What you did                       │
│  Projects, career trajectory, lessons learned   │
├ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─┤
│  🎤 SPEAKER — How you speak (optional add-on)  │
│  Topics, delivery style, appearances            │
└─────────────────────────────────────────────────┘
```

**Mindset** is interpretive — patterns, self-reflection, nuance. It answers questions like "Will this person thrive in our culture?" and "How do they handle uncertainty?"

**Portfolio** is factual — dates, metrics, outcomes. It answers "Have they done this before?" and "What was the impact?"

**Decisions** bridge both worlds. A decision is both a fact ("relocated to build a solo practice in 2023") and a pattern ("prioritizes autonomy over security"). AI agents can follow a decision from portfolio into mindset to understand reasoning, or from mindset into portfolio to find evidence.

**Speaker** is an optional context add-on — topics, delivery format, audience interaction, and appearance history. It answers "What do they speak about?" and "How do they deliver?"

---

## Quick Start

### Option A: Use the Web App

Go to **[humancontext.pro](https://humancontext.pro)**, upload your CV, and let the AI interviewer build your HCP profile in 20-50 minutes.

### Option B: DIY with Templates

1. **Clone this repo** and copy the `templates/` folder into your own private repo
2. **Grab your CV** — any format, any quality. Even a bad one works
3. **Open any AI assistant** (Claude, ChatGPT, etc.) and paste the prompt from [`prompts/quick-start.md`](prompts/quick-start.md) along with your CV
4. **Have a 35-50 minute conversation** — the AI interviews you across both layers: mindset (how you think) and portfolio (what you've done)
5. **Get your draft HCP** — the AI generates all 9 core files (+ 3 optional speaker files if relevant)
6. **Commit and start the monthly rhythm**

> 💡 You don't need to fill everything at once. Even just `IDENTITY.md` + one project in `PROJECTS.md` = a working HCP. Portfolio and mindset can be filled independently, in any order.

> 🌍 **Bilingual support:** Templates and interview prompts are available in English and Russian. The web app detects language automatically.

---

## HCP File Structure

```
your-hcp/
├── mindset/                ← How you think (cognitive profile)
│   ├── IDENTITY.md
│   ├── CAPABILITIES.md
│   ├── COLLABORATION.md
│   └── RISKS.md
├── portfolio/              ← What you did (factual profile)
│   ├── PROJECTS.md
│   ├── TRACK_RECORD.md
│   └── FAILURES.md          (optional)
├── speaker/                ← How you speak (context add-on, optional)
│   ├── SPEAKER_TOPICS.md
│   ├── SPEAKER_STYLE.md
│   └── SPEAKER_APPEARANCES.md
├── DECISIONS.md            ← Bridge between mindset and portfolio
└── META.md                 ← Navigation for AI agents
```

### Mindset Layer

| File | Answers | Update Cadence |
|------|---------|----------------|
| `IDENTITY.md` | "How do you think?" | Quarterly |
| `CAPABILITIES.md` | "What can you do?" | Monthly |
| `COLLABORATION.md` | "How do you work with people?" | Quarterly |
| `RISKS.md` | "What will you bet on?" | When bets are made or resolved |

### Portfolio Layer

| File | Answers | Update Cadence |
|------|---------|----------------|
| `PROJECTS.md` | "What did you build?" | Monthly |
| `TRACK_RECORD.md` | "Where have you been?" | When roles change |
| `FAILURES.md` | "What did you learn the hard way?" | When mistakes happen (optional) |

### Bridge

| File | Answers | Update Cadence |
|------|---------|----------------|
| `DECISIONS.md` | "How do you choose?" | Monthly |

### Navigation

| File | Answers | Update Cadence |
|------|---------|----------------|
| `META.md` | "How should an AI read me?" | When structure changes |

### Speaker (Optional Add-on)

| File | Answers | Context |
|------|---------|---------|
| `SPEAKER_TOPICS.md` | "What do you speak about?" | Optional |
| `SPEAKER_STYLE.md` | "How do you deliver?" | Optional |
| `SPEAKER_APPEARANCES.md` | "Where have you spoken?" | Optional |

---

## Context System

HCP is built around an extensible **context system**. Each context is a coherent set of files that describe one facet of a person's professional identity.

### Professional Context (required)

The core 9 files — mindset, portfolio, decisions, and meta. This is the foundation every HCP profile starts with. It captures who you are as a professional: how you think, what you've built, and how you make decisions.

### Speaker Context (optional)

3 additional files for people who give talks, workshops, or keynotes. Captures speaking topics, delivery style, audience interaction preferences, and a log of past appearances. Activated separately — you can build your professional context first and add speaker later.

### Future Contexts

The context system is designed to grow. Potential future add-ons:

- **Researcher** — publications, methodologies, peer review style
- **Mentor** — teaching approach, mentee outcomes, knowledge transfer patterns
- **Creator** — content portfolio, audience, creative process

Each context follows the same pattern: a focused set of files, an optional interview flow, and independent activation via `enabled_contexts`.

### Context Definition

Each context is defined by a standard shape:

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique identifier (`"professional"`, `"speaker"`) |
| `label` | { en, ru } | Display name per language |
| `description` | { en, ru } | What this context covers |
| `files` | string[] | File names belonging to this context |
| `required` | boolean | Whether every profile must have it |
| `mcpNamespace` | string | Resource namespace prefix |

Profiles track active contexts via `enabled_contexts[]`. New contexts follow this same shape — add the definition, the files, and an optional interview flow.

---

## File Status Lifecycle

Every HCP file progresses through three statuses:

| Status | Meaning |
|--------|---------|
| **empty** | No content yet — the file exists as a template but hasn't been filled |
| **draft** | Has content but needs work — thin sections, missing detail, or `[? VERIFY]` markers |
| **complete** | All required sections filled with substantive content |

### `[? VERIFY]` Markers

When the AI interviewer isn't confident about a fact — a date, a metric, a company name — it flags it with a `[? VERIFY]` marker:

```markdown
Led the migration to microservices at [? VERIFY: Acme Corp, 2021], reducing deploy time by [? VERIFY: 40%].
```

These markers serve two purposes:
1. **Honesty** — the profile explicitly separates confirmed facts from uncertain ones
2. **Action items** — you can search for `[? VERIFY]` to find everything that needs checking

A file with unresolved `[? VERIFY]` markers stays in `draft` status until all markers are resolved.

---

## Interview Modes

The web app supports multiple interview modes depending on your starting point:

| Mode | When to use | Scope |
|------|-------------|-------|
| **Full** | Starting from scratch | All 8 (pro) or 4 (speaker) phases |
| **Improve all** | Reviewing existing profile | All phases, adapts to current content |
| **Improve specific** | Focus on selected files | Warmup + relevant phases + synthesis |
| **Boost file** | Quick single-file improvement | One targeted phase |
| **Resolve flags** | Fix `[? VERIFY]` markers | One phase focused on verification |

### Professional Phases (8)

warmup → identity → decisions → capabilities → collaboration → risks → portfolio → synthesis

### Speaker Phases (4)

speaker-topics → speaker-style → speaker-appearances → speaker-synthesis

Each phase targets specific HCP files and uses context files from earlier phases. The synthesis phase reviews all files, resolves remaining flags, and generates META.md.

---

## Philosophy

Traditional resume answers: **"What did you do?"**
HCP answers: **"Who are you, and what have you done?"**

A resume is a photograph. HCP is a living organism with two layers.

**Mindset** captures what compounds — cognitive patterns, collaboration style, risk appetite. A decision you made in 2019 might involve obsolete tech, but the way you evaluated trade-offs? That's timeless.

**Portfolio** captures what's verifiable — projects with metrics, career trajectory, lessons from failure. AI agents need evidence, not claims.

**Decisions** connect both. They're the seam where facts meet meaning.

---

## The Living System

HCP is not a document you write once. It's a living representation that grows with you.

| Cadence | What | How |
|---------|------|-----|
| **Monthly** | Reflection + pattern review | AI asks questions, updates DECISIONS, CAPABILITIES, and surfaces emerging themes |
| **Quarterly** | Identity distillation | Deep review of IDENTITY.md and COLLABORATION.md — has your core shifted? |
| **On change** | Event-driven updates | New role, major decision, bet made/resolved, project completed |

Use the [`prompts/reflection.md`](prompts/reflection.md) prompt to maintain the rhythm.

---

## Access Control & Views

HCP respects your privacy and NDAs. The protocol defines four visibility scopes:

- **Self View** — Full, unfiltered context visible only to you. A safe space for drafts, doubts, and raw reflections.
- **Public View** — Capabilities, public projects, and broad cognitive patterns. Accessible to any agent.
- **Recruiter View** — Decision-making patterns and risk appetite without sensitive details. Accessible via temporary tokens.
- **Deep Audit View** — Detailed decision logs, failures, and full context. Issued explicitly after mutual consent or NDA.

---

## HCP as MCP Server

Your published HCP profile runs as an [MCP](https://modelcontextprotocol.io/) (Model Context Protocol) server. AI agents connect and query your professional context directly — no scraping, no guessing, no stale data.

### Resources

Each HCP file is exposed as an MCP resource with layer-prefixed URIs:

```
hcp://{slug}/mindset/IDENTITY.md
hcp://{slug}/mindset/CAPABILITIES.md
hcp://{slug}/mindset/COLLABORATION.md
hcp://{slug}/mindset/RISKS.md
hcp://{slug}/portfolio/PROJECTS.md
hcp://{slug}/portfolio/TRACK_RECORD.md
hcp://{slug}/portfolio/FAILURES.md
hcp://{slug}/DECISIONS.md
hcp://{slug}/META.md
hcp://{slug}/speaker/TOPICS.md
hcp://{slug}/speaker/STYLE.md
hcp://{slug}/speaker/APPEARANCES.md
```

Agents can read individual files or use the tools below for higher-level queries. Resources are context-driven: only files from enabled contexts with substantive content are exposed.

### Tools

| Tool | Purpose |
|------|---------|
| `list_contexts` | List available contexts and metadata |
| `get_profile_overview` | Overview with configurable detail (brief/standard/detailed) |
| `get_context_summary` | Focused summary of one context (professional, speaker) |
| `ask_question` | Ask any question about the profile, optionally scoped to a context |
| `get_contacts` | Structured contact info (zero tokens, no LLM call) |
| `compare_contexts` | Compare 2-4 contexts (e.g. professional vs speaker persona) |
| `match_opportunity` | Evaluate fit — returns score, strengths, gaps, talking points |

### Connect from Claude Desktop

```json
{
  "mcpServers": {
    "hcp-postnikov": {
      "url": "https://humancontext.pro/api/profiles/postnikov/mcp/mcp"
    }
  }
}
```

Any MCP-compatible agent can connect the same way. The server speaks Streamable HTTP — no local setup required.

### Discovery Endpoint

`GET /api/profiles/{slug}/mcp` returns machine-readable metadata:

| Field | Content |
|-------|---------|
| `version` | MCP server version |
| `contexts[]` | id, label, file_count per enabled context |
| `tools[]` | All 7 tool names |
| `claude_desktop_config` | Copy-paste ready config |

### Structured Contacts

Contact information is stored as structured data alongside HCP files:

| Field | Type |
|-------|------|
| `email` | string |
| `telegram` | string |
| `linkedin` | URL |
| `twitter` | string |
| `website` | URL |
| `phone` | string |
| `preferred_method` | string |
| `custom` | key-value pairs |

The `get_contacts` tool returns this directly (zero tokens, no LLM call).

---

## HCP as A2A Agent

Each published profile is discoverable via the [A2A](https://a2a-protocol.org/) (Agent-to-Agent) v1.0 protocol.

### Agent Card

`GET /api/profiles/{slug}/agent.json` returns an Agent Card with:

- **`supportedInterfaces`** — MCP endpoint URL, binding (`json-rpc`), protocol version
- **`skills`** — all 7 tools with tags, example questions, input/output modes
- **`capabilities`** — streaming, push notifications, state history

Skills adapt to the profile: `compare_contexts` appears only when 2+ contexts are enabled.

### Domain-Level Discovery

`GET /.well-known/agent.json` lists all published profiles:

```json
{
  "protocol": "a2a",
  "protocolVersion": "1.0.0",
  "agents": [
    { "name": "HCP: Max Postnikov", "url": "https://humancontext.pro/api/profiles/postnikov/agent.json" }
  ]
}
```

Any A2A-compatible platform can discover all HCP profiles on the domain.

---

## Repository Structure

```
hcp-protocol/
├── README.md
├── CONTRIBUTING.md
├── LICENSE
├── templates/
│   ├── mindset/
│   │   ├── IDENTITY.md
│   │   ├── CAPABILITIES.md
│   │   ├── COLLABORATION.md
│   │   └── RISKS.md
│   ├── portfolio/
│   │   ├── PROJECTS.md
│   │   ├── TRACK_RECORD.md
│   │   └── FAILURES.md
│   ├── speaker/
│   │   ├── SPEAKER_TOPICS.md
│   │   ├── SPEAKER_STYLE.md
│   │   └── SPEAKER_APPEARANCES.md
│   ├── DECISIONS.md
│   └── META.md
├── prompts/
│   ├── quick-start.md
│   ├── extract-identity.md
│   ├── extract-decisions.md
│   ├── distill-capabilities.md
│   ├── extract-collaboration.md
│   ├── extract-risks.md
│   ├── extract-portfolio.md
│   └── reflection.md
└── examples/
    └── sample-profile/
```

---

## Contributing

This is an open protocol. We believe every professional deserves a living digital identity, not a dead PDF.

- **Suggest improvements** — open an [Issue](../../issues)
- **Share your HCP** — submit a PR to `examples/` (anonymize if needed)
- **Discuss the future** — join [Discussions](../../discussions)
- **Build tools** — create HCP viewers, exporters, MCP servers — the protocol is yours

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

MIT — use it, fork it, make it yours.

---

*Created by [Max Postnikov](https://www.linkedin.com/in/postnikov/) and [PRO Community](https://prommunity.org).*
