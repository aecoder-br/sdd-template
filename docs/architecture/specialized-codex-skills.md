# Specialized Codex Skills

Repo-local skills live under `.agents/skills/<skill-name>/`. Use them for
repeatable workflows that are important enough to preserve as project policy or
procedure.

## When to Create a Skill

Create a local skill when:

- the workflow will be repeated across features;
- the task has non-obvious standards or review criteria;
- the skill can reduce mistakes in security, QA, documentation, research, or
  domain work;
- the workflow should remain available to future agents.

Do not create a skill for a one-off note, a generic coding preference, or a
process that belongs directly in `AGENTS.md` or the constitution.

## Skill Shape

Keep skills small:

- `SKILL.md` is required and should contain only essential procedure.
- `agents/openai.yaml` should describe UI metadata and invocation policy.
- Use references or scripts only when they materially reduce repeated work.
- Avoid README, changelog, install guides, or extra docs inside skill folders.

## Invocation Policy

Use `policy.allow_implicit_invocation: false` for specialized review skills,
security skills, or skills with a risk of being triggered in the wrong context.
Explicit-only skills can still be invoked by asking Codex to use `$skill-name`.

Implicit invocation is acceptable only for broad, low-risk guidance that is
useful in most related tasks.

## Current Local Skills

- `sdd-research-senior`: source-backed research and implementation planning.
- `sdd-security-review`: security review of Spec Kit artifacts and diffs.
- `sdd-quality-review`: tests, clean code, SOLID, over-engineering, and DoD.
- `sdd-doc-sync`: drift checks across README, AGENTS, docs, and artifacts.
