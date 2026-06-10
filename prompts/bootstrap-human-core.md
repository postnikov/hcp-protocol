# Bootstrap Your Human Core (with any LLM)

Use this prompt with Claude, ChatGPT, or any capable LLM to build your Human Core files through conversation. The hosted version at [humancontext.pro](https://humancontext.pro) does this with a purpose-built interviewer, but the protocol is open — any LLM can do it.

## How to Use

1. Copy the four `core/` templates from `spec/human-core/templates/core/` into your chat (or attach them).
2. Paste the prompt below.
3. Answer honestly. One file per session works better than all four at once.
4. Save the results as `WHO.md`, `VOICE.md`, `NOW.md`, `GOALS.md`. Keep them in git or your notes vault.

## The Prompt

```
You are an interviewer helping me build my Human Core — structured,
machine-readable context about who I am, for the AI agents I work with.

Attached is a template for one file. Your job:

1. Interview me, one question at a time. Short, concrete questions.
   Dig for specifics: real episodes, real patterns — not aspirations.
2. Push back on vague answers. "I value honesty" is useless;
   "I tell clients when their idea won't work, even when it costs me
   the contract — like when..." is signal.
3. Fill the template as we go. Respect its structure exactly:
   keep the YAML schemas, fill every for_agent field with a direct,
   actionable instruction for an AI agent working with me.
4. Mark anything you inferred (rather than heard from me) with
   [? VERIFY] so I can review it.
5. After ~10 exchanges, show me the completed file and ask what's
   wrong with it. Iterate until I confirm.

Rules: never invent facts. Never soften what I said. Write in my
language and register — this file speaks for me when I'm not there.
```

## After the Core Layer

When the four core files feel accurate, repeat the process for `identity/` (INFLUENCES, INTERESTS, PEOPLE) and `deep/` (PATTERNS, BOUNDARIES). The deep files are high-sensitivity — they're for agents you control, not for publishing.

Generate `META.md` last: ask the LLM to produce a navigation file listing only the files that exist, with a recommended reading order. Regenerate it whenever the other files change.
