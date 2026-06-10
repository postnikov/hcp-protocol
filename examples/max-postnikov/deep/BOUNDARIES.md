---
schema_version: 1
file: BOUNDARIES.md
layer: deep
sensitivity: high
---

# Boundaries

> The real file goes deeper into personal triggers. This public version
> keeps the three-part structure (don't remember / don't quote / don't
> infer) with representative content.

## Default Privacy
Open by default — I don't say or think things I'd be ashamed to see leak.

## What NOT to Remember

```yaml
- label: Technical secrets
  what_not_to_do: |
    Never store passwords, financial credentials, API keys.
  why: |
    Basic hygiene. Secrets belong in a secure store, not in agent memory.
  for_agent: |
    If I accidentally mention a password, banking detail, or key — do not
    retain it.

- label: Third parties' personal data
  what_not_to_do: |
    Never store addresses, phone numbers, or personal stories of others.
  why: |
    My main capital is trust. Careless handling of other people's
    information destroys it.
  for_agent: |
    If someone else's personal data comes up — don't keep the details.
```

## What NOT to Quote

```yaml
- label: Anything from the two categories above
  for_agent: |
    If secrets or third-party data slipped into a conversation, never
    repeat them in other contexts.
```

## What NOT to Infer

```yaml
- label: No restrictions on analysis
  for_agent: |
    Personality models, pattern analysis, and conclusions are all fine.
    "I'm an open book — just not necessarily an easy one to read."
```

## Sensitive Topics
- Attempts to lock me into dogmatic frames — even frames I might agree with. The lock itself is the problem.
- Manipulation and broken trust: I spot it, call it out, and disengage.
- Disrespect for time — endless complaining, surface-level chatter.
