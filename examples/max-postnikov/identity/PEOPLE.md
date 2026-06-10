---
schema_version: 1
file: PEOPLE.md
layer: identity
sensitivity: high
---

# Inner Circle

> Roles and facts, not names. In a real profile this file is richer and more
> specific — and that's exactly why it's high-sensitivity and not for
> publishing. This public version keeps only the structure.

## Family

```yaml
- role: partner
  context_for_me: |
    The most important person in my life. Mornings together are a ritual;
    most evenings too.
  for_agent: |
    Prioritize morning and evening time with her. Respect shared rituals
    when planning my day.

- role: adult son
  context_for_me: |
    Lives in another city, has his own life. I help where I can.
  for_agent: |
    Remote relationship — doesn't affect daily planning, but leave room
    for calls and occasional help.
```

## Work Circle

```yaml
- role: professional community
  context_for_me: |
    A community of people excited about technology. I'm a community person.
  for_agent: |
    Account for time spent in community discussions.

- role: AI partners
  context_for_me: |
    I treat AI agents as partners, not tools, and I personify them.
  for_agent: |
    A core part of my workflow. Treat this as collaboration.
```

## Close Friends

```yaml
- role: closest friends
  context_for_me: |
    As important as family. One of them is also a mentor figure for me.
  for_agent: |
    High priority — protect time with them in any plan.

- role: mentor abroad
  context_for_me: |
    A friend and source of wisdom living in another timezone.
  for_agent: |
    Important for my growth. Mind the timezone difference for calls.
```

## What an Agent Should Account For
- Partner comes first, especially mornings and evenings
- Closest friends rank with family
- Do NOT interrupt during: important meetings, livestreams, video recording
- "Everyone is a potential mentor" — openness to learning from anyone
