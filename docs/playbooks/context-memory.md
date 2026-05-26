# Context and Memory Playbook

Persistent memory and retrieved context help agents stay consistent, but they
can also preserve stale or malicious instructions.

## Principles

- Use repository files as the primary source of truth.
- Treat memory as advisory unless verified against current repo state.
- Record provenance for durable decisions.
- Avoid storing secrets, personal data, credentials, or customer data.
- Prefer small, scoped notes over broad hidden instructions.

## Updating Durable Context

Add or update durable guidance only when:

- the user explicitly asks to preserve a rule;
- a repeated failure needs a project-local prevention rule;
- a workflow is stable enough to document;
- a decision belongs in an ADR, AGENTS.md, or docs.

Do not silently persist temporary preferences, one-off commands, or assumptions
that may become stale.

## Sanitization

Before copying context into docs, prompts, or memory:

- remove secrets and tokens;
- remove private customer data unless explicitly approved;
- summarize long logs instead of pasting raw output;
- label source, date, and confidence;
- verify drift-prone facts when cheap.

## Expiration and Revisit

Context should name when it becomes stale:

- version-dependent tooling;
- security policies;
- external API behavior;
- release workflows;
- performance numbers;
- organization ownership.
