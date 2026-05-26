# Agent Operating Rules

<!-- SPECKIT START -->
For additional context about technologies to be used, project structure, shell
commands, and other important information, read the current plan.
<!-- SPECKIT END -->

## Required Reading Order

Before implementing a feature, read the active artifacts in this order:

1. `.specify/memory/constitution.md`
2. `specs/<feature>/spec.md`
3. `specs/<feature>/plan.md`
4. `specs/<feature>/tasks.md`

If an artifact is missing, stop and use the matching Spec Kit skill to create or
repair it instead of guessing.

## Operating Mode

- Respect explicit read-only, review, research, or planning requests.
- Do not edit files while the user is asking for investigation or a plan.
- Keep changes scoped to the active feature, template, or documentation surface.
- Never revert user changes unless the user explicitly asks for that.
- Prefer small, reviewable commits grouped by intent when commits are requested.

## Spec Driven Development

- Keep `spec.md` focused on what users need and why.
- Put stack, architecture, dependencies, and implementation tradeoffs in
  `plan.md`.
- Generate `tasks.md` only after the specification and plan are consistent.
- Use `speckit-analyze` before implementation when requirements, design, or
  task coverage may be inconsistent.
- Treat the constitution gates as release gates, not suggestions.

## Tooling Safety

Ask for explicit human approval before:

- destructive filesystem operations;
- writing outside the workspace;
- pushing branches, creating releases, deploying, or publishing packages;
- mutating GitHub, issue trackers, cloud services, or production systems;
- exposing, rotating, or modifying secrets and credentials;
- installing or enabling new MCP servers, plugins, extensions, or presets.

Default to read-only access for external connectors. Any mutating connector
action must name the target, action, payload, and expected outcome.

## Subagents and Skills

Use subagents when the user explicitly asks for delegation or parallel research.
Keep delegated work bounded and independent: research, security review, QA,
quality review, or documentation drift checks are good candidates.

Prefer repo-local skills under `.agents/skills/` for reusable project workflows.
Use explicit-only invocation for specialized skills unless the skill is safe and
useful for broad automatic triggering.

## Validation

Before closing implementation work, run the validation named in the active plan.
For documentation/template changes, run at least:

```powershell
git diff --check
```

Record any skipped validation with the reason and residual risk.
