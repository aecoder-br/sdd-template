---
name: sdd-research-senior
description: Source-backed research and implementation planning for Spec Driven Design work. Use when Codex must investigate current documentation, compare options, identify risks, synthesize sources, or produce a decision-ready plan before implementation.
---

# SDD Research Senior

Use this skill for read-only research that must become a concrete plan. Do not
edit files while using this skill unless the user separately asks for
implementation.

## Workflow

1. Establish the question, target repo, and active Spec Kit artifacts.
2. Read local sources first: constitution, spec, plan, tasks, README, AGENTS, and
   relevant docs.
3. Search official or primary sources for drift-prone facts.
4. Separate facts from recommendations.
5. Compare viable options with tradeoffs, risks, and rejected alternatives.
6. Produce a concise implementation plan with assumptions and validation.

## Source Standards

- Prefer primary sources: official docs, standards, repository files, ADRs, and
  project-owned docs.
- Label unverified memory or inference as such.
- Include retrieval date for external research when facts may drift.
- Avoid copying long source text; summarize and link.

## Output

Return:

- sources used;
- current local state;
- recommendation summary;
- prioritized changes;
- risks and non-goals;
- validation plan.
