# Quick Start: From CV to HCP in One Session

> You already have a resume. Let's use it as raw material.
> A CV is a compressed, lossy snapshot. HCP is the full picture.
> This prompt helps you decompress your experience into a living profile.

---

## Before You Start

Prepare your CV in any format — PDF, text, LinkedIn export, even a screenshot.
Don't worry about quality. A bad CV is still a starting point.

**Time needed:** 35-50 minutes for the first session. You'll walk away with draft versions of all core HCP files across both layers (mindset + portfolio).

---

## The Prompt

```
I'm converting my traditional CV into an HCP (Human Context Protocol) profile. My CV is attached / pasted below.

Here's what I need you to do:

## PHASE 1: EXTRACTION (you do this silently)

Read my CV and extract:
- Career timeline (roles, companies, durations)
- Domains I've worked in
- Stated skills and technologies
- Any achievements or metrics mentioned
- Gaps or transitions that might tell a story

## PHASE 2: INTERVIEW (we do this together)

My CV shows WHAT I did. You need to understand HOW I THINK.
Ask me questions one at a time. Go in this order:

### Round 1 — Identity (→ IDENTITY.md)
Pick the most interesting transition or role change from my CV and ask:
"I see you moved from [X] to [Y]. What was really behind that decision?"
Then follow up with:
"When you're at your best at work — what does that look like? What conditions make it happen?"

### Round 2 — Decisions (→ DECISIONS.md)
Pick the most senior or complex role from my CV and ask:
"Tell me about the hardest call you had to make in this role. The one where you had real options and real consequences."
Structure my answer into the SCROE format (Situation, Constraints, Reasoning, Outcome, Extraction).

### Round 3 — Capabilities (→ CAPABILITIES.md)
Based on my CV + answers so far, propose 3-5 capability patterns you see.
Frame them as action patterns, not keywords.
Ask me: "Do these ring true? What's missing? What did I overstate?"

### Round 4 — Risks (→ RISKS.md)
Ask: "Looking at your career — what's the biggest bet you've made? Something where you genuinely put something at stake."

### Round 5 — Collaboration (→ COLLABORATION.md)
Ask: "Think of a team where you did your best work. What was your role — not your title, but what you did for the group dynamic?"
Then: "Tell me about a real conflict at work. What happened and how did you handle it?"
Then: "What kind of boss brings out your best? What kind shuts you down?"

### Round 6 — Portfolio (→ PROJECTS.md, TRACK_RECORD.md, FAILURES.md)
Start with: "Let's talk about specific things you built or achieved. What's the project you're most proud of?"
For each project, extract: situation before you → what you specifically did → measurable result.
Push for numbers, dates, team sizes. Then ask: "What's another project that shows a DIFFERENT kind of value?"
Aim for 3-5 projects. Optionally ask: "Any professional mistake that taught you something important?"
Also extract career timeline from CV for TRACK_RECORD.md — verify with the user.

### Round 7 — Evolution
Ask: "Your CV starts at [earliest role]. That person and who you are today — what's the biggest shift in how you think?"

## PHASE 3: GENERATION

After the interview, generate draft versions of all HCP files in two layers:

**Mindset (mindset/):**
1. IDENTITY.md
2. CAPABILITIES.md (3-5 capabilities)
3. COLLABORATION.md (team role, hierarchy, conflict, influence, feedback, trust)
4. RISKS.md (at least one entry)

**Portfolio (portfolio/):**
5. PROJECTS.md (3-5 projects with situation/action/result)
6. TRACK_RECORD.md (career timeline, facts, domain experience)
7. FAILURES.md (optional — only if user shared failure stories)

**Bridge:**
8. DECISIONS.md (with at least one entry in SCROE format)

**Navigation:**
9. META.md (pre-filled with contact info and reading instructions)

Mark every section you're uncertain about with [❓ VERIFY] so I know what to revisit.

## IMPORTANT GUIDELINES

- My CV bullet points like "Increased revenue by 30%" are just starting points. Dig for the HOW and WHY behind every claim.
- Technology names from 3+ years ago are context, not capabilities. Focus on transferable patterns.
- If my CV has gaps — ask about them gently. Gaps are often where the most interesting decisions happened.
- Write in MY voice, not corporate voice. If I sound casual in conversation, the HCP should sound casual too.
- Be honest: if something in my CV sounds inflated, push back. An honest HCP is infinitely more valuable than a polished lie.
- For PORTFOLIO files: push for facts, numbers, dates. "Saved money" → "Reduced costs by $100K annually."
- For MINDSET files: push for patterns, not just stories. "I always..." → "What does that reveal about how you think?"
- COLLABORATION questions often reveal the most when you ask about specific conflicts and difficult bosses. Don't rush those.

[PASTE YOUR CV HERE OR ATTACH AS FILE]
```

---

## What Happens After

Your first HCP draft will be rough. That's perfect. Here's the path forward:

**Day 1** (today): Run this prompt → get draft HCP files in two layers (mindset + portfolio)
**Week 1**: Review drafts, fix what feels wrong, add one more decision to DECISIONS.md
**Week 2+**: Use the [Weekly Reflection](./weekly-reflection.md) prompt every Friday to keep it alive

The goal isn't perfection. The goal is to **start the flywheel**.
A mediocre HCP that gets updated weekly will beat a perfect one that was written once and forgotten.

---

## Tips

- **Bring your worst CV.** Seriously. The worse your CV, the more dramatic the upgrade to HCP. If your CV is already perfect, you probably don't need this.
- **Don't filter yourself.** The AI is extracting patterns, not judging you. Talk about failures, detours, weird career moves. That's where the gold is.
- **It's okay to stop early.** Even just IDENTITY.md + one project in PROJECTS.md = a working HCP. You can always add more later.
- **Portfolio can be filled separately.** If you run out of energy after the mindset interview, come back for portfolio later. Use the [extract-portfolio.md](./extract-portfolio.md) prompt.
- **Use your native language.** If you think more clearly in Russian, Spanish, or Mandarin — do the interview in that language. Translate the output later.
- **Estimated time:** 35-50 minutes for the full flow. 20-25 minutes if you skip portfolio and collaboration.
