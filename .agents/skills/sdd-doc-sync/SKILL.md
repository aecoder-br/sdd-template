---
name: sdd-doc-sync
description: Documentation drift review for Spec Driven Design repositories. Use when Codex must compare README, AGENTS.md, docs, constitution, Spec Kit templates, skills, GitHub templates, and generated artifacts for contradictions or stale guidance.
---

# SDD Doc Sync

Use this skill to find documentation drift. Prefer precise file references and
small remediation suggestions.

## Review Order

1. Read `README.md` and `AGENTS.md`.
2. Read `.specify/memory/constitution.md`.
3. Read relevant `.specify/templates/` files.
4. Read docs under `docs/`.
5. Read local skill metadata under `.agents/skills/`.
6. Read GitHub templates under `.github/` when present.

## Checks

- Commands and skill names match installed metadata.
- Step ordering matches the current Spec Kit workflow.
- Governance rules do not contradict templates.
- Docs do not tell users to enable optional tooling by default.
- Templates remain stack-agnostic unless explicitly scoped.
- Public docs do not reference private context or secrets.

## Output

Return:

- contradictions and stale references;
- missing docs for new workflows;
- redundant docs that should be consolidated;
- exact files to update;
- validation commands to run after docs change.
