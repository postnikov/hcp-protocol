# Contributing to HCP Protocol

Thanks for your interest in shaping the future of professional identity.

## How to Contribute

### Share Your Ideas

- Open an **Issue** to suggest changes to the protocol, templates, or prompts
- Start a **Discussion** for broader topics about the future of resumes, hiring, and AI agents

### Share Your HCP Profile

We'd love to include diverse examples in `examples/`. To contribute:

1. Fork this repo
2. Create a folder in `examples/` with your name or alias
3. Include as many HCP files as you're comfortable sharing
4. **Anonymize** company names, colleague names, and any confidential details
5. Submit a PR

Your example doesn't need to be perfect — real profiles with rough edges are more useful than polished fiction.

### Improve Templates or Prompts

If you've used the templates and found something that could be better:

1. Fork → edit → PR
2. In your PR description, explain **what problem you hit** and **how your change fixes it**
3. If you're changing a template structure, explain why the new structure captures something the old one missed

### Propose New Context Add-ons

HCP supports context-specific extensions (like the Speaker context). If you have an idea for a new context:

1. Define 2-4 files that capture the context
2. Explain what questions they answer that the core profile doesn't
3. Submit a PR to `templates/` with the new context directory and an update to META.md

### Build Tools

The protocol is open. Build whatever you want on top of it:

- HCP viewers and renderers
- MCP server implementations (see the [7-tool MCP spec](https://humancontext.pro) for reference)
- CLI tools for generating or validating HCP files
- Integrations with LinkedIn, GitHub, or other platforms

If you build something, open an Issue or Discussion to share it — we'll link to community tools from the README.

## Guidelines

- Keep templates **universal** — they should work for a junior developer, a CEO, a freelance designer, and a researcher
- Prompts should be **AI-agnostic** — they should work with Claude, ChatGPT, Gemini, or any capable LLM
- Write for humans first, machines second — the protocol should be pleasant to read as plain text
- Respect privacy — never include real company names or personal data in examples without explicit consent

## Questions?

Open a Discussion or reach out to [Max Postnikov](https://www.linkedin.com/in/postnikov/).
