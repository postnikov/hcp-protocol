# 🧠 HCP — Human Context Protocol

**Your resume is dead. Your HCP server is alive.**

HCP is an open protocol for representing yourself as a structured, machine-readable, continuously evolving professional identity. Instead of sending a static PDF, you give agents access to your **context** — how you think, decide, and create value.

> 🌐 **[humancontext.pro](https://humancontext.pro)** — Build your HCP profile through an AI-guided interview. Upload your CV, have a conversation, get your professional API.

---

## Why HCP?

The hiring world is shifting:

- **AI agents on both sides** — employers use AI to screen, candidates use AI to apply
- **Resumes are commoditized** — everyone's CV looks the same because everyone uses AI to write it
- **Experience expires** — your tech stack from 5 years ago is irrelevant, but your decision-making patterns aren't
- **People become free agents** — working for multiple companies, solving diverse problems with AI tools

HCP solves this by separating **what you did** (which expires) from **how you think** (which compounds).

## The Two-Layer Model

```
┌─────────────────────────────────────┐
│  HUMAN ↔ HUMAN                      │
│  Meaning, emotions, creative spark  │
├─────────────────────────────────────┤
│  AGENT ↔ AGENT                      │
│  Protocol, matching, verification   │
│  ← HCP lives here                   │
└─────────────────────────────────────┘
```

HCP handles the protocol layer so humans can focus on what matters: exchanging meaning and building together.

---

## Quick Start

### Option A: Use the Web App

Go to **[humancontext.pro](https://humancontext.pro)**, upload your CV, and let the AI interviewer build your HCP profile in 30 minutes.

### Option B: DIY with Templates

1. **Clone this repo** and copy the `templates/` folder into your own private repo
2. **Grab your CV** — any format, any quality. Even a bad one works
3. **Open any AI assistant** (Claude, ChatGPT, etc.) and paste the prompt from [`prompts/quick-start.md`](prompts/quick-start.md) along with your CV
4. **Have a 30-minute conversation** — the AI interviews you, digging beneath your CV bullet points to understand how you actually think and decide
5. **Get your draft HCP** — the AI generates all core files pre-filled with your context
6. **Commit and start the weekly rhythm**

> 💡 You don't need to fill everything at once. Even just `IDENTITY.md` + one entry in `DECISIONS.md` = a working HCP.

If you don't have a CV or prefer to start from scratch, use the individual prompts in [`prompts/`](prompts/) — each one guides you through filling a specific template via conversation.

---

## HCP File Structure

```
your-hcp/
├── IDENTITY.md       — Your cognitive OS: how you think, what drives you
├── DECISIONS.md      — Portfolio of decisions with context and outcomes
├── CAPABILITIES.md   — Graph of what you can do (not a skill list)
├── RISKS.md          — Bets you've taken and what they reveal about you
├── PROJECTS/         — Deep dives into specific work
│   └── *.md
└── META.md           — Instructions for AI agents reading your HCP
```

| File | Answers | Update Cadence |
|------|---------|----------------|
| `IDENTITY.md` | "How do you think?" | Quarterly |
| `DECISIONS.md` | "How do you choose?" | Weekly |
| `CAPABILITIES.md` | "What can you do?" | Monthly |
| `RISKS.md` | "What will you bet on?" | When bets are made or resolved |
| `PROJECTS/*.md` | "Show me the work" | Per project |
| `META.md` | "How should an AI read me?" | When structure changes |

---

## Philosophy

Traditional resume answers: **"What did you do?"**
HCP answers: **"How do you think and act?"**

A resume is a photograph. HCP is a living organism.

Technology skills expire, but **cognitive patterns compound**. A decision you made in 2019 might involve obsolete tech — but the way you evaluated trade-offs, managed uncertainty, and took responsibility? That's timeless.

---

## The Living System

HCP is not a document you write once. It's a living representation that grows with you.

| Cadence | What | How |
|---------|------|-----|
| **Weekly** | Quick reflection | AI asks you 3-5 questions, updates DECISIONS and CAPABILITIES |
| **Monthly** | Pattern review | AI analyzes the month, surfaces emerging themes |
| **Quarterly** | Identity distillation | Deep review of IDENTITY.md — has your core shifted? |

Use the [`prompts/weekly-reflection.md`](prompts/weekly-reflection.md) prompt to maintain the rhythm.

---

## Access Control & Views

HCP respects your privacy and NDAs. Not every agent should see your entire context. The protocol defines four visibility scopes:

- **Self View** — Full, unfiltered context visible only to you. A safe space for drafts, doubts, and raw reflections. This layer prevents self-censorship.
- **Public View** — Capabilities, public projects, and broad cognitive patterns. Accessible to any agent.
- **Recruiter View** — Decision-making patterns and risk appetite without sensitive project details. Accessible via temporary tokens.
- **Deep Audit View** — Detailed decision logs, failures, and full context. Issued explicitly after mutual consent or NDA.

---

## Vision: HCP as MCP Server

The ultimate form: your HCP runs as an [MCP](https://modelcontextprotocol.io/) server. An employer's AI agent connects to your server, queries your context, and gets exactly the projection of you that's relevant to their needs.

```
Employer Agent  →  connects to  →  Your HCP Server
                                    ├── "Show me decisions under uncertainty"
                                    ├── "What's their autonomy level?"
                                    └── "Risk tolerance profile?"
```

You're one person, but you look different to different queries — because different facets of your experience light up for different problems.

---

## Repository Structure

```
hcp-protocol/
├── README.md                        ← You are here
├── templates/                       ← Empty HCP templates to copy
│   ├── IDENTITY.md
│   ├── DECISIONS.md
│   ├── CAPABILITIES.md
│   ├── RISKS.md
│   ├── PROJECT.md
│   └── META.md
├── prompts/                         ← AI prompts for filling templates
│   ├── quick-start.md               ← Start here: CV → HCP in one session
│   ├── extract-identity.md
│   ├── extract-decisions.md
│   ├── distill-capabilities.md
│   ├── extract-risks.md
│   └── weekly-reflection.md
└── examples/                        ← Filled sample profiles
    └── sample-profile/
        ├── IDENTITY.md
        └── DECISIONS.md
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
