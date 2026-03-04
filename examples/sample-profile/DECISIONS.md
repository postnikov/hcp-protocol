# DECISIONS.md

## Decision Log

### Rewriting the Payment System Mid-Migration

**Date:** 2024-03
**Context:** Staff Engineer at a Series C fintech (200 people). Leading a team of 8 engineers.
**Domain:** technical + strategy
**Uncertainty level:** high

**Situation:**
We were 6 weeks into migrating our payment processing from a legacy monolith to microservices. I discovered that the new architecture had a race condition that would cause duplicate charges under high load. The team had already committed to the timeline publicly. The CEO had mentioned the migration date in an investor call.

**Constraints:**
- Public commitment to a launch date (3 weeks away)
- Team morale invested in the current approach (6 weeks of work)
- Race condition was architectural — not a quick fix
- Couldn't just "be more careful" — the flaw was in the design

**Options considered:**

| Option | Pros | Cons |
|--------|------|------|
| A: Ship with monitoring, fix later | Meets deadline, keeps momentum | Risk of real duplicate charges, erodes trust |
| B: Delay launch by 2 months, redesign | Clean solution, no risk | Breaks promise to investors, team demoralized |
| C (chosen): Hybrid — keep old system as safety net, run new system in shadow mode | Meets deadline *technically*, buys time to fix properly | More complex operationally, requires maintaining two systems temporarily |

**Why I chose this:**
I optimized for *reversibility*. Option A created irreversible damage (customer trust). Option B created irreversible organizational damage (credibility with investors). Option C was operationally ugly but fully reversible — we could fall back to the old system at any moment. Ugly and safe beats clean and risky.

**Outcome:**
Shadow mode caught 3 more bugs we hadn't found. We fully switched over 5 weeks after the original deadline. The CEO was initially frustrated about the "soft launch" framing, but the CFO backed me when I showed the duplicate charge risk. The team learned to build shadow mode into every major migration since.

**What I'd do differently:**
I should have insisted on shadow mode from the start, before we committed to a date. The pattern was obvious in retrospect. Now I advocate for "dark launch by default" on any system touching money.

**Pattern this reveals:**
When facing pressure to ship, I look for the option that preserves optionality. I'd rather be operationally messy than take irreversible risks. I also tend to find solutions that reframe the problem — "launch" doesn't have to mean "cut over."

---

### Hiring a Junior Over a Senior

**Date:** 2024-08
**Context:** Needed to fill a critical backend role. Had two finalists.
**Domain:** people
**Uncertainty level:** medium

**Situation:**
My team needed a backend engineer. The senior candidate had 10 years of experience and could be productive immediately. The junior candidate had 2 years but asked extraordinary questions during the interview — she challenged our architecture in ways that made me uncomfortable (in a good way).

**Constraints:**
- Sprint commitments required someone productive within 2 weeks
- Team was already stretched thin
- Budget allowed only one hire

**Options considered:**

| Option | Pros | Cons |
|--------|------|------|
| A: Hire the senior | Immediate productivity, low risk | Wouldn't challenge our thinking |
| B (chosen): Hire the junior | Fresh perspective, high ceiling | 2-3 month ramp-up, team absorbs mentoring cost |

**Why I chose this:**
We didn't need another pair of hands. We needed a different kind of brain. The team had been building the same way for 2 years, and I could feel us calcifying. The junior's questions during the interview pointed at real weaknesses. I bet that the disruption to our thinking was worth more than 3 months of velocity.

**Outcome:**
First month was hard. Velocity dropped 15%. By month 3, she had proposed a caching strategy that reduced our P95 latency by 40%. By month 6, she was the most valuable member of the team — not because of raw output, but because she made everyone else's output better. The senior candidate took a role at another company and is doing well.

**What I'd do differently:**
I should have been more transparent with the team about WHY I made this choice. Some people felt the velocity hit without understanding the strategic reasoning. Communication, not the decision itself, was the gap.

**Pattern this reveals:**
I value cognitive diversity over immediate productivity. I'm willing to trade short-term efficiency for long-term capability — but I sometimes forget to bring people along on the reasoning.

---

## Decision Patterns Summary

**I tend to:**
- Optimize for reversibility and optionality over speed
- Value diverse thinking over uniform execution
- Find reframes that create new options instead of choosing between bad ones

**I'm strongest when the decision involves:**
- Technical risk with organizational implications — the intersection is where I'm most differentiated

**I'm weakest when the decision involves:**
- Purely interpersonal conflict with no clear "right answer" — I can overcomplicate things that require simple directness

---

*Last updated: 2025-11-15*
