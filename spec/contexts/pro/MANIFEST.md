# HCP-pro — Context Manifest

**Audience:** external evaluators and their AI agents (OUTSIDE) — recruiters, partners, investors, clients.
**Context ID:** `hcp-pro`
**Files:** 5.

HCP-pro is the **evidence layer**. Where Human Core is candid and sensitive, HCP-pro is polished and public-friendly: structured facts an external agent can use to assess fit, match opportunities, and answer questions about your work.

## File Set

| File | Purpose |
|------|---------|
| `CAPABILITIES.md` | What you can do — action patterns with autonomy levels |
| `COLLABORATION.md` | How you work with teams — role, conflict style, trust |
| `PROJECTS.md` | What you built — situation, action, measurable result |
| `TRACK_RECORD.md` | Career timeline, domains, depth of experience |
| `META.md` | Auto-generated routing table for evaluator agents |

## Rubric (deliberately simple)

```
empty → draft → idealno
```

HCP-pro is a **working artifact, not an exam**. One bar: "good enough for a working profile". The 5-level depth rubric belongs to Human Core; here it would just add friction.

## META.md Routing Matrix

Generated META includes a use-case routing table so evaluator agents read the right files in the right order:

| Use case | Read first | Then | Optional |
|----------|-----------|------|----------|
| Hiring for a role | `TRACK_RECORD.md` → `CAPABILITIES.md` | `PROJECTS.md` | `COLLABORATION.md` |
| Culture fit assessment | `COLLABORATION.md` → `CAPABILITIES.md` | `PROJECTS.md` | — |
| Partnership / advisory | `PROJECTS.md` → `TRACK_RECORD.md` | `CAPABILITIES.md` | `COLLABORATION.md` |

META also points agents that need the personality layer (thinking style, risk profile) to the person's Human Core — a separate source of truth with its own access rules.

## Retired v2 Files

`IDENTITY.md`, `RISKS.md`, `DECISIONS.md`, `FAILURES.md` are no longer part of the active spec. Their meaning moved into Human Core (`WHO`, `PATTERNS`, `BOUNDARIES`), where candor doesn't have to compete with polish. Existing profiles keep that data exportable under `legacy/`.

## Templates

See [`templates/`](templates/).
